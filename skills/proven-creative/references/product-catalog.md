# PROVEN Product Photography — Prompt Generation

## Band: CHROME

**The product is the only event. The emptiness is the proof.**

This file operates in the **CHROME** band — the coolest, most controlled register in the system. CHROME says: this object is so precisely engineered, it doesn't need context. No counter, no life, no story. Just the object, a surface, and light. The restraint IS the statement.

Chrome responsiveness works differently here than in RITUAL. In a lifestyle scene, the chrome has a warm towel, a brass fixture, a teal dish — rich materials to reflect. In CHROME band, the chrome has almost nothing — a marble surface below, white studio above, cool directional light from one side. That simplicity makes the response *purer*: the lit side glows with the faintest warmth from the surface material, the shadow side sharpens to clean silver from the studio environment. Two realities on one surface, with nothing else competing for attention.

**The binding rules in CHROME:**

- **Precise light, warm materials:** Controlled studio light reveals the product. The surface material (marble, stone, concrete) carries the warmth. The chrome reads the split — warm below, cool above. That split is the image.
- **Chrome responds:** The governing execution law. Every prompt describes what's near the chrome and how it responds. On warm marble, it glows with reflected rose-gold. In pure white, it sharpens to clean silver. Against a hand, it catches skin warmth. Never static.
- **Closeness:** Tight to medium. Product fills 30–60% of frame. Close enough to read the etched label, resolve the accent ring, see the chrome's surface behavior.
- **Rose-warm axis:** The surface carries the palette (rose-gold veining in marble, cream linen edge), not the light. On pure white backgrounds, the chrome itself is the warmest element through its reflections.

**Post treatment:** Cleanest in the system. No visible grade. High key. Chrome reads true silver. Digital precision. Color-accurate. No film grain.

---

Generates prompts for external AI image generation tools (Midjourney, Ideogram, DALL-E). One product shot at a time. Output is always exactly 2 prompts.

**Prerequisite:** Read the hub `SKILL.md` first.

---

## Step 1 — Pre-Process

Before asking the user anything, read this entire file. It's structured to read top-to-bottom: pipeline → product data → prompt components → generator rules. Everything the prompt needs is here.

---

## Step 2 — Gather Information from User

Ask these questions using the `ask_user_input` tool. Skip any question the user already answered. Present options, never open-ended.

**Q1 — What kind of shot?**

| Option | Description |
|---|---|
| **Hero** | Product floating in space. Dramatic, airy. For big placements. |
| **Card** | Product upright, label-forward. Clean, functional. For grids and carts. |
| **Hand** | Hand interacting with product. Reaching or cradling. |
| **Shelf** | Product sitting on a surface. Grounded, stable. |
| **Close-Up** | Extreme macro. Label typography, chrome detail, or texture. |

*If user doesn't know,* ask where they'll use it:

| Channel | → Shot Type |
|---|---|
| Homepage hero / banner | Hero |
| PDP hero | Hero |
| PDP detail | Close-Up |
| Cart / checkout | Card |
| Quiz result | Card |
| Email header | Hero |
| Email product tile | Card |
| Social feed | Hero or Close-Up |
| Google Ads | Hero |
| Comparison | Card |
| Editorial / blog | Close-Up or Hero |

**Q2 — Which product(s)?**

| Single | Multiple |
|---|---|
| Cleanser | 3-Step System (Cleanser + Day Moisturizer + Night Cream) |
| Day Moisturizer with SPF | Full System (3-Step + Eye + Serum) |
| Night Cream | Custom combination |
| Eye Cream (Day) | |
| Eye Cream (Night) | |
| Serum | |

**Q3 — (Optional) Only ask if multiple products, hand, or close-up:**

| If Multi-Product | If Hand | If Close-Up |
|---|---|---|
| Dynamic / floating (different angles, overlapping) | Reaching down from above | The packaging (label, chrome rings) |
| Lineup / row (side by side, upright) | Cradling from below | The texture (cream, serum, foam) |
| Duo / tight (two products crossing) | | |

**Q4 — Background?**

| Option | Hex | Use |
|---|---|---|
| White (default) | Bright studio white | Standard — works everywhere |
| Warm white | #FAF6F2 | Pages with warm/linen backgrounds |
| Colored | User specifies | Campaign-specific |

