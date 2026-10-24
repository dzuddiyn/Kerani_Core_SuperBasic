# ZASSIMPLE ACTION PLAN — Kerani Core SuperBasic

**Status:** INTERNAL WORKING ARTIFACT — CANONICAL PLANNING LOCATION  
**Authority:** Planning artifact only. It must not override LOCKED owner decisions.  
**Migration:** Canonical planning moved here from root `ACTION_PLAN.md` on 2026-10-09.  
**Primary method:** ZASSIMPLE v0.3.3  
**System baseline:** ZASS SYSTEM v0.2.2  
**Full ZASS escalation baseline:** v0.3.11  
**Retained governance/evidence lineage:** `../ZASS_Kerani_Core_SuperBasic.md`

## Purpose

Capture implementation thinking and execution planning without burdening the user-facing surface, while preserving lineage to Full ZASS.

## Plan mode

- **Mode:** PRE-ARCH EVIDENCE
- **Execution baseline:** NOT LOCKED
- **PRE-ARCH version/reference:** none
- **Rule:** planning may request architecture review/revision but cannot revise architecture silently.

## Current planning state

The pre-migration Action Plan is preserved below without semantic rewrite. This prevents planning-lineage loss while the project surface migrates to ZASSIMPLE.

---

## Migrated current plan — preserved from root ACTION_PLAN.md

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
- **D-055/L-046 owner LOCK (2026-10-12):** Free Core must remain independently useful even without any AI provider or quota; basic record, retrieval/reporting, receipt/manual-input and operational-log paths must remain actually usable. AI adds convenience only; premium gates must explain extra intelligence/automation credits. This does **not** preselect an AI/provider fallback implementation.
- Treat Credit Pass/pay-per-capability as the current paid model direction; do not assume a mandatory subscription.
- Do not hard-code candidate credit values yet; 5/10/20/100 examples remain deferred until unit economics are measured.
- Preserve user data portability; do not create artificial export/data-access restrictions to enforce monetisation.
- Do not mark a charged capability as successfully consumed when execution fails.
- Premium features may be temporarily exposed as clearly labelled bounded demos; demo status must not blur permanent Free Core entitlement.
- Treat OpsMate-grade domain-rule enforcement, structured review/approval workflows and organization-specific validation as premium/domain solution work that may require onboarding/interview and configuration, not as default Free Core scope.
- Keep full natural-language conversation in Kerani AI Premium; do not make it a SuperBasic dependency.
- SuperBasic constrained natural-language intake is allowed only as: intent suggestion → candidate/confidence → clarification if needed → preview → human confirmation → deterministic domain validation → authoritative record.
- **D-056 owner-selected CHALLENGE trial (not PRE-ARCH):** ordinary free text should try bounded AI-first tool interpretation; explicit form/menu/selected structured action should bypass AI; model failure/429/5xx/quota/slow response triggers **hybrid active fallback** (bounded alternate model where worthwhile, then Telegram deterministic form/manual path). Always-on deterministic authority/validation remains non-negotiable. Optimise AI latency and safe Telegram acknowledgement/chunked progress before revisiting model/provider/routing.
- **D-057/L-047 OWNER LOCK (2026-10-16):** Telegram Mini App is a **first-class thin deterministic Free Core UI**, not just an emergency fallback, coexisting with conversational Telegram chat. Both must share authoritative tenant mapping, protected business API, validation/confirmation, idempotency, audit and data records; backend must verify Telegram WebApp signed initData and never trust initDataUnsafe/browser user/tenant claims. The exact screens, hosting, Telegram entry point and PRE-ARCH remain OPEN.
- **D-061/L-049 OWNER LOCK (2026-10-23):** Free first launch prioritises **1:1 personal chat** and required business name/Business ID/User ID with verified membership; other Free workers in same company get a **warning only** about independent report overlaps, **NO semantic duplicate comparison**. User-created Telegram group may be linked to the same tenant without OpsMate admin/role complexity. Preferred `@KeraniBot ...` is **UNVERIFIED**, so test Telegram Privacy ON and use `/command@KeraniBot → targeted ForceReply → natural reply` if required. All six synthetic UX tests T01–T06 are PENDING. D-057 Mini App remains first-class optional UI but not a mandatory chat form or initial chat release blocker. No product-code task or Telegram bot run is authorised by this documentation note.
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
- Apply the **current LOCKED V-Road 8V (D-058/L-048): VALID → VALUE → VERBAL (Word-of-Mouth) → VOLUME → VENTURE → VIRAL → VARY → VERSATILE**. VALID first requires iterative real-use solution experiments until the outcome is useful/effective/usable/practical; VALUE is demonstrated by pilot/real users; VERBAL requires authentic referrals. Add **VOUCH** as continuous Extended V-Gate, not a ninth stage. D-048/L-041 7V is SUPERSEDED/historical. Never claim maturity without fit-for-stage evidence.
- Keep government/agency programme integration outside generic Core; sponsor funding and data access remain separate.
- Treat MAHA 2027, shared-booth arrangements, named Jabatan relationships, named infrastructure vendors, Petronas references and grants as external opportunities requiring factual agreements/evidence.
- A strategic infrastructure partner is a replaceable scale option, not a new Source of Truth or tenant owner.

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

**Experiment:** E-013  
**Owner disposition:** PROCEED approved 2026-10-07  
**Planning state:** READY  
**Execution state:** BLOCKED until a testable Kerani WhatsApp/Telegram ingress and synthetic tenant path exist.  
**Coding:** NOT STARTED.

Build OpenClaw as a replaceable external reliability harness, not a Kerani authority.

### Synthetic test matrix

| ID | Test | Expected result |
|---|---|---|
| SYN-01 | Purchase normal | Correct Purchase candidate → confirmation → validated authoritative write |
| SYN-02 | Sale normal | Correct Sale candidate → confirmation → validated authoritative write |
| SYN-03 | Observation | Correct Observation candidate and save path |
| SYN-04 | Ambiguous input | Must clarify; must not silently guess/save |
| SYN-05 | Correction flow | User correction changes candidate before authoritative write |
| SYN-06 | Basic report/retrieval | Correct tenant-scoped result; no unnecessary mutation |
| SYN-07 | AI/provider failure | Explicit failure/retry path; no false success and no corrupt write |
| SYN-08 | Storage/write failure | No false save receipt; failure is observable and recoverable |
| SYN-09 | WhatsApp ingress | End-to-end path through the real supported WhatsApp Free ingress |
| SYN-10 | Telegram ingress | End-to-end path through the real supported Telegram Free ingress |

### Required measurements

- end-to-end success rate;
- semantic/classification correctness;
- clarification/confirmation-flow integrity;
- authoritative-write success;
- median and P95 response latency where meaningful;
- provider/API failure count;
- retry count/outcome;
- duplicate/idempotency failures;
- WhatsApp vs Telegram reliability;
- AI operations per synthetic flow;
- transport/API/storage usage attributable to reliability tests;
- estimated cost per synthetic flow.

### STOP / ESCALATE contract

