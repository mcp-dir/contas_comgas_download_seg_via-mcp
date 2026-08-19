# Instalação rápida

Comgás: Download de 2ª Via é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_contas_comgas_download_seg_via`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `Comgás: Download de 2ª Via` / `https://api.mcp.ai/p_contas_comgas_download_seg_via`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "contas_comgas_download_seg_via": { "type": "http", "url": "https://api.mcp.ai/p_contas_comgas_download_seg_via" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=contas_comgas_download_seg_via&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9jb250YXNfY29tZ2FzX2Rvd25sb2FkX3NlZ192aWEifQ==)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "contas_comgas_download_seg_via": { "url": "https://api.mcp.ai/p_contas_comgas_download_seg_via" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=contas_comgas_download_seg_via&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_contas_comgas_download_seg_via%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "contas_comgas_download_seg_via": { "type": "http", "url": "https://api.mcp.ai/p_contas_comgas_download_seg_via" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_contas_comgas_download_seg_via
```

Dúvidas? [contas_comgas_download_seg_via@mcp.ai](mailto:contas_comgas_download_seg_via@mcp.ai)
