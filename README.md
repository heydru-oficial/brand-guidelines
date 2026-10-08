# heydru! brand guidelines

The public brand and design system of **heydru!**, a senior-led Drupal
engineering boutique. Everything we use to look and sound like ourselves is
here, in the open: logos, tokens, type, components and the rules behind them.

- **[heydru.com/brand](https://heydru.com/brand)**: the guidelines on our site,
  rendered from this repo.
- **[Live design system](https://claude.ai/artifact/7egsayPbc5T9UtSy3ondg6)**:
  the same system with live component previews in both themes.
- **This repo**: the source files. Merging here updates heydru.com/brand.

**Where values come from.** heydru.com is the reference build: its palette,
typography and voice are recorded here. The original 2021 brandbook (Figma)
is kept below for print and legacy reference. If the two disagree, the
website wins.

## Design system

`design-system/` is the full system:

- `README.md`: the brand book (voice, color, type, layout, logos).
- `tokens.json`: every token in dark and light, in two layers. **Roles**
  (`role-*`, `status-*`, `accent-*`, `chart-*`, the Roles type scale,
  `space-*`, `format-*`) are what new work uses: decks, documents, social
  posts, new pages. **Website tokens** record exactly what heydru.com ships;
  the roles point at them.
- `components/`: specs and previews for the site's components plus `Status`.
- `fonts/`: Poppins 700 and Roboto, with their OFL licenses.

heydru.com/brand renders from this folder; a merge here reaches the site
through the website's brand-sync workflow. `CLAUDE.md` explains how changes
flow.

## Logo system

The source file names three distinct assets — use its own terms, not generic
ones:

| Term (as labeled in the source) | What it is | Files |
|---|---|---|
| **Logotipo** | The wordmark alone, no icon | `logotype-on-dark.svg`, `logotype-on-light.svg` |
| **Síntesis gráfica** (the icon mark — commonly called the *isotipo*) | The "Q" speech-bubble alone, no wordmark | `icon-mark-red.svg` (default), `icon-mark-white.svg` (dark backgrounds), `icon-mark-black.svg`, `icon-mark-blue.svg`, `icon-mark-yellow.svg` (alternates — see below) |
| **Marca gráfica** | Icon + wordmark locked up together | `logo-on-dark.svg`, `logo-on-light.svg` (horizontal), `lockup-vertical-on-dark.svg`, `lockup-vertical-on-light.svg` (icon stacked above wordmark), plus `logo-on-dark-mono.svg` / `lockup-vertical-on-dark-mono.svg` (monochrome — icon and wordmark both white, see below) |

The source file shows both a horizontal lockup (icon beside the wordmark)
and a vertical one (icon stacked above it, e.g. its "heydru-0021" frame) —
both are real, intended variants, not a stylistic one-off. The vertical
files here are composited from the same verified icon and wordmark paths
used everywhere else on this page, not a separate Figma export, so they're
pixel-consistent with the horizontal lockup.

`svg/png/` holds the same files rasterized at 256/512px (icon) and 2x
(wordmark/lockup), for tools that don't take SVG. SVG is still the source;
regenerate PNGs from it (`rsvg-convert`) rather than hand-exporting from
Figma again.

### Alternate icon colors

Red is the default icon color — but the source file's own color-variant
grids (both the horizontal lockup one and the vertical lockup one) also
show the icon in black, blue, and yellow, always with black wordmark text
where there's a wordmark. Consistent across every form:

| | Isotipo (icon alone) | Horizontal lockup | Vertical lockup |
|---|---|---|---|
| Black | `icon-mark-black.svg` | `logo-on-light-black-icon.svg` | `lockup-vertical-on-light-black-icon.svg` |
| Blue | `icon-mark-blue.svg` | `logo-on-light-blue-icon.svg` | `lockup-vertical-on-light-blue-icon.svg` |
| Yellow | `icon-mark-yellow.svg` | `logo-on-light-yellow-icon.svg` | `lockup-vertical-on-light-yellow-icon.svg` |

These alternates are for print and illustration. The website UI uses only the
red mark.

These are real alternates shown in the source, not an invented option — use
red by default, reach for one of these only where context calls for it
(e.g. matching a section's accent color, or a single-ink print constraint).
Don't introduce a color outside this set, and don't recolor the icon
independently of these provided variants.

### Monochrome lockup

The default on-dark lockup is two-tone: red icon, white wordmark
(`logo-on-dark.svg`, `lockup-vertical-on-dark.svg`). The source file's
"heydru-009" frame shows a separate, genuinely distinct third option: icon
and wordmark **both white** — not a recolor experiment, an intended variant
in its own right, in both horizontal and vertical form:

| | Horizontal | Vertical |
|---|---|---|
| Monochrome (icon + wordmark both white) | `logo-on-dark-mono.svg` | `lockup-vertical-on-dark-mono.svg` |

Use it for single-ink or dark/saturated contexts where the two-tone
treatment's red icon would compete with the background — not as a default
replacement for the two-tone on-dark lockup, which stays the primary
on-dark option.

### Clear space

The source file's own guideline frames (not just my judgment): keep clear
space on **all four sides of the marca gráfica equal to one icon-mark's
width/height**, measured from the lockup's outer edges. Don't place other
elements inside that margin.

## Web theme (source: heydru.com)

`tokens/colors.json` → `web` — every color heydru.com uses, per theme. The
site is **dark-first**: `bg` is `#101014`, not Heydru-Black. Heydru-Black
(`#393A3E`) is the light theme's text color.

| Token | Dark | Light | Use |
|---|---|---|---|
| `bg` | `#101014` | `#FFFFFF` | Page background |
| `surface` | `#17171B` | `#F5F5F7` | Panels, service cards |
| `surface-raised` | `#141418` | `#F7F7F9` | Alternating sections, trust strip |
| `text` | `#F5F5F6` | `#393A3E` | Default text |
| `muted` | `#B0B0B8` | `#5A5A5A` | Paragraphs |
| `line` | `#FFFFFF20` | `#393A3E25` | Every hairline and card-grid gutter |
| `red` | `#F0216C` | `#F0216C` | Primary CTA fill, arrows, accent words. As text on white only at 24px+ (4.09:1) |
| `red-text` | `#F896B9` | `#B60C4A` | Small red text: numbers, prose links, eyebrows |
| `on-red` | `#101014` | `#101014` | Text on red — dark, never white |
| `turquoise` | `#70EBE1` | `#70EBE1` | Architecture Advisory art and hover |
| `yellow` | `#FFEA2E` | `#FFEA2E` | Drupal AI Engineering art and hover; dark-theme focus ring |
| `focus` | `#FFEA2E` | `#B60C4A` | 2px focus outline |

The full list (31 tokens, including the secondary text steps and the closing
band) is in `colors.json`. Red2, orange, lightblue and gray3/4/5 below are not
used on the web.

## Colors (2021 brandbook)

`tokens/colors.json` — the full palette as named in Figma's Color Styles,
with hex values read directly from the source file's Color Styles panel
(not reconstructed from memory). Heydru-Red is primary.

The source file also documents full print breakdowns (RGB + CMYK + HEX) for
the four core colors, on its own "COLORES" frame:

| Style | HEX | CMYK |
|---|---|---|
| Heydru-Red | `#F0216C` | C0 M93 Y28 K0 |
| Heydru-Azul (labeled "Heydru Blue" in the source) | `#384993` | C90 M76 Y6 K0 |
| Heydru-Yellow | `#FFEA2E` | C3 M1 Y85 K0 |
| Heydru-Black | `#393A3E` | C73 M65 Y60 K79 |

The remaining eight colors (Red2, lightblue, orange, Turquoise, gray3/4/5,
White) only exist as Color Styles in the file — no CMYK breakdown was given
for them in the source; don't invent one.

**Known discrepancy in the source file, not in these values:** the COLORES
frame's own RGB text label for Heydru-Black reads "R:34 G:33 B:33", which
doesn't actually convert to its own stated HEX (`#393A3E` = RGB 57,58,62).
The HEX and the Color Style's actual fill agree with each other (verified
two independent ways — the Color Style's own value, and the fill actually
used in `logo-dark.svg`/`favicon.svg`), so `#393A3E` is what's recorded here;
the RGB label next to it in the 2021 deck appears to be a typo, left as-is
in the original artwork.

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

### Color system (not in the source — our own addition)

The source file treats all 12 colors as one flat, equal-weight list — no
stated hierarchy, no usage guidance. That's the main thing "missing love" in
the original: a system tells you *how much* of each color to use and *for
what*; a swatch grid doesn't. Modeled on how mature brand systems do this
(e.g. [GitHub's](https://brand.github.com/foundations/color): ~80% neutral,
~10% grey, ~10% hero green):

| Role | Colors | Target share | Use |
|---|---|---|---|
| **Neutral** | Black, White, gray3/4/5 | ~75% | Surfaces, body text, structure — the dominant share of any layout |
| **Primary** | Red | ~15% | The one hero color: CTAs, the icon mark, key emphasis. Don't compete with it using a second saturated color in the same view |
| **Accent** | Azul, Yellow, Red2, orange, Turquoise, lightblue | ~10% | Sparing use for variety, data viz, or illustration — never a substitute for the primary red on a CTA |

### Color ramps (not in the source — our own addition)

GitHub's own brand toolkit gives its hero color and its neutrals a 6-step
tint/shade ramp each, with the base color anchored partway through (their
"GITHUB GREEN" = Green 4 of 6), not just one flat swatch. Same idea applied
here — computed in HSL off the verified base hex, not picked by eye, so
each step is the same hue at a different lightness:

| | 100 | 200 | 300 | 400 | 500 | 600 |
|---|---|---|---|---|---|---|
| **red-*** | `#FDD8E5` | `#F896B9` | `#F24080` | `#F0216C` ← base | `#B60C4A` | `#600627` |
| **neutral-*** | `#FFFFFF` ← Heydru-White | `#D7D8D8` | `#B0B0B2` | `#88898B` | `#616165` | `#393A3E` ← Heydru-Black |

Named `red-NNN`/`neutral-NNN` (not "Red 1-6") deliberately, so these can't
be confused with the distinct named swatches above (`Heydru-Red2`,
`Heydru-gray3/4/5`) — different things, same color family. See
`tokens/colors.json` → `system.ramps` for the machine-readable version.

Also added, for product-UI needs a 2021 print-oriented brandbook never had to
cover (not used by the current site — see **Web theme** for the reds it does use):

| Token | Value | Use |
|---|---|---|
| Heydru-Red-hover | `#D81E61` | Hover/active state for red CTAs/links (~10% darken of Red) |
| Heydru-Red-wash | `rgba(240, 33, 108, 0.08)` | Subtle tinted background (selected row, badge) where solid red is too loud |
| Heydru-Red-wash-strong | `rgba(240, 33, 108, 0.16)` | Hover state for the wash above |

See `tokens/colors.json` → `system` for the machine-readable version.

## Applications

`applications/` — real, current touchpoints, not stock mockup renders (deliberately skipped the
mug/t-shirt/stamp mockups from the 2021 deck — generic swag templates don't reflect how this
brand actually shows up in 2026).

| File | What it is |
|---|---|
| `email-signature.html` | Table-based HTML signature, inline-styled for Outlook/Gmail/Apple Mail compatibility. Open it and copy the rendered block into your email client's signature editor. |
| `linkedin-banner.png` | 1568×392 (LinkedIn's banner slot, effectively 1584×396) — text kept clear of the bottom-left profile-photo overlap zone. Preview in LinkedIn's own banner editor before publishing; exact safe-zone cropping varies by viewport. |

## Legacy source (view-only)

The original [Figma file](https://www.figma.com/design/56WZVAxqnPHaqjkf9TDoZo/final-HEYDRU-2021--Copy-?node-id=1-16) —
**"final HEYDRU 2021 (Copy)," BRANDBOOK page** — is kept as a view-only legacy
reference for anyone who wants to see the original 2021 artwork directly.
Everything in this repo was verified against it, but *this repo*, not the
Figma file, is the one to update going forward — the Figma file isn't
expected to change again.

## Typography

**Poppins 700 + Roboto** — the adopted pairing, as heydru.com ships it.

- **Poppins 700** for headings and step numbers only. Only the 700 weight
  ships; don't specify others. Tight tracking (−0.045em, −0.065em on the
  hero), line height 1.02–1.12.
- **Roboto** (variable 100–900) for everything else: 16px / 1.65 body, 500
  for uppercase labels, 700 for button labels.
- **Minimum size: 12px.**

The 2021 brandbook specified Roboto only (Light, Regular, Bold, ExtraBold).
That is kept in `tokens/typography.md` as legacy reference. Details there.

## Voice

As heydru.com writes it:

- The name is **heydru!** — lowercase with the exclamation mark, even at the
  start of a sentence.
- **We** speak to **you/your team**, and name the client's situation in their
  words: *"No one fully understands our site."*
- Short, declarative headlines with a turn: *"When Drupal gets difficult, we
  step in."*, *"You don't always need a bigger team."*
- Judgment over volume: *"Architecture. Judgment. Control."* No hype, no
  emoji, no extra exclamation marks.
- Plain, true figures as proof (*"150+ sites"*, *"15+ years of Drupal"*).
- The primary action is **Talk to a Drupal Architect ↗**.

## Updating this repo

When heydru.com's styles change (`astro/src/styles/global.css` in
heydru-oficial/heydru-website), update the `web` block in `tokens/colors.json`
and the tables above to match, and update `static`/`public/brand/tokens.json`
on the site. The Figma file is frozen; only logo or print changes would come
from it.
