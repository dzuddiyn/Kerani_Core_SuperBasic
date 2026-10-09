# ZASS — Kerani_Core_SuperBasic

**Full ZASS baseline:** v0.3.11  
**ZASS SYSTEM:** v0.2.2  
**Primary project method:** ZASSIMPLE v0.3.3  
**Project status:** DECIDING — evidence harvesting planned; substantive Core build parked  
**Owner:** Project Owner  
**Updated:** 2026-10-09  
**Repository:** dzuddiyn/Kerani_Core_SuperBasic  
**Retained governance / lineage file:** this file  
**Primary method baseline:** https://github.com/dzuddiyn/ZASS-Zero-to-Architecture-Structured-Sprint/blob/main/ZASSIMPLE/ZASSIMPLE_MY.md

> **Motto:** **Genericity is Generosity.**
>
> We earn genericity through evidence and reuse, then share the useful stack openly so small teams can build on proven work instead of rebuilding it alone.

This project now operates primarily under **ZASSIMPLE v0.3.3**, aligned with **ZASS SYSTEM v0.2.2**. Existing Full ZASS project records are retained as governance/evidence lineage and may be consulted or escalated into when stronger governance is materially required.

Current method principles:

1. **Lightweight di permukaan, lineage kuat sampai execution.**
2. **Present only the next meaningful human action.**
3. **DESIGN starts in ZASSIMPLE; Full ZASS is escalation capability, not the default burden.**
4. **Technical architecture is governed:** DESIGN → CHALLENGE → explicit owner PRE-ARCH lock.
5. **After PRE-ARCH:** run Execution Reality Check → real artifact/sample pack + execution-surface map → detailed ACTION PLAN ↔ PRE-ARCH → evidence-bounded vertical atomic tasks → result/proof → delta planning + PRE-ARCH review.
6. **Before final confirmation:** run the LAST DESIGN / ARCHITECTURE CHALLENGE; after confirmation rebuild the RELEASE ACTION PLAN and release task queue.

If project artifacts and the official method baseline differ, use:
- the retained project lineage for **existing project facts, LOCKED decisions, evidence and historical traceability**;
- `ZASSIMPLE/DESIGN.md`, `ZASSIMPLE/ACTION_PLAN.md`, and `ZASSIMPLE/TASKS.md` for the **current operating surface**;
- official **ZASS SYSTEM v0.2.2 / ZASSIMPLE v0.3.3 / Full ZASS v0.3.11** for current workflow/command semantics.

Only the project owner may make a decision **LOCKED**. A suggestion, AI output, model agreement, experiment PASS, or implementation detail is not automatically a decision.

---

# 0. AI OPERATING RULES

AI may:
- generate ideas and alternatives;
- challenge assumptions;
- identify risks;
- propose experiments;
- map OpsMate evidence;
- compare architecture candidates;
- propose candidate decisions;
- update this file when authorised.

AI may NOT:
- silently change a LOCKED decision;
- invent requirements or evidence;
- treat multi-model agreement as evidence;
- confuse implementation with contract;
- promote ACTION PLAN execution state into a decision;
- generate confirmed architecture while critical decisions remain unresolved;
- override the project owner.

Decision states:

**RAW → CANDIDATE → TESTING → DECIDED → LOCKED**

Other states:

**REJECTED · DEFERRED · SUPERSEDED**

Project execution state in `ZASSIMPLE/ACTION_PLAN.md` must use the ZASSIMPLE v0.3.3 execution/planning states and must not become a second decision ledger or architecture authority.

---

# 1. RAW IDEA

## Original Idea

After relevant OpsMate BSE behaviour and regression tests become stable, inspect the working implementation and extract only the parts that are genuinely reusable for small conversational applications:

**Telegram → Apps Script → AI → data/workspace → response**

The result must come from a tested system, not an imagined framework.

## Why I Want This

- Avoid rebuilding useful infrastructure for every future application.
- Preserve lessons already paid for through real OpsMate bugs, tests and operating experience.
- Separate reusable infrastructure from farm/BSE-specific logic.
- Create a small, understandable foundation that a single maintainer can own.
- Share a proven and safe stack openly when publication requirements are satisfied.

## Provenance

The statements above are inherited from the existing project SoT. They are project context, not new evidence created by this migration.

---

# 2. GOALS

1. Identify which OpsMate components are genuinely reusable.
2. Extract reusable behaviour without farm, BSE, plot, inventory, claim or SME assumptions.
3. Preserve proven behaviour through regression tests and explicit contracts.
4. Define a small configuration/extension contract.
5. Prove the core can run with a non-farm module.
6. Build one independent second application or module composition that demonstrates reuse.
7. Reproduce selected OpsMate behaviour using the new composition.
8. Publish the stack openly only when security, redaction, documentation and licensing are ready.
9. Keep future domain applications as consumers of the core rather than allowing them to silently redefine it.
10. Keep the SuperBasic core useful for micro-SME operations through five generic record families: **Purchase, Sale, Inventory, Observation and Task**, with receipt capture as an input capability.
11. Demonstrate the generic core across exactly three planned domain modules: **Agro, Servis Teknikal, and Makanan & Tempahan**.
12. Keep full natural-language conversation outside SuperBasic as a premium Kerani AI capability so basic operation does not depend on premium model usage.
13. Support **minimum constrained natural-language intake** in SuperBasic so users can type ordinary short operational sentences while preserving deterministic validation and human authority before any authoritative record is written.
14. Keep the free Core genuinely useful on its own: basic receipt capture, purchase/sale/inventory records, operational observations/notes, tasks, basic retrieval/reporting and summary of operational logs.
15. Monetise higher-value intelligence and domain automation through explicit Credit Pass / pay-per-capability rather than making a recurring subscription the primary access model.
16. Keep user business/operational data portable; paid value comes from convenience, domain intelligence, automation, traceability and ready-formatted outputs rather than artificial data lock-in.
17. Position SuperBasic for broad micro-SME adoption through a **free-but-genuinely-useful** product experience, then use pilot evidence/testimonials to support growth while keeping the free/premium boundary explicit.

---

# 3. NON-GOALS

- Building Kerani Core SME in this repository.
- Replacing or redesigning OpsMate while the relevant behaviour is still unstable.
- Building a farm-management system inside the generic core.
- Treating BSE configuration as the generic schema.
- Home Assistant, local LLM, workstation, remote-desktop or hardware work.
- A fully autonomous agent with unrestricted access to business systems.
- A broad platform designed from speculation.
- Additional domain modules beyond **Agro, Servis Teknikal, and Makanan & Tempahan** within the current SuperBasic scope.
- Full premium natural-language conversation as a mandatory SuperBasic capability; constrained natural-language intake for intent suggestion and candidate extraction remains in scope.
- Requiring a dedicated self-hosted server for the SuperBasic baseline.
- Locking a final architecture before extraction evidence exists.
- Artificially restricting export/access to user data in order to force purchase of premium intelligence.
- Making recurring subscription the primary monetisation requirement for current SuperBasic scope.

---

# 4. CONSTRAINTS

## Budget / Operating Model

- Prefer a small, maintainable stack suitable for a single maintainer.
- Avoid abstraction that is not justified by at least two demonstrated uses.
- Control paid AI/API-credit usage; ordinary SuperBasic record operations must not require premium conversational processing.
- Minimum natural-language intake should use the smallest practical model/prompt path and must fall back to clarification rather than consume extra reasoning to guess intent.
- Keep the Apps Script implementation modular enough that new domain behaviour does not collapse into special-case branching or spaghetti code.
- Free/basic capability and metered/premium capability must be distinguishable by capability/entitlement policy rather than scattered feature-specific conditionals.
- Premium capability must disclose its credit cost before execution when a charge applies.
- Failed provider/system execution must not be treated as a successfully consumed paid service.
- Free transport, storage/media, AI/processing, retrieval/report fair-use and Premium Credit Pass are separate controls.
- Telegram removes most WhatsApp transport pressure but does not remove storage, AI/processing, retrieval/report fair-use or abuse limits.
- Provider quotas/prices are configurable inputs, not architecture constants.

## Initial Runtime

- Google Apps Script.
- The SuperBasic baseline does not require a dedicated self-hosted server.

## Initial Customer Channels

- **Shared WhatsApp** = convenience/discovery Free channel with controlled capacity.
- **Telegram** = economic/high-usage Free channel.
- Both resolve to the same tenant identity; channel is not the business Source of Truth.
- Per-number seats and message allowances are configurable operational parameters.

## Initial AI Provider

- Gemini API.

These are initial implementation constraints, not proof that the final reusable contract must remain provider- or channel-specific.

## Security / Privacy

- Secrets must remain outside source control and public examples.
- TEST and production behaviour/data must remain isolated.
- A coding agent must not receive direct production Telegram credentials or unrestricted production-message access.
- Human/operator controls TEST injection and live deployment boundaries.
- Open-source publication requires security review, redacted examples and an explicit licence.

## Domain Boundary

- Domain logic belongs in an application/module layer, not silently inside the generic core.
- The planned domain-module set is intentionally limited to **Agro**, **Servis Teknikal**, and **Makanan & Tempahan**.
- **Agro** covers agriculture broadly, including crops/planting, aquaculture/fish and livestock/poultry; it replaces the narrower project term “Kebun” for the reusable domain layer.
- **Servis Teknikal** covers small technical-service operations such as workshop/repair, domestic electrical wiring, computers, air-conditioning and similar technician jobs.
- **Makanan & Tempahan** covers food stalls/warung/burger operations together with small bakery, made-to-order food and small catering.
- Additional modules are outside the current SuperBasic scope unless the owner later creates a new explicit decision.
- Natural-language interpretation may suggest routing into Core or a domain module, but the target module's deterministic guard/validator remains authoritative for fields and business rules.

## Evidence Constraint

- Genericity must be demonstrated through stable behaviour, extraction and reuse.
- No component becomes generic merely because it sounds reusable.
- OpsMate remains the primary reference implementation for harvesting reusable mechanisms and Agro-domain operational lessons.
- BSE/OpsMate-specific assumptions must not be promoted into the generic Core merely because they are already implemented.

## Near-Term Execution Constraint — October 2026

- Target **10 October 2026** to freeze a stable OpsMate reference baseline for extraction evidence.
- Pilot observations after the freeze should be captured as bug, gap and requirement evidence; they do not automatically reopen or expand the frozen reference scope.
- From **10–15 October 2026**, the priority for this repository is evidence harvesting and minimal skeleton preparation, not substantive Core implementation.
- The evidence-harvesting window should maximise learning from the frozen OpsMate reference through behaviour maps, pilot findings, reuse classification and candidate contracts.
- After the 15 October review, substantive Kerani_Core_SuperBasic implementation is **PARKED** until the owner explicitly restarts the build with suitable local agentic-coding resources.
- Critical safety, integrity or reference-invalidating defects may justify revisiting the freeze; ordinary pilot improvements should remain recorded evidence rather than causing uncontrolled scope churn.

---

# 5. IDEA BLAST

Nothing in this section is automatically approved.

| ID | Idea | Source | Status |
|---|---|---|---|
| I-001 | Extract a small generic conversational-app foundation from proven OpsMate behaviour. | Existing project SoT | RAW |
| I-002 | Separate generic core behaviour from agriculture-domain behaviour and BSE configuration. | Existing project SoT | RAW |
| I-003 | Use a tiny non-farm module as a proof that Core SuperBasic is genuinely generic. | Existing project SoT | RAW |
| I-004 | Publish the proven stack openly after security, redaction, documentation and licensing review. | Existing project SoT | RAW |
| I-005 | Make the free-product promise simple: **record → retrieve → summarize → own your data**; AI should stay mostly behind the experience rather than becoming the product identity. | Product discussion 2026-10-06 | CANDIDATE |
| I-006 | Treat product value as three layers: **SuperBasic Free → Domain Module → Intelligence/Credit**, rather than only Free vs Premium. | Product discussion 2026-10-06 | CANDIDATE |
| I-007 | Build **data history first, intelligence later**: let free usage accumulate useful structured history so later forecasting/domain intelligence becomes more valuable naturally. | Product discussion 2026-10-06 | CANDIDATE |
| I-008 | Explore user-owned/portable storage and an **Export for AI** path so advanced users can analyse their own Kerani data elsewhere without weakening Kerani's value as the operational system of record. | Product discussion 2026-10-06 | CANDIDATE |
| I-009 | Meter premium by useful outcome/capability rather than exposing underlying AI token/provider economics to users. | Product discussion 2026-10-06 | CANDIDATE |
| I-010 | Prove monetisation first with only a few premium killer capabilities per module instead of building a large premium catalogue early. | Product discussion 2026-10-06 | CANDIDATE |
| I-011 | Position Kerani as a lightweight digital-upgrade path for micro-SMEs that currently rely on memory, chat, receipts, notebooks and occasional spreadsheets. | Product discussion 2026-10-06 | CANDIDATE |
| I-012 | Product thesis candidate: **take the discipline of larger-company systems and make it light enough for small businesses.** | Product discussion 2026-10-06 | CANDIDATE |
| I-013 | Give Free users a very small Kerani-hosted OCR allowance, then preserve free receipt recording through manual entry or user-assisted OCR (personal Gemini/Lens to pasted text). | Product/cost discussion 2026-10-07 | CANDIDATE |
| I-014 | V1 central-control-plane candidate: Cloud Run + Firestore + Secret Manager + basic Cloud Logging/Monitoring, while Apps Script remains useful for Google Workspace/customer-edge integration. | Infrastructure discussion 2026-10-07 | CANDIDATE |
| I-015 | Premium Operations Pack candidate: **Alert · Remind · Report · Ask** — IoT alert bridge, task reminder/push, scheduled report, and richer interactive query/retrieval. | Product/extraction discussion 2026-10-09 | CANDIDATE |
| I-016 | Premium Intelligence Pack candidate: **Analysis · Correlation · Graph · Proposal · Forecast** over the tenant's structured history, with capability pricing/credit use derived from measured cost and user value. | Product discussion 2026-10-09 | CANDIDATE |

---

# 6. QUESTIONS / UNKNOWNS

| ID | Question | Why It Matters | Status |
|---|---|---|---|
| Q-001 | Which OpsMate files/functions implement genuinely reusable behaviour? | Defines extraction scope. | OPEN |
| Q-002 | What configuration contract can express a new application without editing core code? | Tests whether reuse is real. | OPEN |
| Q-003 | Which storage abstractions are necessary and which are over-abstraction? | Prevents speculative framework design. | OPEN |
| Q-004 | Which parts should intentionally remain Apps-Script-specific in v0.x? | Controls scope and portability claims. | OPEN |
| Q-005 | How should prompts, schemas and validation be separated from runtime core behaviour? | Protects provider/domain boundaries. | OPEN |
| Q-006 | What is the smallest meaningful second application for proof of reuse? | Required to earn genericity. | OPEN |
| Q-007 | What must be redacted or redesigned before public release? | Protects security and privacy. | OPEN |
| Q-008 | Does this repository deserve a permanent public name after reuse is demonstrated? | Naming must follow demonstrated function. | OPEN |
| Q-009 | Can a module be removed without damaging Core? | Tests module independence. | OPEN |
| Q-010 | Can Core run a non-agricultural module? | Tests genericity. | OPEN |
| Q-011 | Can Telegram be replaced without changing business logic? | Tests channel boundary. | OPEN |
| Q-012 | Can BSE configuration be replaced by another client/farm configuration? | Tests configuration/domain separation. | OPEN |
| Q-013 | Can parser or AI provider change behind the same behaviour contract? | Tests model/provider portability. | OPEN |
| Q-014 | Are raw messages, candidate records and authoritative records clearly distinct? | Protects auditability and state correctness. | OPEN — early positive evidence from E-001A/E-001B |
| Q-015 | Which layer owns routing between direct/read requests and stateful/mutation workflows? | Prevents transport, runtime and domain routing responsibilities from collapsing into one layer. | OPEN |
| Q-016 | Which classes of request require a Durable Inbox, and which should bypass it? | Prevents forcing every request through durable queue infrastructure. | OPEN |
| Q-017 | Is human confirmation a mandatory Core responsibility, an optional Core capability, or application/module policy? | Prevents approval workflow from being over-generalised into Core. | OPEN |
| Q-018 | What storage/media quota keeps Free useful without uncontrolled receipt/image cost? | Calibrates Free usefulness/economics. | OPEN — pilot parameter |
| Q-019 | What AI/processing and report/retrieval fair-use limits prevent heavy Free abuse? | Protects shared capacity. | OPEN — pilot parameter |
| Q-020 | What active-user capacity should one shared WhatsApp number carry before waitlist? | Protects time-to-value. | OPEN — 50 is an example, not locked |
| Q-021 | What signal should trigger a new shared WhatsApp number and waitlist invitation? | Viral operations. | OPEN |
| Q-022 | What synthetic audit cadence gives reliability evidence without distorting real capacity? | Reliability-agent envelope. | OPEN |
| Q-023 | What monthly Kerani-hosted OCR allowance is enough to demonstrate value without uncontrolled variable cost? | Determines Free OCR economics. | OPEN — 1–3/month is a candidate range only |
| Q-024 | Can pasted text from personal Gemini/Lens reliably enter the same candidate → confirm/correct → validate → authoritative-save flow as hosted OCR? | Preserves Free receipt capability after OCR quota. | OPEN |
| Q-025 | Does Cloud Run + Firestore + Secret Manager + basic Monitoring materially simplify V1 central multi-tenant control versus central Apps Script without unnecessary complexity? | Chooses the V1 control-plane implementation. | OPEN |
| Q-026 | What minimum programme-data contract can support assistance matching/evidence without exposing unrelated tenant data? | Defines Government Program Bridge boundary. | OPEN |
| Q-027 | What entitlement/ledger model lets sponsor-funded credits coexist cleanly with Free quota and user-paid Credit Pass? | Prevents funding source from leaking into capability semantics. | OPEN |
| Q-028 | What tested load/cost/reliability envelope qualifies Kerani as ready for a large event or sudden viral spike? | Defines event-readiness gate. | OPEN |
| Q-029 | What measurable threshold should activate an infrastructure partner or dedicated scale tier? | Prevents both premature spend and emergency-only escalation. | OPEN |
| Q-030 | What evidence and permissions are required before citing a partner's enterprise client history or applying for a specific development grant? | Protects credibility and grant claims. | OPEN |
| Q-031 | Where should the Free/Premium boundary sit for reminder/push, scheduled reports and interactive retrieval, and which OpsMate behaviours are genuinely reusable? | Prevents useful Free basics from being crippled while avoiding unbounded automation/AI cost. | OPEN |
| Q-032 | Can Cloudflare Workers + D1 satisfy the V1 webhook/router, tenant/quota/waitlist, scheduled-trigger and lightweight async needs more cheaply/simply than Cloud Run or central Apps Script? | Determines whether a lower-entry-cost control plane can meet Kerani's locked boundaries. | OPEN |

