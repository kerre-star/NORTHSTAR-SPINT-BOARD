# Northstar Sprint — Team Charter
**Project:** Northstar Retail Co. Support Deflection MVP  
**Duration:** 5 Days (Day 1–5)  
**Team Size:** 5 Members  
**Signed Off:** All 5 members ✅

---

## 1. Team Members & Roles

| Member | Role | Primary Responsibility |
|---|---|---|
| Suzanne Wanjiru | Project Manager | Charter, board management, audit log, go-live note |
| Dennis Gitau | Data & Integration Lead | Mock datasets, branch logic wiring, webhooks |
| Dorcas Yego | Design & Build Lead | Flow diagram, UI shell, branch UI integration |
| Keith Ngugi | Research & Taxonomy Lead | Ticket taxonomy, customer phrasing research |
| Timothy Kerre | QA & Documentation Lead | Full path testing, go-live readiness note |

---

## 2. Mission Statement

Build a working Support Deflection MVP for Northstar Retail Co. that reduces manual ticket handling for at least 2 of the 3 repetitive ticket categories — order status, returns & refunds, and stock availability — within 5 days. The product must be demoable end-to-end without a human agent in the loop.

---

## 3. Ways of Working

### Communication
- Primary channel: Team WhatsApp/Slack group
- Daily check-in: Every morning at 9:00 AM EAT (async message, not a call)
- Blockers flagged immediately — not end of day
- No member goes silent for more than 24 hours without notifying the group

### Task Management
- Board hosted on: [Trello / Notion / GitHub Projects]
- Board status updated **same day** the work is done — no batching
- Every task has: Owner + Priority + Definition of Done
- No task exceeds 4 hours — split if larger

### Commit/Edit Convention
All commits and edits follow this format:
```
<type>: <what changed> - <why it matters>
```
**Accepted types:** `feat` `fix` `docs` `test` `refactor` `chore`  
**Examples:**
- `feat: add order-status branch logic - enables users to track orders by ID`
- `fix: correct return eligibility condition - was approving non-returnable items`
- `docs: draft go-live readiness note - required for Day 5 delivery`

❌ `wip`, `updates`, `changes` are NOT acceptable commit messages.

---

## 4. Escalation Path

| Situation | Action | Who |
|---|---|---|
| Member shows 0 activity for 2+ days | Immediate private message, then group escalation | Suzanne Wanjiru |
| Task scope creep beyond 4 hours | Split task, update board same day | Task owner |
| Technical blocker | Post in group with specific question within 2 hours | Blocked member |
| Contribution imbalance flagged at Day 4 audit | Reassign tasks, document reason on board | Suzanne Wanjiru |

---

## 5. Definition of Done — Sprint Level

The sprint is complete when ALL of the following are true:

- [ ] Working prototype covers ≥ 2 ticket types, demoable end-to-end
- [ ] All 3 ticket categories handled in the bot flow
- [ ] 1-page go-live readiness note written and reviewed
- [ ] Raw audit log exported showing all member contributions
- [ ] Peer Reliability Index submitted individually and confidentially
- [ ] All board tasks marked Done with timestamps
- [ ] GitHub repository contains all required documents

---

## 6. Member Sign-Off

By contributing to this project, each member agrees to the ways of working, commit conventions, and escalation paths outlined above.

| Member | Confirmed ✅ |
|---|---|
| Suzanne Wanjiru | ✅ |
| Dennis Gitau | ✅ |
| Dorcas Yego | ✅ |
| Keith Ngugi | ✅ |
| Timothy Kerre | ✅ |

---
*Charter created: Day 1 | Last updated: Day 1*
