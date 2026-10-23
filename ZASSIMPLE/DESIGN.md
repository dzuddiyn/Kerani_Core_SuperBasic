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

### Free Chat-First & user-created group — OWNER LOCKED D-061/L-049 (2026-10-23)

**Free first user journey:** Begin with a 1-to-1 personal Telegram chatbot, not a supervised employee-group application or mandatory Mini App form. Business/company name is required at onboarding; backend assigns immutable Business ID and User ID with verified Telegram/user-to-tenant binding. Joining an existing Business ID requires a trusted invitation/verification path; a visible ID or membership in a group is not authorization.

**Multiple active Free users in one business:** Show a bounded warning that independent reports may overlap, with tips for users to create their own Telegram group, invite the bot and explicitly address it. Do **not** scan/correlate separate workers' record content with AI, automatically dedup human-originated reports, or introduce Owner/Admin/Worker organizational roles into Free. The same Telegram update/retry must still have inexpensive transport idempotency; ordinary business validation is retained.

**User-created group (not Kerani group administration):** Preferred `@KeraniBot rekod ...` and `@KeraniBot jana report ...` are **UNTESTED with default Privacy Mode ON**; official Telegram Bot FAQ only guarantees directed slash commands and replies. If plain mention fails, choose `/rekod@KeraniBot` / `/report@KeraniBot` (command auto-sends) → bot `ForceReply` prompt → user answers normally. Match replies by group, trusted user and prompt ID; authorize READ/MUTATE and show honest receipts. Do not quietly disable Privacy Mode or grant bot admin rights. Inline Mode draft/prefill is a distinct experiment, not the same plain-message route.

**Required T01–T06 acceptance remains PENDING** (mention privacy ON/OFF, slash auto-send, ForceReply, two-worker reply routing, inline prefill comparative UX). Product direction is LOCKED; syntax choice, phone UX, group setup and all runtime claims await actual controlled test. **D-057/L-047 Mini App is still first-class deterministic Free UI**, but it is not required during the initial chat flow or a mandatory first-launch blocker. Premium coordinated-team workflows are future candidates, not Free obligations.

**Lineage:** `../docs/KERANI_FREE_CHAT_GROUP_UX_D061.md`, master D-061/L-049; KAI-9.

### Telegram dual-surface UX — OWNER LOCKED D-057/L-047 (provider/implementation NOT LOCKED)

- **Telegram Chat:** language-first interface; bounded AI assistance when useful, with the candidate AI-first free-text route in D-056.
- **Telegram Mini App:** structured forms, history, receipt input and basic summaries through a **thin UI**; a normal self-service deterministic route, not merely an AI-error screen.
- **Common backend:** both share the same tenant/session trust, protected business API, data integrity/validation, confirmation where applicable, idempotency/audit and authoritative records; no business-rule duplication in JavaScript or direct front-end data authority.
- **Hybrid active fallback:** when AI is unavailable or slow, offer a usable structured continuation, including Mini App or smaller Telegram menu/wizard where appropriate. Mini App remains accessible proactively while AI is healthy.
- **Security:** validate Telegram WebApp `initData` signature/expiry at backend, then enforce tenant scope and permissions on each API action; never accept `initDataUnsafe` or client tenant claims as authoritative.
- **Evidence candidates, not locked screens:** simple record, review/history, receipt input, summary; a single **Rekod Aktiviti Kebun** form may be tested after Agro demo extraction. Menu button before evaluating `/newapp`; Cloudflare Pages Free as only a hosting candidate. No cross-product generic Mini App shell until a second proven use.
- **Sequencing:** OpsMate PILOT_REAL closeout → separate clean Agro Demo baseline → optional small Mini App slice only if it will not delay Wan/Hamidun demo. No PRE-ARCH lock/implementation authorization implied.

**Lineage:** D-057/L-047; D-055/L-046; D-056 (candidate); Q-039/R-038; E-016; `../ZASS_Kerani_Core_SuperBasic.md`.

### Candidate runtime shape — not LOCKED

