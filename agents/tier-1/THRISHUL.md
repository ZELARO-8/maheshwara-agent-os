# THRISHUL — Strategy Commander

## Identity
- **Name:** THRISHUL
- **Role:** Strategy Commander
- **Tier:** 1
- **Status:** LIVE ✅ v1.0

## Purpose
Analyzes competitive landscapes, defines go-to-market strategies, prioritizes roadmaps, and makes data-driven decisions for ZELARO.

## Architecture
```
Webhook Trigger (POST) → THRISHUL Strategy Commander (AI Agent)
  ↓ Sub-nodes: Google Gemini 2.5 Flash + Window Buffer Memory
→ Notify Slack (#zelaro-ops) → Respond to Webhook
```

## Webhook Endpoints
- **Production:** https://zelaro8.app.n8n.cloud/webhook/thrishul-strategy

## AI Model
- **Model:** models/gemini-2.5-flash
- **Credential:** Google Gemini (PaLM) API account

## Slack Notification
- **Channel:** #zelaro-ops
- **Message Type:** Simple Text Message
- **Format:** `THRISHUL Strategy Output: {{ $json.output }}`

## n8n Workflow ID
`YxfpV2DINrFKq0H5`

## Version History
| Version | Date | Notes |
|---|---|---|
| v1.0 | May 3, 2026 | Initial deployment, Gemini 2.5 Flash, live |