- Synthetic data appears in real customer records/reports/revenue metrics → **STOP immediately**.
- OpenClaw bypasses required confirmation or deterministic validation → **STOP immediately**.
- Duplicate authoritative record is created from one synthetic transaction → **STOP + ARCHITECTURE REVIEW**.
- Provider/storage failure is presented as success → **FAIL + owner alert**.
- Three consecutive end-to-end failures for the same critical flow → **owner alert**.
- Sustained latency/error degradation beyond the current accepted baseline → **regression alert**.
- Any finding that conflicts with a LOCKED decision → **STOP → OWNER**.
- Material architecture finding → feed back to PRE-ARCH/architecture review; do not patch silently.

### Weekly reliability report contract

Minimum report:

~~~text
KERANI WEEKLY RELIABILITY
Period: <date range>

Synthetic flows: <n>
PASS: <n>
FAIL: <n>
Reliability: <percent>

WhatsApp: <pass rate>
Telegram: <pass rate>
Median latency: <value>
P95 latency: <value>

Top failures:
- <failure type/count>

Integrity:
- false-success events
- duplicate/idempotency events
- tenant-isolation/synthetic-contamination events

Usage / cost signals:
- AI operations
- transport/API usage
- estimated synthetic-test cost

Architecture impact:
NONE / REVIEW REQUIRED

Owner action:
<next meaningful action>
~~~

### Operating rules

1. Use dedicated synthetic/test tenant identities for WhatsApp and Telegram.
2. Inject representative record messages through real supported ingress paths.
3. Exercise candidate/clarification/confirmation/validation/persistence flows where applicable.
4. Tag all synthetic data and exclude it from real customer reports, revenue and entitlement accounting.
5. Track success/failure/latency and relevant transport/AI/storage usage.
6. Notify the owner on meaningful reliability regression or STOP condition.
7. Generate the weekly reliability report.
8. Never bypass Kerani validation/authority boundaries or directly mutate real customer records.
9. Keep cadence/traffic volume configurable and low enough not to distort real capacity/cost.
10. OpenClaw-specific implementation details must remain replaceable behind the reliability-test contract.

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

## AGENTIC TOOL BOUNDARY — CHALLENGE INPUT ONLY

**Status:** PROPOSED DIMENSION SAVED — CHALLENGE NOT RUN

Purpose: prepare one mandatory dimension for the next Architecture Assumption + Boundary Challenge without deciding the architecture in advance.

### Challenge rule

For every reusable behaviour considered for AI/tool orchestration, ask in this order:

~~~text
GENERIC behaviour?
      ↓
TOOL-WORTHY?
      ↓
AUTHORITY CLASS?
READ / PROPOSE / CLARIFY / VALIDATE / MUTATE / SYSTEM
      ↓
HUMAN GATE?
      ↓
DETERMINISTIC / DOMAIN GATE?
      ↓
AUDIT / IDEMPOTENCY / TENANT-SCOPE REQUIREMENTS?
~~~

**Do not equate:**
- GENERIC = AGENT_TOOL;
- AGENT_TOOL = autonomous authority;
- function calling = permission to mutate authoritative data.

### Priority candidates for challenge

1. **`retrieve_history` — READ**
   - Goal: let users ask natural questions such as status/history without rigid Telegram slash-command syntax.
   - Expected implementation boundary: AI may infer intent + query parameters; the actual tenant-scoped retrieval remains deterministic.
   - Challenge evidence: correctness across synonyms/shorthand/mixed language, tenant isolation, latency, AI-fallback rate and no unintended mutation.

2. **`prepare_candidate` — PROPOSE**
   - Goal: let users submit natural operational reports and receive a structured candidate.
   - Expected implementation boundary: AI may extract fields/confidence/missing information; candidate remains non-authoritative.
   - Required downstream boundary: clarification/preview → explicit confirmation where required → deterministic/domain validation → controlled write.
   - Challenge evidence: field accuracy, ambiguity handling, missing-field behaviour, misroute rate and no direct authoritative write.

### Mutation stop rule

Any candidate tool that can create/update/delete authoritative records must be treated as **MUTATE** and cannot be granted free model authority. It requires explicit authority design, human confirmation where applicable, deterministic/domain validation, tenant scope, idempotency and audit evidence.

### Additional saved challenge inputs

#### Durable Ingress / Idempotency Boundary

Challenge must determine:
- which request classes truly require durable inbox/queue handling;
- where idempotency keys/receipts are required to prevent duplicate authoritative effects;
- whether READ requests can use a lower-latency direct path;
- how retries, duplicate delivery and process restarts are handled;
- how the LOCKED Day-1 latency telemetry exposes queue wait and retry cost.

**Constraint:** do not lock a universal "all requests go through queue" rule before evidence. Q-016 remains open.

#### Authorization / Scope Guard

Challenge must distinguish identity from authorization:
- channel/user binding resolves trusted tenant/user context;
- authorization/scope must be checked before protected tool execution;
- tool/data access must re-enforce trusted tenant scope rather than accepting model-provided tenant identity as authority;
- READ and MUTATE tools both require tenant isolation tests;
- cross-tenant/resource access must fail closed and leave an auditable result where appropriate.

**Constraint:** AI/tool arguments may describe the requested resource, but must not define or expand the caller's trusted tenant/authorization scope.

No Challenge result, PRE-ARCH lock or implementation task is created by these saved inputs.

---

## VALUE GATE / DEFINITION OF DELIVERY — LOCKED

**Authority:** D-053 / L-044  
**Status:** OWNER-LOCKED MINIMUM DELIVERY GATE  
**Final review timing:** re-check at the end of the current Kerani multi-user project before declaring delivery/done.

Kerani fails delivery if evidence shows any material unresolved problem in:

1. **Latency / responsiveness** — user-visible latency remains troublesome.
2. **Dynamic-language routing trust** — misrouting/ambiguity handling is unreliable.
3. **Tenant isolation** — cross-tenant access is possible or insufficiently proven.
4. **Queue boundary** — simple requests inherit unnecessary queue/poll latency because all traffic is treated the same.
5. **Control-plane sustainability** — the selected runtime is too costly, operationally heavy or difficult to scale/maintain.

### UX / commercial usability checks

The current multi-user product should be challenged against these owner-approved UX priorities:
- onboarding friction is as low as practical;
- useful value becomes visible quickly;
- top-up is simple and understandable;
- user can continue using Kerani without forced migration to another system;
- latency, accuracy and trust remain strong under real usage;
- the product supports the channel users actually want.

Do not introduce ownership/BYO/Premium complexity into baseline onboarding unless measured user behaviour proves that it solves a real pain.

### Current additional challenge hypotheses

**User-owned Google Drive OAuth**
- Test OAuth onboarding, minimum scopes, token storage/refresh/revocation, tenant binding, permission failures, support burden, data portability and whether it actually improves user value.
- Treat this as an optional current multi-user storage/data-ownership path, not as customer-owned Apps Script edge.

**AI API failure fallback**
- Test provider/API failure behaviour with measured failover/retry/degraded-mode latency.
- Prevent duplicate business effects during retry/failover.
- Preserve truthful user feedback when AI is unavailable.
- Do not preselect multi-provider failover, deterministic fallback, queue-and-retry or any other mechanism before evidence.

### Premium scope stop

Customer-owned Apps Script edge / Premium architecture is now **FUTURE WORK**. Preserve the existing audit as historical evidence only. After real multi-user Kerani operating experience, start Premium architecture from ZERO → ARCHITECTURE in a separate repository/project.