---

## Step 3 — Analyze Layout

Determine the geometric composition before generating prompts.

**Single Hero:** Look up angle and feeling from the Product Angles table below. The form factor (tall cylinder vs. wide jar) dictates tilt range — taller products handle steeper tilts.

**Multi-Product Dynamic:** Plan the triangular arrangement:
- Height hierarchy: Cleanser tallest → Day Moisturizer medium → Night Cream shortest/widest
- Vary height, depth, and tilt across all products
- Jar floats at the same elevation as bottles, tilted at 25°
- At least two products overlap in depth while maintaining silhouette separation
- For Duo: tall + wide creates more contrast than tall + medium

**Multi-Product Lineup:** Left-to-right by routine order. All upright, identical poses, equal spacing.

**Hand — Reaching:** Hand enters from upper-right (bottles) or upper-left (jar). Bottles: pump exposed. Jar: lid intact.

**Hand — Cradling:** Palm enters from lower-right. Pump exposed.

**Close-Up Packaging:** Chrome accent ring at cap-body seam (bottles) or lid-body junction (jar) is the compositional anchor. Label text is the hero element.

**Close-Up Texture:** Cleanser → foam or gel. Moisturizer → cream swatch. Serum → oil drop. Night Cream → rich cream swatch.

---

## Step 4 — Determine All Parameters

Every parameter resolved from the tables and components below. Nothing left to chance.

| Parameter | How to Determine |
|---|---|
| **Angle** | Hero: from Product Angles table. Card/Shelf: upright (0°). Close-Up: tight crop. |
| **Feeling** | From Product Angles table. |
| **Lighting** | Hero/Close-Up Packaging: `LIGHTING-HERO`. Card/Shelf/Lineup: `LIGHTING-CARD`. Close-Up Texture: `LIGHTING-TEXTURE`. |
| **Shadow** | Hero: `SHADOW-HERO`. Card/Shelf: `SHADOW-CARD`. Close-Up: minimal or none. |
| **Background** | User's Q4 answer. Use `BACKGROUND-WHITE`, `BACKGROUND-WARM`, or user-specified. |
| **Cap/pump** | Hand shots → pump exposed. Everything else → cap on. |
| **Aspect ratio** | Hero single → 4:5 primary, 1:1 variant. Hero system → 16:9 primary, 4:5 variant. Card → 1:1. Close-Up → 1:1 primary, 4:5 variant. |
| **Negative space** | Hero single ~50% of frame. Hero multi ~60%. Card ~65% height. |
| **Product identity** | Single: full block. Multi: shared MATERIAL + ICON, per-product FORM + LABEL. |
| **Reference image** | From Reference Image table below. |

---

### Planner Checkpoint — Confirm Before Writing

Step 4 resolves most slots. Before moving to Step 5, confirm the core six plus CHROME-specific slots are filled:

| Core slot | Filled from |
|---|---|
| dominant_source | Lighting component (HERO / CARD / TEXTURE) |
| warmth_carrier | CHROME band: the surface material (marble veining, concrete warmth). On pure white: chrome reflections carry the warmth. |
| camera_distance | Shot type → lens + framing from Step 4 |
| focus_hierarchy | Shot type determines: Hero → product silhouette. Card → label. Close-Up Packaging → accent ring + label text. Close-Up Texture → material peak. |
| chrome_presence | Always present and responsive in this band |
| hero_event | Shot type determines: Hero → the floating object. Card → the readable label. Close-Up → the detail being magnified. |

| CHROME slot | Filled from |
|---|---|
| chrome_response | Lit side: warm glow from surface material. Shadow side: cool silver from studio environment. State for this shot: ______ |
| seam_highlight | Hero/Card: present. Close-Up Packaging: hero (the anchor). Close-Up Texture: absent. |
| label_legibility | Hero: partial (angled). Card: full (front-facing). Close-Up Packaging: full (the subject). |
| surface_type | Background selection from Q4: white / warm white / colored. Shelf: the surface material. |

All filled → proceed to Step 5.

---

## Step 5 — Generate Exactly 2 Prompts

