# PROVEN UI — Frontend Build Reference

Implementation patterns for building PROVEN pages. Covers CSS foundation, grid system, breakpoints, component HTML/CSS, animation JS, and responsive image handling. The design rules (color semantics, typography, principles, section vocabulary) live in the other reference files — this file is the code layer.

**Prerequisite:** Read the hub `SKILL.md` first — it contains all design rules, color semantics, typography, and section vocabulary.

---

## CSS Foundation

### Font Import

```css
@import url('https://fonts.googleapis.com/css2?family=Albert+Sans:wght@300;400;500;600;700;800;900&family=Source+Serif+4:ital,wght@0,300;0,400;0,500;0,600;0,700;0,800;1,300;1,400;1,500;1,600;1,700;1,800&display=swap');
```

### Color Custom Properties

Defined in `references/tokens.md` — copy the full `:root` block from there. Do not maintain a second copy here.

---

## Breakpoints

```css
/* Mobile first. Add complexity upward. */
@media (max-width: 480px)  { /* xs — phones */ }
@media (max-width: 768px)  { /* sm — primary mobile target */ }
@media (max-width: 1024px) { /* md — tablet */ }
```

---

## Grid & Layout System

### Page Container

```css
.page-container {
  width: 100%;
  max-width: 1440px;
  margin: 0 auto;
}

.content-container {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 48px;
}

@media (max-width: 768px) {
  .content-container {
    padding: 0 24px;
  }
}
```

### Column Grid

12-column base. Most sections use a subset:

| Layout | Columns | Use |
|---|---|---|
| Full bleed | 12/12 | Hero images, dark section backgrounds, photography |
| Wide content | 10/12 centered | Section headlines, single-column body |
| Standard | 8/12 centered | Body copy, single stat, quiz cards |
| Two-column | 5+5 or 6+6 | Comparison, product + copy, image + text |
| Three-column | 4+4+4 | Feature cards, stat triptych |
| Four-column | 3+3+3+3 | Small cards, ingredient grid |
| Asymmetric | 7+5 or 6+4 | Hero with floating card, copy-heavy + visual |

```css
.grid {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  gap: 24px;
}

/* Common span helpers */
.col-4  { grid-column: span 4; }
.col-5  { grid-column: span 5; }
.col-6  { grid-column: span 6; }
.col-7  { grid-column: span 7; }
.col-8  { grid-column: span 8; }
.col-10 { grid-column: span 10; }
.col-12 { grid-column: span 12; }
.col-center-8  { grid-column: 3 / span 8; }
.col-center-10 { grid-column: 2 / span 10; }
```

### Column Collapse Patterns

```css
/* Standard: 3-col desktop → 1-col mobile */
.card-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}

@media (max-width: 768px) {
  .card-grid {
    grid-template-columns: 1fr;
    gap: 16px;
  }
}

/* Two-col: stays two-col at tablet, collapses at mobile */
.two-col {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 48px;
  align-items: center;
}

@media (max-width: 768px) {
  .two-col {
    grid-template-columns: 1fr;
    gap: 32px;
  }
  /* Stack image below text on mobile unless image-first layout */
  .two-col .visual { order: 2; }
  .two-col .copy   { order: 1; }
}
```

---

## Responsive Image Patterns

```css
/* Standard responsive image */
.responsive-image {
  width: 100%;
  height: auto;
  display: block;
}

/* Hero image */
.hero-image {
  width: 100%;
  aspect-ratio: 16/9;
  object-fit: cover;
}

@media (max-width: 768px) {
  .hero-image {
    aspect-ratio: 4/5;
  }
}
```

---

## Hero Layout Specifications

Three layouts. Choose based on page goal — see the selection table in `SKILL.md`.

### Layout A — Full-Bleed Visual + Bottom Overlay
*Reference: Tatcha, Augustinus Bader*

A photo or video fills the entire screen. A dark gradient rises from the bottom 60–65% of the frame, creating a text-safe zone. Copy and CTA sit in this lower zone.