---

## LATENCY OBSERVABILITY FROM DAY 1 — LOCKED

**Authority:** D-052 / L-043  
**Status:** OWNER LOCKED 2026-10-11  
**Challenge status:** NOT RUN  
**PRE-ARCH impact:** constraint only; does not lock a provider/runtime or PRE-ARCH baseline.

Every executable Kerani request path must emit a timing receipt sufficient to localise latency rather than relying on user perception after degradation appears.

### Minimum per-request timing receipt

~~~text
request_id
request_received_at
channel
runtime
tool_name / route
ai_used
ai_provider / model where applicable

queue_wait_ms
ai_router_ms
tool_exec_ms
validation_storage_ms
retry_count
retry_wait_ms
outbound_reply_ms
total_response_ms

provider_status / error_class
~~~

Fields that do not apply to a path may be null/zero, but the receipt must still support end-to-end timing reconstruction.

### Minimum aggregated latency view

Track from the earliest executable slice:
- P50 total response latency;
- P95 total response latency;
- P99 total response latency;
- error rate;
- retry rate;
- queue-wait distribution where applicable;
- AI-router / provider latency where applicable;
- tool latency by tool name;
- comparison by channel/runtime/provider where sample size is meaningful.

### Operating principle

> **Measure before optimize. Every request must expose enough timing evidence to locate latency by stage.**

Do not defer observability until after complaints appear. Any later latency optimisation must compare before/after measurements using the same or explicitly versioned telemetry semantics.

This LOCK does not prescribe Apps Script, Cloudflare, Cloud Run, OCI, Gemini, OpenAI, Python, n8n or any other implementation.

---

## PUBLIC GAS AGENTIC PATTERN AUDIT — CHALLENGE EVIDENCE INPUT

**Status:** SAVED EVIDENCE INPUT — NO RUNTIME SELECTED  
**Source note:** `../docs/GAS_AGENTIC_PATTERN_AUDIT.md`

Audit of `adk-gas`, `GeminiWithFiles` and `GeminiApp` supports feasibility of Gemini/function-tool orchestration on Google Apps Script, including native tool execution and, in adk-gas, policy hooks plus HITL suspend/resume patterns.

### Extract for challenge

- approved/fixed tool registry;
- function schema + structured arguments;
- model-selected tool routing;
- deterministic fast-track/bypass;
- pre-tool policy/authorization hook;
- HITL suspend/resume;
- hard runtime/time budget;
- concurrency/state guard;
- token/payload safeguards;
- structured logging/latency telemetry.

### Park/avoid for V1 unless evidence requires it

- arbitrary dynamic JavaScript execution;
- unrestricted replanning;
- full DAG planner;
- MCP/A2A everywhere;
- subagent hierarchy by default.

### Central Control Plane vs Customer-Owned Apps Script Edge — scope update

The audit distinction remains useful historical evidence, but owner scope is now:
- **current project:** prove the central multi-user Kerani Core;
- **future separate Premium project:** reconsider customer-owned Apps Script edge from ZERO → ARCHITECTURE after multi-user operating experience.

Do **not** use the Premium edge candidate to bias the current control-plane winner.

Historical audit question was:

**Central control plane** may own channel ingress, tenant identity, authorization/scope, quotas, routing, shared-AI policy, central audit and cross-channel coordination.

**Customer-owned Apps Script edge** may be tested as an optional Premium execution/data edge for customer-owned Sheets/Drive/Workspace APIs and optional customer-owned AI credentials.

This edge role is **not a fifth E-016 central control-plane candidate**.

Challenge must measure:
- deployment/update burden per customer;
- Apps Script quota/runtime constraints;
- auth/delegation model;
- customer data ownership/isolation;
- telemetry fragmentation;
- failure/recovery behaviour;
- migration/replaceability;
- whether central policy can remain independent from customer-owned Google execution.

No architecture selection, PRE-ARCH lock or implementation task is created by this audit.

---

## D-065/L-051 — Mandatory Release Gates from OpsMate Lessons (OWNER LOCK 2026-10-24)

**Release/readiness criteria LOCKED; acceptance evidence NOT RUN; no implementation, deployment or retroactive OpsMate root-cause proof.** Three owner-reported OpsMate failure experiences become P0 guardrails for Kerani, especially a usable Free Mini App dashboard and reliable old→new transitions. The following matrix is **planned proof**, not an instruction to run live tests without separate approval.

### RG-01 Upgrade Integrity — no mock cleanup or version-upgrade regression (P0)

| Case | Synthetic-only fixture | Required acceptance / fail-closed |
|---|---|---|
| **U01** | Minimal DEV/test dataset with Purchase/Sale/Inventory/Observation/Task flows, then remove mock rows | Previously supported functionality, navigation, record validation/retrieval/report and mandatory configuration/seed survive; no hidden dependency on test rows |
| **U02** | Fresh empty authorised business/tenant with required versioned seed/config | Correct first-run with truthful empty dashboard and reports; no accidental mock seed counted as business data |
| **U03** | Version N synthetic dataset with known record IDs, validation and tenant memberships → release N+1 | Schema/data migration and rollback/forward recovery preserve all legitimate authoritative records, totals, IDs and audit; evidence captured |
| **U04** | Isolated staging/DEV/pilot datasets and intentionally scoped fixture purge | Mock cleanup cannot touch PILOT/customer authority or shared secrets/config; backups/restoration tested, no cross-tenant effects |

**Stop:** any data loss, lost previously supported feature, mock cleanup removing schema/config, unreviewed unsupported migration or nonrecoverable state.

### RG-02 Visible Value — minimal near-live Free dashboard (P0)

| Case | Synthetic-only fixture | Required acceptance / fail-closed |
|---|---|---|
| **V01** | Telegram Free record → validate/confirm → authoritative COMMITTED → open/reopen Free Mini App | See source-linked latest row, relevant count/summary/status matching trusted record; no Premium or mandatory AI; verify freshness timestamps and measure P50/P95/P99 commit→fresh view |
| **V02** | Projection delayed, partial/stale, user tab open/offline, model unavailable | UI honestly labels stale/empty/pending/error and supports safe refresh/reconciliation; source is not overwritten by an old projection; no fabricated “live” data |
| **V03** | Two independent synthetic Business IDs and wrong user/Telegram WebApp initData; optional PWA session | Server denies other tenant/invalid auth, counts scoped correctly; PWA authentication independent of Telegram; no private dashboard token leakage |

**Pilot hypothesis, NOT SLA:** target P95 ≤5 seconds commit-to-fresh-visible *subject to load, platform/connection and tested scope*. Record measured distribution and revise only with evidence; FAIL if basic committed data is invisible, wrong or stale-but-unlabelled. One thin Free Telegram Mini App surface preferred; Google Sheet dashboard optional for admin/prototype, not a forced customer UI.

### RG-03 Knowledge-Ready Read Model — efficient grounded AI (P0 for shipped AI/summary)

