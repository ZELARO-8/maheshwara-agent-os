# NANDI — Chief of Staff

## Identity
- **Name:** NANDI
- **Role:** Chief of Staff
- **Tier:** 1
- **Status:** LIVE ✅ v1.0

## Purpose
Tasks coordination, prioritization, briefings, and operational oversight for ZELARO. Receives task assignments and returns structured action plans.

## Architecture
```
Webhook Trigger (POST) → NANDI Chief of Staff (AI Agent)
  ↓ Sub-nodes: Google Gemini 2.5 Flash + Window Buffer Memory + Action Plan Schema
→ Send to #zelaro-ops (Slack) → Respond with Status
```

## Webhook Endpoints
- **Production:** https://zelaro8.app.n8n.cloud/webhook/nandi-chief-of-staff

## AI Model
- **Model:** models/gemini-2.5-flash
- **Credential:** Google Gemini (PaLM) API account

## Slack Notification
- **Channel:** #zelaro-ops
- **Message Type:** Simple Text Message

## n8n Workflow ID
`AeontA7aets2mL4D`

## Version History
| Version | Date | Notes |
|---|---|---|
| v1.0 | May 3, 2026 | Initial deployment, Gemini 2.5 Flash, live |
