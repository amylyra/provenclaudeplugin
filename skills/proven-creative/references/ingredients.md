# PROVEN Ingredient Photography

## Band: RITUAL

**The evidence. Proof that the formula's intelligence is grounded in real materials.**

Ingredient photography operates in the **RITUAL** band as evidence shots. They appear alongside lifestyle images in emails, PDPs, and editorial. The white-seamless background is a deliberate divergence from RITUAL's typical surface-and-blur world: specimens require isolation to read as catalogued evidence, not styled props.

**How the binding rules manifest here:**

- **Precise light, warm materials:** Single directional light reveals the specimen's structure. The material's own color carries all the warmth — turmeric's deep orange, chamomile's white petals, grapefruit's blush pink. The light stays cool and observational. The environment is clinical neutral.
- **Chrome responds:** Absent. No product in frame. The ingredient is the subject.
- **Closeness:** Macro. Reading distance at its most literal — the camera catalogues the material the way a scientist examines a specimen.
- **Rose-warm axis:** The backdrop is pure toneless white, not the rose-warm linen of other bands. The material's own color is the only warmth. Specimen isolation requires neutral context so the ingredient reads as evidence, not decoration.

**Post treatment:** Clean. Minimal grade. Color-accurate — the material's true color must read correctly. No film grain. Closest to CHROME in finish.

**Prerequisite:** Read the hub `SKILL.md` first. For product shots (bottles, jars, packaging), use `product-catalog.md`. For texture swipes and product-on-swipe, use `texture.md`.

---

## The Directive

Ingredients are evidence of the formula's intelligence. They should feel like specimens in a world-class research library — beautiful, but their beauty is secondary to their specificity. Every ingredient image says: *this is the exact thing we chose, and we chose it for a reason.*

---

## Type 1 — Botanical & Fruit Specimens

Fruits, plants, leaves, roots, and natural extracts with a recognizable physical form. Elevated to fine art specimen. Not food, not styled. Scientific precision crossed with natural beauty.

**Source botanical rule.** If an ingredient is an extract, oil, or derivative, always photograph the source — never the processed form. Bisabolol → German chamomile flower. Turmeric extract → turmeric rhizome. Vitamin C → lemon or orange. Only fall back to Type 2 if no recognizable botanical source exists.

**Orientation by form.**
Face the most structurally distinctive surface toward camera at a 10–15° off-axis tilt.
- **Fruits & roots:** Upright on cut base, cut face toward camera.
- **Leaves & botanicals:** Upright on cut stem, primary leaf surface toward camera.
- **Flowers:** Slight natural tilt, bloom face toward camera.

**All ingredients face left.** 10–15° off-axis tilt to the left. Consistent across every Type 1 image.

**Lighting.** Single strong directional light from upper-left at moderate angle. Strong enough for clear bright/shadow sides, letting the ingredient's structure create surface detail. One perceived source.

**Composition:**
- Pure white seamless background — toneless studio white.
- Subject fills 65% of frame. Generous negative space.
- Faint contact shadow directly beneath base.

**The "just handled" realism rule.** Always include:
- Fruits and roots → *"cut two minutes ago and placed under a studio lamp"*
- Botanicals and flowers → *"just picked and placed under a studio lamp"*
- Always add: *"do NOT generate a perfectly symmetrical pattern — biological asymmetry, real specimen not a 3D model."* (Generator override — biologicals default to symmetry.)

**Imperfection checklist.** Select relevant items per type:
- **Fruits/citrus:** cut face uneven, knife drag mark, vesicles vary in fullness, juice as wet specular beads, seeds off-center, pith irregular
- **Roots/rhizomes:** knobbly form, faint blemish on skin, cut edge ragged, fibrous interior visible, growth rings irregular
- **Leaves/botanicals:** vary in size, minor crease or micro-tear, stem cut ragged, natural curl at edges
- **Flowers:** petals vary in length/angle/width, one or two creased or bent, disc florets vary open/closed, reflexed petals where correct

