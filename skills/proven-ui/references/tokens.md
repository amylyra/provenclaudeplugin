# PROVEN Design System — Token Reference

Component tokens, CSS patterns, and specs. This is the lookup layer — find the piece you need and use it precisely.

**Prerequisite:** Read the hub `SKILL.md` first.

---

## CSS Custom Properties

Include once per page. These are the canonical values — `references/frontend.md` references this block.

```css
:root {
  /* Canvas & Warm */
  --white: #FFFFFF;
  --linen: #FAF6F2;
  --sand:  #E6DED4;
  --rose:  #DDBFB0;

  /* Cool */
  --sky:   #BCD4E2;

  /* Teal — three registers */
  --teal:       #7295A2;  /* On pure white only */
  --teal-dark:  #4A6D7C;  /* On linen or any off-white */
  --teal-light: #8CAEB9;  /* On dark surfaces */

  /* Structure */
  --navy:  #162743;
  --black: #000000;

  /* Action */
  --ember:       #C26A4A;
  --ember-hover: #A85A3E;
  --ember-dark:  #E08A6A;

  /* Evidence */
  --signal: #FFFA67;

  /* Domain tint */
  --sage: #5E7D7A;

  /* Data Visualization — domain encoding (shape fills only, never text) */
  --data-rose:        #DDBFB0;  /* Genetics & skin type */
  --data-tangerine:   #D88C52;  /* Hormones, age & stress */
  --data-sky:         #BCD4E2;  /* Climate, season & humidity */
  --data-teal-bright: #6AABB2;  /* Water, location & pollution */
  --data-teal:        #7295A2;  /* Lifestyle, sleep & routine */
  --data-signal:      #FFFA67;  /* Outcome & proof */

  /* Data Highlights — pins & dots only, max 1–3 per viewport */
  --highlight-gold:      #F5B840;
  --highlight-tangerine: #F09030;
  --highlight-emerald:   #3CC8B0;
  --highlight-blue:      #5CA8F0;
  --highlight-coral:     #F07058;
  --highlight-purple:    #A878E0;
  --highlight-rose:      #F05878;
}
```

---

## Type Scale

### Headline Tiers

| Tier | Size | Weight | Tracking | Line-height | Use |
|---|---|---|---|---|---|
| **Display** | `clamp(36px, 9vw, 80px)` | 900 | −0.05em | 0.9 | Hero, statement, data showcase, final CTA |
| **Section** | `clamp(28px, 6vw, 56px)` | 900 | −0.045em | 0.92 | Problem cards, results, in-page section headlines |
| **Card** | `clamp(24px, 4.5vw, 42px)` | 800 | −0.04em | 0.95 | Timeline moments, product cards, contained headlines |

### Stat Numbers

| Context | Size | Weight | Tracking |
|---|---|---|---|
| Stat on dark | `clamp(56px, 11vw, 104px)` | 900 | −0.06em |
| Glass stat (over photography) | `clamp(28px, 4vw, 48px)` | 800 | −0.04em |

### Body & Labels

| Level | Size | Weight | Tracking | Line-height |
|---|---|---|---|---|
| Body | 13–14px | 500 | 0 | 1.5–1.55 |
| Sub-headline | 14–16px | 500 | +0.01em | 1.55 |
| Label | 10–11px | 800 | +0.16em | 1.4 |
| Micro label | 9px | 700 | +0.12em | 1.35 |
| Trust copy | 10–11px | 500 | +0.02em | 1.4 |

### Source Serif 4 Accent

When used inside a headline, Source Serif 4 italic at **weight 700** — matching the visual mass of the surrounding Albert Sans 900. The style shift is the event. `letter-spacing: -0.02em`.

---

## Spacing Scale

`4 → 8 → 16 → 24 → 32 → 48 → 80 → 120 → 160 → 200px`

Skip steps aggressively. Interior spacing (16–24px) should feel categorically different from section spacing (120–200px).

**Section padding as pacing:** 200px on desktop, 120px on mobile. A page with ten sections at 200px padding feels like ten rooms. The same page at 80px padding feels like one long hallway.

