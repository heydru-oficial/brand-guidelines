# Heydru Brand Guidelines

**[View the style guide →](https://claude.ai/artifact/KzLNjss2QJZVFs2J7JT5oc)**
— a browsable page with the logo variants, color swatches, and type specimens
below, instead of reading the raw files.

Single source of truth for the Heydru brand: logo assets, color palette, and
typography. Pulled directly from the source Figma file (`final HEYDRU 2021
(Copy)`, Branding page) so every product/site can reuse the same values
instead of re-deriving them.

## Logo

`svg/` — the "Q" speech-bubble icon mark plus the full "heydru!" lockup.

| File | Use |
|---|---|
| `icon-mark-red.svg` | Primary icon mark, Heydru-Red (`#F0216C`). Default choice — favicons, avatars, anywhere the icon stands alone. |
| `icon-mark-black.svg` | Icon mark in Heydru-Black (`#393A3E`), for contexts where red can't be used (print, single-color contexts). |
| `icon-mark-white.svg` | Icon mark in white, for dark/colored backgrounds. |
| `logo-on-dark.svg` | Full lockup (icon + "heydru!" wordmark) with white text, for dark backgrounds. |
| `logo-on-light.svg` | Full lockup with Heydru-Black (`#393A3E`) text, for light backgrounds. |

`svg/png/` — the same five files rasterized at 256/512px (icons) and 2x
(lockups), for tools that don't take SVG. SVG is still the source; regenerate
PNGs from it (`rsvg-convert`) rather than hand-exporting from Figma again.

The icon mark itself is always red (`#F0216C`) in the full lockups — only the
wordmark color changes between the light/dark variants. Don't recolor the
icon independently of these provided variants.

## Colors

`tokens/colors.json` — the full palette as named in Figma's Color Styles,
with hex values read directly from the source file (not reconstructed from
memory). Heydru-Red is primary.

| Style | Hex |
|---|---|
| Heydru-Red | `#F0216C` |
| Heydru-Red2 | `#FE626C` |
| Heydru-Azul | `#384993` |
| Heydru-Yellow | `#FFEA2E` |
| Heydru-Black | `#393A3E` |
| Heydru-White | `#FFFFFF` |
| Heydru-lightblue | `#6DDAFD` |
| Heydru-orange | `#FF9839` |
| Heydru-Turquoise | `#70EBE1` |
| Heydru-gray3 | `#AAAAAA` |
| Heydru-gray4 | `#5A5A5A` |
| Heydru-gray5 | `#333333` |

## Typography

See `tokens/typography.md` — Poppins for headings, Roboto for body text.

## Updating this repo

If the Figma file changes, re-verify values directly from its Color Styles
panel (don't guess/retype from memory) and update `tokens/colors.json` and
the relevant SVGs here first, then re-sync into any consuming project.
