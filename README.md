# Fulla, Augur's example space

The content behind [demo.augur.works](https://demo.augur.works), and the
starter space for the [Augur engine](https://github.com/andratwiro/augur).
Fulla is an invented product, coordination software for a community garden.
Plots, watering rotas, harvests. Everything here is fiction, including the
team.

## Try it

```bash
git clone https://github.com/andratwiro/augur.git
git clone https://github.com/andratwiro/augur-space-fulla.git
cd augur-space-fulla
node ../augur/scripts/dev.mjs
```

That is the whole setup. Prototypes are plain self-contained HTML and also
open straight from disk (`garden/prototypes/<name>/index.html`).

## What's in here

```
space.json                the space's contract with the build
registry.json             the design system's overlay catalog
prototype-status.json     dev-status chips baseline
skills/fulla-ui/          the design system: wired-elements (hand-drawn web
                          components, vendored) plus Fulla's paper tokens;
                          skill.json declares what ships
garden/
├── context.md            internal brief, never published (that is the point)
└── prototypes/
    ├── coordinator-dashboard    the coordinator's desktop overview
    ├── plot-care                mobile member app, three tabs
    ├── garden-map               clickable hand-drawn map of the 48 plots
    └── seed-pod-3d              spinning botanical specimen for live tiles
almanac/prototypes/sowing-wheel  the year as a wheel
signage/prototypes/plot-sign     printable A5 plot signs
base/ components/         gallery tier demos
playground/               scratch space, ships verbatim
```

Only `prototypes/` contents, the gallery tiers, `playground/` and the declared
skill assets publish. `context.md` and everything else beside them stays
private. Keep working notes next to the work.

## Licenses

Space content: MIT. Vendored inside `skills/fulla-ui/vendor/`:
[wired-elements](https://github.com/rough-stuff/wired-elements) (MIT,
© Preet Shihn) bundled as a single classic script, and
[Shantell Sans](https://github.com/arrowtype/shantell-sans) (SIL OFL 1.1).
