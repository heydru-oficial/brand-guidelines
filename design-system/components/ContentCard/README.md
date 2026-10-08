A flat text card laid in a hairline grid: tag, title, one sentence. The site's workhorse for problems, capabilities and situations.

- **Markup:** `.card-grid` > `.content-card` (add `.linked` when the whole card is a link). Inside: `.card-meta` (tag + optional ↗), `h3`, `p`.
- **Grid:** cards sit on a `line`-colored background with a 1px gap, so the gutters read as hairlines. 3 columns (proof grid: 5, then 3 at 1100px, 2 at 760px); 1 column on mobile.
- **Specs:** `card-pad` (34px), `card-meta` style in `meta`, `card-title` style, `card-body` paragraph in `muted`. No radius, no shadow, no image.
- **Hover:** fill moves to `surface-hover`. Inside a `.raised` section the card takes `surface-raised`.
- Write the title in the client's voice when it names a problem ("No one fully understands our site.").
