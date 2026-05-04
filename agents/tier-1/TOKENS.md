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

## Sub-Agents

### REVENUE-TRACKER
- **Workflow ID:** `yWSaZvml18tkEjYT`
- **Webhook (Production):** `https://zelaro8.app.n8n.cloud/webhook/tokens-revenue-tracker`
- **Method:** POST
- **Status:** LIVE ✅ v1.0
- **Purpose:** Analyzes daily, weekly, and monthly revenue data. Identifies trends, flags anomalies, calculates MRR/ARR, and produces actionable financial summaries.
- **Model:** models/gemini-2.5-flash
- **Slack Output:** `#zelaro-ops` — prefix `REVENUE-TRACKER:`

## Webhook Endpoints
- **Production (Head Agent):** https://zelaro8.app.n8n.cloud/webhook/tokens-finance

## AI Model
- **Model:** models/gemini-2.5-flash
- **Credential:** Google Gemini (PaLM) API account

## n8n Workflow ID
- **Head Agent:** `Wzd5rydOa4tRbFPQ`
- **REVENUE-TRACKER Sub-Agent:** `yWSaZvml18tkEjYT`
