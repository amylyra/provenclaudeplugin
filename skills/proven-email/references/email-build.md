# Email Build Reference

How to translate the PROVEN design system into email-safe HTML. Read `proven-ui/SKILL.md` and `proven-ui/references/tokens.md` first — this file only documents where email diverges from the web system. If something isn't addressed here, the proven-ui rule applies.

---

## Design System Reference

**Read these files. Do not duplicate their contents here.**

| Source | What it governs | Email inherits |
|---|---|---|
| `proven-ui/SKILL.md` → "How to Think" | Design philosophy | All of it. Recognition over impression. Calm authority. The one thing. Remove until it breaks. |
| `proven-ui/SKILL.md` → "Color" | Palette, brightness principle, warm/cool interplay, dark registers, teal register rules | All of it. Same hex values. Same usage rules. Same brightness principle. |
| `proven-ui/SKILL.md` → "Typography" | Type scale, Source Serif 4 accent rules, headline tiers | Adapted below — email-specific sizes at 600px canvas. |
| `proven-ui/references/tokens.md` → "Button System" | Button vocabulary, pill shape, context-dependent fills | Adapted below — email-safe bulletproof button pattern. |
| `proven-ui/references/tokens.md` → "Spacing Scale" | Spacing progression, "section padding as pacing" | Adapted below — email-specific spacing at 600px. |
| `proven-ui/references/tokens.md` → "Glass Components" | Glass panels, stat panels, insight chips | **Not available in email.** See "What Email Cannot Do" below. |

---

## What Email Cannot Do

Email clients strip or ignore these proven-ui features. Never attempt them in email HTML:

