# Instalação rápida

Banco PAN MCP é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_pan`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/customize/connectors?modal=add-custom-connector&mcpName=Banco%20PAN%20MCP&mcpServerUrl=https%3A%2F%2Fapi.mcp.ai%2Fp_pan)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors) → **+** → **Adicionar conector personalizado** → `Banco PAN MCP` / `https://api.mcp.ai/p_pan`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "pan": { "type": "http", "url": "https://api.mcp.ai/p_pan" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=pan&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9wYW4ifQ==)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "pan": { "url": "https://api.mcp.ai/p_pan" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=pan&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_pan%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "pan": { "type": "http", "url": "https://api.mcp.ai/p_pan" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_pan
```

Dúvidas? [pan@mcp.ai](mailto:pan@mcp.ai)
