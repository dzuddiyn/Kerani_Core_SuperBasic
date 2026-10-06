# ACTION PLAN — Kerani_Core_SuperBasic

**Purpose:** Execute the short evidence-harvesting window without turning execution tasks into architecture decisions.  
**Authority:** Execution/progress only. `ZASS_Kerani_Core_SuperBasic.md` remains authoritative for questions, risks, decisions, experiments and readiness.  
**Planning date:** 2026-09-29  
**Source:** ZASS_Kerani_Core_SuperBasic.md v0.3.6 — same Git commit  
**ZERO → ARCHITECTURE snapshot:** 63% — DECIDING  
**Evidence Confidence snapshot:** LOW

---

# 1. CURRENT FOCUS

**Focus:** Freeze OpsMate as a reference implementation, harvest maximum reusable/Core and Agro evidence from it, prepare only a minimal SuperBasic skeleton, then PARK substantive implementation.

**Why:** The near-term window is too constrained for reliable Core architecture/build work. Evidence captured from a stable OpsMate baseline and pilot use is more valuable than rushing a speculative framework.

**Substantive Core implementation:** `PARKED` after the 15 October review until the owner explicitly restarts it with suitable local agentic-coding resources.

---

# 2. EXECUTION RULES

- Do not redesign OpsMate during extraction work.
- Respect the LOCKED product boundary: Core = Purchase / Sale / Inventory / Observation / Task + receipt capture; planned modules = Agro / Servis Teknikal / Makanan & Tempahan only.
- Free Core must remain independently useful for basic records, basic retrieval/reporting and operational-log summary; premium gates must explain what extra intelligence/automation requires credits.
- Treat Credit Pass/pay-per-capability as the current paid model direction; do not assume a mandatory subscription.
- Do not hard-code candidate credit values yet; 5/10/20/100 examples remain deferred until unit economics are measured.
- Preserve user data portability; do not create artificial export/data-access restrictions to enforce monetisation.
- Do not mark a charged capability as successfully consumed when execution fails.
- Keep full natural-language conversation in Kerani AI Premium; do not make it a SuperBasic dependency.
- SuperBasic constrained natural-language intake is allowed only as: intent suggestion → candidate/confidence → clarification if needed → preview → human confirmation → deterministic domain validation → authoritative record.
- Treat ambiguous input as a clarification test case; never reward the agent for guessing.
- Reject module work that creates special-case branching or Apps Script spaghetti.
- Do not treat source-file layout as architecture.
- Do not invent Core abstractions merely to create a skeleton.
- Do not change LOCKED ZASS decisions.
- Pilot findings are evidence: classify them as bug, observed gap or new requirement.
- Ordinary pilot findings do not automatically reopen the frozen reference baseline.
- Critical safety, data-integrity or reference-invalidating defects may trigger a deliberate freeze review.
- AI/Copilot should trace, document, classify, scaffold and test; architecture decisions return to the owner/ZASS.
- Human-facing execution should present only the next meaningful action by default; show full IDs/ledgers only for review/audit.
- Use a compact Project Pulse when orientation is useful: current stage, next stage, factual progress if measurable, and save/sync health.
- Never report SAVED/committed unless a real Git result exists; generated Markdown is not a persistence receipt.
- No coding agent receives unrestricted production credentials or production-message access.

---

# 3. 10–15 OCTOBER 2026 PLAN

| Date | Action | State | AI / Copilot role | Human role | Output / Done signal |
|---|---|---|---|---|---|
| **10 Oct** | Freeze OpsMate reference baseline | NEXT | Read repo state; collect commit SHA, relevant tests, known limitations and selected stable workflows. Draft reference metadata. | Confirm the freeze point and selected workflow scope. | Exact frozen commit + stable workflow list + limitations recorded. |
| **10 Oct** | Capture pilot findings | NEXT | Structure rough notes without inventing facts. Separate bug / observed gap / new requirement. | Supply actual pilot observations. | Pilot findings ledger exists; unresolved items are visible. |
| **11 Oct** | Build 3–5 Behaviour Maps | OPEN | Trace actual runtime end-to-end from frozen repo: entry point, route, queue, AI, guard, validation, approval, persistence and response. Include at least one free-text mutation/clarification path if supported by the frozen evidence. | Verify maps match observed behaviour. | 3–5 evidence-backed maps covering different workflow families, including constrained-NL behaviour where evidence exists. |
| **12 Oct** | Build reuse matrix | OPEN | Classify small behaviours as GENERIC / AGRO-GENERIC / OPSMATE-BSE-SPECIFIC / UNCERTAIN with code/test evidence. | Challenge classifications that appear too generic. | Evidence-backed reuse matrix; no whole-file classification shortcuts. |
| **13 Oct** | Extract candidate contracts | OPEN | Compare maps, identify repeated behaviour contracts and unresolved boundaries. | Accept/reject interpretations; do not LOCK architecture merely from repetition. | Candidate Request / Route / Candidate / Validation / Decision / Result / Event contracts documented. |
| **14 Oct** | Prepare minimal repository skeleton | OPEN | Create only evidence-justified folders/files, agent instructions and fixtures. Avoid framework code. | Review diff and reject speculative abstractions. | Minimal skeleton exists without fake maturity or domain leakage. |
| **15 Oct** | Review, package evidence and PARK build | OPEN | Produce gap report: what is proven, uncertain, missing and ready for future local-agent tasks. Optionally add one tiny contract fixture/test only if evidence is sufficient and time remains. | Decide what remains parked and what will be first task when build restarts. | Evidence package coherent; Core build marked PARKED; next restart task identified. |

