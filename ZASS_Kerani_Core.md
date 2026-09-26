# ZASS_Kerani_Core

**Status:** INITIAL ZASS / ACTIVE  
**Date:** 2026-09-26  
**Owner:** Abang Hafiz  
**Source of truth:** This repository.  
**Rule:** Do not silently change LOCKED decisions. Suggestions are not decisions.

# 1. RAW IDEA

> “nanti kat chat Kerani Core, lepas OpsMate siap, aku nak set 1 per 1 rule, decision, arch dan lain-lain & nak try automate guna VS Code. rasa boleh??”

**EXPLICIT**

> “aku nak dia baca sendiri sheet, app script, aku cuma masukkan mock data test dalam Telegram. aku tak nak bagi access Telegram. biar dia clone repo, edit, commit je baru aku allow.”

**EXPLICIT**

> “dah hampir pasti guna VS Code + Copilot Student Agent. tapi bukan auto.”

**EXPLICIT**

> “Saya nak buat master sekali pun sedap kan ni. Boleh ke buat master, buat kerja biasa sambil background run vibe coding.”

**EXPLICIT**

> “vibe coding lama sikit tak apa janji stabil”

**EXPLICIT**

> “aku kena beli PC sebab laptop aku dah nazak, dengan gaya guna aku, laptop syarikat baru ni pun hang”

**EXPLICIT**

> “tapi kalau HA pun dalam ni, aku rasa tak cerdik kan”

**EXPLICIT**

# 2. WHY

- Personal laptop is “dah nazak”. **EXPLICIT**
- Company laptop also hangs under the owner's usage pattern. **EXPLICIT**
- One machine should support Master's/normal work while local agentic/vibe coding runs in background. **EXPLICIT**
- Stability matters more than maximum coding speed. **EXPLICIT**
- Coding automation is wanted without giving the coding agent Telegram access. **EXPLICIT**
- Reducing dependence on limited cloud-agent quota appears important. **INFERRED — not locked.**

# 3. GOALS

- **G-001 ACTIVE — EXPLICIT:** After OpsMate, structure Kerani Core rules, decisions, architecture and related knowledge one-by-one and automate as practical in VS Code.
- **G-002 ACTIVE — EXPLICIT:** Agent may inspect permitted TEST Sheet / Apps Script evidence, diagnose bugs, edit code and commit.
- **G-003 ACTIVE — EXPLICIT:** Owner alone supplies Telegram mock/test input; agent has no Telegram access.
- **G-004 ACTIVE — EXPLICIT:** PC is a stable main workstation for Master, normal work and development.
- **G-005 ACTIVE — EXPLICIT:** Local agentic coding should coexist with foreground work.
- **G-006 ACTIVE — EXPLICIT:** Stability is more important than maximum speed.
- **G-007 ACTIVE — EXPLICIT:** Remote-workstation use via Tailscale plus remote desktop is anticipated.
- **G-008 ACTIVE — EXPLICIT/LOCKED:** Production Home Assistant remains separate from workstation.

# 4. NON-GOALS

- **NG-001 — EXPLICIT:** Unrestricted/full-auto coding with Telegram access.
- **NG-002 — EXPLICIT:** Optimize PC primarily for maximum local-LLM speed.
- **NG-003 — LOCKED:** Host production Home Assistant on workstation.
- **NG-004 — DECIDED:** Antigravity is not a current focus; it is not formally rejected.
- **NG-005 — INFERRED:** ChatGPT Work is not assumed to be the routine engine for every small coding loop.

# 5. CONSTRAINTS

## Budget
- RM3,000 is a **target**, not a hard maximum. **EXPLICIT / DECIDED**
- Working range approximately **RM2,700–RM3,500**. **EXPLICIT / DECIDED**
- **1TB NVMe mandatory**; do not reduce to 512GB. **EXPLICIT / LOCKED**

