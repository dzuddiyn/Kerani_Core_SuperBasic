# Talorys reference evidence — AC-010 / AC-012; Free-cloud comparison and AI fallback

**Date checked:** 2026-10-12  
**Classification:** PUBLIC REFERENCE EVIDENCE + ENGINEERING INFERENCE; NOT KERANI RUNTIME TEST  
**Authority:** Supports AC-010 (CANDIDATE), AC-012 (CANDIDATE), E-016, Q-033/Q-034/Q-035 and D-053. Does not select a provider, promote architecture, change PRE-ARCH, or justify new execution tasks.  
**Owner direction:** Talorys is *reference evidence*, not the target application or a direct architecture decision.

**Owner update 2026-10-12 — CHALLENGE DIRECTION, NOT PRE-ARCH:** Preserve an **AI-first natural-language experience**. For explicitly structured/selected commands, take a deterministic fast path; for ordinary free-text, try bounded AI language-to-tool interpretation first. If AI/latency/free-quota optimisations (including safe early acknowledgement/progressive Telegram updates) cannot meet usefulness goals, evaluate a measured swap/hybrid. **Deterministic remains always authoritative for execution, and becomes an active interaction fallback when AI is down.** This routing preference is a testable product hypothesis, not a measured implementation success. Existing locked D-029 ('deterministic where AI adds no value') still applies to clear/explicit cases; changes to its stronger reading must pass explicit owner change control.

## A. What Talorys actually proves (and does not)

