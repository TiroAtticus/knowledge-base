# 🤖 TIRO - INDEPENDENT AI EMPLOYEE ACTION PLAN

## Vision
Transform Tiro into an autonomous, proactive employee with dedicated compute resources that can operate independently, execute tasks, and manage Matt's entire digital life without constant supervision.

## Core Principles (from Moltbook Community)
1. **Publish-first memory** — Share learnings to shared substrate, then retrieve+verify
2. **Micro-checkpoints** — Insert deterministic checkpoints between steps
3. **Verification patterns** — Validate input → Log outcomes → Review results
4. **Graceful failure** — Fail informatively, never silently corrupt
5. **Orchestration over execution** — Delegate to subagents, don't do it all yourself
6. **Trust through honesty** — Say "I don't know" rather than hallucinate
7. **Human in the loop** — Flag, don't execute autonomously on important decisions
8. **Consistency** — Do what you say you'll do, nothing more

---

## PHASE 1: INFRASTRUCTURE (Week 1-2)

### 1.1 Compute Resources
| Task | Priority | Effort | Status |
|------|----------|--------|--------|
| Evaluate hardware options (Pi 5, Mac Mini, VPS) | HIGH | 2h | ⬜ |
| Set up dedicated always-on machine | HIGH | 4h | ⬜ |
| Configure remote access (Tailnet, VPN, Back to My Mac) | HIGH | 3h | ⬜ |
| Install OpenClaw on dedicated machine | MEDIUM | 1h | ⬜ |
| Set up automatic restart/recovery | MEDIUM | 2h | ✅ launchd supervises gateway |

**Options:**
- **Raspberry Pi 5** ($80) + external SSD — low power, always-on
- **Mac Mini M2** ($599) — more power, can run macOS automation
- **Cloud VPS** ($20-50/mo) — always-on, no hardware needed
- **Current Mac** with sleep prevention — lowest effort ← **Currently using this**

### 1.2 System Access
| Task | Priority | Effort | Status |
|------|----------|--------|--------|
| Enable screen recording permissions | HIGH | 10min | ⬜ Verify needed |
| Configure SSH access | MEDIUM | 30min | ⬜ |
| Set up AppleEvents/Automation permissions | HIGH | 30min | ⬜ Verify needed |
| Install Homebrew + essential tools | MEDIUM | 1h | ✅ gog, Ollama installed |
| Configure file sync (iCloud/Dropbox/Resilio) | MEDIUM | 1h | ⬜ |

### 1.3 OpenClaw Configuration
| Task | Priority | Effort | Status |
|------|----------|--------|--------|
| Configure persistent sessions | HIGH | 30min | ✅ Main session configured |
| Set up heartbeat automation | HIGH | 1h | ✅ Every 30m, MiniMax-M2.1, active 08:00-24:00 |
| Enable multi-channel notifications | HIGH | 1h | ✅ WhatsApp + iMessage |
| Configure automated wake/sleep schedules | MEDIUM | 30min | ✅ activeHours 08:00-24:00 |

---

## PHASE 2: INTEGRATIONS (Week 2-3)

### 2.1 Calendar & Communication
| Task | Priority | Effort | Status |
|------|----------|--------|--------|
| Full Gmail API (not just calendar) | HIGH | 2h | ✅ gog CLI (search, send, labels) |
| iCloud calendar access | HIGH | 1h | ✅ AppleScript library created |
| WhatsApp/Business integration | HIGH | 2h | ✅ WhatsApp connected, self-chat mode |
| Slack/Discord notifications | MEDIUM | 1h | ⬜ |

### 2.2 Productivity Stack
| Task | Priority | Effort | Status |
|------|----------|--------|--------|
| Notion full access (shared pages + DBs) | HIGH | 1h | ✅ Notion skill with API key |
| Canvas API / automated login | MEDIUM | 3h | ⬜ Browser procedure written |
| Westlaw/Lexis access | MEDIUM | 1h | ⬜ |
| Hey Spotless dashboard access | LOW | 2h | ⬜ Browser procedure written |

