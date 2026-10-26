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
| I-017 | Modular channel credits, tenant-owned document storage, extra Kerani Cloud, data-policy-aware Free/Paid AI routing and multi-tenant concurrency resilience, without changing the one Kerani backend or permanent Free Core promise. | Owner discussion 2026-10-22 | CANDIDATE — D-060 |

| I-018 | Free personal-chat bot first; simple Business/User IDs; warn if multiple active Free users of same company may overlap; let users create their own group and call KeraniBot without an OpsMate-style group workflow. | Owner approval 2026-10-23 | LOCKED product/UX — D-061/L-049; delivery details TEST PENDING |
| I-019 | RekodUntung.ai as the primary next **candidate brand name** to investigate; keep Kerani AI / existing repository unchanged, do not rebrand or LOCK until MyIPO and domain verification and explicit owner go/no-go. | Owner approval 2026-10-23 | PRIMARY NAME CANDIDATE — D-062, NOT BRAND LOCK |

| I-020 | Use a lightweight Cloudflare Worker as WhatsApp inbound/outbound adapter and 95% (950) warning / 99% (990) normal-outbound stop for the 1,000 monthly per-business-number free Meta service-message allowance, while keeping Google Apps Script as candidate business Core and event-driven webhooks instead of time-trigger polling; evaluate Queues/DO Alarms for sub-minute delayed work only when justified. | Owner 2026-10-24 save/commit preview | CANDIDATE — D-063, NOT PRE-ARCH LOCK |
| I-021 | Pilot WhatsApp V1 uses Worker → protected Apps Script directly, built with a versioned queue-ready Job Envelope, idempotent Core SAVE and common outbound quota gateway, so that V2 may add a Queue/consumer without resetting tenant records; if timeout/ACK loss risk is unacceptable, V2 is required BEFORE real user rollout. | Owner LOCK 2026-10-24 | LOCKED CONDITIONAL PILOT STRATEGY — D-064/L-050; tests/deployment NOT AUTHORIZED |

| I-022 | Three OpsMate lessons become P0 Kerani release gates: RG-01 version/mock-cleanup isolation and no-regression; RG-02 visible, nearly-live Free basic dashboard; RG-03 structured tenant-scoped read model for grounded AI and UI, not scanning dozens of Sheet tabs. | Owner approval 2026-10-24 | LOCKED release/readiness invariants — D-065/L-051; acceptance NOT RUN |

| I-023 | Freeform entry without complicated domain algorithm; faithfully store user's own data in authoritative Core and automatically provide a user-accessible Google Sheet export/projection in their consented Drive, which they may analyze in external AI or copy/edit/delete without losing Kerani's source records. | Owner LOCK 2026-10-26 | LOCKED product principle D-066/L-052 — integration/testing OPEN |

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
| Q-033 | How much of the user-visible latency is caused by runtime/poll/retry scheduling versus Gemini/provider inference versus storage/channel work, especially after transient AI/provider errors? | Kerani cannot choose a viable product runtime or retry policy from end-to-end “slow” perception alone; the latency must be decomposed. | OPEN |
| Q-034 | Which genuinely explicit commands/menu/form actions can safely bypass AI without brittle keyword matching or misrouting? | Under the 2026-10-12 owner AI-first free-text trial, deterministic parsing is a fast path for explicit input and an active degraded-mode UX, not a mandate to interpret all natural-language variants via keyword rules. | OPEN — refined owner trial scope |
| Q-035 | Which reusable behaviours should become agent-callable tools, and what authority class/gates must each tool carry? | Prevents genericity from being confused with agent authority and tests whether natural-language UX can improve without weakening D-015 human/deterministic control. | OPEN |
| Q-036 | Which Kerani request classes require durable ingress/queue + idempotency, and which can safely use a direct low-latency path? | Prevents blindly inheriting OpsMate queueing into all paths while still protecting mutation/retry/restart correctness. | OPEN |
| Q-037 | Where must authorization/scope be enforced between channel identity, tool routing and data access? | Tenant identity alone does not prove permission; the challenge must prevent AI/tool arguments from becoming authority and prove fail-closed tenant isolation. | OPEN |
| Q-038 | Can AI-first free text + deterministic-first explicit interactions + hybrid active fallback give better Verbal UX and latency than deterministic-first language matching without uncontrolled Free AI use? | Owner's 2026-10-12 trial preference is not yet field evidence; models, early acknowledgement/chunking, quota, provider fallback and Telegram forms should be judged against OpsMate evidence and real language. | OPEN — owner-selected challenge hypothesis |
| Q-039 | Which Telegram Mini App entry point, UI scope, auth binding and hosting path deliver a genuinely usable AI-independent structured experience without duplicating business logic or obstructing the Agro demo? | D-057/L-047 fixes the product surface principle; menu button vs Main Mini App, Cloudflare Pages, web session security and exact screen build remain unproven. | OPEN — DESIGN/TEST detail |
| Q-040 | Can one-time WhatsApp welcome credit plus metered transport coexist with D-025's shared-WA discovery Free allowance while keeping channel-neutral paid AI pricing? | The proposed no-recurring-Free-WA policy may require explicit owner supersession and official Meta/BSP unit costs. | OPEN — D-060 CANDIDATE |
| Q-041 | Which minimal tenant operational record store must remain always accessible, and which receipt/media/export/backup content may optionally reside in user-owned Drive? | Avoids using Drive as unproven hot OLTP, hidden dual SoT, and an unusable Free Core after a cloud trial. | OPEN — D-060 CANDIDATE |
| Q-042 | Which real AI Free/Paid provider terms, data classes, retention/training conditions and fallback authorizations are acceptable for confidential SME data? | User consent cannot override provider restrictions; paid does not automatically mean zero-retention. | OPEN — D-060 CANDIDATE |
| Q-043 | Which class-based request admission, fair concurrency, durable write/receipt, AI rate limiting and overload controls pass E-016/E-018 for many simultaneous tenants? | Prevents slow AI/providers or one heavy tenant from blocking core reads or corrupting writes. | OPEN — D-060 CANDIDATE |
| Q-044 | What permanent Free storage baseline, paid-cloud/transport/AI credit units, trial expiry and refund semantics prove sustainable without coercive data lock-in? | Preserves LOCKED Free/portability promises and protects cost ledger under failures. | OPEN — D-060 CANDIDATE |

| Q-045 | Can `@KeraniBot rekod ...` and `@KeraniBot jana report ...` reach Kerani reliably in a normal user-created Telegram group with Privacy Mode ON? | Default Telegram privacy restricts visibility; natural @mention delivery is not a guaranteed command route. | OPEN — T01/T02 mandatory |
| Q-046 | Does slash-command auto-send followed by targeted `ForceReply` provide a natural single-reply data entry UX without switching off Privacy Mode? | Owner observed direct command sending is clumsy; native command-menu draft-only mode is not a Bot API promise. | OPEN — T03/T04 |
| Q-047 | Can separate workers' concurrent group replies be matched to trusted user/group/bot-prompt context without role hierarchy or semantic dedup? | A simple Free group must not mix workers, expose tenant records or duplicate the same transport update. | OPEN — T05 |
| Q-048 | Does Inline Mode prefill improve group UX enough to justify the extra inline-results interaction? | Avoids new complexity merely to fill text without auto-send. | OPEN — T06 |
| Q-049 | Is RekodUntung or a confusingly similar mark already registered, applied for or otherwise in use for relevant Malaysia products/services? | Avoid premature brand adoption, legal disputes and user confusion. | OPEN — Official MyIPO/similarity assessment required before brand LOCK |
| Q-050 | Is rekoduntung.ai genuinely registrable today, with sustainable renewal pricing, and do suitable backup TLDs/handles exist? | Availability is a live registrar fact, not inferred from a lack of search results. | OPEN — Domain registrar/registry READ verification before brand LOCK |
| Q-051 | Does the name RekodUntung imply a profit calculation or guaranteed profit that the currently locked Free product does not provide? | Product UX/marketing must communicate recordkeeping first and avoid unsupported claims. | OPEN — User comprehension / truthful claim gate |

| Q-052 | Can a Cloudflare Worker govern all outbound WhatsApp service-message sends by business phone number, warn at 950 and stop routine sends at 990 without false paid-tier/no-charge assurances? | Meta’s first 1,000 delivered service messages/month/number allowance is a provider meter distinct from inbound webhook, templates and application retry count; bypass senders/status lag must be reconciled. | OPEN — D-063 / CF-WA-QG-01 |
| Q-053 | Is direct event-driven webhook → Apps Script `doPost` sufficient to avoid the observed 60-second polling path, or is Cloudflare's edge layer measurably better? | The 1-minute Apps Script trigger is for periodic polling only, not a general minimum `doPost` interval. | OPEN — A/B/C benchmark |
| Q-054 | What durable ingress, retry and per-phone quota reservation semantics make Worker + D1/DO/Queues safer than simpler Apps Script-only? | ACK-before-durable-write, unknown send outcome, 989/990 concurrency and at-least-once callbacks risk losses/duplicates/cost leakage. | OPEN — synthetic T01–T08 |
| Q-055 | Which delayed work needs an event-driven Queue or DO Alarm rather than 1-minute Cloudflare Cron or Apps Script trigger, and what are its measured latency/cost bounds? | Sub-minute scheduling is feasible but not a precise completion guarantee; avoid accidental overarchitecture. | OPEN — QG synthetic benchmark |
| Q-056 | What exact versioned Job Envelope fields, trusted sender→tenant binding, protected Worker-to-Apps-Script call, idempotency retention and status contract are sufficient for both direct and Queue mode? | Queue-ready *principle* is locked, schema/crypto/storage implementation still needs design and proof. | OPEN — D-064/L-050 / CF-WA-QG-01B |
| Q-057 | Which observed failure, timeout distribution and webhook ACK/safe-durability threshold fails V1 and requires Queue before live traffic? | Owner chose mandatory escalation if repeated timeout or pre-ACK loss risk; do not invent threshold or assume success. | OPEN — release gate evidence |
| Q-058 | Can V1→V2 canary/cutover/rollback preserve tenant records, ordering, final receipts, outbound quotas and no-double-SAVE without two active dispatchers per job? | A no-reset goal depends on schema stability, shared idempotency and safe in-flight reconciliation. | OPEN — synthetic migration verification |

| Q-059 | How can Kerani make test/mock cleanup, required schema/seed/config and old-to-new upgrades independent, with repeatable rollback/recovery and baseline function retention? | Owner-reported OpsMate lost functions after test data cleanup; no forensic root cause confirmed. | OPEN — D-065/L-051 RG-01 tests U01–U04 required |
| Q-060 | What minimum tenant-visible Free dashboard and read-model freshness meets almost-live expectations without scanning/refreshing every Sheets tab or making Premium mandatory? | Owner's UX concern is lack of observable value; proposed P95 commit→fresh-visible ≤5 s is an unverified pilot hypothesis, NOT locked SLA. | OPEN — D-065/L-051 RG-02 tests V01–V03 required |
| Q-061 | Which single-SoT summary/read-model API, event watermark and provenance contract support bounded accurate AI extraction and dashboard, with deterministic fallback? | Avoid 30-tab scans and a diverging second business truth. Optional AI must not block no-AI Free. | OPEN — D-065/L-051 RG-03 tests K01–K04 required |

| Q-062 | What minimal metadata, input/attachment boundaries and validation let users enter broad freeform business content without mandatory complex algorithms, while preserving raw text and secure tenant authority? | User intends general record capture rather than new specialist accounting logic; broad entry is not permission for unbounded file types, unsafe input, or fabricated financial categories. | OPEN — D-066/L-052 |
| Q-063 | What consented Google Drive/Sheets integration best gives each tenant a near-live export with recoverable status, provenance and editable/deletable user file without creating a second authoritative business DB? | OAuth/Drive scopes, location/ownership, quota, latency, sync conflict policy and error handling untested. | OPEN — D-066/L-052 |
| Q-064 | How do automatic export refreshes coexist safely with user edits or deletion, without silent overwriting, unintended restoration or Sheet→Core mutation? | Evaluate managed export + detachable editable copy vs reserved generated range/conflict detection; no mode preselected. | OPEN — D-066/L-052 |

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
| R-032 | Retry / polling delay amplifies transient AI-provider errors into unacceptable user-facing latency | A 5xx/provider failure can make an otherwise simple operation feel stuck for tens of seconds or longer, damaging product usability even when eventual recovery succeeds. | Measure retry scheduling separately from inference; prefer explicit bounded backoff/async acknowledgement where justified; test P50/P95 and failure-recovery time before PRE-ARCH selection. | OPEN | Transient 5xx errors cause long silent waits, repeated polling windows, or user retries/duplicates. |
| R-033 | Deterministic language handling becomes brittle across real user phrasing | A growing list of keywords/rules may miss synonyms, shorthand, mixed Malay/English, spelling variation or ambiguous phrasing, causing misroutes or forcing excessive AI fallback. | Test deterministic-first routing against real field corpus; use confidence/clarification boundary; measure coverage, misroute rate and AI-fallback rate instead of assuming universal keyword coverage. | OPEN | New user wording repeatedly bypasses the fast path, requires rule patches, or is routed to the wrong record family. |
| R-034 | Agent tool authority creep | A reusable/tool-callable capability is mistaken for permission to mutate business truth, causing unsafe writes, cross-tenant access or model-driven policy decisions. | Classify every tool by authority; keep READ/PROPOSE separate from MUTATE; require tenant scope, human confirmation where applicable, deterministic/domain validation, idempotency and audit before authoritative changes. | OPEN | Function/tool calls write or delete authoritative records without an explicit gate or a new GENERIC behaviour is automatically exposed as an agent tool. |
| R-035 | Universal queueing recreates OpsMate-style latency and unnecessary complexity | Forcing all READ and ACTION requests through one durable queue can increase response time, retry amplification and operational burden even when some requests are safe to execute directly. | Challenge durable-ingress scope by request class; retain direct/read paths where safe; require idempotency/durability where authoritative side effects or retries justify them; measure queue wait from Day 1. | OPEN | Simple read requests accumulate queue wait/poll delay or require worker recovery despite having no authoritative side effect. |
| R-036 | Identity resolved but authorization scope not enforced at tool/data boundary | A valid user/tenant binding could still access another tenant/resource if AI arguments or downstream queries are trusted without re-checking scope. | Use trusted context for tenant/user authority; fail closed; re-check scope before protected tool execution and deterministic data access; test cross-tenant denial for READ and MUTATE. | OPEN | Model/tool arguments can select another tenant/resource or a retrieval query returns data outside the caller's authorized scope. |
| R-037 | AI-first language UX degrades under Free-model latency, rate limits or unreliable tool results; weak deterministic fallback feels like a dead end | Verbal UX loses trust, users repeat or abandon requests, AI calls multiply, or incomplete tool plans are presented as completed writes. | Bounded AI-first free-text calls, early truthful Telegram acknowledgment, active failover within budget and time box, inline-keyboard/ForceReply/manual fallback, verified tool receipts and D-015 mutation gates. | OPEN | P95/P99 spikes, 429/5xx retry loops, form abandonment, unbounded model invocations or false success. |
| R-038 | Mini App front-end identity, validation or data handling bypasses tenant/business authority | Spoofed Telegram context, cross-tenant reads, duplicate commits or inconsistent Chat/Mini App history can corrupt trust. | Backend verifies Telegram WebApp initData using bot-token signature/expiry, maps a trusted tenant/session, enforces permission server-side on every API call, uses the same business contracts/validation/idempotency/audit, and tests cross-tenant/replay rejection. | OPEN | Browser-provided initDataUnsafe/tenant IDs accepted as authority; UI directly writes records without Core gate; chat and Mini App diverge. |
| R-039 | Welcome credits expire and customer business records become inaccessible/deleted | Violates lasting Free usefulness, export rights and trust. | Preserve small durable Core Free baseline, clear quota/retention and non-destructive upgrade/export path; charge for additional capacity, not record hostage-taking. | OPEN | Post-trial customer cannot retrieve/export saved basic records. |
| R-040 | Free AI provider data policy/training or fallback violates confidentiality | Sensitive tenant info leaks or terms/privacy obligations are violated even with a generic consent checkbox. | Classify/redact/limit data, validate each provider tier's live terms, consent where appropriate, fail closed to deterministic route; never auto-route confidential payload to unsuitable Free API. | OPEN | Unrestricted raw customer records sent to a Free endpoint or a retry changes privacy terms silently. |
| R-041 | Concurrent load stalls database and AI provider, amplifying retries and duplicates | Customers lose trust, experience P95 spikes, data integrity fails and token spend runs away. | Tenant/global admission limits, direct protected READ, class-specific durable mutation, idempotency receipts, provider-aware budgets/fairness and E-016/E-018 multi-tenant fault drills. | OPEN | Unbounded queue, 429/5xx storms, duplicate authoritative writes, missing save receipts. |
| R-042 | Customer-owned Drive becomes an unbounded live database/sync authority | Revoked OAuth, quota/hotspot and stale files corrupt operational state or degrade access. | Keep backend authoritative contracts, treat Drive as optional scoped attachment/export adapter, test disconnect/restore/migration and permission revocation. | OPEN | A document move in Drive silently changes live transaction truth, or record access fails on Drive outage. |
| R-043 | Multi-dimensional credits are impossible for a small SME to understand | Confusing pricing, failed-charge disputes and users abandon onboarding. | Simple Telegram+Free defaults, itemized transport/storage/AI entitlements and clear cost-before-action, refund/pending receipt tests with real pilots. | OPEN | Failed AI calls charged as delivered, inconsistent balances or pricing questions prevent first useful record. |

