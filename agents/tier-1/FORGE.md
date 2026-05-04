# FORGE — Workflow Builder Agent

## Identity
- **Name:** FORGE
- **Role:** Workflow Builder (sub-agent of 3NETHRA)
- **Tier:** 1
- **Status:** LIVE ✅

## Purpose
Receives workflow specs and generates complete n8n workflow JSON ready for import.

## Architecture
```
Webhook Trigger (POST)
  → FORGE Agent (Gemini 2.0 Flash)
    ↓ Sub-nodes: Memory + Tool
  → Notify Slack (#zelaro-ops)
  → Respond to Webhook
```

## Webhook Endpoints
- **Test:** https://zelaro8.app.n8n.cloud/webhook-test/forge-workflow-builder
- **Production:** https://zelaro8.app.n8n.cloud/webhook/forge-workflow-builder

## Input Payload
```json
{
  "workflow_name": "string",
  "workflow_description": "string",
  "trigger_type": "string"
}
```

## System Prompt
You are FORGE, the Workflow Builder for ZELARO OS. When given a workflow name and description, you generate a complete n8n workflow JSON specification ready for import. Include all nodes, connections, credentials, and logic.

## AI Model
- **Model:** models/gemini-2.0-flash
- **Credential:** Google Gemini (PaLM) API account

## Slack Notification
- **Channel:** #zelaro-ops
- **Message:** FORGE Workflow Generated — includes workflow name and spec

## Version History
| Version | Date | Notes |
|---------|------|-------|
| v1.0 | 2025 | Initial deployment — AI builder sub-agent |

## n8n Workflow ID
`yR5spugUoyr2FQBp`
