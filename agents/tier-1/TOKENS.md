# TOKENS — Finance & Revenue Controller

## Identity
- **Name:** TOKENS
- **Role:** Finance & Revenue Controller
- **Tier:** 1
- **Status:** LIVE ✅ v1.0

## Purpose
Tracks revenue, manages budgets, analyzes financial KPIs, forecasts cashflow, and optimizes pricing and margins for ZELARO.

## Architecture
```
Webhook Trigger (POST) → TOKENS Finance Controller (AI Agent)
  ↓ Sub-nodes: Google Gemini 2.5 Flash + Window Buffer Memory
→ Slack Simple Text Message (#zelaro-ops) → Respond to Webhook
```

## Webhook Endpoints
- **Production:** https://zelaro8.app.n8n.cloud/webhook/tokens-finance

## AI Model
- **Model:** models/gemini-2.5-flash
- **Credential:** Google Gemini (PaLM) API account

## Slack Notification
- **Channel:** #zelaro-ops
- **Message Type:** Simple Text Message
- **Format:** `TOKENS Finance Output: {{ $json.output }}`

## n8n Workflow ID
`Wzd5rydOa4tRbFPQ`

## Version History
| Version | Date | Notes |
|---|---|---|
| v1.0 | May 3, 2026 | Initial deployment, Gemini 2.5 Flash, live |
