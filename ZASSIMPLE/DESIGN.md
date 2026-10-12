# ZASSIMPLE DESIGN — Kerani Core SuperBasic

**Status:** DRAFT READY FOR CHALLENGE  
**Design Progress:** 4/4 — purpose / main flow / main elements / relevant LOCKED decisions  
**Authority:** Current ZASSIMPLE design surface. It must preserve existing LOCKED project lineage and verified evidence; Full ZASS is retained for governance/history and escalation when materially required.

**Project state:** 65% — DECIDING  
**Evidence confidence:** LOW  
**Pre-confirmation challenge:** NOT RUN  
**Challenge count:** 0  
**Architecture impact of this distillation:** NONE  
**Execution baseline:** NOT LOCKED  
**PRE-ARCH version/reference:** none

> **Show the project, not the repository.**

This file distils retained project truth into the current ZASSIMPLE human-facing design view. It does **not** add, remove, confirm, supersede or re-score any architecture/product decision.

**Method baseline:** ZASS SYSTEM v0.2.2 · ZASSIMPLE v0.3.3 · Full ZASS v0.3.11 (escalation/governance when required).

## Purpose

Kerani Core SuperBasic is a deliberately small generic micro-SME core that should remain useful on its own for basic operational record keeping.

Its Free baseline centres on:
- Purchase;
- Sale;
- Inventory;
- Observation;
- Task;
- receipt capture/input where available;
- basic retrieval, summaries and reports.

The product should stay lightweight, affordable and portable. Domain depth, richer automation and higher-order intelligence sit outside the generic Free Core rather than turning Core into a large special-case system.

**OWNER LOCKED — D-055/L-046 (2026-10-12):** Free Core must stay independently useful even if all AI services fail or quota is exhausted. **AI is optional convenience, never the prerequisite for basic operation.** The deterministic business/authorization/validation path is always authoritative; fallback routing details are not architecture-locked.

## Main flow

### Locked user-facing record flow

1. User interacts through a supported channel.
2. Channel resolves to a persistent Kerani tenant identity.
3. For short operational free text, Kerani may suggest intent/category and extract a structured candidate.
4. Ambiguous input must trigger clarification rather than silent guessing.
5. The user reviews the candidate and may confirm, correct or cancel.
6. Deterministic/domain validation runs before an AI-interpreted mutation becomes authoritative.
7. Authoritative records can then be retrieved, summarised and reported.
8. When a request crosses the Free boundary, Kerani should clearly surface the relevant Premium capability rather than silently failing.

### Candidate runtime shape — not LOCKED

The current runtime candidate separates direct/read work from stateful/mutation work, with channel adaptation before business logic and a Core ↔ Domain Module boundary.

Whether routing ownership, Durable Inbox usage and confirmation responsibility belong universally in Core remains unresolved.

**Lineage:** D-015 · AC-005 · Q-015 · Q-016 · Q-017

## Main elements

| Layer | Current distilled truth |
|---|---|
| **Experience** | WhatsApp, Telegram and future interfaces are channels/bindings, not the identity of Kerani or the tenant. |
| **Identity & data** | One persistent tenant identity; tenant-isolated history; channel migration without data migration; user export rights preserved. |
| **Free Core** | Purchase · Sale · Inventory · Observation · Task · receipt input · basic retrieval · basic summaries/reports. |
| **Domain modules** | Exactly three planned modules: Agro · Servis Teknikal · Makanan & Tempahan. |
| **Premium domain solution** | OpsMate-grade validated operational workflows may require structured onboarding, domain contracts and controlled validation/persistence. |
| **Premium Operations — CANDIDATE** | Alert · Remind · Report · Ask. |
| **Premium Intelligence — CANDIDATE** | Analysis · Correlation · Graph · Proposal · Forecast. |
| **AI boundary** | Deterministic-first where AI adds no value; constrained natural-language convenience may exist in Free; rich/open-ended conversation remains Premium. |
| **Free channels** | Telegram is the economic/high-usage Free channel; shared WhatsApp is a controlled convenience/discovery channel. |
| **Premium channel path** | Dedicated/owned WhatsApp and optional customer-owned Google/Apps Script/AI may be configured later without changing tenant identity. |
| **Reliability** | OpenClaw is a replaceable external synthetic reliability/audit harness, not Kerani business authority or the production control plane. |
| **IoT safety boundary** | Kerani may add context, history, notification and escalation; a critical device/PLC/HA alarm must not depend solely on Kerani/LLM/cloud. |
| **POS / ERP growth** | Future adapter/contract path; established ERP-owned records remain authoritative in the ERP. |
| **Government/programme bridge** | Optional; sponsor funding does not grant blanket data authority; agency/programme remains authority for eligibility/approval/status. |
| **Growth model** | Evidence-first, low-cost-at-low-usage, controlled scale, replaceable partners, V-Road maturity. |