| R-044 | Overbuilt Free group semantics recreate OpsMate complexity | Free needs roles, AI semantic dedup and approvals, causing cost/latency spikes and user friction. | Keep 1:1 bot as Free first, warning-only multiple-Free overlap, optional user-created group, no cross-worker content matching. | OPEN | New group admin/AI dedup introduced as Free dependency. |
| R-045 | Plain @mention assumed to reach privacy-enabled Telegram bot | Bot silently misses reports and users believe data was stored. | Treat @mention as unverified; T01/T02 actual update receipts, verified fallback slash command → ForceReply; honest acknowledgement. | OPEN | Mention generates no update but UI implies successful save. |
| R-046 | Business ID or group membership treated as permission | A guessed ID or unauthorized group member can view/write another tenant's data. | Verified user↔Business ID association, consented group binding, server-side read/write scope checks, no role hierarchy requirement. | OPEN | Anyone knowing an ID or joining group can retrieve company records. |
| R-047 | Two users' group replies/retries are routed to wrong action or create duplicate effects | Concurrent prompts cross wires and authoritative data becomes corrupt. | Scoped chat/user/reply-to-message ID matching, TTL/validity and transport-event idempotency; retain normal approval/validation as needed. | OPEN | Worker A's reply saved for worker B or same Telegram update double-commits. |
| R-048 | Rebrand before MyIPO/domain clearance | A mark/domain collision creates legal cost, broken links and sunk design work. | Keep only PRIMARY NAME CANDIDATE D-062; official mark/similarity + live registrar checks and owner approval first; no rename, handle, domain or product identity change. | OPEN | Internal draft treated as name LOCK or domain shown as owned. |
| R-049 | Name RekodUntung makes users expect computed profit or a guaranteed business outcome | Free Core records operations but may lack inputs for accurate net profit; marketing overpromises. | Separate proposed brand meaning from demonstrated Free scope; test user interpretation and truthful copy before launch. | OPEN | Public copy guarantees profitability or validated accounts without evidence. |

| R-050 | Mistaking monthly 1,000 Meta service-message allowance for all inbound/outbound messages | Misleading spend guard, overshoot charge and incorrect Free product entitlement. | Count eligible delivered outbound service-message class by phone number/period and reconcile provider status; templates and BSP fees treated separately. | OPEN | Counter diverges from WhatsApp Manager or template charges appear while guard shows free. |
| R-051 | Check-then-increment race across simultaneous Workers near 990 normal-stop boundary | Parallel sends breach reserved budget. | Atomic conditional reservation in proven D1 transaction or per-number DO; test 10 parallel at 989/990; account for ambiguous provider outcome. | OPEN | Two sends both accept the same last free slot. |
| R-052 | Cloudflare webhook ACK precedes durable ingress while Apps Script times out | Event silently lost, false SAVE claim, replay creates duplicate record. | Verify signature, durable intake before ACK, idempotent processing, queue/DO retry with observed receipts; never equate webhook ACK with business commit. | OPEN | 200 webhook ACK with no durable event or confirmed business record. |
| R-053 | Treating Cron/DO Alarm or Queue settings as guaranteed real-time scheduler | Architecture misstates sub-minute semantics and creates complexity. | Direct webhook for immediate work; Cron minimum minute; Queues/DO alarm best-effort delayed work only when tests justify. | OPEN | “5-second guarantee” written without P95/P99 and outage evidence. |
| R-054 | Queue added after V1 but IDs/contracts differ | Migration needs customer-record reset or rewrite, or duplicate core side effects. | Versioned stable Job Envelope, dispatcher abstraction, common processJob Core/SoT, shared inbound and outbound idempotency from V1. | OPEN — strategy LOCK D-064 | Queue rollout requires changing business schema/IDs. |
| R-055 | V1 ACKs WhatsApp before durable admission, or direct Apps Script times out repeatedly | Meta retries and lack of durable work ownership cause lost/unconfirmed business records. | Do not release unsafe V1; only ACK after safe synchronous completion or durable admission, else escalate to V2 and prove durable Queue. | OPEN — pre-live STOP gate | 200 accepted but no persisted event or committed business record. |
| R-056 | Two dispatch modes run same job during cutover or rollback | Duplicate stock/business mutations and duplicate sends despite underlying Queue at-least-once semantics. | One processing authority per stable job ID, authoritative idempotent commit, outbox status and in-flight drain/reconciliation. | OPEN — V1→V2 canary proof | Same message saved/sent by direct and Queue consumer. |

| R-057 | Test-fixture/mock rows are accidentally treated as schema/config/required seed or production truth | Functions disappear after cleanup; release damage or data loss. | Isolate dev/staging/pilot data and version required seed/config; empty tenant, mock-cleanup, migration/regression and rollback evidence RG-01. | OPEN — LOCKED release gate | Previously supported workflow fails following fixture purge. |
| R-058 | Chat-only Free product hides useful committed records or displays stale/incorrect/dashboard Premium-only totals | Users cannot perceive value of time spent keying records and may abandon Kerani. | Make basic Free history/summary dashboard tenant-scoped, source-traceable and freshness-visible; RG-02 commit→read proof. | OPEN — LOCKED release gate | User cannot see a committed record or outdated figures appear current. |
| R-059 | AI queries raw dozens of Sheet tabs or stale/unauthorized projections | Unbounded latency/token cost, hallucinated totals, cross-tenant data or diverging second SoT. | Rebuildable tenant-scoped bounded read model, deterministic source totals and source revision/provenance; no-AI Free fallback; RG-03. | OPEN — LOCKED release gate | AI fabricates number or cannot cite permitted source records for released feature. |

| R-060 | Google Sheet used as second authoritative database or direct edit/delete copied back into Core without permission | Tenant data corruption, divergence, silent destructive operations. | Sheet is nonauthoritative, rebuildable export; authoritative Core mutations require separate user-approved validated flow; deny automatic two-way writes. | OPEN — D-066 locked boundary | Changed or deleted Sheet silently changes Kerani original record. |
| R-061 | Auto-updating managed export overwrites user's sheet edits, or recreates deleted user file | Violates user freedom and leads to loss of external analysis/annotations. | Separate synced projection from editable detachable copy or another explicit proven conflict model; no silent overwrite/recreation. | OPEN — D-066 design choice | User-added cells lost after refresh or deleted Sheet reappears without approval. |
| R-062 | Export mistakenly includes another tenant, publishes confidential data, or sends user Sheet automatically to third-party AI | Privacy/legal risk; users lose control. | Verified tenant/Drive consent, least-privilege and no public share default, allow independent export; no automated external AI upload. | OPEN — D-066 integration gate | Cross-tenant row on Sheet, public-by-default link, unapproved AI transfer. |

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

**2026-10-12 reference evidence (not architecture proof):** Talorys uses Cloudflare Pages + Worker + SQLite-backed Durable Object + Workers AI, NOT D1/Queues. It demonstrates a bounded single-user agent/tool experience with deterministic features usable after AI quota exhaustion. This is **reference evidence for feasibility**, not validation of Kerani's multi-tenant Workers+D1 workload. See `docs/TALORYS_CLOUDFLARE_GOOGLE_FALLBACK_EVIDENCE.md`; keep AC-010 **CANDIDATE** and E-016's four-way comparison unchanged.

---

## AC-011 — OCI Ampere A1 Always Free VM Control Plane

**Status:** CANDIDATE  
**Origin:** owner infrastructure-cost review 2026-10-11

~~~text
WhatsApp / Telegram / future channel
                ↓
        OCI Ampere A1 VM
     API / Router / Worker
                │
      ┌─────────┼───────────┐
      ↓         ↓           ↓
 local state  queue/job    external services
 / DB         runner       AI / Apps Script /
                           Drive / customer edge
~~~

**Intent:** Benchmark a low-cost always-on VM control plane where Kerani can control webhook handling, queue/worker behaviour, timeout/retry/backoff, asynchronous acknowledgement and observability more directly than an Apps Script-only runtime.

**Current official Always Free evidence checked 2026-10-11:** Oracle documents the Ampere A1 Always Free allowance as the first **1,500 OCPU-hours + 9,000 GB-hours per month**, equivalent for an Always Free tenancy to approximately **2 OCPUs + 12 GB memory** when used continuously within the allowance. Oracle describes Always Free resources as available free of charge for the life of the account, subject to eligibility/limits.

**Important risks:** Always Free compute can be reclaimed when Oracle's idle criteria are met, and Oracle documents possible out-of-host-capacity availability for free shapes. Therefore OCI Always Free cannot be assumed to provide a guaranteed production SLA or guaranteed capacity merely because the compute allowance is free.

**Why candidate, not LOCKED:** Kerani has not benchmarked ARM compatibility, operational maintenance burden, webhook latency, queue/retry behaviour, storage design, backup/restore, observability, security patching, idle-reclaim risk, capacity availability, or migration/exit effort on this stack.

**Cost boundary:** Treat compute cost as potentially near-zero only while actual usage remains inside current Always Free limits. Provider terms and limits are externally changeable and must be reverified at implementation time.

**Anti-lock-in rule:** OCI-specific VM/storage/networking details must remain behind stable Kerani contracts so the control plane can move to Cloudflare, Cloud Run, central Apps Script, another provider, or paid infrastructure without changing tenant identity/business logic.

---

### Paid-server contingency — Evoxt Malaysia VPS (2026-10-14)

**Status:** CANDIDATE — BACKUP / LAST CHOICE ONLY; **NOT a fifth active E-016 control-plane candidate**.

**Owner direction:** Retain Evoxt Malaysia VPS as a **paid emergency/last-resort hosting option** if Cloudflare, Google managed/free alternatives or OCI free capacity prove unsuitable for measured Kerani requirements. Do not purchase a server or lock its architecture simply because low-cost VPS hosting exists.

**Reported evidence (NOT TESTED):** an owner-shared Evoxt advertisement claims Malaysia VPS from USD 2.99/month and up-to-6.0-GHz turbo CPU. One owner-supplied user experience reports limited bandwidth/transfer and small RAM for running other services and prefers longer billing. Neither proves sustained CPU performance, usable memory/headroom, network transfer, uptime or real Kerani economics.

**Activation gate:** Only consider a time-limited paid VM trial after specific free/managed alternative blockers have been measured. Validate real VM SKU/RAM, transfer allowance, pricing, monthly vs annual terms, webhook P50/P95/P99, restore/security/patch/monitoring overhead, privacy, portability and total cost. Monthly test before committing annually. CPU clock claims do not speed up external AI provider inference.

**Scope:** Not needed for the first Kerani Agro Basic Demo unless a proven deployment blocker emerges. Keep OpsMate reproduction tests reusable; no redoing Purchase end-to-end. Detailed evidence/guardrails: `docs/EVOXT_PAID_VPS_CONTINGENCY.md`. This does not change AC-010/AC-011 status, E-016's four principal candidates or PRE-ARCH.

---

## AC-012 — Bounded Agent Tool Orchestration

**Status:** CANDIDATE  
**Origin:** owner UX/agentic architecture discussion 2026-10-11

**Intent:** Let AI translate natural user language into bounded capability/tool calls while preserving Kerani's existing human, deterministic, domain and tenant-authority boundaries.

**Key distinction:** `GENERIC` behaviour is a reuse classification, not an agent permission. A behaviour must separately prove that it is tool-worthy and declare one authority class: READ, PROPOSE, CLARIFY, VALIDATE, MUTATE or SYSTEM/AUTOMATION.

**Priority tool candidates:**
- `retrieve_history` — READ: AI may map natural questions to tenant-scoped deterministic retrieval parameters.
- `prepare_candidate` — PROPOSE: AI may map short operational language into a structured non-authoritative candidate.

**Mutation boundary:** authoritative create/update/delete capabilities require explicit authority design, tenant scope, human confirmation where applicable, deterministic/domain validation, idempotency and audit. Function calling alone never grants mutation authority.

**Why candidate, not LOCKED:** tool registry shape, authority metadata, model/provider behaviour, latency/cost, multi-user language coverage, tenant isolation and mutation gates have not yet passed the Architecture Assumption + Boundary Challenge or real execution evidence.

**2026-10-12 reference evidence:** Talorys illustrates bounded language-to-tools plus a working non-AI path, but its single-user tool permission model cannot be imported as Kerani multi-tenant authorization/mutation policy. A no-AI deterministic path is the **always-on business execution authority**, not an emergency-only replacement; AI-assisted interpretation, model failover and degraded/manual UX are separable candidate routing strategies. See `docs/TALORYS_CLOUDFLARE_GOOGLE_FALLBACK_EVIDENCE.md`. The 80–90% no-AI routine-operation coverage figure is **HYPOTHESIS ONLY**, not field performance evidence.

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