---

## Readability — Minimum Opacity Values

### Dark surfaces (cool dark, teal dark, navy)

| Element | Minimum |
|---|---|
| Body text / descriptions | `rgba(255,255,255, 0.55)` |
| Subheadlines / secondary | `rgba(255,255,255, 0.60)` |
| Hero sub-headlines | `rgba(255,255,255, 0.70)` |
| Labels / metadata | `--teal-light` (#8CAEB9) |
| Tags / pills | `rgba(255,255,255, 0.55)` |
| Footer text | `rgba(255,255,255, 0.50)` minimum |
| Decorative (ghost numbers) | No minimum — intentionally invisible |

### Light surfaces (white, linen)

| Element | Minimum |
|---|---|
| Body text on linen | `rgba(0,0,0, 0.58)` |
| Body text on white | `rgba(0,0,0, 0.55)` |
| Subtext / secondary | `rgba(0,0,0, 0.60)` |
| Card descriptions at 13–15px | `rgba(0,0,0, 0.58)` |
| Labels on linen | `--teal-dark` (#4A6D7C) |
| Labels on white | `--teal` (#7295A2) |

### Overlaid text on gradients/photography

Cool dark gradients pass white text contrast naturally. Teal dark gradients at their lightest end should be checked for AA compliance. Over photography, add a dark scrim overlay if the image is too light. 3:1 minimum for large text, 4.5:1 for body.

**The rule:** When in doubt, bump opacity by 0.1. The page earns authority through spacing and typography — not by making body copy disappear.

---

## Button System — Full Vocabulary

Every button is pill-shaped (`border-radius: 9999px`). Shape is sacred. Fill, color, and opacity adapt.

### On Light Backgrounds (white, linen, warm gradients)

| Style | CSS | Purpose | Example |
|---|---|---|---|
| Ember filled pill | `background: var(--ember); color: #fff` | Primary commitment | "Get started", "Take the quiz" |
| Ember outline pill | `box-shadow: inset 0 0 0 1.5px var(--ember); color: var(--ember)` | Hero secondary only, paired with filled Ember | "Learn more" |
| Ember text link | `color: var(--ember)` + arrow character | Content navigation | "Learn more ›", "Shop now ›" |
| Black outline pill | `box-shadow: inset 0 0 0 1px rgba(0,0,0,0.25); color: var(--black)` | Content secondary, utility | "Compare systems" |
| Black text link | `color: var(--black)` + subtle underline | Inline paragraph links | Links within body copy |

### On Dark Backgrounds (cool dark and teal dark gradients)

Both dark registers use the same vocabulary. Glass tinting uses neutral glass (`rgba(255,255,255,0.08)`) on cool dark, and slightly warmer glass (`rgba(255,255,255,0.10)`) on teal dark.

| Style | CSS | Purpose | Example |
|---|---|---|---|
| White filled pill | `background: #fff; color: var(--black)` | Primary action on dark | "Get started", "Shop now" |
| Glass pill | `background: rgba(255,255,255,0.15); backdrop-filter: blur(20px); color: #fff` | Secondary on dark | "Explore", "See details" |
| Dark pill + Ember icon | `background: rgba(255,255,255,0.08); color: #fff` with small Ember circle containing icon | Utility/expand on dark | "Compare [+]" |
| Ember-dark text link | `color: var(--ember-dark)` + arrow | Content navigation on dark | "Learn more ›" |
| White text link | `color: rgba(255,255,255,0.85)` + arrow | Secondary navigation on dark | "Details ›" |

### On Photography (lifestyle images, hero images with overlaid text)

| Style | CSS | Purpose | Example |
|---|---|---|---|
| White filled pill | `background: #fff; color: var(--black)` | Primary action over photos | "Get started" |
| Warm glass pill | `background: rgba(255,255,255,0.25); backdrop-filter: saturate(120%) blur(16px); color: #fff` | Secondary over photos | "See if I'm eligible" |
| Glass pill (cool) | `background: rgba(255,255,255,0.15); backdrop-filter: saturate(180%) blur(20px); color: #fff` | Alternate secondary | "Learn more" |

### Key Pairings

- **Hero on light:** Ember filled pill + Ember outline pill
- **Hero on dark/photography:** White filled pill + glass pill
- **Content zone:** Ember text links carry navigational rhythm. Black outline pills for secondary utility. No filled Ember buttons in content.
- **Dark section:** White filled pill (primary) + glass pill (secondary)
- **Utility with icon accent:** Neutral pill with small Ember-filled circle containing `+`, `→`. The button doesn't become Ember — it contains a small Ember element.

---

## Signal — Usage Specs

- **Proof tags** — small pill-shaped labels: "Clinically tested," "93% effective." Max 2 per card, max 3 per marketing page.
- **Stat underlines** — yellow stroke beneath key data numbers. Use on 1–2 hero stats, not every number.
- **Dark card accent bars** — small 3px yellow bars beneath white stats on dark backgrounds.
- **Result card data** — Signal's one dense moment: quiz results, skin profiles, ingredient match pills.
- **Trust badges** — one per form maximum. "🔒 Encrypted" near checkout.

**Signal never appears as:** Buttons, links, or any interactive element. Text color, icon tint, or section borders. Section backgrounds or card fills. Inside the same component as Ember.

---

## Glass Components

| Component | Use | Tint |
|---|---|---|
| **Stat panels** | Large numbers + descriptors floating over photography | White or warm |
| **Insight chips** | Single data points (pill-shaped) — always contextual over photography, never collected in grids | White |
| **Mock UI cards** | Quiz outputs, progress bars, formula breakdowns | White fill (solid for dense info) |
| **Profile cards** | Factor clusters, skin summaries, comparisons | Rose for personal, Sky for scientific |
| **Progressive stacks** | Layered cards showing input → output sequence | Varying opacity per layer |
| **Floating UI** | Nav, filter bars, sticky CTAs | Match section beneath |

Glass is not decoration. Every glass element carries content. Standard content cards use solid fills — glass appears when content needs to coexist with what's behind it.

### Glass-on-Photography Pairing (Composites)

| Photography type | Glass tint | Lead panel content | Max panels |
|---|---|---|---|
| Skin close-up | Rose glass | Personal factor ("Your hydration: 72%") | 3 |
| Lifestyle / routine | White glass or warm glass | Contextual insight ("47 factors analyzed") | 2 |
| Product (chrome) | Not glass — use Signal proof tag | Trust credential ("MIT AI, 2018") | 1 |
| Dark section (no photo) | Neutral glass on navy/teal | Large stat number | 2 |

---

## Glass CSS Tokens

```css
/* White glass (default) */
background: rgba(255, 255, 255, 0.72);
backdrop-filter: saturate(180%) blur(20px);

/* Warm glass */
background: rgba(250, 246, 242, 0.72);
backdrop-filter: saturate(180%) blur(20px);

/* Rose glass (personal data) */
background: rgba(221, 191, 176, 0.25);
backdrop-filter: saturate(160%) blur(16px);

/* Sky glass (scientific data) */
background: rgba(188, 212, 226, 0.25);
backdrop-filter: saturate(180%) blur(16px);

/* Glass stat panel (over photography) */
background: rgba(255, 255, 255, 0.65);
backdrop-filter: saturate(180%) blur(16px);
border-radius: 16px;

/* Glass on cool dark surfaces */
background: rgba(255, 255, 255, 0.08);
backdrop-filter: saturate(180%) blur(20px);

/* Glass on teal dark surfaces */
background: rgba(255, 255, 255, 0.10);
backdrop-filter: saturate(160%) blur(20px);
```

---

## Gradient Tokens

### Light Surface Gradients

```css
/* White → warm */
background: linear-gradient(180deg, #FFFFFF 0%, #FAF6F2 50%, #F5F0EA 100%);

/* White → cool */
background: linear-gradient(180deg, #FFFFFF 0%, #EEF3F7 50%, #E4EDF2 100%);

/* Warm-to-cool drift (signature PROVEN gradient) */
background: radial-gradient(ellipse at 50% 40%, #FFFFFF 0%, #FAF6F2 40%, #EBF0F0 100%);
```

**Rule:** If someone can immediately *see* a gradient on a light surface, it's too strong — it should register as a feeling. Dark surface gradients are the exception: the drift is intentional and perceptible.

### Dark Surface Gradients

```css
/* Cool dark (science, data, authority) */
background: linear-gradient(160deg, #162743 0%, #1a3148 40%, #1d3a52 100%);

/* Cool dark — atmospheric (teal/sky drift) */
background: linear-gradient(170deg, #162743 0%, #1b3550 50%, #1e4258 100%);

/* Cool dark — radial depth */
background: radial-gradient(ellipse at 30% 70%, #1e4258 0%, #162743 60%, #111e33 100%);

/* Teal dark — linear */
background: linear-gradient(160deg, #3a5a68 0%, #4A6D7C 40%, #5f8594 100%);

/* Teal dark — full ramp (teal dark → teal) */
background: linear-gradient(150deg, #4A6D7C 0%, #5f8594 45%, #7295A2 100%);

/* Teal dark — radial depth */
background: radial-gradient(ellipse at 50% 50%, #7295A2 0%, #5a8090 40%, #3a5a68 100%);
```

### Domain Tint Gradients (Light Surfaces)

Whisper-soft section backgrounds for factor-domain content. The tint should register as atmosphere — visible but not named.

```css
/* Rose domain (biology, skin, personalization) — ~10–12% */
background: linear-gradient(180deg, #FFFFFF 0%, rgba(221,191,176,0.12) 100%);

/* Sky domain (environment, climate, intelligence) — ~12–14% */
background: linear-gradient(180deg, #FFFFFF 0%, rgba(188,212,226,0.14) 100%);

/* Sage domain (lifestyle, routine, wellness) — ~8–10% */
background: linear-gradient(180deg, #FFFFFF 0%, rgba(94,125,122,0.09) 100%);
```

### When to Use Which Dark Register

| Content type | Dark register | Why |
|---|---|---|
| Data showcase / stat sections | Cool dark | Evidence is objective — cool conveys rigor |
| Science / methodology | Cool dark | Research lives in the analytical register |
| Final CTA / commitment | Cool dark | The last moment carries authority |
| Brand statement (intent pages) | Cool dark | Authority earns trust |
| Factor breakdown / profile data | Teal dark | The system showing its work — softer authority |
| Profile reveal, recognition beats | Teal dark | Showing the user their data, personal but systematic |
| Routine / system explanation | Teal dark | Engineered system presented accessibly |

### Image Placeholder Gradients (by Band)

Preview the final photograph's temperature. Use these on placeholder areas before real photography is placed.

```css
/* CHROME band — cool, grey-silver, neutral */
background: linear-gradient(155deg, #e8e8e8 0%, #dddcda 20%, #d0ceca 40%, #c8c6c2 60%, #c0bcb8 80%, #b8b4b0 100%);

/* RITUAL band — warm-cool interplay, linen base, cool shadows */
background: linear-gradient(150deg, #e8ddd2 0%, #ddd0c4 25%, #d0c2b4 50%, #c4b6a8 75%, #bcaea0 100%);

/* SKIN band — warmest, skin tones, rose-warm axis */
background: linear-gradient(145deg, #c8b8a4 0%, #baa88e 30%, #a89474 60%, #c0ac90 100%);
```
| Formula / ingredient context | Teal dark | The system's output, grounded |

---

## Data Pin — CSS Pattern

The pin is a container. The value goes inside, positioned above center (the shape tapers at bottom).

```css
.pin-stat {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  position: relative;
  flex-shrink: 0;
}
.pin-stat svg { display: block; }
.pin-stat-val {
  position: absolute;
  top: 37%;                    /* Above center — shape tapers at bottom */
  left: 50%;
  transform: translate(-50%, -50%);
  font-weight: 800;
  letter-spacing: -0.03em;
  color: #fff;                 /* var(--navy) on light fills */
  line-height: 1;
}
```

### Pin Fill Colors by Context

| Context | Fill | Semantic |
|---|---|---|
| Data point on dark surface | `rgba(255,255,255,0.10)` | Subtle — value inside dominates |
| Environmental factor (climate) | `var(--data-sky)` | Cool = external (UV, climate, altitude) |
| Environmental factor (water/location) | `var(--data-teal-bright)` | Cool = water, pollution, geography |
| Biological factor (genetics, barrier) | `var(--data-rose)` | Warm = internal (barrier, skin type) |
| Biological factor (age, hormones) | `var(--data-tangerine)` | Warm = hormonal, age-related |
| Lifestyle factor | `var(--data-teal)` | Neutral = behavioral (sleep, routine, stress) |
| Result / measured outcome | `rgba(255,250,103,0.12)` | Signal tint = proof |
| **Emphasis / highlighted factor** | `var(--highlight-gold)` etc. | **Bright highlight — max 3 pins per page** |
| Exit intent / profile save | `rgba(114,149,162,0.12)` | Teal tint = personalization state |

**Pin text color rule:** Value text inside pins always uses `#fff` on dark fills and `var(--navy)` on light fills. Never use data viz or highlight colors as pin text.

---

## Data Visualization Colors

Six domain colors for data fills and strokes. These encode factor categories across charts, gauges, tags, and profile visualizations.

| Token | Hex | Domain | Use as |
|---|---|---|---|
| `--data-rose` | `#DDBFB0` | Genetics & skin type | Bar fill, donut stroke, gauge ring, tag bg, dot |
| `--data-tangerine` | `#D88C52` | Hormones, age & stress | Same — splits biological into two voices |
| `--data-sky` | `#BCD4E2` | Climate, season & humidity | Same — ambient environmental |
| `--data-teal-bright` | `#6AABB2` | Water, location & pollution | Same — splits environmental from climate |
| `--data-teal` | `#7295A2` | Lifestyle, sleep & routine | Same — behavioral factors |
| `--data-signal` | `#FFFA67` | Outcome & proof | Gauge ring, chart segment for match/result |

### Usage on light surfaces (white, linen, domain-tinted)

- **Bar fills:** Solid base color, pill-shaped (`border-radius: 9999px`), 6–8px height. Track: `rgba(0,0,0,0.04)`.
- **Tag pills:** Base color at 20–25% opacity as background. Dark text (use core palette navy). 6–8px domain dot inside.
- **Donut strokes:** Base color, 18–22px stroke-width, `stroke-linecap: round`.
- **Domain dots:** 6–10px circles in base color beside labels or inside rows.

### Usage on dark surfaces (navy, teal dark)

- **Bar fills:** Solid base color or left-to-right gradient (darker → base). Track: `rgba(255,255,255,0.06)`.
- **Gauge rings:** Base color, 8–10px stroke-width, `stroke-linecap: round`. Track: `rgba(255,255,255,0.06)`.
- **Stat card tints:** `rgba(base, 0.05–0.10)` as card background. Text inside always white.
- **Domain dots:** Base color, same sizing.

### Text rule (hard constraint)

Numbers, labels, and all text on data visualizations use **core palette colors only**. Navy (`var(--navy)`) on light surfaces. White (`#fff`) on dark surfaces. Data viz colors never appear as text — they are shape fills only.

---

## Data Highlight Colors

Seven bright accent colors. Used exclusively for Data Pin fills and small indicator dots (5–6px). Maximum 1–3 per viewport. These are emphasis markers — punctuation on the data layer.

| Token | Hex | Priority |
|---|---|---|
| `--highlight-gold` | `#F5B840` | Primary — lead highlight |
| `--highlight-tangerine` | `#F09030` | Primary — warm emphasis |
| `--highlight-emerald` | `#3CC8B0` | Primary — cool emphasis |
| `--highlight-blue` | `#5CA8F0` | Primary — data callout |
| `--highlight-coral` | `#F07058` | Supporting — attention, change |
| `--highlight-purple` | `#A878E0` | Supporting — adaptive, behavioral |
| `--highlight-rose` | `#F05878` | Supporting — urgency, flags |

**Hierarchy:** Gold → Tangerine → Emerald → Blue are the first four. Coral, Purple, and Rose are supporting — use only when the primary four are already in play.

**Where highlights appear:** Data Pin fills (the pin SVG shape, white text inside). Indicator dots (5–6px) beside legend items or gauge values. Badge pills on dense data screens (quiz results).

**Where highlights never appear:** Bar chart fills, donut strokes, gauge rings (use data viz tier). Text color. Section backgrounds. Card fills. Buttons. Any component larger than a pin or small dot.

---

## Motion Tokens

Three tiers. Never mix. Never loop.

**Scroll-bound transformations** — content morphs, numbers count up, locked to scroll position. One or two per page maximum.

**Scroll-triggered reveals** — default for most content:
```css
/* Base reveal */
opacity: 0;
transform: translateY(40px);
transition: opacity 0.8s cubic-bezier(0.16, 1, 0.3, 1),
            transform 0.8s cubic-bezier(0.16, 1, 0.3, 1);

/* Stagger siblings */
transition-delay: 80ms; /* add 80–150ms per sibling */
```

**Micro-interactions** — hovers and state changes:
```css
transition: 150ms ease-out;
/* Nothing bounces, pulses, or loops */
```

---

## Two-Icon SVG Definitions

Include once per page. Reuse via `<use href="#logo"/>` and `<use href="#pin"/>`.

```html
<svg style="position:absolute;width:0;height:0" aria-hidden="true">
  <defs>
    <symbol id="logo" viewBox="0 0 93 107">
      <path d="M93 39.2928V26.9812L82.3545 20.8254L74.6243 25.2969L57.2709 15.264V6.1558L46.6253 0L35.9798 6.1558V15.264L18.5011 25.3696L10.6455 20.8254L0 26.9812V39.2928L8.2117 44.0417V63.2687L0 68.0309V80.3425L10.6455 86.4983L18.7187 81.8286L35.9798 91.8086V100.857L46.6253 107L57.2709 100.844V91.8086L74.4198 81.9012L82.3347 86.5247L93 80.3293V68.0309L85.0389 63.4074V43.8964L93 39.2928ZM41.3157 9.24691L46.5923 6.17562L51.8689 9.24691V15.3895L46.5923 18.4608L41.3157 15.3895V9.24691ZM5.33596 36.2083V30.0657L10.6455 27.001L15.9551 30.0657V36.2083L10.6785 39.2796L5.33596 36.2083ZM15.9551 77.2778L10.6785 80.3491L5.40191 77.2778V71.1352L10.6455 68.0309L15.9551 71.1022V77.2778ZM51.9349 97.7531L46.6583 100.824L41.3817 97.7531V91.6105L46.6583 88.5392L51.9349 91.6105V97.7531ZM71.7221 68.0309V77.2778L54.7447 87.0795L46.6121 82.3768L38.4796 87.0795L21.2779 77.1721V68.0309L13.5477 63.5395V43.7709L21.2911 39.2928V29.927L38.5455 19.9535L46.6253 24.6232L54.6985 19.9535L71.7089 29.7817V39.2928L79.703 43.9162V63.4074L71.7221 68.0309ZM87.6772 71.1154V77.2778L82.4006 80.3491L77.124 77.2778V71.1352L82.4006 68.0639L87.6772 71.1154ZM82.4006 39.2928L77.124 36.2215V30.0789L82.4006 27.0142L87.6772 30.0789V36.2215L82.4006 39.2928Z"/>
    </symbol>
    <symbol id="pin" viewBox="0 0 135 208">
      <path d="M0 116.483V38.838L67.2439 0L134.488 38.8225V116.468L67.2439 207.666L0 116.483ZM14.8366 47.3999V107.921L67.2439 138.182L119.651 107.921V47.3999L67.2439 17.1394L14.8366 47.3999Z"/>
    </symbol>
  </defs>
</svg>
```