Use when: Brand awareness, campaign pages, moments where the lifestyle image or process video should overwhelm the first impression. Not ideal as a primary conversion hero — the visual competes for attention with the CTA.

**Asset requirements:** Lifestyle or skin photography, or 6–12 second muted video loop — both vertically composed. Bottom third must be naturally dark or able to accept a dark gradient. Video must have a poster frame fallback. Mute/unmute control top-right required for video.

**Gradient requirements:** The text-safe gradient must start no higher than 65% from the top. The gradient midpoint must reach no lighter than `#5f4a3a` for white text to pass WCAG AA. If the image is naturally light at the bottom, add `rgba(0,0,0,0.35–0.45)` overlay before applying the gradient. Test in actual conditions — don't assume a gradient will hold.

**Mobile behavior:** The gradient text-safe zone must occupy at minimum the bottom 50% of the viewport at 375px. Headline at `clamp(32px, 8vw, 52px)`. Subhead is optional — if it pushes the CTA above 80% screen height, remove it. CTA sits flush to the bottom of the gradient zone.

### Layout B — Stacked Image Top, Copy Bottom
*Reference: Ritual, Hims, Care/of, Curology*

Image panel occupies the top ~45% of the mobile viewport. Below, a clean white or linen surface holds the headline, subhead, and full-width CTA. No contrast battles.

Use when: The page needs to communicate product tangibly before asking for action. Effective for paid traffic landing pages and concern-specific pages.

**Asset requirements:** Photography that reads clearly at a 9:16 crop in the top 45% of a phone screen. Product arrangement, lifestyle close-up, or skin texture.

**Mobile behavior:** Image fixed at `40–45vh` — never taller or the CTA falls below the fold. If headline + subhead + CTA don't fit above the fold at 375px, drop the subhead first.

### Layout C — Floating Card Over Image
*Reference: Glossier, Dieux, Summer Fridays*

Lifestyle photography fills the background. A white or near-white card anchors to the bottom of the frame with a full-width CTA inside it. Trust micro-copy sits directly below the CTA button inside the card.

Use when: A page needs warmth from photography but also needs dense, legible copy.

**Asset requirements:** Lifestyle photography, portrait-oriented. The upper 55–60% of the image needs visual interest — the card covers the lower portion.

**Mobile behavior:** The card covers the bottom 40–45% of the viewport. Primary subject must be in the upper 55% of the frame. Card uses `border-radius: 16px 16px 0 0` and sits flush to the bottom edge. CTA inside the card is full-width.

### Shared Rules for All Hero Layouts

**Photography first, 9:16.** Shoot all hero assets vertical. 9:16 fills a mobile phone without cropping decisions at render time. If only horizontal photography exists, Layout B is the safest choice.

**One visual idea per image.** The hero photo sets a single emotional tone — intimacy of skin texture, warmth of a face in real light, or precision of a product arrangement. Mixed intent reads as unfocused.

**Full-width CTA on mobile.** Every layout uses a full-width CTA button on mobile (`width: calc(100% - 32px)` minimum). Centered compact buttons reduce tap target size and signal the action is optional. It isn't.

**Trust micro-copy placement.** One line, 11–12px, center-aligned, directly beneath the CTA button: "3 min · No card required · 100K+ formulas." This answers the hesitation at the exact moment it forms.

**CTA in thumb zone.** On mobile, the primary CTA must sit between 60–80% of the screen height on first load at 375px. If it requires scroll, the layout is too tall.

**Dark surface register.** On curiosity pages (landing pages, PDPs, quiz entry), heroes are always bright — white, linen, or a subtle light gradient. On intent pages (about, science, campaign), the hero may use cool dark (navy) for authority. Teal dark is not used for heroes.

---

## Component Patterns

### Stat Card

```html
<div class="stat-card">
  <div class="stat-number">93<span class="stat-unit">%</span></div>
  <div class="stat-underline"></div>
  <p class="stat-label">reported improvement within 30 days</p>
</div>
```

