# CLAUDE.md

Guidance for Claude (or any AI agent) working in this repo.

## What this repo is

The public source files for the heydru! brand: logos (`svg/`), the 2021
brandbook values (`tokens/`), touchpoints (`applications/`) and the design
system (`design-system/`).

## Source of truth and the direction changes flow

```
heydru.com CSS (heydru-oficial/heydru-website, astro/src/styles/global.css)
   → this repo: tokens/colors.json `web` block + design-system/
   → heydru-website syncs design-system/ and svg/ back in and renders /brand from them
   → the Claude Design System artifact is re-synced from design-system/
```

- **Values come from the live site.** When a color, size or font changes in
  `global.css`, update `design-system/tokens.json` (and the `web` block in
  `tokens/colors.json`) to the same value. Don't change a value here that the
  site doesn't use.
- **Never hand-edit heydru-website's vendored copy** (`astro/src/brand-system/`,
  `astro/public/brand/svg/`). Change files here; the website's
  `brand-sync.yml` workflow opens a PR there.
- A merge to `main` touching `design-system/` or `svg/` pings
  heydru-website's `brand-sync.yml` immediately via
  `.github/workflows/dispatch-brand-sync.yml` (needs the
  `HEYDRU_WEBSITE_DISPATCH_TOKEN` secret here; falls back to the daily cron
  if that secret is missing). To run brand-sync by hand instead:
  `gh workflow run brand-sync.yml -R heydru-oficial/heydru-website`.

## design-system/

The same files as the heydru! Design System artifact on claude.ai (the
artifact is a viewer and working copy; this folder is the durable copy).

- `README.md`: the brand book, written as usage rules that name tokens.
  heydru.com/brand renders it, so it is public copy: keep it in the brand
  voice and free of build notes.
- `tokens.json`: every family except `type` is a **list**
  (`{"tokens":[{"name","value","usage"}]}`); colors are
  `{"dark": …, "light": …}` with dark first. Don't convert it to a
  name→value map. Every token keeps a `usage` note.
- **Two layers in tokens.json.** Roles (`role-*`, `status-*`, `accent-*`,
  `chart-*`, the `Roles` type group, `space-*`, `format-*`) are for new work;
  most color roles are aliases (`"{muted}"`) of website tokens. Website tokens
  record what heydru.com ships: don't delete or rename them while the site
  uses them, and don't point new work at them when a role exists.
- `components/`: `bundle.css` (classes ported from the site) and one folder per
  component with `preview.html` + `README.md`. `Cover/` is the artifact's cover.
- `fonts/`: Poppins 700 and Roboto variable, byte-identical to
  heydru.com/fonts, with their OFL licenses. Add no font without its license.
- `assets/*/README.md`: notes for the files in `svg/` and `applications/`.

## Rules that must hold

- Text contrast: 4.5:1 on its ground in both themes (3:1 at 24px+). `red` is
  text on white only at 24px+; small red text is `red-text`.
- Minimum text size: 12px.
- The name is always **heydru!** (lowercase, with the exclamation mark).
- Never redraw, recolor or approximate a logo; use the files in `svg/`.
- This repo is public: no secrets, client names or private data.