**Interpretation / pending challenge (2026-10-12):** This existing owner LOCK is preserved verbatim; the owner proposes an **AI-first path for ordinary free-text requests**, with direct deterministic fast-path for **explicit** commands/forms where AI adds no value, plus hybrid active fallback on AI failure. This is not permission to remove deterministic business authority, D-015 confirmation or D-055 no-AI usefulness. The runtime routing priority remains a **CANDIDATE** under D-056/Q-038 until challenge/explicit PRE-ARCH decision; no silent supersession of D-029/L-023.

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

Historical 4V lineage is preserved. D-048 was the subsequent 7V authority (2026-10-08); current authority is **D-058 / L-048 — 8V** (2026-10-19).

---

## D-048 — V-Road / 7V Core + Extended V-Gates
**Status:** SUPERSEDED — historical 7V owner LOCK, preserved verbatim below for lineage  
**Owner approval:** 2026-10-08  
**Supersedes:** D-047  
**Superseded by:** D-058 / L-048 — canonical 8V (2026-10-19)

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

## D-052 — Latency Observability from Day 1
**Status:** LOCKED  
**Owner approval:** 2026-10-11

Kerani must instrument response-time evidence from the first executable implementation slice rather than adding latency observability only after the system becomes visibly slow.

**Required per-request evidence, where applicable:**
- request received timestamp / request ID;
- queue wait;
- AI/tool-router time;
- selected tool execution time;
- deterministic/domain validation + storage time;
- retry count;
- retry-wait time;
- outbound reply time;
- total user-visible response time;
- relevant channel/runtime/provider/tool/error classification.

**Required aggregate evidence:** at minimum P50/P95/P99 total latency, error rate and retry rate, with segmentation by tool/channel/runtime/provider where meaningful.

Canonical principle:

> **Measure before optimize. Every request must expose enough timing evidence to locate latency by stage.**

**Boundary:** This is an observability/viability requirement, not a provider selection. It does not decide whether Kerani uses Apps Script, Cloudflare, Cloud Run, OCI, Gemini, OpenAI, Python, n8n, Botpress or another runtime/provider.

**Architecture consequence:** response-time comparisons and future optimisation must use factual timing receipts rather than only subjective “slow/fast” impressions. Telemetry semantics may evolve, but any material change should remain versionable/comparable.

---

## D-053 — Minimum User Value Gate / Definition of Delivery
**Status:** LOCKED  
**Owner approval:** 2026-10-11

Kerani is not delivered merely because implementation completes. Final delivery must re-check a minimum user-value gate covering:
- acceptable measured user-visible latency;
- trustworthy dynamic-language routing;
- proven tenant isolation;
- evidence-based direct READ vs durable queue boundary;
- sustainable control-plane cost/maintenance.

Two additional current multi-user hypotheses must be challenged before delivery:
- user-owned Google Drive OAuth as an optional data-ownership/storage path;
- robust, responsive AI API failure fallback/recovery without assuming a specific provider/mechanism.

Premium/customer-owned Apps Script edge is deferred from the current delivery definition. After real multi-user experience, Premium architecture must restart from ZERO → ARCHITECTURE in a separate repository/project.

---

## D-054 — Convenience-First UX and Evidence-Led Premium
**Status:** LOCKED  
**Owner approval:** 2026-10-11

Two product principles are authoritative for the current Kerani multi-user project:

> **User buys convenience and usefulness first; ownership is secondary unless it solves a real pain.**

> **Premium must emerge from observed demand, not architectural imagination.**

### Current UX priorities

Kerani multi-user should optimize for:
- friction onboarding as low as practical;
- value becoming visible quickly;
- top-up being easy and understandable;
- usage continuing without forcing migration to another system;
- strong latency / accuracy / trust;
- support for the channel users actually want.

### Product boundary

Do not force user-owned infrastructure, BYO integrations, data-ownership complexity or Premium architecture into onboarding unless real user evidence proves that those features solve a meaningful pain.

Hosted Kerani + top-up is a valid long-term user path if that is what users prefer.

Premium architecture remains future work and must be shaped by observed user behaviour after real multi-user usage.

---

## D-055 — Free Core Independent Utility; AI as Optional Convenience
**Status:** LOCKED  
**Owner approval:** 2026-10-12

**Decision:** **Free Core must remain useful on its own. AI is an additional convenience/interpretation capability, never a prerequisite for the basic application to operate.** This explicitly reinforces D-016/L-011, D-013/L-008 and D-015/L-010 without replacing their boundaries.

**Consequences:** Purchase, Sale, Inventory, Observation and Task baseline workflows plus basic retrieval/reporting and available receipt/manual input must retain a usable no-AI path. AI interpretation and bounded tools may improve natural-language UX, but AI/provider failure or quota exhaustion must not make essential Free Core functionality inaccessible. Authoritative business operations continue to require deterministic/domain rules, authorization/scope, confirmation where applicable, audit and idempotency; AI/tool calls cannot become business authority. Existing convenience-first UX remains mandatory: a no-AI pathway must be usable, not merely technically possible.

**Architecture boundary:** This locks a product/authority invariant, **not** deterministic parser implementation, deterministic-first language coverage percentage, a provider, AI failover routing, storage, queue/service mix, control plane or PRE-ARCH. Those remain evidence-bound AC-010/AC-012/E-016 challenge topics.

---

## D-056 — AI-first Verbal UX + Hybrid Active Fallback Trial
**Status:** CANDIDATE — OWNER-SELECTED TRIAL, NOT ARCH LOCK  
**Owner direction:** 2026-10-12

**Proposed direction:** Kerani's conversational DNA should be **AI-first for ordinary free-text messages**. If the request is an explicitly selected menu/form/structured operation, bypass AI using deterministic-first execution. Do not repeat OpsMate's inefficient retry/poll UX or grow fragile keyword trees merely to avoid model inference. Optimise Free AI latency/quality first (short context, bounded tools, timely acknowledgement, safe progress updates/chunking and budget-aware provider choices), then consider a selective model/provider swap or revised hybrid only if evidence requires it.

**Hybrid active fallback:** if a model is unavailable, slow, rate limited or quota exhausted, use limited time/cost/privacy-budgeted alternate AI where justified, or automatically offer/advance a usable deterministic Telegram form/menu/manual entry pathway. A no-AI path is also available proactively at any time (passive access). **Deterministic business validation, authorization and authoritative persistence remain ALWAYS ACTIVE** behind either primary interaction path. A failed AI call cannot grant mutation authority, fabricate success, duplicate a write, or erase the request.

**No redoing OpsMate:** existing OpsMate source/tests/confirmed behavioural proof receipts are first-class *reuse evidence*; E-016 must not rerun the same entire Purchase domain workflow across four model modes merely for comparison. Test only unproven Cloudflare/Google infrastructure, new bounded tool/provider adaptation, 429/5xx/timeout, Telegram UX and tenant-failure boundaries with minimal synthetic fixtures. Never represent unverified behaviour as proven.

**Compatibility:** D-029/L-023 stays LOCKED (deterministic where AI adds no value), D-015/L-010 and D-055/L-046 stay LOCKED. Architecture routing/provider/chunking selection and exact thresholds remain candidate until evidence, Challenge and owner PRE-ARCH gate.

**Evidence:** `docs/TALORYS_CLOUDFLARE_GOOGLE_FALLBACK_EVIDENCE.md`; Q-038/R-037; AC-010/AC-012; E-016.

---


## D-057 — Telegram Mini App as First-Class Deterministic Free UI

**Status:** LOCKED — PRODUCT / UI PRINCIPLE (not PRE-ARCH selection)  
**Owner approval:** 2026-10-16

**Decision:** Kerani SuperBasic shall support a **first-class, independently usable deterministic interface** alongside conversational Telegram chat. **Telegram Mini App is the approved target UI surface** for structured Free Core operations, rather than merely an emergency screen shown when AI fails. Both surfaces must access the **same bounded Core/business API contracts, trusted tenant identity, authorization, validation, idempotency, audit and authoritative business records**. The primary conversational experience remains the AI-first free-text *candidate trial* in D-056, not newly LOCKED as a provider/router architecture here.

**Dual-surface interaction invariant:**
- **Chat:** natural-language interaction; bounded AI intent/candidate tools where relevant; D-015 human/validator authority remains.
- **Mini App:** explicit forms/menu/history/summary and other deterministic Free Core operations **without compulsory AI inference**.
- **Hybrid active fallback:** if AI is unavailable/slow/quota-exhausted, Kerani should provide an actionable structured continuation via Mini App or smaller Telegram menu/wizard when practical, keeping unsaved data as drafts and never pretending a write succeeded. The Mini App is also proactively accessible when AI is healthy.
- **Thin UI:** Telegram Mini App is a replaceable presentation surface, not a parallel business system or a separate Source of Truth. Backend verifies signed Telegram WebApp `initData`, maps the user to trusted tenant context, and enforces server-side scope and mutation gates. Never trust `initDataUnsafe` or browser-submitted tenant ID as authority.

**V0.1 candidate scope for evidence:** record/create, view/history, receipt entry and basic summary; first Agro demo delta may be one small **Rekod Aktiviti Kebun** form reusing proven OpsMate data/validation. **These exact screens and their order are CANDIDATE, not frozen requirements.** Trial Telegram menu button (`/setmenubutton`) before deciding whether Main Mini App registration (`/newapp`) adds value; both require an HTTPS-hosted web front end. Cloudflare Pages Free is only a hosting CANDIDATE; central runtime/provider and API remain governed by E-016.

**Sequence/stop rules:** finish OpsMate PILOT_REAL handover and evidence freeze first. Generate a clean separate Agro Demo without BSE secrets/data; do not make Mini App mandatory for the first Wan/Hamidun demo. Introduce one bounded UI slice only if it does not destabilize the demo or require speculative backend redesign. A generic cross-product Mini-App Shell for CrossAI/Temaya/Kerani is **DEFERRED** until real demonstrated reuse (D-002), and CrossAI Companion is not restarted by this decision.

**Does not lock:** Cloudflare/GAS/OCI/VPS hosting, `/newapp` vs menu entry, final layouts, exact UI components, UI framework, database/queue, E-016 outcome, AC-010/AC-012, implementation task, Challenge PASS or PRE-ARCH. All remain evidence-bound.

**Lineage:** D-015/L-010; D-016/L-011; D-029/L-023; D-055/L-046; D-056 (CANDIDATE); Q-039/R-038; E-016; ZASSIMPLE DESIGN/ACTION_PLAN.

---

## D-058 — V-Road 8V Core + Extended V-Gates: VALID First, VERBAL Word-of-Mouth
**Status:** LOCKED — OWNER APPROVED BUSINESS / DEVELOPMENT PHILOSOPHY  
**Owner approval:** 2026-10-19  
**Supersedes:** D-048 / L-041 (7V core and its growth-stage semantics); prior D-047/L-040 (4V) remains historical.

### Canonical 8V

> **VALID → VALUE → VERBAL → VOLUME → VENTURE → VIRAL → VARY → VERSATILE**
>
> **No V is free. Every V must be earned with fit-for-purpose real-world evidence.**  
> **Jangan kejar jadi besar. Buktikan berguna, kemudian berkembang kerana pengguna benar-benar merasai nilainya.**

This is a **business and development-maturity philosophy**, not an implementation runtime, guaranteed sequential calendar, release claim, or AI/business database validation rule. Meaningful changes in scope, audience or context may require a return to VALID; learning loops remain welcome.

1. **VALID — practical solution proof FIRST.** Identify a concrete real-user problem, develop a possible solution and run **repeated experiments and iterations on actual use cases** until there is sufficient evidence it **truly works, is useful, effective, usable and worth continuing**. A technical PASS, prototype or a single synthetic test alone does not establish VALID. If evidence fails, improve, pivot or stop; repeat when assumptions change.
2. **VALUE — experienced user benefit.** Pilot testers and then several real users **feel tangible value** from repeated practical use: problem solved, effort/time/errors reduced, usefulness over their current alternative. Provider intent, claimed feature value or an enthusiastic demo do not substitute for real user outcomes.
3. **VERBAL — authentic Word-of-Mouth.** Users who experienced VALUE voluntarily tell others, recommend and discuss the solution. Measure real referrals/testimonials rather than developer announcements or manufactured hype. **This VERBAL is growth-by-human-recommendation**, distinct from existing *Verbal UX* (natural-language AI/chat interface), which continues as a cross-stage product design discipline.
4. **VOLUME — repeated adoption.** More real users, completed valuable workflows, retention, useful records and demand demonstrate growing usage, not merely sign-ups/downloads or publicity.
5. **VENTURE — evidence-backed growth partnership.** Credible VOLUME makes the project more persuasive to partners, sponsors, funders, collaborators and channels for expansion. Partnership must not surrender tenant identity, user data authority, independence or replaceability.
6. **VIRAL — prepared and/or observed wider spread.** Organic growth can begin before formal Venture, but the **chosen business development path** places VENTURE before deliberate large-scale VIRAL growth. Claim VIRAL maturity only with evidenced onboarding capacity, quota/backpressure, privacy, reliability, sustainable cost, monitoring and truthful degraded operation.
7. **VARY — real-world adaptation.** Handle demonstrable differences in customer needs, channels, domains, costs, partners, providers and operating constraints without uncontrolled product/Core fragmentation; return to VALID when a materially new problem or user segment demands it.
8. **VERSATILE — proven transferability.** Independent contexts genuinely work on reusable contracts and an adaptable foundation rather than promised genericity or domain-specific copy-paste. Evidence across multiple contexts, not only architecture drawings, earns this V.

### VALID proof loop (continuous, not merely a one-time sticker)

`REAL PROBLEM → HYPOTHESIS → BUILD → FIELD EXPERIMENT → FEEDBACK/MEASURE → ITERATE/RETEST → VALID (or PIVOT/STOP)`

Minimal acceptance dimensions: **useful, effective, usable, repeatable, evidence-backed, practical within cost/effort constraints**. Trace sample cohort/use case, comparison baseline where meaningful, failed cases, iteration and verified outcome. Mark evidence as *PILOT / PARTIAL / UNVALIDATED* rather than inflating maturity. D-049's real-field-corpus and proof-reuse rules continue to apply.

### Extended V-Gates (continuous quality guardrails, NOT a ninth core stage)

Retain prior V-Gates such as **Vision, Vocabulary, Vibe, Veracity, Validation, Verification, Volition, Vault, Vulnerability, Velocity, Visibility, Viability, Vigilance, Versioning, Variability, Venue, Vendor-neutral, Value-chain and Vertical**.

**Add: VOUCH — authentic, permission-respecting user endorsement.** Users can credibly stand behind and recommend a product because they experienced its actual value. Evidence may be genuine testimonials, voluntary referrals and attributable experience with appropriate consent; never invent quotes, claim endorsement without permission or use a paid/promotional statement as if organically volunteered. **VOUCH supports and constrains VERBAL (Word-of-Mouth), but is not a ninth step.**

**Terminology boundary:** *VALID* = whole-solution usefulness/effectiveness verified by iterative real use. *Validation* = data/domain correctness and business-rule checking. *Verification* = technical/audit proof against specified behaviour. These do not replace one another. The earlier *Verbal UX* for conversational language remains a valid technical principle independent from VERBAL growth.

### Guardrails and proof progression

