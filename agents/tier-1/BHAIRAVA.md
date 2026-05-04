# BHAIRAVA — Creative Director

## Identity
- **Name:** BHAIRAVA
- **Role:** Creative Director
- **Tier:** 1
- **Status:** LIVE ✅ v1.0

## Purpose
Generates brand content, campaign copy, social media posts, visual briefs, and creative strategies. Bold, fiery, high-impact creative output for ZELARO.

## Architecture
```
Webhook Trigger (POST) → BHAIRAVA Creative Director (AI Agent)
  ↓ Sub-nodes: Google Gemini 2.5 Flash + Window Buffer Memory
→ Notify Slack (#zelaro-ops) → Respond to Webhook
```

## Webhook Endpoints
- **Production:** https://zelaro8.app.n8n.cloud/webhook/bhairava-creative-director

## AI Model
- **Model:** models/gemini-2.5-flash
- **Credential:** Google Gemini (PaLM) API account

## Slack Notification
- **Channel:** #zelaro-ops
- **Message Type:** Simple Text Message
- **Format:** `BHAIRAVA Creative Output: {{ $json.output }}`

## n8n Workflow ID
`tO0KUtfjNx5AWHBA`

## Version History
| Version | Date | Notes |
|---|---|---|
| v1.0 | May 3, 2026 | Initial deployment, Gemini 2.5 Flash, live |