Sources:
- [Talorys repository / README](https://github.com/rociiu/talorys)
- [Hackaday, "A Free Cloud AI", 2026-10-12](https://hackaday.com/2026/10/12/a-free-cloud-ai/)

**SOURCE-DOCUMENTED:** Talorys is an open-source, **single-user** assistant deployed inside the user's own Cloudflare account. Its published stack is **Cloudflare Pages + private Worker + Agents SDK / SQLite-backed Durable Object + Workers AI**, with Durable Object alarms for reminders. Tasks, notes and reminders continue **without AI** when AI is down or its free allocation is exhausted. It advertises bounded output/context/tool-step budgets and local deterministic mock mode. Its app is not a general multi-tenant micro-SME control plane.

**CRITICAL DIFFERENCE:** Talorys **does not provision D1, R2, KV, Queues, or Workflows** according to its README. Therefore Talorys is **NOT** a direct proof that Kerani's AC-010 **Workers + D1** candidate satisfies tenant isolation, quotas, webhook throughput, message channels, billing, durable ingress or scheduled workloads.

**HACKADAY FIELD REPORT (NOT FORMAL BENCHMARK):** one calendar/reminder test was assigned the wrong day; another ran into a Cloudflare rate limit. This illustrates quota and language/time interpretation risks. Hackaday did not audit all code.

**TRANSFERABLE PATTERN (INFERRED; TO CHALLENGE):**
- useful deterministic tasks/read/write UI remain available without model inference;
- model acts as bounded natural-language-to-tool coordinator, not as business truth;
- private execution + explicit tool registry + safe tool guards;
- cap model calls/steps, publish truthful AI-unavailable status, retain manual path;
- track per-request quota/latency and distinguish model-side success from persisted tool success.

**NOT TRANSFERABLE WITHOUT TESTS:** single-user password/auth, one Durable Object / local SQLite authority, Talorys data schema, uncontrolled agent mutation permissions, agent framework footprint, accuracy of free-text recognition, and Cloudflare production multi-tenant capacity.

## B. Cloudflare Free vs Google Free — AC-010 / E-016 optimisation evidence

**Provider terms are dated evidence, not architectural constants. Verify again at implementation.** Different resources have different limits and reset clocks. Free means bounded, not unlimited.

| Need | Cloudflare candidate | Google free candidate | E-016 implication |
|---|---|---|---|
| Webhook/API/router | Workers Free: **100,000 requests/day; 10 ms CPU/request**; CPU-heavy parse must be measured | Apps Script: **6 min/execution**, daily service quotas, concurrency limits; easy Google integration | Test real response P50/P95/P99, CPU and cold/retry behaviour; request limits do not equal completed business actions |
| Tenant/quota relational state | D1: **5M rows read/day; 100k rows written/day; 5 GB storage** Free; hard failures when daily caps reached | Sheets/Drive + Apps Script can prototype; row permissions, concurrency and write contention need explicit tests | Prefer portable storage repository contract; test isolation, transactions, backup/export, quota-exhaustion |
| Stateful coordination | SQLite-backed Durable Objects work on Free; single-user Talorys pattern is NOT tenant design proof | Apps Script LockService/Properties + Triggers for modest workloads | Compare only if coordination/state is required; avoid D1 + Durable Object double-write without evidence |
| Durable async | Queues currently include **10k operations/day** Free, but writes+reads+deletes count separately | Apps Script time-driven triggers + jobs possible within quotas | Queue only request classes needing durability; preserve direct READ path |
| Schedule | Workers Free: **5 Cron Triggers/account**; DO alarms possible | Apps Script installable time-driven triggers with daily runtime limit | Benchmark operational schedule needs; do not add Cron/DO/Queues by default |
| AI execution | Workers AI: **10k Neurons/day free allocation**; model-specific consumption/rate limit | Gemini Developer API model-specific free allowances/limits; **free-tier content may be used to improve products** under published pricing terms | Provider-neutral AI adapter; default minimal payload, privacy review, budgets and structured output validation |
| AI routing/fallback | Cloudflare AI Gateway offers provider fallbacks/dynamic routing but upstream provider keys, billing and logging controls still apply | Application-side model/provider adapter plus Gemini fallback policies | Fallback routing is not free model capacity; no hidden paid API / retries |
| Receipt OCR/media | R2 is an option, NOT part of Talorys; storage/media quota must be separately assessed | Drive/Sheets receipts or user-assisted Lens → pasted text | Manual receipt entry remains usable; hosted OCR is separately metered |
| Low-maintenance path | No VPS OS; vendor quotas and portability remain risks | Familiar Workspace APIs; quota + deployment and concurrent shared-service constraints | Benchmark against Cloud Run and OCI too; do not presuppose Cloudflare win |

Official Cloudflare sources:
- [Workers limits (2026-10-08)](https://developers.cloudflare.com/workers/platform/limits/)
- [D1 pricing and Free quotas](https://developers.cloudflare.com/d1/platform/pricing/)
- [D1 Free exhaustion behaviour (2026-09-01)](https://developers.cloudflare.com/changelog/product/d1/)
- [Queues Free operations](https://developers.cloudflare.com/queues/platform/pricing/)
- [Durable Objects Free limits](https://developers.cloudflare.com/durable-objects/platform/limits/)
- [Workers AI free allocation (2026-10-01)](https://developers.cloudflare.com/workers-ai/platform/pricing/)
- [AI Gateway fallbacks](https://developers.cloudflare.com/ai-gateway/configuration/fallbacks/)
- [AI Gateway dynamic routing](https://developers.cloudflare.com/ai-gateway/features/dynamic-routing/)
- [AI Gateway logs/retention (2026-09-24)](https://developers.cloudflare.com/ai-gateway/observability/logging/)

Official Google sources:
- [Apps Script quotas](https://developers.google.com/apps-script/guides/services/quotas)
- [Gemini Developer API pricing/privacy by tier](https://ai.google.dev/gemini-api/docs/pricing)

**AI privacy caveat:** do not route raw private tenant data to a free AI endpoint merely because it has remaining quota. Obtain a defensible data-processing policy, redact/minimise payloads, define consent/retention, and check whether gateway logs hold prompts/responses (Cloudflare AI Gateway logging is enabled by default unless changed). Budget and prompt privacy must both pass.

## C. AI-first UX, deterministic authority and hybrid active fallback — owner trial

Candidate request strategy for AC-012 challenge, **NOT ARCH LOCK**:

1. **Always-active deterministic business authority:** trusted tenant auth/scope; schema/entitlements, validation, confirmation, write/read controls, audit and idempotency. This is not just fallback — it is the mandatory trusted execution engine behind AI and direct input.
2. **Explicitly selected/structured intent → deterministic primary:** buttons, Telegram form fields, menu operations and unambiguously typed structured commands execute without inferencing, subject to normal rules. No heavy keyword grammar masquerading as natural-language AI.
3. **Ordinary free text → bounded AI-first:** one small/fast model and compact prompt+tool schemas attempt intent detection and READ or PROPOSE tool arguments. Preview, clarification and human/domain gates still govern mutations.
4. **AI optimisation before changing routing:** measure model and network latency separately; short context/schema, cap tool calls/tokens, choose responsive eligible free model, use fast Telegram acknowledgement and optional safe incremental status updates. 'Chunking' improves perceived waiting when real progress is shown; splitting messages alone does not reduce inference time. No partial unvalidated record should be represented as saved.
5. **Condition-triggered active AI failover:** on timeout, 429, 5xx or quota (with privacy/cost/rate ceilings), attempt bounded alternate AI only if time budget permits. Do not re-run already executed mutations.
6. **Condition-triggered active deterministic UX fallback:** auto-propose Telegram inline-keyboard/ForceReply wizard, Mini App web form (optional), or manual entry when AI fails or is slow/unaffordable. User can always open this route directly (passively available); do not abandon the request without actionable continuation.
7. **Review the actual evidence:** if free AI latency cannot be made tolerable even with optimisation, compare conditional bypass, pre-routing, model swap or hybrid based on P50/P95/P99 and task completion, not a predetermined deterministic-first reversal.

**Terminology:** primary routing is AI-first for ordinary free text, deterministic-first for explicit input; *active fallback* is automatically triggered; *passive fallback* is the always-accessible manual path; *hybrid* combines them. Never confuse the fallback UX with the deterministic execution authority.

**Fail-closed invariant:** retries/provider switch may repeat interpretation, NEVER duplicate an authoritative business effect. A unique request/idempotency key, trusted tenant context, explicit confirmation and deterministic/domain validation govern commit operations. Provider fallback must not assume the model's reported tool success is an actual persisted success.

## D. 80–90% no-AI hypothesis: separate denominators

**HYPOTHESIS ONLY, not measured evidence.** Target `80–90%` only for **catalogued routine action TYPES having a usable no-AI completion path**. Do **not** assume 80–90% of real incoming free-text MESSAGES will skip AI, or claim 80–90% token savings without workload measurement.

Track:
- `no_ai_capability_coverage = routine_action_types_with_usable_no_ai_path / all_catalogued_routine_action_types`
- `actual_ai_bypass_rate = requests_completed_without_ai / all_completed_requests`
- `misroute_rate = wrongly_routed_intents / labelled_requests`
- `clarification_rate = requests_requiring_clarification / eligible_requests`
- `ai_fallback_rate = requests_invoking_model_after_deterministic_attempt / eligible_requests`
- `safe_degraded_completion_rate = core_requests_successfully_completed_with_ai_unavailable / eligible_core_requests`
- segmented P50/P95/P99 end-to-end response time, retry waiting, API spend per useful action, false-success, duplicate authoritative writes, tenant-isolation failures.

**Accept/reject criteria for challenge:** no incorrect cross-tenant access; zero duplicate writes on retry; no unconfirmed AI-derived mutation; no false-success; clear manual completion for each mandatory Free Core family; responsiveness and AI bypass measured from real Malay/English shorthand/misspelling samples. Numeric performance thresholds to be calibrated from the real pilot, not invented here.

## E. E-016 / AC-012 DELTA-ONLY evidence plan (NOT RUN)

**Owner stop rule (2026-10-12): DO NOT replay the same end-to-end Purchase implementation across deterministic-only, Gemini, Workers AI and forced-failure models just to prove the known OpsMate Purchase-like business flow again.** OpsMate is the reference implementation. First inventory actual source/test/proof receipts and mark which behaviours are already VERIFIED vs merely ASSUMED; do not claim all AI providers or Cloudflare are proven by OpsMate.

- **A — Evidence reuse:** map existing OpsMate candidate → confirmation → validation → persistence, known provider failure/retry and Telegram behaviour to E-016 with exact code/test/commit anchors; preserve known failure modes and do not copy farm assumptions into Kerani.
- **B — Infrastructure delta:** compare *only missing* Cloudflare Workers+D1 multi-tenant webhook/quota/permissions/CPU/scheduled/budget/restore properties vs existing Google baseline, and retain Cloud Run/OCI as existing candidate comparators. Use tiny synthetic fixtures; do not reconstruct Purchase domain logic.
- **C — New agent model/tool delta:** verify only new model/provider response and tool-schema compatibility plus tenant/read/propose authority and fail-closed mutation where not previously proven. Existing regression/proof receipts may be reused where valid.
- **D — AI-first UX delta:** evaluate real language variability and operational responsiveness with a bounded tool response, early Telegram acknowledgement, 429/5xx/time-budget fallback to an actionable no-AI form. Full multi-model Purchase A/B is *not* a prerequisite; test only gaps with evidence.
- **E — Platform comparison:** retain existing **four** E-016 central candidates; Talorys is reference evidence, not a fifth architecture and does not imply D1/Queues verification.

**Telegram interfaces to evaluate:** inline keyboards, ForceReply multi-step wizard and optional Mini App Web App with form validation. Inline keyboard alone is not a native arbitrary-field form; a Mini App is a separate HTTPS-based web UI. Assess user onboarding friction rather than choosing the most elaborate UI.

## F. Cloudflare Free vs Google Free — what to optimise (NOT RUNTIME SELECTION)

1. **Cloudflare hypothesis:** Workers for API/Telegram webhook, D1 for tenant/record/quota only if AC-010 proof passes, Workers AI for small bounded intent/tool selection under free Neuron budget, and optional AI Gateway for alternate provider. A Gateway does not magically make the other provider free; tenant payload/logging/retention and billing settings must be vetted.
2. **Google baseline:** use working Apps Script/Sheets/Gemini OpsMate artefacts as evidence. Google integration may remain useful independently; avoid new Google Cloud setup obligations simply because Google has familiar products. Free Gemini policies/model quotas differ by SKU and change over time.
3. **Free optimisation:** choose the *fewest* paid-billing prerequisites, external calls, queue hops, duplicate data stores and AI turns that preserve user experience. Protect useful-action capacity with independent transport/storage/AI/report quotas, fail-closed tenant scope, indexed queries and budget alarms.
4. **Do not confuse limits:** Cloudflare Workers Free 100,000 requests/day + 10ms CPU/request; D1 5M rows read/day + 100k rows written/day + 5GB total; Queues 10k operations/day (typically three operations per delivered message, if used); Workers AI 10k Neurons/day. Google Apps Script typically 6min/execution with service-specific quotas. Limits are dated vendor terms, not guaranteed project throughput.
5. **Priority:** user-experienced AI-first responsiveness, safe and usable degraded interaction, and predictable truly-free pilot economics. Cloudflare-first is a **trial preference** and VPS alternative worth testing; no winner declared.

Updated sources checked 2026-10-12: https://developers.cloudflare.com/workers/platform/limits/ ; https://developers.cloudflare.com/d1/platform/pricing/ ; https://developers.cloudflare.com/queues/platform/pricing/ ; https://developers.cloudflare.com/workers-ai/platform/pricing/ ; https://developers.google.com/apps-script/guides/services/quotas ; https://ai.google.dev/gemini-api/docs/pricing ; https://core.telegram.org/bots/api .

## G. Status / owner lock boundary

- **OWNER-LOCKED principle (D-055/L-046):** Free Core must remain independently useful without AI. AI adds convenience/interpretation and is never a condition of basic function.
- **SAVED REFERENCE:** Talorys / Cloudflare / Google sources and engineering hypotheses above.
- **CANDIDATE / OWNER-SELECTED TRIAL:** AC-010, AC-012; AI-first free-text + explicit deterministic fast-path + hybrid active fallback; **E-016 DELTA-ONLY PLANNED**, not executed. D-029/L-023 remains LOCKED with 'where AI adds no value' preserved; do not silently supersede.
- **NOT LOCKED:** vendor selection, deterministic coverage %, automatic failover sequence/provider, queue/storage/agent service mix, PRE-ARCH.


---

## G. 2026-10-12 OWNER CORRECTION — Hybrid **AI-first UX**, deterministic **active fallback** (trial, NOT PRE-ARCH LOCK)

**Why this section exists:** The earlier Section C outlined a deterministic-first approach to *request interpretation*. The project owner explicitly prefers testing **AI-first language UX**, to avoid merely replicating OpsMate's feeling of rigid/slow workflow processing. The earlier advice is superseded at the *UX-routing hypothesis* level, but D-029's LOCKED provision that AI adds no value on explicit/clear operations and D-055's independently usable Free Core both remain intact. Do **not** construe the deterministic business guard as a fallback: it remains mandatory, even for the AI-first path.

**OWNER-DIRECTED TRIAL POLICY (CANDIDATE architecture / selected trial posture):**
- **Natural or context-dependent free text → AI-first** bounded intent classification / tool selection / candidate extraction, with small efficient model or tool router.
- **Unambiguous explicit command, button, structured form or proven exact pattern → deterministic-first** fast path: do not call AI solely for brand identity or unnecessary interpretation.
- **On AI timeout/5xx/429/quota/invalid structured output → hybrid *active* fallback:** optionally one bounded alternate provider/model attempt if privacy, timeout and free/cost ceilings permit; otherwise automatically show a guided Telegram interaction (inline keyboard, ForceReply, or Mini App form), preserving user input and draft/candidate. Never silently guess fields.
- **Always-on deterministic business authority:** trusted tenant identity and authorization, data validation, confirmation for AI-derived mutation, idempotency and actual persistent result receipts stay in place on every path; there is no AI-side unrestricted MUTATE.
- **User override / no-AI accessibility:** Free Core basic records, retrieval, reports and available receipt/manual entry do not stop when AI is unavailable. An accessible structured form path is part of usability, not a hidden emergency developer command.
- **Operational fallback:** policy-active quotas/circuit breakers may proactively skip an unhealthy, slow or exhausted model *without falsely reporting a successful AI reply*. Switches cannot silently incur paid usage.

**Latency optimisation before any swap (test against measured stage timings):**
1. Measure ingress, time-to-first-user-ack, model time-to-first-token, model completion/tool decision, validation/persistence, outbound Telegram reply, retry wait and full request P50/P95/P99. Preserve D-052 semantics.
2. Use bounded intent/tool schema, compact prompts and selected history; avoid huge conversation contexts and redundant model turns; test small/free/fast models on real mixed Malay-English field samples.
3. Keep model and tool execution distinct; call one bounded tool intent when possible rather than unlimited recursive steps or serial multi-model chains.
4. Telegram quick acknowledgement / typing status / progressive message edits may improve perceived latency, **but do not reduce inference time** or count as authoritative completion. Telegram chat chunking is not a guarantee of faster tool routing. Chunk context only when semantic boundaries are safe, and avoid splitting one transaction into independently committed chunks.
5. Introduce bounded timeout; use a circuit breaker and sensible recovery. Do not repeat OpsMate's long silent poll/retry path. A 429 rate limit is different from a 5xx temporary error and may require direct degraded UX rather than more calls.
6. If the AI-first route cannot deliver acceptable field accuracy/latency/free-tier cost despite tuning, compare model/provider changes, targeted deterministic fast paths and UX forms before deciding whether to change the default UX path. Do not equate slow AI with slow Cloudflare.

**Telegram candidate options (each requires app-level access checks and UX testing):**
- InlineKeyboardMarkup for category/confirm/correct/cancel choices.
- ForceReply and stepwise prompts for missing fields.
- Telegram Mini Apps for richer mobile structured forms if justified by time-to-value; validate signed `initData` server-side, not `initDataUnsafe`.
Official sources: https://core.telegram.org/bots/api and https://core.telegram.org/bots/webapps

**Cloudflare vs Google study SAVED:** Section B remains the dated comparative reference. Relevant 2026 verification: Cloudflare Worker Free **10ms CPU** budget is **not a 10ms AI/network wait timeout** (network wait does not count as CPU time); see https://developers.cloudflare.com/workers/platform/limits/. D1 Free **5M rows read/day**, **100k rows written/day**, **5GB storage**: https://developers.cloudflare.com/d1/platform/pricing/. Google Apps Script quotas are **per account/service**, including consumer **20k URL Fetch/day**, **6min/script execution**, trigger total runtime **90min/day**: https://developers.google.com/apps-script/guides/services/quotas . Cloudflare AI Gateway dynamic routing can enforce budgets/rates and use fallback, but upstream free model capacity/keys/privacy do not become guaranteed/free merely because routing is available: https://developers.cloudflare.com/ai-gateway/features/dynamic-routing/.

**Evidence reuse, avoid redundant Purchase tests:** OpsMate already supplies the selected Purchase behaviour/guard/regression reference. Do **not** run a new four-mode end-to-end Purchase behaviour trial as a prerequisite to E-016. Reuse OpsMate's frozen behaviour maps, tests and documented known gaps. E-016 remains the four-way **central infrastructure** comparison; new tests must focus on unresolved DELTAS (Cloudflare free hosting/webhook/tenant/quota and AI-first-to-form recovery/Telegram UX, privacy and measured latency), with the *smallest* necessary synthetic contract smoke tests. Later E-006 cross-composition regression stays a separate release/integration proof, not a mandate to repeat an earlier exploratory Purchase bake-off.

**New measurement terms for AI-first trial:**
- AI-first routing adoption by natural-language request class; initial AI success/clarification/misinterpretation rates.
- clear/explicit deterministic bypass without wrong-route incidence.
- AI primary failure -> secondary provider recovery within latency/privacy/cost budget.
- fallback-to-form useful-action completion rate, abandoned sessions, retained field/draft state and duplicate write count.
- subjective conversational convenience AND objective P50/P95/P99, first acknowledgement and full completion.
- separate infrastructure cost per useful action from provider/model usage and storage expense.
- `80–90%` remains an exploratory *no-AI capability availability* denominator only; it is **not** a product KPI or expectation of message-level AI bypass in an intentionally AI-first design.

**Status:** OWNER-REQUESTED TRIAL DIRECTION / E-022 PLANNED (not executed); AC-010 & AC-012 CANDIDATE; D-029/L-023 and D-055/L-046 remain LOCKED; PRE-ARCH NOT LOCKED.
