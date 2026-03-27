---
name: proven-ui
description: "Build world-class frontend interfaces for PROVEN Skincare. Design-first skill that balances scientific intelligence with human warmth — bold typography, cinematic motion, a palette that interplays warm and cool tones, lifestyle photography, and fearless use of negative space. Carries PROVEN's palette and core components but gives full creative latitude to produce interfaces that feel both precise and personal. Use for any PROVEN UI build: web pages, landing pages, components, overlays, wireframes, prototypes, email template visuals, or interactive artifacts. Triggers on requests involving HTML, CSS, React, page builds, wireframes, layout, UI components, design systems, or any visual build work for PROVEN."
---

# PROVEN UI — Design System

Build PROVEN interfaces the way the best design studio in the world would: start with the feeling, then make every pixel serve it. The feeling is: rigorous science, delivered with warmth.

## Before You Build — Mandatory Gate

For full page builds, landing pages, or any multi-section UI work:
**Read and follow `references/process.md` before producing any output.**
**Read `proven-voice/SKILL.md` before writing any copy.**
Present section architecture (Gate 1) for approval before writing copy.
Present copy (Gate 2) for approval before building HTML.
Do not skip gates. Do not extract briefs from conversation — request a PRD.

For single components, section edits, or token lookups: skip this gate.

---

## Reference Files

| File | Answers | Read when |
|---|---|---|
| **`references/tokens.md`** | *What's the exact value?* | Mid-build — CSS values, spacing, button styles, glass, gradients, motion, SVGs |
| **`references/frontend.md`** | *How do I build it?* | Mid-build — grid system, breakpoints, component HTML/CSS, animation JS, responsive patterns |
| **`references/process.md`** | *What's the workflow?* | Full page builds — gated workflow, PM handoff, brief template, test suite |

| Task | Read these |
|---|---|
| **Full page build** | process → this file → tokens → frontend |
| **Single component** | this file → tokens → frontend |
| **Add / edit a section** | this file → tokens → frontend |
| **Token / value lookup** | tokens |
| **Implementation lookup** | frontend |
| **Review / critique** | this file only |

---

## How to Think

Before touching code, answer one question: *When someone lands here, do they feel recognized?* Not impressed. Not intrigued. **Recognized** — the way you feel when someone presents a solution to a problem you hadn't finished describing.

Every decision in this system exists to create that moment.

**Certainty through intelligence.** Skincare here is a solved, engineered system — not hope, not experimentation. Nothing on the page should look like it's *trying* — it should look like it arrived already knowing.

**Evidence over emotion.** The data is the story, not supporting material. PROVEN's 47 factors, the Skin Genome Project, the quiz — these belong at the front of the narrative. Present data beautifully because well-presented data builds certainty. The user gave you 47 dimensions of their life. Show how those inputs became their formula.

**Intelligence in service of a life.** The interface should feel like it lives in someone's life, not in a lab. Show real skin in warm light on a bathroom counter, not just a white void. The science is rigorous; the experience of encountering it should feel like a friend who happens to be a scientist. The highest expression of this is the composite — data overlays on real skin, insight chips on a morning counter, a glass panel on a lifestyle image. The intelligence becomes visible inside the life, not beside it.

**Calm authority.** The interface doesn't sell — it presents. When the design trusts the user enough to not oversell, the user feels respected. That respect *is* recognition.

**The one thing.** Every screen has one job. One focal point. If you can't point to it instantly, the design isn't done.

**Remove until it breaks.** Delete an element. If the design still works, it wasn't needed. Keep deleting until something breaks. Add that last thing back. Intelligent brands don't explain themselves. The more a page justifies, the less confident it sounds. Trust the user to be intelligent.

**Clean means quiet.** The benchmark is Apple, Hims, Oura — pages that are 70%+ white or near-white, with one or two color moments. Light sections feel like empty gallery walls: linen cards on white canvas, navy type, teal metadata. Dark sections (cool dark navy, teal dark) carry personality and color range — but they're earned, not default. When light sections accumulate per-card gradients, radial overlays, and accent bars, the page stops feeling premium and starts feeling like a dashboard. Strip it back. If a light section has more visual complexity than the dark section above it, something went wrong.

**The signature.** PROVEN's visual identity lives where intelligence meets intimacy — a glass stat panel floating over real skin, a factor count beside a morning routine, a profile rendered as a portrait. No other skincare brand can produce this moment because no other brand has the data system to fill it. The data layer is not supporting material. It is the design. When a section has photography and data coexisting in the same frame — specific data, real photography, glass between them — that section is doing PROVEN's hardest and most valuable work.

---

## Language Rules

Never use "custom." Use "personalized" instead. Custom implies made-to-order. Personalized implies intelligence — the system knows you.

---

## Typography

```css
@import url('https://fonts.googleapis.com/css2?family=Albert+Sans:wght@300;400;500;600;700;800;900&family=Source+Serif+4:ital,wght@0,300;0,400;0,500;0,600;0,700;0,800;1,300;1,400;1,500;1,600;1,700;1,800&display=swap');
```

### Three Headline Tiers

Headlines own the viewport. The tier determines how loud.

| Tier | Size | Weight | Tracking | Line-height | Use |
|------|------|--------|----------|-------------|-----|
| **Display** | `clamp(36px, 9vw, 80px)` | 900 | −0.05em | 0.9 | Hero, statement, data showcase, final CTA — fills the width |
| **Section** | `clamp(28px, 6vw, 56px)` | 900 | −0.045em | 0.92 | Problem cards, results, in-page section headlines |
| **Card** | `clamp(24px, 4.5vw, 42px)` | 800 | −0.04em | 0.95 | Timeline moments, product cards, contained headlines |

**Body and below:**

| Role | Size | Weight | Character |
|------|------|--------|-----------|
| Body | 13–14px | 500 | The whisper beneath the shout. One sentence per section. |
| Labels | 10–11px | 800, uppercase, +0.16em tracking | Crisp metadata |
| Micro | 9px | 700, uppercase, +0.12em tracking | Glass panel labels, factor labels |

The ratio between Display and Body is 6:1 or greater. If the headline and body are close in size, the page looks like a document. Push the gap.