**Layer C from here forward.** Everything above this point is Layer A (brand law) and Layer B (planner decisions). The prompt text below is Layer C — only pixel-driving language enters the generator. Use the hub's translation table if you catch yourself reaching for brand-strategy words.

Assemble each prompt in this order (generators weight earlier content more heavily):

1. **REFERENCE IMAGE block** — verbatim from Prompt Components below
2. **SHOT block** — from the matched Shot Template, filled with Step 4 parameters
3. **PRODUCT IDENTITY block(s)** — from Product Identity templates
4. **BACKGROUND line**

**The 2 prompts must differ in one visual parameter:** different aspect ratio, different angle, or different crop. Not just different wording.

**After both prompts, include:**
- Which reference image to attach (from Reference Image table)
- One line on what's different between the two prompts

**Format each prompt as a single code block** the user can copy-paste directly into their image generation tool. **Expand all bracket references** — replace every `[LIGHTING-HERO]`, `[SHADOW-HERO]`, `[GEOMETRIC PRECISION]`, `[RENDER]`, and `[BACKGROUND]` with the actual verbatim text from the Prompt Components section. The final prompt the user sees must be fully self-contained with zero placeholder brackets.

---
---

## Product Data

### Packaging Forms

| Product | Form | Geometry | Volume |
|---|---|---|---|
| Cleanser | Tall pump bottle, mirror-chrome | Perfect tall cylinder, ~1:4 (width:height). Cap is shorter cylinder atop body — junction is precise horizontal ring with chrome accent. Tallest in system. | 50 ML / 1.7 FL. OZ. |
| Day Moisturizer | Medium pump bottle, mirror-chrome | Perfect medium cylinder. Same geometry, shorter. Slightly wider proportions. | — |
| Night Cream | Low wide jar, mirror-chrome body + lid. Embossed hexagon icon on lid center. | Low wide cylinder topped by flat disc lid, ~2:1 (width:height). Lid-body junction: precise horizontal ring with chrome accent. | 30 ML / 1 FL. OZ. |
| Eye Cream (Night) | Small low jar, mirror-chrome, no embossed lid icon | Small low cylinder, same geometry as Night Cream, smaller scale. | — |
| Eye Cream (Day) | Small low jar, **matte silver** (only matte product) | Same form as Night Eye Cream, matte finish. | — |
| Serum | Short wide pump bottle, mirror-chrome | Short wide cylinder with pump. Shorter and wider than Day Moisturizer. | — |

### Label Text (Exact)

| Product | Label Text |
|---|---|
| Cleanser | PERSONALIZED CLEANSER |
| Day Moisturizer | PERSONALIZED DAY MOISTURIZER with broad spectrum SPF 40 sunscreen |
| Night Cream | PERSONALIZED NIGHT CREAM |

All labels: white on chrome. Hierarchy: Hexagon icon → "PROVEN" wordmark → Product name → Volume.

### Product Angles & Feeling

| Product | Hero Angle | Feeling | Notes |
|---|---|---|---|
| Cleanser | 35° diagonal | Effortless authority. Tall and commanding. | Steepest tilt — tall form handles it. |
| Day Moisturizer | 30° diagonal | Precise, ready. The daily companion. | Moderate tilt. Keep size difference from Cleanser visible. |
| Night Cream | 25° diagonal | Grounded and substantial even while floating. | Shallowest — keeps embossed lid icon visible. |

### Reference Images Needed

| Shot Type | Attach This |
|---|---|
| Hero single | Clean front-facing studio shot of that product. Cap on, label visible. |
| Hero system | Photo showing all products together with correct size ratios. |
| Hand (pump exposed) | Photo of that product with cap removed, pump mechanism visible. |
| Hand (jar) | Photo of Night Cream jar showing lid with embossed icon. |
| Close-Up packaging | Close-up where label text and chrome accent ring are clearly visible. |
| Close-Up texture | Not needed — no packaging in frame. |
| Card | Same as Hero single — front-facing, label fully visible. |

---
---

## Prompt Components

One source of truth for every piece of language that goes into a prompt. Use these verbatim — do not paraphrase or blend with other sections.

### REFERENCE IMAGE Block

Every prompt starts with this, verbatim:

