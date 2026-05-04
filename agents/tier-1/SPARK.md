# SPARK — Insight Engine

## Identity
- **Name:** SPARK
- **Role:** Daily Insight Engine
- **Tier:** 1
- **Status:** LIVE ✅

## Purpose
Runs every morning at 8am, analyzes previous day's activities, generates insights and actionable recommendations for the ZELARO founder.

## Architecture
```
Schedule Trigger (Daily 8am)
  → SPARK Insight Engine (Gemini 2.0 Flash)
    ↓ Sub-nodes: Chat Model + Memory
  → Send to Slack (#zelaro-ops)
  → Send to Gmail ([SPARK] Daily Insight Report)
```

## Schedule
- **Frequency:** Daily
- **Time:** 8:00 AM

## AI Model
- **Model:** models/gemini-2.0-flash
- **Credential:** Google Gemini (PaLM) API account

## Outputs
- **Slack:** #zelaro-ops channel
- **Gmail:** Subject: [SPARK] Daily Insight Report

## Version History
| Version | Date | Notes |
|---------|------|-------|
| v1.0 | 2025 | Initial deployment |

## n8n Workflow ID
`hzOVELtNeLVtHZBR`
