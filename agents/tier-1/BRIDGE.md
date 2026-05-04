# BRIDGE — Integration Hub

## Identity
- **Name:** BRIDGE
- **Role:** Integration Hub (routes data between ZELARO systems)
- **Tier:** 1
- **Status:** LIVE ✅

## Purpose
Receives integration requests and routes data between Notion, Slack, Gmail, and Google Drive based on integration type.

## Architecture
```
BRIDGE Webhook (POST)
  → Route by Integration Type (Switch)
    → Create Notion Page
    → Send to Slack
    → Send Gmail
    → Upload to Drive
    → Unknown Integration Type (Manual fallback)
  → Confirm to #zelaro-ops
  → Respond with Status
```

## Input Payload
```json
{
  "integration_type": "notion|slack|gmail|drive",
  "source": "string",
  "destination": "string",
  "payload": "object"
}
```

## Webhook Endpoint
- **Production:** https://zelaro8.app.n8n.cloud/webhook/bridge-integration-hub

## Routing Logic
| integration_type | Action |
|-----------------|--------|
| notion | Create Notion Page |
| slack | Send to Slack |
| gmail | Send Gmail |
| drive | Upload to Drive |
| unknown | Manual Review |

## Confirmation
- **Channel:** #zelaro-ops
- **Response:** Status object with routing result

## Version History
| Version | Date | Notes |
|---------|------|-------|
| v1.0 | 2025 | Initial deployment |

## n8n Workflow ID
`aYeuQLon3lw3gDjG`