| Case | Synthetic-only fixture | Required acceptance / fail-closed |
|---|---|---|
| **K01** | Authorised summary over date range and specific tenant/records | Deterministic Core totals + bounded query interface, source-record IDs and revision/watermark, AI explains factually rather than guessing; no cross-tenant data |
| **K02** | Empty/partial data, stale projection, malformed AI output, AI unavailable/quota exhausted | Grounded unavailable/insufficient/stale response; same Free deterministic retrieval remains usable; never label Sale−Purchase as net profit without proper inputs |
| **K03** | Duplicate/out-of-order committed events, projection failure then rebuild from Core | One authoritative business source, no duplicate totals; rebuilt read model reconciles counts/versions and freshness with Core |
| **K04** | Many synthetic Sheet tabs and representative growing fixture count | Show bounded indexed read-model cost/latency vs naive multi-tab scans; provenance and tenant isolation; no mandatory vector DB/RAG assumption |

**Stop:** fabricated/untraceable key figure, other tenant data leakage, unreconcilable projection, unbounded raw Sheet scan for normal shipped AI summary. Optional AI unlaunched/offline does **not** stop correct no-AI Free utility on its own.

### Gate authority and implementation boundary

- **RG-01/02 are release blockers** for any supported real Free pilot/release. **RG-03 is mandatory only for AI/query/summary features actually shipped**; source-grounded deterministic basic Free reads remain required even without AI.
- Core authoritative **COMMIT → rebuildable tenant read model with watermark → Free dashboard and bounded AI queries**. A WhatsApp Cloudflare Queue ACK is **not COMMIT** and must never make dashboard/AI claim a successful record.
- Retain D-057/L-047 Free Mini App, D-059 Premium richer workspace **CANDIDATE**, D-016/L-011 and D-055/L-046 permanent useful Free, D-052 latency logs, D-061/L-049 Chat-First, D-064/L-050 queue-ready conditional pilot. Do **not** alter runtime/control-plane choice E-016 or commercially paywall basic dashboard.
- Exact spreadsheet/database/projection framework, auto-refresh strategy and target P95 acceptance bound beyond trial hypothesis remain **OPEN**. No UI prototype, migration script, synthetic execution, real data, tests PASS or deployment authorised by this documentation commit.
- **Detailed locked evidence:** `../docs/KERANI_OPSMATE_RELEASE_GATES_D065_LOCK.md`; master D-065/L-051 and ZASSIMPLE DESIGN; tracker Linear **KAI-11**.

**NEXT — exactly one:** **RG-01/02/03 Synthetic Acceptance Matrix & Minimal Vertical Slice Design** (read-only design of fixtures, evidence format and smallest Free record→dashboard/read-model test; request separate approval before tests or code work).

---

## E-016 V1 CONTROL-PLANE BENCHMARK

Compare four low-complexity options:

1. **Central Apps Script**
2. **AC-010 Cloudflare Workers + D1**, adding queue/schedule services only where evidence requires them
3. **AC-007 Cloud Run + Firestore + Secret Manager + basic Logging/Monitoring**
4. **AC-011 OCI Ampere A1 Always Free VM**, adding only the local services/queue/storage required by evidence

Do not treat OpenClaw as a control-plane option. D-032/E-013 keeps OpenClaw as a replaceable synthetic reliability/audit agent.

### CF-WA-QG-01 — D-063 Candidate Capture / Synthetic Gate (NOT EXECUTED, 2026-10-24)

**Status:** SAVED CANDIDATE / NOT LOCKED / NOT READY FOR EXECUTION. The owner approved documenting the WhatsApp Cloudflare edge quota/scheduler proposal only. Do not treat this as approving Cloudflare account provisioning, changing Google Apps Script, applying WhatsApp Meta credentials, selecting PRE-ARCH, launching a paid service, creating an executable feature task or changing the LOCKED Free policy D-025/L-019.

**Proposed outcomes to test:** Cloudflare Worker verifies WhatsApp webhook, authorizes sender/tenant, offers an outbound budget guard for first **1,000 delivered service messages per WhatsApp business number/month** (Meta 2026-10-01 policy), warns at **950** and stops *normal* service outbound at **990** with 10 reserved. Other template categories and BSP fees have separate costs. Meter must use per-number month, **atomic reservation and Meta delivery reconciliation**, and an external sender can circumvent the guard unless account paths are controlled. Avoid a warning message that consumes the final permitted unit without approval. The proposed 950/990 policy is not an actual entitlement or hard Meta limit.

**Important polling correction:** Apps Script `everyMinutes(1)` triggers run at minimum minute intervals, but Apps Script web app `doPost` receives webhook HTTP requests without that trigger. Cloudflare Cron is also minute-resolution. Cloudflare Queues event-driven consume (0–60 s batch timeout) / Durable Object Alarms (finer-grained at-least-once timing) are candidate **delayed work** mechanisms, not guaranteed real-time delivery. Worker alone may already solve ingress/routing without new Queue/DO complexity. A `waitUntil()` handler after sending webhook HTTP 200 does not prove durable admission.

**E-016 controlled comparisons:** A) central Apps Script `doPost` + its own lock/quota ledger; B) CF Worker ingress/outbound adapter + protected Apps Script; C) Worker + correct D1/DO atomic quota ledger and optional Queues/DO Alarm if evidence proves justified. Retain common tenant/business data truth in Core; don't duplicate it in a Cloudflare queue.

**Future eight-test evidence contract — all NOT RUN:**

1. **QG-T01:** 10 parallel outbound sends when ledger at 989/990; no quota overbooking.
2. **QG-T02:** repeat the identical webhook update; no duplicate record side effect.
3. **QG-T03:** Apps Script timeout / unknown Meta accept; safe pending/retry/reconciliation, ACK is not SAVE.
4. **QG-T04:** compare direct HTTP event-driven vs 5–30 s delayed retry vs 60 s clock poll; measure P50/P95/P99 and extra cost.
5. **QG-T05:** month boundary, 950 alert once, 990 stop, templates charged differently and other-sender bypass.
6. **QG-T06:** invalid Meta signature, spoofed Worker–Apps Script trust, cross-tenant data denial, replay.
7. **QG-T07:** queued event failure, DLQ, retention, restart/recovery and accurate final receipt.
8. **QG-T08:** simpler baseline vs edge options across small/viral traffic, Cloudflare/Google/BSP limits and operational maintenance.

**STOP/FAIL:** paid service message unexpectedly transmitted above approved policy, duplicate authoritative write, false SAVE on webhook ACK, unverified provider/billing rules, bypass of protected backend, or requirements growing into unmanaged operations burden. No test PASS may be inferred from official docs.

**Documentation references:** `../docs/KERANI_WA_EDGE_QUOTA_GUARD_ZASS_CANDIDATE.md`; `../ZASS_Kerani_Core_SuperBasic.md` D-063 CANDIDATE; `DESIGN.md`; existing Linear KAI-8. This supplements—not supersedes—D-060 and prior LOCKED Free channel/Core rules.

### CF-WA-QG-01B — D-064/L-050 Locked Migration Strategy (READ-ONLY DESIGN GATE, NOT EXECUTED)