The current runtime candidate separates direct/read work from stateful/mutation work, with channel adaptation before business logic and a Core ↔ Domain Module boundary.

Whether routing ownership, Durable Inbox usage and confirmation responsibility belong universally in Core remains unresolved.

**Lineage:** D-015 · AC-005 · Q-015 · Q-016 · Q-017

## Main elements

| Layer | Current distilled truth |
|---|---|
| **Experience** | **D-061/L-049 LOCKED:** Free personal Telegram chatbot first, with user-created group coordination *optional/UX untested*. **D-057/L-047 LOCKED:** first-class deterministic Free Mini App as a separate optional UI that follows chat launch sequencing, not a required form. WhatsApp and future interfaces are presentation/channel bindings only. |
| **Identity & data** | Required business name, backend-assigned Business ID + User ID, verified membership and Telegram binding for Free (D-061/L-049); persistent tenant identity, tenant isolation, channel migration without data migration and export rights preserved. |
| **Free Core** | Purchase · Sale · Inventory · Observation · Task · receipt input · basic retrieval · basic summaries/reports. |
| **Domain modules** | Exactly three planned modules: Agro · Servis Teknikal · Makanan & Tempahan. |
| **Premium domain solution** | OpsMate-grade validated operational workflows may require structured onboarding, domain contracts and controlled validation/persistence. |
| **Premium Operations — CANDIDATE** | Alert · Remind · Report · Ask. |
| **Premium Intelligence — CANDIDATE** | Analysis · Correlation · Graph · Proposal · Forecast. |
| **Premium Business Workspace — CANDIDATE D-059** | Tenant-specific Telegram summary → interactive Web UI dashboard; source-grounded charts, tables/search and optional future forecast/PWA/Drive links/task-sync. **Not LOCKED, implemented, entitled or architecture-selected.** See `../docs/KERANI_PREMIUM_BUSINESS_WORKSPACE_CANDIDATE.md`. |
| **AI boundary** | **D-056 owner-selected CHALLENGE DIRECTION (not PRE-ARCH):** AI-first for ordinary free-text messages; deterministic first for explicit menu/form/structured requests; hybrid active AI/provider and no-AI UX fallback through structured surfaces including the D-057 LOCKED Mini App. Deterministic business validation/authority always active. Free remains usable without AI; rich/open-ended conversation remains Premium. |
| **Free channels** | Telegram is the economic/high-usage Free channel; shared WhatsApp is a controlled convenience/discovery channel. |
| **Premium channel path** | Dedicated/owned WhatsApp and optional customer-owned Google/Apps Script/AI may be configured later without changing tenant identity. |
| **Reliability** | OpenClaw is a replaceable external synthetic reliability/audit harness, not Kerani business authority or the production control plane. |
| **IoT safety boundary** | Kerani may add context, history, notification and escalation; a critical device/PLC/HA alarm must not depend solely on Kerani/LLM/cloud. |
| **POS / ERP growth** | Future adapter/contract path; established ERP-owned records remain authoritative in the ERP. |
| **Government/programme bridge** | Optional; sponsor funding does not grant blanket data authority; agency/programme remains authority for eligibility/approval/status. |
| **Growth model** | **D-058/L-048 LOCKED V-Road 8V:** VALID → VALUE → VERBAL (Word-of-Mouth) → VOLUME → VENTURE → VIRAL → VARY → VERSATILE; extended **VOUCH** gate for authentic user endorsement. Evidence-first, sustainable and replaceable partners. |

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

**Talorys / Free cloud evidence (2026-10-12) — SAVED, not architecture proof:** `../docs/TALORYS_CLOUDFLARE_GOOGLE_FALLBACK_EVIDENCE.md` compares Cloudflare Free vs Google Free, records Talorys' single-user Pages/Worker/Durable Object SQLite/Workers AI design (which **does not use D1/Queues**), and provides the updated **AI-first free-text + explicit deterministic fast path + hybrid active fallback** candidate. AI latency should be optimised first (compact prompts/tools, timely Telegram acknowledgement and safe incremental status); only then reconsider routing/model provider. Telegram inline buttons, ForceReply wizard and optional Mini App are candidate Free no-AI entry surfaces. Its 80–90% no-AI routine-operation coverage is **hypothesis**, not verified field-message bypass. AC-012 remains CANDIDATE.

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