## Product ladder

| Layer | What the user gets |
|---|---|
| **Free Core** | Record · retrieve · basic summary/report |
| **Premium Operations — CANDIDATE** | Alert · Remind · Scheduled Report · Interactive Ask/Retrieval |
| **Premium Intelligence — CANDIDATE** | Analysis · Correlation · Graph · Proposal · Forecast |
| **Premium Domain Solution** | OpsMate-grade validated workflows with structured onboarding/domain rules |

Exact Credit Pass values, quotas, bundle design and premium capability pricing remain deferred.

## Current architecture candidates

### Runtime / module boundary

**AC-005 — CANDIDATE**

Current evidence supports testing an explicit channel boundary, request routing, generic Core orchestration and separate Domain Module contracts. Direct/read and stateful/mutation paths may differ.

Still unresolved:
- who owns request routing;
- which requests truly need a Durable Inbox;
- whether human confirmation is universally Core-owned or policy/module-owned.

### Tenant-centric hosted-Free → owned-Premium

**AC-006 — CANDIDATE**

Tenant identity and history remain independent from channel/provider choices. Shared Free infrastructure may later transition to owned/dedicated Premium infrastructure without tenant/data migration.

### Agentic Tool Boundary — CANDIDATE

**AC-012 — Bounded Agent Tool Orchestration**

Kerani may use AI as a bounded language-to-tool orchestrator, but **GENERIC behaviour does not automatically become an agent-callable tool, and an agent-callable tool does not automatically receive mutation authority**.

Candidate authority classes:

| Authority class | Candidate examples | Agent role | Required gate |
|---|---|---|---|
| **READ** | `retrieve_history`, retrieve status/report | Interpret natural-language request into tenant-scoped query parameters | deterministic tenant/query scope; no mutation |
| **PROPOSE** | `prepare_candidate` | Convert short operational language into structured candidate + confidence/missing fields | preview/clarification; no authoritative write |
| **CLARIFY** | ask missing field / disambiguate intent | Ask bounded follow-up question | no mutation; preserve original evidence |
| **VALIDATE** | deterministic/domain validator | Invoke/check rule boundary | validator remains authoritative for rules |
| **MUTATE** | commit/update/delete authoritative record | Agent must not receive free mutation authority | explicit human confirmation + deterministic/domain validation + audit/idempotency |
| **SYSTEM / AUTOMATION** | scheduled reminder/report | Invoke only pre-authorised bounded automation | entitlement + tenant scope + audit/failure receipt |

Two priority candidates for challenge:
- **`retrieve_history` — READ candidate:** natural-language history/status questions may map to deterministic tenant-scoped retrieval instead of requiring rigid commands such as `/retrieve_status <plot>`.
- **`prepare_candidate` — PROPOSE candidate:** natural-language operational reports may become structured candidates for clarification/preview before any authoritative mutation.

Candidate flow:

~~~text
natural-language input
        ↓
bounded language/tool router
        ↓
tool registry + authority metadata
   ┌──────────┬──────────┬──────────┐
   ↓          ↓          ↓
 READ       PROPOSE    CLARIFY
   │          │          │
   └──────────┴────┬─────┘
                   ↓
         human confirmation where required
                   ↓
        deterministic/domain validation
                   ↓
          controlled MUTATION
~~~

This remains **CANDIDATE** until challenged against real OpsMate behaviour, D-015 human-authority rules, tenant isolation, latency/cost and real-language variability.

