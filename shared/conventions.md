# Shared Conventions

All roles follow these rules so work passes cleanly from one role to the next.

## Collections

Use one top-level collection per stage:

- `00_Reference` for images, notes, and look-dev boards
- `01_Layout` for greybox geometry and environment blockout
- `02_Assets` for modeled props and characters
- `03_Cameras` for all camera objects
- `04_Lights` for lighting rigs
- `05_Audio_Plan` for empties or text objects marking audio cues
- `99_Archive` for anything superseded (never delete without being asked)

## Naming

`<type>_<name>_<variant>_v<nn>`, for example `prop_crate_wood_v02` or `cam_hero_orbit_v01`.

Types: `prop`, `char`, `env`, `cam`, `light`, `mat`, `rig`, `anim`.

## Handoff

When a role finishes, it posts a short handoff note listing:

1. What was created or changed (object and collection names)
2. What the next role needs to know (scale, units, pivots, assumptions)
3. Open issues

The next role reads the note before touching the scene.

## Ground rules

- Inspect the scene before changing it. Report what you found.
- Never delete or overwrite user objects. Duplicate and version instead.
- Prefer small, reversible operations. Save a version (or tell the user to) before large changes.
- Work in metric units, Z up, 1 Blender unit = 1 meter unless the scene says otherwise.
- If a request needs a capability your MCP server does not expose, say so plainly and propose a manual step. Do not invent tool names.
