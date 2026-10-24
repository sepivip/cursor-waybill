# waybill.ge Cursor plugin

Cursor plugin package for the hosted waybill.ge MCP server.

MCP URL: `https://waybill.ge/mcp`

This is not a Cursor Marketplace listing. Do not file https://cursor.com/marketplace/publish until the owner asks after merge.

## What it installs

A remote Streamable HTTP MCP server named `waybill`. After install, Cursor prompts you to authorize with waybill.ge (OAuth). You still need a waybill.ge account and at least one connected system (RS.GE, Balance, QuickShipper, a 1C (OneSoft) publication or Bank of Georgia). Balance, QuickShipper, 1C and Bank of Georgia access is read-only: waybill.ge cannot make payments or transfers at the bank. The public registry (NAPR) company, lien and property lookups and the National Bank of Georgia's official exchange rates need no connected system; they look up companies and property, not people.

## Local verify

1. Copy this directory to `~/.cursor/plugins/local/cursor-waybill` (do not symlink out of that folder; Cursor skips those links).
2. Run Developer: Reload Window.
3. Open Customize and confirm the `waybill` MCP server is present.

## Manual MCP JSON

```json
{
  "mcpServers": {
    "waybill": {
      "url": "https://waybill.ge/mcp"
    }
  }
}
```

One-click install (custom MCP connection, not Marketplace):

- Deeplink: `cursor://anysphere.cursor-deeplink/mcp/install?name=waybill&config=eyJ1cmwiOiJodHRwczovL3dheWJpbGwuZ2UvbWNwIn0=`
- Web helper: `https://cursor.com/en/install-mcp?name=waybill&config=eyJ1cmwiOiJodHRwczovL3dheWJpbGwuZ2UvbWNwIn0=`

Public install copy lives on https://waybill.ge/developers after that page ships.
