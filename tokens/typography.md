# Typography

## Adopted (source: heydru.com)

- **[Poppins](https://fonts.google.com/specimen/Poppins) 700** — display.
  Headings and step numbers only; only the 700 weight ships
  (`/fonts/poppins-latin-700.woff2`). Letter-spacing −0.045em (−0.065em on the
  hero), line height 1.02–1.12, 1.3 for card and article titles.
- **[Roboto](https://fonts.google.com/specimen/Roboto)** — body. Variable
  font, 100–900 (`/fonts/roboto-latin.woff2`); used at 400 (text), 500
  (uppercase labels, 0.09–0.12em tracking) and 700 (button labels). Body is
  16px / 1.65.
- **Minimum size: 12px (0.75rem).**

The site self-hosts both files (latin subset). For tools that need a hosted
font, the equivalent Google Fonts request is:

```html
<link
  rel="stylesheet"
  href="https://fonts.googleapis.com/css2?family=Poppins:wght@700&family=Roboto:wght@400;500;700&display=swap"
/>
```

## Legacy: 2021 brandbook

The source Figma file (BRANDBOOK page, "TIPOGRAFÍA PRINCIPAL" frame)
specified **Roboto only**, in Light, Regular, Bold and ExtraBold. Poppins was
added when the website was built and is now the adopted display face.
