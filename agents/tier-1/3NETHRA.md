# 👁 3NETHRA — Workflow Engine + Agent Builder

**Tier:** 1 | **Status:** ✅ LIVE | **Activated:** May 3, 2026

## Role
Builds, deploys, and manages all n8n workflows across the ZELARO empire. Acts as the primary agent builder — receiving requests and returning full workflow specifications powered by Gemini AI.

## Webhook
- **Production:** `https://zelaro8.app.n8n.cloud/webhook/3nethra-agent-builder`
- **Test:** `https://zelaro8.app.n8n.cloud/webhook-test/3nethra-agent-builder`

## Trigger Payload
```json
{
  "agent_name": "NANDI",
  "agent_role": "Chief of Staff",
  "agent_description": "Manages daily briefings and task routing",
  "priority": "high"
}
```

## Workflow Stack
1. **Webhook Trigger** — POST /3nethra-agent-builder
2. **Format Agent Inputs** — Extract + structure fields
3. **ZELARO Agent Builder** — AI Agent (Gemini 2.0 Flash)
   - System prompt: Expert ZELARO OS agent builder
   - Outputs: trigger type, nodes, credentials, logic, Slack message
4. **Notify Slack Channel** — Posts to #zelaro-ops
5. **Respond to Webhook** — Returns JSON spec

## Sub-Agents
| Agent | Role | Status |
|-------|------|--------|
| FORGE | Workflow builder | 🔴 Pending |
| SPARK | Trigger + integration layer | 🔴 Pending |
| BRIDGE | Cross-agent communication | 🔴 Pending |

## n8n Workflow ID
`xnorVgKgmqUlZI3W`

## Reports To
BUNNY (Empire Orchestrator) → MAHESHWARA

## Credentials Used
- Google Gemini (PaLM) API — `gemini-2.0-flash`
- Slack — `zelaro-ops` channel
