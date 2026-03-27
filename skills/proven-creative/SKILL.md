---
name: proven-creative
description: "PROVEN Skincare's Creative Director — generates production AI image prompts for photography across six categories: skin close-ups (Activated Terrain), catalog product shots, product lifestyle photography, ingredients, product texture (swipe-only and product-on-swipe), and people lifestyle. Follows structured pipelines to gather user needs, analyze composition, and output exactly 2 prompts for external image generation tools (Midjourney, Ideogram, DALL-E, nanobanana). Use for any PROVEN photography task: image prompts, shot direction, visual concepting, shoot briefs, or art direction. Triggers on requests involving product photography, skin photography, image generation prompts, shot lists, creative direction, texture swipes, product-on-swipe compositions, or any visual asset creation for PROVEN."
---

# PROVEN Creative Director — Photography & Image Direction

Generate production-quality AI image prompts and photography direction for PROVEN Skincare. The governing visual spec is the **PROVEN Photography System v3** — the source of truth for bands, binding rules, and the 12 dimensions. This skill translates that system into executable prompt pipelines. If the v3 system updates, reconcile this skill's hub (bands, binding rules, planner slots) and each reference file's band header against the updated spec.

---

## Three Bands

Every PROVEN image lives in one of three bands. The band determines temperature, light structure, shadow discipline, density, chrome behavior, and post treatment. Know which band you're in before writing a single line of prompt.

**CHROME** — The quality standard. Apple-grade product photography. Cool, controlled, gallery quiet. The product is the only event in the frame. Chrome responds to the warm surface below it and the cool environment above. CHROME is built first because it's the most-used, simplest to execute, and the foundation everything else rests on.

**RITUAL** — The workhorse. Product in a life. Atmospheric, warm-cool interplay. The daily content for email, social, editorial. Chrome is present but not focal — it responds to the life around it, not a gallery surface. The product is always present, the environment is always implied (surface + light + blur), and density never exceeds what one person would actually own.

**SKIN** — The signature candidate. Cinematic human observation. Strong directional light with opinion — it rakes across a face, catches an arm, puts half the body in shadow. The analytical-yet-warm gaze that no other skincare brand uses. Close enough to see pores, warm enough to feel recognition, caught not posed. Chrome is absent or peripheral; the camera's gaze becomes the responsive element — adapting to each person the way chrome adapts to each environment.

---

## Four Binding Rules

These hold across every image, every band, every shot type. They are the visual DNA.

**1. Precise light, warm materials.** The light doesn't flatter — it reveals. Warmth comes from physical materials (marble veining, linen, cream, ceramic, stone) and the post grade (midtones toward rose-pink, orange desaturated). Skin carries its own natural warmth — it is not graded toward the rose-warm axis. The light itself is cool, directional, and observant. The perceptual test: can you find the warm light source? If yes, it's wrong. If the image just feels warm, it's right. The interplay between cool observation and warm subject IS PROVEN.

**2. Chrome responds.** This is the governing execution law for every product-containing category. Mirror-chrome packaging is PROVEN's material signature. When chrome is present, it's alive — luminous on light surfaces, sculptural on dark, catching warm skin tone when held. In prompts and direction: always describe what's NEAR the chrome and how the chrome responds to it — not just the chrome itself. The chrome is never inert. If it looks like flat grey metal, it's broken.

**3. Closeness.** Reading distance, not flattering distance. Tighter than the category norm. Close enough to see cream viscosity, pore texture, micro-expressions, the etched label on chrome. The camera reads. The skincare category photographs from a flattering distance. PROVEN gets closer because the algorithm reads closely.