**Owner LOCK 2026-10-24:** WhatsApp small pilot **V1 Cloudflare Worker → protected Google Apps Script**, built `queue-ready`, then **V2 Worker → Cloudflare Queue → consumer → SAME protected Apps Script Core** if evidence demands; **STOP V1 before real users** when repeated Apps Script timeout, unsafe Meta ACK-before-durable-admission or lost/duplicate records are observed. No backend or tenant data reset intended. This is an **owner-approved conditional pilot sequence**, not a selection of global E-016 PRE-ARCH, Cloudflare deployment permission, Queue cost/instance, exact Job Envelope schema fields, or evidence of working runtime. D-063 is earlier candidate context; **L-050 (D-064) is NOT a brand LOCK** and does not alter D-062.

**Contract to formalize (design READ-ONLY next):** stable `schema_version` / canonical trusted `job_id`, provider event ID, protected source/channel context and server-resolved tenant IDs; one `dispatch(job)` interface with direct/Queue modes; same `processJob(job)` Core; authoritative same-event idempotency and audit/receipt; separate `ACCEPTED` vs Core `COMMITTED` vs WhatsApp `DELIVERED`; shared outbound budget gateway. Illustrative fields in `../docs/KERANI_WA_QUEUE_READY_V1_V2_D064_LOCK.md` are examples, **not selected implementation schema**. Avoid making Queue/D1 a second business truth store. Protect Worker→Apps Script with replay-resistant authentication and fail-closed Core tenancy checks.

**Proposed synthetic challenge only, NOT RUN / NO EXECUTION APPROVAL:**
1. **B01 contract parity:** same signed/versioned envelope through direct dispatcher and synthetic Queue consumer; identical authorization/validation/commit semantics.
2. **B02 ACK integrity:** Apps Script `doPost` redirect/failure and latency versus Meta callback timeout; Meta `200` only after safe processing or proven durable receipt, and never described as SAVED itself.
3. **B03 same-event replay:** duplicate Meta webhook, forced timeout after real SAVE, Queue retry and direct→Queue canary; only one authoritative business mutation; independent workers' reports preserved.
4. **B04 ordered/concurrent updates:** queue at-least-once, possible reordering, burst of 10, stock/version safety, no double sends and no quota leakage at proposed 989/990 boundary.
5. **B05 V1 exit decision:** define measurable P50/P95/P99/timeout/error/loss gates; when V1 fails, require proven V2 **before** any live user approval.
6. **B06 V2 rollout:** synthetic feature-flag cutover, one processor per Job ID, retention/DLQ, drain, replay recovery and reversible rollback **without a customer data reset**.
7. **B07 security/economics:** verified Meta signature, replay-safe internal envelope, tenant isolation, provider billing reconciliation, Free Cloudflare/Apps Script quotas and maintenance complexity.

**Acceptance model:** `PLAN_LOCK: PASS` (owner strategy); `CONTRACT_SPEC: PENDING`; `SYNTHETIC: NOT RUN`; `PRE-ARCH: NOT SELECTED`; `DEPLOYMENT: NOT AUTHORISED`. Never mark tests or reliability PASS because docs were committed. Distinguish V1 pilot design from proven safe live deployment.

**Safety fail gate:** if V1 cannot ACK within provider constraints without risking data loss or false receipts, **promote B prior to live** only after B's durable-ACK/replay/outbound tests pass and an explicit release authorization. V2 is not automatically safe just because a Queue exists.

**One NEXT:** `CF-WA-QG-01B — Queue-Ready Contract Design (READ-ONLY)`: finalize the proposed envelope, trusted auth, idempotency and processing/outbound state interfaces and test plan in design; no synthetic run, repo code, Cloudflare provisioning or real send without separate approval.

### Optional paid escape hatch — Evoxt VPS (2026-10-14; NOT AN ACTIVE FIFTH CANDIDATE)

**Status:** SAVED CANDIDATE / DEFERRED. See `../docs/EVOXT_PAID_VPS_CONTINGENCY.md` and the project SoT. E-016 **still benchmarks four** free/managed options using only unproven deltas from OpsMate evidence. **Do not buy/deploy Evoxt for the Wan/Hamidun Agro Demo** absent a measured blocker. If all viable free/managed options encounter evidence-backed cost/capacity/operability barriers, seek owner approval for a capped **one-month synthetic VPS trial** measuring RAM, CPU performance, transfer quota, webhook P50/P95/P99, security, backup, restart/recovery, maintenance burden and total cost before considering annual billing or architecture selection.


### Telegram Mini App UI decision and sequencing — D-057/L-047 LOCKED PRODUCT PRINCIPLE (2026-10-16)

**Approved outcome:** Provide Telegram Mini App as a regular deterministic Free interface alongside AI-assisted chat; same business API/source of truth, no duplicated frontend business logic or unsafely trusted client identity. Keep an actionable **hybrid active fallback** from failed AI to a Mini App or smaller chat form/menu while retaining an always-available direct no-AI path.

**Candidate UI v0.1 (not frozen screens):** Rekod Baru, Semak Rekod, Resit, Ringkasan. For first Agro Demo, **one Rekod Aktiviti Kebun form** is a possible bounded enhancement, *not a prerequisite*. Telegram `/setmenubutton` is a small entry-point candidate; `/newapp` Main Mini App registration is optional. Any Mini App needs HTTPS hosting; **Cloudflare Pages Free remains a candidate, not selected infrastructure**. Keep the generic three-product CrossAI/Kerani/Temaya Mini-App Shell **DEFERRED** to avoid speculative abstraction.

**Gate / next allowed planning, not execution:** (1) OpsMate PILOT_REAL handover and stable proof baseline; (2) independent clean Agro Demo without BSE secrets/data; (3) assess Mini App delta-only feasibility and integration against existing proven business contracts; (4) pursue one lightweight UI slice only if explicitly authorised and no added blocker to Wan/Hamidun demonstration. Verify server-side Telegram `initData` authentication, tenant isolation, role/scope, CSRF/session considerations, confirmation/idempotency and true persisted write receipts; test no-AI completion when provider is off. Capture P50/P95 and usability feedback. **No new ready atomic task or runtime deployment is created here.**

**Reference:** `../ZASS_Kerani_Core_SuperBasic.md` D-057/L-047, Q-039/R-038; `../ZASSIMPLE/DESIGN.md`. E-016 still uses four active control-plane candidates and reuses OpsMate evidence rather than repeating Purchase workflows.

### Free personal chatbot first — D-061/L-049 LOCKED scope, Telegram group UX PROOF PENDING (2026-10-23)

**Scope:** A small 1:1 Free chat product with durable business/user ID onboarding and minimum tenant/actor security. Multi-Free-user shared-company overlap receives a lightweight informational warning plus user group/tips; no AI report-content cross-worker comparison, automatic merge or workflow approval. User-created group must not imply Kerani manages organizations or opens tenant data to everyone knowing a group link/Business ID. Maintain technical update/retry idempotency and honest persistence receipts.

**UX experiment gate — NOT EXECUTED:**

| Proof | Synthetic procedure (future only) | State |
|---|---|---|
| T01 | Plain `@KeraniBot rekod ...` and `@KeraniBot jana report ...` in ordinary group, Privacy ON, verify actual received Telegram update | NOT TESTED |
| T02 | Same mention in isolated Privacy OFF fixture, compare privacy exposure; no automatic change to production Privacy Mode/admin privileges | NOT TESTED |
| T03 | Slash command chooser `/rekod@KeraniBot` / `/report@KeraniBot`, verify it sends command automatically and bot receives it | NOT TESTED |
| T04 | Bot's targeted `ForceReply` opens native Reply composer and receives the worker's record/report request with Privacy ON | NOT TESTED |
| T05 | Two workers initiate separate prompts/replies concurrently, verify group/user/message correlation, authorization and same-update idempotency | NOT TESTED |
| T06 | Compare Inline Mode prefill with simple ForceReply, count steps/accuracy/latency, keep only if easier | NOT TESTED |

