# 🏛 MAHESHWARA AGENT OS — ZELARO Empire
> **v1.1 | May 3, 2026 | Owner: Vinay Akula | ZELARO Founder**

ZELARO's 58-agent autonomous empire operating system. All workflows, agent specs, task assignments, and documentation live here.

---

## 🗺 Empire Hierarchy

### Tier 0 — God Layer
| Agent | Role |
|-------|------|
| 🏛 MAHESHWARA | Empire Architect |

### Tier 1 — Main Agents (8)
| # | Agent | Role | Status |
|---|-------|------|--------|
| 1 | 🔱 BUNNY | Empire Orchestrator | 🟡 Pending |
| 2 | 🐂 NANDI | Chief of Staff | 🔴 Not Built |
| 3 | 👁 3NETHRA | Workflow Engine + Agent Builder | ✅ LIVE |
| 4 | 🔱 BHAIRAVA | Brand & Creative OS | 🔴 Not Built |
| 5 | ⚡ THRISHUL | Revenue & Sales OS | 🔴 Not Built |
| 6 | ⚡ ZEUS | Tech & Product OS | 🔴 Not Built |
| 7 | 👑 HERA | Operations & Legal OS | 🔴 Not Built |
| 8 | 💰 TOKENS | Finance & Metrics OS | 🔴 Not Built |

### Tier 2 — Sub-Agents
| Parent | Subs |
|--------|------|
| 3NETHRA | FORGE · SPARK · BRIDGE |
| NANDI | HERALD · SCRIBE · SENTINEL |

---

## 📡 Stack & Connections

| Tool | Usage |
|------|-------|
| n8n | Workflow automation engine (zelaro8.app.n8n.cloud) |
| Notion | OS registry + documentation |
| Slack | Agent comms → #zelaro-ops |
| Gmail | Labels: [MAHESHWARA] [NANDI] [3NETHRA] etc |
| Google Drive | /MAHESHWARA/ → Logs · Briefs · Workflows |
| Google Calendar | MAHESHWARA Weekly Sync — Every Monday 9AM |
| Gemini 2.0 Flash | AI engine for all agents |
| GitHub | This repo — source of truth for all workflows |

---

## 👁 3NETHRA — Agent Builder (LIVE)

**Webhook (Production):** `https://zelaro8.app.n8n.cloud/webhook/3nethra-agent-builder`

**How to trigger:**
```bash
curl -X POST https://zelaro8.app.n8n.cloud/webhook/3nethra-agent-builder \
  -H "Content-Type: application/json" \
  -d '{
    "agent_name": "NANDI",
    "agent_role": "Chief of Staff",
    "agent_description": "Manages daily briefings, task routing, and founder calendar",
    "priority": "high"
  }'
```

**Flow:** Webhook → Format Inputs → ZELARO Agent Builder (Gemini 2.0 Flash) → Slack #zelaro-ops → Respond

---

## 📁 Repo Structure

```
maheshwara-agent-os/
├── README.md                    ← This file
├── agents/
│   ├── tier-0/
│   │   └── MAHESHWARA.md
│   ├── tier-1/
│   │   ├── 3NETHRA.md           ← LIVE
│   │   ├── NANDI.md
│   │   ├── BUNNY.md
│   │   ├── BHAIRAVA.md
│   │   ├── THRISHUL.md
│   │   ├── ZEUS.md
│   │   ├── HERA.md
│   │   └── TOKENS.md
│   └── tier-2/
│       ├── FORGE.md
│       ├── SPARK.md
│       └── BRIDGE.md
├── workflows/
│   ├── 3NETHRA-agent-builder.json
│   ├── MAHESHWARA-planner.json
│   ├── MAHESHWARA-validator.json
│   └── CEO-morning-briefing.json
└── docs/
    ├── activation-log.md
    └── gap-closure-log.md
```

---

## 📋 Activation Log

| Date | Action | Agent |
|------|--------|-------|
| May 3, 2026 | Fixed n8n failures (Gemini, Slack) | All workflows |
| May 3, 2026 | Closed 8 MAHESHWARA gaps | MAHESHWARA |
| May 3, 2026 | Built + Published workflow | 3NETHRA |
| May 3, 2026 | Created GitHub repo | ZELARO-8 |

---

*Scope: ZELARO + EVERYTHING AVAILABLE only. All work happens in existing pages. This is just the registry.*