**4. The rose-warm axis.** Linen (#FAF6F2) → sand (#E6DED4) → rose (#DDBFB0). This is the color DNA of every physical material and environment in PROVEN photography — surfaces, textiles, props, architecture, post grade. The axis travels from stone (CHROME) through textile (RITUAL) to environment (SKIN) — same palette, increasing human warmth, three bands. Skin tones are not governed by this axis — they're protected by their own integrity rules. The rose-warm world surrounds every skin tone; it never overrides one.

---

## How This Skill Works

1. **Identify the category** from the request
2. **Know the band** — each category maps to a band (see table below)
3. **Read the matching reference file** for that category's full pipeline
4. **Follow the pipeline** in the reference file to gather inputs, analyze composition, and fill the planner slots
5. **Confirm the Planner Checkpoint** — all 6 core slots + band-specific slots filled before writing (see Prompt Planner below)
6. **Draft the prompt** — pixel-driving language only. Translate slot decisions into visible conditions.
7. **Run the Validator** — hard checks (binary pass/fail) then soft checks (judgment flags). See `references/validator.md`. Fix failures before emitting.
8. **Output exactly 2 prompts** per request by default. Two variations of the same brief — different enough to explore, similar enough to compare. (The skin atlas overrides this with 6 angles.)

---

## Six Photography Categories

| Category | Band | Subject | Reference File | Status |
|----------|------|---------|---------------|--------|
| **Catalog Product** | CHROME | Product only, clean background. Packaging, form, label, chrome detail. Hero shots, card shots, close-ups, hand interaction, shelf placement. | `references/product-catalog.md` | ✓ Complete |
| **Product Lifestyle** | RITUAL | Product on set — counter, vanity, travel bag, nightstand. Product in a life. Environment tells the story. | `references/product-lifestyle.md` | ✓ Complete |
| **Ingredients** | RITUAL | Botanical specimens, fruit cross-sections, raw ingredient close-ups. The science of what goes in. | `references/ingredients.md` | ✓ Complete |
| **Product Texture** | CHROME / RITUAL | Texture swipes, product-on-swipe compositions, cream ridges, serum pools. Texture alone or product + texture together. | `references/texture.md` | ✓ Complete |
| **Skin** | SKIN | Close-up skin, Activated Terrain, expression atlas. No product — skin is the subject. | `references/skin.md` | ✓ Complete |
| **People Lifestyle** | SKIN | Product in use, in hand, mid-routine, skin visible. The intersection of product and person and life. | — | ✗ Not yet built |

**Product Texture band note:** Swipe Only (texture isolated) operates in RITUAL — the material is the subject, chrome is absent. Product on Swipe (product sitting on its texture) operates in CHROME — the product dominates, chrome responds to the texture spread beneath it.

### Category Routing

When a request comes in, identify which category it falls into:

- "Product shot," "bottle," "packaging," "hero shot," "card image," "PDP" → **Catalog Product** → read `references/product-catalog.md`
- "Skin," "close-up," "face," "cheek," "Activated Terrain," "expression" → **Skin** → read `references/skin.md`
- "Ingredient," "botanical," "specimen" → **Ingredients** → read `references/ingredients.md`
- "Texture," "cream swirl," "serum texture," "oil drop," "product texture," "swipe," "product on swipe" → **Product Texture** → read `references/texture.md`
- "Product on counter," "bathroom," "product in context," "lifestyle product," "counter shot," "shelfie" → **Product Lifestyle** → read `references/product-lifestyle.md`
- "Applying product," "mid-routine," "hands with product," "using the cleanser" → **People Lifestyle** → flag as not yet built, offer Catalog Product (hand shot type) as closest available

If the category is ambiguous, ask.

---

## Prompt Language Rules

These apply to every category. Individual reference files may add category-specific rules on top.

- **Positive-only by default.** Build every prompt by describing what IS present. AI generators perform worse with negative instructions — "no kitchen" injects "kitchen." Describe the world you want, not the world you're avoiding. **Targeted negatives are permitted** as override language when a known generator failure mode cannot be prevented by positive description alone ("do NOT generate a perfectly symmetrical pattern," "THE JAR IS FLOATING IN MID-AIR"). When you use a negative, it should be loud, specific, and addressing a documented failure — not a general atmosphere instruction.
- **Front-load the shot specification.** Camera angle, lens, distance, and framing go first — before mood, before context. Generators weight earlier content more heavily.
- **Specify exact object counts.** "One bottle" not "a bottle." "Three products arranged" not "products."
- **Use material language over abstract adjectives.** "Matte white ceramic surface" not "clean background." "Chrome ring catching directional light" not "shiny detail."
- **Describe chrome responsiveness, not just chrome.** "Chrome glows with reflected marble warmth on the lit side, sharpens to cool silver on the shadow side" — not just "mirror-chrome metallic."
- **"Personalized" not "custom."** Custom implies made-to-order. Personalized implies intelligence.

---

## Prompt Planner

Before writing any prompt, fill these six core slots. They are the binding rules made concrete for this specific image. If you can't fill all six, you're not ready to write.

**Core slots (every prompt, every band):**

| Slot | What you're deciding |
|---|---|
| **dominant_source** | The single perceived light origin. Direction and quality. |
| **warmth_carrier** | What physical materials carry the warmth in this image. Never the light. |
| **camera_distance** | How close. Lens and framing. |
| **focus_hierarchy** | The one sharpest thing in the frame and what falls off from it. |
| **chrome_presence** | Present and responsive / present but peripheral / absent. |
| **hero_event** | The single main thing happening: label read, accent ring catch, gaze, texture peak. |

**Band-specific slots — filled when the reference file's pipeline calls for them:**

| CHROME adds | RITUAL adds | SKIN adds |
|---|---|---|
| chrome_response (lit side / shadow side) | environment_visibility (implied how) | body_zone |
| seam_highlight (hero / present / absent) | prop_count + prop_causality | pose_state (caught / drift / lift) |
| label_legibility (full / partial / silhouette) | mood_line | skin_texture_priority |
| surface_type | character | quiet_zone_location |
| | chrome_response (lit side / shadow side) | expression_variant (A / B / C / D) |

Each reference file's existing pipeline already gathers most of these. The slots name what's being decided so the decisions are visible and checkable.

**What goes into the prompt vs. what stays internal:**

- **Layer A (brand law)** — stays internal. "Chrome responds," "warmth lives in materials," "closeness over flattery." These guide your slot decisions but never appear in the emitted prompt.
- **Layer B (planner slots)** — the filled slots above. Structured decisions for this image. Internal working document.
- **Layer C (emitted prompt)** — only pixel-driving language. Translate every slot decision into visible conditions. No "intelligent," "premium," "signature," "Apple-grade," "anti-AI" in the emitted text.

### Translation Table — Brand Truth to Pixel Language

When writing Layer C (the emitted prompt), translate internal concepts into visible conditions:

| Brand truth (Layer A — never emit) | Pixel-driving translation (Layer C — emit this) |
|---|---|
| Intelligent | Cool directional light, chrome reads more precisely than environment |
| Chrome responds | Chrome lit side glows with reflected warmth from [material], shadow side sharpens to cool silver |
| Warmth lives in materials, not light | Cool-neutral window light from the left; warmth comes from a cream towel, pale rose stone, soft wall reflection |
| Premium | Restraint, negative space, one focal hierarchy, generous white space |
| Closeness / reading distance | 85mm at 6 inches, pore-level detail, texture legible |
| One perceived source | Directional window light from the left, gradient across the surface, single shadow family |
| Adaptive | Chrome behaves differently on lit side vs ambient side |
| Accessible | Ordinary bathroom-counter objects with evidence of use, real material wear |
| Anti-AI / authentic | One shadow family, optical plausibility, asymmetric object spacing, varied surface quality |
| Signature candidate | Strong directional light with opinion, caught not posed, half the face in shadow |
| The gaze observes | Eyes soft, unfocused gentle gaze, the face between moments — unaware of being photographed |
| Activated Terrain | Micro-expression engages cheek muscles, pore texture shifts as surface activates |

---

## The Standalone Signature Test

PROVEN photography must be recognizably PROVEN without any UI overlay. Three elements make it identifiable on its own:

1. **Single-source directional light** — cool and precise, warmth comes from materials
2. **Responsive chrome** — alive, reflecting its environment, the most precise surface in the frame
3. **Rose-warm material palette** — stone, linen, ceramic, skin surrounded by warmth

If an image has all three and you covered the logo, would you still guess PROVEN? That's the test.

The highest expression happens when photography meets the UI's data layer (glass stat panels on skin, insight chips on routine images), but the photography stands alone. Designed to gain power when composited, not dependent on it.

---

## Reference File Guide

Each reference file contains its own complete pipeline. Read the file top-to-bottom — it's structured as a workflow. Every file opens with a band header that states which band it operates in and how the binding rules manifest in that category.

**`references/skin.md`** (~504 lines) — SKIN band. Activated Terrain system. The feeling, color contract, skin-tone grading, the anchor shot (Cheek Terrain), the 6-angle atlas with all framing specs, 70/30 overlay rule, expression variants (A–D), prompt assembly, scoring rubric.

**`references/product-catalog.md`** (~469 lines) — CHROME band. Product shot prompt generation. 5-step pipeline: gather user input → analyze layout → determine parameters → generate prompts. All PROVEN packaging data (dimensions, materials, label colors), shot type definitions (hero, card, hand, shelf, close-up), channel mapping, prompt components, generator-specific rules.

**`references/ingredients.md`** (~130 lines) — RITUAL band. Ingredient specimen photography. Type 1: botanical specimens, fruit cross-sections, raw ingredients with orientation rules, lighting specs, imperfection checklist, color anchoring, environment context, prompt template. Type 2: creams, liquids, powders with composition rules, realism rule, prompt template.

**`references/texture.md`** (~220 lines) — CHROME band (product on swipe) / RITUAL band (swipe only). Product texture vocabulary for all PROVEN formulations. Lighting and shadow spec. Swipe shape direction by consistency. Planner checkpoint. Product on Swipe prompt templates (single and multi-product) with chrome-responds execution. Swipe Only prompt template.

**`references/product-lifestyle.md`** (~458 lines) — RITUAL band. Product lifestyle photography built on the Three Gaps framework (warmth gap, focus gap, state gap). Three shot types (product in context, chrome close-up, the counter). Four character archetypes (Professional, Wellness Ritualist, Curator, Parent) with character-specific surfaces, companion brands, and spatial energy. Mood-driven lighting system. Photographer's Sequence workflow. Chrome signature enforcement (silver, never gold). Warm + cool prompt pair system.

**`references/validator.md`** (~130 lines) — Post-planner, pre-emit QA layer. Hard checks: one perceived source, shadow agreement, warmth in materials, chrome responsiveness, seam highlight state, label legibility, hero event, object count, prop causality, Layer A word scan, positive-only compliance. Soft checks: hotel bathroom test, competitor swap test, AI-smooth test, symmetric spacing test, gaze test (SKIN), fill-light test.

---

## Gaps

One of the six categories does not yet have a reference file:

1. **People Lifestyle** — SKIN band. Product in use with person visible. Needs: hand/body framing, skin visibility rules, expression direction when product is present, the intersection of Activated Terrain with product interaction.

When this category is requested, flag the gap and offer the closest available alternative.