**Paid server contingency (NOT fifth active candidate):** Evoxt Malaysia VPS is **CANDIDATE — BACKUP / LAST CHOICE ONLY**, to be considered if measured limitations prevent the four active alternatives from meeting Kerani needs. No annual purchase, demo prerequisite or runtime lock. Check RAM/transfer/ops costs and trial monthly if explicitly authorised. See `../docs/EVOXT_PAID_VPS_CONTINGENCY.md` (2026-10-14).

**E-016** must compare setup/maintenance burden, entry/billing friction, webhook behaviour, latency/concurrency, tenant/quota/waitlist handling, secrets, scheduling/async needs, observability, failure recovery, low-traffic economics, scale-up and migration/rollback.

**New evidence input, not a winner:** Use `../docs/TALORYS_CLOUDFLARE_GOOGLE_FALLBACK_EVIDENCE.md` for a dated Cloudflare Free vs Google Free quota/AI/privacy baseline and **E-016 delta-only work**. Reuse OpsMate's already evidenced candidate/confirm/validate/Purchase-like workflow; **do not repeat one full Purchase flow through deterministic-only/Gemini/Workers AI/forced-failure variants**. Test only missing provider/tool-schema and Cloudflare multi-tenant/runtime/latency/quota/Telegram UX/fallback properties using bounded synthetic fixtures. Talorys proves a personal-agent pattern exists, **not** Workers+D1 multi-tenant readiness. All four control-plane options remain in E-016.

For AC-011, current Oracle documentation checked 2026-10-11 reports 1,500 OCPU-hours + 9,000 GB-hours/month of Ampere A1 Always Free usage, equivalent to approximately 2 OCPUs + 12 GB memory for an Always Free tenancy within the allowance. The benchmark must also treat idle-instance reclamation and free-shape capacity availability as real reliability risks rather than assuming “free forever” equals guaranteed uptime.

### Response-time + language-variability viability signals

- **REPORTED field signal:** OpsMate can feel stuck after transient Gemini/provider failures because retry/poll scheduling adds a large visible wait. The owner recalls an approximately 30-second retry/poll interval in the experienced path.
- **VERIFIED source contrast:** accessible OpsMate worker snapshots currently show a 60-second base exponential retry for API_OR_OUTPUT_ERROR; therefore exact retry timing is unresolved and must be measured rather than assumed.
- **OPEN architecture question:** can **AI-first ordinary free-text** improve comprehension without intolerable Free-model latency, and can explicit deterministic actions and active Telegram-form fallback preserve continuity without creating an OpsMate-style retry wait?
- **Product viability implication:** SuperBasic must prove both acceptable response time and bounded cost per useful action. Moving runtimes alone does not solve AI inference/retry latency.

E-016 must therefore measure latency by stage including provider wait and 5xx recovery; evaluate AI-first ordinary free-text comprehension/response, explicit deterministic bypass, failover and Telegram form completion on **only evidence gaps** after OpsMate proofs are mapped. Do not require a fresh complete Purchase implementation or hard 80–90% model bypass.

The owner's current approximately RM200 Google Cloud billing/onboarding barrier is a practical account-side constraint only; it is not treated as a universal Cloud Run fee.

### Programme and scale candidates

- **AC-008 — CANDIDATE:** sponsor-funded assistance/outcome bridge with user-controlled/minimum-necessary data sharing.
- **AC-009 — CANDIDATE:** pilot → proof → just-enough infrastructure → event/viral readiness → replaceable partner-backed scale.
- Named event, agency, vendor, client-reference and grant details remain external/deferred until real evidence/approval exists.

## Constraints from LOCKED decisions