---

# 7. RISKS & FAILURE SCENARIOS

| ID | Failure / Risk | Impact | Possible Mitigation | Status | 🚨 Early warning signal |
|---|---|---|---|---|---|
| R-001 | Premature abstraction | Core becomes speculative and difficult to maintain. | Extract only after stable OpsMate evidence. | OPEN | Interfaces appear before a second demonstrated use. |
| R-002 | Hidden OpsMate assumptions | Generic core fails outside BSE/OpsMate. | Behaviour map + reuse ledger + regression tests. | OPEN | BSE vocabulary or sheet-column assumptions appear in core contracts. |
| R-003 | Core becomes Kerani Core-specific | Reuse claim becomes false. | Keep domain code/config in consumer modules. | OPEN | Core requires agriculture concepts to run. |
| R-004 | Over-engineering | Cost and complexity exceed value. | Prefer smallest interface demonstrated by two uses. | OPEN | New abstractions exist with no evidence-backed consumer. |
| R-005 | Regression during extraction | Proven behaviour is lost. | Preserve/port relevant harness tests before refactor. | OPEN | New composition cannot reproduce a selected baseline test. |
| R-006 | Secret or private-data exposure | Unsafe public release. | No secret commits; redacted fixtures; publication review. | OPEN | Real token, chat ID or operational record appears in repo fixtures. |
| R-007 | Public stack is confusing or unsafe | Users deploy incorrect defaults or misunderstand scope. | Clear scope, examples, threat notes and versioning. | OPEN | Documentation implies production safety that has not been tested. |
| R-008 | Architectural drift | Implementation silently overrides project decisions. | This ZASS file remains authoritative; use change control. | OPEN | Code or docs contradict an L-xxx record. |
| R-009 | Linear pipeline over-generalisation | Read/query requests are forced through queue, AI or human approval even when unnecessary. | Classify request behaviour before selecting an execution path; test direct/read and stateful/mutation paths separately. | OPEN | Commands such as report/history/lookup/status begin requiring LLM or approval without evidence that they need it. |
| R-010 | Overconfident natural-language routing | AI guesses an intent/category or fields and causes the wrong record type or wrong business meaning to reach persistence. | AI may only suggest intent/candidate; low/ambiguous confidence must trigger clarification; require human confirmation and deterministic domain validation before authoritative write. | OPEN | Ambiguous free text is silently converted into a saved record or a domain writer receives unconfirmed/unvalidated AI output. |
| R-011 | Free/premium boundary becomes manipulative or confusing | Free product feels crippled, users do not trust feature gates, or growth messaging over-promises business outcomes. | Keep Free Core independently useful; explain premium value/cost explicitly; validate messaging with pilot users/testimonials; avoid guaranteed-outcome claims. | OPEN | Basic record/retrieval workflows become paywalled, premium prompts appear before value is demonstrated, or marketing implies guaranteed grants/certification/financing. |
| R-012 | Free onboarding friction | Setup kills first-value experience. | Shared hosted Free first; owned infra later. | OPEN | API keys/OAuth needed before first record. |
| R-013 | Heavy Free tenant exhausts shared AI/storage/report capacity | Other users degrade. | Per-tenant limits + rate/fair-use controls. | OPEN | Few tenants dominate usage. |
| R-014 | Tenant isolation failure | Cross-customer data exposure. | Tenant-scoped storage/auth + isolation tests. | OPEN | Binding can access another tenant. |
| R-015 | Shared WhatsApp overcrowding | Free becomes nearly useless before habit forms. | Active-seat cap + waitlist + new-number provisioning. | OPEN | Only a few completed records fit per user. |
| R-016 | Channel migration duplicates/orphans history | Data continuity breaks. | Permanent tenant identity; channel binding only. | OPEN | Migration requires data copy. |
| R-017 | Waitlist growth invisible to owner | Viral demand is lost. | Queue metrics + owner notification. | OPEN | Full-capacity replies without owner alert. |
| R-018 | Synthetic audit contaminates real truth | Test data leaks into customer reports. | Synthetic tenants/tagging + normal authority path. | OPEN | Test records appear as customer truth. |
| R-019 | Central shared runtime bottleneck | Viral growth overloads Apps Script/AI/storage. | Metering + replaceable runtime/provider boundaries. | OPEN | Latency tracks tenant count. |
| R-020 | Hosted OCR subsidy becomes a cost sink | Free users repeatedly scan receipts and consume OCR/storage without conversion or useful retained records. | Tiny monthly hosted-OCR allowance, one-pass/cache where possible, DIY OCR/manual fallback, per-tenant metering. | OPEN | OCR usage grows much faster than completed useful records. |
| R-021 | DIY OCR fallback bypasses record integrity | Pasted external OCR text is trusted as authoritative data. | Treat pasted OCR text as untrusted input; run normal candidate/confirmation/deterministic validation flow. | OPEN | External OCR text is saved directly without review. |
| R-022 | Premature Cloud complexity | V1 gains operational burden before scale needs it. | Keep one small Cloud Run service + Firestore + Secret Manager + basic logs/alerts only; benchmark against Apps Script alternative. | OPEN | Multiple services/queues/databases appear before measured need. |
| R-023 | Sponsor/data-authority conflation | Funding arrangement becomes de facto access to private tenant data. | Separate sponsor entitlement from data contract; purpose-bound consent + minimum fields. | OPEN | Sponsor requests broad/raw database access. |
| R-024 | False government/partner endorsement | Kerani overstates institutional or enterprise backing. | Cite only verified approved relationships; distinguish partner capability from client endorsement. | OPEN | Marketing wording implies an unapproved endorsement. |
| R-025 | Partner lock-in | Emergency scale partner becomes permanent architecture dependency. | Portable Core/contracts/data + replaceable provider boundary + exit path. | OPEN | Migration requires rewriting business logic or moving tenant identity. |
| R-026 | Viral cost/load shock | Sudden event traffic creates uncontrolled API spend, latency or data loss. | Load gate, cost ceiling, throttling/backpressure, waitlist/fallback, observability. | OPEN | Variable cost or latency rises non-linearly with signups. |
| R-027 | Event-driven roadmap distortion | MAHA or another event forces premature features/architecture. | Treat event as candidate milestone; readiness gates remain authoritative. | OPEN | Scope changes are justified only by event date. |
| R-028 | Grant-dependency distortion | Product decisions optimize for grant criteria instead of user value. | 4V Value-first principle; architecture viable without specific grant. | OPEN | Roadmap stalls or breaks if grant is unavailable. |
| R-029 | Unsupported impact causality | Programme reporting overclaims that funding caused observed outcomes. | Separate descriptive outcomes from causal evidence/methodology. | OPEN | Before/after delta is presented as proof of causation. |
| R-030 | Safety-critical IoT alert depends on Kerani/LLM/cloud | A Kerani/provider outage could suppress a real-world safety alarm. | Keep deterministic/local device/PLC/HA alarm path authoritative; Kerani adds context, push, history and escalation only. | OPEN | Safety response is unavailable when Kerani, AI or internet is unavailable. |
| R-031 | Free-tier control-plane ceiling becomes hidden dependency | A pilot works cheaply, then hits provider limits or reset windows unexpectedly during growth. | Meter usage, test exhaustion/fallback, keep provider boundary portable, and define upgrade/partner trigger before public scale. | OPEN | Request/database/queue limits are approached without alerting or a paid/alternate path. |

---

# 8. METHOD REVIEWS

## MR-001 — Evidence-led extraction review

**Method:** First principles + Maintainability + Minimal viable experiment  
**Scope:** OpsMate BSE → Kerani_Core_SuperBasic extraction strategy  
**Reviewer / Model:** AI-assisted project review  
**Date:** 2026-09-29

### Findings

- OpsMate should be treated as a **reference implementation and evidence source**, not as an architecture template.
- Audit should begin from observable behaviour, not source-file names.
- Behaviour contracts should be defined before implementation is copied.
- Generic infrastructure, agriculture-domain behaviour and BSE-specific configuration need separate classifications.
- A non-farm module is a stronger genericity test than renaming farm concepts.
- Equivalent tested behaviour is more important than identical source code.

### Contradictions

- The previous Section 16 used several **AC-xxx** IDs for process/evidence proposals, while ZASS v0.3.2 reserves **AC-xxx** for Architecture Candidates. This migration preserves traceability but moves the canonical records to D/E entries where appropriate.

### New Questions

- Q-009 through Q-014.

### New Risks

- Existing risks R-001 through R-008 are retained; no additional risk is promoted solely by this migration.

### Experiments Suggested

- E-001 through E-006.

### Candidate Decisions

- D-006 through D-009.

---

# 9. MULTI-AI REVIEW RULES

Agreement between AI models is not evidence.

Disagreement must be converted into a question, experiment, trade-off or candidate decision.

No significant multi-AI disagreement is currently recorded in this project SoT.

| ID | Topic | Model / Reviewer Views | What Must Be Resolved | Result |
|---|---|---|---|---|
| MA-001 | — | — | — | OPEN / unused |

---

# 10. OPTIONS

## Decision Topic — How to derive the reusable core

### Option A — Evidence-led extraction

**Description:** Freeze proven OpsMate behaviour, map observable workflows, classify reuse, define contracts, then implement and test a clean composition.

**Advantages:**
- grounded in working behaviour;
- preserves regression evidence;
- reduces hidden BSE assumptions;
- supports model/provider independence.

**Disadvantages:**
- slower than copying source directly;
- requires careful baseline and behaviour mapping.

**Risks:**
- can still over-generalise if evidence is weak.

**Evidence:**
- strategy review and existing OpsMate regression practice; full extraction proof is still pending.

### Option B — Direct refactor / rename of OpsMate

**Description:** Refactor the existing OpsMate structure directly into a reusable core.

**Advantages:**
- superficially faster;
- reuses existing source layout.

**Disadvantages:**
- likely carries hidden domain and implementation coupling;
- can mistake current Apps Script structure for intended architecture.

**Risks:**
- produces “OpsMate without BSE” rather than a genuinely reusable core.

**Decision state:** No new owner decision is created by this comparison. D-002 already locks the principle that genericity must be earned through extraction and reuse.

---

# 11. ARCHITECTURE CANDIDATES

Create AC entries only for genuine architecture arrangements.

## AC-005 — Candidate runtime/module boundary

**Status:** CANDIDATE  
**Origin:** legacy Section 16.6; retained as AC because it is an actual architecture boundary candidate.

**Summary:**

Evidence now suggests that the runtime/module boundary may require more than one interaction path rather than one universal linear pipeline:

~~~text
Channel Adapter
      ↓
Request Router
      │
      ├── Direct / Read Path
      │       ↓
      │   controlled handler
      │
      └── Stateful / Mutation Path
              ↓
         Durable Inbox
              ↓
          Core Pipeline
              ↓
        Module Contract
              ↓
         Domain Module
~~~

**Key characteristics:**
- channel boundary before business logic;
- constrained free-text mutation requests may pass through an intent-suggestion/candidate stage before module dispatch, but D-015 does not by itself LOCK where that router is implemented;
- request routing is explicit and its ownership remains unresolved (Q-015);
- Durable Inbox appears relevant to stateful/mutation workflows but is not yet proven as universal (Q-016);
- Core performs generic orchestration;
- domain behaviour is supplied through a module contract;
- human confirmation may be mandatory, optional, or application/module policy and remains unresolved (Q-017);
- BSE becomes configuration/test data rather than the generic schema.

**Candidate Core responsibilities:**
- normalise;
- route;
- validate generic state/contract rules;
- dispatch modules;
- manage generic approval states where applicable;
- emit audit/events;
- produce safe responses.

**Dependencies:**
- behaviour evidence from OpsMate;
- contract definitions;
- a non-farm module test;
- storage/durable-inbox evidence.

**Advantages:**
- separates channel, runtime, core and domain concerns;
- supports testing genericity independently.

**Trade-offs:**
- Request routing may itself become over-generalised if ownership is assigned too early.
- Durable Inbox and approval semantics may be over-generalised and remain unproven.

**Critical risks:**
- R-001, R-002, R-003, R-004, R-009.

### Candidate Comparison

No second genuine architecture candidate has yet been recorded. Do not invent AC-002/AC-003 merely to fill a comparison table.

---

## AC-006 — Tenant-centric Hosted-Free → Owned-Premium architecture

**Status:** CANDIDATE**

~~~text
Channel (WA / Telegram / future)
              ↓
         TENANT IDENTITY
              ↓
   ┌──────────┼──────────┐
   ↓          ↓          ↓
Control     Data      Execution/AI
credits     tenant    shared Free
quotas      history   or owned Premium
entitlement export
~~~

Free uses shared infrastructure with tenant isolation. Premium may move to dedicated/owned WhatsApp, Google/Apps Script Edge and optional customer-owned AI without changing tenant identity. POS/ERP integration later uses adapters/contracts; ERP remains authoritative for ERP-owned records.

Non-constant parameters: WA seat limit, message allowance, storage quota, AI/processing quota, report fair-use, provider/model and onboarding price.

---


## AC-007 — V1 central control-plane implementation candidate

**Status:** CANDIDATE

~~~text
WhatsApp / Telegram
        ↓
     Cloud Run
  central API/router
        │
   ┌────┼──────────────┐
   ↓    ↓              ↓
Firestore        Secret Manager    Logging/Monitoring
tenant/quota     credentials       health/cost signals
waitlist
        │
        ↓
Apps Script / Drive / AI / customer-edge integrations
~~~

**Intent:** Use Cloud Run as the central multi-tenant control/API plane, Firestore for compact operational state, Secret Manager for platform credentials, and basic Logging/Monitoring for reliability. Keep Apps Script as a lightweight Google Workspace/customer-edge tool rather than forcing it to be the entire central SaaS runtime.

**Why candidate, not LOCKED:** Current Google Cloud economics and scaling characteristics look suitable for low-traffic V1, but Kerani workload, cost-per-use and operational complexity have not yet been benchmarked against the simpler central-Apps-Script alternative.

**V1 anti-overengineering rule:** no Kubernetes, no large microservice split, no BigQuery dependency, no Agent Platform dependency, and no speculative queue/cache layer unless evidence requires it.

---


## AC-008 — Sponsor-Funded Assistance & Outcome Bridge

**Status:** CANDIDATE

~~~text
Tenant Records
      ↓
Assistance Matcher
      ↓
User Review / Consent
      ↓
Programme Adapter
   ┌──────┼──────────┐
   ↓      ↓          ↓
Evidence Sponsor   Outcome
Pack     Credits   Report
   └──────┼──────────┘
          ↓
        Agency
~~~

**Intent:** Let Kerani help micro-SMEs/agro operators discover potentially relevant assistance programmes, prepare evidence from their own structured history, receive sponsored capability/credits where available, and produce consented programme outcome reporting.

**Authority boundary:** Kerani is a matching/evidence/reporting layer. The programme/agency remains authoritative for eligibility, approval, funding and official programme status.

**Data boundary:** Sponsor payment does not create blanket access to tenant data. Programme sharing must be purpose-bound, minimum-necessary and user-authorised; aggregation/anonymisation is preferred where individual data is unnecessary.

**Integration direction:** Start with export/report/fixture formats. Agency-specific APIs are deferred until a real programme requires them.

---

## AC-009 — Pilot → Viral Launch → Partner-Backed Scale

**Status:** CANDIDATE

~~~text
Operational Pilot
      ↓
Proof / Regression Evidence
      ↓
SuperBasic V1
      ↓
Just-Enough Scalable Infrastructure
      ↓
Load / Reliability / Cost Gates
      ↓
Large-Event / Viral Readiness
      ↓
Distribution / Public-Sector Partner
      +
Strategic Infrastructure Partner
      ↓
Measured Adoption + Reliability
      ↓
Grant / Development Evidence Pack
      ↓
Further Scale
~~~

**Intent:** Grow from evidence rather than speculative infrastructure spend. Pilot proves value and behaviour; V1 stays cheap at low usage; load/reliability controls prepare for sudden demand; official distribution and replaceable infrastructure partnerships may accelerate scale without surrendering Kerani product/data authority.

**Named-event/vendor boundary:** MAHA 2027, any specific Jabatan, any specific software/infrastructure vendor, Petronas-related credentials and any grant programme remain candidate/deferred counterpart details until independently verified and formally available.

**Partner boundary:** Partner capacity may strengthen operational credibility, but Kerani must remain portable and must not imply that a partner's client endorses Kerani.

---


## AC-010 — Cloudflare-First Lightweight Control Plane

**Status:** CANDIDATE  
**Origin:** cost/hosting review 2026-10-09

~~~text
WhatsApp / Telegram / future channel
                ↓
        Cloudflare Worker
        API / Router / Control
                │
      ┌─────────┼───────────┐
      ↓         ↓           ↓
      D1      Queue/Cron   external services
 tenant/quota  async/time   AI / Apps Script /
 waitlist      work         Drive / customer edge
~~~

**Intent:** Test a low-entry-cost serverless control plane using Cloudflare Workers with D1 for compact tenant/quota/waitlist state, plus scheduled/async facilities only where evidence requires them. Apps Script may remain a Google Workspace/customer-edge integration surface.

**Why candidate, not LOCKED:** Kerani has not yet benchmarked webhook behaviour, state access, concurrency, queue/schedule semantics, observability, security, failure recovery, migration or real workload cost on this stack.

**Cost constraint:** The owner currently encounters an approximately RM200 Google Cloud billing/onboarding barrier in their own account context. Treat this as a practical user-side constraint, **not** as a universal Cloud Run fee. Provider pricing/free-tier terms remain externally changeable and must be reverified before implementation.

**OpenClaw boundary:** OpenClaw remains the replaceable reliability/synthetic-agent layer under D-032/E-013, not the production control-plane authority. Self-hosted or rented-server OpenClaw may be used for reliability execution later, but does not replace the V1 control-plane benchmark.

**Anti-lock-in rule:** Cloudflare-specific storage/scheduling semantics must stay behind stable Kerani contracts so moving to Cloud Run, another provider or customer-owned infrastructure does not require rewriting business logic or migrating tenant identity.

---

# 12. DECISION LEDGER

## D-001 — Repository purpose

**Status:** LOCKED

**Problem:** Prevent reusable infrastructure work from becoming mixed with the Kerani Core SME product domain.

**Options considered:** Generic extraction repository / Kerani Core SME repository.

**Decision:** This repository is an OpsMate-derived generic-core extraction, not Kerani Core SME.

**Reason:** Separate reusable infrastructure from the SME product domain.

**Trade-offs:** Requires later integration with domain modules rather than embedding them here.

**Evidence / experiment:** Existing project scope and owner-approved SoT.

**Related risks:** R-002, R-003.