**Additional challenge inputs — SAVED, not LOCKED:**
- **Durable Ingress / Idempotency Boundary:** determine which request classes require durable inbox/queue semantics and idempotency, and which READ paths should bypass queueing to preserve responsiveness. Do **not** assume every request must traverse a queue.
- **Authorization / Scope Guard:** tenant identity resolution is not sufficient on its own; challenge must prove authorization/scope enforcement before tool execution and again at the tool/data boundary. AI-supplied arguments must not be trusted to define tenant authority.

**Talorys / Free cloud evidence (2026-10-12) — SAVED, not architecture proof:** `../docs/TALORYS_CLOUDFLARE_GOOGLE_FALLBACK_EVIDENCE.md` compares Cloudflare Free vs Google Free, records Talorys' single-user Pages/Worker/Durable Object SQLite/Workers AI design (which **does not use D1/Queues**), and defines separable no-AI core, bounded AI interpretation, model failover and degraded-manual experiments. Its 80–90% no-AI routine-operation coverage is **hypothesis**, not verified field-message bypass. AC-012 remains CANDIDATE.

**Supporting comparison notes:**
- `../docs/OPSMATE_VS_KERANI_AGENTIC_TOOL.md` — visual/data-flow comparison of OpsMate workflow-centric behaviour versus the candidate Kerani bounded Agentic Tool architecture.
- `../docs/GAS_AGENTIC_PATTERN_AUDIT.md` — public implementation-pattern audit of `adk-gas`, `GeminiWithFiles` and `GeminiApp`, including the **Central Control Plane vs Customer-Owned Apps Script Edge** distinction.

Both notes are supporting evidence/analysis only; neither LOCKS AC-012 nor runs Challenge Design.

### V1 control-plane candidates

No provider is selected or LOCKED.

| Option | Current role |
|---|---|
| **Central Apps Script** | Simplicity baseline for E-016; must be evaluated separately from any customer-owned Apps Script edge role |
| **Cloudflare Workers + D1** | AC-010 lightweight low-entry-cost serverless candidate |
| **Cloud Run + Firestore + Secret Manager + basic Monitoring** | AC-007 scalable managed-serverless candidate |
| **OCI Ampere A1 Always Free VM** | AC-011 low-cost always-on VM candidate with direct queue/retry/runtime control |

**E-016** must compare setup/maintenance burden, entry/billing friction, webhook behaviour, latency/concurrency, tenant/quota/waitlist handling, secrets, scheduling/async needs, observability, failure recovery, low-traffic economics, scale-up and migration/rollback.

**New evidence input, not a winner:** Use `../docs/TALORYS_CLOUDFLARE_GOOGLE_FALLBACK_EVIDENCE.md` for a dated Cloudflare Free vs Google Free quota/AI/privacy baseline and separately test provider failure (429/5xx/timeout), AI-free core completion, explicit user clarification, and one budgeted alternate-AI recovery path. Talorys proves a bounded personal-agent pattern exists, **not** that Cloudflare Workers+D1 meets Kerani multi-tenant requirements. All four control-plane options remain in E-016.

For AC-011, current Oracle documentation checked 2026-10-11 reports 1,500 OCPU-hours + 9,000 GB-hours/month of Ampere A1 Always Free usage, equivalent to approximately 2 OCPUs + 12 GB memory for an Always Free tenancy within the allowance. The benchmark must also treat idle-instance reclamation and free-shape capacity availability as real reliability risks rather than assuming “free forever” equals guaranteed uptime.

### Response-time + language-variability viability signals

- **REPORTED field signal:** OpsMate can feel stuck after transient Gemini/provider failures because retry/poll scheduling adds a large visible wait. The owner recalls an approximately 30-second retry/poll interval in the experienced path.
- **VERIFIED source contrast:** accessible OpsMate worker snapshots currently show a 60-second base exponential retry for API_OR_OUTPUT_ERROR; therefore exact retry timing is unresolved and must be measured rather than assumed.
- **OPEN architecture question:** deterministic-first can only be a genuine fast path if it handles enough real short operational language without fragile keyword explosion or unsafe misrouting.
- **Product viability implication:** SuperBasic must prove both acceptable response time and bounded cost per useful action. Moving runtimes alone does not solve AI inference/retry latency.

E-016 must therefore measure latency by stage, including retry/backoff time after provider 5xx errors, and must measure deterministic fast-path coverage / misroute / clarification / AI-fallback rates over real field language samples.

