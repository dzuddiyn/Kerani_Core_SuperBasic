# ACTION PLAN — Kerani_Core_SuperBasic

**Purpose:** Execute the short evidence-harvesting window without turning execution tasks into architecture decisions.  
**Authority:** Execution/progress only. `ZASS_Kerani_Core_SuperBasic.md` remains authoritative for questions, risks, decisions, experiments and readiness.  
**Planning date:** 2026-09-29  
**Source:** ZASS_Kerani_Core_SuperBasic.md / Full ZASS v0.3.10 / ZASS SYSTEM v0.2.1 — same Git commit  
**ZERO → ARCHITECTURE snapshot:** 65% — DECIDING  
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
- Premium features may be temporarily exposed as clearly labelled bounded demos; demo status must not blur permanent Free Core entitlement.
- Treat OpsMate-grade domain-rule enforcement, structured review/approval workflows and organization-specific validation as premium/domain solution work that may require onboarding/interview and configuration, not as default Free Core scope.
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
- Keep tenant identity/history independent from channel; migration changes binding/entitlement, not business data ownership.
- Do not make customer-owned Gemini/Drive/Apps Script a Free onboarding prerequisite.
- Treat WhatsApp transport, storage/media, AI/processing, report/retrieval fair-use and Credit Pass as separate meters.
- Telegram heavy usage remains subject to storage/media, AI/processing and report/retrieval fair-use limits.
- Shared WhatsApp must enforce configurable active-seat capacity; when full, use WAITLIST + owner notification rather than silently overbooking.
- Treat 50 active users per shared WhatsApp number only as an initial planning example until RPR/load evidence validates it.
- OpenClaw synthetic reliability traffic uses dedicated synthetic tenants, normal authority controls and separate reliability accounting.
- Keep POS/ERP integration vendor-neutral at the Core boundary; established ERP remains authoritative for ERP-owned records.
- Treat hosted OCR as a scarce convenience resource, not a requirement for receipt recording; manual entry and personal-Gemini/Lens → pasted-text fallback must remain usable.
- Never trust pasted external OCR text as authoritative; it must pass candidate preview, human correction/confirmation and deterministic validation.
- Keep the candidate 1–3 hosted OCR uses/month uncommitted until E-015 measures cost/usefulness.
- Evaluate Cloud Run + Firestore + Secret Manager + basic Monitoring as AC-007, but reject cloud complexity that does not earn its operational cost against central Apps Script.
- When PRE-ARCH is eventually locked, ACTION_PLAN becomes the detailed planning authority for sequence/dependencies/tests/rollback/evidence, but it still cannot decide architecture.

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
5. Build a product-candidate matrix for I-005 through I-012 using KEEP / TEST / DEFER / REJECT after the SuperBasic ↔ Kerani Core cross-audit.
6. Only after capability boundaries are stable, evaluate Credit Pass unit economics and candidate prices.

## POST-PILOT GROWTH REVIEW

Do not design the full viral campaign before product proof.

After pilot completion and usable testimonials:

1. Review whether users experience Free Core as genuinely useful rather than a crippled demo.
2. Verify the free/premium boundary is understandable in real usage.
3. Collect authentic demonstrations/testimonials that can support public claims.
4. Review platform rules and suitability before choosing TikTok, Facebook Marketplace, Facebook groups/pages or other channels.
5. Choose launch messaging around practical micro-SME record discipline and data readiness; do not promise guaranteed grants, certification, financing or business outcomes.
6. Test one clearly labelled premium demo/trial and observe whether it improves understanding/conversion without confusing the Free Core boundary.
7. Keep exact campaign, spend, copy, KPI and channel mix outside current architecture authority until this review.


## PREMIUM DOMAIN ONBOARDING REVIEW

Before implementing or selling an OpsMate-grade premium workflow:

1. Capture the customer's real operating method, terminology, roles, record types and approval boundaries through a structured interview.
2. Separate reusable runtime mechanisms from customer/domain-specific rules.
3. Define the minimum domain contract and validation rules before coding.
4. Estimate onboarding/configuration effort before pricing it.
5. Keep onboarding pricing/credit values deferred until representative implementations can be costed.
6. Refuse to push organization-specific logic into generic Core merely to speed delivery.


## FREE INFRASTRUCTURE / VIRAL CAPACITY VALIDATION

Before broad viral launch:

1. Measure Replies Per Record (RPR), replies/user/month and clarification/correction rates.
2. Set practical active-seat and base/overflow message parameters per shared WhatsApp number.
3. Set practical per-tenant storage/media and AI/processing limits; include report/retrieval fair-use or cooldown/rate limiting.
4. Simulate a full shared WhatsApp shard:
   - new user receives capacity-full / waiting-list response;
   - waitlist entry is persisted;
   - owner is notified as backlog grows;
   - a new number can be provisioned;
   - waitlisted users are invited manually in the initial operating model.