---

## D-002 — Genericity principle

**Status:** LOCKED

**Decision:** Genericity is earned through extraction and reuse, not assumed during design.

**Reason:** Prevent speculative abstraction.

**Consequences:** UNCERTAIN behaviour remains in the reference implementation until evidence supports extraction.

**Revisit trigger:** Only owner-approved evidence showing this principle blocks necessary, demonstrated reuse.

---

## D-003 — Guiding motto

**Status:** LOCKED

**Decision:** The guiding motto is **“Genericity is Generosity.”**

**Reason:** A proven, safe stack should be shareable for others to build upon.

**Consequences:** Openness is a goal, not permission to broaden the core without evidence.

---

## D-004 — Public-release gate

**Status:** LOCKED

**Decision:** Public release happens only after security review, redaction, documentation and explicit licence.

**Reason:** Openness must not expose secrets, operational data or unsafe defaults.

**Related risks:** R-006, R-007.

---

## D-005 — Permanent project name

**Status:** DEFERRED

**Decision:** PENDING.

**Decision drivers:** Demonstrated function and reuse.

**Options considered:** Keep temporary name / rename after proof.

**Revisit trigger:** Reuse proof stage passes.

---

## D-006 — Freeze a reference baseline before extraction

**Status:** CANDIDATE  
**Migrated from:** legacy AC-001.

**Problem:** Later extraction needs a stable comparison point.

**Candidate decision:** Freeze a clean OpsMate checkpoint with tested workflows, regression tests, redacted sample inputs, expected outputs and known limitations before extracting relevant behaviour.

**Evidence / experiment:** E-001 and actual OpsMate regression evidence required.

**Decision:** PENDING.

---

## D-007 — Behaviour-first audit

**Status:** TESTING  
**Migrated from:** legacy AC-002.

**Candidate decision:** Audit observable workflows first, then locate the implementation that performs each stage.

**Reason:** Avoid copying Apps Script/BSE structure as architecture.

**Evidence / experiment:** E-001A mapped the Input Usage / Inventory workflow from observable behaviour to implementation locations using an OpsMate TEST snapshot. E-001B then verified the actual worker runtime and corrected the map where it had mistaken a regression parser for the primary runtime parser.

**Decision:** PENDING.

---

## D-008 — Four-way reuse classification

**Status:** TESTING  
**Migrated from:** legacy AC-003.

**Candidate decision:** Classify extraction findings as **GENERIC**, **AGRO-GENERIC**, **OPSMATE/BSE-SPECIFIC**, or **UNCERTAIN**.

**Reason:** Preserve a domain layer between generic core and client-specific configuration.

**Evidence / experiment:** E-001A showed that the four-way classification is useful when applied to behaviour-level stages; one source file can contain mixed generic, domain and BSE-specific concerns. E-001B reinforced that classification should target responsibilities such as extract → guard → validate rather than assuming a particular parser implementation is generic.

**Decision:** PENDING.

---

## D-009 — Contract before source code

**Status:** TESTING  
**Migrated from:** legacy AC-004.

**Candidate decision:** Define minimum input/output/state promises before copying implementation.

**Reason:** Behaviour contracts should survive changes in regex, deterministic parser, Gemini, GPT or future local models.

**Evidence / experiment:** E-001A exposed a candidate request → candidate → human decision → authoritative TEST domain result → response/event contract without requiring the current Apps Script implementation to become the contract. E-001B strengthened this by separating AI extraction, deterministic guard and domain validation as distinct responsibilities.

**Decision:** PENDING.

---

## D-010 — SuperBasic core product scope

**Status:** LOCKED  
**Owner approval:** 2026-10-01

**Decision:** Kerani_Core_SuperBasic is a deliberately small generic micro-SME core centred on **Purchase, Sale, Inventory, Observation and Task** records. Receipt scanning/capture is an input capability that produces a reviewable structured record; it is not a separate business domain.

**Operating boundary:** The baseline must remain useful without a dedicated self-hosted server and without premium natural-language processing.

**Reason:** Keep the core small, understandable, low-cost and broadly useful across micro-SME operations.

**Consequences:** Domain-specific schemas and workflows belong in modules; premium conversational AI must not become a dependency of basic record keeping.

---

## D-011 — Planned domain-module set

**Status:** LOCKED  
**Owner approval:** 2026-10-01

**Decision:** The current SuperBasic product scope contains exactly three planned domain modules:

1. **Agro** — crops/planting, aquaculture/fish, livestock/poultry and related small agricultural operations.
2. **Servis Teknikal** — workshop/repair, domestic wiring, computers, air-conditioning, machinery and related technician services.
3. **Makanan & Tempahan** — stalls/warung/burger businesses, small bakery, made-to-order food and small catering.

**Reason:** These three represent materially different, common micro-SME operating patterns while remaining small enough to test genericity without turning the project into a large platform.

**Consequences:** “Kebun” is replaced by **Agro** as the reusable agriculture-domain name.

---

## D-012 — Module simplicity and stop rule

**Status:** LOCKED  
**Owner approval:** 2026-10-01

**Decision:** Do not add further domain modules to the current SuperBasic scope after Agro, Servis Teknikal and Makanan & Tempahan. Each module must remain separable and simple enough that the Apps Script codebase does not degrade into special-case branching or spaghetti code.

**Early warning signal:** Repeated module-name conditionals, duplicated pipelines, or cross-module dependencies begin appearing in Core.

**Consequence:** A future domain that requires substantial special handling should become a separate application/project or require a new owner decision rather than being forced into SuperBasic.

---

## D-013 — Premium natural-language boundary

**Status:** LOCKED  
**Owner approval:** 2026-10-01

**Decision:** Full, natural conversational interaction belongs to **Kerani AI Premium**, not Kerani_Core_SuperBasic. The premium layer may use OpenAI and paid API/subscription credits; SuperBasic must remain functional without this premium capability.

**Reason:** Protect basic affordability and allow explicit control of paid AI-credit consumption.

**Consequences:** SuperBasic may use constrained extraction/OCR/AI where justified, but rich open-ended conversation is a separate premium product capability.

---

## D-014 — OpsMate extraction role

**Status:** LOCKED  
**Owner approval:** 2026-10-01

**Decision:** Continue extracting as much proven, reusable learning as practical from OpsMate. Reusable mechanisms feed Core candidates; agriculture-operational behaviour feeds the **Agro** module; BSE-specific assumptions remain reference/configuration evidence rather than Core behaviour.

**Reason:** OpsMate contains working behaviour already paid for through implementation, regression tests and pilot use.

**Consequences:** Evidence harvesting remains behaviour-first and contract-first; source files are not copied wholesale as architecture.

---

## D-015 — Minimum constrained natural-language intake

**Status:** LOCKED  
**Owner approval:** 2026-10-01

**Decision:** Kerani_Core_SuperBasic supports a **minimum constrained natural-language intake** for short operational free text. AI is allowed to:
1. suggest the user's likely intent/category;
2. extract a structured candidate;
3. provide a confidence/ambiguity signal.

AI is **not** allowed to decide or persist the authoritative record by itself.

**Required behaviour:**

~~~text
FREE TEXT
   ↓
INTENT SUGGESTION
   ↓
candidate category + confidence
   │
   ├── sufficiently clear
   │       ↓
   │   candidate preview
   │
   └── ambiguous / low confidence
           ↓
      ask category / clarification
           ↓
      candidate preview
           ↓
 [Benar] [Betulkan] [Buang]
           ↓
 deterministic domain guard / validator
           ↓
 authoritative structured record
~~~

**Safety rule:** Low or ambiguous confidence produces a question, not an AI guess.

**Authority rule:** Human confirmation and deterministic domain validation are mandatory before an AI-interpreted mutation becomes authoritative.

**Two-stage interpretation:** Prefer a small intent-routing step (“what is the user trying to do?”) followed by the relevant Core/domain parser (“what fields are required?”), instead of one monolithic prompt that attempts every domain simultaneously.

**Premium boundary:** This does not change D-013. Open-ended conversation, long-context reasoning and rich assistant behaviour remain Kerani AI Premium.

**Reason:** Give SuperBasic practical natural-language convenience without allowing probabilistic interpretation to silently corrupt business records or inflate premium AI-credit usage.

**Related risk:** R-010.

---

## D-016 — Free Core and premium intelligence boundary

**Status:** LOCKED  
**Owner approval:** 2026-10-06

**Decision:** Kerani_Core_SuperBasic must remain a genuinely useful free product. The free baseline includes:
- basic receipt capture/extraction where available;
- Purchase, Sale and basic Inventory records;
- Observation / operational note capture;
- Task;
- basic record retrieval and basic business reports;
- summary/retrieval of operational logs.

Free Core may summarize what is already recorded, but it does **not** need to perform higher-order correlation, causality, forecasting or domain intelligence across business and operational data.

When a user requests a capability outside the free boundary, the product must respond explicitly that the requested analysis/automation is a premium capability and offer the relevant paid action; it must not silently fail, hang, or return a generic error merely because the feature is gated.

**Premium candidates include:** forecasting, cross-data intelligence, deeper domain analysis, advanced natural-language reasoning, government/domain document generation, and richer automation.

**Reason:** Keep the generic Core independently useful while making paid value come from additional intelligence and automation rather than from basic access to the user's own records.

---

## D-017 — Credit Pass / pay-per-capability model

**Status:** LOCKED  
**Owner approval:** 2026-10-06

**Decision:** The current primary monetisation direction is **not a mandatory recurring subscription**. Paid capabilities are metered using **Credit Pass / pay-per-capability**.

Required rules:
- show the credit cost before executing a charged capability;
- allow domain modules to expose metered premium capabilities;
- a domain-module onboarding/allowance model may exist, but its exact commercial structure and quota values remain deferred;
- when included/free allowance is exhausted, additional usage may consume Credit Pass;
- a provider/system failure must not be recorded as a successfully delivered paid capability.

**Reason:** Align payment with actual higher-cost/higher-value usage, keep the free Core accessible, and retain flexibility across AI providers whose cost structures may change.

**Deferred:** exact credit prices, monthly allowances, onboarding cost and credit-to-currency economics.

---

## D-018 — Data portability and no artificial lock-in

**Status:** LOCKED  
**Owner approval:** 2026-10-06

**Decision:** Kerani must not depend on artificial data lock-in as its monetisation mechanism. Users may access/export their own stored data and may analyse it independently using ordinary tools or external AI applications.

**Paid value proposition:** convenience, structured workflow, domain contracts, forecasting/intelligence, automation, traceability, and ready-formatted outputs.

**Reason:** A technically capable user being able to export a file and analyse it elsewhere is acceptable; Kerani should win on workflow quality and domain capability rather than blocking access to user data.

---

## D-019 — Credit values and commercial calibration

**Status:** DEFERRED  
**Owner approval:** 2026-10-06

**Candidate examples discussed — NOT LOCKED pricing:**

| Capability | Candidate credit value |
|---|---:|
| Forecast / advanced analysis | 5 credits |
| Richer domain/service forecast or analysis | 10 credits |
| Domain/module onboarding | 100 credits |
| MyGAP-style report generation | 20 credits |

**Decision:** Exact credit values are not approved yet.

**Before pricing is locked, evaluate:** actual model/API cost, number of calls/retries, provider failure rate, document-generation cost, operational overhead, value to user, included allowance, and safety margin.

**Revisit trigger:** SuperBasic architecture is stable enough to identify capability boundaries and representative workloads can be costed/tested.

---

## D-020 — Free-first product/growth principle

**Status:** LOCKED  
**Owner approval:** 2026-10-06

**Decision:** Kerani_Core_SuperBasic should be positioned for broad micro-SME adoption using a **free-but-genuinely-useful** product as the primary acquisition hook.

The product/growth principle is:

> **Free must solve a real basic operational-record problem on its own; premium must clearly add higher-order intelligence, domain capability or automation.**

**Required growth behaviour:**
- public messaging should lead with practical usefulness and the fact that the basic product is free;
- the free tier must not be an intentionally crippled demo;
- the boundary between free/basic and premium/credit capabilities must be visible and understandable;
- when a premium capability is requested, explain what extra value it provides and what it costs instead of hiding the feature or returning an opaque error;
- growth claims must not promise guaranteed grants, certification, financing or business outcomes; Kerani may state that structured records can improve readiness for applications, reporting and evidence requirements;
- meaningful growth push should follow pilot evidence and real user feedback/testimonials rather than relying only on speculative marketing claims.

**Growth intent:** after pilot validation, use short-form demonstrations, testimonials and relevant micro-SME communities/channels to show how basic record discipline can help small businesses become more data-ready.

**Not locked by this decision:** exact viral campaign, platform mix, Marketplace eligibility/tactics, ad spend, creator strategy, copy variants, launch timing or KPI targets. These must be reviewed later against platform policy, pilot evidence and actual conversion behaviour.

**Reason:** The intended advantage is not to hide useful basics behind payment, but to make record-keeping accessible enough that micro-SMEs can start building structured business/operational history; paid capability becomes valuable when users later want more intelligence, forecasting, domain workflows or formal outputs.

---

## D-021 — Premium sampling / demo allowance

**Status:** LOCKED  
**Owner approval:** 2026-10-06

**Decision:** Kerani may occasionally allow selected premium capabilities to run **free as a demo/trial**, without changing their normal premium classification.

**Rules:**
- a free demo does not convert the feature into a permanent Free Core entitlement;
- the product should clearly label the capability as a premium feature being demonstrated;
- demo usage should be deliberate and bounded so users can experience the value before spending credits;
- exact frequency, eligibility, promotional trigger and demo quota remain implementation/growth decisions for later review.

**Reason:** Let users experience premium value before buying credits while preserving a clear Free Core / premium boundary.

---

## D-022 — OpsMate-grade validated operational workflows are premium domain solutions

**Status:** LOCKED  
**Owner approval:** 2026-10-06

**Decision:** Complex operational-record workflows of the kind proven in OpsMate — where records must follow domain-specific operating rules, required-field rules, validation, clarification, review/approval boundaries, and controlled persistence — are **not part of the generic Free Core baseline** merely because the underlying runtime mechanisms may be reusable.

Such workflows belong to a **premium/domain solution layer** and may require:
- structured onboarding;
- a special interview/discovery step to understand the user's operating method, terminology, roles, validation rules and required records;
- configuration/domain-contract setup;
- onboarding cost and/or metered premium usage.

**Boundary:** The reusable runtime mechanisms may still be extracted into Core candidates, but the business-operating method, domain rules, forms, validation semantics and organization-specific workflow must remain outside generic Core unless independently proven generic.

**Reason:** OpsMate demonstrates that high-fidelity operational record keeping can be valuable precisely because it checks records against how work is actually performed before data becomes authoritative. That value requires configuration and domain understanding, so it should not be disguised as a zero-setup generic feature.

**Deferred:** exact onboarding interview format, onboarding price/credits, service level, configuration ownership and which modules receive this depth first.

---


## D-023 — Tenant identity independent of channel
**Status:** LOCKED  
**Owner approval:** 2026-10-07

Every business/user has a persistent Kerani tenant identity. WhatsApp, Telegram, Web and future interfaces are bindings only. Changing channel must not require data migration or a new tenant.

---

## D-024 — Free onboarding = time-to-first-value
**Status:** LOCKED  
**Owner approval:** 2026-10-07

A Free user should reach a first useful/authoritative record through shared Kerani infrastructure without first creating Gemini credentials, Google Drive layout or Apps Script deployment. Customer-owned infrastructure is a later upgrade/onboarding step.

---

## D-025 — Free channel economics + channel-neutral intelligence
**Status:** LOCKED  
**Owner approval:** 2026-10-07

Telegram is the economic/high-usage Free channel. Shared WhatsApp is a convenience/discovery Free channel with controlled allowance. After shared-WA limits, user may top up transport, migrate to Telegram, or buy Premium onboarding for dedicated/owned WhatsApp.

Premium intelligence Credit Pass pricing is the same regardless of channel.

---

## D-026 — Shared WhatsApp capacity, waitlist and seat reclaim
**Status:** LOCKED  
**Owner approval:** 2026-10-07

Each shared Free WhatsApp number has a configurable maximum active-seat count. **50 is an initial planning example, not a locked invariant.**

At capacity: new user gets a capacity-full/waitlist reply; waitlist entry is recorded; owner is notified as backlog grows; owner provisions another number; waiting users are manually invited initially.

A seat is released when tenant moves to Telegram-primary or Premium own-WhatsApp. Tenant/history remain intact.

---

## D-027 — Practical independent Free quotas
**Status:** LOCKED  
**Owner approval:** 2026-10-07

Free has independent controls for: WhatsApp transport; storage/media (especially images/receipts); AI/processing; retrieval/report fair-use/rate limit; and Premium Credit Pass.

Telegram heavy users still face storage, AI/processing, retrieval/report and abuse controls. Exact values are pilot-calibrated and must remain practically useful.

---

## D-028 — Product quota ≠ raw transport quota
**Status:** LOCKED  
**Owner approval:** 2026-10-07

User-facing usefulness is based on useful actions/records/reports, while Kerani internally meters transport replies, Replies Per Record, AI operations and completed records separately.

Candidate/clarify/correct/confirm/validate/audit flow must not be removed merely to save WhatsApp messages.

---

## D-029 — Shared Free AI, deterministic-first
**Status:** LOCKED  
**Owner approval:** 2026-10-07

Free may use shared Kerani AI/processing with per-tenant metering/limits. Free onboarding does not require BYO Gemini. Core should use deterministic routing/retrieval/validation where AI adds no value. Customer-owned AI remains optional later.

---

## D-030 — Tenant-isolated, channel-independent storage
**Status:** LOCKED  
**Owner approval:** 2026-10-07

Storage belongs to tenant, not WhatsApp shard. Channel migration does not relocate history. Images/receipts/documents have practical Free storage quota. User export rights under D-018 remain.

---

## D-031 — Premium own-WhatsApp onboarding
**Status:** LOCKED  
**Owner approval:** 2026-10-07

Users who insist on WhatsApp and do not want repeated top-ups may pay explicit onboarding for dedicated/owned WhatsApp infrastructure, substantially larger channel allowance and extra convenience/richer AI features. Google/Drive/Apps Script Edge may also be configured where appropriate.

Premium intelligence Credit Pass prices remain channel-neutral. Exact onboarding fee/allowance/bundle are deferred.

---

## D-032 — OpenClaw synthetic reliability/audit agent
**Status:** LOCKED  
**Owner approval:** 2026-10-07

Use OpenClaw as a replaceable external reliability harness to inject scheduled synthetic record messages through real Free WhatsApp and Telegram ingress, observe outcomes, detect regressions, notify the owner and generate a weekly reliability report.