The owner's current approximately RM200 Google Cloud billing/onboarding barrier is a practical account-side constraint only; it is not treated as a universal Cloud Run fee.

### Programme and scale candidates

- **AC-008 — CANDIDATE:** sponsor-funded assistance/outcome bridge with user-controlled/minimum-necessary data sharing.
- **AC-009 — CANDIDATE:** pilot → proof → just-enough infrastructure → event/viral readiness → replaceable partner-backed scale.
- Named event, agency, vendor, client-reference and grant details remain external/deferred until real evidence/approval exists.

## Constraints from LOCKED decisions

The design must preserve these boundaries:

- **Free must remain genuinely useful — D-055/L-046 explicitly LOCKED.** Basic Core operation must not require AI; deterministic execution and a usable no-AI input/retrieval path stay available under model outage/quota exhaustion. Premium adds higher-order intelligence, domain capability, automation and convenience rather than blocking basic access.
- **Genericity is earned.** OpsMate supplies evidence; reusable mechanisms may feed Core, agriculture behaviour may feed Agro, and BSE-specific rules stay outside generic Core.
- **Human authority remains explicit.** AI-interpreted mutations require review/confirmation and deterministic/domain validation before authoritative write.
- **No artificial data lock-in.** Users may access/export their own data.
- **Tenant identity is channel-independent.** Moving between WhatsApp, Telegram or future channels must not require a new tenant/history.
- **Quotas are independent.** Transport, storage/media, AI/processing, report/retrieval fair-use and Premium credits are separate controls.
- **Deterministic-first Free processing.** Free onboarding does not require BYO Gemini.
- **OpenClaw is not business authority.** Synthetic monitoring must not bypass normal controls or contaminate customer truth.
- **Critical IoT alarm path stays local/deterministic.** Kerani may augment it, not become the sole safety dependency.
- **Sponsor ≠ data authority.** Programme sharing is minimum-necessary and purpose-bound; agency remains programme authority.
- **Growth must be evidence-led.** Pilot proof precedes public-scale claims; viral readiness requires load, cost, reliability, fallback and observability evidence.
- **Infrastructure/partners must remain replaceable.** Core, tenant identity, portability and business authority cannot be surrendered to one provider/partner.
- **Real field evidence comes early.** When real samples exist they are first-class execution evidence; missing real samples must be marked UNVALIDATED rather than field-proven.
- **V-Road applies:** Value → Verbal → Volume → Viral → Vary → Venture → Versatile. Every V must be earned through evidence.
- **Latency Observability from Day 1 — LOCKED.** Every implemented request path must emit enough timing evidence to decompose user-visible latency by stage from ingress to reply. At minimum capture request start, queue wait where applicable, AI/tool-router time where applicable, tool execution, validation/storage, retry count + retry-wait, and total response time. Aggregate at least P50/P95/P99 plus error/retry rate, segmented by tool/channel/runtime/provider where meaningful. Instrumentation begins with the first executable slice; do not wait until the system feels slow.
- **Convenience-first UX — LOCKED.** User value is prioritized over ownership complexity. Onboarding friction, time-to-value, top-up continuity, latency/accuracy/trust and desired-channel fit are first-order design concerns. Premium features must arise from observed demand rather than being forced into the current Core architecture.

## Open assumptions / unresolved boundaries

These remain open; this design projection does not resolve them:

1. **Routing ownership** between direct/read and stateful/mutation paths — Q-015.
2. **Durable Inbox scope** — Q-016.
3. **Confirmation ownership**: Core-mandatory vs optional capability vs module/application policy — Q-017.
4. **Minimum Core ↔ Module contract**.
5. **Generic validation vs domain validation boundary**.
6. **Provider/parser substitution** behind a stable behaviour contract.
7. **V1 control-plane selection** — E-016; Apps Script vs Cloudflare vs Cloud Run.
8. **Exact Free quotas / shared-WA limits / OCR allowance** — pilot-calibrated.
9. **Premium Operations Pack** — candidate only; needs OpsMate/reuse/cost/safety evidence.
10. **Premium Intelligence Pack** — candidate only; needs real-data usefulness, uncertainty/error and unit-economics evidence.
11. **Government-programme bridge / event-scale / partner-scale** — planned experiments/evidence still incomplete.
12. **Response-time root cause + retry policy** — Q-033/R-032; exact experienced 30-second cadence is reported, while accessible worker snapshots show 60-second base exponential retry.
13. **Deterministic language coverage** — Q-034/R-033; must be proven against real multi-user phrasing rather than assumed from keyword rules.
14. **Agentic Tool Boundary** — Q-035/R-034/AC-012; challenge must distinguish GENERIC behaviour → tool-worthiness → authority class → required human/deterministic gate. Priority candidates: `retrieve_history` as READ and `prepare_candidate` as PROPOSE.