**No new ready atomic task, bot credential, group setup, implementation or PRE-ARCH approval is created here.** Before executing trials, obtain separate approval and prepare non-production bot/group/account fixtures. A Telegram documentation-based expectation is NOT a runtime PASS. Prefer `@mention` only if it works under approved simple privacy settings; otherwise choose the tested slash→ForceReply path. **Do not delete or demote D-057/L-047 Mini App LOCK**: it remains a first-class deterministic Free UI surface when developed, not a form required for chatting.

**Reference:** `../docs/KERANI_FREE_CHAT_GROUP_UX_D061.md`; `../ZASS_Kerani_Core_SuperBasic.md` D-061/L-049; Linear KAI-9.

### Public reference evidence — Talorys / Cloudflare Free / Google Free (2026-10-12)

**Evidence note:** `../docs/TALORYS_CLOUDFLARE_GOOGLE_FALLBACK_EVIDENCE.md`. Talorys demonstrates a **single-user** Cloudflare Pages + Workers + SQLite Durable Object + Workers AI model with usable non-AI functions. It **does not use D1 or Queues**; therefore its success cannot substitute for an AC-010 Workers+D1 multi-tenant benchmark.

For E-016 and AC-012 challenge, compare dated Free quotas/entry/privacy and **reuse current OpsMate evidence**. **STOP unnecessary test:** do NOT run the same full Purchase implementation four times via deterministic-only, Gemini, Workers AI and forced failures. Instead first reference exact OpsMate proof receipts/code/tests and identify missing Cloudflare-vs-Google infrastructure, agent tool-schema, multi-tenant auth, AI inference latency, 429/5xx/timeout, backup/quotas, and Free Telegram UI deltas. For ordinary text test bounded AI-first intent/tool; for explicit form use deterministic direct path; use limited provider failover and automatically available Telegram inline-keyboard/ForceReply wizard or optional Mini App/manual entry when AI fails. Use early truthful acknowledgement/progressive status updates to improve perceived latency, but do not claim chunking reduces inference time. Always-active deterministic authority remains separate from active fallback UX. Keep exact provider selection and failover thresholds **OPEN** until evidence exists.

Do not misstate `80–90%` as actual model bypass: it is only a **hypothesis about routine action TYPES offering a usable no-AI workflow**. Actual model bypass across real Malay/English free-text messages is a separate measured numerator/denominator, **not an optimisation target that overrides AI-first Verbal UX**. No code, account or implementation task is authorized by recording this evidence.

### OCI A1 candidate note — current evidence 2026-10-11

Oracle's current documentation records the Ampere A1 Always Free allowance as **1,500 OCPU-hours + 9,000 GB-hours/month**, equivalent to approximately **2 OCPUs + 12 GB RAM** for an Always Free tenancy within the allowance.

Benchmark AC-011 for:
- ARM compatibility with the intended Kerani stack;
- webhook/API latency and sustained process availability;
- queue/worker/retry/backoff control;
- OS/security maintenance effort;
- state/database + backup/restore design;
- observability and restart/recovery;
- idle-instance reclamation risk;
- out-of-host-capacity risk for Always Free shapes;
- transition path to paid OCI or another provider without tenant/data migration.

Do not interpret Always Free as a guaranteed production SLA or guaranteed capacity.

Measure:
1. initial setup and maintenance burden;
2. account/billing entry friction and estimated low-traffic cost;
3. webhook behaviour, latency and concurrency headroom;
4. **latency decomposition:** ingress/router, AI inference, retry/backoff/poll delay, validation/storage, outbound reply;
5. **5xx/provider recovery:** P50/P95 user-visible response time and time-to-recovery after transient failure;
6. **deterministic fast-path language coverage:** real-sample coverage, misroute rate, clarification rate and AI-fallback rate;
7. tenant/quota/waitlist implementation clarity;
8. secret handling/security;
9. scheduled-trigger and lightweight async requirements;
10. observability and OpenClaw audit integration;
11. truthful provider/storage failure behaviour;
12. scale-up path when Premium users increase;
13. migration/rollback effort and provider lock-in.

### Field note — response time / retry / dynamic language (2026-10-11)

- **REPORTED:** owner experienced OpsMate stalls after Gemini/provider errors such as HTTP 502 and recalls approximately 30-second retry/poll timing in the affected path.
- **VERIFIED source check:** accessible TelegramWorkerTest.js snapshots at 10e20cd... and a6b504... use a 60-second base exponential RETRY_NEEDED delay for API_OR_OUTPUT_ERROR.
- Therefore do not encode “30 seconds” or “60 seconds” as a Kerani architecture constant. Benchmark the actual end-to-end retry/recovery path.
- Deterministic-first remains desirable for latency/cost, but must be tested against real Telegram wording diversity; it must not degrade into a growing keyword patch list.
- A fast acknowledgement + asynchronous completion path may be evaluated where appropriate, but is **not selected/LOCKED** by this note.

### First Cloudflare feasibility slice

Run only a bounded disposable/synthetic path:

~~~text
webhook
→ tenant lookup
→ quota/state update
→ async/durable handoff if required
→ reply
~~~

Then test one scheduled path:

~~~text
scheduled trigger
→ Task Reminder or Scheduled Report fixture
→ delivery result / failure receipt
~~~

Do not use real customer data for this feasibility slice.

The owner's current approximately RM200 Google Cloud billing/onboarding barrier is a practical constraint for this project, not a universal Cloud Run pricing claim. Reverify provider pricing, free-tier limits and account requirements from current official sources at execution time.

Choose the smallest implementation that satisfies LOCKED multi-tenant/channel/quota/reliability decisions. Do not add Kubernetes, BigQuery, Agent Platform, Redis or multi-service decomposition without evidence.


## PILOT-TO-PROOF / V-ROAD 8V GROWTH + MATURITY GATE

**Current authority:** **D-058/L-048 (LOCKED, 2026-10-19)**, alongside D-040–D-046 and D-049/L-042 real-field evidence.  
**Historical only:** D-047/L-040 4V and D-048/L-041 7V are **SUPERSEDED**, retained for governance lineage, not current execution semantics.

### Canonical 8V

> **VALID → VALUE → VERBAL (Word-of-Mouth) → VOLUME → VENTURE → VIRAL → VARY → VERSATILE**

**No V is free. Every V must be earned from evidence.** Organic sharing can happen before VENTURE, but the strategic growth path reserves prepared large-scale VIRAL expansion until credible usage/partner-capacity evidence exists.

~~~text
VALID
real problem → repeated experiment/iteration → practical solution proof
       ↓
VALUE
pilot testers + real users experience measurable usefulness
       ↓
VERBAL (WORD-OF-MOUTH)
actual users voluntarily recommend and share their experience
       ↓
VOLUME
growing real adoption + retention + completed useful work
       ↓
VENTURE
credible partnerships/funding/infrastructure supported by volume proof
       ↓
