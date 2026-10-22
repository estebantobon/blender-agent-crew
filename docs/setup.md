# Setup

## Requirements

- Blender (version required by your chosen MCP server)
- Python 3.10+ if the MCP server needs it
- GitHub Copilot with MCP support enabled and Claude Opus available in your org

## 1. Install the Blender side

Install the Blender add-on from your chosen Blender MCP server. Enable it in Preferences > Add-ons, then start its server from the Blender sidebar.

## 2. Register the MCP server in Copilot

Add the server to your MCP configuration (for VS Code, `.vscode/mcp.json` or user settings). Example shape, adjust command and args to your server:

```json
{
  "servers": {
    "blender": {
      "command": "uvx",
      "args": ["blender-mcp"]
    }
  }
}
```

## 3. Pick the model

In the Copilot model picker, select Claude Opus.

## 4. Verify

Ask: "List the objects in the current Blender scene." If the agent returns them, the bridge works.

## Security notes

- The MCP server gives the agent control over your Blender session, including running Python. Run it only on trusted machines and scenes.
- Keep the server bound to localhost.
- Check with your security team before approving it for firm-wide use.
