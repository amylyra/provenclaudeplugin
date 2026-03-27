# PROVEN Prompt Validator

Post-planner, pre-emit QA layer. Run this after filling the planner slots, before the prompt text ships to a generator. The planner prevents most failures structurally — the validator catches what slips through.

---

## How to Use

After filling the planner checkpoint and drafting the prompt, run the hard checks first (binary pass/fail), then the soft checks (judgment calls). Fix any failures before emitting.

---

## Hard Checks — Mechanical, Binary

These are pass/fail. If any hard check fails, the prompt does not ship.

### Light Logic

- [ ] **One perceived source declared.** The prompt describes a single origin of light — one window, one direction, one gradient. If you can identify two competing light sources in the prompt text, it fails.
- [ ] **Shadow family agrees with source.** Shadows fall in one consistent direction, matching the declared light. Shadows on surfaces, shadows beneath objects, and shadows on chrome all agree.
- [ ] **Warmth is in materials, not light.** The prompt describes warm physical materials (marble, towel, ceramic, linen, cream, skin) and cool/neutral light. If the light itself is described as warm, golden, or amber, it fails.

### Chrome Logic (product-containing prompts only)

- [ ] **Chrome described responsively.** The prompt states what the chrome reflects on the lit side AND the shadow side. "Mirror-chrome metallic" alone fails. "Lit side glows with reflected marble warmth, shadow side sharpens to cool silver" passes.
- [ ] **Chrome is the most responsive surface.** If another surface in the prompt is described with more reflective detail than the chrome, it fails.
- [ ] **Seam highlight state declared.** The prompt explicitly states the accent ring as hero, present, or absent. Omission fails.
- [ ] **Label legibility declared.** Full, partial, or silhouette. Omission fails.

### Hero Event

- [ ] **One hero event identifiable.** Reading the prompt, you can point to the single main thing happening: label read, accent ring catch, texture peak, gaze, micro-expression. If two events compete for attention at equal weight, it fails.

### Composition Plausibility

- [ ] **Exact object count stated.** "One bottle," "three products," "two swipes." Not "a bottle," "products," "swipes."
- [ ] **Prop causality present (RITUAL).** Every non-PROVEN object has a verb of arrival or a reason to be there. If an object exists only for visual interest, it fails.
- [ ] **No full-room specification (RITUAL).** Surface + light + blur. If the prompt specifies wall color, tile pattern, architectural style, or room layout, it fails. The room is implied.

### Language Compliance

- [ ] **No Layer A brand words in emitted text.** Scan for: "intelligent," "premium," "adaptive," "signature," "anti-AI," "Apple-grade," "recognizable," "personalized" (as a descriptor of the image, not the product name). If any appear in the text that goes to the generator, it fails.
- [ ] **Positive-only by default.** Every negative in the prompt is either (a) a documented generator-failure override (symmetry, jar grounding) or (b) absent. Atmosphere negatives ("no kitchen," "no garden") fail unless they've been flagged as overrides with documented justification.

---

## Soft Checks — Judgment Calls

These are not binary. They catch drift, genericism, and AI tells. Flag concerns and suggest rewrites.

### The Hotel Bathroom Test

Read the prompt. Close your eyes. Does the image that forms feel like a real person's counter — with evidence of use, specific character, asymmetric arrangement? Or does it feel like a luxury hotel bathroom — pristine, symmetric, styled, generic? If hotel, flag and diagnose: is it the surface (too pristine?), the props (too decorative?), the light (too even?), or the composition (too centered?)?

### The Competitor Swap Test

Read the prompt. Replace "PROVEN" with "Curology" or "Function of Beauty." Does the prompt still work unchanged? If yes, the prompt is generic. Diagnose: what's missing that would make it specifically PROVEN? Usually the answer is chrome responsiveness (the chrome isn't described as alive), the warmth-carrier specificity (generic "warm tones" instead of named materials), or closeness (the camera isn't close enough to read).

### The AI-Smooth Test

Does the prompt describe a world where everything is equally perfect? Every edge sharp, every surface equally glossy, every object equally polished? Flag and inject imperfection: material wear on RITUAL objects, biological asymmetry on ingredients, uneven ridge depth on textures, skin texture variation on SKIN subjects.

### The Symmetric Spacing Test

Are objects described as evenly spaced, parallel to each other, or centered in frame? PROVEN compositions are asymmetric by design — off-center product placement, objects at the angle they landed, diagonal groupings. Flag any prompt that describes even spacing, centered composition, or parallel arrangement.

### The Gaze Test (SKIN only)

Does the prompt describe a person who is posing or a person who was caught? "Looking at the camera confidently" is posing. "Eyes soft, unfocused gentle gaze, the face between moments" is caught. If the subject sounds aware they're being photographed, flag it.

### The Fill-Light Test

Even though "one perceived source" allows shaping tools, does the *result* described in the prompt sound like it has competing light origins? "Lit evenly from all sides" sounds like fill. "Strong directional from the left, shadow side falls to soft darkness" sounds like one source shaped well. The prompt should describe the *look* of single-source light, not just declare it.

---

## Failure Response

**Hard check failure:** Do not emit. Fix the specific violation and re-run the check.

**Soft check flag:** Rewrite the flagged element. The prompt can ship after the rewrite, without re-running all checks — just verify the specific flag is resolved.

**Example — hard failure:**

Draft prompt: *"Golden sunlight floods a luxurious marble bathroom with neatly arranged objects beside a PROVEN bottle"*

Hard check failures:
- Light logic: warmth is in the light ("golden sunlight"), not materials
- Composition: "neatly arranged" = symmetric spacing
- No perceived source declared
- Chrome not described responsively
- No seam highlight state
- "Luxurious" = Layer A brand word

Rewrite direction: cool-neutral directional light from one window. Warm marble surface carries the warmth. Objects have verbs and angles. Chrome lit side reflects marble warmth, shadow side reflects cool room. Accent ring is the brightest point. Specify seam highlight state.

**Example — soft flag:**

Draft prompt passes all hard checks but the counter sounds like a hotel: pristine white marble, brass fixtures, perfectly folded towels, candle perfectly centered.

Soft flag: Hotel Bathroom Test. Diagnose: surface is too pristine (add veining, water ring near faucet), objects are too decorative (give the towel a verb — "bunched, damp, grabbed fast"), candle is centered (push off-center, wick trimmed with wax drip history).