## Evidence posture

Current confidence remains **LOW**.

What is materially stronger:
- one OpsMate workflow has direct runtime verification;
- locked product/tenant/channel/data/authority boundaries are coherent;
- real-field-evidence-first execution method is approved.

What is still not proven enough:
- **final User Value Gate / Definition of Delivery (D-053):** measured latency, routing trust, tenant isolation, queue-boundary fitness and sustainable control-plane operations;
- generic Core extraction across multiple workflows/domains;
- non-farm reuse;
- quota/isolation/migration behaviour at scale;
- V1 control-plane winner;
- Premium Operations/Intelligence reuse/economics;
- viral/event-scale behaviour;
- partner/programme operational evidence;
- OpenClaw end-to-end reliability on real Kerani ingress.

## Challenge gate

Design coverage is now **4/4**, so the next design gate is challenge, not confirmation.

**Recommended challenge:** Architecture Assumption + Boundary Challenge.

**Mandatory challenge dimensions:**
1. runtime/module and routing ownership;
2. response-time/retry + dynamic-language viability, with the LOCKED Day-1 latency telemetry requirement treated as a non-negotiable execution constraint;
3. V1 control-plane selection evidence for the current multi-user Kerani Core. The previously explored **customer-owned Apps Script edge** is now FUTURE WORK for a separate Premium ZERO → ARCHITECTURE project and must not influence the current control-plane winner;
4. **Agentic Tool Boundary:** GENERIC behaviour ≠ automatically AGENT_TOOL; classify candidate tools as READ / PROPOSE / CLARIFY / VALIDATE / MUTATE / SYSTEM, and prove the human/deterministic gate for each authority level. This dimension must also test **Durable Ingress / Idempotency scope**, **Authorization / Scope Guard enforcement**, **user-owned Google Drive OAuth feasibility**, and **robust/responsive AI API failure fallback**, without pre-deciding that every request uses a queue or a specific fallback provider.

**Why:** the product/design surface is coherent, but several material architecture boundaries, agent/tool authority boundaries and the V1 control-plane choice remain candidates.

A challenge PASS does not automatically confirm final architecture. For this technical project it should lead toward a reviewed PRE-ARCH candidate and explicit owner gate when the evidence is sufficient. After PRE-ARCH lock, run Execution Reality Check before detailed task slicing, using real artifacts/samples and execution-surface mapping before evidence-bounded vertical atomic tasks.

## Final challenge lineage

Not run.

## Challenge / revision lineage

None yet.

Do not silently revise a LOCKED decision. Material architecture findings must return to governed review.

## PRE-ARCH execution baseline

- **Status:** NOT LOCKED
- **Baseline version/reference:** none
- **Challenge summary:** not run
- **Owner approval:** none
- **Evidence still required before final confirmation:** tracked by the current ZASSIMPLE design/action-plan evidence state, with retained project lineage consulted when needed
- **Supersedes / superseded by:** none

## Lineage

Human-facing compact lineage only:

- **Core/product:** D-010–D-022
- **Tenant/channel/quota/reliability:** D-023–D-033
- **Programme/growth/partner:** D-035–D-049
- **Observability requirement:** D-052 / L-043
- **Delivery Value Gate:** D-053 / L-044
- **Convenience-first UX / evidence-led Premium:** D-054 / L-045
- **Premium candidates:** D-050 · D-051
- **Architecture candidates:** AC-005–AC-012
- **Current control-plane evidence gate:** E-016
- **Retained Full ZASS lineage / escalation reference:** `../ZASS_Kerani_Core_SuperBasic.md`
- **Method baseline:** ZASS SYSTEM v0.2.2 · ZASSIMPLE v0.3.3 · Full ZASS v0.3.11
- **Migration contract:** `MIGRATION_CONTRACT.md`
