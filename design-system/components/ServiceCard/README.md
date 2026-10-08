One card per service, with a line-art diagram. Used only for the three heydru! services.

- **Markup:** `.service-grid` > `a.service-card.{rescue|advisory|ai}`: `.card-meta` (`01 /` + ↗), `.service-art` (inline SVG drawn in `currentColor`), `h3`, `p`, `.card-cta`.
- **Color per service:** Drupal Rescue → `red`, Architecture Advisory → `turquoise`, Drupal AI Engineering → `yellow`. The art and the hover border take that color; nothing else does.
- **Specs:** `surface` fill, 1px `line` border, padding 28px / `service-pad`, `grid-gap` between cards, art box 185px tall, `service-title` heading.
- **Hover:** lifts 6px and the border takes the service color; on the site the art also animates (draw-in, layered shift, nodes rising).
- Art is 1–2px strokes, no fills except small node dots. Don't add icons or illustrations in another style.