Synthetic traffic uses dedicated TEST identities, is explicitly tagged, follows normal routing/clarification/confirmation/validation/persistence controls, cannot bypass Kerani authority, cannot contaminate real customer truth, and is metered separately from real user entitlements.

---

## D-033 — POS / ERP growth path
**Status:** LOCKED  
**Owner approval:** 2026-10-07

Kerani must support a future adapter/contract integration path to POS/accounting/ERP so growing customers do not need to abandon Kerani. Established ERP-owned records remain authoritative in the ERP. Kerani reads/analyzes and only performs controlled validated/idempotent writes.

Future integration metadata should support source_system, external_id, sync_status, synced_at and idempotency_key. Exact vendors are deferred.

---


## D-034 — Free hosted OCR allowance + DIY OCR fallback

**Status:** CANDIDATE

**Candidate decision:** Free Core should include a deliberately small monthly Kerani-hosted OCR allowance so users can experience receipt scanning, but receipt recording must remain possible after that allowance through manual entry or user-assisted external OCR such as personal Gemini/Google Lens followed by pasted text into Kerani.

External/pasted OCR output is **not authoritative**. It must enter the same review path as Kerani OCR:

~~~text
receipt image or pasted OCR text
        ↓
candidate extraction
        ↓
[Benar] [Betulkan] [Batal]
        ↓
deterministic validation
        ↓
authoritative record
~~~

**Pilot parameter:** 1–3 hosted OCR uses/month is only a candidate starting range, not a LOCKED quota.

**Reason:** Preserve Free usefulness and micro-SME survival value while preventing OCR/image-processing cost from becoming unlimited variable exposure.

---


## D-035 — Government Program Bridge
**Status:** LOCKED  
**Owner approval:** 2026-10-07

Kerani may provide an optional institutional/government programme bridge for assistance matching, sponsored capabilities, application evidence packs and outcome reporting. This bridge is not a dependency of Free Core and must not redefine generic Core business-record authority.

---

## D-036 — Sponsor ≠ Data Authority
**Status:** LOCKED  
**Owner approval:** 2026-10-07

A government, agency, association or other sponsor may fund credits, onboarding or capabilities for a tenant without thereby gaining ownership of or blanket access to that tenant's raw business data.

Payment authority and data-access authority are separate contracts.

---

## D-037 — Minimum-Necessary, Purpose-Bound Data Sharing
**Status:** LOCKED  
**Owner approval:** 2026-10-07

Programme data sharing must expose only the fields required for a stated purpose and must be visible to the user before sharing. User authorisation is required for programme-specific individual-data disclosure unless another lawful basis is explicitly established outside Kerani's product assumptions. Aggregated/anonymised reporting is preferred where individual data is unnecessary.

Unrelated chats, receipts, customers and business records must not be silently included.

---

## D-038 — Agency Remains Programme Authority
**Status:** LOCKED  
**Owner approval:** 2026-10-07

Kerani may identify a **potential match**, explain requirements, prepare evidence and transmit/report approved data, but the relevant agency/programme remains authoritative for eligibility, approval, funding, official status and programme rules.

Kerani must not promise approval or represent a candidate match as confirmed eligibility.

---

## D-039 — Outcome Reporting ≠ Automatic Causation
**Status:** LOCKED  
**Owner approval:** 2026-10-07

Kerani may report measured before/after or longitudinal outcome changes, but must not claim that a programme or grant caused those changes unless the evidence and methodology support a causal conclusion.

---

## D-040 — Pilot-to-Proof Strategy
**Status:** LOCKED  
**Owner approval:** 2026-10-07

Kerani growth begins with operational pilot evidence. Real workflows, clarification, correction, validation, confirmation, authoritative writes, retrieval, failures and recovery should become reusable regression/reliability evidence rather than being treated only as testimonials.

Pilot proof precedes broad public-scale claims.

---

## D-041 — Just-Enough Viral-Ready Infrastructure
**Status:** LOCKED  
**Owner approval:** 2026-10-07

V1 infrastructure should be inexpensive at low usage while preserving a clear path to controlled scale. Kerani must avoid speculative high fixed infrastructure cost, but it must also prepare for sudden load through measurable capacity, quotas, backpressure/rate controls, waitlist/fallback behaviour, observability and graceful degradation.

Overload must not create false-success responses or silent data loss.

---

## D-042 — Event Launch Readiness
**Status:** LOCKED  
**Owner approval:** 2026-10-07

A large-event or viral public launch must pass explicit onboarding, load, reliability, cost-safety, demo and contingency gates before it is treated as ready.

A named event such as MAHA 2027 may be a strategic target, but no specific event is an architecture dependency or assumed commitment.

---

## D-043 — Public-Sector Collaboration Boundary
**Status:** LOCKED  
**Owner approval:** 2026-10-07

Kerani may pursue official collaboration in which a department/agency receives measurable digitalisation, adoption or programme-outcome evidence and Kerani receives legitimate outreach/demo access such as shared exhibition space when formally approved.

The collaboration must be programme/institution based, not a personal favour or private KPI-for-access bargain. It must not imply endorsement beyond what the agency has actually approved.

---

## D-044 — Replaceable Strategic Infrastructure Partner
**Status:** LOCKED  
**Owner approval:** 2026-10-07

Kerani may use a software/infrastructure partner for hosting, deployment support, monitoring, operational capacity or scale assistance so growth does not require large speculative capital expenditure.

The partner may earn infrastructure/service revenue; Kerani may gain capacity and operational credibility. Kerani Core, tenant identity, user-data portability and business authority must remain portable and must not be locked to one partner.

---

## D-045 — Partner Credibility ≠ Client Endorsement
**Status:** LOCKED  
**Owner approval:** 2026-10-07

A partner's verified enterprise track record may be cited as evidence of the partner's capability only when accurate and permitted. A partner having served a client such as Petronas must never be represented as that client endorsing Kerani unless an explicit endorsement exists.

---

## D-046 — Grant-Readiness by Evidence
**Status:** LOCKED  
**Owner approval:** 2026-10-07

Kerani may use pilot outcomes, adoption, reliability, cost efficiency, programme impact and verified partner capacity to build evidence for government/development funding applications.

Grant approval is never assumed, and product architecture must remain viable without a particular grant.

---

## D-047 — 4V Growth Principle
**Status:** SUPERSEDED  
**Owner approval:** 2026-10-07  
**Superseded by:** D-048 — V-Road / 7V Core + Extended V-Gates

**Previous decision:** **4V — Value → Volume → Viral → Versatile.**

**Why superseded:** The 4V principle captured growth direction but compressed several distinct maturity disciplines into four words. The owner expanded the model so user interaction, trust, operating quality, variability, partnership, ecosystem portability and maturity can be governed and evidenced explicitly without changing the underlying value-first philosophy.

Historical 4V lineage is preserved. New growth/maturity authority is D-048.

---

## D-048 — V-Road / 7V Core + Extended V-Gates
**Status:** LOCKED  
**Owner approval:** 2026-10-08  
**Supersedes:** D-047

### Canonical principle

> **V-Road — 7V Core + Extended V-Gates**  
> **Value → Verbal → Volume → Viral → Vary → Venture → Versatile**
>
> Kerani AI must earn each maturity state through evidence. It does not become mature merely by accumulating features, AI capability or infrastructure.
>
> **No V is free. Every V must be earned.**  
> **Do not skip the Vs.**

### 7V Core

1. **Value** — solve a real micro-SME problem before chasing reach. Evidence is useful completed work and repeated usefulness, not feature count or signup count.
2. **Verbal** — meet users through simple human-language interaction. Users should be able to type/speak naturally while Kerani carries the structure through candidate, clarification, confirmation and deterministic validation. Verbal is not voice-only.
3. **Volume** — repeated useful adoption, completed records, retained users and accumulated business history prove repeated value. Volume is not QR scans/downloads/signups alone.
4. **Viral** — broad or sudden growth becomes possible only after onboarding, reliability, cost, quota, waitlist/backpressure, observability, graceful-degradation and truthful-failure controls are prepared. Virality is prepared, not assumed.
5. **Vary** — absorb real-world variation in channels, domains, payer models, providers, workloads and programme requirements without forking or fragmenting generic Core. Configuration/adapters should change before Core contracts.
6. **Venture** — use the right public-sector, sponsor, infrastructure, software, association, event or funding partners to accelerate growth without surrendering product authority, tenant identity, user-data authority or portability.
7. **Versatile** — become portable across domains, channels, providers, infrastructure, programmes, partners, integrations and scales through proven reuse rather than declared abstraction.

### Extended V-Gates

These gates are not a second linear lifecycle. They are continuous quality/evidence disciplines that constrain the 7V Core.

**Foundation / Human**
- **Vision** — problem, user and intended outcome are clear.
- **Vocabulary** — domain language is understood without leaking domain assumptions into generic Core.
- **Vibe** — serious system, simple experience; the product should feel light even when backend controls are rigorous.

**Trust / Authority**
- **Veracity** — factual status only; no false SAVE, false success or invented data.
- **Validation** — interpreted input does not become authoritative without required deterministic/domain checks.
- **Verification** — important claims remain testable through evidence, logs, receipts, regression and audit.
- **Volition** — user retains meaningful control: confirm, correct, cancel, consent, export and choose capabilities/channels.
- **Vault** — secrets, credentials, tenant boundaries and sensitive data are protected.
- **Vulnerability** — failures, abuse paths, isolation leaks, duplicate writes, overload and security weaknesses are actively tested.

**Operating**
- **Velocity** — optimise time to first useful value, not API speed alone.
- **Visibility** — transform scattered operational information into structured, searchable and reportable data.
- **Viability** — AI, WhatsApp, OCR, storage, infrastructure and support economics remain sustainable.
- **Vigilance** — monitoring, OpenClaw synthetic checks, alerts, reliability and cost signals operate continuously.
- **Versioning** — change remains traceable, compatible/migratable and rollback-aware.

**Scale**
- **Variability** — traffic, cost, latency, user mix, record size, quota and event spikes are measured operating conditions.
- **Vary** — the system's ability to absorb that variability without Core fragmentation.
- **Venue** — prove the product outside the lab: farm, workshop, shop, booth, field event or programme demo.

**Ecosystem**
- **Vendor-neutral** — partner/provider substitution must not require rewriting business logic or moving tenant authority.
- **Value-chain** — Kerani may connect users, suppliers, customers, agencies, programmes, accounting/POS/ERP and partners without pretending to own every external Source of Truth.
- **Vertical** — useful domain depth belongs in domain modules/solutions, not by contaminating generic Core.

### Maturity destination

~~~text
7V CORE + EXTENDED V-GATES
            ↓
          VITAL
            ↓
        👑 V-KING
~~~

- **Vital** — Kerani becomes operationally important because users repeatedly depend on its utility/history/workflow, not because of artificial lock-in.
- **V-King 👑** — aspirational north star: **become needed, not merely known.** It is not an architecture state, market-dominance claim, or eighth V.

Canonical line:

> **Jangan kejar jadi besar. Jadi berguna sampai ramai perlukan.**

### Anti-shortcut rules

- Viral without Value → attention without retention.
- Volume without Veracity → more bad data.
- Volume without Viability → scale amplifies losses.
- Viral without Vigilance → failure becomes public.
- Venture without Vary → every partner creates a custom fork.
- Venture without Volition → user authority gets sacrificed.
- Versatile without Verification → speculative framework.
- Vital through artificial lock-in → rejected interpretation.
- V-King without Value → branding fantasy.

### Evidence rule

> **Every V requires evidence appropriate to that V.**

Minimum interpretation:
- Value → completed useful workflows / repeated usefulness.
- Verbal → understandable successful human-language intake with safe clarification/confirmation.
- Volume → repeated real usage and retained useful records.
- Viral → measured load, cost, fallback and reliability evidence.
- Vary → multiple channels/domains/providers/payers without Core fork.
- Venture → real partner/programme use without authority or portability leakage.
- Versatile → proven portability across multiple contexts.
- Vital → sustained operational dependence based on utility.
- V-King → broad voluntary adoption/trust; never claimed from aspiration alone.

This principle complements D-020 free-first growth, D-040 Pilot-to-Proof, D-041 viral-ready infrastructure and D-043–D-046 partnership/grant boundaries.

---

## D-049 — Real-Field-Evidence-First Execution
**Status:** LOCKED  
**Owner approval:** 2026-10-09

Real operator/customer samples are first-class execution evidence from the earliest available day. Critical user-facing workflows must be anchored to real field samples whenever such samples exist. Synthetic fixtures may supplement real evidence, but must not silently replace available real-world evidence.

Canonical rule:

> **No sample, no assumption.**

Where a real sample does not yet exist, the relevant behaviour must be marked **UNVALIDATED** rather than being treated as field-proven.

### Field-sample preservation

Real samples should preserve the operational meaning that makes them valuable, including where relevant:
- original wording;
- shorthand and mixed language;
- ambiguity/incompleteness;
- line breaks/format;
- attachment/input type;
- actual missing information.

Personally identifying or sensitive details may be redacted when needed, but redaction must not erase the semantics being tested.

### Execution bridge

For critical user-facing workflows, execution should be traceable through:

~~~text
REAL FIELD CORPUS
        ↓
EXECUTION PROOF MATRIX
        ↓
REUSABLE TEST PROCEDURE
        ↓
ATOMIC TASK INSTANCE
        ↓
PROOF RECEIPT
        ↓
INVALIDATION CHECK
   ├─ proof still valid → PASS_REUSED
   └─ invalidated       → RERUN
~~~

This bridge is execution evidence/planning structure, not a new architecture authority.

### Atomic-task evidence anchor

Where real field evidence exists, an execution task should carry:
- **REAL EVIDENCE ANCHOR**;
- **FIELD SAMPLE IDs**;
- **EXPECTED BEHAVIOUR CONTRACT**;
- **PROOF REUSE KEY**;
- **INVALIDATION TRIGGERS**.

Do not duplicate a long test procedure for every sample. Separate **procedure** from **case/data** so one reusable procedure may execute many field samples.

### Defect-to-corpus rule

A real defect should strengthen the durable corpus:

~~~text
real defect
→ freeze exact relevant input
→ assign corpus/sample ID
→ reproduce FAIL
→ add regression expectation
→ minimal fix
→ sample PASS
→ retain as regression evidence
~~~

A PASS may be reused only while its relevant source/contract/procedure/runtime assumptions remain valid. If an invalidation trigger is hit, rerun the affected proof instead of blindly rerunning every historical case.

**Scope boundary:** This decision applies to Kerani execution. Upstream change to the shared ZASS System Architecture-to-Execution Standard is deferred until E-019 demonstrates that the method reduces repeated execution work without weakening reliability or traceability.

---



## D-050 — Premium Operations Pack: Alert · Remind · Report · Ask
**Status:** CANDIDATE
**Origin:** OpsMate/Kerani extraction + product discussion 2026-10-09

Selected operational automation and richer retrieval capabilities may form a Premium Operations Pack:

| Candidate | Capability | Candidate boundary |
|---|---|---|
| **P-01 — IoT Alert Bridge** | Receive an event/alert from a SuperBasic IoT/device integration and notify the user with useful context/history/escalation. | Kerani is not the sole critical alarm/controller. Device/PLC/HA or equivalent deterministic local path remains authoritative for critical alarm behaviour. |
| **P-02 — Task Reminder + Push Notification** | Automatically remind users about tasks/time/status and push through supported channels. | Basic Task remains available in Free Core; automated reminder/push is a Premium convenience candidate. |
| **P-03 — Scheduled Report** | Deliver daily/weekly/monthly or event-timed reports automatically. | Basic/manual report remains available in Free Core; scheduled delivery is a Premium automation candidate. |
| **P-04 — Interactive Query / Retrieval** | Let users ask richer conversational questions over their own structured history and receive tenant-scoped retrieval/summaries. | Basic deterministic lookup/retrieval remains Free; richer conversational/multi-record retrieval is a Premium candidate. |

> **Premium Operations Pack — Alert · Remind · Report · Ask**

Important boundaries:
- This is a **CANDIDATE**, not a LOCKED premium entitlement.
- Free Core must remain genuinely useful under D-016/D-020.
- Premium candidacy focuses on automation, richer context/intelligence, scheduled delivery and cross-channel convenience rather than removing basic task/report/retrieval capability from Free.
- Critical alarms must not depend solely on Kerani Premium, an LLM, internet connectivity or a cloud provider.
- Exact credit cost, quota, cadence, delivery channel, IoT protocol and escalation policy are deferred.
- Reusable runtime mechanisms should be extracted from OpsMate only after behaviour evidence shows they are generic.

Evidence needed before LOCK: OpsMate behaviour audit for reminder/report/query/push families, one non-BSE reuse example where practical, cost/load measurements, delivery/failure semantics, and an IoT alert safety-boundary test.

---


## D-051 — Premium Intelligence Pack: Analysis · Correlation · Graph · Proposal · Forecast
**Status:** CANDIDATE  
**Origin:** product discussion 2026-10-09

Kerani may package higher-order intelligence over structured tenant history as a separate Premium Intelligence layer:

| Candidate | Capability | Candidate boundary |
|---|---|---|
| **PI-01 — Analysis** | Analyse operational/business records for patterns, performance, cost, output or other domain-relevant questions. | Basic summary/report remains Free; deeper multi-record reasoning is Premium candidate. |
| **PI-02 — Correlation** | Explore relationships between selected variables/records. | Must distinguish observed association from causal claim. |
| **PI-03 — Graph** | Generate useful visualisations/trends from structured data. | Simple tabular/basic reporting may remain Free; richer generated visualisation is Premium candidate. |
| **PI-04 — Proposal** | Draft recommendations, proposals or structured action documents from the user's own data and stated goals. | Must surface assumptions and avoid presenting generated recommendations as authoritative external approval. |
| **PI-05 — Forecast** | Produce bounded forecasts using sufficient history and appropriate domain/external inputs. | Forecast uncertainty, source data and assumptions must be visible; exact model/provider/cost is deferred. |

Candidate product ladder:

~~~text
FREE CORE
record → retrieve → basic summary/report

PREMIUM OPERATIONS
Alert · Remind · Report · Ask

PREMIUM INTELLIGENCE
Analysis · Correlation · Graph · Proposal · Forecast
~~~

**Important boundaries:**
- This is a **CANDIDATE**, not a LOCKED premium entitlement or pricing decision.
- Premium Intelligence must operate on tenant-authorised data and preserve D-018 portability/no artificial lock-in.
- Correlation must not be presented as causation without evidence.
- Forecast/proposal output must expose uncertainty/assumptions where material.
- Exact Credit Pass values, included allowance, model/provider, chart/export format and domain-specific intelligence remain deferred.
- Free Core remains useful without these capabilities.

Evidence needed before LOCK: representative real records, useful-output tests, error/uncertainty behaviour, latency/cost measurements, and user-value evidence for at least a small subset of these capabilities.