```css
.stat-card {
  text-align: center;
  padding: 40px 32px;
}

.stat-number {
  font-size: clamp(48px, 6vw, 96px);
  font-weight: 800;
  letter-spacing: -0.04em;
  line-height: 1;
  color: var(--navy);
}

.stat-unit {
  font-size: 0.5em;
  vertical-align: super;
}

.stat-underline {
  width: 48px;
  height: 3px;
  background: var(--signal);
  margin: 16px auto 20px;
}

.stat-label {
  font-size: 15px;
  color: rgba(0,0,0,0.55);
  max-width: 180px;
  margin: 0 auto;
  line-height: 1.5;
}
```

### Quiz Result / Profile Card

```html
<div class="profile-card glass-rose">
  <div class="profile-card-header">
    <span class="profile-label">Your Skin Profile</span>
    <span class="profile-tag">Sensitive · Dry</span>
  </div>
  <div class="profile-factors">
    <!-- factor rows -->
  </div>
</div>
```

```css
.profile-card {
  border-radius: 20px;
  padding: 32px;
  background: rgba(221, 191, 176, 0.25);
  backdrop-filter: saturate(160%) blur(16px);
  border: 1px solid rgba(221, 191, 176, 0.3);
}

.profile-label {
  font-size: 13px;
  font-weight: 600;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: var(--teal-dark);
}

.profile-tag {
  font-size: 13px;
  font-weight: 500;
  color: rgba(0,0,0,0.5);
  padding: 4px 10px;
  background: rgba(0,0,0,0.06);
  border-radius: 9999px;
}
```

### Testimonial

```html
<figure class="testimonial">
  <blockquote>
    <p>My derm asked what I changed. It was one brand.</p>
  </blockquote>
  <figcaption>
    <span class="testimonial-name">Sarah K.</span>
    <span class="testimonial-meta">Combination · San Francisco · 6 weeks</span>
  </figcaption>
</figure>
```

```css
.testimonial {
  border-left: 3px solid var(--rose);
  padding-left: 24px;
  margin: 0;
}

.testimonial blockquote p {
  font-family: 'Source Serif 4', serif;
  font-style: italic;
  font-size: clamp(18px, 2vw, 24px);
  font-weight: 400;
  line-height: 1.5;
  color: var(--navy);
  margin: 0 0 16px;
}

.testimonial-name {
  font-weight: 600;
  font-size: 14px;
  display: block;
}

.testimonial-meta {
  font-size: 13px;
  color: rgba(0,0,0,0.45);
}
```

### Navigation

```css
.nav {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 100;
  height: 72px;
  display: flex;
  align-items: center;
  background: rgba(255, 255, 255, 0.85);
  backdrop-filter: saturate(180%) blur(20px);
  border-bottom: 1px solid rgba(0,0,0,0.06);
  transition: background 0.3s ease;
}

/* Over dark/photography sections */
.nav.nav-dark {
  background: rgba(22, 39, 67, 0.5);
  border-bottom: 1px solid rgba(255,255,255,0.08);
}

@media (max-width: 768px) {
  .nav { height: 60px; }
  .nav-links { display: none; }
  .nav-hamburger { display: flex; }
}
```

---

## Animation Implementation

All animation uses the Intersection Observer API — no scroll event listeners. Three tiers map to `tokens.md` motion values.

### Base Scroll-Triggered Reveal

Apply `data-reveal` to any element that should fade in on scroll. JS handles the rest.

```html
<div data-reveal>...</div>
<div data-reveal data-reveal-delay="80">...</div>   <!-- stagger siblings -->
<div data-reveal data-reveal-delay="160">...</div>
```

```css
[data-reveal] {
  opacity: 0;
  transform: translateY(40px);
  transition: opacity 0.8s cubic-bezier(0.16, 1, 0.3, 1),
              transform 0.8s cubic-bezier(0.16, 1, 0.3, 1);
}

[data-reveal].revealed {
  opacity: 1;
  transform: translateY(0);
}
```

```js
// Reveal observer — include once per page
const revealObserver = new IntersectionObserver((entries) => {
  entries.forEach(el => {
    if (el.isIntersecting) {
      const delay = el.target.dataset.revealDelay || 0;
      setTimeout(() => el.target.classList.add('revealed'), Number(delay));
      revealObserver.unobserve(el.target);
    }
  });
}, { threshold: 0.15 });

document.querySelectorAll('[data-reveal]').forEach(el => revealObserver.observe(el));
```

