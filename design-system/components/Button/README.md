The square call-to-action: red fill, dark ink, label and arrow pushed to opposite ends.

Use `.button` for the one primary action in a view — on heydru.com that is always **Talk to a Drupal Architect ↗**. Use `.button.secondary` (transparent, `line` border, `text-strong` label) for a second action beside it; never two red buttons together.

- **Markup:** `<a class="button" href="…">Label<span aria-hidden="true">↗</span></a>`. Supply the label and a trailing glyph: ↗ leaves the site or opens a booking, → goes deeper on-site, ↓ jumps down the page.
- **Specs:** min-height 54px, padding `button-y` × `button-x`, `button` text style (Roboto 700, 16px), `radius-none`, gap 28px.
- **States:** hover → `red-hover` fill and a 2px lift; focus → 2px `focus` outline, 4px offset. Motion is removed under `prefers-reduced-motion`.
- **Ink:** `on-red` (#101014), never white — 4.65:1 on `red`, 9.1:1 on `red-hover`.