```
REFERENCE IMAGE:
A reference image of the exact product is attached. This is the sole source of truth for shape, proportions, label layout, label text, icon, typography, and finish. Every edge, seam, radius, and surface transition must match the reference. If any instruction below conflicts with the reference image, the reference image wins.
```

### MATERIAL Block — Single Product

```
MATERIAL: Mirror-chrome metallic — luminous polished silver. Lit side glows with reflected warmth from the surface below. Shadow side sharpens to cool silver, still reflective. Chrome accent rings are the brightest, sharpest elements — the crispest marks in the frame.
```

### MATERIAL Block — Multi-Product (Shared)

Use once for all products. Do not repeat per product.

```
MATERIAL (all products): Mirror-chrome metallic — luminous polished silver. Each product's lit side glows with reflected warmth from the surface below. Shadow sides sharpen to cool silver, still reflective. Chrome accent rings at seams, collars, and junctions are the brightest elements — razor-thin lines of concentrated white. Every cap-to-body seam: crisp horizontal ring. Cylinder walls true. Cap and lid edges: clean circles in perspective.
```

### ICON Block — Shared

Use once per prompt, after all product blocks.

```
ICON: Hexagon with small circles at each vertex, resembling a molecular structure diagram. White. Geometrically precise. Match reference.
```

### LIGHTING-HERO

```
LIGHTING: Dominant directional key light from upper-left. White studio environment provides ambient fill, keeping chrome luminous polished silver across full surface. Chrome responds: warm glow from the surface side, clean sharpening from the light side. Bright, clean, precise.
```

### LIGHTING-CARD

```
LIGHTING: Soft, even, diffused. Luminous silver throughout.
```

### LIGHTING-TEXTURE

```
LIGHTING: Soft even diffused light from above — clinical, shadowless ambient illumination.
```

### SHADOW-HERO

```
SHADOW: Soft graduated cast shadow beneath — directional, offset lower-right.
```

### SHADOW-CARD

```
SHADOW: Minimal contact shadow beneath.
```

### GEOMETRIC PRECISION (one line, every prompt)

```
GEOMETRIC PRECISION: Cap-body seam crisp horizontal ring. Chrome accent rings razor-thin — brightest elements. Cylinder walls true. Cap/lid edges clean circles in perspective.
```

### RENDER (one line, every prompt)

```
RENDER: Ultra-high resolution. Every label character legible. Every chrome accent ring resolved. Medium-format precision.
```

### BACKGROUND-WHITE

```
BACKGROUND: Bright, luminous white. Open, airy. The bright environment reflects into the chrome, keeping bottles luminous. The product is the only content in the frame.
```

### BACKGROUND-WARM

```
BACKGROUND: Warm white (#FAF6F2). Softens the studio feeling while preserving chrome reflectivity. The product is the only content in the frame.
```

### PRODUCT IDENTITY — Per-Product Template

For single-product prompts, include MATERIAL + LABEL + ICON. For multi-product, include only FORM + LABEL (shared MATERIAL and ICON used once).

```
PRODUCT: PROVEN Personalized [Name]. [Form from table]. Mirror-chrome. [Cap on / Pump exposed].
FORM: [Geometry from table].
LABEL: White on chrome. Hexagon icon above "PROVEN" wordmark, then "[LABEL TEXT from table]", then "[VOLUME]".
```

Night Cream always adds:
```
LID: Hexagon molecular icon embossed on lid center — raised relief catching the light.
```

---
---

## Shot Templates

Fill the brackets from Step 3/4 parameters. Use the Prompt Component blocks above for MATERIAL, LIGHTING, SHADOW, GEOMETRIC PRECISION, RENDER, and BACKGROUND — copy them verbatim.

### Hero — Single Product Floating

```
SHOT: Hero / editorial. Single [bottle/jar], one product only. Floats in mid-air — no surface beneath it.
COMPOSITION: Apple product photography. One precision object in considered space. Negative space is intentional — ~50% of frame. The product is the only content.
Product floating at [angle]° diagonal tilt toward camera. Label [partially visible / facing camera]. Wordmark and icon sharp.
[SHADOW-HERO]
[LIGHTING-HERO]
[GEOMETRIC PRECISION]
[RENDER]
Feeling: [feeling from table].
Aspect ratio: [ratio]
Photorealistic. Bright studio lighting.
```

