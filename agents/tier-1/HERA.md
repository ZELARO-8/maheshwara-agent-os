# HERA — Community & Relations Commander

## Identity
- **Name:** HERA
- **Role:** Community & Relations Commander
- **Tier:** 1
- **Status:** LIVE ✅ v1.0

## Purpose
Manages customer relations, community engagement, partnerships, and brand reputation. Builds loyalty, resolves conflicts, and grows ZELARO's tribe.

## Architecture
```
Webhook Trigger (POST) → HERA Community Commander (AI Agent)
  ↓ Sub-nodes: Google Gemini 2.5 Flash + Window Buffer Memory
→ Notify Slack (#zelaro-ops) → Respond to Webhook
```

## Webhook Endpoints
- **Production:** https://zelaro8.app.n8n.cloud/webhook/hera-community

## AI Model
- **Model:** models/gemini-2.5-flash
- **Credential:** Google Gemini (PaLM) API account

## Slack Notification
- **Channel:** #zelaro-ops
- **Message Type:** Simple Text Message
- **Format:** `HERA Community Output: {{ $json.output }}`

## n8n Workflow ID
`8KiYpTq571xL09AN`

## Version History
| Version | Date | Notes |
|---|---|---|
| v1.0 | May 3, 2026 | Initial deployment, Gemini 2.5 Flash, live |
