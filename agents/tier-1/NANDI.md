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

## Sub-Agents

### BRIEF-BOT
- **Workflow ID:** `w61bQbGPWqAjAuuF`
- **Webhook (Production):** `https://zelaro8.app.n8n.cloud/webhook/brief-bot`
- **Method:** GET
- **Status:** LIVE ✅ v1.0
- **Purpose:** Generates daily operational briefs for ZELARO. Synthesizes task lists, priorities, and project status into clear structured briefings for the team.
- **Model:** models/gemini-2.5-flash
- **Slack Output:** `#zelaro-ops` — prefix `BRIEF-BOT:`

## Webhook Endpoints
- **Production (Head Agent):** https://zelaro8.app.n8n.cloud/webhook/nandi-chief-of-staff

## AI Model
- **Model:** models/gemini-2.5-flash
- **Credential:** Google Gemini (PaLM) API account

## n8n Workflow ID
- **Head Agent:** (NANDI head workflow)
- **BRIEF-BOT Sub-Agent:** `w61bQbGPWqAjAuuF`