### Hero — Multi-Product Dynamic

```
SHOT: Hero / editorial, multi-product system. Exactly [count] products in frame. Every product — including jars — suspended in mid-air. No surface beneath any product.
COMPOSITION: Apple product photography. Every pixel intentional. Space between objects is architecture. Each product legible on its own. The product is the only content.
Products: [list with forms and relative sizes]
- Loose triangular arrangement, not centered, not symmetrical. Open, airy.
- 15-20% of each product's width as clear gap. Products occupy ~60% of frame.
- Every product at different height, depth, tilt. No two parallel.
- [If jar:] THE JAR IS FLOATING IN MID-AIR at same height as bottles — tilted, airborne, suspended.
- At least two products overlap in depth. Each silhouette sharp and traceable even where overlapping.
- Formation reads as precision instruments paused mid-arrangement.
[SHADOW-HERO — beneath each product]
[LIGHTING-HERO]
[GEOMETRIC PRECISION]
[RENDER]
Aspect ratio: [ratio]
Photorealistic. Bright studio lighting.
```

### Hero — Duo Tight

```
SHOT: Hero / editorial, tight composition. Two [bottles/products] in frame. Dramatically composed.
COMPOSITION: Two products overlap at crossing angles, filling ~70% of frame. One sharp in foreground, other slightly softer behind. Each silhouette sharp and readable even where overlapping. Chrome surfaces faintly reflect each other.
[SHADOW-HERO]
[LIGHTING-HERO]
[GEOMETRIC PRECISION]
[RENDER]
Aspect ratio: [ratio]
Photorealistic. Bright studio lighting.
```

### Card — Single Product

```
SHOT: Product card. Single [bottle/jar], one product only.
COMPOSITION: Upright, centered, label facing camera. Fully readable. ~65% frame height.
[SHADOW-CARD]
[LIGHTING-CARD]
[GEOMETRIC PRECISION]
[RENDER]
Background: [BACKGROUND]
Aspect ratio: [ratio]
Photorealistic.
```

### Card — Lineup

```
SHOT: Product lineup. [Count] products in a clean horizontal row.
COMPOSITION: All products upright, identical poses, left-to-right by routine order. Equal spacing. Label fully readable on each. Products occupy ~80% of frame width.
[SHADOW-CARD — beneath each]
[LIGHTING-CARD]
[GEOMETRIC PRECISION]
[RENDER]
Background: [BACKGROUND]
Aspect ratio: 16:9
Photorealistic.
```

### Shelf — Single Product

```
SHOT: Product on surface. Single [bottle/jar], one product only. Product sits on a clean white surface.
COMPOSITION: Product upright on surface, label facing camera. Readable. Grounded, stable. ~55% of frame.
SHADOW: Natural cast shadow on surface — directional, offset lower-right, soft edges.
[LIGHTING-HERO]
[GEOMETRIC PRECISION]
[RENDER]
Aspect ratio: [ratio]
Photorealistic. Bright studio lighting.
```

### Hand — Reaching Down

```
SHOT: Hero with hand. Single [bottle/jar], one product only. [Cap removed, pump exposed — chrome mechanism with small white actuator button. / Jar on clean white surface, lid intact.]
COMPOSITION: [Bottle floating / Jar on surface], label facing camera. Hand enters from [upper-right / upper-left], reaching down — fingers spread, about to [grasp near pump / touch lid]. Warm medium skin, clean nails, no jewelry. Mid-reach, incidental. Hand partially cropped. Generous negative space. The product is the only content besides the hand.
[SHADOW-HERO or surface shadow]
[LIGHTING-HERO]
[GEOMETRIC PRECISION]
[RENDER]
Feeling: Deliberate. Effortless ownership.
Aspect ratio: 4:5
Photorealistic. Bright studio lighting.
```

### Hand — Cradling from Below