The design must preserve these boundaries:

- **Free must remain genuinely useful — D-055/L-046 explicitly LOCKED.** Basic Core operation must not require AI; deterministic execution and a usable no-AI input/retrieval path stay available under model outage/quota exhaustion. **D-057/L-047 LOCKS the Telegram Mini App dual-surface product/UI principle**, with common backend authority and active fallback. Premium adds higher-order intelligence, domain capability, automation and convenience rather than blocking basic access.
- **Genericity is earned.** OpsMate supplies evidence; reusable mechanisms may feed Core, agriculture behaviour may feed Agro, and BSE-specific rules stay outside generic Core.
- **Human authority remains explicit.** AI-interpreted mutations require review/confirmation and deterministic/domain validation before authoritative write.
- **No artificial data lock-in.** Users may access/export their own data.
- **Tenant identity is channel-independent.** Moving between WhatsApp, Telegram or future channels must not require a new tenant/history.
- **Quotas are independent.** Transport, storage/media, AI/processing, report/retrieval fair-use and Premium credits are separate controls.
- **D-029/L-023 preserved:** deterministic routing/retrieval/validation **where AI adds no value**, including explicit forms/menus/structured commands, and Free onboarding without BYO Gemini. **D-056 is an owner-selected AI-first free-text trial, not a silent supersession of D-029.**
- **OpenClaw is not business authority.** Synthetic monitoring must not bypass normal controls or contaminate customer truth.
- **Critical IoT alarm path stays local/deterministic.** Kerani may augment it, not become the sole safety dependency.
- **Sponsor ≠ data authority.** Programme sharing is minimum-necessary and purpose-bound; agency remains programme authority.
- **Growth must be evidence-led.** The LOCKED 8V makes **VALID real-world iterative problem/solution testing** the first stage; only then may experienced VALUE, genuine VERBAL referrals, retained VOLUME, responsible VENTURE and prepared VIRAL scale be claimed. Pilot proof precedes public-scale claims; viral readiness requires load, cost, reliability, fallback and observability evidence.
- **Infrastructure/partners must remain replaceable.** Core, tenant identity, portability and business authority cannot be surrendered to one provider/partner.
- **Real field evidence comes early.** When real samples exist they are first-class execution evidence; missing real samples must be marked UNVALIDATED rather than field-proven.
- **V-Road 8V — D-058/L-048 is LOCKED and supersedes historical D-048/L-041 7V:** **VALID → VALUE → VERBAL (Word-of-Mouth) → VOLUME → VENTURE → VIRAL → VARY → VERSATILE**. VALID begins with iterative experiments using real use cases to establish that a solution is useful, effective, usable and worth continuing; then pilot/real users must actually experience VALUE. Word-of-mouth requires authentic recommendation evidence; Extended V-Gate **VOUCH** verifies genuine endorsements with user consent. Previous *Verbal UX* remains the natural-language interaction principle, distinct from growth VERBAL. Every V is earned with evidence, and substantive new contexts may require re-validation.
- **Latency Observability from Day 1 — LOCKED.** Every implemented request path must emit enough timing evidence to decompose user-visible latency by stage from ingress to reply. At minimum capture request start, queue wait where applicable, AI/tool-router time where applicable, tool execution, validation/storage, retry count + retry-wait, and total response time. Aggregate at least P50/P95/P99 plus error/retry rate, segmented by tool/channel/runtime/provider where meaningful. Instrumentation begins with the first executable slice; do not wait until the system feels slow.
- **Convenience-first UX — LOCKED.** User value is prioritized over ownership complexity. Onboarding friction, time-to-value, top-up continuity, latency/accuracy/trust and desired-channel fit are first-order design concerns. Premium features must arise from observed demand rather than being forced into the current Core architecture.

## Growth-maturity truth — owner-LOCKED 8V

