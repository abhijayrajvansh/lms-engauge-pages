# Engauge Learning Brand Colours & Themes

This README distills the key visual identity directions captured in `Brand Guidelines Style Sheet.pdf` so designers and engineers can quickly apply Engauge Learning's brand palette across web and product work.

## Core Palette
| Name        | Hex     | RGB          | CMYK             | Notes |
|-------------|---------|--------------|------------------|-------|
| Cobalt      | `#0047AB` | 0 · 71 · 171 | 98 · 81 · 0 · 0  | Primary accent; dominant backgrounds, CTAs, links. |
| Charcoal    | `#1D1D1D` | 29 · 29 · 29 | 72 · 66 · 65 · 76 | Body text, icons, header/footer fills; pairs with both blues and greys. |
| Pearl Grey  | `#EDEDED` | 237 · 237 · 237 | 6 · 4 · 4 · 0 | Neutrals, cards, backgrounds to offset Cobalt/Charcoal. |

### Usage Guidance
- **Primary actions**: prioritize Cobalt for buttons, highlights, and navigation states; ensure WCAG AA contrast against Pearl Grey or white (#FFFFFF background works with Cobalt at 4.22:1 contrast for large text, consider bold fonts for small text).
- **Typography & icons**: default to Charcoal for optimum readability on light backgrounds; switch to Pearl Grey or white for inverse treatments over Cobalt fills.
- **Surface hierarchy**: use Pearl Grey for panels, dividers, and subtle backgrounds to let Cobalt accents pop. Introduce a white base layer whenever more breathing room is needed.

## Typography Stack
- **Primary display face**: `Glancyra` (all caps + lowercase examples given in the guide); reserve for logotype or hero statements.
- **Complementary system fonts**: `Gotham`, `Poppins`, or `Raleway` for UI copy, supporting headlines, and long-form text. Choose based on platform availability (Gotham for print, Poppins/Raleway for web via Google Fonts).
- Maintain consistent letter-spacing across uppercase Glancyra treatments to echo the logotype feel shown in the PDF.

## Iconography & Pattern
- Maintain the Engauge Learning icon within Cobalt or reversed white on Charcoal; spacing should mirror logotype proportions in the PDF.
- The brand pattern showcased in the guide can sit in Pearl Grey overlays behind content blocks; drop opacity to 8–12% when used within interfaces to avoid visual noise.

## Implementation Checklist
1. Import the primary palette into your design system tokens (`brand.cobalt`, `brand.charcoal`, `brand.pearlGrey`).
2. Configure typography styles: `display` (Glancyra), `heading/body` (Poppins/Raleway), `mono` (system fallback).
3. Apply accessibility checks whenever Cobalt is paired with Pearl Grey or white, especially for small labels (<16px).
4. Reference the PDF iconography exports when recreating SVGs to preserve stroke thickness.

For deeper context or assets, review `/Users/abhijayrajvansh/Desktop/Engauge-Assets/Branding/Brand Guidelines Style Sheet.pdf`.