---

# 13. LOCKED DECISIONS

This section is authoritative. Architecture and implementation must not contradict these records.

## L-001

**Source Decision:** D-001  
**Decision:** This repository is an OpsMate-derived generic-core extraction, not Kerani Core SME.  
**Locked by:** Project Owner  
**Date:** inherited from pre-v0.3.2 project SoT  
**Supersedes:** None

## L-002

**Source Decision:** D-002  
**Decision:** Genericity is earned through extraction and reuse, not assumed during design.  
**Locked by:** Project Owner  
**Date:** inherited from pre-v0.3.2 project SoT  
**Supersedes:** None

## L-003

**Source Decision:** D-003  
**Decision:** The guiding motto is “Genericity is Generosity.”  
**Locked by:** Project Owner  
**Date:** inherited from pre-v0.3.2 project SoT  
**Supersedes:** None

## L-004

**Source Decision:** D-004  
**Decision:** Public release requires security review, redaction, documentation and explicit licence.  
**Locked by:** Project Owner  
**Date:** inherited from pre-v0.3.2 project SoT  
**Supersedes:** None

## L-005

**Source Decision:** D-010  
**Decision:** SuperBasic is a small generic micro-SME core for Purchase, Sale, Inventory, Observation and Task, with receipt capture as an input capability; no dedicated self-hosted server or premium natural-language processing is required for baseline operation.  
**Locked by:** Project Owner  
**Date:** 2026-10-01  
**Supersedes:** None

## L-006

**Source Decision:** D-011  
**Decision:** The planned domain-module set is exactly Agro, Servis Teknikal and Makanan & Tempahan; Agro replaces the narrower reusable-domain name Kebun.  
**Locked by:** Project Owner  
**Date:** 2026-10-01  
**Supersedes:** None

## L-007

**Source Decision:** D-012  
**Decision:** No additional domain modules are in the current SuperBasic scope; modules must remain simple and separable enough to avoid Apps Script spaghetti.  
**Locked by:** Project Owner  
**Date:** 2026-10-01  
**Supersedes:** None

## L-008

**Source Decision:** D-013  
**Decision:** Full natural-language conversation belongs to Kerani AI Premium using paid AI/API capability; SuperBasic must remain usable without it.  
**Locked by:** Project Owner  
**Date:** 2026-10-01  
**Supersedes:** None

## L-009

**Source Decision:** D-014  
**Decision:** OpsMate remains the primary evidence source: reusable mechanisms feed Core, agriculture behaviour feeds Agro, and BSE-specific assumptions do not become generic Core behaviour.  
**Locked by:** Project Owner  
**Date:** 2026-10-01  
**Supersedes:** None

## L-010

**Source Decision:** D-015  
**Decision:** SuperBasic includes constrained natural-language intake using intent suggestion + candidate extraction + confidence, with clarification for ambiguity, explicit human confirmation and deterministic domain validation before any authoritative AI-interpreted write.  
**Locked by:** Project Owner  
**Date:** 2026-10-01  
**Supersedes:** None; clarifies the boundary in D-013/L-008.

## L-011

**Source Decision:** D-016  
**Decision:** Free Core remains independently useful for basic records, receipt capture where available, retrieval/basic reporting and operational-log summary; higher-order correlation, forecasting, domain intelligence and advanced automation may be premium, and gated requests must be explained explicitly rather than silently failing.  
**Locked by:** Project Owner  
**Date:** 2026-10-06  
**Supersedes:** None

## L-012

**Source Decision:** D-017  
**Decision:** The primary paid model is Credit Pass / pay-per-capability rather than mandatory recurring subscription; charged capability cost is shown before execution, and failed delivery is not treated as a successful paid service.  
**Locked by:** Project Owner  
**Date:** 2026-10-06  
**Supersedes:** None

## L-013

**Source Decision:** D-018  
**Decision:** User data remains accessible/exportable; Kerani does not use artificial data lock-in to force premium purchase. Paid value comes from workflow, domain intelligence, automation, traceability and ready-formatted outputs.  
**Locked by:** Project Owner  
**Date:** 2026-10-06  
**Supersedes:** None

## L-014

**Source Decision:** D-020  
**Decision:** SuperBasic growth is free-first: the free product must solve a real basic record-keeping problem, premium must add clearly explained higher-order value, and major public growth should be driven by pilot evidence/testimonials rather than by crippling the free tier or overstating outcomes.  
**Locked by:** Project Owner  
**Date:** 2026-10-06  
**Supersedes:** None

## L-015

**Source Decision:** D-021  
**Decision:** Selected premium capabilities may occasionally be offered as bounded free demos/trials without changing their permanent premium classification.  
**Locked by:** Project Owner  
**Date:** 2026-10-06  
**Supersedes:** None

## L-016

**Source Decision:** D-022  
**Decision:** OpsMate-grade operational workflows that enforce domain operating rules, validation, clarification, review and controlled persistence belong to premium/domain solutions and may require structured onboarding/interview and setup cost; reusable runtime mechanisms may still feed Core candidates.  
**Locked by:** Project Owner  
**Date:** 2026-10-06  
**Supersedes:** None

---


## L-017
**Source Decision:** D-023  
**Decision:** Tenant identity/history are channel-independent; migration does not create a new tenant or require data migration.  
**Date:** 2026-10-07

## L-018
**Source Decision:** D-024  
**Decision:** Free onboarding prioritises first value using shared infrastructure; owned Google/Gemini/Edge is not a Free prerequisite.  
**Date:** 2026-10-07

## L-019
**Source Decision:** D-025  
**Decision:** Telegram is economic/high-usage Free; shared WhatsApp is controlled convenience; intelligence Credit Pass is channel-neutral.  
**Date:** 2026-10-07

## L-020
**Source Decision:** D-026  
**Decision:** Shared WhatsApp has configurable active seats, explicit waitlist, owner notification, new-number provisioning and seat reclaim.  
**Date:** 2026-10-07

## L-021
**Source Decision:** D-027  
**Decision:** Transport, storage/media, AI/processing, report/retrieval fair-use and Credit Pass are separate controls; Telegram does not remove non-transport quotas.  
**Date:** 2026-10-07

## L-022
**Source Decision:** D-028  
**Decision:** Product usefulness is not raw message quota; integrity confirmation/validation flow is not sacrificed to save messages.  
**Date:** 2026-10-07

## L-023
**Source Decision:** D-029  
**Decision:** Free may use shared Kerani AI with per-tenant limits and deterministic-first behaviour; BYO Gemini is optional later.  
**Date:** 2026-10-07

## L-024
**Source Decision:** D-030  
**Decision:** Storage is tenant-isolated/channel-independent with practical media limits and export rights.  
**Date:** 2026-10-07

## L-025
**Source Decision:** D-031  
**Decision:** Premium onboarding may provide dedicated/owned WhatsApp with much larger channel capacity and richer convenience/AI; intelligence prices stay channel-neutral.  
**Date:** 2026-10-07

## L-026
**Source Decision:** D-032  
**Decision:** OpenClaw is a replaceable synthetic reliability harness through real ingress; it cannot bypass Kerani authority or contaminate real customer truth.  
**Date:** 2026-10-07

## L-027
**Source Decision:** D-033  
**Decision:** Future POS/ERP integration uses adapters/canonical contracts; ERP remains authoritative for ERP-owned records and writes are controlled.  
**Date:** 2026-10-07


## L-028
**Source Decision:** D-035  
**Decision:** Kerani may provide an optional government/institutional programme bridge for assistance matching, sponsored capability, application evidence and outcome reporting without making it a Free-Core dependency.  
**Date:** 2026-10-07

## L-029
**Source Decision:** D-036  
**Decision:** Sponsor payment/funding authority is separate from tenant-data ownership/access authority.  
**Date:** 2026-10-07

## L-030
**Source Decision:** D-037  
**Decision:** Programme data sharing is minimum-necessary, purpose-bound and visible/user-authorised; aggregate/anonymise where individual data is unnecessary.  
**Date:** 2026-10-07

## L-031
**Source Decision:** D-038  
**Decision:** The agency/programme remains authoritative for eligibility, approval, funding and official status; Kerani provides matching/evidence/reporting only.  
**Date:** 2026-10-07

## L-032
**Source Decision:** D-039  
**Decision:** Kerani may report measured outcomes but must not convert correlation or before/after change into an unsupported causal claim.  
**Date:** 2026-10-07

## L-033
**Source Decision:** D-040  
**Decision:** Operational pilot evidence becomes proof/regression/reliability evidence before broad public-scale claims.  
**Date:** 2026-10-07

## L-034
**Source Decision:** D-041  
**Decision:** V1 uses just-enough low-cost infrastructure with a measurable controlled-scale path, graceful degradation and no false-success under overload.  
**Date:** 2026-10-07

## L-035
**Source Decision:** D-042  
**Decision:** Large-event/viral launch requires readiness gates; a named event such as MAHA 2027 is a candidate target, not an architecture dependency.  
**Date:** 2026-10-07

## L-036
**Source Decision:** D-043  
**Decision:** Public-sector collaboration must be official and outcome-based; legitimate outreach/demo access may follow formal programme collaboration, without personal-favour exchange or false endorsement.  
**Date:** 2026-10-07

## L-037
**Source Decision:** D-044  
**Decision:** Kerani may use replaceable strategic infrastructure/software partners for capacity and credibility while preserving Core, tenant, portability and business authority.  
**Date:** 2026-10-07

## L-038
**Source Decision:** D-045  
**Decision:** Verified partner enterprise experience may support partner credibility, but a partner client's name cannot be presented as Kerani endorsement without explicit evidence/permission.  
**Date:** 2026-10-07

## L-039
**Source Decision:** D-046  
**Decision:** Government/development grant readiness is built from evidence; no particular grant is assumed.  
**Date:** 2026-10-07

## L-040
**Source Decision:** D-047  
**Status:** SUPERSEDED  
**Decision:** Historical 4V principle: **Value → Volume → Viral → Versatile**.  
**Date:** 2026-10-07  
**Superseded by:** L-041 / D-048

## L-041
**Source Decision:** D-048  
**Decision:** **V-Road — 7V Core + Extended V-Gates**: Value → Verbal → Volume → Viral → Vary → Venture → Versatile; each V must be earned by evidence, Extended V-Gates continuously govern trust/UX/operations/scale/ecosystem quality, Vital is operational dependence through utility, and V-King is an aspirational north star rather than an eighth V.  
**Locked by:** Project Owner  
**Date:** 2026-10-08  
**Supersedes:** L-040 / D-047

## L-042
**Source Decision:** D-049  
**Decision:** Real field samples are first-class execution evidence from the earliest available day; critical user-facing workflows use a field-corpus → proof-matrix → reusable-procedure → atomic-instance → proof-receipt → invalidation/reuse path, and synthetic fixtures do not silently substitute for available field evidence.  
**Locked by:** Project Owner  
**Date:** 2026-10-09  
**Supersedes:** None

---

# 14. REJECTED IDEAS

No project idea is newly marked REJECTED by this migration.

| ID | Idea | Reason Rejected | Related Decision |
|---|---|---|---|
| — | — | — | — |

---

# 15. DEFERRED ITEMS

| ID | Item | Why Deferred | Revisit Trigger |
|---|---|---|---|
| D-005 | Permanent project name | Function has not yet been proven through reuse. | Proof stage passes. |
| E-001 | Classify completed OpsMate components | Relevant OpsMate baseline must be stable first. | Stable reference checkpoint exists. |
| E-002 | Extract one candidate component | Classification and contract evidence are not ready. | E-001 produces an evidence-backed candidate. |
| E-003 | Assemble minimum generic workflow | Generic components have not yet been extracted. | E-002 passes. |
| E-004 | Build a second tiny application | Core reuse contract not yet proven. | E-003 passes. |
| E-005 | Public-release review | Stack is not yet proven or publication-ready. | Reuse proof is complete. |
| E-006 | OpsMate reproduction test | New composition does not yet exist. | Core + Agro + BSE test config + adapter can be integrated. |
| D-019 | Exact Credit Pass values / commercial calibration | Unit economics and representative workloads are not yet validated. | Stable capability boundaries + measured provider/API costs and workload tests. |
| D-020-T | Growth-channel tactics and viral campaign design | The principle is locked, but platform fit, policy, conversion behaviour and testimonial quality require real pilot evidence. | Pilot complete + usable testimonials + platform-policy review + launch readiness. |
| D-026-P | Shared WhatsApp capacity values | Seats/allowance/overflow/provision threshold need RPR evidence. | Pilot RPR + load data. |
| D-027-P | Free storage/AI/report quota values | Need usefulness + cost evidence. | Pilot workload metrics. |
| D-031-P | Premium WhatsApp package/pricing | Setup effort/economics unmeasured. | Premium onboarding pilot. |
| D-032-P | Reliability-agent cadence | Synthetic volume must not distort capacity. | Reliability pilot. |
| D-033-P | POS/ERP vendor contracts | No real integration selected. | First integration customer/use case. |
| D-034-P | Hosted OCR monthly allowance | Exact free allowance must balance first-value usefulness with OCR/storage/provider cost. | Pilot completed-receipt rate + OCR cost-per-use + conversion evidence. |
| AC-007-P | V1 central control-plane choice | Cloud Run remains viable but has not been benchmarked against Cloudflare Workers+D1 or central Apps Script for Kerani workload, entry cost and ops complexity. | E-016 three-way load/cost/ops comparison before PRE-ARCH lock. |
| D-035-P | Exact programme/agency integration | No real government programme contract is selected. | Real programme/counterpart + authoritative data requirements. |
| D-037-P | Exact shared fields/consent wording/legal basis | Requirements differ by programme and jurisdiction. | Programme-specific legal/privacy review. |
| D-042-P | MAHA 2027 / named event arrangement | Strategic target only; booth/access/load commitment is not yet evidenced. | Formal event/agency opportunity + readiness evidence. |
| D-043-P | Shared booth / Jabatan collaboration terms | No official collaboration is assumed. | Formal departmental/programme approval. |
| D-044-P | Named infrastructure/software partner + commercial terms | Partner capacity, SLA, pricing and exit terms are unverified here. | Due diligence + written commercial/technical agreement. |
| D-045-P | Petronas/customer reference wording | A vendor's client history and permission to cite it must be verified. | Verifiable reference + permitted wording. |
| D-046-P | Specific grant programme/application | No particular funding approval or eligibility is assumed. | Current official programme + eligibility/evidence review. |
| D-048-P | Exact viral/load/partner thresholds | V-Road principle is locked; thresholds require measured traffic/cost/reliability data. | Pilot + load-test evidence. |
| D-050-P | Premium Operations Pack entitlement/pricing/automation parameters | Alert/Reminder/Report/Ask boundaries and costs are not yet evidenced enough to LOCK. | OpsMate behaviour audit + pilot/reuse/cost/safety evidence. |
| D-051-P | Premium Intelligence Pack packaging/pricing/model choices | Analysis/Correlation/Graph/Proposal/Forecast need measured cost, output-quality and user-value evidence. | Representative real-data pilot + unit-economics review. |
| AC-010-P | Cloudflare control-plane service mix and limits | Exact Workers/D1/queue/schedule usage and provider limits are externally changeable and workload-dependent. | Current official-term verification + E-016 benchmark evidence. |

---

# 16. OPEN LOOPS

Architecture freeze is blocked by the following:

- [ ] Freeze a stable OpsMate reference checkpoint.
- [x] Map at least one complete observable OpsMate workflow. Behaviour Map #1 (Input Usage / Inventory) is recorded in E-001A.
- [ ] Populate the evidence-backed reuse matrix.
- [ ] Resolve Q-015: ownership of routing between direct/read and stateful/mutation paths.
- [ ] Resolve Q-016: which request classes require Durable Inbox rather than treating it as universal.
- [ ] Resolve Q-017: whether human confirmation is Core-mandatory, optional capability, or module/application policy.
- [ ] Define minimum Core ↔ Module contract.
- [ ] Prove Core can run a non-farm module.
- [ ] Determine the boundary between generic validation and domain validation.
- [ ] Test parser/provider substitution behind a stable contract.
- [ ] Validate D-015 with clear, ambiguous and misrouted free-text cases: AI suggestion → clarification/preview → human confirmation → deterministic domain validation → authoritative record.
- [ ] Run the OpsMate reproduction test.
- [ ] Complete public-release safety review before any open release.
- [ ] Resolve or deliberately defer critical architecture questions before confirmation.
- [ ] After SuperBasic architecture is available, cross-audit it against the existing Kerani Core discussions/designs and adopt only capabilities that remain lightweight, generic and maintainable.
- [ ] Before locking Credit Pass prices, measure representative AI/OCR/document/forecast workloads and derive unit economics; do not infer prices from token cost alone.
- [ ] After pilot, review the free/premium boundary with real users and testimonials before public growth push; then decide channel mix, launch copy and viral tactics.
- [ ] Test whether a bounded free demo of one premium capability materially improves user understanding/conversion without confusing the permanent Free Core boundary.
- [ ] Define the minimum onboarding/interview contract for OpsMate-grade premium workflows before any such domain solution is sold or generalized.
- [ ] Calibrate shared-WA seats/base allowance/overflow using RPR and real usage; do not freeze 50 as invariant.
- [ ] Calibrate Free storage/media, AI/processing and report/retrieval fair-use limits.
- [ ] Validate waitlist → owner notify → new number → manual invite under viral-load simulation.
- [ ] Validate WhatsApp→Telegram and shared-WA→Premium migration with one tenant/history.
- [ ] Run OpenClaw synthetic reliability harness and verify weekly report/alerts with zero customer-data contamination.
- [ ] Validate tenant isolation across channels/storage.
- [ ] Test one POS/ERP-like adapter fixture before claiming enterprise readiness.
- [ ] Test hosted OCR vs personal-Gemini/Lens paste fallback through the same candidate/confirmation/validation path; measure cost per completed receipt.
- [ ] Decide the Free hosted-OCR allowance only after pilot evidence; keep 1–3/month as a candidate range.
- [ ] Run E-016 three-way benchmark: central Apps Script vs AC-010 Cloudflare Workers+D1 vs AC-007 Cloud Run stack for V1 cost/entry barrier, latency, concurrency, state/quota/waitlist clarity, scheduling/async needs, observability and migration flexibility.
- [ ] Convert operational pilot cases into a documented proof/regression set under D-040.
- [ ] Run E-017 mock Government Program Bridge: potential match → consented evidence pack → sponsor entitlement → outcome report, with no unrelated-data leakage.
- [ ] Run E-018 viral/event-scale drill: onboarding spike, quotas/backpressure, waitlist/fallback, cost ceiling, OpenClaw reliability and partner-scale activation/rollback.
- [ ] Define a partner activation threshold and exit/portability test before treating any infrastructure partner as a scale safety net.
- [ ] Treat MAHA 2027/shared booth/Jabatan/vendor/Petronas/grant details as real-counterpart work, not architecture facts, until verified.
- [ ] Build the first Kerani real-field corpus from earliest available pilot/operator messages; preserve raw semantics and mark missing-real-sample behaviours UNVALIDATED.
- [ ] Run E-019 Evidence-Seeded Execution Pilot on one Purchase slice: field corpus → proof matrix → reusable procedure → atomic task instance → proof receipts → deliberate invalidation/reuse check.
- [ ] Measure whether E-019 materially reduces duplicated procedure prose/retesting while preserving reliability and traceability before proposing any upstream ZASS System change.
- [ ] Before architecture confirmation, follow Full ZASS v0.3.10 governance: DRAFT ARCH → ARCHITECTURE CHALLENGE → controlled revision → owner LOCK PRE-ARCH → detailed ACTION_PLAN ↔ PRE-ARCH → atomic evidence tasks → PRE-ARCH review → LAST ARCHITECTURE CHALLENGE → BUILD ARCHITECTURE → explicit YA, CONFIRM ARCHITECTURE.

