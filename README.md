# Blender Agent Crew

A set of role-based agent instructions that turn a general coding agent (GitHub Copilot with Claude Opus) into a small 3D production team inside Blender, driven through a Blender MCP server.

Inspired by the role structure in Scenario's open-source Blender plugin. This project contains no Scenario code and does not call Scenario's service.

## How it works

- **Blender MCP server** is the connector. It exposes scene inspection, Python execution, and render control to the agent.
- **GitHub Copilot** is the MCP client, with Claude Opus as the model.
- **Roles** in `roles/` are focused instruction files. Each one tells the agent how to act as one member of the crew and which Blender operations to use.
- **Shared conventions** in `shared/` define naming, collections, and how roles hand work to each other.

## The crew

| # | Role | Focus |
|---|------|-------|
| 1 | Concept Artist | References and look development from the viewport |
| 2 | 3D Artist | Modeling, remeshing, cleanup of selected meshes |
| 3 | Animator | Rigging and keyframe motion |
| 4 | Surfacing Artist | Materials and PBR setup |
| 5 | Layout Artist | Greybox scenes, environments, lighting setup |
| 6 | Camera Operator | Camera paths, orbits, dollies, cranes |
| 7 | Render Artist | Stills and finished shots |
| 8 | Sound Designer | Audio planning and sequencer placement |

## Quick start

1. Install Blender and a Blender MCP server (see `docs/setup.md`).
2. Add the MCP server to Copilot.
3. Open this repo in your editor. Copilot picks up `.github/copilot-instructions.md`.
4. Ask for a role by name, for example: "Act as the Layout Artist and greybox a small warehouse interior."

## Status

Early draft. Role files describe capabilities in general terms. Map them to the exact tool names your MCP server exposes.

## License

Add a GPL-3.0-or-later LICENSE file if you reuse any GPL code from the projects this was inspired by. Confirm with your internal open-source review before distributing outside your organization.