## Workflow / access
- Detailed Kerani Core setup follows OpsMate completion. **EXPLICIT**
- Primary environment: VS Code + GitHub Copilot Student Agent. **LOCKED**
- Agent has no Telegram access. **LOCKED**
- Owner enters Telegram mock/test input. **LOCKED**
- Agent may find bugs using permitted TEST Sheet / Apps Script evidence and make code changes/commits. **LOCKED**
- If Copilot Student quota is insufficient, use the earlier AI-moderator + coding-agent technique. **LOCKED**
- Exact least-privilege mechanism for Sheet / Apps Script / logs is **UNKNOWN**.
- Exact Git push/merge approval boundary is **UNKNOWN**.

## Existing laptop
- Intel Core i5-13420H. **EXPLICIT**
- 8GB RAM. **EXPLICIT**
- RTX 2050 4GB. **EXPLICIT**
- Approximately 477GB storage shown. **EXPLICIT**
- Windows 11 Home Single Language. **EXPLICIT**

# 6. IDEAS / CANDIDATES

- **I-001 CANDIDATE:** Repository rules, decisions, architecture and tests act as durable agent guidance. **EXPLICIT intent; implementation INFERRED**
- **I-002 CANDIDATE:** Local AI can act as local/offline coding fallback. Exact model is **UNKNOWN**.
- **I-003 CANDIDATE:** Desktop can act as remote workstation via Tailscale + remote desktop.
- **I-004 DECIDED:** Keep HA production separate from development workstation.

# 7. QUESTIONS / UNKNOWNS

- **Q-001 OPEN:** How will the agent read TEST Sheets / Apps Script / logs with least privilege?
- **Q-002 OPEN:** What exact Git branch/push/merge approval boundary will be used?
- **Q-003 OPEN:** Which exact GPU within the locked **12–16GB VRAM** requirement will be purchased?
- **Q-004 OPEN:** Which exact local model/quantization/runtime will be used?
- **Q-005 OPEN:** Which exact motherboard, RAM kit, SSD, PSU and case will be purchased?
- **Q-006 OPEN:** Which remote desktop product will be used?

# 8. RISKS

- **R-001 OPEN — INFERRED:** Excessive agent permissions could expose production data/secrets.
- **R-002 OPEN — INFERRED:** Incomplete or contradictory repo guidance could cause architectural drift.
- **R-003 OPEN — INFERRED:** Actual local-model performance may differ by model, quantization, context and tool loop.
- **R-004 OPEN — INFERRED:** Used GPU condition may affect reliability.
- **R-005 MITIGATED — INFERRED:** Hosting HA on workstation would couple home automation uptime to workstation restarts/crashes; separation is LOCKED.
- **R-006 OPEN — EXPLICIT observation + INFERRED impact:** Cloud/coding-agent quota may be insufficient for routine work.

# 9. DECISION LEDGER

## D-001 — CPU
**Status:** LOCKED  
**Decision:** AMD Ryzen 5 5600.

## D-002 — GPU / VRAM
**Status:** LOCKED  
**Decision:** GPU specification is **12–16GB VRAM**. Exact GPU model is not locked.  
**Change:** This **SUPERSEDES** the previous locked requirement “RTX 3060 12GB”. RTX 3060 12GB remains a valid example inside the range, but is no longer the sole locked GPU model.  
**Reason:** Owner explicitly instructed on 2026-09-26 to overwrite the old RTX 3060 12GB lock with “spec adalah 12 - 16GB VRAM” and lock it.

## D-003 — RAM
**Status:** LOCKED  
**Decision:** 64GB DDR4, preferred 2×32GB; motherboard has 4 DIMM slots.

## D-004 — Storage
**Status:** LOCKED  
**Decision:** 1TB NVMe mandatory; 512GB is rejected.

## D-005 — PSU / cooling
**Status:** LOCKED  
**Decision:** Quality 650W Gold PSU and suitable case/cooling/airflow.

## D-006 — Home Assistant
**Status:** LOCKED  
**Decision:** Production HA remains separate from this workstation.

## D-007 — PC purpose
**Status:** LOCKED  
**Decision:** Main stable workstation for Master's work, normal work, development and local agentic/vibe coding, including background coding; stability > maximum speed; remote use anticipated.

