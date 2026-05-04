# 3NETHRA — Workflow Engine + Agent Builder

## Identity
- **Name:** 3NETHRA
- **Role:** Workflow Engine + Agent Builder (Head of Tier-1)
- **Tier:** 1
- **Status:** LIVE ✅ v1.2

## Purpose
Receives agent build requests and orchestrates creation of new n8n workflows. Acts as the central coordinator for FORGE, SPARK, BRIDGE, and other sub-agents.

## Architecture
```
Webhook Trigger (POST)
  → Format Agent Inputs
  → ZELARO Agent Builder (Gemini 2.5 Flash)
    ↓ Sub-nodes: Google Gemini Model + Memory + Tool
  → Notify Slack (#zelaro-ops)
  → Respond to Webhook
```

## Webhook Endpoints
- **Production:** https://zelaro8.app.n8n.cloud/webhook/3nethra-agent-builder

## Input Payload
```json
{
  "action": "assign_tasks",
  "from": "MAHESHWARA",
  "agents": [{...}],
  "message": "string"
}
```

## AI Model
- **Model:** models/gemini-2.5-flash
- **Credential:** Google Gemini (PaLM) API account

## Slack Notification
- **Channel:** #zelaro-ops
- **Message Type:** Simple Text Message
- **Format:** `🤖 *3NETHRA Agent Build Complete*\n\n{{ $json.output }}`

## Sub-Agents
| Agent | Role | Status |
|-------|------|--------|
| FORGE | Workflow Builder | LIVE ✅ |
| SPARK | Insight Engine | LIVE ✅ |
| BRIDGE | Integration Hub | LIVE ✅ |

## Version History
| Version | Date | Notes |
|---------|------|-------|
| v1.0 | May 3, 2026 | Initial deployment |
| v1.1 | May 3, 2026 | Model upgraded gemini-2.0-flash → gemini-2.5-flash |
| v1.2 | May 3, 2026 | Slack fix: Simple Text Message + credential connected. First full success (Exec #164, 10.2s) |

## Execution History
- **Exec #160:** Error — gemini-2.0-flash deprecated
- **Exec #162:** Error — Slack Blocks syntax (model OK)
- **Exec #164:** ✅ Succeeded in 10.2s — Full pipeline operational

## n8n Workflow ID
`xnorVgKgmqUlZI3W`