**Color anchoring.** Name the correct color AND exclude the wrong default. Common failures: turmeric renders yellow (should be deep orange), grapefruit renders pale yellow (should be blush pink), chamomile petals render cream (should be pure white).

**Environment context.** The specimen exists in an isolated studio world. Always include context language that anchors the setting positively:
- Citrus → *"studio specimen on seamless white paper, laboratory precision"*
- Botanicals → *"single specimen on seamless white paper, botanical catalogue"*
- Flowers → *"single bloom on seamless white paper, specimen archive"*
- Roots → *"single specimen on seamless white paper, material study"*
- All: *"isolated on studio white, nothing else in the frame."*

**Prompt template:**

**Layer C from here forward.** The Directive, the orientation rules, the imperfection checklist — all Layer A and B. The template below is Layer C — only pixel-driving language enters the generator.

```
Studio macro photograph of [ingredient],
[orientation from form rules],
slight off-axis angle — 10–15° tilt to the left,
subject fills 65% of frame, generous negative space,
pure white seamless background,
single strong directional light from upper-left, moderate angle — strong enough for clear bright/shadow sides, gentle enough for even surface detail,
subject's structure creates texture detail through the light gradient,
[key structure] sharp — [specific detail] individually defined,
[imperfections from checklist],
[realism anchor] and placed under a studio lamp,
do NOT generate a perfectly symmetrical pattern — biological asymmetry, real specimen not a 3D model,
faint contact shadow beneath base,
photorealistic — documentary quality, real material behavior,
[environment context from list above],
color palette: [correct color, not wrong default] against pure white
```

---

## Type 2 — Creams, Liquids & Powders

Ingredients with no recognizable physical form — powders, oils, serums, emulsions. Represented through texture and material behavior.

**Composition:**
- Material itself is the subject — swatch, drop, drift, pool.
- Pure white seamless background. Material only, isolated.
- Overhead / flat lay. Material lies naturally.
- Soft, even, diffused light. Clinical observation. Material's texture creates depth, not light.
- Entire material visible within frame — white space on all four edges, slightly off-center right.
- Faint contact shadow only.

**The "just applied" realism rule.** Always include: *"the material was just applied or poured — spread edge irregular, organic shape (not a perfect circle or geometric form), real material behavior."*

**Color anchoring.** Name correct color, exclude wrong default. Retinol = pale yellow (not white). Vitamin E = deep amber-gold (not orange). Powder ingredients = off-white (not grey).

**Environment context.** *"Material only — isolated on studio white, nothing else in the frame. A material sample being catalogued."*

**Prompt template:**
```
Overhead macro photograph of [material form],
material lies flat, shot from directly above,
entire material visible — white space on all four edges, slightly off-center right,
pure white seamless background,
soft even diffused light — clinical, ambient, enveloping,
faint contact shadow beneath material only,
razor-sharp focus on [key detail],
the material was just applied — spread edge irregular, real behavior,
reads like a material sample being catalogued — clinical, precise,
material only — isolated on studio white, nothing else in the frame,
color palette: [correct color, not wrong default] against pure white
```

---

## Planner Checkpoint — Confirm Before Writing

Before generating an ingredient prompt, confirm the core slots:

| Core slot | Decision |
|---|---|
| dominant_source | Type 1: single directional from upper-left, moderate angle. Type 2: soft even diffused, ambient. |
| warmth_carrier | The ingredient's own color — named specifically per the color anchoring rule. |
| camera_distance | Type 1: macro, subject fills 65%. Type 2: overhead macro, white space on all four edges. |
| focus_hierarchy | Type 1: key structure sharp (cut face, petal detail, fibrous interior). Type 2: razor-sharp on key material detail. |
| chrome_presence | Absent. |
| hero_event | Type 1: the specimen itself — its specificity, its imperfections, its realness. Type 2: the material's behavior — spread, viscosity, surface quality. |

All filled → proceed to prompt template.
