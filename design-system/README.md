heydru! is a senior-led Drupal engineering boutique. The look is dark, editorial and square: big tight Poppins headlines, quiet Roboto text, hairline rules, and one hot red that marks what matters. heydru.com is the reference build. When this system and an older brand file disagree, follow this system.

## Name and voice

- Write the name as **heydru!**: lowercase, with the exclamation mark, including at the start of a sentence. Never "Heydru", "HEYDRU" or "Heydru!".
- Speak as **we** to **you/your team**, and name the client's situation in their own words. Card titles are often first-person client quotes: *"No one fully understands our site."*, *"Upgrade or rebuild? We can't decide."*
- Keep it short and declarative. Headlines are one sentence, often split into a statement and a turn: *"When Drupal gets difficult, we step in."*, *"Three situations. Senior Drupal judgment."*, *"You don't always need a bigger team."*
- Lead with judgment, not volume: *"Architecture. Judgment. Control."*, *"Precision over volume."* Avoid hype words, exclamation marks (the one in the name is enough) and emoji.
- Use plain facts as proof (*"150+ sites"*, *"40+ locales"*, *"15+ years of Drupal"*) and never invent figures.
- The primary action is always **Talk to a Drupal Architect ↗**. The fallback is **Prefer email? hi@heydru.com**.
- Site copy is in English. Spanish appears only in slugs (`/conversemos`) and named assets.

## Roles: start here for new work

Tokens come in two layers. **Roles** (`role-*`, `status-*`, `accent-*`, `chart-*`, the **Roles** type group, `space-*`, `format-*`) say what a value is for. They are what decks, documents, social posts and new pages use. The **website tokens** below them (`bg`, `muted`, `card-title`, `service-pad`…) record exactly what heydru.com ships, and the roles point at them, so nothing on the site changes.

- **Text has three levels:** `role-text-primary`, `role-text-secondary`, `role-text-tertiary`. Don't reach for `nav`, `meta`, `faint` or `subtle`; those are website details.
- **Surfaces:** `role-surface-page`, then `role-surface-section` for alternating bands, `role-surface-card` for cards and panels, and `role-surface-emphasis` for the single closing call to action. Separate everything with `role-border`.
- **Action:** one `role-action` fill per view with `role-on-action` text; `role-link` for inline links and small accent text; `role-focus` on anything interactive.
- **Type:** `role-display` (once per page or slide), `role-h1` to `role-h4`, `role-body-l`, `role-body`, `role-small`, `role-label`. Headings are Poppins 700; everything else is Roboto. Nothing below `role-label` (12px).
- **Space:** a 4px scale, `space-1` (4px) to `space-24` (96px). Pick from it; don't invent 13px or 25px.

## Status, services and charts

- **Status colors** are `status-success`, `status-warning`, `status-danger`, `status-info`. Every one passes 4.5:1 as text in both themes. Always pair them with a word or icon; color alone never carries meaning.
- **Danger is orange, not red.** Brand red means "act here". An error in red would look like a call to action, and orange against turquoise success stays distinguishable for red–green color blindness.
- **Services keep their colors on any ground** through `accent-rescue`, `accent-advisory` and `accent-ai`. In light, the advisory and AI accents darken to `#0f766e` and `#7a6100` so marks and text stay readable on white. To use the bright yellow or turquoise on white, make it a fill and put `#101014` ink on it.
- **Charts** use `chart-1` to `chart-5` in that order. `chart-1` (red) is the series the chart is about; `chart-5` (gray) is the baseline or "everything else". Label series directly instead of relying on a legend where you can.

## Light and print

Proposals, PDFs, email and print are **light**. Use the same roles with the light theme: `role-surface-page` is white, text is `#393a3e`, and links and small red text are `#b60c4a`. Use bright `red` only for fills, the logo and type at 24px and above. The logo on light is `logo-on-light.svg`.

## Formats

Canvas sizes and margins are the `format-*` tokens: 16:9 slides (1920×1080, 96px margins), square and 4:5 social posts (1080 wide, 80px margins), Open Graph images (1200×630), the LinkedIn banner (1584×396, bottom-left kept clear) and A4 (20mm margins, light theme). One statement per slide or post; the logo sits bottom-left at one icon-mark of clear space.

## Color (website tokens)

The system is **dark-first**. `dark` is the default theme and `light` is the alternate one, switched with the theme toggle.