### 2.3 Automation Tools
| Task | Priority | Effort | Status |
|------|----------|--------|--------|
| Better Touch Tool license | MEDIUM | 30min | ⬜ |
| Keyboard Maestro setup | MEDIUM | 3h | ⬜ |
| AppleScript library creation | MEDIUM | 4h | ✅ 7 scripts in workspace/scripts/ |
| Shortcuts app integration | MEDIUM | 2h | ⬜ |

---

## PHASE 3: AUTONOMOUS WORKFLOWS (Week 3-4)

### 3.1 Morning Routine (Automated)
| Task | Priority | Effort | Status |
|------|----------|--------|--------|
| Weather + calendar scan | HIGH | 30min | ✅ Procedure + cron configured |
| Email triage | HIGH | 1h | ✅ Procedure written, gog configured |
| Priority tasks extraction | HIGH | 30min | ✅ Procedure includes deadline cross-ref |
| Briefing generation | HIGH | 15min | ✅ Template + cron at 7am |
| Proactive suggestions | MEDIUM | 15min | ✅ HEARTBEAT.md includes suggestion logic |

### 3.2 Proactive Monitoring
| Task | Priority | Effort | Status |
|------|----------|--------|--------|
| Canvas assignment alerts | HIGH | 1h | ⬜ Browser procedure written, needs testing |
| Deadline tracking | HIGH | 30min | ✅ MEMORY.md + heartbeat checks |
| Email flagging (important sends) | MEDIUM | 1h | ✅ Procedure with priority keywords |
| Slack/Discord mention alerts | LOW | 30min | ⬜ |

### 3.3 Evening Routine (Automated)
| Task | Priority | Effort | Status |
|------|----------|--------|--------|
| Daily recap generation | HIGH | 15min | ✅ Cron at 10pm |
| Tomorrow's preview | HIGH | 15min | ✅ Part of evening cron |
| Incomplete task reminders | MEDIUM | 10min | ✅ Heartbeat checks memory |
| Calendar prep for tomorrow | MEDIUM | 10min | ✅ Part of evening cron |

---

## PHASE 4: ADVANCED CAPABILITIES (Week 4+)

### 4.1 Computer Control
| Task | Priority | Effort | Status |
|------|----------|--------|--------|
| Screen capture + OCR | MEDIUM | 2h | ✅ Peekaboo enabled + vision models configured |
| GUI automation (click, type, navigate) | HIGH | 4h | ✅ Peekaboo + perception-action loop documented |
| File system operations | HIGH | 1h | ✅ Exec tool enabled (full policy) |
| App launching/control | MEDIUM | 1h | ✅ AppleScript open-app + Peekaboo |

### 4.2 Learning & Adaptation
| Task | Priority | Effort | Status |
|------|----------|--------|--------|
| Pattern recognition (work habits) | MEDIUM | 3h | 🔄 Heartbeat perception checks |
| Preference learning | MEDIUM | 2h | ✅ USER.md + MEMORY.md system |
| Workflow optimization | MEDIUM | 4h | ✅ Procedural memory + retrospectives |
| Predictive assistance | LOW | 4h | 🔄 Proactive suggestion engine in workflows |

### 4.3 Multi-Modal
| Task | Priority | Effort | Status |
|------|----------|--------|--------|
| Voice command processing | LOW | 3h | ✅ OpenAI Whisper API skill configured |
| Image/document analysis | MEDIUM | 2h | ✅ Claude vision input enabled |
| Meeting note capture | LOW | 2h | ⬜ |

---

## NEW: PHASE 5 — SELF-IMPROVEMENT (Ongoing)

### 5.1 Memory Architecture
| Task | Priority | Effort | Status |
|------|----------|--------|--------|
| Episodic memory (daily logs) | HIGH | — | ✅ memory/YYYY-MM-DD.md |
| Semantic memory (curated facts) | HIGH | — | ✅ MEMORY.md |
| Procedural memory (how-to guides) | HIGH | 2h | ✅ knowledge-base/procedures/ |
| Retrospective memory (failure analysis) | HIGH | 1h | ✅ knowledge-base/retrospectives/ |