---

# 17. EXPERIMENTS / EVIDENCE

## E-001 — Classify completed OpsMate components

**Status:** DEFERRED

**Question being tested:** Can completed OpsMate behaviour be separated into evidence-backed reuse classes?

**Hypothesis:** Stable OpsMate behaviour will reveal components that can be classified without speculative abstraction.

**Method:** Freeze baseline, map behaviour, then build the extraction ledger.

**Success criteria:** Ledger contains evidence-backed classification and links to tests/behaviour.

**Result:** PENDING.

**Conclusion:** PENDING.

**Affected decisions:** D-006, D-007, D-008.

---

## E-001A — One Workflow Extraction Audit: Input Usage / Inventory

**Status:** PASS — workflow slice only; parent E-001 remains incomplete.  
**Date:** 2026-09-29  
**Source snapshot:** `BSE-dzuddiyn01gmail/BSE-OpsMate-TEST` main at commit `10e20cd601421bb114ff3bfd7edf9e3f5e8160c4`.

**Evidence files reviewed:**
- `docs/ARCHITECTURE.md`
- `docs/DEVELOPMENT_STATUS.md`
- `InventoryReviewTest.js`
- `TelegramWorkerTest.js`
- `TelegramQueueTest.js`
- `TelegramApprovalUiTest.js`
- `GeminiUnifiedTest.js`

**Question being tested:** Can one proven OpsMate workflow be mapped behaviour-first, classified without treating source-file structure as architecture, and expressed as an implementation-independent contract candidate?

**Input example:**

~~~text
PENGGUNAAN BAHAN
Item: Sarung tangan pakai buang
Kuantiti: 2 kotak
~~~

### Behaviour Map #1

| Stage | Observed behaviour | Current implementation evidence | Initial classification |
|---|---|---|---|
| 1 | Receive Telegram message | `receiveBseTelegramTest()` | `GENERIC` candidate — channel adapter |
| 2 | Persist raw request durably | `TELEGRAM_TEST_QUEUE` | `GENERIC` candidate |
| 3 | Interpret/extract a structured candidate from the queued report | `bseUnifiedProcess_()` using Gemini 3.1 Flash Lite | extraction responsibility: `GENERIC` candidate; current Gemini implementation: implementation detail |
| 4 | Apply deterministic contract guard to model output | `bseUnifiedGuard_()` and domain-specific guard helpers | guard responsibility: `GENERIC` candidate; individual domain rules vary |
| 5 | Apply inventory-domain validation and canonicalisation | `bseInventoryValidateResult_()` | validation mechanism may be generic; inventory/date/unit semantics are `AGRO-GENERIC` / domain-specific |
| 6 | Persist candidate representation | worker `candidate_json` | `GENERIC` candidate |
| 7 | Route actionable PASS to human review | queue → `NEEDS_HUMAN_REVIEW` | `GENERIC` candidate |
| 8 | Send confirmation card as reply to original message | `bseTelegramApprovalEnsureCard_()` | `UNCERTAIN` — possible generic capability |
| 9 | Bind Benar / Betulkan / Buang to original reporter | reporter confirmation core | `UNCERTAIN` |
| 10 | Benar invokes domain writer boundary | `bseInventoryApprovalBoundaryCore_()` → `bseInventoryReviewCore_()` | `AGRO-GENERIC` |
| 11 | Write approved TEST domain record | `TEST_INVENTORY_EVENT` | behaviour: `AGRO-GENERIC`; Sheet/schema: `OPSMATE/BSE-SPECIFIC` |
| 12 | Write review/audit evidence | `TEST_INVENTORY_REVIEW` | audit concept: `GENERIC`; representation: `OPSMATE/BSE-SPECIFIC` |
| 13 | Move queue to terminal inventory TEST state | `INVENTORY_APPROVED_TEST` / reject counterpart | domain state |
| 14 | Close card and emit reporter/owner notification | Telegram approval UI | notification behaviour: generic candidate; transport: Telegram-specific |

### Observed state distinction

~~~text
RAW TELEGRAM MESSAGE
        ↓
durable queue
        ↓
AI extraction
        ↓
deterministic guard
        ↓
domain validation
        ↓
candidate_json
        ↓
NEEDS_HUMAN_REVIEW
        ↓
human confirmation
        ↓
authoritative TEST domain record + audit
        ↓
terminal state + response/event
~~~

This provides early positive evidence for Q-014: the current workflow distinguishes the raw message, candidate state and authoritative TEST domain record. E-001B later strengthened this finding by showing that candidate representation can also differ from authoritative persistence representation. Q-014 remains OPEN until this separation is checked across additional workflow families.

### Candidate contract exposed by the workflow

~~~text
REQUEST
- source reference
- actor/reporter
- channel context
- received_at
- original text

→ CANDIDATE
- intent/domain
- extracted fields
- validation state
- missing fields
- original evidence
- production boundary

→ HUMAN DECISION
- confirm
- correct
- discard

→ AUTHORITATIVE DOMAIN RESULT
- approved domain record
- audit record
- terminal state

→ RESPONSE / EVENT
~~~

This is a contract candidate only. It does not make Telegram, Apps Script, Google Sheets, the inventory parser, or the current approval UI part of the generic Core by default.

### Result

**Observed result:** PASS for this workflow slice. One real OpsMate workflow can be mapped behaviour-first and separated into generic candidates, domain behaviour, BSE-specific representation and uncertain boundaries.

**Learning:** Classification should be applied to small behaviours/contracts rather than whole files. A single OpsMate source file can mix generic mechanism, domain semantics and BSE-specific persistence. The initial map also over-associated the regression helper `bseInventoryParseMessage_()` with runtime parsing; E-001B corrected this and reinforced that source helpers must not be mistaken for runtime architecture.

**Uncertain boundary:** Human confirmation/approval appears reusable, but this experiment does not prove whether it belongs in Core, is an optional Core capability, or belongs to the application/module policy.

**Impact:** **PROCEED**.
- D-007 → `TESTING`
- D-008 → `TESTING`
- D-009 → `TESTING`
- D-006 remains `CANDIDATE`
- parent E-001 is **not PASS**; a complete evidence-backed component ledger still requires a frozen reference baseline and broader workflow coverage.

---

## E-001B — Behaviour Map #1 Runtime Verification

**Status:** PASS — audit found and corrected a material mapping error.  
**Date:** 2026-09-29  
**Verified source:** `BSE-dzuddiyn01gmail/BSE-OpsMate-TEST` main at commit `a6b504aff254935023ea19d6a1ce90dff597deb2`.  
**Compared against E-001A snapshot:** `10e20cd601421bb114ff3bfd7edf9e3f5e8160c4`.

**Question being tested:** Does Behaviour Map #1 accurately describe the effective runtime path for Input Usage / Inventory?

### Result

The lower half of Behaviour Map #1 remains supported: durable queue, candidate state, human review, reporter confirmation, domain writer, authoritative TEST record, audit and response/notification.

A material error was found in the parser/runtime section. The ordinary Telegram worker does not primarily call `bseInventoryParseMessage_()`. The effective runtime path is:

~~~text
Telegram intake
→ request routing
→ TELEGRAM_TEST_QUEUE for report workflow
→ processBseTelegramTestQueue()
→ bseUnifiedProcess_()
→ Gemini extraction
→ bseUnifiedGuard_()
→ domain-specific guards
→ bseInventoryValidateResult_()
→ candidate_json
→ clarification / NEEDS_HUMAN_REVIEW
→ reporter confirmation
→ domain writer
→ authoritative TEST record + audit
→ response / notice
~~~

`bseInventoryParseMessage_()` remains useful deterministic logic and regression evidence, but this experiment does not treat it as the primary runtime parser.

### Additional source-derived findings

1. The current OpsMate intake now has direct command/retrieval branches such as report/history/record/plot retrieval before an ordinary report is queued.
2. Therefore not every request passes through the same queue → AI → approval path.
3. Candidate representation can differ from authoritative persistence representation. For example, an Input Usage candidate may be represented as `Input_Usage_Log` / `INPUT_USAGE`, while the inventory approval boundary persists the approved TEST domain result through the inventory event writer.
4. `TelegramApprovalUiTest.js` contains repeated function definitions from implementation history; the final effective definition wins in Apps Script/JavaScript. This is additional evidence that file-level copying is not a safe extraction method.
5. The user-facing reject/discard label changed from `Buang` to `Batal` in the current repo while the internal terminal state remains `DISCARDED_BY_REPORTER`; this is a UI wording change rather than a contract-level behaviour change.

### Learning

- **AI extraction ≠ deterministic guard ≠ domain validation.**
- The reusable candidate is the responsibility/contract boundary, not Gemini, regex or a specific parser function.
- **source file ≠ behaviour ≠ contract ≠ architecture**.
- The runtime may need at least two interaction families: a direct/read path and a stateful/mutation path.
- Durable Inbox and human approval should not be assumed to be universal.

### ZASS impact

- D-007 remains `TESTING` with stronger evidence.
- D-008 remains `TESTING` with stronger evidence.
- D-009 remains `TESTING` with stronger evidence.
- AC-005 remains `CANDIDATE` and is refined to include direct/read vs stateful/mutation paths.
- Q-014 remains OPEN but has stronger evidence.
- Add Q-015, Q-016 and Q-017.
- Add R-009.
- D-006 remains `CANDIDATE`.
- Parent E-001 remains incomplete.
- No decision becomes LOCKED.

---

## E-002 — Extract one candidate component

**Status:** DEFERRED

**Question being tested:** Can one GENERIC candidate be extracted without breaking its proven behaviour?

**Success criteria:** Relevant OpsMate-derived regression tests pass against the extracted implementation.

**Result:** PENDING.

**Affected decisions:** D-009.

---

## E-003 — Assemble minimum generic workflow

**Status:** DEFERRED

**Question being tested:** Can Core SuperBasic execute a domain-neutral workflow?

**Success criteria:** TEST workflow runs without farm/BSE vocabulary, domain code forks or hidden client assumptions.

**Additional pass signal:** Core can run a non-farm dummy module such as Echo or Todo.

**Result:** PENDING.

**Affected architecture candidate:** AC-005.

---

## E-004 — Build a second tiny application

**Status:** DEFERRED

**Question being tested:** Is the extracted core reusable without a major rewrite?

**Success criteria:** A second application works through configuration/extension points.

**Result:** PENDING.

**Affected decisions:** D-002, D-009.

---

## E-005 — Public-release review

**Status:** DEFERRED

**Question being tested:** Is the stack safe and understandable enough to publish?

**Success criteria:** No secrets/private data; safe examples; documentation; threat notes; explicit licence.

**Result:** PENDING.

**Affected decision:** D-004.

---

## E-006 — OpsMate reproduction test

**Status:** DEFERRED  
**Migrated from:** legacy AC-006.

**Question being tested:** Can the new composition reproduce selected, documented OpsMate workflows?

**Proposed composition:**

**Kerani_Core_SuperBasic + Kerani_Agro + BSE test configuration + Telegram adapter**

**Pass signal:** Selected OpsMate workflows pass the same behaviour contracts using the new composition.

**Failure signals:**
- Core cannot run a non-farm module.
- Removing a module damages Core.
- BSE-specific assumptions leak into Core.
- Changing channel/parser/provider requires business-logic rewrite.
- Raw messages are confused with authoritative records.

**Result:** PENDING.

**Affected architecture candidate:** AC-005.

---


## E-007 — Free onboarding to first record
**Status:** PLANNED  
**Pass:** first useful/authoritative record without customer-owned API keys, Apps Script deployment or Google/Gemini setup.

## E-008 — RPR + shared-WA capacity
**Status:** PLANNED  
Measure Replies Per Record, replies/user/month, clarification/correction rate, inactive seats and overflow demand.

## E-009 — Channel migration continuity
**Status:** PLANNED  
**Pass:** WA→Telegram and shared-WA→Premium preserve one tenant, history and credits.

## E-010 — Free quota fairness
**Status:** PLANNED  
**Pass:** heavy Telegram user cannot bypass storage/media, AI/processing or report/retrieval fair-use limits or degrade another tenant.

## E-011 — Tenant isolation
**Status:** PLANNED  
**Pass:** Tenant A cannot retrieve/mutate/enumerate Tenant B data through any channel.

## E-012 — Waiting-list viral-capacity drill
**Status:** PLANNED  
**Pass:** full shard creates explicit waitlist, owner alert and clean manual invite to new shard without duplicate tenant.

## E-013 — OpenClaw reliability audit
**Status:** PLANNED — OWNER APPROVED FOR EXECUTION DESIGN 2026-10-07  
**Execution state:** tracked in ACTION_PLAN; implementation must not start before the required test ingress/runtime exists.

**Question:** Can a replaceable external synthetic agent prove that Kerani still behaves correctly through the same WhatsApp/Telegram paths used by real Free users?

**Required synthetic coverage:**
- normal Purchase;
- normal Sale;
- Observation;
- ambiguous input that must clarify rather than guess;
- correction/confirmation flow;
- basic report/retrieval;
- provider/AI failure handling;
- storage/authoritative-write failure handling;
- WhatsApp ingress;
- Telegram ingress.

**Required measurements:** end-to-end success rate, semantic/classification correctness, confirmation-flow integrity, authoritative-write success, latency, provider/API failures, retry behaviour, duplicate/idempotency failures, per-channel reliability, AI operations per test and estimated infrastructure cost per test.

**PASS:** synthetic WhatsApp/Telegram tenants traverse normal controls, detect/report injected or observed failures, generate owner alerts when required, and produce a weekly reliability report without contaminating real customer data, business reports, revenue metrics or product entitlements.

**STOP / ESCALATE conditions:**
- synthetic data reaches real customer truth;
- the agent bypasses required confirmation/validation;
- duplicate authoritative records are created;
- provider failure is reported as false success;
- a material architecture defect is revealed.

Exact test cadence and traffic volume remain deferred/pilot-calibrated.

## E-014 — POS/ERP adapter fixture
**Status:** PLANNED  
**Pass:** small external-system fixture maps through stable adapter with external IDs/idempotency and controlled read/write semantics.



## E-015 — Hosted OCR allowance + DIY OCR fallback

**Status:** PLANNED

**Question:** Can Kerani preserve useful Free receipt recording while sharply limiting hosted OCR cost?

**Test:** Compare Kerani-hosted OCR on a small monthly allowance against personal Gemini/Lens → pasted OCR text → Kerani candidate flow.

**Pass signals:**
- both paths reach the same confirmation/validation boundary;
- external OCR text never bypasses review;
- manual entry remains available;
- hosted OCR cost per completed useful receipt can be measured;
- the candidate 1–3/month allowance can be calibrated from real use rather than guessed.

---

## E-016 — V1 central control-plane benchmark

**Status:** PLANNED

**Question:** Which low-complexity control-plane option best satisfies Kerani's LOCKED multi-tenant/channel/quota/reliability boundaries at the lowest practical entry cost?

**Compare:**
1. central Apps Script;
2. **AC-010 Cloudflare Workers + D1** with only evidence-needed queue/schedule services;
3. **AC-007 Cloud Run + Firestore + Secret Manager + basic Logging/Monitoring**.

**Measure:** setup/maintenance effort, webhook behaviour, request latency, concurrency headroom, tenant/quota/waitlist implementation, secret handling, scheduled/async capability, observability, failure recovery, estimated low-traffic cost, free-tier/entry barriers, scale-up path and migration/rollback flexibility.

**Required practical test for AC-010:** webhook → tenant lookup → quota/state update → durable/async step where needed → reply; then one scheduled trigger → reminder/report path.

**OpenClaw note:** OpenClaw is not a fourth control-plane competitor. D-032/E-013 keeps it as a replaceable synthetic reliability/audit agent.

**Pass condition:** choose the smallest option that satisfies LOCKED boundaries, has truthful failure behaviour and a documented upgrade/exit path, without premature infrastructure or hidden provider lock-in.

---


## E-017 — Mock Government Programme Bridge

**Status:** PLANNED

**Question:** Can Kerani support assistance matching, sponsor-funded capability and programme outcome reporting without granting a sponsor blanket tenant-data authority?

**Fixture flow:**

~~~text
tenant profile/history
→ potential programme match
→ required-field disclosure
→ user review/consent
→ application evidence pack
→ sponsor-funded entitlement
→ continued Kerani usage
→ programme outcome report
~~~

**PASS signals:**
- programme sees only approved/required fields;
- unrelated tenant data remains private;
- sponsor funding does not imply raw-data access;
- agency remains authoritative for eligibility/approval;
- sponsored entitlement is auditable and separate from user-paid credits;
- outcome report distinguishes measured change from causal claim;
- export/report path works without requiring a bespoke agency API.

---

## E-018 — Viral/Event-Scale + Partner-Scale Drill

**Status:** PLANNED

**Question:** Can Kerani stay safe, useful and economically bounded during a sudden launch/event spike, and can a replaceable infrastructure partner be activated without changing product authority or tenant history?

**Test areas:**
- rapid onboarding spike;
- shared-WA capacity/waitlist and Telegram fallback;
- AI/OCR/storage/report quota pressure;
- Cloud/Apps-Script runtime capacity under the selected V1 architecture;
- cost ceilings and variable-cost alerts;
- graceful degradation/backpressure;
- OpenClaw synthetic reliability during load;
- partner activation threshold;
- partner-scale handoff;
- rollback/exit while preserving tenant identity/history.

**PASS signals:**
- no false-success or silent data loss;
- user-visible degradation/fallback is truthful;
- one heavy cohort cannot starve all tenants;
- cost growth remains observable/bounded;
- synthetic monitoring detects meaningful regression;
- partner activation does not require business-logic rewrite or tenant-data migration;
- rollback/exit is documented and testable.