| Proven-UI Feature | Email Substitute |
|---|---|
| `backdrop-filter` (glass effects) | Solid fill at equivalent color. Warm glass → linen (#FAF6F2). Cool glass → #F5F9FB. |
| CSS custom properties (`var(--ember)`) | Hardcoded hex values inline. |
| CSS grid / flexbox | Table-based layout. |
| `clamp()` responsive sizing | Fixed sizes + `@media` breakpoint at 620px. |
| `border-radius` (Outlook) | VML fallback for buttons. Rounded corners decorative only — must work without them. |
| Source Serif 4 italic accent (Outlook) | Degrades to Georgia italic. Layout must work with fallback. |
| Hover states (mobile) | CTA hover color is desktop-only enhancement. Tap target size matters more. |
| Scroll-based animation / motion | Static. No animation in email. |

---

## Email-Adapted Type Scale

Adapted from proven-ui's three headline tiers for a 600px canvas. Same font stack, same weight logic, compressed sizes.

**Font import** (in `<style>` block — Gmail/Apple Mail only):
```css
@import url('https://fonts.googleapis.com/css2?family=Albert+Sans:wght@400;500;600;700;800;900&family=Source+Serif+4:ital,wght@1,700&display=swap');
```

**Fallback stacks** (always inline):
- Headlines: `'Albert Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif`
- Accent: `'Source Serif 4', Georgia, 'Times New Roman', serif`

| Role | Proven-UI Tier | Email Desktop | Email Mobile (≤620px) | Weight | Tracking |
|---|---|---|---|---|---|
| Hero headline | Display | 32–36px | 28px | 900 | −0.03em |
| Section headline | Section | 24–28px | 22px | 800 | −0.02em |
| Body | Body | 15–16px | 15px | 500 | 0 |
| Label / metadata | Label | 11px uppercase | 10px uppercase | 700 | +0.12em |
| CTA text | — | 15px | 15px | 600 | +0.02em |

**The ratio rule holds:** proven-ui demands 6:1 between Display and Body. At 600px, 32px/15px = 2.1:1 — less dramatic, but the tightest ratio email can support while remaining readable. Compensate by making the headline the only bold element on screen — the weight contrast (900 vs. 500) does the work that size can't.

**Source Serif 4 in email:** One word per email maximum. In the subject line or hero headline only. Never in body copy. The italic shift is an event — same rule as proven-ui, same restraint.

---

## Email-Adapted Spacing

Proven-ui's spacing scale `4 → 8 → 16 → 24 → 32 → 48 → 80 → 120 → 160 → 200px` adapts to the 600px email canvas.

| Context | Desktop | Mobile (≤620px) |
|---|---|---|
| Section padding (top/bottom) | 48–64px | 32–40px |
| Content padding (left/right) | 32–40px | 24px |
| Between headline and body | 16px | 12px |
| Between body and CTA | 24–32px | 24px |
| Between sections (divider) | 1px sand (#E6DED4) + 48px padding above/below | Same |
| Image margin (bottom) | 24px | 16px |

**Pacing principle (from proven-ui):** Each scroll on mobile should reveal one idea — one hero, one text block, one CTA. If two competing elements appear in the same thumb-scroll, the email is too dense. Add padding or remove an element.

---

## Email-Adapted Color

All hex values come from `proven-ui/references/tokens.md`. Do not define new colors.

### Email-specific rules (on top of proven-ui's color rules):

**Brightness principle in email:** The first section is always white (#FFFFFF) or linen (#FAF6F2). **Bright colors consistently outperform dark in email.** Light surfaces (white, linen) are the default for every section. A navy dark section can appear once per email at most — never as the hero, never as the opener. When in doubt, stay light. The performance data is unambiguous here.

**The cool section problem:** Proven-ui uses sky (#BCD4E2) for cool sections. In email, sky at full opacity is too heavy for a background at 600px — the email feels corporate. Use a lighter variant: #F5F9FB (essentially white with a sky cast). Reserve full sky for accent elements (icons, small labels).

**Dark mode overrides:** Navy (#162743) backgrounds can invert in dark mode clients. Add explicit dark mode overrides in `<style>`:
```css
@media (prefers-color-scheme: dark) {
  .dark-section { background-color: #162743 !important; }
  .dark-section * { color: #FFFFFF !important; }
  .ember-cta { background-color: #C26A4A !important; }
}
```
Also declare `<meta name="color-scheme" content="light dark">` in the `<head>`.

**Teal register (same as proven-ui, critical for email):**
- Teal (#7295A2) — on pure white backgrounds only
- Teal-dark (#4A6D7C) — on linen or any off-white. This is the default for email body metadata.
- Teal-light (#8CAEB9) — on navy dark sections only
- Never use base teal on linen — it fails WCAG AA contrast.

---

## Email CTA Button (Bulletproof)

Translates proven-ui's "Ember filled pill" into an email-safe pattern that renders in Outlook, Gmail, Apple Mail, and Yahoo.

```html
<table role="presentation" cellpadding="0" cellspacing="0" border="0" style="margin: 0 auto;">
  <tr>
    <td align="center" style="background-color: #C26A4A; border-radius: 50px; padding: 14px 32px;">
      <a href="{{ cta_url }}" style="color: #FFFFFF; font-family: 'Albert Sans', Helvetica, Arial, sans-serif; font-size: 15px; font-weight: 600; text-decoration: none; display: inline-block; letter-spacing: 0.02em;">
        Take the Quiz
      </a>
    </td>
  </tr>
</table>
```

**On dark sections (navy):** Use white filled pill instead of ember — same as proven-ui's dark background button vocabulary.

```html
<td align="center" style="background-color: #FFFFFF; border-radius: 50px; padding: 14px 32px;">
  <a href="{{ cta_url }}" style="color: #000000; font-family: 'Albert Sans', Helvetica, Arial, sans-serif; font-size: 15px; font-weight: 600; text-decoration: none; display: inline-block;">
    Shop Your Routine
  </a>
</td>
```

**Mobile:** CTA becomes full-width, 56px height (thumb-friendly):
```css
@media only screen and (max-width: 620px) {
  .cta-button { width: 100% !important; text-align: center !important; }
  .cta-button td { padding: 16px 24px !important; }
}
```

**Rules (from proven-ui button vocabulary):**
- One primary CTA per email. Pill shape. Ember on light, white on dark.
- Text links (`color: #C26A4A` + `›` arrow) for secondary navigation in body copy.
- Never: generic CTA text ("Learn More," "Click Here," "Shop Now"). Always action-specific.

---

## Klaviyo Personalization Tokens

| Token | Use Case | Rule |
|---|---|---|
| `{{ first_name\|default:'there' }}` | Greeting | Use only when followed by personalized content. "Hi Sarah" + generic body = fake personalization. |
| `{{ first_name\|default:'Your' }}` | Possessive | "{{ first_name }}'s updated formula" — only in subscriber emails. |
| `{{ person\|lookup:'Skin Type' }}` | Quiz data | Only if profile has this property populated. |
| `{{ person\|lookup:'Primary Concern' }}` | Concern targeting | Use to select content blocks dynamically. |

---

## Technical Constraints

- **600px max content width.** Table-based layout only.
- **Inline styles required** for Outlook. `<style>` blocks for Gmail/Apple Mail. Duplicate critical styles inline.
- **Images blocked by default.** Every image needs alt text. Email must communicate with images off.
- **Maximum 3 images per email.** More triggers aggressive blocking in corporate clients.
- **Unsubscribe:** `{% unsubscribe 'Unsubscribe' %}`. Always present. Always visible.