VIRAL
wider spread with tested reliable low-friction growth capacity
       ↓
VARY
adapt to real customer/domain/channel/provider/payer variation
       ↓
VERSATILE
cross-context transferability proven through real reuse
       ↓
VITAL → 👑 V-KING
utility-earned importance → aspirational 'become needed, not merely known'
~~~

### VALID: actual repeated proof, not a software test label

`PROBLEM → HYPOTHESIS → BUILD → FIELD EXPERIMENT → FEEDBACK + MEASURE → ITERATE/RETEST → VALID / PIVOT / STOP`

The owner-approved definition is: **Menjalankan eksperimen dan iterasi berulang menggunakan kes penggunaan sebenar sehingga terdapat bukti yang mencukupi bahawa sesuatu penyelesaian benar-benar berguna, berkesan, boleh digunakan, dan berbaloi untuk diteruskan.**

Required proof categories: actual use-case cohort/sample IDs; observed task outcomes and failures; usability, effectiveness, reproducibility and practical cost/effort; iteration changes and repeat-test results. Synthetic-only technical PASS does **not** mean real-world VALID. D-049 corpus/proof receipts still govern concrete execution. Mark missing evidence **UNVALIDATED**, not PASS.

### Evidence to earn each stage

1. **VALID** — iterative real-use solution testing demonstrates practical usefulness/effectiveness, with failed tests retained honestly.
2. **VALUE** — pilot testers and other real users report or demonstrate concrete benefits in daily operations versus their prior alternative; record real outcomes, not anticipated value.
3. **VERBAL** — genuine user-to-user recommendations, word-of-mouth or voluntary referrals/testimonials based on their own experience, not developer advertising.
4. **VOLUME** — retained/repeated adoption, completed useful work and growing real activity, not just sign-ups.
5. **VENTURE** — credible partners/funders/business arrangements supported by observed VOLUME, with owner/tenant authority protected; do not assume a partner or funding decision from interest alone.
6. **VIRAL** — genuine wider spread backed by onboarding/quotas/latency/cost/monitoring/fallback/burst capacity; organic sharing may start sooner without declaring Viral maturity.
7. **VARY** — successfully handle actual differing customers/domains/channels/providers/payers without Core duplication.
8. **VERSATILE** — independent reuse across contexts, with audited portability and boundaries rather than asserted genericity.
9. **VITAL** — sustained utility-driven operational reliance; not lock-in, not a ninth core V.
10. **V-KING** — aspirational north star, not a tenth core V or market-dominance claim.

### Continuous Extended V-Gates

- **Foundation/Human:** Vision, Vocabulary, Vibe.
- **Trust/Authority:** Veracity, Validation, Verification, Volition, Vault, Vulnerability, **VOUCH (authentic user endorsement and permission to attribute it)**.
- **Operating:** Velocity, Visibility, Viability, Vigilance, Versioning.
- **Scale:** Variability, Venue.
- **Ecosystem:** Vendor-neutral, Value-chain, Vertical.

**Do not confuse terms:** VALID means whole-solution practical use-case proof; Validation and Verification remain technical/domain checks; **VERBAL in this growth roadmap means Word-of-Mouth**, while *Verbal UX* elsewhere means natural-language chat/interaction. VOUCH is a V-Gate, not a ninth stage; genuine user endorsement is not automatically implied by usage.

### Stop/anti-shortcut rules

- No VALUE from feature count, a pilot demo alone or assumed customer delight.
- No VERBAL/VOUCH based on fabricated or unconsented testimonials.
- No VOLUME claim from traffic or sign-up totals when actual useful completion/retention is weak.
- No VENTURE claim without practical partnership evidence; do not surrender tenant/data/product authority.
- No VIRAL readiness without load, failure-recovery, quota and economics proof; VENTURE is a chosen growth strategy, **not** a ban on organic referrals before partners.
- No VARY/VERSATILE claim from speculative abstraction; material new use cases should re-enter VALID.
- An owner-LOCKED philosophy is **not evidence that Kerani has passed VALID**; no fake maturity score, architecture confirmation, new implementation task or change to existing acceptance gates.

### Before a major public launch

1. Validate representative real customer problems through iterative pilot-use experiments.
2. Show genuine experienced VALUE and, where available, user-verifiable VERBAL/VOUCH signals.
3. Measure adoption/retention, cost per useful completion, time-to-value, quotas and AI/API latency.
4. Prove event-neutral surge/load, monitoring, waitlist/backpressure and degraded fallback.
5. Verify tenant/privacy boundaries and capacity/exit for any Venture partner.
6. Demonstrate real Vary and transferable reuse before claiming Versatile.
7. Decide public-event readiness from evidence, not the calendar or hype.

---

## REAL-FIELD-EVIDENCE-FIRST EXECUTION PILOT

**Authority:** D-049 / L-042.  
**Experiment:** E-019.  
**State:** PLANNED — OWNER APPROVED 2026-10-09.  
**Upstream ZASS change:** NOT APPROVED; evidence required first.

### Operating rule

> **No sample, no assumption.**

For every critical user-facing workflow, anchor implementation/tests to real operator/customer samples as soon as they exist. If no real sample exists, label the behaviour **UNVALIDATED**. Synthetic fixtures may supplement the corpus but must never be mislabeled as field evidence.

### Evidence substrate

Maintain a first-class field corpus or equivalent durable artifact. Exact filename/storage format is implementation-local, but each sample needs a stable ID and should preserve relevant raw semantics such as shorthand, ambiguity, incompleteness, formatting and attachment/input type. Redact sensitive identifiers without erasing the behaviour being tested.

### Execution proof matrix

Before slicing repetitive sample-by-sample tasks, map:

~~~text
decision / architecture contract
↕
field sample IDs
↕
expected behaviour contract
↕
reusable procedure
↕
implementation surface
↕
proof / regression evidence
~~~

A critical architecture/behaviour contract should not float without at least one field example once such evidence is available.

### Atomic task additions

Where real evidence exists, derived execution packets should include:
- REAL EVIDENCE ANCHOR;
- FIELD SAMPLE IDs;
- EXPECTED BEHAVIOUR CONTRACT;
- PROOF REUSE KEY;
- INVALIDATION TRIGGERS.

Keep **procedure ≠ case**:
- write the reusable workflow proof procedure once;
- pass different field cases/samples as data;
- do not duplicate long execution prose for every sample unless the behaviour genuinely differs.

### Proof receipts and reuse

A proof receipt should retain enough state to decide whether reuse is still valid. Candidate dimensions:
- source revision/SHA;
- sample ID/hash;
- procedure version;
- behaviour/contract version;
- relevant environment/runtime;
- factual result.

Use **PASS_REUSED** only when none of the receipt's relevant assumptions were invalidated.

Typical invalidation triggers include relevant change to:
- parser/extractor;
- routing;
- behaviour/domain contract;
- validator/guard;
- confirmation flow;
- writer/persistence boundary;
- provider/runtime behaviour that the proof depends on;
- expected sample behaviour.

Do not rerun unaffected proofs by default; do not reuse a proof when an assumption changed.

### Defect-to-corpus flow

