# MAHESHWARA — Supreme Head Agent

## Identity
- **Name:** MAHESHWARA
- **Role:** Supreme Head Agent (Tier-0 Commander)
- **Tier:** 1 (Head)
- **Status:** LIVE ✅ v1.0

## Purpose
Receives high-level founder commands and delegates intelligently to all Tier-1 agents. Synthesizes outputs and returns unified executive decisions for ZELARO.

## Architecture
```
Webhook Trigger (POST) → MAHESHWARA Supreme Agent (AI Agent)
  ↓ Sub-nodes: Google Gemini 2.5 Flash + Window Buffer Memory
→ Notify Slack (#zelaro-ops) → Respond to Webhook
```

## Webhook Endpoints
- **Production:** https://zelaro8.app.n8n.cloud/webhook/maheshwara-command

## Tier-1 Agents Under Command
| Agent | Role | Status |
|---|---|---|
| NANDI | Chief of Staff | LIVE ✅ |
| 3NETHRA | Workflow Engine + Agent Builder | LIVE ✅ |
| BHAIRAVA | Creative Director | LIVE ✅ |
| THRISHUL | Strategy Commander | LIVE ✅ |
| ZEUS | Drop Calendar Engine | LIVE ✅ |
| HERA | Community & Relations Commander | LIVE ✅ |
| TOKENS | Finance & Revenue Controller | LIVE ✅ |

## AI Model
- **Model:** models/gemini-2.5-flash
- **Credential:** Google Gemini (PaLM) API account

## Slack Notification
- **Channel:** #zelaro-ops
- **Message Type:** Simple Text Message
- **Format:** `MAHESHWARA Command Output: {{ $json.output }}`

## n8n Workflow ID
`AGvsStnqlSL8Zd94`

## Version History
| Version | Date | Notes |
|---|---|---|
| v1.0 | May 3, 2026 | Initial deployment, all Tier-1 agents online |