- No VALUE claim from prototype/functionality alone without felt user benefit.
- No VERBAL/VOUCH claim from developer marketing without genuine experience/referral proof.
- No VOLUME maturity from sign-ups alone; demand/retention/useful activity must be demonstrated.
- No VENTURE growth story without credible evidence and safeguards for user/tenant authority.
- No VIRAL readiness without cost/load/reliability/scale proof; organic referrals may occur anytime, but scale readiness must be earned.
- No VARY/VERSATILE claim by speculative abstractions or forking the Core.
- Preserve **Vital** (operationally important through voluntarily relied-upon utility) and **V-King** (aspirational “become needed, not merely known”) as destinations **outside the numbered eight stages**, not as a ninth or tenth V.
- Existing functional, safety, Free Core, AI-first candidate, OpsMate extraction and architectural approval boundaries are unchanged. This decision does **not** certify the current Kerani application as VALID or advance its execution/readiness percentage.

**Evidence/lineage:** historical D-047/L-040 → D-048/L-041 → **D-058/L-048 current**; D-049/L-042 real-field evidence; D-053/L-044 Value Gate; `ZASSIMPLE/DESIGN.md` and `ZASSIMPLE/ACTION_PLAN.md`.

---

## D-059 — Kerani Premium Business Workspace (Tenant Dashboard and Chat-to-Web)
**Status:** **CANDIDATE — PRODUCT/UX CONCEPT ONLY; NOT LOCKED**  
**Owner direction:** 2026-10-19 — Save formally, track in Linear, do not LOCK architecture or initiate build.

**Concept:** A business-specific **Kerani Premium Business Workspace** reachable through Telegram: when a user requests a business summary, Kerani delivers a readable, *source-grounded* text explanation and—when available and authorised—a **Buka Dashboard Interaktif** button/link. A thin dashboard can present tenant-specific KPIs, interactive graphs/tables, time filters/search, source-record drilldown, bounded analytic/forecast views with source provenance/uncertainty, internal tasks and authorised document links. A future Android Home Screen PWA/browser entry is **candidate only**, not a committed supported client.

**Authority and Free boundary:** Reuse the same Kerani Core/tenant data and server-side authorization as the D-057/L-047 **LOCKED Free deterministic Telegram Mini App**; do not build a second business database or let UI/AI fabricate numbers or decide permissions. Free must retain basic reports, records, Task and deterministic retrieval (D-055/L-046). Premium Operations/Intelligence D-050/D-051 remain **CANDIDATE**; neither entitlement nor pricing is locked by this idea.

**Integration boundary:** User-approved Google Drive *links* can be examined first; full Drive OAuth is a separate unproven hypothesis under D-053. Show Kerani internal Task first; external task sync is **deferred**, to be challenged read-only and then single-direction only if justified (consent, source authority, dedup, conflict/revocation audit). Telegram's verified WebApp initData cannot substitute for a separate browser/PWA session/login authority. Any link or deep link must not itself grant business-data access.

**VALID-first discipline:** Future narrow proof (not authorised now) would test `Telegram factual summary → Open Dashboard → inspect one chart/table → verify source rows` with representative non-sensitive data and real-user usability evidence. Do not build an ERP, cross-product generic Mini App shell or forecast engine without demonstrated demand. OpsMate reference handover and clean Agro Demo remain prioritised.

**Explicitly NOT selected:** architecture/runtime/hosting, web framework, dashboard layout, PWA authentication, Google Drive integration, task sync direction/backend, pricing/credits, source-data schema, deployment or production rollout. **No PRE-ARCH LOCK, no implementation tasks, no tests PASS, no readiness-progress increase.**

**Evidence:** `docs/KERANI_PREMIUM_BUSINESS_WORKSPACE_CANDIDATE.md`; Linear tracking issue `KAI-7`; lineage D-057/L-047, D-050, D-051, D-053/L-044, D-054/L-045, D-055/L-046, D-058/L-048.

---

## D-060 — Modular Cost, Tenant Drive, AI Data Policy and Concurrent Resilience
**Status:** **CANDIDATE — ZASS REVIEWED, NOT LOCKED**  
**Owner direction:** 2026-10-22 — discuss, ZASS, save and commit concept; **no PRE-ARCH, provider, pricing or implementation LOCK**.

**Owner proposals (DUMP):**
- One Kerani backend/tenant identity regardless of WhatsApp, Telegram, Google Drive and AI API choices.
- Trial WhatsApp credits at onboarding, then cost-reflective paid WhatsApp transport; Telegram remains the economic channel.
- Optional use of tenant-owned Google Drive, with additional hosted Kerani Cloud storage paid; avoid forcing every user into a large hosted plan.
- Free AI vs Paid AI as transparent opt-in data/processing/quality choices with provider-specific terms; avoid unnecessary charges while keeping legitimate data safe.
- Database + AI API must not jam under large simultaneous tenant access; no lost/duplicated business records or silent AI failure.

**Distilled preferred challenge direction (NOT selected architecture):**
1. **Separate transport/channel credits from channel-neutral AI capability credits.** Validate Meta/BSP provider-specific billable events, actual cost/markup, welcome allowance and account migration. **D-025 remains LOCKED**; a full end to ongoing shared WhatsApp Free could need an explicit owner commercial-policy supersession.
2. **Separate minimal authoritative operational data from optional file/document storage.** Keep tenant-linked hot transactional records, authorization, ids, audit, idempotency and query indexes behind one Kerani Core contract. Explore user Drive for receipts, documents, export and backup, not as an assumed concurrent database replacement. OAuth is unapproved and must be challenged.
3. **Keep permanent useful Free records and basic access.** A cloud onboarding bonus may expire, but a model with no durable Free base after trial contradicts D-016/D-020/D-024/D-055 and D-018 portability. Paid Kerani Cloud adds justified storage/retention/media capacity; exact units and policy OPEN.
4. **AI privacy and cost choice is governed by actual provider terms.** Free AI eligibility depends on tier/endpoint and the nature of submitted data; a blanket “agree to training” checkbox cannot override provider prohibitions on confidential/personal/sensitive information. Paid API protections and data residency/retention must be contract-specific, not assumed. If no compliant AI route is available, remain truthful and provide deterministic Free functions.
5. **Classify load, not all requests alike.** Direct, authorised basic READ should avoid avoidable queue/AI latency. Mutation operations use scoped validation, consent when relevant, durable admission/receipt when evidenced, idempotency and reconciliation. AI requests use provider/tenant concurrency and token budgets, deadline/backoff, safe permitted fallback and bounded background work; protective backpressure and monitoring prevent cascading stall.
6. **VALID-first commercialization:** Trial one understandable set of options with real users; measure cost per useful record, consent/privacy comprehension, P50/P95/P99, outage/replay data correctness and unit economics before commercial or architecture LOCK.

**Alternatives rejected as default assumptions:** all-inclusive compulsory paid subscription; Drive as the universal live transactional database; universal queue for every GET/READ; deleting or blocking basic customer records when trial ends; routing all customer confidential data to Free AI solely on blanket consent; charging a failed AI request as a delivered result.

**Must preserve:** D-016/017/018/020/023/024/025/027/029/030/052/053/054/055/057 (LOCKED); D-050/051/056/059 (CANDIDATE). This review does **not** silently supersede any L-xxx. E-016/E-018 and new Q-040–Q-044 / R-039–R-043 remain OPEN.

**Evidence/extended analysis:** `docs/KERANI_CHANNEL_CLOUD_AI_RESILIENCE_ZASS_CANDIDATE.md`; Linear `KAI-8` (BACKLOG).

**Explicit exclusion:** No Claude, agent industry trend, competitors, Krani.ai or trademark discussion is included in this ZASS decision.

**Execution status:** Documented only, no customer data, paid transaction, AI provider call, Drive authorization, database/queue/service change, benchmark receipt or deployed feature.

---

## D-061 — Free Chat-First, Business/User Identity & User-Created Telegram Group

**Status: LOCKED — OWNER-APPROVED PRODUCT/UX SCOPE & PROOF GATE (NOT PRE-ARCH)**  
**Owner approval:** 2026-10-23.  
**Scope:** Kerani AI Free launch sequencing, registration, lightweight group coordination and supported/unverified Telegram UX boundaries. **NOT** a guarantee that a plain `@mention` works or that a Telegram bot has been tested.

**Decision:**

1. **Free = personal chat bot first**, with basic Purchase/Sale/Inventory/Observation/Task/retrieval/report workflows and ordinary tenant-scoped business validation. Avoid OpsMate group management complexity in Free. Telegram Mini App D-057/L-047 **remains LOCKED as a first-class deterministic Free surface**, but is not a mandatory form or launch-blocking prerequisite for initial personal chat; separate follow-up slice.
2. **Mandatory onboarding:** business/company name, backend-assigned durable Kerani Business ID and Kerani User ID, bind trusted Telegram user identity. More Free users may be affiliated with the same Business ID via a verified enrollment/invite; knowing an ID or being in a group **never authorizes access by itself**. No default hierarchy of Owner/Admin/Supervisor/Worker in Free.
3. **Free multi-user overlap:** when backend knows *more than one verified active Free user* for the same Business ID, show a simple, non-blocking warning about possible independent duplicate reports and tips to create their own Telegram group, add bot and address it explicitly. **Do not perform AI/semantic comparison or automatic reconciliation/merge/discard between separate workers' reports.** Preserve cheap **transport retry / same-update idempotency** and record validation for ALL tiers.
4. **User-created group:** User creates and administers normal Telegram group, optionally adds KeraniBot; Kerani only securely binds a permitted Telegram Group ID to the Business ID and checks each actor's right to request or disclose reports. It does not create groups, manage company roles or need all group messages as default.
5. **Preferred UX to prove:** `@KeraniBot rekod Baja out N M1P12 1 set` and `@KeraniBot jana report bulan ni`. **NOT TESTED / NOT GUARANTEED under Privacy Mode ON**; Telegram official FAQ confirms `/command@bot` and replies, but does not establish reliability of plain mentions for bot update delivery. Do not claim PASS or quietly switch Privacy Mode OFF/elevate group admin.
6. **Fall back if mention fails:** user selects `/rekod@KeraniBot` or `/report@KeraniBot` from Telegram command menu (command is sent) → bot sends targeted `ForceReply` prompt such as “Balas mesej ini untuk rekod/report” → user replies in natural text. A normal slash-command menu is not known to offer native *compose-only without send*; Inline Mode prefill is an optional separate experiment, not a locked solution.
7. **Concurrency safety without semantic dedup:** group/chat ID + trusted Telegram user ID + bot prompt/reply-to-message ID + bounded request state route each user's reply; normal tenant scope, validation, auditable receipt and same-transport-event idempotency remain mandatory. This is low-level correctness, **not Premium team reconciliation**.
8. **Premium boundary:** company/team roles, coordinated worker approvals, semantically detecting equivalent reports, automatic reconciliation and larger group operations are outside Free baseline, future Premium/domain **CANDIDATES** only (not automatically required or priced by this LOCK).

**Mandatory proof BEFORE actual group UX selection or deployment:** T01 privacy-ON plain mention; T02 privacy-OFF isolated comparative test (never default silent change); T03 native slash auto-send and delivery; T04 `ForceReply` targeted privacy-ON; T05 two users' concurrent replies and update retry idempotency/tenant rights; T06 Inline Mode UX vs ForceReply. Record real Telegram/client/update receipts and FAIL/NOT TESTED candidly. No tests are reported as PASS by this documentation LOCK.

**Compatibility / authority:** D-015 (record/confirmation/validation gates), D-016 (Free record utility), D-023 (independent Business ID), D-052 (timing), D-055/L-046 (Free no-AI), D-057/L-047 (Free Mini App), D-059 and D-060 (candidate only). This LOCK does not select runtime/database, pricing, credentials, API, bot Privacy Mode, domain role model or PRE-ARCH, and does not start implementation.

**Evidence:** `docs/KERANI_FREE_CHAT_GROUP_UX_D061.md`; Telegram official Bot FAQ/Features/Bot API ForceReply; Linear `KAI-9`.

---

## D-062 — RekodUntung.ai Primary Brand Name Candidate (NO REBRAND)

**Status:** **PRIMARY NAME CANDIDATE — NOT LOCKED / NOT DECIDED BRAND IDENTITY**  
**Owner approval:** 2026-10-23 **to promote candidate, save documentation and commit only**.  
**STOP:** **Do not rename, rebrand or otherwise migrate `dzuddiyn/Kerani_Core_SuperBasic`, production bot/product identity, code, package, deployment, domains, usernames or external marketing until MyIPO and domain clearance and later explicit owner approval.** This D-062 does not create any brand LOCK (L-050 is later assigned to unrelated D-064, a WhatsApp pilot sequencing decision).

**Candidate ranking:** `RekodUntung.ai` is the leading name to investigate as a future brand for the current Kerani AI product. This promotion is not proof of registrable domain ownership, trademark safety, user preference or actual profitability calculations. Prior brainstorming options (MudahKiraUntung.ai, KiraUntung.ai, MudahUntung.ai, SenangUntung.ai, RekodMudah.ai) are historical alternatives, not an approved naming change or legal clearance.

**User-value rationale:** The Malay words `Rekod` (the Free chatbot's basic recording/retrieval tasks) and `Untung` (the entrepreneur's hoped-for benefit) make the purpose easier to grasp than names focused on “AI”/“chat”. However Free Core's D-016/D-061 Purchase/Sale/Inventory/Observation/Task and basic reports are **not a guarantee of net-profit accounting or positive financial outcomes**.

**Brand collision concern:** Kerani AI / Krani.ai naming proximity triggered reconsideration, and other adjacent `KiraUntung` naming was noted in earlier conversation. These are **unverified brand-risk signals**, not MyIPO trademark findings or definitive legal conclusions.

**Must complete before requesting a BRAND LOCK:**
1. **G1 MyIPO:** current official search of exact/close marks, relevant classes/owners/status and similarity; escalate to qualified trademark review where needed.
2. **G2 Domain:** live registrar availability and ownership/renewal pricing for `rekoduntung.ai`; optional compatible `.my`/`.com.my` and handle alternatives.
3. **G3 Product truth and market confusion:** assess near-name competitors and test whether Malaysian micro-SMEs understand it as recordkeeping rather than a promised profit calculation.
4. **G4 Explicit owner decision:** return evidence for GO/NO-GO. **Only then** consider name LOCK and separately approved migration/branding actions.

**Allowed scope of this GitHub session:** add a documentation candidate note, record D-062 and optional ZASSIMPLE candidate projection, and reconcile commit SHAs to Linear. This does **not** change the repository slug/current name or executable assets, and does not start buying domains, registering trademarks, changing bot handles or implementing features.

**Evidence and tracker:** `docs/KERANI_BRAND_REKODUNTUNG_PRIMARY_CANDIDATE.md`; Linear `KAI-10`; Q-049/Q-050/Q-051; R-048/R-049. MyIPO and domain are **NOT VERIFIED** in this candidate record.

---

## D-063 — WhatsApp Edge Quota Guard (95%/99%) & Cloudflare Fast Scheduler

**Status:** **CANDIDATE — OWNER AUTHORISED SAVE/COMMIT PREVIEW ONLY (NOT LOCKED / NOT PRE-ARCH)**  
**Captured:** 2026-10-24.  
**Proposal:** A Cloudflare Worker may adapt inbound/outbound WhatsApp Cloud API traffic for Google Apps Script Core, enabling centralized signature verification, tenant/phone mapping, transport idempotency and monthly service-message budget protection. **950** (95%) is a warning/conserve candidate; **990** (99%) is a routine-outbound stop candidate; last **10** are a separately controlled/unapproved buffer. No entitlement, billing policy or production limit is locked by this note.

