 Northstar Retail Co. — Support Deflection MVP
 The Northstar Sprint 
Team: Suzanne Wanjiru · Dennis Gitau · Dorcas Yego · Keith Ngugi · Timothy Kerre  
Sprint Duration: 5 Days

What We Built

A conversational support chatbot for Northstar Retail Co. that automatically handles the 3 most repetitive customer support ticket types — reducing manual agent workload by an estimated 75%.

Live Demo: [https://landbot.online/v3/H-3493256-DR2064DXKIJOLLJ6/index.html]
 The Problem
Northstar's support team was drowning in repetitive tickets:
- 45% — Order status queries ("Where is my order?")
- 35% — Returns & refund queries ("How do I return this?")
- 20% — Stock availability queries ("Is this back in stock?")

These tickets required no specialist knowledge — just lookups and policy explanations. A bot could handle them.

 What the Bot Does

| Ticket Type | Bot Capability | Estimated Deflection |
|---|---|---|
| Order Status | Checks order ID + email/ZIP → returns live status + ETA | ~75% |
| Returns & Refunds | Checks eligibility → gives instructions or policy explanation | ~65% |
| Stock Availability | Looks up SKU/product → returns stock count + restock date | ~85% |

Additional features:
- Zapier integration — escalates unresolved cases to support inbox automatically
- CSAT collection — rates every resolved session 1–5
- Restock notifications — customers opt-in to email alerts
- Human takeover — damaged items and complex cases go straight to an agent

 Repository Structure
northstar-support-mvp/
│
├── README.md                    ← This file
├── TEAM_CHARTER.md              ← Team ways of working, roles, escalation path
├── TICKET_TAXONOMY.md           ← 8+ customer phrasings per ticket category
├── GO_LIVE_READINESS_NOTE.md    ← What works, known issues, handover guide
├── TEST_LOG.md                  ← 15 test paths with pass/fail results
├── AUDIT_LOG.md                 ← Full contribution history by member and day
├── mock-orders.json             ← 12 mock orders (shipped/processing/delayed/delivered)
├── mock-returns-policy.json     ← Return eligibility rules + 6 case examples
└── mock-inventory.json          ← 10 SKUs with size/colour variants + stock counts

 Sprint Results

| Metric | Result |
|---|---|
| Ticket categories covered | 3 of 3 ✅ |
| Test paths completed | 15 |
| Test paths passing | 14 / 15 (93%) |
| Known broken paths | 1 (product name search — non-blocking) |
| CSAT baseline | 4.2 / 5 |
| All board tasks completed | 18 / 18 ✅ |
 How to View the Bot

1. Click the demo link above
2. Type or click any of the 3 support categories
3. Follow the conversation — the bot handles the rest

No login required. Works on mobile and desktop.

 Assignments Delivered

| Assignment | Document |
|---|---|
| Assignment 1 — Charter + Board | `TEAM_CHARTER.md` + GitHub Project Board |
| Assignment 2 — Delivery + Audit Log | `GO_LIVE_READINESS_NOTE.md` + `AUDIT_LOG.md` |
| Assignment 3 — Baseline + Peer | Submitted individually (confidential) |