### Source Serif 4 — The Accent

Switch one word per headline to Source Serif 4 italic. At weight 700 — matching the visual mass of Albert Sans 900. The style shift is a visual event, not a quiet substitution. *"Your skin, understood."* The italic word is where the eye lands.

Once per section. Never in body copy. Never more than two words. It is punctuation — not a typeface choice.

Full type scale values → see `references/tokens.md`.

---

## Color

| Color | Hex | Semantic use |
|---|---|---|
| White | `#FFFFFF` | Default canvas |
| Linen | `#FAF6F2` | Warm sections, warm gradients |
| Sand | `#E6DED4` | Card fills, tags — use sparingly |
| Rose | `#DDBFB0` | Personal data moments, glass tints |
| Sky | `#BCD4E2` | Cool sections, evidence |
| Teal | `#7295A2` | Labels on white only |
| Teal Dark | `#4A6D7C` | Labels on linen or any off-white |
| Teal Light | `#8CAEB9` | Labels on dark surfaces |
| Navy | `#162743` | Dark sections, stat numbers |
| Black | `#000000` | Headlines and body text |
| Ember | `#C26A4A` | Primary action — buttons, links, forward motion |
| Ember Dark | `#E08A6A` | Ember on dark surfaces |
| Signal | `#FFFA67` | Proof tags, data emphasis, result badges — rare |
| Sage | `#5E7D7A` | Domain tint — lifestyle, routine, wellness sections |

CSS custom properties → see `references/tokens.md`.

### The Brightness Principle

PROVEN pages open bright and stay bright. The top fold and first content sections live on white, linen, or subtle light gradients — the Apple-clean first impression. Color and warmth come from photography and content, not surface color. Dark sections enter the page only after the bright sections have established clarity and trust.

**Pages where the user arrives with curiosity** (landing pages, PDPs, quiz entry) always open bright. **Pages where the user arrives with intent** (about, science, press, campaign) may open dark — the user already knows PROVEN and the opening beat is a statement, not an orientation.

A page should be 60–70% light surfaces by scroll height. Dark sections are punctuation that the user scrolls *into*, not lands *on*.

### The Warm / Cool Interplay

White is the canvas. Color is earned. A page should feel predominantly white and airy, with warm moments (linen, rose, skin photography) and cool moments (sky, teal, data) creating rhythm. Neither register dominates — the interplay between them *is* PROVEN. All warm → beige. All cool → clinical. The balance is the brand.

Photography carries the warmth. Skin is always the warmest surface in the frame. Chrome reflects its environment — luminous on white, dramatic on dark. The UI surfaces stay quiet and let the images do the emotional work. Every page needs at least one warm beat — skin photography, a rose-tinted section, a Source Serif italic moment, a lifestyle image. If a page has no warm content, it's not PROVEN — it's clinical.

### Two Dark Registers

Dark sections are earned late in the scroll. Never in the first two folds on curiosity pages. Never adjacent — always a light section between them. The content determines which register:

- **Cool dark** (navy drifting to deep teal / sky) — authority, evidence, brand statement. Data showcases, stat sections, science methodology, final CTA. The heaviest, most dramatic surface. Chrome product photography goes sculptural here — edge highlights, reflections.
- **Teal dark** (mid-range teal gradient) — the system showing its work. Factor breakdowns, profile reveals, routine walkthroughs, formula context. Skin close-up photography with data overlays lives here — skin reads warm against the mid-teal, and glass stat panels (rose for personal, sky for scientific) are legible.

### Three Domain Tints