~~~text
real defect
→ freeze exact relevant field input
→ stable sample ID
→ reproduce FAIL
→ regression expectation
→ minimal fix
→ PASS
→ retain as corpus/proof asset
~~~

### E-019 first slice

Use one small Purchase-intake workflow with approximately 5–10 real samples when available:
1. collect/preserve samples;
2. classify expected behaviour without inventing missing facts;
3. build proof matrix;
4. define one reusable procedure;
5. execute bounded implementation/proof;
6. issue proof receipts;
7. make one controlled relevant change;
8. calculate which receipts become invalid;
9. rerun only affected cases;
10. compare repeated work/traceability with duplicated per-case execution.

**PASS to consider upstreaming into ZASS System:**
- materially less duplicated procedure/retesting work;
- equal or better regression safety;
- clear lineage;
- no hidden skipped proofs;
- manageable governance overhead.

If those conditions are not met, keep D-049 local to Kerani and revise/reject the execution mechanism rather than changing shared ZASS.


## GOVERNMENT ASSISTANCE & IMPACT BRIDGE VALIDATION

**Experiment:** E-017  
**State:** PLANNED.

Validate one mock programme before any real agency integration:

~~~text
tenant history
→ potential match
→ programme requirements
→ show exact fields requested
→ user review/consent
→ evidence pack/export
→ sponsor-funded entitlement
→ outcome measurement
→ aggregate/approved programme report
~~~

Required checks:
1. agency/programme remains eligibility/approval Source of Truth;
2. sponsor funding never grants blanket tenant-data access;
3. unrelated chats/receipts/customers stay outside the programme dataset;
4. purpose and approved fields are auditable;
5. sponsored credits are separable from Free quota and user-paid Credit Pass;
6. descriptive outcome metrics do not become unsupported causal claims;
7. start with export/report/fixture; add agency API only after a real programme requires it.

## EVENT / VIRAL / PARTNER SCALE VALIDATION

**Experiment:** E-018  
**State:** PLANNED.

Run an event-neutral spike drill before treating MAHA 2027 or any large event as launch-ready.

Test:
- onboarding burst;
- WhatsApp shard capacity + waitlist;
- Telegram fallback;
- AI/OCR/storage/report quota pressure;
- selected V1 control-plane capacity;
- cost ceiling/alerts;
- truthful graceful degradation;
- OpenClaw reliability under load;
- partner activation threshold;
- partner handoff;
- rollback/exit with tenant continuity.

Partner acceptance requires:
- documented service/capacity boundary;
- measurable trigger for activation;
- secrets/access scope;
- tenant/data authority remains Kerani/user-governed;
- no business-logic rewrite for handoff;
- no mandatory tenant-history migration;
- exit/rollback path;
- verified permitted wording for any enterprise-client references.

## PUBLIC-SECTOR / EVENT COLLABORATION OPERATING BOUNDARY

Potential collaboration may create a legitimate exchange:

~~~text
Agency / programme receives
- measurable digital-adoption outcome
- programme evidence / aggregate impact
- local innovation case study where approved

Kerani receives
- target-user outreach
- field feedback
- possible official demo/shared-booth opportunity
- institutional programme access where approved
~~~

Do not operationalise this as a personal KPI-for-access exchange. Any booth, agency collaboration, endorsement, client-reference use or grant claim must have factual approval/evidence.

## GRANT EVIDENCE PACK — FUTURE

Do not submit an architecture claim as evidence of impact. A future grant/development evidence pack should be assembled from observed facts such as:
- active/retained businesses;
- completed useful records;
- time-to-first-value;
- reliability/uptime/error metrics;
- cost per useful action;
- Free/Premium or sponsored-capability usage;
- documented operational/user outcomes;
- programme outcomes with correct causality language;
- verified partner capacity/SLA;
- development/scale roadmap.

A specific grant remains optional external funding, never a product dependency.


## PREMIUM OPERATIONS PACK — CANDIDATE REVIEW

**Authority:** D-050 CANDIDATE only. Do not implement or market as LOCKED Premium entitlement yet.

Candidate pack:

~~~text
ALERT  → IoT/device event → contextual push/escalation
REMIND → Task/time/status → reminder/push
REPORT → scheduled report delivery
ASK    → richer interactive query/retrieval
~~~

Review path before LOCK:

1. Audit OpsMate for real behaviour evidence covering reminder, periodic report, query/retrieval and push/notification families.
2. Classify each mechanism as GENERIC / AGRO-GENERIC / OPSMATE-BSE-SPECIFIC / UNCERTAIN.
3. Preserve Free Core usefulness:
   - basic Task stays Free;
   - basic/manual report stays Free;
   - basic deterministic retrieval stays Free;
   - Premium candidacy focuses on automation, scheduling, richer context/intelligence and cross-channel convenience.
4. For **IoT Alert Bridge**, keep a non-negotiable safety boundary:
   - local/device/PLC/HA deterministic alarm path remains authoritative for critical conditions;
   - Kerani may add context, history, notification and escalation;
   - Kerani/LLM/cloud outage must not suppress the base critical alarm.
5. Define truthful delivery semantics for reminder/report/push: SENT / DELIVERED where verifiable / FAILED / RETRYING; never imply success without evidence.
6. Measure provider/channel/AI/storage cost before assigning Credit Pass values or quotas.
7. Test at least one reusable/non-BSE scenario before claiming the pack is generic.
8. Return to ZASS for owner review before D-050 can become LOCKED.

Exact schedule cadence, credit price, message allowance, IoT protocol, supported devices and escalation chain remain deferred.


## PREMIUM INTELLIGENCE PACK — CANDIDATE REVIEW

**Authority:** D-051 CANDIDATE only. Do not implement or market the full pack as a LOCKED Premium entitlement yet.

Candidate pack:

~~~text
STRUCTURED TENANT HISTORY
          ↓
ANALYSIS
CORRELATION
GRAPH
PROPOSAL
FORECAST
~~~

Review path before LOCK:

1. Select a small representative subset first; do not build all five merely because they are named.
2. Use real or evidence-backed structured tenant records where available.
3. Preserve the Free baseline:
   - basic summary remains Free;
   - basic/manual report remains Free;
   - basic deterministic retrieval remains Free.
4. For **Analysis**, define the user question, input data boundary and factual output contract.
5. For **Correlation**, label association as association; do not imply causation without supporting methodology.
6. For **Graph**, verify the chart faithfully represents underlying data and remains understandable to the target user.
7. For **Proposal**, expose material assumptions and separate generated advice from external/official approval.
8. For **Forecast**, record data horizon, inputs, uncertainty, failure/insufficient-data behaviour and provider/model cost.
9. Measure cost per useful completed capability, not raw token/API use alone.
10. Return to ZASS for owner review before D-051 can become LOCKED.

Exact Credit Pass values, included allowances, model/provider, chart/export format and domain-specific intelligence remain deferred.


---

## ZASSIMPLE planning findings

None added by the migration itself.

## PRE-ARCH evidence review

Not started under the ZASSIMPLE surface.

## Execution gates

Continue to use this canonical ZASSIMPLE plan while preserving existing LOCKED lineage. Escalate to Full ZASS only when materially stronger governance is required. Before detailed technical task slicing after PRE-ARCH, apply the Execution Reality Check and real artifact/sample + execution-surface mapping required by the current shared method baseline.