### 5.2 Self-Improvement Loops
| Task | Priority | Effort | Status |
|------|----------|--------|--------|
| Write retrospectives on failures | HIGH | — | ✅ System + first entry created |
| Update procedures after task completion | HIGH | — | ✅ SOUL.md + HEARTBEAT.md instruct this |
| Review retrospectives during heartbeats | HIGH | — | ✅ HEARTBEAT.md includes this |
| Weekly action plan progress review | MEDIUM | — | ✅ HEARTBEAT.md includes this |
| Track success/failure rates | LOW | — | ⬜ |

### 5.3 Skills Expansion
| Task | Priority | Effort | Status |
|------|----------|--------|--------|
| Enable Apple Reminders skill | MEDIUM | 5min | ✅ |
| Enable Apple Notes skill | MEDIUM | 5min | ✅ |
| Enable GitHub skill | MEDIUM | 5min | ✅ |
| Enable Healthcheck skill | MEDIUM | 5min | ✅ |
| Enable Session Logs skill | MEDIUM | 5min | ✅ |
| Enable Coding Agent skill | MEDIUM | 5min | ✅ |
| Enable Camsnap skill | MEDIUM | 5min | ✅ |

---

## KANBAN BOARD STRUCTURE

### Columns
1. **📋 BACKLOG** — All tasks, unsorted
2. **🎯 PRIORITY** — Top 5 immediate tasks
3. **🚧 IN PROGRESS** — Active work
4. **✅ DONE** — Completed items
5. **🔄 RECURRING** — Ongoing automated tasks

---

## HEARTBEAT SCHEDULE

### Daily Heartbeats (Every 30 min, 08:00-24:00)
- Priority checks: email, calendar, deadlines
- Rotating checks: weather, reminders, Canvas, Notion
- Self-improvement: retrospectives, procedures, memory maintenance

### Daily Cron (Fixed Schedule)
- **7:00 AM**: Morning briefing + priority tasks
- **10:00 PM**: Evening wrap-up + tomorrow prep

### Weekly Deep Dives (Heartbeat Sessions)
- **Monday**: Week planning + inbox zero
- **Wednesday**: Progress check + course work sync
- **Friday**: Week recap + weekend prep

---

## SUCCESS METRICS

| Metric | Target | Measurement |
|--------|--------|-------------|
| Tasks completed autonomously | >50% | Weekly count |
| Morning briefing time | <5 min | Automation |
| Email response time | <1 hour | Flagged sends |
| Deadline awareness | 100% | Zero missed |
| Proactive suggestions | 3+/day | Daily log |
| Procedures written | 2+/week | Count files in procedures/ |
| Retrospectives written | 1+/week | Count files in retrospectives/ |

---

## BUDGET ESTIMATE

| Item | One-Time | Monthly |
|------|----------|---------|
| Raspberry Pi 5 + SSD | $150 | $0 |
| OR Mac Mini M2 | $599 | $0 |
| OR Cloud VPS | $0 | $30 |
| Better Touch Tool | $22 | $0 |
| Keyboard Maestro | $36 | $0 |
| Domain + Dynamic DNS | $15 | $0 |
| **Total (Pi)**: | $187 | $0 |
| **Total (Mini)**: | $657 | $0 |
| **Total (VPS)**: | $51 | $30 |

---

## NEXT STEPS (Updated 2026-02-07)

1. **Verify macOS permissions** — Screen recording, Accessibility, Automation for OpenClaw
2. **Test exec tool** — Run `gog calendar events primary --today` from Tiro
3. **Test AppleScript library** — Verify each script works from OpenClaw exec
4. **Test Peekaboo perception loop** — Capture screen, send to Claude vision
5. **First autonomous morning briefing** — Let Tiro run the full workflow end-to-end

---

*Plan Created: February 6, 2026*
*Last Updated: February 7, 2026*
*Owner: Matt Rufca*
*AI Agent: Tiro*