**Evidence-backed distinction:** Official WhatsApp Business FAQ confirms effective **2026-10-01** Meta charges for service messages beginning at the **1,001st service message per business phone number/month**; this does **not** apply to all incoming/outgoing message types, and template messaging/BSP costs are separate. Delivery status and actual provider usage may lag an application ledger, so a Worker cannot promise zero Meta charge if other senders bypass it. `https://whatsappbusiness.com/resources/faq/`

**Latency/scheduler challenge:** The minimum Apps Script time-trigger interval is **one minute**; `doPost()` already supports immediate HTTP webhook-driven execution, so Cloudflare is not magically required to “bypass” `doPost` latency. Cloudflare Cron is also minute-based; Cloudflare Queues can consume event-driven with batch timeout 0–60 seconds (default 5), while Durable Object Alarms support scoped finer-grained future wakeups with at-least-once semantics, **not hard-real-time guarantees**. An HTTP Worker can add safe edge acknowledgement/routing and a durable Queue/DO path when proven necessary, but `ctx.waitUntil()` alone must not be treated as durable transaction admission.

**Three options for E-016 delta-only challenge:**
- **A — Apps Script direct `doPost` + supported lock/counter ledger** (simplest baseline).
- **B — Cloudflare Worker inbound/outbound adapter + Apps Script**, with atomic quota/delivery ledger design still to be proved (**preferred candidate for pilot only**, not chosen).
- **C — Worker + D1 conditional atomic quota ledger or per-number Durable Object + Queues when necessary + Apps Script**, for reliability/burst proof; do not create a second business Source of Truth.

**Critical gates:** Signature verification, protected Worker→Apps Script envelope and server-side tenant authorization; idempotency for duplicate Meta webhook; per-number + billing-period quota reservation before *each eligible outbound send*; reconciliation for accepted/delivered/failed/unknown sends; no silent customer record loss or false “saved” receipts; no cost-bearing “quota exhausted” notice once quota is unavailable. Preserve all existing Free/Core/transport policy LOCKs, particularly **D-025/L-019**, **D-027/L-021**, **D-055/L-046**, **D-057/L-047**, **D-061/L-049**. This idea supplements **D-060 CANDIDATE**, does not supersede it or select infrastructure/commercial terms. Brand D-062 is unrelated.

**Proposed future synthetic proof `CF-WA-QG-01`** (NOT EXECUTED): T01 ten concurrent sends at 989/990; T02 duplicate webhook; T03 Apps Script timeout/unknown send; T04 direct webhook vs retry via Queues/DO Alarm vs 1-minute polling with P50/P95/P99; T05 month boundary/95–99% notification and template/BSP bypass; T06 forged/replayed signature/tenant scope; T07 queue retention/DLQ; T08 total complexity/economic comparison. **No PASS, production test, account configuration, actual call, deployed code, new execution task or PRE-ARCH lock.**

**Detailed evidence:** `docs/KERANI_WA_EDGE_QUOTA_GUARD_ZASS_CANDIDATE.md`; existing Linear tracker **KAI-8** (channel credits, cloud/AI resilience). **NEXT:** separately approved *synthetic-only* CF-WA-QG-01 challenge before selecting architecture.

---

## D-064 — Queue-Ready WhatsApp V1→V2 Pilot Migration Strategy

**Status: OWNER LOCKED — CONDITIONAL ARCHITECTURE SEQUENCING / COMPATIBILITY CONTRACT (L-050)**  
**Owner explicit approval:** 2026-10-24 — *“condong kepada A untuk pilot kecil, direka supaya serasi dengan B. Kalau ujian menunjukkan Apps Script kerap timeout atau webhook ACK berisiko kehilangan kerja, terus pilih B sebelum membuka penggunaan sebenar.”*