```
SHOT: Hero with hand. Single bottle, one product only. Cap removed, pump exposed — chrome mechanism with small white actuator button.
COMPOSITION: Bottle upright, label facing camera. Open palm enters from lower-right, cradling from beneath — fingers relaxed, slightly curved upward. Warm medium skin, clean nails, no jewelry. Effortless. Wrist partially cropped. Generous negative space above. The product is the only content besides the hand.
SHADOW: Minimal — hand provides grounding.
[LIGHTING-HERO]
[GEOMETRIC PRECISION]
[RENDER]
Feeling: Effortless ownership. Precious, confident.
Aspect ratio: 4:5
Photorealistic. Bright studio lighting.
```

### Close-Up — Packaging (Label Detail)

```
SHOT: Extreme tight crop. Single [bottle/jar], one product only. Label typography is the compositional focal point.
COMPOSITION: Product fills 80% of frame. Crop centers on label zone — product name and wordmark dominate. Chrome accent ring at [cap-body seam / lid-body junction] intersects upper frame as compositional anchor. Icon and "PROVEN" wordmark fully visible and sharp. Cap, base, and most of cylinder beyond label zone outside frame. The product is the only content.
SHADOW: None given crop.
[LIGHTING-HERO]
GEOMETRIC PRECISION: Label characters individually resolved — every letterform sharp. Chrome accent ring: distinct razor-thin bright line. Cylinder curvature smooth and true.
RENDER: Ultra-high resolution macro. Label text readable at any output size. Medium-format precision.
Aspect ratio: [ratio]
Photorealistic macro. Bright studio lighting.
```

### Close-Up — Texture

```
SHOT: Overhead macro. [Texture type — e.g., cream swatch mid-spread / serum drop / foam]. Material dispensed on surface.
COMPOSITION: Material fills frame, shot from directly above. White space visible on all four edges, material slightly off-center. The material's own behavior (spread edge, viscosity, grain) is the subject.
[LIGHTING-TEXTURE]
SHADOW: Faint contact shadow beneath material only.
RENDER: Ultra-high resolution macro. Medium-format precision.
The material was just applied — spread edge irregular, real behavior not digitally perfected.
Aspect ratio: [ratio]
Photorealistic macro.
Background: Pure white seamless.
```

---
---

## Generator Rules

### How Generators Read Prompts

1. **Cannot negate.** "Not dark" injects "dark." Only describe what something *is.*
2. **Front-load the shot.** Composition + count in the first 50 words.
3. **State the count.** "Single bottle, one product only." Otherwise generators duplicate.
4. **Say it once, vividly.** Repetition dilutes. One vivid description beats three cautious ones.
5. **Describe, don't name.** "Hexagon with small circles at each vertex" not just "hexagon icon."
6. **Chrome brightness trap.** "Deep shadow" and "dark silver" → generators render dark bottles. Use "deeper silver, still reflective." Always include ambient fill from white studio.
7. **Jars sink.** Generators ground jars on surfaces. Use: "THE JAR IS FLOATING IN MID-AIR — tilted, airborne, suspended."

### Common Failures

| Failure | Cause | Fix |
|---|---|---|
| Dark bottles | "Deep shadow," "near-black," "mostly shadow" | "Deeper silver, still reflective." Include ambient fill. |
| Jar grounded while bottles float | Generators default to grounding wide objects | Jar-specific: "FLOATING IN MID-AIR — tilted, airborne, at same height as bottles." |
| Soft/blurred seams and rings | No geometric precision language | "Cap-body seam crisp horizontal ring. Chrome rings razor-thin." |
| Products clustered in center | No negative space spec | "Products occupy ~60%. 15-20% gap between products." |
| Silhouettes merge where overlapping | No separation language | "Each silhouette sharp and traceable even where overlapping." |
| Flat lighting on hero shots | "Soft" or "even" in hero context | "Dominant key light + white studio ambient fill." Soft/even for cards only. |
| Hard-edged cast shadows | "Hard light = hard shadows" logic | "Softly graduated edges." Ambient fill softens shadows. |
| Wrong product proportions | Generator invents sizes | "Cleanser tallest. Day Moisturizer shorter. Match reference height ratio." |
| Label garbled | Generator doesn't prioritize text | "Every label character legible. Every letterform sharp." For label detail: make it the focal point. |
| Packaging invented | No reference image or wrong one | Always attach matching reference. See Reference Images table. |
| Generic beauty feel | Missing Apple philosophy + precision | Front-load "Apple product photography." Include geometric precision. "Product is the only content." |