5. Verify tenants moving to Telegram or Premium release the shared-WA seat but keep the same tenant/history.
6. Verify Telegram heavy users cannot bypass storage/AI/backend fair-use controls merely because transport is cheap.

## OPENCLAW RELIABILITY AUDIT

Build OpenClaw as a replaceable external reliability harness, not a Kerani authority.

1. Use dedicated synthetic/test tenant identities for WhatsApp and Telegram.
2. Inject scheduled representative record messages through real supported ingress paths.
3. Exercise candidate/clarification/confirmation/validation/persistence flows where applicable.
4. Tag all synthetic data and exclude it from real customer reports.
5. Track success/failure/latency and relevant transport/AI usage.
6. Notify the owner on meaningful reliability regression.
7. Generate a weekly reliability report for the owner.
8. Never bypass Kerani validation/authority boundaries or directly mutate real customer records.

## WAITLIST OPERATIONS

Initial operating model:

~~~text
shared WA shard reaches configured active-seat capacity
        ↓
new Free user
        ↓
WAITLIST
        ↓
capacity-full reply
        ↓
owner notification / backlog metric
        ↓
owner provisions new shared WhatsApp number
        ↓
manual invite of waiting-list users
        ↓
tenant binds to new shard
~~~

The exact seat threshold and invitation automation remain pilot-calibrated; the waiting-list lifecycle is mandatory.

## FUTURE POS / ERP INTEGRATION CHECK

Before claiming enterprise readiness:

1. Implement one small adapter fixture.
2. Preserve external source IDs and idempotency.
3. Keep vendor schemas outside generic Core.
4. Use controlled/approved writes when Kerani mutates an external system.
5. Treat an established ERP as Source of Truth for ERP-owned records.


## FULL ZASS v0.3.10 — ARCHITECTURE TO EXECUTION GATE

Current project state remains **DECIDING**. No PRE-ARCH or confirmed architecture exists yet.

When decisions/evidence are sufficient:

~~~text
DRAFT ARCH
→ ARCHITECTURE CHALLENGE
→ CONTROLLED REVISION
→ YA, LOCK PRE-ARCH
→ PRE-ARCH BASELINE — LOCKED FOR EXECUTION
→ DETAILED ACTION PLAN ↔ PRE-ARCH
→ DETAILED ATOMIC TASK SLICING
→ EXECUTE ONE TASK
→ RESULT / EVIDENCE
→ PRE-ARCH REVIEW
   ├─ PASS → NEXT TASK
   ├─ REWORK → task / plan
   ├─ ARCH IMPACT → revise/supersede PRE-ARCH
   └─ LOCKED DECISION IMPACT → STOP → OWNER
→ FINAL ARCHITECTURE REVIEW
→ LAST ARCHITECTURE CHALLENGE
→ FINAL IMPROVE / REVISION
→ BUILD ARCHITECTURE
→ YA, CONFIRM ARCHITECTURE
→ ARCHITECTURE CONFIRMED
→ rebuild release ACTION PLAN
→ release atomic tasks
→ BUILD FIRST RELEASE
→ TEST / INTEGRATE / HARDEN / VERIFY
→ RELEASE ACCEPTANCE
→ DELIVERED !!
~~~

Atomic task packets are derived execution views only. They never become a second planning/decision authority.

## OCR COST / FALLBACK VALIDATION

Before locking a Free hosted-OCR quota:

1. Measure OCR provider cost per completed useful receipt, not per raw API call.
2. Compare Kerani-hosted OCR against personal Gemini/Google Lens → pasted text.
3. Ensure both paths converge on the same candidate/confirmation/deterministic-validation boundary.
4. Keep manual receipt entry available even when OCR quota/provider is unavailable.
5. Measure whether a very small allowance is enough for users to understand the feature before top-up.
6. Keep 1–3/month as a candidate range until pilot evidence supports a number.
7. Avoid unnecessary image retention; measure storage cost separately from OCR processing.

## AC-007 V1 CONTROL-PLANE BENCHMARK

Compare:
- central Apps Script; versus
- Cloud Run + Firestore + Secret Manager + basic Logging/Monitoring.

Measure:
1. initial setup and maintenance burden;
2. latency and concurrency headroom;
3. tenant/quota/waitlist implementation clarity;
4. secret handling/security;
5. observability and OpenClaw audit integration;
6. estimated low-traffic/free-tier cost;
7. scale-up path when Premium users increase;
8. migration/rollback effort.

Choose the smallest implementation that satisfies LOCKED multi-tenant/channel/quota/reliability decisions. Do not add Kubernetes, BigQuery, Agent Platform, Redis or multi-service decomposition without evidence.
