# Error Recovery

What to do when things go wrong during the pipeline. Covers image generation failures, assembly issues, and quality problems.

---

## Image Generation Failures

### Gemini returns no image
- **First:** Check that the prompt doesn't contain content policy triggers (nudity language, medical terminology that reads as graphic). Rewrite to avoid triggers while preserving intent.
- **Second:** Retry once with a simplified prompt — keep the core composition but strip secondary detail.
- **Third:** If still failing, proceed without the image. Insert the full prompt text as a placeholder with a note: "Image pending — generate externally with this prompt." The pipeline does not stop for image failure.

### Gemini returns an image but wrong aspect ratio
- Retry with explicit aspect ratio in the generation call.
- If the connector doesn't support aspect ratio control, note the discrepancy and proceed — the image can be cropped in post.

### Gemini returns an image but it looks off-brand
Run these checks against the four binding rules. You can evaluate based on the image description and generation parameters even without seeing the image yourself:

**1. Light check** — Did the prompt specify cool directional light with warm materials? If the prompt was correct but the image looks warm-lit (golden, amber, even), it's a generation drift problem. Regenerate with stronger light language: "cool-neutral hard directional light, single source upper left, NO warm light, NO golden hour."

**2. Chrome check** — Did the prompt describe chrome responsively (what it reflects on lit vs. shadow side)? If chrome looks flat or grey in the result, add more aggressive chrome language: "mirror-chrome reflects warm marble on lit face, cools to sharp silver on shadow face, accent ring catches as brightest point in frame."

**3. Closeness check** — Is the framing tight enough? Gemini tends to pull back to "product photography" default framing. If the image looks like a standard e-commerce shot (full bottle, centered, lots of negative space), regenerate with explicit framing: "crop tight — label fills 60% of frame" or "macro distance — cream texture fills frame edge to edge."

**4. Rose-warm axis check** — Are the materials in the correct color family (linen → sand → rose)? If the background is stark white, cool grey, or generic beige instead of the rose-warm axis, specify materials by name: "French linen surface (#FAF6F2), not white, not grey."

### When to give up on regeneration
After 2 regeneration attempts for the same image slot, stop. Deliver the best of what you have, flag the issue in the QA notes with the specific binding rule that failed, and include the prompt so the human can generate externally with a different tool (Midjourney, Ideogram).

---

## Assembly Failures

### HTML won't render correctly
- Check that Google Fonts (Albert Sans, Source Serif 4) are loaded via `<link>` tag, not `@import`.
- Check that PROVEN design tokens are applied from proven-ui/references/tokens.md — don't approximate colors or spacing.
- For email HTML: Klaviyo has rendering quirks. Use tables for layout, inline CSS, and avoid CSS grid/flexbox.

### Image won't composite into layout
- If the image is a base64 string from Gemini, convert to a hosted URL or file reference before inserting into HTML.
- If the image dimensions don't match the layout slot, note the mismatch and proceed with CSS `object-fit: cover` — flag for the human to review crop.

---

## Brand QA Failures

### QA score below 7 on any axis
- Do NOT regenerate the entire asset. Identify the specific element that failed:
  - **Customer axis low:** The copy isn't speaking to the audience's actual concern. Rewrite the headline and CTA using proven-voice, keeping everything else.
  - **Goal axis low:** The CTA doesn't match the campaign objective. Sharpen the CTA and check that the visual hierarchy leads to it.
  - **Brand axis low:** Something doesn't look or sound like PROVEN. Check: is the copy using filler language? Is the image generic (hotel bathroom test)? Are the design tokens wrong?
- Fix the specific failing element. Re-run QA on the fix only, not the whole asset.

### QA can't run (context too full)
- Deliver the asset without QA. Note clearly: "Brand QA skipped due to context limits. Run QA in a follow-up session by pasting the HTML and asking proven-brand-qa to score it."

---

## Context Window Degradation

Signs that context is getting too full:
- Responses get noticeably shorter
- Instructions from skills are being ignored or simplified
- Copy starts sounding generic (losing PROVEN voice specificity)
- Design tokens are approximated instead of exact

**What to do:**
1. Stop the current channel. Deliver what's complete.
2. Summarize what's done and what remains.
3. Suggest continuing in a new session: "Start a new Cowork task and say: Continue the [campaign name] — email is done, social posts remaining. Here's the narrative: [paste the master narrative]."
