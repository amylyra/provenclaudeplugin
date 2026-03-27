# Channel Specs

Platform-specific formats, dimensions, and limits. Update this file when platforms change specs — don't edit the agent files.

Last updated: March 2026

---

## Email

| Element | Spec |
|---|---|
| Subject line | ≤50 chars recommended, ≤90 chars max |
| Preheader | ≤100 chars |
| Hero image | 600×400px (1.5:1) |
| Email width | 600px max |
| Layout | Tables, inline CSS. No CSS grid/flexbox. |
| Personalization | Klaviyo tokens: `{{ first_name }}`, `{{ email }}`, etc. |

---

## Instagram

| Format | Aspect Ratio | Image Size | Copy Limit |
|---|---|---|---|
| Feed post (square) | 1:1 | 1080×1080 | 2,200 chars |
| Feed post (portrait) | 4:5 | 1080×1350 | 2,200 chars |
| Story / Reel | 9:16 | 1080×1920 | Overlay text only |
| Carousel | 1:1 or 4:5 | 1080×1080 or 1080×1350 | 2,200 chars (caption) |

Notes: First 125 chars visible before "more." Hashtags: 3-5 relevant, not 30.

---

## TikTok

| Format | Aspect Ratio | Copy Limit |
|---|---|---|
| Video / Image post | 9:16 | 4,000 chars |

Notes: First ~80 chars visible before truncation. Hook in the first line.

---

## LinkedIn

| Format | Aspect Ratio | Image Size | Copy Limit |
|---|---|---|---|
| Single image | 1.91:1 | 1200×627 | 3,000 chars |
| Square image | 1:1 | 1080×1080 | 3,000 chars |
| Carousel (PDF) | variable | 1080×1080 per slide | 3,000 chars |

Notes: First ~140 chars visible before "see more." Professional tone, but still PROVEN voice — not corporate.

---

## X (Twitter)

| Format | Aspect Ratio | Image Size | Copy Limit |
|---|---|---|---|
| Post | — | — | 280 chars |
| Post with image | 16:9 or 1:1 | 1200×675 or 1080×1080 | 280 chars |

---

## Google Ads

| Element | Limit |
|---|---|
| Headline | ≤30 chars |
| Long headline | ≤90 chars |
| Description | ≤90 chars |
| Image (landscape) | 1.91:1 (1200×628) |
| Image (square) | 1:1 (1200×1200) |

Notes: Minimum 3 headlines, 2 descriptions for responsive search ads. No exclamation marks in headlines.

---

## Meta Ads (Facebook / Instagram)

| Element | Limit |
|---|---|
| Primary text | ≤125 chars (visible before truncation) |
| Headline | ≤40 chars |
| Description | ≤30 chars |
| Image (feed) | 1:1 (1080×1080) |
| Image (story) | 9:16 (1080×1920) |
| Video | 1:1 or 4:5 (feed), 9:16 (story) |

Notes: Text overlay on images should be ≤20% of image area for best delivery.

---

## Website / Landing Page

| Element | Spec |
|---|---|
| Hero image | 1440×800 (16:9) or full-width responsive |
| Max content width | 1200px (per proven-ui tokens) |
| Breakpoints | Per proven-ui/references/frontend.md |
| Fonts | Albert Sans (UI), Source Serif 4 (editorial) via Google Fonts `<link>` |