**Named-event note:** MAHA 2027 may later supply a concrete load scenario, but this experiment must remain event-neutral.

---


## E-019 — Evidence-Seeded Execution Pilot
**Status:** PLANNED — OWNER APPROVED 2026-10-09

**Question:** Can real-field-evidence-first execution reduce repeated atomic-task/test orchestration while preserving or improving correctness, traceability and regression safety?

**Initial slice:** one small **Purchase intake** workflow.

**Initial field-sample target:** approximately 5–10 real operator/customer messages as soon as they are available. This range is an execution target, not an architecture constant.

**Method:**

~~~text
REAL FIELD CORPUS
→ map sample IDs to expected behaviour
→ build EXECUTION PROOF MATRIX
→ define one reusable procedure for the workflow class
→ execute bounded implementation/task instance
→ generate proof receipts
→ make one controlled relevant code/contract change
→ evaluate invalidation rules
→ rerun only affected proofs
→ mark unaffected valid proofs PASS_REUSED
~~~

**Minimum sample coverage where available:**
- normal/clear input;
- ambiguous or incomplete input;
- correction/confirmation behaviour;
- one failure/edge case relevant to the slice.

**Proof matrix must connect:**
- architecture/decision lineage;
- field sample ID;
- expected behaviour contract;
- reusable procedure;
- implementation surface;
- required proof/evidence.

**Proof receipt should identify enough state to decide reuse/invalidation, such as:**
- source revision/SHA;
- field-sample ID or stable sample hash;
- procedure version;
- behaviour/contract version;
- relevant runtime/environment;
- factual result.

The exact receipt schema is implementation detail unless later evidence justifies standardisation.

**PASS signals:**
- real samples influence implementation before late-stage testing rather than appearing only after build;
- one reusable procedure can execute multiple cases without copy-pasting the procedure into each task;
- a real defect/sample can become a durable regression case;
- proof reuse is factual and traceable;
- a controlled change invalidates only the proofs whose assumptions were affected;
- no required regression is skipped merely to reduce work;
- task/result lineage remains clear;
- measured execution/retest overhead is lower than an equivalent duplicated-case workflow.

**FAIL / ESCALATE signals:**
- real sample meaning is sanitised until ambiguity/field behaviour is lost;
- synthetic examples are reported as real field evidence;
- PASS_REUSED is claimed without a valid reuse key/invalidation check;
- proof reuse hides a regression;
- the reusable procedure becomes so generic that it obscures workflow-specific acceptance criteria;
- the method creates more governance overhead than the repeated work it is intended to remove.

**Upstream gate:** Do not change the shared ZASS System Architecture-to-Execution Standard from this idea alone. First review E-019 evidence. If the pilot demonstrates material benefit without weaker reliability/traceability, propose the smallest upstream ZASS refinement separately.

---

# 18. ARCHITECTURE READINESS

ZERO → ARCHITECTURE measures readiness to form and confirm architecture. It is not coding progress.

| Criterion | Weight | Score | Contribution | Reason |
|---|---:|---:|---:|---|
| Purpose/problem clear | 10% | 1 | 10% | Extraction purpose is explicit. |
| Users/stakeholders and desired outcomes clear | 10% | 0.5 | 5% | Future small teams/maintainers are implied; primary consumer is not yet formally proven. |
| Scope and non-goals clear | 10% | 1 | 10% | Scope and exclusions are explicit. |
| Constraints and quality attributes known | 10% | 1 | 10% | Runtime, channel, provider, security and maintainability constraints are documented. |
| Options and trade-offs compared | 10% | 0.5 | 5% | Evidence-led extraction vs direct refactor is compared, but architecture alternatives are not yet tested. |
| Critical assumptions closed or have experiments | 15% | 0.5 | 7.5% | E-001A and E-001B tested one workflow family and corrected the runtime map; major assumptions remain open. |
| Major risks addressed | 10% | 0.5 | 5% | Guardrails exist; evidence of effectiveness is pending. |
| Main system flows clear | 10% | 0.5 | 5% | One stateful workflow is mapped and a direct/read path is now observed, but ownership and broader cross-workflow evidence remain incomplete. |
| Major decisions LOCKED | 10% | 0.75 | 7.5% | Product, tenant/channel, quota, reliability, institutional-data, pilot/scale/partner, V-Road and real-field-evidence execution principles are locked; extraction/runtime boundaries still require evidence. |
| No critical architecture blockers | 5% | 0 | 0% | Evidence baseline, contracts and reproduction proof are still missing. |

**ZERO → ARCHITECTURE score:** **65%**

**Status:** **DECIDING**

**Progress bar:** **[███████░░░] 65% — DECIDING**

**Readiness gate:** **NOT READY**

Architecture blockers:
- no frozen reference evidence package;
- one behaviour map is corrected and a second interaction family is observed, but broader reference-baseline and cross-workflow contract evidence remain incomplete;
- no validated Core ↔ Module contract;
- AC-005 is untested;
- no non-farm genericity proof;
- no reproduction-test result.

A DRAFT ARCH may be proposed only after readiness reaches at least 70%. Architecture confirmation requires the Full ZASS v0.3.10 PRE-ARCH evidence loop, LAST ARCHITECTURE CHALLENGE, BUILD ARCHITECTURE gate and the exact owner response **YA, CONFIRM ARCHITECTURE**.

## Evidence Confidence

**Evidence Confidence:** **LOW**

**Reason:** Direct OpsMate evidence exists for one mapped workflow family and its runtime verification, but the frozen reference package, broader workflow coverage, module-contract proof, non-Agro proof, constrained-NL edge-case validation and reproduction test are still incomplete. Product and monetisation boundaries are clearer, but Credit Pass unit economics and scale/provider behaviour are not yet empirically validated.

---

# 19. ARCHITECTURE GENERATION INSTRUCTION

Current state: **NOT READY FOR CONFIRMED ARCHITECTURE**.

When readiness later becomes READY, architecture must be generated only from:
1. Goals
2. Constraints
3. LOCKED decisions
4. Required workflows
5. Known risks
6. Validated evidence
7. Explicitly accepted trade-offs

Any missing major decision must be returned as an **ARCHITECTURE BLOCKER**, not silently assumed.

---

# 20. CHANGE CONTROL

After architecture exists:

~~~
New idea
↓
CANDIDATE
↓
Impact analysis
↓
DECISION
↓
Human approval
↓
LOCK
↓
Architecture update
~~~

If a LOCKED decision must change:
1. create a new decision entry;
2. explain why the previous decision is no longer valid;
3. perform impact analysis;
4. mark the old decision SUPERSEDED;
5. LOCK the replacement decision;
6. update architecture only after the replacement is locked.

## v0.3.2 semantic migration note

The previous Section 16 used AC-001 through AC-006 for a mixture of process proposals, architecture boundary and test strategy. Under ZASS v0.3.2, AC means **Architecture Candidate** only.

Canonical migration:

| Legacy ID | Previous meaning | Canonical v0.3.2 record |
|---|---|---|
| AC-001 | Reference implementation baseline | D-006 (CANDIDATE) |
| AC-002 | Behaviour-first audit | D-007 (CANDIDATE) |
| AC-003 | Four-way reuse matrix | D-008 (CANDIDATE) |
| AC-004 | Contract before source code | D-009 (CANDIDATE) |
| AC-005 | Candidate runtime/module boundary | AC-005 retained |
| AC-006 | Reproduction test | E-006 |

This mapping preserves historical traceability and prevents future misuse of AC IDs.


## Full ZASS v0.3.10 / ZASS SYSTEM v0.2.1 alignment — 2026-10-07

This project now follows the current official ZASS SYSTEM surface and architecture-to-execution contract.

**System routing:** DUMP / DECIDE / DESIGN. Full ZASS remains the stronger-governance DESIGN path.

**Human-facing rule:** progressive disclosure; present only the next meaningful human action; never claim SAVE/sync without a real persistence receipt.

**Architecture-to-execution gate for this project:**

~~~text
DRAFT ARCH
→ ARCHITECTURE CHALLENGE
→ CONTROLLED REVISION
→ owner: YA, LOCK PRE-ARCH
→ PRE-ARCH BASELINE — LOCKED FOR EXECUTION
→ capable reasoner / planner
→ DETAILED ACTION_PLAN ↔ PRE-ARCH
→ DETAILED ATOMIC TASK SLICING
→ EXECUTE ONE TASK
→ RESULT / EVIDENCE
→ PRE-ARCH REVIEW
   ├─ PASS → NEXT TASK
   ├─ REWORK → task/action plan
   ├─ ARCH FINDING → revise/supersede PRE-ARCH
   └─ LOCKED-DECISION IMPACT → STOP → OWNER
→ sufficient implementation evidence
→ FINAL ARCHITECTURE REVIEW
→ LAST ARCHITECTURE CHALLENGE
→ FINAL IMPROVE / REVISION
→ BUILD ARCHITECTURE
→ owner: YA, CONFIRM ARCHITECTURE
→ ARCHITECTURE CONFIRMED
→ rebuild release ACTION PLAN
→ release atomic tasks
→ BUILD FIRST RELEASE
→ integration / hardening / verification / acceptance
→ DELIVERED !!
~~~

ACTION_PLAN.md remains planning/execution authority only; it cannot decide or silently change architecture. Derived atomic task packets are execution views, never a second planning authority.


## v0.3.6 project semantic alignment note

The project baseline was aligned on 2026-10-01 from v0.3.2 to **v0.3.6**. Current project operation therefore also follows:
- the ZASS Convergence Loop principle;
- explicit `PROPOSED FOR PROCEED` approval sets;
- Architecture Readiness and qualitative Evidence Confidence as separate axes;
- the current Full-ZASS command surface `ZASS!! / PROCEED / PIVOT / COMMIT`; `PARKED` remains a state, not a Full-ZASS command.

Historical v0.3.2 migration notes above remain as provenance.

## ZASS SYSTEM UI/UX alignment — 2026-10-01

The official ZASS SYSTEM UI/UX contract is also active for this project. This is a presentation/product-surface alignment, not a new architecture decision and not a method-version bump.

**Applicable system rules:**
- **Present only the next meaningful human action.**
- Keep local ZASS tooling first-class; future AI-SYNC Web is a UX/automation/projection layer, not the authority layer.
- GitHub project files and Git history remain the engineering Source of Truth.
- Prefer progressive disclosure: hide internal IDs, full ledgers and validator codes during ordinary work unless review/audit requires them.
- Human-facing work should prefer a compact Project Pulse rather than exposing the whole lifecycle continuously.
- Contextual surfaces may include **Ready to Lock**, **Architecture Forming**, **Current Task**, **Delivered**, and escalation notice only when a human action is useful.
- ACTION_PLAN / ARCHITECTURE / TASKS may be projected into human-facing views, but the projections do not become authority.
- SAVE/sync status must be factual: authoritative persistence requires a real Git commit/receipt; generated Markdown alone is not SAVED.
- Future web presentation must reuse the same validator/core semantics rather than duplicate rule logic.
- Full ZASS remains an escalation/governance capability; no automatic migration or invented complexity score is permitted.

**Project-specific consequence:** ordinary chat/project updates should stay compact and action-oriented while preserving full lineage in the repository for review when needed.

---

# 21. RECOMMENDED PROJECT STRUCTURE

Before extraction, keep the repository deliberately small.

Current/near-term authority structure:

~~~
Kerani_Core_SuperBasic/
├── ZASS_Kerani_Core_SuperBasic.md    ← project SoT
├── ACTION_PLAN.md                    ← current execution plan only
├── docs/
│   └── DEV_WORKFLOW.md
└── README.md
~~~

When evidence justifies growth:

~~~
Kerani_Core_SuperBasic/
├── ZASS_Kerani_Core_SuperBasic.md
├── ACTION_PLAN.md                    ← optional; execution only
├── ARCHITECTURE.md                   ← only after architecture is built
├── README.md
├── src/
├── tests/
├── config/
└── docs/
    ├── DEV_WORKFLOW.md
    ├── EXTRACTION_LEDGER.md
    ├── adr/
    ├── experiments/
    └── reviews/
~~~

Do not create code, abstractions or folders merely to make the project look mature.

Authority hierarchy:

1. GitHub project ZASS file — project facts/decisions/readiness.
2. Official ZASS v0.3.6 — workflow semantics.
3. ACTION_PLAN.md — current execution/progress plan only; it does not decide architecture.
4. ARCHITECTURE.md — confirmed/draft architecture representation when applicable.
5. Local repository — working copy.
6. AI project workspace / memory / chat — context only.

---

# 22. STANDARD ZASS COMMANDS

This project inherits ZASS v0.3.6 command semantics.

- **ZASS / ZASS!!** — full structured exploration; do not change LOCKED decisions.
- **ZASS REVIEW** — challenge using a named method/perspective.
- **ACTION PLAN** — show/update execution state only; never LOCK a decision.
- **ZASS CHALLENGE** — attack assumptions, edge cases and contradictions.
- **ZASS DECIDE** — show unresolved candidate decisions and trade-offs.
- **PROCEED** — approve exactly the explicit `PROPOSED FOR PROCEED` set shown in the latest ZASS mapping. Unlisted items are excluded; proposals marked for LOCK become LOCKED. PROCEED does not commit or push.
- **COMMIT** — after approval, commit and push the approved project-file changes atomically and report the real commit SHA.
- **DRAFT ARCH** — prepare/revise a working architecture draft from authoritative state; does not confirm architecture.
- **BUILD ARCHITECTURE** — run the confirmation gate; if READY, request exact owner response **YA, CONFIRM ARCHITECTURE**.
- **ZASS AUDIT** — audit architecture against ZASS state.
- **ZASS IMPACT** — analyse impact before changing architecture.

When the user intentionally invokes ZASS or ZASS!!, check the project baseline against the latest official ZASS repository when access is available.

---

# APPENDIX A — CANDIDATE GENERIC SURFACE

This remains a candidate audit surface, not a build plan.

| Candidate surface | Evidence needed before extraction |
|---|---|
| Telegram adapter | Works without OpsMate-specific message or identity assumptions. |
| Apps Script runtime boundary | Portable deployment/configuration contract. |
| Gemini adapter | Domain-neutral prompt/input/output boundary and safe error handling. |
| Request pipeline | Reusable stages that do not encode farm or SME workflow. |
| Queue and worker | Generic state transitions and retry/review semantics. |
| Parser/normaliser | Input contract independent of an OpsMate record type. |
| Reply engine | Deterministic response contract and safe fallback replies. |
| Logging/evidence | Generic event schema with protected-data rules. |
| Configuration/secrets boundary | No credentials in source; app-specific settings separated. |
| Test harness | Reproducible tests without live Telegram production traffic. |

---

# APPENDIX B — EVIDENCE-LED EXTRACTION ROUTE

**State:** CANDIDATE strategy; not a final architecture.

Do not refactor OpsMate directly into Kerani. Treat OpsMate BSE as a proven reference implementation and test the route:

**OpsMate BSE → evidence baseline → actual behaviour map → reuse matrix → contracts → Core SuperBasic → Agro module → integration → reproduction test**

Target:

**proven behaviour → contracts → boundaries → tests → architecture → clean implementation**

## Four-way reuse matrix

| Classification | Meaning | Typical destination |
|---|---|---|
| GENERIC | Meaningful without farm/business domain. | Core candidate |
| AGRO-GENERIC | Reusable agriculture-domain behaviour across crops, aquaculture or livestock, not generic infrastructure. | Kerani Agro candidate |
| OPSMATE/BSE-SPECIFIC | Tied to BSE/site/plot convention/columns/history. | Config, reproduction fixture or PARK |
| UNCERTAIN | Evidence is insufficient. | Remain in reference implementation; create Q/R/E |

Quick heuristic: if removing the agriculture context leaves the behaviour meaningful, it may be a Core candidate. If its meaning depends on agriculture but not BSE, it may be an Agro candidate. This heuristic does not replace evidence.

## Contract questions

For every extraction candidate, define:
- accepted input and context;
- normalised/candidate output;
- validation/confidence/failure states;
- authority transition and required human approval;
- reply/audit event;
- behaviour tests that must remain stable.

## Candidate delivery sequence

This sequence is a candidate plan, not a LOCKED decision:

1. Freeze reference baseline.
2. Map actual behaviour.
3. Build reuse matrix.
4. Define behaviour contracts.
5. Extract and test Core SuperBasic alone.
6. Build Kerani Agro from AGRO-GENERIC findings.
7. Integrate Core + Agro + BSE test configuration + adapter.
8. Run E-006 OpsMate reproduction test.
9. Run ZASS review before any architecture boundary becomes DECIDED or LOCKED.

---

# DEFINITION OF DONE — PROOF STAGE

**OpsMate behaviour complete/stable enough for selected scope**  
→ **components classified with evidence**  
→ **generic components extracted**  
→ **relevant regression tests pass**  
→ **Core runs a non-farm module**  
→ **second independent use works**  
→ **no major core rewrite is required for reuse**  
→ **selected OpsMate behaviour is reproduced by the new composition**  
→ **public-release safety review passes**  
→ **generic core is proven enough to name/version publicly**

Until then, this remains an extraction proof project, not a framework claim.

---

# PROJECT ZASS CHANGELOG

## 2026-10-09 — Method baseline corrected to current ZASS SYSTEM / ZASSIMPLE

- Updated current-facing method truth to **ZASS SYSTEM v0.2.2 / Full ZASS v0.3.11 / ZASSIMPLE v0.3.3**.
- Kerani Core SuperBasic now operates primarily under ZASSIMPLE; retained Full ZASS records remain governance/evidence lineage and escalation material when stronger governance is materially required.
- Current technical execution semantics now include **Execution Reality Check**, real artifact/sample pack, execution-surface mapping, evidence-bounded vertical atomic tasks and delta planning/PRE-ARCH review.
- Historical snapshots embedded inside migrated planning history were intentionally not rewritten.
- No project D/L/Q/R/E/AC architecture/product decision was added, removed, superseded, confirmed or re-scored.
- ZERO → ARCHITECTURE remains 65% and Evidence Confidence remains LOW.


## 2026-10-09 — ZASSIMPLE current-design distillation committed

- Distilled current Full ZASS truth into `ZASSIMPLE/DESIGN.md` as a human-first project/design view.
- Design coverage is now 4/4: purpose, main flow, main elements and relevant LOCKED constraints are represented.
- Current architecture candidates remain candidates; no control-plane provider, Premium Pack or PRE-ARCH baseline was LOCKED by this distillation.
- Preserved current project state: 65% — DECIDING, Evidence Confidence LOW.
- Next design gate is Architecture Assumption + Boundary Challenge; this commit does not run that challenge.
- No D/L/Q/R/E/AC decision/evidence state was changed, superseded or re-scored.


## 2026-10-09 — ZASSIMPLE surface migration contract committed

