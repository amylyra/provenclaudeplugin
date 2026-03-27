# Product Reference Images

Each product has reference images in the `products/` directory. When generating images via Gemini, **always pass the relevant reference image** so the model renders the correct bottle form, chrome finish, label, and proportions.

## Product Map

| Product Name | Directory | Reference Images | Key Visual Details |
|---|---|---|---|
| **Personalized Cleanser** | `products/personalized-cleanser/` | `hero.png`, `cap-open` | Tall pump bottle, mirror-chrome metallic finish, white-on-chrome label, molecular hexagon icon with small circles at each vertex |
| **Personalized Night Cream** | `products/personalized-night-cream/` | `hero.png`, `cap-open` | Jar with chrome lid, same chrome finish and label system |
| **Personalized SPF** | `products/personalized-spf/` | `hero.png`, `cap-open.jpg` | Tube format, chrome cap, same label system |
| **System Kit** | `products/system-kit/` | `hero.jpg` | All three products together |

## How to Use

1. When the brief mentions a product, identify it from this map.
2. Load the reference image(s) from the matching directory.
3. Pass the reference image to Gemini alongside the structured prompt from proven-creative.
4. In the Gemini call, instruct: "Use this reference image for exact product form, chrome finish, label placement, and proportions. Do not alter the bottle design."

### Which image to use when

| Email context | Use this image | Why |
|---|---|---|
| Product hero (default) | `hero.png` / `hero.jpg` | Front-facing, clean, immediately recognizable. Best performer in email. |
| Product detail or texture focus | `cap-open` / `cap-open.jpg` | Shows the product in use state — open, accessible, real. Good for welcome flows and routine education. |
| System / multi-product | `system-kit/hero.jpg` | All products together. Use for system-level messaging, subscription emails, full-routine campaigns. |

## Adding New Products

When PROVEN launches a new product:
1. Create a new directory under `products/` with the product slug.
2. Add `hero.png` (front-facing, clean white background, high resolution) and `cap-open` variant.
3. Add a row to the Product Map table above.
4. Push to GitHub and sync the marketplace.

## Image Requirements

- `hero.png` / `hero.jpg` — Front-facing product shot, clean white background, minimum 1024px wide
- `cap-open` / `cap-open.jpg` — Product with cap off, showing the opening or pump extended
- Keep individual images under 5MB each
- Total plugin zip must stay under 50MB