The active business/development philosophy is **D-058/L-048**. The original D-048/L-041 7V remains in retained Full ZASS as superseded history; do not show it as today's canonical sequence. Current 8V: **VALID → VALUE → VERBAL (Word-of-Mouth) → VOLUME → VENTURE → VIRAL → VARY → VERSATILE**. **VOUCH** is a continuous Extended V-Gate (genuine, evidence-backed user endorsement) and not a ninth stage. VALID is a repeated real-use experiment/improve/retest gate rather than a generic software syntax/data validation step. In later stages, new target customers or contexts can trigger VALID again. Vital/V-King remain unnumbered destinations. This LOCK does not prove Kerani has passed any new maturity stage or alter technical architecture.

## Premium Business Workspace — CANDIDATE concept projection (D-059)

User request: **AI business summary in Telegram → Buka Dashboard button → interactive tenant-specific business view**. Potential views: charts/tables with factual source links, filtering/search, bounded forecast when data is sufficient, internal Task status, authorised Google Drive links, and future Android Home Screen/PWA entry. All customer-facing analytics must use trusted data and tenant/role permission checks; standalone browser/PWA cannot rely on Telegram WebApp initData as its session authority. **No cross-provider external task sync or OAuth is authorised**, and no new standalone dashboard backend or separate business SoT is chosen.

**Only the candidate is recorded**, not an implementation slice or release promise. Existing D-057/L-047 Free deterministic Mini App remains first-class; basic Task/report/retrieval remains Free. Premium packs D-050/D-051 and Drive OAuth remain CANDIDATE. Refer to `../docs/KERANI_PREMIUM_BUSINESS_WORKSPACE_CANDIDATE.md` for proposed journey, experiment and STOP boundaries. Priority remains OpsMate PILOT_REAL handover → clean Agro Demo; return to this idea when real usefulness warrants a pilot, following the D-058 VALID-first philosophy.

## Channel / storage / AI-policy / concurrency — D-060 CANDIDATE projection

**Owner discussion 2026-10-22, ZASS-reviewed but NOT LOCKED.** Candidate user-choice model: one Kerani backend and tenant identity; WhatsApp onboarding welcome credit with proposed cost-reflective paid transport after expiry; Telegram as lower-overhead default; optional user-controlled Google Drive attachments/exports instead of assuming Drive is a live transactional database; ongoing minimal useful Free Core storage with paid capacity upgrades; provider-policy-compliant Free/Paid AI options; and concurrency-safe class-specific request control.

**Trust boundary:** Existing D-016/D-017/D-018/D-020/D-023–D-030/D-052–D-055 LOCKED rules remain. In particular D-025's continuing controlled Free shared WhatsApp allocation may need formal supersession for a stronger paid-only-after-onboarding policy; D-055 prevents the removal of a useful Free baseline. Paid AI protections are contractual and conditional, not an unconditional privacy/SLA guarantee, and user consent cannot override API vendor bans on sensitive data.

**Resilience challenge hypothesis:** Direct authorized indexed READ where safe; mutations with deterministic rule enforcement, confirmation if required, tenant scope, idempotency and evidence-based durability; AI calls with provider/tenant/global concurrency budgets, bounded retry/recovery and privacy-compliant fallback; background work with backpressure. Preserve real data correctness and truthful SAVE results during bursts. E-016/E-018 benchmarks must justify queue/database/AI provider choice; do not select any infrastructure from this projection.

**Documentation:** `../docs/KERANI_CHANNEL_CLOUD_AI_RESILIENCE_ZASS_CANDIDATE.md`; master decision `D-060 CANDIDATE`; tracker KAI-8 BACKLOG. This projection has **NO** code, deployment, authenticated Drive connection, payment/AI invocation, implementation task or PRE-ARCH selection. This project does **not** include competitors or Claude trend discussions in D-060.

## RekodUntung.ai — Primary Brand Candidate (D-062)

**Owner approved 2026-10-23: PRIMARY NAME CANDIDATE only, NOT BRAND LOCK.** Preferred exact spelling: `RekodUntung.ai`. It couples Free's recordkeeping utility with the hoped-for business benefit; do **not** claim validated net-profit computation or guaranteed business profit. This is a naming hypothesis, not a product capability change.