- **Neutrals lead.** Grounds are `bg`, with `surface-raised` on alternating sections and `surface` for panels and service cards. Text is `text`, and paragraphs are `muted`. The secondary text steps are `text-soft`, `nav`, `meta`, `faint`, `subtle` and `caption`, from brightest to dimmest. `caption` is the floor, so never set text dimmer than it.
- **Red is the one hero color.** Use `red` for the primary button fill, the arrow glyphs, the status dot, the process-step rule, and the accent half of a headline ("we step in."). Keep a view to one red action.
- **Use `red` as text only at 24px and larger in light.** It is 4.09:1 on white. For small red text (numbers, links in prose, article eyebrows, the current TOC item) use `red-text`: #f896b9 in dark, #b60c4a in light.
- **Put dark ink on red.** Button labels use `on-red` (#101014), not white. On hover the fill moves to `red-hover`.
- **Accents belong to the services.** `turquoise` is Architecture Advisory and `yellow` is Drupal AI Engineering. Each is used only for that service's line art and hover border. `yellow` is also the dark-theme `focus` ring and the skip-link fill. Never set `yellow` or `turquoise` as text on a light ground, or `blue` as text on `bg`.
- **The closing band** is the only tinted ground: `surface-closing`, edged in `red-border`.
- **Of the 2021 brandbook swatches,** only two came back, and only as roles: orange is `status-danger` in dark, and lightblue is `status-info` and `chart-4` in dark. Red2 and gray3/4/5 stay out of new work; their values are in the brand-guidelines repo for print.

## Typography (website styles)

- **Poppins 700** is the display face. It is used only for headings and step numbers, always bold, with tight tracking (−0.045em by default, −0.065em on the hero). Line height is 1.02–1.12 for big headings and 1.3 for card and article titles. Only the 700 weight ships, so don't specify any other.
- **Roboto** (a variable font, 100–900) is the body face. Body text is 16px with 1.65 line height. Use 400 for text, 500 for eyebrows and 700 for button labels.
- **Hierarchy:** `hero` → `page-title` → `closing` → `h2` → `h3`, then the card-level `service-title`, `card-title`, `list-title`. Under the headings, `lead` sits beneath a heading, `body` and `card-body` carry the text, and `eyebrow` and `card-meta` are the uppercase labels.
- Headings are fluid: each style's usage note gives the `clamp()` the site uses. Keep heading widths short (h2 max 780px, card titles max 340px) so lines break into phrases.
- **Highlight with color, not weight.** Inside a headline, wrap the turn in a `span` colored `red`. On the hero, one word gets a 2px red underline rotated −2°.
- **12px (0.75rem) is the minimum text size.** `eyebrow`, `card-meta`, `trust` and `index` all sit at that floor.

## Layout and spacing

- Content sits in a `container` (1280px max) with a `gutter` of 56px each side. The gutter drops to `gutter-tablet` at `bp-laptop` and `gutter-mobile` at `bp-mobile`. The header has its own `header-max` of 1600px and a height of `header-height`.
- Sections are `section-y` tall top and bottom (`section-y-mobile` on phones). Each opens with an eyebrow, `eyebrow-gap`, then an h2. A short `section-description` sits right-aligned beside it, and `heading-gap` separates the heading from the content.
- Separate things with **1px hairlines in `line`**, not shadows or boxes. Card grids sit on a `line` background with a 1px gap, so the gutters read as rules. The only shadows are `shadow-dropdown` (the services menu), `shadow-status` and `shadow-orbit`.
- **Everything is square.** Use `radius-none` on buttons, cards, panels and the theme toggle. `radius-round` is only for true circles: the status dot, the motion toggle and the orbit.
- Number things with two digits and a slash: `01 /`, `02 /`. Numbers appear in eyebrows, card meta, ruled lists and article rows.

## Iconography and imagery

- There is no icon font. Direction glyphs are typed characters: **↗** for leaving or booking, **→** for going deeper, **↓** for scrolling down, **＋** (full-width plus) for list markers, **⌄** for menus. Color them `red` when they mark an action.
- Diagrams are **line art in `currentColor`**: 1–2px strokes, small filled nodes, no fills or gradients. Examples are the hero platform grid and the three service drawings in `ServiceCard`. Each takes one color: `red`, `turquoise` or `yellow`.
- Photography is limited to the founder portrait, square and grayscale. Don't use stock imagery or mockups.

## Motion and states

- **Hover:** buttons lift 2px and service cards lift 6px. Linked cards fill with `surface-hover`, and article rows slide 12px. Transitions run 0.2–0.25s.
- **Links never change by color alone.** On hover, every link gains an underline: navigation links turn `text` with a `text`-colored 2px underline; footer, breadcrumb and inline links turn `role-link` with a 1px underline; menu rows also get a light background. Prose links are always underlined and thicken to 2px on hover.
- **You are here:** the current page's link carries `aria-current="page"` and a solid 2px `red` underline (in a menu, a 2px `red` inset rule on the left and `role-link` text). A section counts as current for every page under it: Insights is current on each article.
- **Focus:** a 2px solid outline in `focus` (yellow in dark, #b60c4a in light), offset 6px on links and 4px on buttons.
- **Reduced motion:** honor `prefers-reduced-motion` by removing every animation and transition, and hide the pause control.
- **Text selection:** `selection-bg` with `selection-text`.

## Logos

- Use **logo-on-dark.svg** (red mark, white wordmark) on `bg`, and **logo-on-light.svg** (red mark, #393A3E wordmark) on white. On the site the logo swaps with the theme.
- **icon-mark-red.svg** is the favicon and avatar. Use the white mark on red or photographic grounds.
- **Clear space** is one icon-mark width on all four sides of a lockup.
- Never recolor the mark outside the provided files, redraw it, or set "heydru!" in Poppins as a substitute for the wordmark.
