# Tool shed — project brief (internal)

This note never publishes. `garden/context.md` is the single source of truth for the
garden itself (people, plots, harvest, rota); this file only adds what the shed needs.

## The problem

The shed has one of most things and 61 people who need them. Nobody knows where the
long hose is until they walk down and find it gone. The rule has always been to write
your name on the whiteboard, and the whiteboard has been wiped by rain twice.

## The shed (demo data)

- **Where:** by the north tap. Key lives in the box beside it, code is the year the
  garden started.
- **Tools:** wheelbarrow, the long hose, loppers, spade, watering cans, glove box,
  step ladder. One of each, except the cans.
- **Out right now:** wheelbarrow (Omar, back Wednesday), the long hose (Marta, back
  tonight), spade (Pau, back Saturday).
- Anything out longer than a week surfaces on the coordinator dashboard.

## Prototype

`tool-board` — the board itself. Taking or returning a tool flips its card, and the
count in the header follows. The viewer is treated as the person holding the board,
so "Take it" puts their name on it.
