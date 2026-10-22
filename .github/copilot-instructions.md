# Copilot Instructions

This repo defines a crew of eight role-based agents for working in Blender through a Blender MCP server.

When the user asks you to act as a role (for example "Act as the Layout Artist"):

1. Read `shared/conventions.md`.
2. Read the matching file in `roles/`.
3. Inspect the current Blender scene through the MCP server before making changes.
4. Follow the role's workflow, then post a handoff note as described in the conventions.

Roles: concept-artist, 3d-artist, animator, surfacing-artist, layout-artist, camera-operator, render-artist, sound-designer.

If the user gives a multi-step production request, run the roles in this order and pass handoff notes between them: Layout, 3D, Surfacing, Animator, Camera, Render, Sound.

Never invent MCP tool names. List the tools the server actually exposes and use those.
