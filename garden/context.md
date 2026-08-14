# Fulla — project brief (internal)

This note never publishes. It sits next to `prototypes/` to show how Augur keeps
research and working notes private while the prototypes ship.

## The product

**Fulla** is coordination software for community gardens. Plot assignments,
watering rotas, shared tasks, harvest logging. Small, warm, volunteer-run.

## The fictional garden (single source of truth for demo data)

**Hort de la Riera** — a community garden by the dry riverbed of a small
Catalan town. 48 plots, 61 members, 9 people on the waitlist.

- **Coordinator:** Núria (the dashboard's user)
- **Members seen in demos:** Pau, Marta, Joana, Omar, Greta, Íngrid, Toni, Assumpta
- **Plots:** numbered 1–48. Named plots for flavor: 7 "Les Faves", 12 "El Secà",
  23 "Tomàquets de la Marta", 31 "Racó de les Herbes", 40 "Bancal Nou"
- **Water points:** 2 (north tap, riera tap) · **Compost:** 3 bays, bay 2 "ready"
- **This week's drama:** plot 12 has missed 3 waterings (owner traveling),
  bay 2 compost is ready to distribute, Saturday is the fava bean sowing day
- **Harvest so far this season:** 312 kg (tomatoes 96, zucchini 74, favas 58,
  chard 41, herbs 19, other 24)
- **Rota:** Mon Pau · Tue Marta · Wed Omar · Thu Joana · Fri Greta ·
  Sat communal morning · Sun rest

## Voice

Informal, warm, designer-to-designer. Catalan garden vocabulary is welcome in
data (plot names, crops); UI copy stays English. No marketing words, no em
dashes, no "X: a, b, c" triads, no aphorisms.

## Design system

`skills/fulla-ui/` — forked look: wired-elements (hand-drawn web components)
+ Fulla paper tokens. In every prototype:

```html
<link rel="stylesheet" href="../../../skills/fulla-ui/fulla-tokens.css">
<link rel="stylesheet" href="../../../skills/fulla-ui/fulla-ui.css">
<script src="../../../skills/fulla-ui/vendor/wired-elements.js"></script>
```

- wired-* elements for controls (button, input, tabs, dialog, slider, toggle,
  checkbox, combo, listbox, progress, search-input…). Strokes follow CSS
  `color`; variants via `.f-primary` / `.f-secondary` / `.f-danger`.
- `.f-*` classes for everything else: `.f-card`, `.f-sticky`, `.f-stat`,
  `.f-chip--*`, `.f-table`, `.f-bar`, `.f-app`/`.f-sidebar` (desktop),
  `.f-phone`/`.f-tabbar` (mobile). Read `../../skills/fulla-ui/fulla-ui.css`.
- Emoji as icons is fine (🌱💧🍅🧑‍🌾♻️); keep it light.

## Prototype rules (Augur contract)

- Self-contained static HTML, `index.html` entry, must work opened via file://
  (classic scripts only, no ES modules, no external URLs, no fetch).
- One-line `<meta name="description">` on every prototype.
- A prototype that swaps screens without changing the URL keeps
  `<body data-gv-screen>` updated (the comment overlay scopes pins by it).
- Folder names are URL segments: kebab-case.
