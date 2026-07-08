# ARPI MCP

Remote MCP server by [ARPI Inc.](https://arpi.ai) — AI-powered ECG analysis with ARPI's ECG AI.

Submit ECG images and receive AI-generated diagnosis reports directly from your MCP client.

- **Endpoint:** `https://mcp.arpi.ai/mcp` (Streamable HTTP)
- **Auth:** OAuth — the client is guided through login on first connection

## Tools

| Tool | Description |
|------|-------------|
| `authenticate` | Sign in to ARPI |
| `open_image_submission` | Start an ECG image submission |
| `submit_image_for_diagnosis` | Submit an ECG image for AI diagnosis |
| `fetch_diagnosis_reports` | Retrieve diagnosis reports |
| `list_available_capabilities` | List available analysis capabilities |
| `invoke_arpi_capability` | Invoke a specific analysis capability |

## Installation

### Claude Code

```bash
claude mcp add --transport http arpi-mcp https://mcp.arpi.ai/mcp
```

Or via the plugin marketplace:

```bash
claude plugin marketplace add arpi-ai/arpi-mcp
claude plugin install arpi-mcp@arpi-mcp
```

### Claude.ai / Claude Desktop

Settings → Connectors → Add custom connector → `https://mcp.arpi.ai/mcp`

### Other MCP clients

Any client supporting Streamable HTTP with OAuth can connect to `https://mcp.arpi.ai/mcp`.

## Repository layout

This repository contains registry/marketplace metadata only — the server itself is hosted by ARPI.

- `server.json` — [official MCP Registry](https://registry.modelcontextprotocol.io) listing
- `.claude-plugin/marketplace.json` + `plugins/arpi-mcp/` — Claude Code plugin marketplace

## Privacy & Support

- Privacy policy: https://arpi.ai/privacy
- Support: support@arpi.ai

ARPI's ECG AI is a medical AI service. Diagnosis reports are for reference and do not replace professional medical judgment.