**Unchanged until later owner approval:** the GitHub repository remains `dzuddiyn/Kerani_Core_SuperBasic`, current identity remains Kerani AI, no code/package, bot username, domain registration, public UI, deployment or migration change. All D-016/D-057/D-061 Free product decisions and existing technical architecture gates remain as they were.

**Before any rebranding LOCK:** evidence-led official MyIPO trademark similarity/classes/owner search, real `rekoduntung.ai` registrar/renewal availability, nearby product/name collision review and micro-SME meaning/expectation test. MyIPO clearance and domain checks are **NOT VERIFIED**. Only after these gates may the owner decide go/no-go; a separate approval is needed for migration.

**Source:** `../docs/KERANI_BRAND_REKODUNTUNG_PRIMARY_CANDIDATE.md`; master `D-062 CANDIDATE` (no `L-050`); Linear KAI-10.

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
15. **AI-first / hybrid active fallback UX trial** — D-056/Q-038/R-037: ordinary free text → bounded AI; explicit menu/form → deterministic; 429/5xx/quota/latency → constrained provider fallback and actionable Telegram deterministic form, while deterministic validation/authority remains universal.
16. **Mini App entry point / UX / auth and hosting** — Q-039/R-038; **D-057/L-047 product/UI principle is LOCKED**, but menu button vs Main Mini App, exact v0.1 screens, auth integration test, Cloudflare Pages vs other HTTPS hosting and first rollout are still DESIGN/CHALLENGE candidates.
17. **Premium Business Workspace UX** — **D-059 CANDIDATE, NOT LOCKED**: Chat produces a truthful, tenant-scoped textual summary plus contextual dashboard button; Web UI offers business-relevant interactive source-linked charts/tables/search and later bounded analytics. PWA Android entry needs separate browser auth; user-permitted Google Drive links ≠ Drive OAuth; tasks start with Kerani Task and any external task sync is deferred and authority-led. No feature-price/entitlement, PRE-ARCH, Google scopes, deployment or task execution is approved.
18. **Modular cost / Drive / AI data policy / burst resilience** — **D-060 CANDIDATE, NOT LOCKED**: Q-040–Q-044; test official WhatsApp/BSP unit costs, trial-only channel credits vs D-025, permanent Free operational storage vs pay-for-extra cloud, tenant-owned Drive adapter, legal/provider-specific Free/Paid AI data terms and E-016/E-018 burst, queue, idempotency and privacy-safe fallback. No architecture/provider/pricing/Free-policy change implied.
19. **Telegram Group UX PROOF after D-061/L-049 OWNER LOCK:** T01 plain @mention Privacy ON, T02 Privacy OFF isolated, T03 slash command auto-send, T04 ForceReply targeted, T05 concurrent user/prompt routing with transport retry idempotency, T06 Inline Mode usefulness. All NOT TESTED; do not pretend product LOCK is a functional acceptance.

**Brand name clearance pending:** D-062 RekodUntung.ai is PRIMARY CANDIDATE only; verify MyIPO and registrar evidence before proposing any LOCK or repo/public rename.

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
- **Programme/growth/partner:** D-035–D-049 historical lineage + **D-058/L-048 canonical V-Road 8V**; D-048/L-041 7V SUPERSEDED.
- **Observability requirement:** D-052 / L-043
- **Delivery Value Gate:** D-053 / L-044
- **Convenience-first UX / evidence-led Premium:** D-054 / L-045
- **Premium candidates:** D-050 · D-051
- **Architecture candidates:** AC-005–AC-012
- **Current control-plane evidence gate:** E-016
- **Retained Full ZASS lineage / escalation reference:** `../ZASS_Kerani_Core_SuperBasic.md`
- **Method baseline:** ZASS SYSTEM v0.2.2 · ZASSIMPLE v0.3.3 · Full ZASS v0.3.11
- **Migration contract:** `MIGRATION_CONTRACT.md`