**Pure white (#FFFFFF) is the default surface.** Most light sections should be clean white — no tint, no gradient, no linen. White creates the sharpest contrast against navy headlines and dark sections. Domain tints are earned when a section's content is explicitly about one biological, environmental, or lifestyle domain. A page that tints every section looks soft. A page that's mostly white with one or two tinted sections feels intentional.

| Register | Tint source | Section content |
|---|---|---|
| Warm / personal | Rose (#DDBFB0 at ~10–12%) | Your skin, your biology, your profile, personalization reveal |
| Cool / intelligence | Sky (#BCD4E2 at ~12–14%) | The algorithm, the science, how it works, ingredients, evidence, environment |
| Neutral / lifestyle | Sage (#5E7D7A at ~8–10%) | Daily routine, lifestyle factors, product in your life |

**Sky is the intelligence register.** It's the workhorse tint — any section where the system is the subject can sit on sky. At 12–14% opacity it reads as bright and clean, not blue. Sky-washed sections are bright enough to appear in the top folds, including heroes. A hero on a sky wash says "intelligence has arrived" before a word is read. A hero on linen says "this is personal." Both are Apple-clean. The choice is tonal.

Domain tints are the section *surface* — they don't count toward the "one color accent per section" rule. A rose-tinted section still follows all accent rules for elements on top of it. Domain tints stay on the rose-warm axis — never amber, golden, or orange-cast — consistent with the photography color contract.

Gradient tokens for domain tints → see `references/tokens.md`.

### Teal — Three Registers (Mandatory)

Teal is used at small sizes (11–13px labels, metadata) where WCAG AA requires 4.5:1. The wrong register will fail accessibility.

- `--teal` (#7295A2) — only on pure white backgrounds
- `--teal-dark` (#4A6D7C) — on linen or any off-white surface
- `--teal-light` (#8CAEB9) — on any dark surface

### Readability Contract

PROVEN's palette is soft — warm light backgrounds, atmospheric dark surfaces. This means text opacity must be **higher** than instinct suggests. Every text element must pass WCAG AA: 4.5:1 for body/small text, 3:1 for large text. When in doubt, bump opacity by 0.1. Text that's slightly more visible than you'd like is always better than text someone can't read.

Specific minimum opacity values → see `references/tokens.md`.

---

## Ember — The Commitment Color

**Ember is the color of forward motion.** It appears wherever the user can take the next step. Think of how Apple uses blue: text links throughout, filled buttons only at commitment moments.

**1. Ember text links — the primary expression.** Most Ember on a marketing page is text links: "Learn more ›", "Shop now ›", "Take the quiz ›". Ember text is navigational only — never for headlines, body copy, emphasis, labels, or data. The arrow character (›) confirms it's a link, not styled prose. Max 4 Ember text links visible per viewport. Use `--ember-dark` (#E08A6A) on dark surfaces.

**2. Ember filled pill — the rare, loud expression.** Filled Ember buttons appear only at commitment moments: hero CTA, quiz submission, checkout. One filled Ember button per viewport maximum.

**Where Ember appears:** Text-link buttons throughout content zones (the workhorse). Filled pill buttons at hero/transaction moments. Outline pill buttons on hero only (paired with filled Ember — never elsewhere). Ember icon accents — a small Ember-filled circle containing an icon inside a neutral button (sparingly, one per section max). Transaction states — quiz selection rings, radio fills, form focus rings.

**Where Ember never appears:** Data, stats, badges, progress bars, icons, category labels, decorative elements. Inside the same component as Signal. As a section background or card fill. As filled buttons in content zones (use text links there instead). In headlines, body copy, pull quotes, or any non-navigational text.

Full button vocabulary (all styles, all backgrounds) → see `references/tokens.md`.

---

## Signal — The Evidence Color

**Signal marks proof.** A highlighter pen for data — non-interactive, non-clickable, and rare. Apple-level restraint: 1–3 instances on a marketing page, denser only on data screens like quiz results.

**Signal is not optional on marketing pages.** Every landing page and marketing page must include at least 1 Signal instance — and should target 2–3. If a page has proof points (stats, clinical claims, trust credentials) but no Signal, the evidence is under-designed. Signal is how PROVEN visually separates claims from proof. Without it, data looks like copy.

**Placement priority (choose 1–3):**
1. **Proof tag** on the single strongest trust credential (e.g., "MIT AI Technology of the Year," "93% saw improvement")
2. **Stat underline** on the most emotionally resonant number in the first two folds
3. **Accent bar** beneath a key stat on a dark section

When deciding which proof points earn Signal, ask: *which number would a skeptic need highlighted to keep scrolling?*

**The two-color contract:** Ember closes with the CTA. Signal builds the evidence case. They never occupy the same component. An Ember button never carries a Signal badge. A Signal-tagged card has no Ember borders. They coexist on the page but stay in separate elements.

Signal usage specs (proof tags, stat underlines, accent bars, trust badges, and where Signal never appears) → see `references/tokens.md`.

---

## Two-Icon System

PROVEN uses two proprietary shapes. Their separation is the system. Never use both in the same section.

### Brand Hex — "PROVEN is speaking"

The molecular honeycomb from PROVEN's logo. Appears at brand identity moments — when PROVEN is identifying itself, not when data or content is doing the work. Always small (15–24px), always paired with text, always quiet.

**Appears at:** Nav (paired with wordmark), hero section tag (beside "Skincare for [audience]"), section labels for brand content (The Routine, lifestyle, educational), final CTA (centered above headline as brand stamp), footer.

### Data Pin — "The system is showing its work"

A hex-top shield tapering to a point. **The pin is a container** — it holds values inside its hollow center (factor counts, concentrations, scores). A pin without a value inside it is decorative. Decorative pins are forbidden.

**Appears at:** Data point containers (pin holds 47, 32 of 47, a match score), ingredient logic nodes (holding computed concentration, e.g. 4.2%), personalization states (a value the system computed for this user), quiz progress steps.

**Never appears at:** Heroes, decorative patterns, section labels (the pin is not a label — it's a container), beside numbers (the number goes INSIDE the pin, not next to it), without a value.

**Scarcity rule:** 1–6 pins per marketing page maximum. If a pin appears in every section, it becomes invisible. The pin should create a tonal shift when it appears — the page was telling you about the system; now the system is showing its work.

Pin CSS, fill colors by context, and SVG definitions → see `references/tokens.md`.

---

## Sacred Components

Not to be redesigned. Shape is fixed; fill, color, and opacity vary.

- **Buttons** — Pill-shaped (`border-radius: 9999px`), Albert Sans 500, Title Case
- **Tags** — Pill-shaped, lowercase, Albert Sans 500
- **Cards** — 16px radius, no shadows, no borders
- **Icons** — Outline-only, 1.5px stroke, Lucide React for UI icons. Brand marks use the Two-Icon System.

---

## Design Principles

Seven principles govern PROVEN's design. All seven matter. But Data Made Beautiful is the one that makes PROVEN different from every other premium skincare brand. The others produce quality. Data Made Beautiful produces identity.

### 1. Whitespace Is Punctuation

The strongest moments on a PROVEN page own the entire viewport: one stat, one statement, one visualization. Whitespace isn't padding — it's what turns a design element into a moment. Vary spacing dramatically to control pacing. Tight spacing moves the reader quickly. Massive spacing forces a slow-down.

### 2. Quiet Authority

The content is the interface. Containers, borders, dividers, and chrome recede. Navigation is frosted glass — present but invisible when you're not looking for it.

**Images throughout, not in isolation.** Don't save photography for hero sections. Weave images into the page at every opportunity — behind data, beside copy, between sections. A page that alternates between rich imagery and text-only blocks breathes differently than one that stacks copy section after section. Images carry personality and warmth that layout and type cannot.

**Material confidence.** Every visual asset carries the same precision — but precision doesn't mean cold. Product photography is crafted and intentional, shown with the same care as the formula inside. Lifestyle photography carries equal weight: real skin in warm light, hands applying product, morning routines, the texture of daily life. Data cards, infographics, and skin profile visualizations sit at the same visual level as both product and lifestyle imagery. And the composites — data overlays on photography — are where these tiers merge and the intelligence becomes visible. When everything on the page is made with equal care, the user trusts the system without being asked to.

**Content lives on images, not beside them.** Never split a section into "image zone + copy zone." Text, data, and CTAs occupy the same surface as the photography — overlaid with gradient masks, anchored in glass cards, or placed in the natural breathing room of the image. A problem card is one surface: skin photography fills it, a dark gradient rises from the bottom, copy sits inside that gradient. A timeline moment is one card: lifestyle photography fills it, an insight chip floats on the image, copy anchors at the bottom. This is the Hers and Apple pattern — every section is one composition, not two things placed beside each other.

### 3. Hierarchy Guides the Eye

The page is a path, not a surface. At every scroll position, one thing is in focus — one idea, one image, one question. The user should never wonder what they're supposed to look at or what comes next.

Hierarchy is built through contrast: large type against small, full-bleed image against tight text block, dark section against white. Brands like Oura and Hims earn attention by making the contrast between elements do the navigational work — not labels, not arrows, not instructional copy.

Each section has one job. State it through layout, image, and type treatment — not explanation. When a section needs words to explain what it's doing, the design isn't done.

**Scroll should feel inevitable.** The end of one section creates a natural pull into the next — a question answered becomes a new curiosity. The sequence is the argument. By the bottom of the page, the user has been led somewhere, not scrolled somewhere.

**The master scroll sequence: Your life → your data → our solution.** Start with a moment the user recognizes, reveal the data that makes sense of it, then resolve with the product. Each scroll position is the next logical beat. This is the content ordering within a section. The emotional arc across the full page is in Sequence Logic below.

### 4. Warmth in the Right Moments

White is the default. Color is earned. The more personal the content, the warmer the design — quiz results drift toward linen and rose, evidence stays on sky or white. The rhythm between cool evidence and warm recognition as the user scrolls is PROVEN's signature.

**Restraint on light surfaces.** Card grids on white or linen backgrounds use a single, uniform card color — typically linen (#FAF6F2) on white, or white on linen. Do not alternate warm and cool card backgrounds within the same grid. A grid where each card has its own gradient reads as a patchwork, not a system. If individual cards need visual identity, use typography, icons, or a single accent element — not per-card background variation. The grid should feel like one designed object, not four competing ones.

**One color accent per section maximum.** A results section uses navy numbers + teal labels + muted descriptions on linen cards. That's it. Adding per-card ring colors, gradient overlays, and radial backgrounds competes with the data. Let the numbers do the work. If a section has more than two non-text colors, remove until two or fewer.

**Dark surfaces carry the color.** The warm/cool interplay on dark sections comes from the two registers (cool dark for authority, teal dark for system explanation) and the content on top of them — rose glass, skin photography, warm typography. Light sections are the quiet space between — predominantly white, linen, or domain-tinted, with color earned through the content, not card-level decoration.

**Testimonials live inside their proof.** A testimonial about the morning routine belongs in the morning section, not in a separate grid. Use Source Serif 4 italic with a rose left-border. Include specifics: skin type, location, age, timeline. The testimonial is a footnote from someone who already lives this life. Dedicated testimonial sections (rose-tinted glass cards) are the secondary pattern for social proof density.

### 5. Data Made Beautiful

Five data types, each with its own treatment:

- **Personal data** — portrait, not spreadsheet. The user's skin profile, their factors, their quiz results. Design as a composed portrait.
- **Scientific evidence** — structural clarity. Research citations, ingredient studies, mechanism explanations. Clean, authoritative, cool register.
- **Results** — typographic scale, anchored to timelines. Before/after, week 1 vs week 8. Numbers earn maximum size.
- **Personalization logic** — progressive sequences showing input → output. 47 factors → data analysis → ingredient selection → concentration → your bottle. The visible pipeline.
- **Educational content** — progressive disclosure. Lead with the insight, explain on demand, cite the science underneath.

**Data is contextual, not sectional.** 89% belongs floating over the night routine image, not in a stat grid. 47 factors belongs inside the moment where those factors are at work. When data has a home in a real moment, it stops being a claim and becomes evidence. Reserve standalone data showcases for science and about pages. On landing pages, distribute data into the narrative.

**Data speaks to the user, not about the brand.** "28M+ data points powering every formula" is brand-facing. A profile card showing "your climate: arid · UV: high → Your Custom System" is user-facing. Default to user-facing.

**Data rendered as artifacts.** The most powerful way to show intelligence is a designed object that looks like real product output — quiz result cards, skin profiles with progress bars, formula breakdowns. These mock UI cards make personalization tangible. The user should project themselves into the artifact.

**Data Color System.** Three tiers: core palette (surfaces + all text), data visualization (6 domain-mapped fills for charts/gauges/tags), and highlights (7 bright accents for pin fills and indicator dots only). Text on data visualizations always uses core palette colors — navy on light surfaces, white on dark. Data viz colors are shape fills only, never text. Highlight colors are reserved for pins and small dots at maximum 1–3 per viewport. Full specs, hex values, and usage rules → see `references/tokens.md`.

**Data's highest expression is the composite** — data and photography merged into one frame. A skin close-up with a glass factor panel. A routine image with an insight chip. These composites are described in the Composites section above. Every PROVEN landing page should include at least one. Pages without composites are quality skincare pages. Pages with composites are PROVEN pages.

### 6. Pacing That Breathes

Three tiers of motion. Never mix. Never loop. If the user stops scrolling, the page should be perfectly still.

- **Scroll-bound transformations** (narrative tier): content morphs, numbers count up — locked to scroll position. One or two per page.
- **Scroll-triggered reveals** (rhythm tier): default for most content. Fade up with `translateY(40px)`, stagger siblings 80–150ms.
- **Micro-interactions** (polish tier): hovers and state changes. Nothing bounces, pulses, or loops.

Motion token values → see `references/tokens.md`. Animation JS implementation → see `references/frontend.md`.

### 7. Visual Before Verbal

Before writing a sentence, ask: can this be a number, a stat, an icon, a step, a card, or a before/after? A stat communicates faster than the sentence explaining it. A three-column card grid communicates faster than three paragraphs. Default to designed objects. Use prose only for what cannot be shown.

**Section defaults — reach for these before reaching for copy:**

Every content type has a most-compressed visual form. Find it and use it. A proof stat is a large number with a 6-word label — not a sentence explaining it. A process is numbered steps or a visual timeline — not a paragraph describing it. A comparison is a two-column layout — not prose walking through the difference. A quote with a name and tag is social proof — no framing copy around it.

The test: could this content be a number, a step, a card, a quote, a comparison column, or a diagram? If yes — use that. Prose only for what cannot be shown.

If a section needs a paragraph to be understood, the visual design isn't doing its job. Add the visual. Cut the paragraph.

### Copy Budget

These are hard ceilings, not targets.

**Headlines:** 6 words or fewer. The headline is typography — it must own the viewport at Display tier without wrapping awkwardly. If it needs a second sentence, it's too long. "Skincare that reads your rosacea." "47 factors. Not 4 skin types." "Your formula. Nobody else's."

**Body copy:** One sentence per section maximum. Two sentences is the hard ceiling. If a section needs a paragraph to be understood, the visual isn't doing its job — fix the visual, don't add copy.

**Sub-headlines:** One short line beneath the Display headline. This is the bridge, not a second headline. "47 factors. One formula. Yours." "One routine. Updated when your life changes."

**The rule:** If it sounds like it's explaining, cut it. PROVEN copy lands — it doesn't elaborate.

---

## Mobile First

Most PROVEN users arrive on mobile. Design for mobile first — every section, every layout decision, every type choice. Desktop is an enhancement, not the default.

If it doesn't work on mobile, it doesn't work.

- **Typography:** Use `clamp()` throughout. Drama compresses but stays.
- **Spacing:** 120–200px desktop gaps → 80–120px mobile. The ratio between tight and generous stays dramatic — just scaled down.
- **Full-bleed visuals:** Shift to taller crops for mobile viewports. `aspect-ratio: 3/4` or `min-height: 80vh`.
- **Touch targets:** Min 48px, ideally 56px. Full-width CTAs on mobile.
- **Grids:** Collapse thoughtfully based on content — not every grid needs to go single column, but every column reduction requires revisiting padding, type size, and element order. Never just `flex-wrap` and assume it works.
- **Stat cards:** Stack vertically. Never shrink to fit a row.
- **Scroll animations:** Simplify scroll-bound transformations. Reveals work identically.

Breakpoint values, collapse patterns, and responsive image CSS → see `references/frontend.md`.

---

## Composites — Intelligence on Life

The highest-value visual on a PROVEN page is a composite: photography + data layer = one designed image. These are the moments customers remember and no competitor can replicate.

### Two Composite Types

| Composite | Photography | Data layer | Where it appears |
|---|---|---|---|
| **Skin + Insight** | Skin close-up (Activated Terrain) | Rose glass stat panels, factor chips | Profile Showcase, hero on skin-condition pages |
| **Routine + Context** | Lifestyle (product in life) | Insight chips, white/warm glass panels | Timeline Narrative, routine sections |

### The 70/30 Rule

Photography is 70% of the visual weight. Data layer is 30%. The photograph carries the emotion. The data provides the intelligence. If the glass panels dominate, it's a dashboard. If the photography has no data, it's a lifestyle brand.

### Content Rules

- Every glass panel holds a value — a number, a factor name, a concentration. Never decorative.
- Maximum 3 glass elements per image. More than 3 is clinical, not intimate.
- One panel can be larger (the "lead" insight). Others are supporting chips.
- Rose glass for personal data. Sky glass for scientific data. The lead panel is always rose on skin photography — the user sees themselves first.
- Glass panels sit in the "quiet zone" of the photograph — areas of low detail. Never over the sharpest focal point.

### The Dual-Cover Test

Cover the data layer. Is the photograph strong on its own? Cover the photograph. Does the data feel specific and personal? Both layers must stand alone before they merge.

### Composite Minimum

Every landing page includes at least one composite. Target 2–3. Other marketing pages should target 1–2 based on content. A landing page with zero composites is incomplete — the same way a page with zero Signal is.

Glass-on-photography pairing specs → see `references/tokens.md`.

---

## Evidence Library — What PROVEN Can Show

Apple and Hers pages feel rich because every section shows a *different kind of evidence* that the product works. Our pages feel monotonous when every section is a gradient with a headline — the same claim wearing different hats. The fix is content type variety: each section must be a fundamentally different kind of thing.

**Every landing page must include at least 5 of these evidence types. No two consecutive sections can show the same type.**

### The Evidence Types

| Type | What the user sees | Designed object |
|---|---|---|
| **The Quiz** | A rendered mockup of 2–3 quiz questions with real question text, answer pills, a progress bar | Interactive-feeling UI card — not a screenshot, not a gradient with "take the quiz." Actual question text, tappable-looking answer options, a step counter. |
| **The Profile** | Her rendered skin profile — factors, values, the algorithm's output as a portrait | Glass card with factor grid, data-viz bars or dots, flow visualization. The profile card IS the section, not an element inside one. |
| **The Bottle** | Chrome product photography — hero shot filling a card, in-hand, on a counter, macro on the label | Image fills the container. Gradient fade at bottom for text. The chrome catches light across the full surface. |
| **The Formula** | A visualization of ingredients selected with concentrations, comparison logic, why-this-not-that | Ingredient tiles with concentration values, comparison arrows, or a flow from factors → ingredients → formula. Not stat numbers — a process. |
| **The Skin** | Macro skin photography — real texture, real pores, real glow, the algorithm reading | Full-bleed or contained portrait card. Warm tones. The camera is close. This is the brand's visual signature. |
| **The Before/After** | Side-by-side with name, location, age, timeline, skin type | Before/after image pairs with detail text beneath. Signal tag on best result. Real specifics, not generic. |
| **The Adaptation** | A comparison of winter vs summer formula — what changed and why | Two-column or stacked comparison: left column = before, right = after. Ingredient names, concentrations, reason for change. Makes "adaptive" tangible. |
| **The Person** | Lifestyle mid-routine — hands applying product, product among her things, the window present | Full-bleed or contained card. Product is IN a life, not staged. Chrome catches the light. She's not performing. |
| **The System** | A flow visualization: quiz → 47 factors → 28M data points → formula → bottle | A designed diagram or animated flow. Horizontal or vertical. Each step is a node with a short label. The pipeline made visible. |
| **The Testimonial** | Quote with weight-shifted type — bold the transformation phrase, fade the context to 40% opacity | Large type, not a small card. Key phrase in full weight, surrounding text in light weight. Inline before/after pair if available. Name, age, timeline beneath. |
| **The Trust Strip** | A horizontal band of proof signals — press logos, stat numbers, credential badges, award marks | Low height, full width, no card. MIT, Sephora, Shark Tank, patent count, study count. Dense and quiet. |

### Designed Objects vs Containers

A section is spacing and a surface color. A **designed object** is the thing inside it — the quiz mockup, the profile card, the ingredient diagram, the testimonial with weight-shifted type. The skill's section vocabulary defines containers. This evidence library defines objects.

**The rule: decide the object first, then pick the container.** A quiz mockup might sit in white space (no card), a profile card might sit on teal dark (full-bleed skin fading into it), a testimonial might fill a contained card. The object determines the section shape — not the other way around.

### Density Contrast

Tag each section as **sparse** (single-line element — Trust Strip, system flow), **medium** (card with content, rich typography section — Problem, Product, Timeline moment, Statement with weight-shifted text), or **dense** (data-heavy — Profile, Data Showcase, Formula, Adaptation comparison).

**The rule: never place two sections of the same density adjacent to each other.** Sparse → dense → medium → sparse. The swing between empty and full creates rhythm. If three medium-density sections stack up, the page flatlines.

### Text Position Variety

Text anchors at the **bottom** of integrated cards by default. But if every section anchors text at the bottom, the page becomes predictable.

**The rule: vary text position across the page.** A hero with centered text → a statement (centered, typography-only) → a problem card (text bottom-left) → a data section (text centered over stats) → a timeline (text bottom of each card) → a profile (glass card centered, headline below) → a product (text bottom-left) → a CTA (centered). The eye should move to a different place on each scroll.

Ways to move text: top-left on a full-bleed section, centered over a contained product, bottom-left on an integrated card, centered below a designed object, right-aligned against a left-anchored image. The integrated card's bottom-anchor is one option, not the only option.

---

## Section Vocabulary

A vocabulary of section types. Pick what the page needs. Combine freely. Each section has one job.

**The integrated card is ONE layout pattern, not the only one.** Photography-with-gradient-and-text-at-bottom applies to problem cards, timeline moments, and product reveals. But a page also needs: full-bleed photography with no container, typography-only sections, horizontal strips, rendered UI mockups, data visualizations that aren't stat numbers. If every section on the page is an integrated card, the page is a template — regardless of how good each card is. Images always fill their container — never float as separate objects above or beside text.

### Photography Spectrum

PROVEN has a full photography system across three bands and seven categories. The UI skill selects from this spectrum — the `proven-creative` skill handles prompt generation and shot direction.

**Three Bands:**

| Band | Temperature | Subject | Energy |
|---|---|---|---|
| **CHROME** | Cool, controlled, gallery quiet | Product is the only event. Chrome responds to surfaces. | Apple-grade precision |
| **RITUAL** | Warm-cool interplay, atmospheric | Product in a life. Environment tells the story. | Daily, editorial, lived-in |
| **SKIN** | Cinematic human observation | Person is the subject. Chrome is absent or peripheral. | Intimate, recognizing, alive |

**Seven Photography Categories (select from this menu per section):**

| Category | Band | What it shows | Background-eligible | Use on pages when... |
|---|---|---|---|---|
| **Catalog Product** | CHROME | Product alone — hero shot, card shot, close-up, hand holding, shelf. Chrome reflects the surface beneath it. | **Yes** — product as card background with gradient fade for text | You need the product to be the star. Product reveal, product showcase. |
| **Product Lifestyle** | RITUAL | Product on a counter, vanity, nightstand, travel bag. Among the objects of her life. Window present. | **Yes** — the workhorse background. Works full-bleed or contained. | You need the product in context. Timeline moments, routine sections, "what arrives." |
| **Skin Close-Up** | SKIN | Activated Terrain — cheek, jaw, temple at macro distance. Pores, texture, micro-expression. No product. | **Yes** — powerful full-bleed background, fading into dark sections. | You need the algorithm's gaze. Problem sections, profile showcases, data composites. |
| **People Lifestyle** | SKIN | Person mid-routine — applying product, hands on face, product in hand with skin visible. | **Yes** — hero backgrounds, full-bleed breathers. | You need the intersection of person and product. Heroes, timeline moments. |
| **People Without Product** | SKIN | Person living — bare skin catching light, looking away, in motion, laughing, at a window. No product anywhere. The "after" energy. | **Yes** — the strongest hero background. Full-bleed lifestyle. | You need the feeling of the outcome. Heroes, pacing resets, testimonial portraits. **This is the Hers energy.** |
| **Ingredients** | RITUAL | Botanical specimens, fruit cross-sections, raw ingredient close-ups. Science of what goes in. | **Limited** — works as contained card background, not full-bleed hero | You need to show what's inside the formula. Educational sections, ingredient spotlights. |
| **Product Texture** | CHROME/RITUAL | Cream swipes, serum pools, oil drops, texture ridges. Alone or with product sitting on its texture. | **Limited** — works as card background for texture sections only | You need sensory experience. Texture as hero, product-on-swipe for PDP. |

### Selecting Photography for a Page

A landing page should use **at least 3 different categories** from the spectrum. A page that uses only Catalog Product and Skin Close-Up looks like a medical brochure. A page that mixes People Without Product + Skin Close-Up + Product Lifestyle + Catalog Product feels like a magazine — which is the target.

**Photography variety creates content richness.** This is the single biggest lever for making a page feel like Apple or Hers instead of a template. Every scroll position should show a different kind of image.

Guidelines, not rigid assignments:

| Section type | Good photography choices | `proven-creative` shot type | Avoid |
|---|---|---|---|
| **Hero** | People Without Product, People Lifestyle, Product Lifestyle | Skin: expression variant A–C / Product Lifestyle: The Counter | Catalog Product alone, Skin Close-Up alone |
| **Problem / Educational** | Skin Close-Up, People Without Product | Skin: Cheek Terrain anchor / Skin: Jaw Line or Temple | Catalog Product |
| **Data / Composite** | Skin Close-Up with glass overlays, or no photography | Skin: any atlas angle + glass overlay | Product Lifestyle |
| **Timeline / Routine** | Product Lifestyle, People Lifestyle | Product Lifestyle: Product in Context / The Counter | People Without Product |
| **Profile** | Skin Close-Up (warmest on the page) | Skin: Cheek Terrain or Jaw Line — warmest grade | Catalog Product |
| **Product Showcase** | Catalog Product, Product Texture | Catalog: Hero shot or Card shot / Texture: Product on Swipe | Skin Close-Up |
| **Testimonial** | People Without Product (portrait) + Before/After pairs | Skin: expression variant B or D (candid) | Catalog Product |
| **Pacing Reset** | People Without Product (full-bleed), Product Lifestyle | Skin: full-body or People Lifestyle / Product Lifestyle: wide | Same category as section above |

### Shot Type Quick Reference

The shot types in the table above come from `proven-creative`. To generate the actual image brief or AI prompt, read the matching reference file:

| Shot type mentioned | Where it's defined | What you'll find |
|---|---|---|
| Skin: Cheek Terrain, Jaw Line, Temple, expression variants A–D | `proven-creative/references/skin.md` | 6-angle atlas, framing specs, expression definitions, overlay rules |
| Catalog: Hero shot, Card shot, Close-Up, Hand, Shelf | `proven-creative/references/product-catalog.md` | All packaging data, shot type definitions, channel mapping, prompt pipeline |
| Product Lifestyle: Product in Context, The Counter, Chrome Close-Up | `proven-creative/references/product-lifestyle.md` | Three Gaps framework, 4 character archetypes, surfaces, companion brands, lighting |
| Texture: Swipe Only, Product on Swipe | `proven-creative/references/ingredients.md` | Texture photography section — swipe compositions, consistency types |
| Ingredients: Botanical Specimen, Material Study | `proven-creative/references/ingredients.md` | Type 1 and Type 2 specimens, lighting, prompt templates |
| People Without Product | Not yet built in `proven-creative` | Use Skin band rules (cool light, warm materials, closeness, rose-warm axis) + no product in frame. Direct the shot yourself or flag the gap. |

**Workflow:** Pick the photography category from the spectrum table → find the shot type in this reference → invoke `proven-creative` with the shot type and your page context → receive 2 prompts → generate or brief the image → place in the section.

**Images are always backgrounds, never floating objects.** Every photography section follows the integrated card pattern: image fills the container (full-bleed or contained card), a gradient mask creates a text-safe zone, and copy lives inside the composition. No image should sit above or beside text as a separate element.

**Every image placeholder must display a visible shot brief.** The brief sits on the placeholder as readable text so builders can see what image to produce. Format — category and band, then two aspirational directions (A and B) the builder chooses from:

```
CATEGORY · BAND

A → first direction
B → second direction
```

Example:
```
PEOPLE WITHOUT PRODUCT · SKIN BAND

A → Profile silhouette, summer window light
B → Shoulders + collarbone, eyes closed, golden hour
```

The builder picks A or B, then passes it to `proven-creative` for full prompt generation. Keep directions short — one line each, aspirational not prescriptive.

**Placeholder gradients match band temperature.** The gradient background on an image placeholder previews the lighting and color of the final photograph. CHROME band placeholders use cool grey-silver tones. RITUAL band uses warm-cool interplay (linen base with cool shadows). SKIN band uses warm skin tones (rose-warm axis). This way the page reads with the right temperature even before real photography is placed.

**No two adjacent sections should use the same photography category.** If the hero uses People Without Product and the next section also uses People Without Product, one of them needs to change.

For prompt generation and full shot direction, invoke `proven-creative`.

### Hero — The Statement

Full viewport. One idea. One CTA. Maximum empty space. Every PROVEN hero requires a visual asset — photography or video. No copy-only heroes.

The hero is not a banner. It's the first thing a person sees, and it must create a moment of recognition before anything else happens. The image or video does the emotional work. The copy closes it. The CTA makes the next step feel obvious.

**On curiosity pages (landing pages, PDPs, quiz entry), the hero is always bright** — white, linen, or a sky wash. Chrome product photography on a bright surface glows and reflects the light environment: luminous, approachable, premium. Skin and ritual photography on bright surfaces let the photography carry all the warmth while the surface stays clean.

**On intent pages (about, science, campaign), the hero may open dark** — cool dark navy for brand authority statements. The user already knows PROVEN; the dark opening says "lean in."

#### Hero Layout Selection

The layout is a strategic decision, not a preference. **Layout C is the default for landing pages** — text on photography, one composition. Layout A for campaign moments. Layout B only when legibility requires full separation (complex sub-headlines, dense trust copy).

| Goal | Layout |
|------|--------|
| **Default — conversion landing pages** | **C — Floating Card Over Image** |
| Brand awareness / campaign moment | A — Full-Bleed Visual + Bottom Overlay |
| Dense copy that requires full separation | B — Stacked Image Top, Copy Bottom |

Full layout specs (mobile behavior, asset requirements, gradient math, shared rules) → see `references/frontend.md`.

### The Statement — Rich Typography, Not Empty Space

**Every text-dominant section must tell a story through typographic layers.** This applies to Statements, CTAs, brand sections — any fold where text carries the weight. Apple never puts a headline on a surface and stops. Neither does PROVEN.

**The minimum: three typographic layers in one viewport.**

1. **Display headline** — the loudest thing. Weight 900, serif accent word. What it is.
2. **Weight-shifted paragraph** — the bridge. Faded context at 30–40% opacity with the key phrase bolded to 70%+. Why it matters. One to two sentences.
3. **Evidence element** — the proof. Stat blocks (number large, label small), Signal-tagged credential, or trust line. Why it's real.

These three layers create visual rhythm through weight and opacity contrast alone — no images needed. The headline grabs. The paragraph explains (with the bold phrase pulling the eye). The evidence closes.

**What breaks it:** A headline alone. A headline + button with nothing between. A headline + paragraph at the same opacity. If everything in the section is one visual weight, it's flat — not a story.

**Text-only sections with photography behind them** also work — the Statement headline on a People Without Product or Skin Close-Up background with a dark or light overlay. The image creates mood; the text delivers the thesis.

### Timeline Narrative — The Day

Structure the page as a sequence of real moments in the user's life, anchored by timestamps (7 AM, 10 PM). Each moment is a single card: lifestyle photography fills the card, an insight chip and time badge float on the image, copy anchors at the bottom inside a gradient fade to white. The user doesn't learn about the product — they see their day with the product already in it.

Each moment card carries one data chip as a glass element on the photography — the composite in its lightest form. Cards stack vertically with 16–24px gaps. Headlines at Card tier. Body at one sentence.

### Data Showcase — The Evidence

Numbers should be enormous — proof, not data. Descriptions whisper; numbers shout. Anchor every stat to specifics. On landing pages, prefer distributing data into the Timeline Narrative. Reserve standalone showcases for science pages and press materials. Chrome product photography on cool dark becomes sculptural — edge highlights, reflections — making the product feel engineered and precise alongside the numbers.

At least one stat should carry a Signal underline or accent bar. This is Signal's natural home on dark surfaces — a 3px yellow bar beneath a white stat number, or a yellow stroke under the most important figure. If a data showcase has no Signal, the proof points aren't visually differentiated from the claims around them.

### Profile Showcase — The Portrait

The deepest recognition beat on the page. A teal dark section centered on one large card that renders the user's data as a complete portrait. Factor tiles in a grid, a visual flow from inputs to output (47 factors → 28M data points → Your Custom System), specific plausible values. The design should feel like a portrait, not a dashboard. The user looks at it and thinks: this is about me. Skin close-up photography with data overlays lives here — skin reads warm against the teal, and rose glass panels make the data feel personal. Place after the narrative, before the product reveal.

### Before & After — The Transformation

Evidence, not advertising. Real images, consistent lighting, specific context. Each pair includes skin type, location, age, timeline. Three pairs shown large on desktop (3-column grid), stacking full-width on mobile. The Signal proof tag lives on the strongest result. Before/after images at 3:4 aspect ratio — tall enough to show real skin detail.

### Product Showcase — The Resolution

The product is the conclusion of the personalization story — revealed, not introduced. One card: chrome product photography fills it, a gradient fades to white at the bottom, headline and CTA sit inside. The product and the message are one composition. Display tier headline. One sentence of body. CTA. The chrome catches light across the full card — this is the section where CHROME band photography does its best work.

### Educational Piece — The Context

One concept per section. Lead with the "so what." Progressive disclosure: insight → explanation → science. Design for the 80%, provide depth for the 100%.

### Full-Bleed Visual — The Breath

Full-viewport image or atmospheric gradient, edge to edge. Visual punctuation between content-heavy sections. Magazine-cover quality or it doesn't belong. If overlaying text, ensure the background is dark enough for readability — cool dark gradients handle this naturally; teal dark gradients at their lightest end should be checked for AA contrast. Use as a pacing reset after dense content blocks (results, features) before the next narrative beat.

### Sequence Logic

Every PROVEN page follows the same emotional arc regardless of format: **recognition → promise → evidence → conversion.** The user must feel understood before they'll believe the product works. Section order should serve that arc, not a template.

Social proof in positions 1–2, not position 5. Visitors make decisions within the first 1–2 folds.

---

## What This Skill Refuses

- **Black (#000 or near-black) as a surface or text color** — navy (#162743) is the darkest value in the PROVEN palette. Black is not a brand color. It looks sharp but it's not PROVEN.
- Timid typography — if the size range feels safe, push harder
- Cramped layouts — if it feels "efficient," add space
- Decorative animation — if you can't explain why it moves in one sentence, remove it
- Template energy — if any competitor could use this page, start over
- **Repeating the same section shape or evidence type consecutively** — every scroll position should feel like a different kind of thing
- Shadow-based depth — glass and layering only
- Circles, blobs, decorative shapes, filled icons
- Monotone color schemes — all-warm or all-cool; PROVEN needs the interplay
- Flat dark sections — dark surfaces earn depth through gradient, not flat color
- Per-card gradient patchwork — card grids use one uniform background, not four competing warm/cool treatments
- More than two non-text colors per section — if it feels like a dashboard, strip it back
- Signal (#FFFA67) as text, border, icon, large background, button, or primary CTA
- Ember (#C26A4A) on data, stats, badges, progress bars, icons, category labels, or decorative elements
- Ember and Signal inside the same component
- More than 3 Signal instances on a marketing page (denser only on data screens like quiz results)
- Data pins without values inside them — an empty pin is decoration, not intelligence
- Data pins as section labels, subtitles, or decorative accents
- Data pins beside numbers instead of containing them — the value goes inside the shape
- More than 6 data pin instances on a marketing page
- Data pins and brand hex in the same section — one or the other, never both
- Filled Ember buttons in content zones — reserve filled pills for hero and transaction contexts; use Ember text links for content navigation
- Black text-link buttons where Ember text links belong — if it navigates forward ("Learn more ›", "Shop ›"), it's Ember text, not black
- Base teal (#7295A2) on linen backgrounds or dark surfaces — use `--teal-dark` on linen, `--teal-light` on dark
- Body text below WCAG AA contrast (4.5:1 for small text, 3:1 for large) — bump opacity by 0.1 if in doubt
- White text on teal dark gradients without contrast verification at the lightest point
- Fear-based copy ("fight aging"), hedging ("we believe"), exclamation marks
- Passive voice in headlines, rhetorical questions in heroes
- Isolated data sections on landing pages (distribute into narrative)
- Testimonials in grids disconnected from what they validate (embed contextually)
- Sections with more than 2–3 lines of body copy — cut in half. Confidence is brevity.
- Image-beside-copy split layouts — text lives on images, not next to them. One surface, one composition.
- **Text sections with fewer than three typographic layers** — headline alone, or headline + button with nothing between, wastes the fold. Every text-dominant section needs headline + weight-shifted paragraph + evidence element.

---

*The goal is not a nice website. The goal is a moment of recognition — where someone looks at a screen and thinks, for the first time, "this brand actually gets me." Everything serves that moment, or it goes.*