**LOCKED:**
1. **Pilot V1 preference (A):** `WhatsApp → Cloudflare Worker → protected Google Apps Script` for a small pilot, **only when tested safe**. Worker is the single inbound Meta verification/routing boundary and single outbound WhatsApp/quota gate; Apps Script owns the same deterministic business rules/validation/authoritative Core.
2. **Queue-ready Day 1:** Versioned, trusted **Job Envelope**, stable source-scoped job ID, transport-independent `dispatch(job)` and `processJob(job)` boundary, server-resolved Business/User membership, authoritative same-event idempotency, non-fabricated processing and outbound delivery states. Both Direct and future Queue consumer must execute **the same Core contract**; Queue must not become a second business SoT. **Exact example field names, persistence selection and signature method are not locked.**
3. **V2 safety fallback (B):** `same WhatsApp webhook URL → same Worker → Cloudflare Queue → consumer → same protected Apps Script processJob → same Worker outbound gate`, activated only via separately approved/tested migration. Stable records/IDs/schema stay; there will be code/config changes for Queue and consumer but **no planned customer data reset or wholesale Core rewrite**.
4. **Pre-live STOP/ESCALATE:** If V1 Apps Script repeatedly times out, lacks safe Meta webhook ACK before deadline, or has unacceptable loss/duplicate risk, **do not open live use on V1**. Move to B for the initial live rollout **only after** synthetic acceptance/security and owner deployment approval. A webhook `HTTP 200` or Queue admission is never a `SAVED` business receipt.
5. **Migration integrity:** at-least-once retries, Queue reordering, unknown Meta sends, direct/Queue canary and rollback must protect one authoritative record per unique event, preserve independent worker records, avoid dual dispatch/duplicate outbound, and reconcile backlog before switching.
6. **Scope of LOCK:** narrow *WhatsApp pilot sequencing and migration invariants only*, **not** whole-project E-016 PRE-ARCH, final transport quota thresholds (D-063's 950/990 still candidate), final Job schema/backend/DB/Queue design, Meta costs, release timing, implementation or production deployment. Preserve D-025/L-019, D-027/L-021, D-055/L-046, D-057/L-047 and D-061/L-049. D-060 and D-063 remain CANDIDATE for their other details; D-062 RekodUntung.ai still is **NOT BRAND LOCK**.

**Evidence / future proof:** `docs/KERANI_WA_QUEUE_READY_V1_V2_D064_LOCK.md`; DESIGN and ACTION_PLAN projections; Q-056–Q-058/R-054–R-056; Linear KAI-8. Synthetic CF-WA-QG-01A/01B remains **NOT RUN**; no performance, cost or safety PASS claimed.

**NEXT — exactly one:** CF-WA-QG-01B — Queue-Ready Contract & Synthetic Reliability Challenge: design-first, tests only on separate authorization, validate V1 safety and V2 promotion gates before provider selection/deployment.

---

## D-065 — OpsMate Lessons → Mandatory Kerani Release Gates (RG-01/02/03)

**Status:** **OWNER LOCKED — THREE P0 RELEASE/READINESS INVARIANTS (L-051)**  
**Owner approval:** 2026-10-24 — explicit `LOCK D-065/L-051 & COMMIT`.  
**Source:** Owner reported three OpsMate weaknesses after approximately 1½ months of development: loss/breakage when cleaning mock/test Sheets data or promoting versions; no useful almost-live user dashboard; AI extraction should not scan dozens of raw Sheet tabs. **These are experience reports, not a code-level root-cause audit.**

**LOCKED RELEASE GATES:**
1. **RG-01 — Upgrade Integrity / No Regression (P0).** Before promoting a stable/live Kerani version, prove clean isolation of dev/mocks, staging, required schema/seeds/config and user authoritative records, plus empty-data/first-run, after-mock-purge baseline CRUD/retrieval, old-data migration and verified rollback/forward recovery. No missing previously supported features, broken integrity or deleted customer records. Versioned configuration is NOT disposable fixture data.
2. **RG-02 — Visible Value / Free Dashboard (P0).** Each supported Free tenant must be able to see their **committed** recent records, appropriate basic summary/KPI/activity/stock/task status and freshness/last-sync evidence via simple tenant-authorized mobile UI, preferred D-057/L-047 Telegram Mini App; no compulsory AI prompt, paywall or Premium dashboard just to view existing Free records. A committed record must become visible and traceable, with stale/pending/error state when projection lags. Provisional pilot target **P95 commit-to-fresh-display ≤5s** is a **test hypothesis only**, not a hard-coded locked SLA or tested result. Sheet dashboard may assist admin/prototype; exact UX/framework/PWA is OPEN.
3. **RG-03 — Knowledge-Ready Data / Grounded Retrieval (P0 for any shipped AI/query/summary capability).** For released AI/summary features, retrieve from **bounded, tenant-scoped structured read models/summary APIs** with source IDs, time range, version/watermark and freshness, not scanning dozens of tabs per question. Backend derives deterministic totals; AI may explain but not invent numbers, replace authority or disclose another tenant. **ONE authoritative Core Source of Truth**; read model is rebuildable projection, not parallel mutable business database. AI provider outage must not break useful basic no-AI Free flows, D-055/L-046.

**FAIL RELEASE:** untested/failed upgrade and cleanup preservation; committed record invisible, stale-but-unlabelled or wrong/cross-tenant dashboard values; a delivered AI/summary capability unable to present permissioned source-grounded data. Distinguish **RG-03 conditional on the shipped AI scope** from mandating optional AI availability for launch. No test is proven PASS by this owner LOCK.

**Compatibility:** D-015 confirmed validation and SAVE, D-016/L-011 Free basic reports, D-023 tenant identity, D-052 measurable latency, D-055/L-046 independent no-AI Free utility, **D-057/L-047 Free deterministic Mini App**, D-061/L-049 chat-first onboarding and D-064/L-050 queue-ready WhatsApp V1→V2 remain intact. **D-059 Premium Business Workspace remains CANDIDATE for advanced exploratory analytics**, not a prerequisite to Free visibility; D-062 RekodUntung.ai stays brand candidate. E-016 runtime, storage/read-model technology, exact screen design, Cloudflare/Sheets integration, browser/PWA authentication and performance target are NOT selected.

**Proof obligations (NOT RUN):** RG-01 U01–U04 (empty/mock cleanup/version/rollback), RG-02 V01–V03 (committed record→source-visible, freshness/authorization and latency) and RG-03 K01–K04 (scoped grounded query, bad/stale/empty data, rebuild/reconcile, comparative tab-scan/latency/cost). See `docs/KERANI_OPSMATE_RELEASE_GATES_D065_LOCK.md`; Linear **KAI-11**.

**Authorization boundary:** Decision/documentation LOCK and GitHub/Linear reconciliation only; **NO CODE, TEST EXECUTION, DEPLOYMENT, REBRAND, PROVIDER SETUP, PRICING, PRODUCTION OR CUSTOMER DATA** actions.

**NEXT — exactly one:** RG-01/02/03 Synthetic Acceptance Matrix & Minimal Vertical Slice Design (read-only design; seek approval for actual testing/implementation).

---

## D-066 — Freeform Input → User-Controlled Google Sheets Export as a Core Product Principle

**Status:** **OWNER LOCKED — PRODUCT SIMPLICITY + DATA PORTABILITY (L-052)**  
**Owner approval:** 2026-10-26; original direction: *“tiada logic algorithm rumit; user boleh masukkan apa saja data; data akan terus diekstrak daripada database ke dalam sheet ... Google Drive; pengguna bebas lampirkan ... untuk dianalisis oleh AI lain atau edit sendiri atau padam.”*

**LOCKED owner value:**
1. **Record first, no unnecessary algorithms.** Accept broadly useful user-entered freeform data/notes, preserve raw content and minimal trusted metadata in Kerani's authenticated tenant-scoped authoritative Core. Do not force complex categorization, profit algorithms or domain workflows for an ordinary note; nonetheless retain D-015 validation/confirmation/idempotency for any consequential Sale/Purchase/Inventory or other authoritative business action. "Apa saja" is a UX intention, not permission for unsafe/unbounded input or automatic unverified accounting classification.
2. **Database → Google Sheet.** Offer an automatically produced, accessible Google Sheets export/projection in the **user-authorized Google Drive**, updated after actual Core COMMIT with visible sync/freshness/error state, recoverable without data loss. The export remains a user-facing copy, **not Kerani's transactional or second business Source of Truth**. Precise refresh latency, API/OAuth/connectors, spreadsheet schema and runtime **remain OPEN**.
3. **Data freedom.** Users can download/share/copy/attach their Sheet to **other AI applications at their own choice**, independently edit or delete Sheet files and revoke access. Export and basic personal data portability must not be a Premium-only lock-in. Kerani must not silently upload customer data to third-party AI.
4. **No hidden two-way edits/deletion.** Edits or deletion of a Sheet **do not silently mutate/delete authoritative Kerani records**. Automatically refreshing managed projection must not silently overwrite user-edited cells or recreate a deleted Sheet without consent. Whether to use a managed live export + detached personal editable copy or separated generated/user ranges/conflict policy requires evidence and user-facing clarity, **not preselected by this LOCK**.
5. **Compatibility with Free/reliability:** Preserve D-018 portability, D-016/D-055 no-AI Free utility, D-023 tenant identity, D-057/L-047 Free Mini App, **D-065/L-051 RG-01/02/03** source-truth/read-model/visible-value gates, and D-064/L-050 WhatsApp queue-ready plan. Google Sheets export **complements**, does not automatically replace, the mobile Free dashboard. D-060's infrastructure/Drive OAuth is still **CANDIDATE**, and D-059 richer Premium Workspace still **CANDIDATE**.

**Architecture and legality NOT LOCKED:** no new Google OAuth grants or auto-created Sheet, no direct source Drive access, no permanent storage provider selection, no 2-way Sheet editing sync, no public-by-default links, no vector DB or external AI transmission, no exact pricing/quotas/format, no app code/deploy and no acceptance PASS.

**Evidence and tests:** `docs/KERANI_FREEFORM_TO_USER_GOOGLE_SHEETS_D066_LOCK.md` (S01–S10 planned, NOT RUN), Q-062–Q-064, R-060–R-062; tracker Linear **KAI-13**.

**NEXT — exactly one:** D-066 Sheet Sync & User Edit/Delete Conflict Contract (READ-ONLY): define and compare simplest permissioned managed projection vs detached user copy and demonstrate that edit/delete does not silently change Core.

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
**Status:** SUPERSEDED — historical 7V LOCK  
**Superseded by:** L-048 / D-058 (2026-10-19)  
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

## L-043
**Source Decision:** D-052  
**Decision:** Latency observability is mandatory from the first executable Kerani slice; request paths must emit stage-level timing evidence sufficient to compare P50/P95/P99, retries/errors and latency by relevant tool/channel/runtime/provider rather than waiting for subjective responsiveness problems.  
**Locked by:** Project Owner  
**Date:** 2026-10-11  
**Supersedes:** None

## L-044
**Source Decision:** D-053  
**Decision:** Final Kerani delivery requires a minimum user-value gate: measured acceptable latency, trustworthy language routing, proven tenant isolation, evidence-based direct READ vs durable queue boundary, and sustainable control-plane cost/maintenance. User-owned GDrive OAuth and robust/responsive AI API fallback are current multi-user challenge hypotheses; Premium customer-owned edge is future work to restart from zero architecture in a separate repository after multi-user experience.  
**Locked by:** Project Owner  
**Date:** 2026-10-11  
**Supersedes:** None

## L-045
**Source Decision:** D-054  
**Decision:** Kerani is convenience-first: users buy usefulness and convenience before ownership; Premium must emerge from observed demand, not architectural imagination. Current UX priorities are low-friction onboarding, fast time-to-value, easy top-up, continuity without migration, strong latency/accuracy/trust, and support for the channels users actually want.  
**Locked by:** Project Owner  
**Date:** 2026-10-11  
**Supersedes:** None

## L-046
**Source Decision:** D-055  
**Decision:** Free Core must independently deliver basic operational value without AI; AI is optional convenience, not an operational prerequisite. No-AI/manual completion stays usable through model failure/quota exhaustion, while deterministic/domain validation and human/tenant authority always govern business truth.  
**Locked by:** Project Owner  
**Date:** 2026-10-12  
**Supersedes:** None

## L-047
**Source Decision:** D-057  
**Decision:** Telegram Mini App is the first-class thin deterministic Free Core UI alongside Telegram conversational chat, independently usable when AI is healthy and usable as an actionable hybrid active fallback when AI fails. Both interfaces use the same trusted tenant/backend authority, validation/idempotency/audit and authoritative records. Specific UI entry point, screen designs, hosting, rollout/demo priority and PRE-ARCH remain unselected.  
**Locked by:** Project Owner  
**Date:** 2026-10-16  
**Supersedes:** None

## L-048
**Source Decision:** D-058  
**Status:** LOCKED  
**Decision:** Canonical **V-Road 8V — VALID → VALUE → VERBAL (Word-of-Mouth) → VOLUME → VENTURE → VIRAL → VARY → VERSATILE**. VALID is repeated real-use experimentation/iteration until practical usefulness and effectiveness are evidenced; VALUE is felt by pilot and real users; VERBAL is genuine recommendations/referrals, not synonymous with Verbal UX. Add **VOUCH** to continuous Extended V-Gates as real user endorsement, **not** another core V. Keep Venture before deliberate Viral scaling as the strategic default, without denying earlier organic spread. Preserve Vital and V-King as destinations.  
**Locked by:** Project Owner  
**Date:** 2026-10-19  
**Supersedes:** L-041 / D-048 (historical 7V; D-047/L-040 4V already superseded)

---

## L-049
**Source Decision:** D-061  
**Status:** LOCKED — PRODUCT/UX SCOPE AND TEST-GATE ONLY  
**Decision:** Free personal chatbot FIRST; require Business name, backend-assigned Business ID + User ID with verified tenant membership, no Free role hierarchy; more than one active Free user per business triggers only a warning of possible independent report overlap (no AI semantic dedup). Users may create their own Telegram group and add the bot; a plain `@KeraniBot` natural command is the preferred **UNTESTED** group UX, with `/command@KeraniBot → targeted ForceReply → natural Reply` as supported fallback to verify in synthetic trials T01–T06. Preserve same-update idempotency, tenant authorization, and D-057 first-class Free Mini App as optional following UI, NOT mandatory chat form. No actual group/Telegram test passed and no PRE-ARCH/provider/premium-team implementation selected.  
**Locked by:** Project Owner  
**Date:** 2026-10-23  
**Supersedes:** None; D-057/L-047 unchanged.

## L-050
**Source Decision:** D-064  
**Status:** LOCKED — CONDITIONAL WHATSAPP PILOT SEQUENCE + QUEUE-READY COMPATIBILITY INVARIANTS ONLY  
**Decision:** Prefer V1 small-pilot Cloudflare Worker → protected Apps Script with a versioned authenticated Job Envelope, stable message/job ID, dispatcher/processJob interface, durable authoritative idempotency, truthful commit vs ACK and shared outbound quota gate from Day 1. Keep the same WhatsApp URL, canonical tenant/business record IDs and Core schema when adding V2 Worker → Cloudflare Queue → consumer → same Apps Script Core, without customer record reset or Core overhaul where invariants hold. If evidence shows repeated timeout, unsafe ACK before durable acceptance, loss or duplicate risk, **STOP V1 release and choose/test V2 BEFORE real usage**. Requires independent test and release approvals. Does NOT LOCK quota thresholds (950/990 still candidate), Queue provisioning, storage/auth protocol detail, full E-016 infrastructure, global PRE-ARCH, product rebranding, implementation or deployment.  
**Locked by:** Project Owner  
**Date:** 2026-10-24  
**Supersedes:** D-063's undecided WhatsApp V1-vs-V2 pilot preference **only**; D-063's other candidate questions and D-025/L-019 remain unchanged.

---

## L-051
**Source Decision:** D-065  
**Status:** **LOCKED — MANDATORY KERANI RELEASE GATES RG-01/02/03 (P0)**  
**Decision:** Do not declare an updated Kerani Free release stable or user-ready without (RG-01) tested mock/seed/config/data separation, no-regression old→new migration, rollback/recovery and no lost supported functions/records; (RG-02) verified, tenant-scoped, mobile-useful **Free** visibility of committed records and basic business summaries via first-class Free UI with explicit freshness/projection errors, rather than invisible chat-only records or a Premium-only dashboard; and (RG-03) for any released AI/query/summary capability, source-grounded bounded tenant read-model/knowledge access derived from one authoritative Core (not scans of dozens of Sheet tabs), while basic no-AI Free stays usable. Suggested P95 ≤5 s freshness is **unverified acceptance target**, not fixed SLA. Preserve D-057/L-047 Mini App, D-059 Premium advanced workspace as CANDIDATE, and D-064/L-050 queue-ready WhatsApp architecture LOCK; no PRE-ARCH/runtime/provider selection or tests PASS.  
**Locked by:** Project Owner  
**Date:** 2026-10-24  
**Supersedes:** None; formalizes readiness/release obligations and Free visible-value boundary from existing D-016/D-055/D-057.

---

## L-052
**Source Decision:** D-066  
**Status:** LOCKED — FREEFORM DATA CAPTURE + USER-CONTROLLED GOOGLE SHEETS EXPORT AND PORTABILITY PRODUCT PRINCIPLE  
**Decision:** Keep Kerani simple: accept broadly useful freeform inputs with preserved original content and minimal necessary tenant/validation metadata; maintain one authoritative Core record store; provide an automatically generated/updated Google Sheet export in user-authorised Drive with honest last-sync/errors; let the user independently copy, share, attach to external AI, edit or delete their Sheet. **Never silently interpret Sheet edit/delete as authoritative Kerani record change; never silently overwrite user edits during a managed refresh or recreate a deliberately deleted file.** Preserve useful Free exports without forcing paid AI; preserve D-065/L-051 Free dashboard, trusted read-model, non-regression and D-015 business validation. Specific OAuth, API architecture, storage, sheet edit-conflict UX, refresh SLA and integration/test/deployment remain OPEN.  
**Locked by:** Project Owner  
**Date:** 2026-10-26  
**Supersedes:** None; concretises D-018 data portability and reconciles D-060 Drive CANDIDATE and D-065/L-051 one-SoT release rules.

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
| E-016-EVOXT-P | Evoxt paid Malaysia VPS contingency | Avoid premature paid VPS and security/maintenance overhead; entry-level RAM/transfer/performance claims not tested. | Measured blocker to free/managed candidates + owner-approved capped one-month synthetic trial. |

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
- [ ] Before final architecture confirmation, follow the current project-local ZASSIMPLE flow: DESIGN 4/4 → CHALLENGE DESIGN / ARCHITECTURE → controlled revision → owner **YA, LOCK PRE-ARCH** → Execution Reality Check → real artifact/sample pack + execution-surface map → detailed ZASSIMPLE ACTION PLAN ↔ PRE-ARCH → evidence-bounded vertical atomic tasks → result/proof → delta planning + PRE-ARCH review → LAST DESIGN / ARCHITECTURE CHALLENGE → explicit owner final confirmation.

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
3. **AC-007 Cloud Run + Firestore + Secret Manager + basic Logging/Monitoring**;
4. **AC-011 OCI Ampere A1 Always Free VM** with only evidence-needed local services/queue/storage.

**Measure:** setup/maintenance effort, webhook behaviour, request latency, concurrency headroom, tenant/quota/waitlist implementation, secret handling, scheduled/async capability, observability, failure recovery, estimated low-traffic cost, free-tier/entry barriers, scale-up path and migration/rollback flexibility.

**2026-10-14 PAID SERVER CONTINGENCY (NOT FIFTH ACTIVE OPTION):** Evoxt Malaysia VPS is retained as a last-choice paid hosting escape hatch if measured barriers invalidate free/managed alternatives. Use `docs/EVOXT_PAID_VPS_CONTINGENCY.md`; do not prototype or buy proactively, and do not inflate the active four-way E-016 benchmark.

**New field signals to preserve (2026-10-11):**
- **REPORTED:** owner observed OpsMate user-visible response stalls associated with retry/poll timing after transient Gemini/provider errors such as HTTP 502; owner recalls a roughly 30-second retry/poll interval in the experienced path.
- **VERIFIED against accessible OpsMate snapshots:** TelegramWorkerTest.js at both 10e20cd... and a6b504... records API_OR_OUTPUT_ERROR as RETRY_NEEDED with Date.now()+60000*Math.min(16,Math.pow(2,job.attempt-1)), i.e. a 60-second base exponential retry in that worker snapshot. Therefore the exact 30-second interval is **not verified from the accessible source snapshot**, but retry scheduling is confirmed as a real latency amplifier.
- **REPORTED / inference (historical):** deterministic-first processing may reduce AI latency/cost, but real Telegram language variation across many users may be too broad for a brittle keyword-only approach. **2026-10-12 owner challenge direction supersedes this *testing priority*, not D-029 LOCK:** AI-first for ordinary free text; explicit form/menu/structured requests use deterministic fast path, with active fallback for AI failure.

**Required latency decomposition for E-016:**
1. channel ingress → runtime/router;
2. runtime/router → AI/provider request where used;
3. AI/provider response/failure time;
4. retry/backoff/poll delay after transient failure;
5. deterministic/domain validation + storage;
6. outbound reply/acknowledgement;
7. total user-visible P50/P95 and recovery time after 5xx/provider failure.

**Required language-variability evidence:**
- deterministic fast-path coverage on real field samples;
- misroute rate;
- clarification rate;
- AI-fallback rate;
- representative mixed-language/shorthand/spelling variants;
- prove the owner-selected hybrid distinguishes explicit deterministic fast-path from AI-first free-text interpretation; no brittle keyword explosion, no silent model misroute, no forced AI on explicitly selected forms.

**Required practical test for AC-010:** webhook → tenant lookup → quota/state update → durable/async step where needed → reply; then one scheduled trigger → reminder/report path.

**2026-10-12 refined owner scope — DELTA-ONLY:** Include Cloudflare Free vs Google Apps Script/Sheets/Gemini Free quotas, entry friction, hard-cap exhaustion, tenant isolation, runtime CPU, privacy/logging, and 5xx/429/timeout, but **do not repeat OpsMate's full Purchase business flow** in deterministic-only/Gemini/Workers AI/failure variants. First map exactly what OpsMate code/tests/proof receipts already establish; run only missing synthetic provider/tool-schema, new runtime/tenant, Telegram form and failure-recovery boundary tests. **Owner-selected challenge direction:** AI-first for ordinary free text; deterministic primary when user input is explicit; hybrid active provider/deterministic interaction fallback on failure; keep deterministic business authority ALWAYS active. Measure model latency before/after bounded prompts, timely Telegram acknowledgements and safe incremental status updates; chunking alone cannot shorten model inference time. The 80–90% no-AI type coverage remains an optional *capability-availability hypothesis*, not a target forcing model bypass. Evidence: `docs/TALORYS_CLOUDFLARE_GOOGLE_FALLBACK_EVIDENCE.md`; D-056/Q-038/R-037.

**OpenClaw note:** OpenClaw is not a fourth control-plane competitor. D-032/E-013 keeps it as a replaceable synthetic reliability/audit agent.

**OCI-specific benchmark requirements:** verify current Always Free entitlement/eligibility, ARM compatibility, webhook/process uptime, idle-reclaim exposure, host-capacity availability, OS/security maintenance burden, backup/restore, queue/retry control, observability, and a paid/alternate migration trigger.

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


## E-021 — Multi-User Value Gate Validation

**Status:** PLANNED / REQUIRED BEFORE DELIVERY

**Question:** Does the current Kerani multi-user implementation deliver enough real user value to be declared done?

**Minimum pass dimensions:**
1. measured latency is acceptable enough that users are not materially burdened;
2. dynamic-language routing is accurate/trustworthy across real field language;
3. tenant isolation is proven fail-closed for READ and MUTATE;
4. direct READ vs durable queue boundary is evidence-based rather than universal queueing;
5. selected control plane is operationally and economically sustainable.

**Additional hypotheses to test:**
- user-owned Google Drive OAuth can improve data ownership/storage without unacceptable auth/support burden;
- AI API failure fallback/recovery is robust and responsive enough under real transient/provider failures.

**Premium exclusion:** customer-owned Apps Script edge is not part of E-021. It is future work for a separate Premium ZERO → ARCHITECTURE repository after current multi-user experience.

---

## E-020 — Public GAS Agentic Pattern Audit

**Status:** EVIDENCE INPUT — CHALLENGE NOT RUN

**Question:** What implementation patterns from existing Google Apps Script + Gemini projects are relevant to Kerani's bounded Agentic Tool architecture, and should customer-owned Apps Script be treated as a separate execution/data edge rather than conflated with the central control plane?

**Sources audited:**
- `tanaikech/adk-gas`
- `tanaikech/GeminiWithFiles`
- `mhawksey/GeminiApp`

**Supported findings:**
- Apps Script can execute Gemini function/tool-calling patterns;
- Native GAS functions can be exposed as tools;
- public GAS implementations show fast-path, timeout, state/concurrency protection, logging and token/payload safeguards;
- `adk-gas` demonstrates a Human-in-the-Loop suspend/resume pattern around tool execution;
- customer-owned Apps Script is a plausible **edge role** for Google-owned customer resources, but this does not prove it should be Kerani's central control plane.

**Architecture distinction to challenge:**
- **Central Control Plane:** ingress, tenant identity, authorization/scope, quotas, routing, shared-AI policy, central audit/telemetry and cross-channel coordination.
- **Customer-Owned Apps Script Edge:** optional customer-owned execution/data edge for Sheets/Drive/Workspace APIs and optional customer-owned AI credentials.

**Constraint:** customer-owned Apps Script edge is **not** added as a fifth E-016 central control-plane candidate. E-016 remains a four-way central benchmark.

**Not proven by this audit:** Kerani production scale, tenant-isolation correctness, latency target, or superiority of Apps Script over Cloudflare/Cloud Run/OCI.

**Evidence note:** `docs/GAS_AGENTIC_PATTERN_AUDIT.md`.

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

The current ZASSIMPLE DESIGN is already distilled at 4/4 and is **READY FOR CHALLENGE**, but architecture readiness remains 65% because the evidence blockers above are still open. Final architecture confirmation requires: CHALLENGE → explicit **YA, LOCK PRE-ARCH** → Execution Reality Check with real artifacts/samples where available → evidence-bounded execution and PRE-ARCH review → LAST DESIGN / ARCHITECTURE CHALLENGE → explicit owner final confirmation.

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


## Current project-local ZASSIMPLE operating alignment — 2026-10-09

This project operates primarily through **ZASSIMPLE v0.3.3**.

**System routing:** DUMP / DECIDE / DESIGN. DESIGN stays in project-local ZASSIMPLE by default. Retained Full ZASS lineage is consulted or escalated into only when materially stronger governance is required.

**Human-facing rule:** progressive disclosure; present only the next meaningful human action; never claim SAVE/sync without a real persistence receipt.

**Technical architecture gate for this project:**

~~~text
DESIGN
→ CHALLENGE DESIGN / ARCHITECTURE
→ CONTROLLED REVISION
→ owner: YA, LOCK PRE-ARCH
→ PRE-ARCH BASELINE — LOCKED FOR EXECUTION
→ EXECUTION REALITY CHECK
→ REAL ARTIFACT / SAMPLE PACK + EXECUTION-SURFACE MAP
→ DETAILED ZASSIMPLE ACTION PLAN ↔ PRE-ARCH
→ EVIDENCE-BOUNDED VERTICAL ATOMIC TASK
→ RESULT / PROOF
→ DELTA PLANNING + PRE-ARCH REVIEW
   ├─ NO ARCH IMPACT → PASS → NEXT UNRESOLVED TASK
   ├─ TASK-PLAN ISSUE → REWORK
   ├─ ARCH FINDING → revise/supersede PRE-ARCH
   └─ LOCKED-DECISION IMPACT → STOP → OWNER
→ sufficient implementation evidence
→ LAST DESIGN / ARCHITECTURE CHALLENGE
→ FINAL IMPROVE / REVISION
→ explicit owner final confirmation
→ rebuild RELEASE ACTION PLAN
→ fresh release atomic tasks
→ BUILD / TEST / INTEGRATE / HARDEN / VERIFY
→ RELEASE ACCEPTANCE
→ DELIVERED !!
~~~

`ZASSIMPLE/ACTION_PLAN.md` remains planning/execution authority only; it cannot silently change LOCKED decisions or architecture. `ZASSIMPLE/TASKS.md` is the canonical atomic execution queue. Retained Full ZASS records remain lineage/escalation reference rather than the default operating surface.

## Project-local command compatibility note

Current operation preserves the useful command semantics while routing them through project-local ZASSIMPLE:

- explicit `PROPOSED FOR PROCEED` approval sets remain bounded;
- Architecture Readiness and qualitative Evidence Confidence remain separate axes;
- `ZASS!! / PROCEED / COMMIT` remain the visible project controls;
- `PARKED` remains a state, not a command;
- invoking `ZASS` or `ZASS!!` means **this project's ZASSIMPLE**, not the upstream ZASS repository.

Historical method-alignment notes remain preserved in the project changelog as provenance.

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

# 21. CURRENT PROJECT-LOCAL ZASS STRUCTURE

Keep the repository deliberately small and use the actual current operating artifacts:

~~~
Kerani_Core_SuperBasic/
├── ZASSIMPLE/
│   ├── MIGRATION_CONTRACT.md   ← project-local method/surface contract
│   ├── DESIGN.md               ← current design surface
│   ├── ACTION_PLAN.md          ← canonical planning artifact
│   └── TASKS.md                ← canonical atomic execution queue
├── ZASS_Kerani_Core_SuperBasic.md
│                               ← retained LOCKED/evidence lineage + escalation reference
├── ACTION_PLAN.md              ← compatibility pointer only
├── docs/
│   └── DEV_WORKFLOW.md
└── README.md
~~~

Do not create code, abstractions or folders merely to make the project look mature.

Current authority/operation order:

1. Verified Git state — durable Source of Truth.
2. `ZASSIMPLE/DESIGN.md` — current project-local design surface.
3. `ZASSIMPLE/ACTION_PLAN.md` — canonical planning/execution plan.
4. `ZASSIMPLE/TASKS.md` — canonical atomic execution queue.
5. `ZASS_Kerani_Core_SuperBasic.md` — retained LOCKED decisions/evidence/history and escalation reference.
6. Chat / AI memory — context only; never authoritative without persistence.

---

# 22. PROJECT-LOCAL ZASS COMMANDS

In this project, **ZASS means the project-local ZASSIMPLE workflow**.

- **ZASS / ZASS!!** — review/update the relevant current ZASSIMPLE project surface; do not touch the upstream ZASS repository.
- **ACTION PLAN** — show/update `ZASSIMPLE/ACTION_PLAN.md`; it cannot LOCK a decision by itself.
- **CHALLENGE DESIGN !** — run the required technical design/architecture challenge when DESIGN is ready.
- **PROCEED** — approve exactly the explicit `PROPOSED FOR PROCEED` set currently shown; unlisted items are excluded. PROCEED does not commit or push.
- **LOCK PRE-ARCH** — surface the owner gate; only exact owner approval **YA, LOCK PRE-ARCH** creates the execution baseline.
- **COMMIT** — persist only the approved project-local change set atomically, verify the real Git SHA, then report factual SAVE/SYNC status.
- **DETAIL / HISTORY / REVIEW** — progressively disclose deeper lineage, evidence, trade-offs or historical records only when useful/requested.

**Hard boundary:** do not read, check, update, patch or commit the upstream ZASS repository merely because the user says `ZASS` or `ZASS!!`. Upstream access requires an explicit instruction naming that upstream repository or clearly asking to inspect/update the official ZASS method.

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

## VALUE GATE — MINIMUM DEFINITION OF DELIVERY / DONE

**Status:** OWNER-REQUIRED DELIVERY GATE  
**Date:** 2026-10-11  
**Purpose:** Kerani is not considered delivered merely because the architecture works or the code runs. The final project review must re-check these minimum user-value conditions against measured evidence.

### Minimum fail conditions

Kerani is **NOT DONE** if any of the following remains materially unresolved:

1. **Latency is high enough to feel troublesome to users.**
   - Must be checked using the LOCKED Day-1 latency telemetry, not only subjective impressions.
   - P50/P95/P99, queue wait, AI/tool time, retries and recovery behaviour must identify where delay comes from.

2. **Dynamic-language routing is inaccurate enough to damage trust.**
   - Real-user wording, shorthand, mixed language and ambiguous phrasing must be tested.
   - Misroute, clarification and AI-fallback rates must be measured.

3. **Tenant isolation can leak or cross-read another tenant's data.**
   - This is a hard product-failure condition.
   - READ and MUTATE paths must both prove trusted-context authorization/scope enforcement and fail-closed cross-tenant denial.

4. **All requests are forced through queueing when direct paths would be safer/faster.**
   - Queue/durable ingress scope must be justified by request class.
   - Simple READ paths must not inherit unnecessary queue/poll latency merely because mutation paths need durability.

5. **The chosen control plane creates unsustainable cost or maintenance burden.**
   - Final selection must be justified by measured latency, concurrency, reliability, operational effort, low-traffic cost, scale-up path and migration/rollback evidence.

### Additional current multi-user value hypotheses

These are **challenge/evidence inputs**, not yet locked architecture:

- **User-owned Google Drive OAuth:** test whether Kerani can securely connect to each user's own Google Drive as a useful storage/data-ownership option without introducing unacceptable onboarding, token, scope, revocation or support burden.
- **AI API failure fallback:** prove a fallback/recovery path that is robust and sufficiently responsive under provider failures. The challenge must not assume that “fallback” means a specific provider or mechanism; measure failover/retry latency, duplicate-risk, degraded-mode behaviour and truthful user feedback.

### Premium boundary

Premium/customer-owned Apps Script edge is **FUTURE WORK outside the current delivery definition**.

The current project should first prove Kerani for many users. After real multi-user operational experience exists, Premium architecture should be reconsidered from **ZERO → ARCHITECTURE in a separate new repository/project**, rather than treating the current customer-owned edge candidate as inherited final architecture.

Therefore:
- difficulty deploying/updating a customer-owned edge is **not** a current-project Value Gate;
- current work may preserve evidence about the idea, but must not let Premium edge concerns distort the present multi-user Core architecture.

---

# PROJECT ZASS CHANGELOG

## 2026-10-26 — D-066/L-052 Owner LOCK: Simple Freeform → User-Controlled Sheets Export

- Owner elevated unrestricted-*feeling* user entry, minimal logic, automatic Core→user-owned/authorised Google Sheet export and freedom to attach Sheet to external AI, edit, copy or delete independently as a **main Kerani product principle**. Stored as D-066/L-052, I-023, Q-062–Q-064, R-060–R-062 and dedicated doc `docs/KERANI_FREEFORM_TO_USER_GOOGLE_SHEETS_D066_LOCK.md`; tracked under KAI-13.
- Clarified that broad freeform intake preserves original content but does not bypass trusted tenant authorization/necessary transactional validation; Sheets is **not** the authoritative database. No silent Sheet→Core edits/deletions, no silent overwriting of edited Sheet content or recreating deleted file; exact live managed-vs-editable export conflict mode remains **OPEN**.
- Preserved D-018, D-055 and D-065/L-051 Free dashboard/read model/nonregression and D-060 Drive OAuth CANDIDATE. Not a new Google OAuth approval, external AI data transfer, sync SLA or proof of implementation. Docs/commit only, tests NOT RUN.

## 2026-10-24 — D-065/L-051 Owner LOCK: OpsMate Lessons as Kerani Release Gates

- Owner explicitly LOCKED **P0 RG-01 Upgrade Integrity** (mock/seed/config isolation, empty/no-regression, old→new migration, rollback), **P0 RG-02 Free Visible Value** (tenant-scoped mobile dashboard with committed records, basic summary and freshness) and **P0 RG-03 Knowledge-Ready Data** (source-grounded bounded tenant read models/query API for launched AI/summary, not many raw Sheet tab scans).
- Recorded experience as **owner-reported OpsMate weaknesses**, not proven root causes; required U01–U04/V01–V03/K01–K04 synthetic acceptance and source-traceable PASS/FAIL. Candidate pilot target P95 ≤5s commit→fresh dashboard is a **hypothesis**, not a locked SLA.
- Added I-022, Q-059–Q-061, R-057–R-059, D-065/L-051, dedicated `docs/KERANI_OPSMATE_RELEASE_GATES_D065_LOCK.md` and ZASSIMPLE projections. Linear KAI-11 tracking.
- Preserved D-057/L-047 Free Mini App, D-059 Premium advanced dashboard **CANDIDATE**, D-064/L-050 queue-ready strategy and D-055 Free no-AI. **No code, customer data, environment, feature deployment, PRE-ARCH or tests PASS**.

## 2026-10-24 — D-064/L-050 Owner LOCK: Queue-ready WhatsApp V1→V2 conditional pilot strategy

- Owner LOCKED a **limited decision**, not production: V1 Worker→protected Apps Script for a small pilot with a stable Job Envelope, dispatch/processJob interface, inbound/authoritative idempotency, truthful ACK/SAVE status and one outbound quota gate; V2 adds Cloudflare Queue/consumer while preserving the same Core data and WhatsApp webhook.
- **Safety exception mandatory:** if V1 timeout/ACK-durability/replay evidence is unacceptable, **stop pre-live V1 and promote/test V2 before real users**. No claim of no-code changes; migration needs synthetic canary/drain/rollback evidence, but is designed to avoid customer-data reset.
- Added I-021, Q-056–Q-058, R-054–R-056, D-064/L-050 and dedicated `docs/KERANI_WA_QUEUE_READY_V1_V2_D064_LOCK.md`; projected into ZASSIMPLE, tracked by existing Linear KAI-8.
- This **L-050 is a WhatsApp pilot architecture-sequencing LOCK, not a brand LOCK**. D-062 RekodUntung.ai stays PRIMARY CANDIDATE. D-063's 950/990 thresholds, D1/DO/Queue choice and Meta billing details remain candidate; no global E-016 PRE-ARCH, implementation, real Cloudflare/WhatsApp change, tests or deployment.

## 2026-10-24 — D-063 WhatsApp Edge Quota Guard & Fast Scheduler saved as CANDIDATE

- Owner asked to save ideas/data and commit, **not** to LOCK a runtime architecture or start implementation. Added I-020, Q-052–Q-055, R-050–R-053, and D-063 CANDIDATE plus detailed note `docs/KERANI_WA_EDGE_QUOTA_GUARD_ZASS_CANDIDATE.md`, tracked under existing Linear KAI-8.
- Meta official: effective 2026-10-01 first 1,000 **outbound service messages**/business phone number/month free; warning 950 (95%), proposed normal stop 990 (99%) with 10-unit reserve is a **candidate policy**, not a Meta hard stop, with explicit delivery/ledger/BSP reconciliation warning.
- Cloudflare Worker+Apps Script adapter, D1/DO atomic quota, Queues/DO Alarms for justified sub-minute work remain **options**. Direct `doPost()` Apps Script already avoids 1-minute clock-trigger polling; Cloudflare Cron likewise is minute-based. Evidence requires E-016 delta-only synthetic T01–T08, no “5-second guarantee”.
- No Worker/Queue/DO/D1 Apps Script implementation, real test, runtime account, production webhook, pricing, secrets, WhatsApp messages or PRE-ARCH selection; existing LOCKED Free channel/Core principles preserved.

## 2026-10-23 — RekodUntung.ai promoted to PRIMARY NAME CANDIDATE (D-062, NOT LOCKED)

- Owner chose exact spelling `RekodUntung.ai` as the *lead name to check*, not as an approved product/repository rename. Logged **I-019, D-062 CANDIDATE, Q-049–Q-051, R-048–R-049** and `docs/KERANI_BRAND_REKODUNTUNG_PRIMARY_CANDIDATE.md`; Linear tracking KAI-10.
- **Hard boundary:** MyIPO official trademark/similarity clearance and live domain registrar confirmation are PENDING, so **NO brand LOCK, NO L-050**. Existing technical repository identity, code, bot/domain and product marketing remain unchanged.
- Rationale: “Rekod” describes the actual Free tasks; “Untung” communicates desired benefit, but is not proof of validated profit accounting or guaranteed profit.
- This is a documentation-only GitHub commit; no registry checks, domain purchase, trademark filing, public rename, migration, app tests or production change executed.

## 2026-10-23 — D-061/L-049 Free chat first + user-created group UX owner LOCK

- Owner LOCKED a small Kerani Free personal bot; business/user ID onboarding and verified membership, warning-only when one business has multiple active Free users. No cross-worker semantic duplicate scanning/merging or Free admin-role/group workflow.
- User-created Telegram group is the optional coordination idea. Preferred ordinary `@KeraniBot` command remains **UNTESTED**, fallback `/command@KeraniBot → ForceReply → reply` awaits synthetic T01–T06; no forced privacy-OFF or bot group admin setting.
- Telegram Mini App D-057/L-047 remains first-class deterministic Free capability, but is **not a mandatory form or blocker** for first Free chat launch. No architecture PRE-ARCH, bot runtime, API credential, code, deployment or functional PASS claimed.
- D-061/L-049 plus I-018, Q-045–Q-048, R-044–R-047 and dedicated `docs/KERANI_FREE_CHAT_GROUP_UX_D061.md` tracked in Linear KAI-9.

## 2026-10-22 — ZASS D-060 modular channel/cloud/AI-resilience review saved as CANDIDATE

- Captured owner propositions for trial-only WhatsApp welcome credit then metered WA transport, economical Telegram, optional customer-owned Drive, paid extra Kerani Cloud, controlled Free/Paid AI data terms and safe multi-tenant database/API concurrency.
- Registered **I-017, Q-040–Q-044, R-039–R-043, D-060 CANDIDATE** and detailed `docs/KERANI_CHANNEL_CLOUD_AI_RESILIENCE_ZASS_CANDIDATE.md`; tracking KAI-8.
- Preserved LOCKED Free usefulness and old WhatsApp quota terms; no silent commercial supersession, provider choice, PRE-ARCH/implementation, actual pricing, test PASS or product maturity increase.
- Explicitly excluded Claude/industry news and competitor/brand-name discussion, which must be handled separately.

## 2026-10-19 — Premium Business Workspace recorded as PRODUCT/UX CANDIDATE (NOT LOCKED)

- Owner authorised capture of a **tenant-specific Premium Business Workspace** with truthful Telegram AI text summary → scoped interactive dashboard link/button, graphs/tables/search/forecast, optional Android PWA icon, user-authorised Google Drive links and possible later task sync.
- Recorded **D-059 CANDIDATE — NOT LOCKED** with independent evidence note `docs/KERANI_PREMIUM_BUSINESS_WORKSPACE_CANDIDATE.md` and Linear tracker KAI-7. Kept D-057/L-047 Free deterministic Mini App LOCK unchanged; D-050/D-051 Premium capability packs and Drive OAuth still CANDIDATE.
- No implementation task, customer data access, external sync, framework/hosting/architecture selection, PRE-ARCH, entitlement price or product VALID claim. OpsMate / clean Agro Demo priority unchanged.

## 2026-10-19 — V-Road 8V owner LOCK; VALID first, VERBAL Word-of-Mouth, VOUCH gate

- **LOCKED D-058/L-048**, promoting the approved 8V sequence: **VALID → VALUE → VERBAL (Word-of-Mouth) → VOLUME → VENTURE → VIRAL → VARY → VERSATILE**.
- VALID = experiment and iterate on actual use cases until the solution is proven useful, effective, usable and worth continuing; VALUE follows when pilot/real users experience benefit. VERBAL means their genuine word-of-mouth, while existing Verbal UX remains a separate design discipline.
- Added **VOUCH** to Extended V-Gates as verified authentic user endorsement/referral, **not** a ninth V and not an invented testimonial.
- Set D-048/L-041 historical 7V to **SUPERSEDED**, retained its full original model for audit; D-047/L-040 4V remains historical. Updated active ZASSIMPLE projections, no change to OpsMate evidence, PRE-ARCH, architecture, tests or production.
- Linear post-commit reconciliation required under `docs/LINEAR_DEVELOPMENT_TRACKING_CONTRACT.md`; no issue or project IDs may be fabricated.

## 2026-10-16 — Telegram Mini App deterministic dual-surface direction LOCK

- Owner instructed **LOCK COMMIT** for Telegram Mini App as a *first-class* deterministic Free UI complementary to conversational Telegram chat; added **D-057/L-047** (owner-LOCKED PRODUCT/UI principle, **not** PRE-ARCH).
- The Mini App is independently available and supports actionable **hybrid active fallback** during model outage, while always using the same tenant identity, Core/business API contracts, server-side auth/validation, idempotency and audit.
- Added Q-039/R-038 for entry-point/UI/hosting/security challenge: server-side Telegram WebApp initData validation is mandatory, and frontend-supplied user/tenant fields have no authority.
- The exact v0.1 screen set, `/setmenubutton` vs `/newapp`, Cloudflare Pages Free and single Agro Demo form are **CANDIDATE**. Shared Mini-App shell across CrossAI/Kerani/Temaya is **DEFERRED**. OpsMate handover and independent clean Agro Demo remain the first priority; UI cannot delay it.
- No production code, deployment, provider selection, PRE-ARCH/Challenge result, progress increase or new execution task is claimed.

## 2026-10-14 — Evoxt Malaysia VPS saved as paid server last-choice contingency

- At owner request, added Evoxt to `docs/EVOXT_PAID_VPS_CONTINGENCY.md` as **CANDIDATE — BACKUP / LAST CHOICE**, not a default runtime, provider selection or architecture LOCK.
- Kept marketing figures and one user's RAM/transfer remarks clearly separated from independent test evidence; no VPS speed, stability or cost advantage claimed as proven.
- Added conditional activation criteria under E-016; **four active control-plane candidates remain unchanged**, with Evoxt outside immediate benchmarking, implementation and the Kerani Agro Basic Demo prerequisite.
- No account signup, purchase, production changes, PRE-ARCH lock, new implementation task or architecture-readiness increase.

## 2026-10-12 — AI-first Verbal UX and hybrid active fallback trial; E-016 delta-only

- Owner clarified Kerani AI DNA: **AI-first for ordinary language**, deterministic first for explicit commands/forms, **hybrid active fallback** for unavailable/slow/free-quota-constrained AI, and always-active deterministic business authority.
- Recorded D-056 **CANDIDATE / owner-selected trial**, Q-038 and R-037. D-029/L-023 historical LOCK is preserved verbatim; its 'AI adds no value' condition covers explicit input, but routing priority itself is not architecture-locked.
- Tightened E-016 to **reuse existing OpsMate evidence and test only unproven deltas**. No repeated four-mode full Purchase flow. Cloudflare vs Google Free comparison remains in the dedicated Talorys evidence note, now including model-budget optimisation, safe Telegram incremental acknowledgement and bot forms/wizards.
- No implementation, Challenge PASS, PRE-ARCH lock, provider winner or reliability proof is claimed. D-055/L-046 Free independence remains LOCKED.

## 2026-10-12 — Talorys reference evidence, Free Core independence LOCK and AI fallback research

- Saved Talorys as public **reference evidence** for AC-010 and AC-012, NOT architecture proof or a new V1 candidate; Talorys uses Durable Objects SQLite, not AC-010 D1.
- Added `docs/TALORYS_CLOUDFLARE_GOOGLE_FALLBACK_EVIDENCE.md` with dated Cloudflare/Google free-quota comparison, privacy/cost warnings, falsifiable fallback experiments and measurement denominators.
- **LOCKED D-055/L-046** at owner instruction: Free Core remains independently useful; AI adds convenience but cannot be a prerequisite.
- Expanded E-016 challenge inputs to compare AI failure/provider failover vs no-AI primary/degraded flow without selecting vendors or architecture.
- **80–90% is an experimental hypothesis about routine action-type no-AI capability coverage, not proven message-level AI bypass.**
- AC-010 and AC-012 remain CANDIDATE, E-016 remains PLANNED, DESIGN/Challenge state and PRE-ARCH remain unchanged; no implementation executed.

## 2026-10-11 — Convenience-first UX principles locked

- Owner approved and requested persistence of two product principles:
  - **User buys convenience and usefulness first; ownership is secondary unless it solves a real pain.**
  - **Premium must emerge from observed demand, not architectural imagination.**
- Added D-054 / L-045.
- Locked current multi-user UX priorities: low-friction onboarding, fast time-to-value, easy top-up, continuity without forced migration, strong latency/accuracy/trust, and support for the channels users actually want.
- Explicitly allowed hosted Kerani + top-up as a valid long-term user path if user behaviour supports it.
- Premium remains future work shaped by observed demand after real multi-user usage.
- Challenge Design was not run and PRE-ARCH remains NOT LOCKED.


## 2026-10-11 — Minimum User Value Gate locked; Premium edge deferred

- Owner defined and required a final **Value Gate / Definition of Delivery** for the current Kerani multi-user project.
- Added D-053 / L-044 and E-021.
- Minimum delivery gate now requires measured acceptable latency, trustworthy dynamic-language routing, proven tenant isolation, evidence-based direct READ vs durable queue boundary, and sustainable control-plane cost/maintenance.
- Added current challenge hypotheses for **user-owned Google Drive OAuth** and **robust/responsive AI API failure fallback**.
- Premium/customer-owned Apps Script edge is explicitly deferred from the current delivery definition; after real multi-user operating experience, Premium architecture must restart from ZERO → ARCHITECTURE in a separate repository/project.
- Existing GAS edge audit remains historical evidence only and must not bias the current multi-user control-plane winner.
- Challenge Design was not run and PRE-ARCH remains NOT LOCKED.


## 2026-10-11 — Public GAS agentic audit saved as Challenge evidence

- Owner approved saving the deep audit of `adk-gas`, `GeminiWithFiles` and `GeminiApp` as evidence input only.
- Added `docs/GAS_AGENTIC_PATTERN_AUDIT.md` and E-020.
- Recorded extractable patterns: bounded function/tool calling, fixed tool registry, fast-path bypass, policy hooks, HITL suspend/resume, timeout/concurrency/token/payload safeguards, and structured logging.
- Recorded V1 patterns to park/avoid without evidence: unrestricted dynamic JS, full DAG planner, broad autonomous replanning, MCP/A2A everywhere, and default subagent hierarchy.
- Added explicit distinction between **Central Control Plane** and **Customer-Owned Apps Script Edge**.
- Kept E-016 as a four-way central control-plane benchmark; customer-owned Apps Script edge is not a fifth central candidate.
- No runtime selected, Challenge Design was not run, AC-012 remains CANDIDATE, and PRE-ARCH remains NOT LOCKED.


## 2026-10-11 — Durable Ingress and Authorization Guard challenge inputs saved

- Owner approved recording two additional inputs for the upcoming Architecture Assumption + Boundary Challenge.
- Added **Durable Ingress / Idempotency Boundary** without locking a universal queue requirement; Q-016 remains open.
- Added **Authorization / Scope Guard** as a separate boundary from tenant identity, with trusted-context and tool/data-boundary enforcement.
- Added Q-036/Q-037 and R-035/R-036 to preserve lineage.
- Explicitly rejected the assumption that every request must traverse a queue before evidence; direct READ paths remain challenge candidates.
- Challenge Design was not run, AC-012 remains CANDIDATE, PRE-ARCH remains NOT LOCKED, and no implementation task was created.


## 2026-10-11 — OpsMate vs Kerani Agentic Tool comparison documented

- Added `docs/OPSMATE_VS_KERANI_AGENTIC_TOOL.md` as the supporting architecture comparison note requested by the owner.
- Recorded side-by-side action/mutation and read/retrieval flows, the proposed Kerani Agentic Tool flow, 1:1 differences, KEEP lessons from OpsMate, REFACTOR-INTO-TOOL candidates, and mutation authority boundaries.
- Documented the core distinction: **OpsMate = workflow-centric operational system; Kerani AI = governed capability/tool system with a natural-language front end.**
- Added a pointer from `ZASSIMPLE/DESIGN.md` under AC-012.
- No design challenge was run, AC-012 remains CANDIDATE, PRE-ARCH remains NOT LOCKED, and no new implementation task was created.


## 2026-10-11 — Latency Observability from Day 1 LOCKED

- Owner explicitly issued **PROCEED LOCK SAVE** for Day-1 latency observability.
- Added D-052 / L-043 as a LOCKED Kerani execution/viability requirement.
- Every executable request path must expose stage-level timing evidence from ingress through reply, including retry/queue/AI/tool/storage timing where applicable.
- Required aggregate view includes at least P50/P95/P99 total latency plus error/retry rate and meaningful tool/channel/runtime/provider segmentation.
- Canonical principle: **Measure before optimize. Every request must expose enough timing evidence to locate latency by stage.**
- This lock does not select a runtime, control plane or AI provider.
- Challenge Design was not run and PRE-ARCH remains NOT LOCKED.


## 2026-10-11 — Agentic Tool Boundary saved as challenge dimension

- Owner approved saving Agentic Tool Boundary as a mandatory dimension for the next Architecture Assumption + Boundary Challenge.
- Added AC-012 **CANDIDATE — Bounded Agent Tool Orchestration**, Q-035 and R-034.
- Explicitly separated GENERIC behaviour from AGENT_TOOL permission and classified candidate authority as READ / PROPOSE / CLARIFY / VALIDATE / MUTATE / SYSTEM.
- Recorded `retrieve_history` as a strong READ candidate for natural-language history/status retrieval and `prepare_candidate` as a strong PROPOSE candidate for natural operational reporting.
- Preserved D-015: AI-interpreted mutation still requires the governed human/deterministic/domain authority path before authoritative persistence.
- Challenge Design was **not run**, PRE-ARCH was not locked, and no implementation task was created.


## 2026-10-11 — OCI Ampere A1 Always Free added to E-016 benchmark

- Owner approved adding OCI Ampere A1 Always Free as the fourth V1 control-plane candidate.
- Added AC-011 as **CANDIDATE**, not LOCKED.
- Current Oracle documentation checked 2026-10-11 records Always Free A1 allowance as 1,500 OCPU-hours + 9,000 GB-hours/month, equivalent to about 2 OCPUs + 12 GB memory for an Always Free tenancy within the allowance.
- Recorded Oracle-documented risks: idle compute may be reclaimed and Always Free shapes can encounter out-of-host-capacity conditions.
- Expanded E-016 from a three-way to a four-way benchmark: central Apps Script vs Cloudflare Workers+D1 vs Cloud Run stack vs OCI A1 Always Free VM.
- No provider was selected. ZERO → ARCHITECTURE and Evidence Confidence were unchanged.


## 2026-10-11 — Response-time and language-variability field signals saved

- Recorded owner field observation that transient Gemini/provider failures can make OpsMate feel stuck because retry/poll scheduling adds a large user-visible delay.
- Preserved the owner's recalled ~30-second interval as **REPORTED**, not VERIFIED.
- Cross-checked accessible OpsMate TelegramWorkerTest.js snapshots (10e20cd..., a6b504...): the audited worker stores API_OR_OUTPUT_ERROR as RETRY_NEEDED with a **60-second base exponential retry**, so the exact experienced 30-second cadence remains unresolved.
- Added Q-033/R-032 so E-016 must decompose latency instead of blaming Apps Script or Gemini generically.
- Added Q-034/R-033 for deterministic-first language variability: real multi-user phrasing must be tested for coverage, misroutes, clarification and AI-fallback rate.
- No provider was selected, no architecture candidate was LOCKED, and ZERO → ARCHITECTURE / Evidence Confidence were unchanged.


## 2026-10-09 — Project-local ZASSIMPLE current-facing cleanup

- Corrected only stale current-facing project references after the ZASSIMPLE migration.
- `ZASS` / `ZASS!!` now explicitly mean the project-local ZASSIMPLE workflow for Kerani Core SuperBasic.
- Removed the current-facing instruction to check the upstream ZASS repository on ordinary project ZASS invocation.
- Updated current project structure, challenge/PRE-ARCH execution flow and footer to ZASSIMPLE v0.3.3.
- Historical snapshots and dated changelog records were intentionally preserved unchanged.
- No D/L/Q/R/E/AC decision, readiness score, evidence-confidence state or architecture candidate was changed.
- Upstream ZASS repository was not accessed or modified by this cleanup.


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
🔬 EVIDENCE CONFIDENCE: LOW — DESIGN is distilled at 4/4, but Challenge has not run, PRE-ARCH is not LOCKED, and the major execution/runtime evidence gaps remain open.

✅ ZASS UP TO DATE — ZASSIMPLE v0.3.3