- Owner-approved `ZASSIMPLE/MIGRATION_CONTRACT.md` v0.1 persisted using ZASSIMPLE v0.3.3 as the method baseline.
- Created `ZASSIMPLE/DESIGN.md`, `ZASSIMPLE/ACTION_PLAN.md`, and `ZASSIMPLE/TASKS.md`.
- Moved canonical planning location to `ZASSIMPLE/ACTION_PLAN.md` while preserving the complete pre-migration root Action Plan content.
- Converted root `ACTION_PLAN.md` to a compatibility pointer so two planning authorities cannot diverge.
- Full ZASS remains the governance/evidence/decision backplane; ZASSIMPLE is the human-facing design/planning/execution surface.
- No D/L/Q/R/E/AC architecture/product decision was added, removed, superseded, confirmed or re-scored by this migration.
- ZERO → ARCHITECTURE remains 65% and Evidence Confidence remains LOW.


## 2026-10-09 — Premium Intelligence + Cloudflare control-plane candidates

- Added I-016 and D-051 **CANDIDATE** for **Premium Intelligence Pack — Analysis · Correlation · Graph · Proposal · Forecast**.
- Preserved product ladder: Free Core basic record/retrieve/summary/report → Premium Operations automation/retrieval → Premium Intelligence higher-order reasoning/visualisation/forecasting.
- Added AC-010 **CANDIDATE — Cloudflare-First Lightweight Control Plane**.
- Updated E-016 from a two-way Cloud Run vs Apps Script comparison to a three-way benchmark: Apps Script vs Cloudflare Workers+D1 vs Cloud Run stack.
- Recorded the owner's current approximately RM200 Google Cloud billing/onboarding barrier as a practical account-side constraint only; it is not treated as a universal Cloud Run fee.
- Kept OpenClaw under D-032/E-013 as a replaceable synthetic reliability/audit agent, not a production control-plane competitor.
- Added Q-032 for Cloudflare feasibility and R-031 for free-tier/limit exhaustion risk.
- Added D-051-P and AC-010-P deferred parameters; provider limits/pricing must be reverified when implementation begins.
- No provider is LOCKED. ZERO → ARCHITECTURE remains 65%; E-016 must produce evidence before control-plane selection.


## 2026-10-09 — Premium Operations Pack candidates saved

- Added I-015 and D-050 **CANDIDATE** for **Premium Operations Pack — Alert · Remind · Report · Ask**.
- Candidate capabilities: P-01 IoT Alert Bridge, P-02 Task Reminder + Push Notification, P-03 Scheduled Report, P-04 Interactive Query/Retrieval.
- Preserved Free usefulness: basic Task, manual/basic reporting and deterministic/basic retrieval are not removed from Free by this candidate.
- Added R-030 safety boundary: critical IoT alarms retain a deterministic/local authoritative path; Kerani may add context, push, history and escalation.
- Added Q-031 for Free/Premium boundary and OpsMate reuse evidence.
- Exact pricing, quotas, cadence, delivery channel, IoT protocol and escalation policy remain deferred under D-050-P.
- No LOCKED decision or architecture-readiness score changed; this commit records product candidates and their evidence requirements.


## 2026-10-09 — Real-field-evidence-first execution LOCK

- LOCKED D-049 / L-042: real operator/customer samples become first-class execution evidence from the earliest available day.
- Locked **No sample, no assumption**: when no real sample exists, the behaviour is UNVALIDATED rather than field-proven.
- Added the Kerani execution bridge: field corpus → execution proof matrix → reusable test procedure → atomic task instance → proof receipt → invalidation check → PASS_REUSED or rerun.
- Added task evidence anchors: real evidence anchor, field sample IDs, expected behaviour contract, proof reuse key and invalidation triggers.
- Locked procedure-vs-case separation to reduce repeated execution prose/work while preserving observable acceptance criteria.
- Locked defect-to-corpus flow so real defects become durable regression assets.
- Added E-019 Evidence-Seeded Execution Pilot using one Purchase slice and an initial target of roughly 5–10 real field samples.
- Deferred any shared ZASS System execution-standard change until E-019 demonstrates reduced repetition without weaker reliability/traceability.
- ZERO → ARCHITECTURE remains 65% and Evidence Confidence remains LOW; the execution method is approved but not yet proven on Kerani.


## 2026-10-08 — V-Road / 7V Core + Extended V-Gates LOCK

- SUPERSEDED D-047 / L-040 historical 4V principle without deleting lineage.
- LOCKED D-048 / L-041: **V-Road — 7V Core + Extended V-Gates**.
- Canonical 7V Core: **Value → Verbal → Volume → Viral → Vary → Venture → Versatile**.
- Added Extended V-Gates for Vision, Vocabulary, Vibe, Veracity, Validation, Verification, Volition, Vault, Vulnerability, Velocity, Visibility, Viability, Vigilance, Versioning, Variability, Venue, Vendor-neutral, Value-chain and Vertical.
- Locked evidence discipline: **No V is free. Every V must be earned. Do not skip the Vs.**
- Defined **Vital** as operational importance earned through utility, and **V-King 👑** as the aspirational destination **“become needed, not merely known”**, not an eighth V or market-dominance claim.
- Added anti-shortcut rules so Viral/Volume/Venture/Versatile maturity cannot be claimed without supporting gates/evidence.
- Renamed deferred scale-parameter lineage from D-047-P to D-048-P.
- ZERO → ARCHITECTURE remains 65% and Evidence Confidence remains LOW; this is a governance/maturity-model refinement, not new empirical evidence.


## 2026-10-07 — Government bridge + partner-backed scale + 4V growth LOCK

- Owner PROCEED + COMMIT LOCKED D-035–D-047 / L-028–L-040.
- Locked optional Government Assistance & Impact Bridge principles: sponsor funding is separate from data authority; sharing is minimum-necessary/purpose-bound; agency remains eligibility/approval authority; outcome reporting cannot invent causality.
- Locked Pilot-to-Proof, just-enough viral-ready infrastructure, event-readiness, official public-sector collaboration boundary, replaceable strategic infrastructure partner, partner-credibility/endorsement boundary and evidence-led grant-readiness.
- Locked **4V — Value → Volume → Viral → Versatile**. Variable demand is treated as a scale condition managed through controls and replaceable partners, not as a fifth V.
- Added AC-008 Sponsor-Funded Assistance & Outcome Bridge and AC-009 Pilot → Viral Launch → Partner-Backed Scale as CANDIDATE architectures.
- Added E-017 mock Government Programme Bridge and E-018 viral/event-scale + partner-scale drill.
- Kept MAHA 2027, any named Jabatan/booth arrangement, named vendor, Petronas reference, commercial terms, specific grant and exact scale thresholds DEFERRED until real evidence/agreements exist.
- ZERO → ARCHITECTURE remains 65% and Evidence Confidence remains LOW; these locks clarify strategy/boundaries but do not add runtime or institutional evidence.


## 2026-10-07 — Footer sync to Full ZASS v0.3.10

- Corrected the project footer to the canonical Full ZASS v0.3.10 surface: `[🧠 ZASS!!]-[▶️ PROCEED]-[📦 COMMIT]`.
- Removed PIVOT from the footer only; the PIVOT command remains valid in the method.
- Updated the Evidence Confidence reason to cite actual current evidence and unresolved tests.
- Normalized the version-check line to `✅ METHOD BASELINE — ZASS SYSTEM v0.2.2 · Full ZASS v0.3.11 · ZASSIMPLE v0.3.3`.
- No decision, readiness score, experiment result or architecture state changed.


## 2026-10-07 — Full ZASS v0.3.10 / ZASS SYSTEM v0.2.1 sync + OCR/Cloud candidates

- Updated project method baseline from Full ZASS v0.3.6 to **v0.3.10** and ZASS SYSTEM to **v0.2.1**.
- Adopted governed architecture-to-execution flow: ARCHITECTURE CHALLENGE → controlled revision → LOCK PRE-ARCH → detailed ACTION_PLAN ↔ PRE-ARCH → atomic evidence tasks → PRE-ARCH review → LAST ARCHITECTURE CHALLENGE → explicit architecture confirmation → first-release plan/tasks → DELIVERED.
- Preserved ACTION_PLAN as execution/planning authority only; architecture/decision authority remains in ZASS + owner gates.
- Added I-013 / D-034 CANDIDATE / E-015: tiny hosted OCR allowance plus manual/personal-Gemini/Lens paste fallback through the same candidate/confirmation/validation boundary. 1–3/month remains a pilot parameter, not LOCKED.
- Added I-014 / AC-007 CANDIDATE / E-016: evaluate Cloud Run + Firestore + Secret Manager + basic Logging/Monitoring as the V1 central control plane while keeping Apps Script useful at the Google Workspace/customer edge.
- Added Q-023–Q-025 and R-020–R-022 for OCR economics/integrity and premature-cloud-complexity risk.
- ZERO → ARCHITECTURE remains 65% and Evidence Confidence remains LOW because these updates add governance/candidates, not new runtime evidence.

## 2026-10-07 — OpenClaw synthetic reliability experiment PROCEED

- Owner approved proceeding with the already LOCKED D-032/L-026 OpenClaw synthetic reliability direction.
- Expanded E-013 with a concrete synthetic coverage set, required reliability/cost metrics, PASS criteria and STOP/ESCALATE conditions.
- Kept OpenClaw replaceable and outside business-authority boundaries; synthetic traffic must use dedicated identities and never contaminate real customer truth or entitlements.
- Execution planning is delegated to ACTION_PLAN; no implementation or atomic coding task was started by this update.
- ZERO → ARCHITECTURE remains 65%; no new runtime evidence was produced.

## 2026-10-07 — Tenant/channel/quota + viral-capacity LOCK

- LOCKED D-023–D-033 / L-017–L-027: channel-independent tenant identity, low-friction Free onboarding, Telegram-vs-WhatsApp economics, shared-WA capacity/waitlist/reclaim, independent Free resource quotas, useful-action quota semantics, shared deterministic-first AI, tenant-isolated storage, Premium own-WhatsApp onboarding, OpenClaw reliability harness and POS/ERP growth path.
- 50 users per shared WhatsApp number remains a planning example, not an architecture invariant.
- Added AC-006, Q-018–Q-022, R-012–R-019 and E-007–E-014.
- ZERO → ARCHITECTURE moves from 63% to 65%; Evidence Confidence remains LOW pending pilot/load/isolation/migration evidence.

## 2026-10-06 — Premium demo + OpsMate-grade premium workflow LOCK

- Saved the broader product idea set as CANDIDATE ideas: simple free-product promise, three-layer value model, data-history-first, user-owned/export-for-AI direction, outcome-based crediting, limited premium killer features, micro-SME digital-upgrade positioning and the “large-system discipline made lightweight” thesis.
- LOCKED D-021/L-015: selected premium capabilities may occasionally be offered free as bounded demos/trials without changing their permanent premium classification.
- LOCKED D-022/L-016: OpsMate-grade validated operational workflows are premium/domain solutions, not generic Free Core features merely because some runtime mechanisms are reusable.
- LOCKED the right to require structured onboarding/interview, domain-contract configuration and onboarding cost for those complex workflows.
- Preserved extraction discipline: reusable mechanisms may feed Core, while organization/domain-specific operating rules remain outside generic Core unless independently proven generic.
- Added explicit future tests for premium-demo clarity/conversion and the minimum onboarding/interview contract.
- ZERO → ARCHITECTURE remains 63% and Evidence Confidence remains LOW; these are product-boundary decisions, not new architecture evidence.

## 2026-10-06 — Free-first product/growth principle LOCK

- LOCKED D-020/L-014: SuperBasic growth is built around a **free-but-genuinely-useful** product, not a crippled demo.
- LOCKED the messaging boundary: free/basic solves real record-keeping and basic retrieval needs; premium/credit adds higher-order intelligence, domain capability and automation.
- LOCKED explicit premium communication: gated features must explain additional value/cost rather than disappear or fail opaquely.
- LOCKED evidence-led growth: major public push follows pilot evidence and authentic user feedback/testimonials.
- Added R-011 for manipulative/confusing free-premium boundaries and over-promised outcome claims.
- Deferred exact viral campaign, platform mix, Marketplace tactics, ad spend, copy variants, launch timing and KPI targets until post-pilot review.
- ZERO → ARCHITECTURE remains 63% and Evidence Confidence remains LOW; this is a product/growth principle, not runtime architecture evidence.

## 2026-10-06 — Free Core + Credit Pass product model LOCK

- LOCKED D-016/L-011: Free Core must remain useful standalone for basic records, receipt capture where available, basic retrieval/reporting and operational-log summary; higher-order intelligence/forecasting/domain automation may be premium.
- LOCKED explicit premium-gate UX: gated requests must explain the premium capability rather than silently failing or returning an unrelated error.
- LOCKED D-017/L-012: primary paid direction is Credit Pass / pay-per-capability rather than mandatory recurring subscription; credit cost is shown before charged execution.
- LOCKED failed-delivery guardrail: provider/system failure is not treated as a successfully delivered paid capability.
- LOCKED D-018/L-013: user data stays accessible/exportable and artificial data lock-in is not the business model.
- DEFERRED D-019: exact values such as 5/10/20/100 credits, module allowance/onboarding pricing and credit economics require measured unit economics.
- Added a post-architecture dependency: cross-audit SuperBasic against prior Kerani Core work and adopt only lightweight/generic/maintainable capabilities.
- ZERO → ARCHITECTURE remains 63% and Evidence Confidence remains LOW; these product decisions do not substitute for runtime evidence.

## 2026-10-01 — ZASS SYSTEM UI/UX contract sync

- Synced the project with the official locked ZASS SYSTEM UI/UX contract without changing Full ZASS v0.3.6 method semantics.
- Adopted the primary UX rule: **Present only the next meaningful human action.**
- Added progressive-disclosure guidance, compact Project Pulse, contextual action cards, factual Git-backed SAVE receipts and artifact projection semantics.
- Recorded the system split: local first-class tooling remains independently usable while future AI-SYNC Web is the UX/automation/projection layer over the same authority.
- Kept GitHub as engineering Source of Truth and prohibited duplicate validator semantics in future web presentation.
- No LOCKED project decision, architecture candidate, readiness score or Evidence Confidence value changed.

## 2026-10-01 — Minimum constrained natural-language intake LOCK

- LOCKED D-015/L-010: SuperBasic includes minimum constrained natural-language intake.
- AI authority is limited to intent suggestion, candidate extraction and confidence/ambiguity signalling.
- Ambiguous or low-confidence input must trigger category selection/clarification rather than guessing.
- AI-interpreted mutations require candidate preview, explicit human confirmation and deterministic Core/domain validation before authoritative persistence.
- Preserved D-013/L-008: rich/open-ended natural-language conversation remains Kerani AI Premium.
- Added R-010 for overconfident natural-language routing.
- Refined AC-005 only as a candidate to acknowledge an intent-suggestion stage without locking router ownership.
- ZASS baseline remains v0.3.6; ZERO → ARCHITECTURE remains 63% and Evidence Confidence remains LOW because no new runtime validation evidence was added.

## 2026-10-01 — SuperBasic product scope LOCK + ZASS v0.3.6 alignment

- LOCKED D-010/L-005: five generic record families — Purchase, Sale, Inventory, Observation and Task — with receipt capture as an input capability and no dedicated self-hosted-server requirement.
- LOCKED D-011/L-006: exactly three planned domain modules — Agro, Servis Teknikal and Makanan & Tempahan; Agro replaces the narrower reusable-domain name Kebun.
- LOCKED D-012/L-007: no additional domain modules in current SuperBasic scope; module simplicity and anti-spaghetti are explicit stop rules.
- LOCKED D-013/L-008: full natural-language conversation is Kerani AI Premium and must not be required for basic SuperBasic operation.
- LOCKED D-014/L-009: OpsMate remains the primary evidence source; reusable mechanisms feed Core, agriculture behaviour feeds Agro, and BSE-specific assumptions remain outside generic Core.
- Updated the project method baseline from ZASS v0.3.2 to v0.3.6 semantics.
- Added Evidence Confidence = LOW while ZERO → ARCHITECTURE remains 63% — DECIDING.
- No architecture candidate was promoted or confirmed.

## 2026-09-29 — Near-term evidence-harvesting plan

- Approved a time-boxed execution plan around an OpsMate reference freeze targeted for 10 October 2026.
- Pilot outcomes are to be captured as bug/gap/requirement evidence rather than automatically expanding the frozen reference scope.
- Set 10–15 October 2026 as an evidence-harvesting window: freeze metadata, pilot findings, 3–5 behaviour maps, reuse matrix, candidate contracts and minimal repository skeleton preparation.
- Added `ACTION_PLAN.md` as the execution authority for this window.
- Substantive Kerani_Core_SuperBasic implementation is PARKED after the review until the owner explicitly restarts the build with suitable local agentic-coding resources.
- This planning change does not alter LOCKED decisions and does not increase ZERO → ARCHITECTURE readiness; it remains 63%.

## 2026-09-29 — Runtime verification / E-001B

- Verified Behaviour Map #1 against OpsMate TEST main at `a6b504aff254935023ea19d6a1ce90dff597deb2`.
- Corrected the runtime parser path: ordinary report processing uses `bseUnifiedProcess_()` → Gemini → `bseUnifiedGuard_()` → domain validation, not `bseInventoryParseMessage_()` as the primary worker parser.
- Added Q-015, Q-016 and Q-017.
- Added R-009 for linear-pipeline over-generalisation.
- Refined AC-005 to distinguish direct/read and stateful/mutation paths while keeping it `CANDIDATE`.
- Kept D-007, D-008 and D-009 at `TESTING`; no LOCKED decision changed.
- ZERO → ARCHITECTURE remains 63%.

## 2026-09-29 — Behaviour Map #1 / E-001A

- Recorded the first evidence-backed workflow map using OpsMate TEST commit `10e20cd601421bb114ff3bfd7edf9e3f5e8160c4`.
- Added E-001A for Input Usage / Inventory.
- Moved D-007, D-008 and D-009 from `CANDIDATE` to `TESTING`.
- Kept D-006 as `CANDIDATE` and parent E-001 incomplete.
- Updated open loops and readiness wording; ZERO → ARCHITECTURE remains 63% because one workflow slice does not close the major architecture blockers.
- No LOCKED decision changed.

---

# CURRENT ZASS FOOTER STATE

[🧠 ZASS!!]-[▶️ PROCEED]-[📦 COMMIT]

🏗️ ZERO → ARCHITECTURE: [███████░░░] 65% — DECIDING
🔬 EVIDENCE CONFIDENCE: LOW — one OpsMate workflow has direct runtime verification; the new real-field-evidence execution bridge and most later V-Road stages remain unproven on Kerani.

✅ ZASS UP TO DATE — v0.3.10