### Scroll-Bound Number Counter

One or two per page maximum. Numbers count up as the element enters the viewport.

```html
<span class="count-up" data-target="93" data-suffix="%">0%</span>
```

```js
const counterObserver = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (!entry.isIntersecting) return;
    const el = entry.target;
    const target = parseInt(el.dataset.target, 10);
    const suffix = el.dataset.suffix || '';
    const duration = 1600;
    const start = performance.now();

    const tick = (now) => {
      const progress = Math.min((now - start) / duration, 1);
      const eased = 1 - Math.pow(1 - progress, 3); // ease-out cubic
      el.textContent = Math.round(eased * target) + suffix;
      if (progress < 1) requestAnimationFrame(tick);
    };

    requestAnimationFrame(tick);
    counterObserver.unobserve(el);
  });
}, { threshold: 0.5 });

document.querySelectorAll('.count-up').forEach(el => counterObserver.observe(el));
```

### Scroll-Bound Progress Bar

For ingredient match bars, result fill indicators, profile completeness.

```html
<div class="progress-bar" data-fill="78">
  <div class="progress-fill"></div>
</div>
```

```css
.progress-bar {
  height: 4px;
  background: rgba(0,0,0,0.08);
  border-radius: 9999px;
  overflow: hidden;
}

.progress-fill {
  height: 100%;
  width: 0%;
  background: var(--teal);
  border-radius: 9999px;
  transition: width 1.2s cubic-bezier(0.16, 1, 0.3, 1);
}
```

```js
const progressObserver = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (!entry.isIntersecting) return;
    const fill = entry.target.querySelector('.progress-fill');
    const pct = entry.target.dataset.fill || 0;
    fill.style.width = pct + '%';
    progressObserver.unobserve(entry.target);
  });
}, { threshold: 0.3 });

document.querySelectorAll('.progress-bar').forEach(el => progressObserver.observe(el));
```

### Micro-Interactions

```css
/* Button hover */
.btn {
  transition: transform 150ms ease-out, box-shadow 150ms ease-out, background 150ms ease-out;
}
.btn:hover {
  transform: translateY(-1px);
}
.btn:active {
  transform: translateY(0);
}

/* Card hover — lift only, no color shift */
.card {
  transition: transform 200ms ease-out, box-shadow 200ms ease-out;
}
.card:hover {
  transform: translateY(-4px);
  box-shadow: 0 16px 40px rgba(0,0,0,0.10);
}

/* Image subtle zoom on hover */
.image-zoom-wrap {
  overflow: hidden;
  border-radius: inherit;
}
.image-zoom-wrap img {
  transition: transform 600ms cubic-bezier(0.16, 1, 0.3, 1);
}
.image-zoom-wrap:hover img {
  transform: scale(1.03);
}
```

### Navigation Scroll Behavior

```js
// Nav transparency transition as user scrolls past hero
const nav = document.querySelector('.nav');
const hero = document.querySelector('.hero');

if (nav && hero) {
  const heroObserver = new IntersectionObserver(([entry]) => {
    nav.classList.toggle('nav-dark', entry.isIntersecting);
  }, { threshold: 0.1 });
  heroObserver.observe(hero);
}

// Sticky CTA appears after scrolling past first viewport
const stickyCTA = document.querySelector('.sticky-cta');
if (stickyCTA) {
  window.addEventListener('scroll', () => {
    stickyCTA.classList.toggle('visible', window.scrollY > window.innerHeight * 0.8);
  }, { passive: true });
}
```

---

## What This File Doesn't Cover

- Token values (type scale, spacing, buttons, glass, gradients, motion values, pin CSS, SVGs) → `references/tokens.md`
- Design rules (color semantics, typography, Ember, Signal, Two-Icon, principles, section vocabulary) → `SKILL.md`
- Page build workflow → `references/process.md`
