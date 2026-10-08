Status labels and the chart key: the role layer's feedback colors, for reports, proposals and dashboards.

- **Markup:** `<span class="status success|warning|danger|info">✓ Live</span>`. Always include a word, and lead with a glyph (✓ ! ✕ →), so meaning never depends on color alone.
- **Colors:** `status-success`, `status-warning`, `status-danger`, `status-info`. Each passes 4.5:1 as text in both themes. Square, 1px border in the text color, `role-label` type.
- **Danger is orange.** Brand red means "act here"; never use `red` for an error.
- **Chart key:** series in `chart-1` … `chart-5` order, `chart-1` for the subject, `chart-5` for the baseline. Prefer labelling lines directly over a separate key.
- Introduced with the role layer; heydru.com doesn't use these yet.