---

# 4. PILOT FINDINGS FORMAT

Pilot notes may be rough. AI should normalise them into:

~~~text
ID:
Date:
Workflow:
What the user did:
What the system did:
Expected:
Classification: BUG / OBSERVED_GAP / NEW_REQUIREMENT
Severity:
Workaround:
Status:
Evidence/reference:
~~~

Do not convert a pilot request directly into Core architecture. Feed mature findings back through ZASS.

---

# 5. TARGET EVIDENCE PACKAGE BY 15 OCTOBER

Minimum useful outcome:

- frozen OpsMate commit SHA and reference scope;
- pilot findings ledger;
- 3–5 Behaviour Maps from materially different workflows;
- evidence-backed four-way reuse matrix;
- candidate behavioural contracts;
- constrained-NL evidence cases covering clear intent, ambiguous intent and incorrect/misrouted suggestion where available;
- explicit unresolved questions/risks;
- minimal repository skeleton and AI-agent instructions if time permits;
- optional small contract fixture/test only if it follows evidence already collected;
- one clear restart task for future local agentic coding.

**Not required by 15 October:**
- completed Kerani_Core_SuperBasic;
- confirmed architecture;
- production Telegram adapter;
- multi-provider framework;
- generic database abstraction;
- plugin system;
- Kerani Agro implementation;
- full non-farm proof application;
- additional domain modules beyond Agro, Servis Teknikal and Makanan & Tempahan;
- Kerani AI Premium natural-language conversation.

---

# 6. AI WORK MODE

For each task, AI/Copilot should:

1. read the frozen reference and relevant ZASS records;
2. inspect actual implementation/test evidence;
3. make the smallest evidence-backed artifact/change;
4. mark uncertainty explicitly;
5. run available tests/checks when code changes;
6. show changed files/diff and PASS/FAIL;
7. stop when an architecture decision is required.

Preferred task size: one workflow, one evidence table, one contract, one fixture or one small scaffold at a time.

---

# 7. STOP / PARK RULE

On **15 October 2026**, stop substantive Core work after the evidence review unless the owner explicitly extends the window.

After that:

`Kerani_Core_SuperBasic substantive build = PARKED`

Restart trigger:

`Owner explicitly restarts build with suitable local agentic-coding resources.`

The first restart session should consume the frozen evidence package rather than re-reading OpsMate from zero.

## POST-ARCHITECTURE DEPENDENCY

After a SuperBasic architecture is available:

1. Cross-audit it against the earlier Kerani Core work/discussions.
2. Build a small comparison/reuse matrix.
3. Adopt only capabilities that are demonstrably lightweight, generic and maintainable.
4. Reject or defer anything that adds unnecessary infrastructure, duplicated semantics or Apps Script spaghetti.
5. Only after capability boundaries are stable, evaluate Credit Pass unit economics and candidate prices.

## POST-PILOT GROWTH REVIEW

Do not design the full viral campaign before product proof.

After pilot completion and usable testimonials:

1. Review whether users experience Free Core as genuinely useful rather than a crippled demo.
2. Verify the free/premium boundary is understandable in real usage.
3. Collect authentic demonstrations/testimonials that can support public claims.
4. Review platform rules and suitability before choosing TikTok, Facebook Marketplace, Facebook groups/pages or other channels.
5. Choose launch messaging around practical micro-SME record discipline and data readiness; do not promise guaranteed grants, certification, financing or business outcomes.
6. Keep exact campaign, spend, copy, KPI and channel mix outside current architecture authority until this review.
