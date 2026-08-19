---
name: contas_comgas_download_seg_via-mcp
description: Skill da REST API do Comgás: Download de 2ª Via na MCP.AI: 1 endpoint em /api/contas_comgas_download_seg_via. Comgás: Download de 2ª Via, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago. Autentique com workspace API key (sk_live) gerada em app.mcp.ai/settings/api-keys. Use quando o usuário pedir algo coberto pelos endpoints.
---

# Comgás: Download de 2ª Via — REST API skill

Você tem acesso à **Comgás: Download de 2ª Via** REST API na MCP.AI.

> Comgás: Download de 2ª Via, consulta em fonte oficial. Hospedado pela plataforma, sem credenciais da plataforma, pague por consulta com crédito pré-pago.

## Base URL

```
https://api.mcp.ai/api/contas_comgas_download_seg_via
```

Todo endpoint é um **POST** na Base URL + o path abaixo. Os parâmetros vão no corpo JSON.

## Autenticação

Inclua em toda request:

```
Authorization: Bearer sk_live_...
Content-Type: application/json
```

> Gere sua chave em **https://app.mcp.ai/settings/api-keys** (workspace API key `sk_live_…`, não expira, revogável). Uma única chave serve pra todos os seus MCPs.

## Formato de resposta

```json
{ "ok": true, "tool": "<tool_id>", "result": <payload> }
```

## Exemplo cURL

```bash
curl -X POST https://api.mcp.ai/api/contas_comgas_download_seg_via/consultar \
  -H "Authorization: Bearer sk_live_..." \
  -H "Content-Type: application/json" \
  -d '{"codigo_usuario":"..."}'
```

## Reportar problemas

Se um endpoint retornar erro, vazio ou dado inesperado, reporte (não desista calado): **POST /api/contas_comgas_download_seg_via/report** com `{ "message": "...", "context"?: "...", "conversation"?: [...] }`. Isso notifica o time da MCP.AI.

## Endpoints (1)

#### `contas_comgas_download_seg_via_consultar`

Comgás: Download de 2ª Via, consulta em fonte oficial. _(POST /api/contas_comgas_download_seg_via/consultar)_

| Parâmetro | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `cnpj` | string | Não | Parâmetro de consulta "cnpj". |
| `codigo_usuario` | string | Sim | Parâmetro de consulta "codigo_usuario". |

---

Este MCP também funciona via **conexão MCP** (Claude / Cursor) em `https://api.mcp.ai/p_contas_comgas_download_seg_via` — veja o [README](../../README.md). A skill acima é pra consumir a **REST API** direto (agente próprio / código).
