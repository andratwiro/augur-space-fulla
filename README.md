# Fulla — Augur's example space

The demo content behind [demo.augur.works](https://demo.augur.works), and the
starter space for the [Augur engine](https://github.com/andratwiro/augur).
Fulla is a fictional product: coordination software for a community garden
(plots, watering rotas, harvests). Everything here is invented.

## Try it locally

Clone this repo and the engine side by side, then run the dev shell from in
here:

```bash
git clone https://github.com/andratwiro/augur.git
git clone https://github.com/andratwiro/augur-space-fulla.git
cd augur-space-fulla
node ../augur/scripts/dev.mjs
```

That's the whole setup: login rail, overlays, hot reload. Prototypes also open
directly from disk (`garden/prototypes/<name>/index.html`) — they are plain
self-contained HTML.

## What's in here

```
space.json                  the space's contract with the build
registry.json               the design system's overlay catalog (labels)
prototype-status.json       dev-status chips baseline
skills/fulla-ui/            the design system: wired-elements (hand-drawn
                            web components, vendored) + Fulla paper tokens;
                            skill.json declares what ships
garden/
├── context.md              internal brief — NEVER published (that's the point)
└── prototypes/
    ├── coordinator-dashboard   desktop overview for the garden coordinator
    ├── plot-care               mobile member app (SPA, three tabs)
    ├── garden-map              clickable hand-drawn map of the 48 plots
    └── seed-pod-3d             spinning botanical specimen (canvas live-tile)
base/ components/           gallery tier demos
playground/                 scratch space (ships verbatim)
```

Only `prototypes/` contents, the gallery tiers, `playground/` and the declared
skill assets publish. `context.md` and everything else beside them stays
private by construction — keep working notes next to the work.

## Licenses

Space content: MIT. Vendored inside `skills/fulla-ui/vendor/`:
[wired-elements](https://github.com/rough-stuff/wired-elements) (MIT,
© Preet Shihn) bundled as a single classic script, and
[Shantell Sans](https://github.com/arrowtype/shantell-sans) (SIL OFL 1.1).