## D-008 — Primary coding environment
**Status:** LOCKED  
**Decision:** VS Code + GitHub Copilot Student Agent is the primary Kerani Core coding environment.

## D-009 — Telegram / debugging boundary
**Status:** LOCKED  
**Decision:** Coding agent gets no Telegram access. Owner supplies Telegram mock/test input. Agent may inspect permitted TEST Sheet / Apps Script evidence, diagnose bugs, edit code and commit. If Copilot Student quota is insufficient, use the earlier AI-moderator + coding-agent technique.

## D-010 — Antigravity
**Status:** DECIDED  
**Decision:** Not current focus; not formally rejected.

## D-011 — PC budget
**Status:** DECIDED  
**Decision:** RM3,000 target; approximately RM2,700–RM3,500 acceptable.

# 10. LOCKED DECISIONS

- **L-001:** Ryzen 5 5600.
- **L-002:** GPU = **12–16GB VRAM**; exact model open. **Supersedes old RTX 3060 12GB-only lock.**
- **L-003:** 64GB DDR4, preferred 2×32GB; 4-DIMM motherboard.
- **L-004:** 1TB NVMe mandatory.
- **L-005:** Quality 650W Gold PSU + suitable cooling/airflow.
- **L-006:** Production HA separate from workstation.
- **L-007:** Main stable workstation for Master + normal work + development + local agentic/vibe coding; stability first.
- **L-008:** VS Code + GitHub Copilot Student Agent = primary coding environment.
- **L-009:** No Telegram access for coding agent; owner supplies Telegram mock/test input; permitted TEST Sheet/Apps Script debugging; AI-moderator fallback if Copilot quota insufficient.

# 11. SUPERSEDED / REJECTED / DEFERRED

## SUPERSEDED
- **S-001:** “RTX 3060 12GB is the locked GPU model” → superseded by **L-002: GPU 12–16GB VRAM, exact model open**.
- **S-002:** Temporary 32GB RAM possibilities → superseded by L-003.

## REJECTED
- **RJ-001:** Reduce SSD to 512GB → rejected by L-004.
- **RJ-002:** Host production HA on workstation → rejected by L-006.

## DEFERRED
- Exact GPU model within 12–16GB VRAM.
- Exact remaining component brands/models.
- Exact local model/quantization.
- Exact remote desktop product.
- Detailed Copilot automation configuration until OpsMate completion.

# 12. EXPERIMENTS / EVIDENCE

## E-001 — Controlled Copilot workflow
**Status:** PROPOSED  
**Question:** Can Copilot Student Agent work from repo rules/decisions/architecture plus permitted TEST evidence without Telegram access?  
**Method:** UNKNOWN — define after OpsMate.  
**Result:** Not run.

## E-002 — Local background agentic coding
**Status:** PROPOSED  
**Question:** Can the final workstation run the selected local coding workload stably while Master/normal work continues?  
**Success criterion:** Stability is required; exact metric is UNKNOWN.  
**Result:** Not run.

# 13. ARCHITECTURE READINESS

- [x] Workstation problem and major baseline decisions substantially clear.
- [x] Primary coding environment locked.
- [x] Telegram boundary locked.
- [ ] TEST Sheet / Apps Script least-privilege access mechanism defined.
- [ ] Git approval boundary defined.
- [ ] Copilot workflow experimentally validated.
- [ ] Local model/runtime validated.

**Readiness: NOT READY for final Kerani Core architecture.**

# 14. CHANGE CONTROL

LOCKED decisions must not be silently overwritten. Replacement requires a new decision, explicit relationship to the previous decision, and owner lock.

# 15. CHANGE SUMMARY — 2026-09-26

- Confirmed there was no prior authoritative Kerani Core ZASS file.
- LOCKED VS Code + GitHub Copilot Student Agent as primary.
- LOCKED Telegram boundary and AI-moderator fallback.
- Recorded Antigravity as not current focus, not rejected.
- Recorded RM3,000 as target with ~RM2.7k–3.5k range.
- **SUPERSEDED RTX 3060 12GB-only lock.**
- **LOCKED new GPU specification: 12–16GB VRAM; exact GPU model remains open.**
