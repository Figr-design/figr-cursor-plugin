# Figr — Cursor marketplace

Public install source for the Figr Cursor plugin (MCP + `figr-mcp` skill + rule).

**Live repo:** https://github.com/Figr-design/figr-cursor-plugin (public)

## Install

### Local (fastest)

```bash
git clone https://github.com/Figr-design/figr-cursor-plugin.git
ln -s "$PWD/figr-cursor-plugin/figr" ~/.cursor/plugins/local/figr
```

Then **Developer: Reload Window** in Cursor. Confirm the Figr MCP server and `figr-mcp` skill under Customize.

### Team marketplace

Dashboard → Plugins → Add Marketplace → import this GitHub repo. Install the **figr** plugin for the team.

### Official marketplace

Submit at https://cursor.com/marketplace/publish when ready for public listing.

## Layout

```text
.cursor-plugin/marketplace.json   # marketplace name: figr
figr/                             # plugin name: figr
  .cursor-plugin/plugin.json
  mcp.json                        # → https://mcp.figr.design/mcp
  rules/figr-mcp.mdc
  skills/figr-mcp/
```

## MCP only

If you only need the server (no skill/rule):

```json
{
  "mcpServers": {
    "figr": {
      "url": "https://mcp.figr.design/mcp"
    }
  }
}
```
