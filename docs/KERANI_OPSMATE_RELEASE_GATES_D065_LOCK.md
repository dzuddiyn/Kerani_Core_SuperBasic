# Kerani AI — OpsMate Lessons → Mandatory Release Gates RG-01 / RG-02 / RG-03

**Decision:** D-065, **OWNER LOCKED** as L-051 on **2026-10-24**.  
**Scope:** Kerani Free release/readiness acceptance from the owner's approximately 1½-month OpsMate development experience. These are **P0 release gates**, **not proof that implementation exists**, not authorisation to run tests or deploy a new system.  
**Authority:** `ZASS_Kerani_Core_SuperBasic.md` D-065/L-051; design and action plan projections; Linear KAI-11 for progress tracking.  
**Evidence distinction:** The three OpsMate problems are **owner-reported field/development observations**, not a forensic verified root-cause analysis. Proposed mechanisms below are **engineering mitigations**, not factual claims about exactly why OpsMate failed.

## 1. DUMP — three owner-reported OpsMate weaknesses

1. **Promote test to stable:** Some working functions vanish/break after cleaning Sheets/database mock/test data or preparing a stable version. Prevent regressions and data/config coupling in Kerani.
2. **No visible dashboard:** Users may abandon the app if they expend effort keying records but cannot see timely business outcomes. Quick choices: optimized Google Sheets dashboard, Telegram Mini App/web UI, free/open-source web template/ChatGPT-assisted UI, optional phone Home Screen icon/PWA. **Almost-live real-time** sync with authoritative records is essential; avoid building multiple duplicate UI systems.
3. **AI knowledge access:** AI must consume an efficient, structured, bounded knowledge/query layer instead of scanning dozens of raw Sheet tabs for each question.

**Product thesis:** Chat-first recording is insufficient without observable value. **Free users MUST be able to see their records and basic results.** Premium may add deeper interpretation, richer analytics/forecast and business-workspace conveniences but cannot gate essential record visibility already promised by Free.

## 2. Three mandatory release gates (LOCKED, P0)

### RG-01 — Upgrade Integrity / Non-Regression

**Locked outcome:** A promoted Kerani version does not lose a previously supported committed Free capability or silently corrupt/drop customer records after test/mock data cleanup, schema change, configuration/seed cleanup or deployment. Treat **code**, **data/schema**, **seed/config**, **synthetic test fixtures** and **customer/tenant records** as separately owned/versioned concerns.

**Minimum pre-release proof:**
- Separate DEV/mock, reproducible staging, and consented PILOT environments/datasets; test cleanup must not have permission to erase pilot/customer records. If separate infrastructure is impractical initially, use verified hard isolation and scoped destructive operations, not unbounded wipe scripts.
- **Empty data / first run:** all supported UX routes load, show a truthful empty state, don't rely on fake seed rows to calculate or authenticate.
- **Mock purge then retest:** removing fixture rows does not remove mandatory configuration, schema definition, ID allocation, mappings, formulas/templates or tenant bootstrapping; run baseline CRUD, retrieval/report, auth and dashboard/AI queries.
- **Upgrade migration:** known old-version dataset → current schema, mapping and validation; checksum/count/integrity before/after where appropriate. Schema changes versioned with compatible backward reads or tested migration; NO destructive clean on authoritative data.
- **Regression contract:** replay real-*shape* anonymized/synthetic examples, compare old supported functions, error semantics and business invariants; no assertion of PASS from documentation or sample sheet.
- **Rollback/recovery:** backed-up/versioned configuration and data, reversible application rollback *or* proven forward-recovery when schema rollback is unsafe, and restore drills that keep any newly committed production records safe.
- **Receipt:** capture commit/release version, environment, fixture IDs, migration evidence, specific test PASS/FAIL, dataset provenance and discovered differences.

**FAIL / STOP:** a previously supported record workflow disappears without explicitly approved change, configuration is silently deleted by fixture cleanup, unauthorized tenant data is lost, new version cannot read old valid records, or rollback/recovery damages authoritative data. Don't misstate unknown root cause as proven.

### RG-02 — Visible Value / Minimal Live Free Dashboard

**Locked outcome:** Every supported Free tenant can **see the useful result of records already committed** in a visible, independently usable basic UI without compulsory AI or Premium access. Reuse D-057/L-047 **Free Telegram Mini App** as preferred initial customer-facing surface while retaining D-061 chat-first onboarding. Dashboard visibility includes relevant KPI/summary, latest records/history, activity/stock/task status as applicable to currently supported modules; don't promise all domains/modules are simultaneously implemented.

**Minimum pre-release proof:**
- A user can **record → validate/confirm as required → receive authoritative COMMITTED receipt → open Free dashboard → see record and an accurate basic count/summary**, with server-verified tenant permissions.
- A page opened before the commit **refreshes or is safely refreshable** to the new record. Data freshness timestamp / source revision or projection watermark is visible; stale/pending/failed or empty data must be labelled and recoverable. Never display stale values indistinguishably as live.
- Dashboard and Telegram chat basic reports use the **same trustworthy Core records/read APIs**, not divergent totals. Source drill-down for at least one visible figure.
- Screens remain helpful on mobile; one front end for Telegram Mini App may later have independently authenticated PWA/Home Screen candidate, not mandatory Android native widgets or parallel Free sites.
- **Near-real-time target:** candidate pilot acceptance hypothesis **P95 commit→fresh-visible ≤5 seconds** with evidence under defined load, browser state and data size; exact bound is **not a hard platform SLA/LOCK** until measured and explicitly approved. Measure P50/P95/P99, stale/projection error rate and backfill time; failure must show honest freshness.
- Sheet may support admin/debugging/prototype dashboard but cannot replace mandatory usable tenant-scoped Free customer UI without real usability proof. Avoid relying on Apps Script simple `onEdit` triggers for programmatic/API mutations: refresh the projection from authoritative commits or a reconciled change path.

**FAIL / STOP:** user records are committed but inaccessible/invisible to authorized user; dashboard is Premium-only; it misstates totals, presents unsynchronized stale numbers as current, leaks other tenant data, silently misses records after worker retry or declares SAVE before commit.

**Free/Premium boundary:** Free includes simple record/transaction counts, purchase/sale/stock/task/activity summaries, basic history, retrieval/report and truthful freshness. **Premium Business Workspace D-059 remains CANDIDATE** for optional richer exploratory charts, multi-domain intelligence, forecasting, deeper automation, PWA conveniences where value is proven. Do not imply current features/screens have been implemented or validated.

### RG-03 — Knowledge-Ready Data / Grounded AI Access

**Locked outcome:** For any AI/query/summary capability included in a release, AI reads **tenant-scoped structured read models, compact indexed summaries and bounded data-access tools**, not unbounded scans of dozens of operational Sheet tabs on every request. Maintain **one authoritative Core Source of Truth**. Read model is rebuildable and versioned **projection**, not a second mutable accounting/operations database or independent source of business truth.

**Minimum pre-release proof:**
- A Core `COMMITTED` event updates an indexed, well-defined view or schedules retriable projection update; each projection has `source_record_ids`, source revision/event watermark, tenant/domain, aggregation period, freshness and missing-data markers as relevant.
- AI tool contract like `getBusinessSummary(scope, range)`, `getRecentRecords(...)`, `getInventoryStatus(...)` enforces user/business rights and bounded time/row/token budgets. Exact tool names and storage technology are **DESIGN OPEN**. Basic no-AI queries from D-016/D-055 must still work when the model is unavailable.
- For a report grounded in source records, deterministic backend computes totals; AI only expresses/explains supplied verified summaries, cites record/period provenance and admits incomplete data. No fabricated net profit or claims of causality without proper cost/inputs.
- Empty, stale, delayed, corrupt and recomputation-from-SoT scenarios tested; rebuilt projection reconciles with authoritative counts/hashes. Newer Core write is not invisible forever because a background projection silently failed.
- Performance checks compare bounded read model vs naïve full Sheet scanning under representative fixture volume, recording actual latency, correctness, data exposure, read/write quotas and recovery cost. **No requirement to deploy vector DB, embeddings or generalized RAG by default.**

**FAIL / STOP for released AI/summary feature:** invented numbers, unauthorized cross-tenant access, no source trace, divergence between UI/AI and Core, unbounded tab scanning required for ordinary queries, or inability to detect stale projections. **RG-03 does not block an otherwise correctly functioning no-AI Free baseline solely because optional AI is disabled or unlaunched**.

## 3. One-data-truth architecture projection (candidate technology, LOCKED semantics)

```text
Telegram Chat / Free Mini App / WhatsApp (when enabled)
                 │
                 ▼
     Kerani Core Auth + Validate + Commit
         ONE AUTHORITATIVE BUSINESS SoT
                 │
     source revision / commit receipt
                 │
                 ▼
          Rebuildable Read Model
      by tenant/domain + source watermark
             /                   \
            ▼                     ▼
    Free Dashboard          Grounded AI Query
 latest records/KPIs         bounded retrieval/
 status/freshness             sourced explanation
```

- **No duplicate business writes** between dashboard/AI and Core; UI is thin. Dashboard visible only after authoritative COMMIT, not webhook ACK, Queue accepted or AI response.
- **Projection pipeline** may be synchronous or asynchronous and remains subject to performance and correctness tests. Queue-ready D-064/L-050 for WhatsApp is unaffected: a Queue does not guarantee business data/summary has committed or refreshed.
- Source-of-truth may involve Apps Script/Sheets in a narrow pilot; final runtime, database or read-model implementation remain E-016 architecture challenges. Never presume Sheets as reliable high-concurrency OLTP by default.
- **Freshness contract** is mandatory; actual refresh transport (poll-on-open, short bounded refresh, SSE/websocket/event sync) is **NOT LOCKED**. An idle phone tab and disconnected network need truthful stale UX.
- Authorization revalidated server-side for Mini App `initData` and separately for any browser/PWA session. Never trust tenant IDs or unauthenticated dashboard URLs.

## 4. Minimal example Free dashboard — illustrative not implemented

- Header: Business name, selected date range, last updated / projection status.
- Simple verified cards: Sales total, Purchase/Expenses as *recorded*, operational activity count, Task done/pending, basic inventory count **only if underlying inputs are complete**.
- Latest records with date/status and direct tenant-scoped source drill-down.
- Empty/pending/stale/error states and retry/reconciliation indicator.
- Chat → `Buka Rekod` / `Buka Ringkasan` in Free Mini App; use the same API; avoid making users repeat AI prompts just to view their own data.
- **Do not label Sale–Purchase difference as net profit** without all required expenses, stock/COGS, accrual etc. D-062 RekodUntung.ai remains unverified brand candidate.

## 5. Compatibility with existing LOCKs and non-LOCKs

| Existing decision | Preserved boundary |
|---|---|
| **D-015/L-010** | Deterministic validation/confirmation before authoritative write; no fictitious SAVED |
| **D-016/L-011** | Free basic records, history, retrieval and reporting remain useful |
| **D-018 portability** | Data ownership/export not impaired by projection/dashboard |
| **D-023 tenant identity** | Business and User IDs independent of channel and display surface |
| **D-052 latency** | Measure P50/P95/P99 and error/retry; do not assert untested thresholds |
| **D-055/L-046** | No-AI useful Free baseline |
| **D-057/L-047** | First-class deterministic Free Telegram Mini App; RG-02 gives it a visible-value minimum |
| **D-059 CANDIDATE** | Premium advanced workspace remains an optional richer tier; core visibility stays Free |
| **D-061/L-049** | Personal Free chat first; basic UI is an optional first-class way to see data, not a mandatory input form |
| **D-064/L-050** | WhatsApp V1 Worker+Apps Script queue-ready path unchanged; no pre-live ACK-before-durable receipt |
| **D-062 CANDIDATE** | No public RekodUntung.ai brand LOCK or code/repo rename |

**No forced technologies:** No locked frontend framework, Google Sheet layout/number of tabs, cloud provider, database, vector store, Cron mechanism, Telegram launch mode, widget/PWA, paid tier price, hard 5-second SLA or architecture PRE-ARCH. Product/acceptance invariants alone are LOCKED.

## 6. Future verification suite: RG-01 / RG-02 / RG-03 (NOT RUN)

| Test | Purpose / evidence | Gate |
|---|---|---|
| U01 | A previously supported Purchase/Sale/Task record still works after dev mock data deleted | RG-01 |
| U02 | Fresh empty tenant + mandatory seeds/config boots and shows empty dashboard without exceptions | RG-01/02 |
| U03 | Old dataset → new schema and rollback/forward-recovery; record IDs, tenant access and checksums consistent | RG-01 |
| U04 | Clean staging/PILOT isolation and a restricted cleanup cannot touch real records | RG-01 |
| V01 | Save record → dashboard visible latest row/summary (provenance) with P50/P95/P99 measured | RG-02 |
| V02 | Reopen/stale/offline page, projection delay/failure, partial data, source revision/last-updated shows truth | RG-02 |
| V03 | Cross-tenant access and any browser/PWA/Telegram identity confusion denied | RG-02/03 |
| K01 | Bounded tenant-scoped AI retrieval correctly explains deterministic totals with source IDs/range | RG-03 |
| K02 | Empty/stale/failed model and wrong-source request returns controlled incomplete/read-only fallback, not invented value | RG-03 |
| K03 | Projection rebuild/reconciliation from Core, including duplicate/retry and out-of-order events, gives source-equivalent result | RG-02/03 |
| K04 | Query latency/cost/privacy under tens of synthetic Sheet tabs compared with structured read model; no universal tab scan | RG-03 |

**Decision rule:** Every relevant gate must PASS using execution receipts before claiming pilot release readiness. Keep Free no-AI working while optional AI is absent; exact P95 target/fixture scale are to be proven and separately finalized. A documentation-only GitHub commit is **NOT** a runtime or UI PASS.

## 7. Governance and single NEXT

**Current work:** owner-authorized **LOCK D-065/L-051 and commit documentation**, project-scoped changes only; no testing/deployment, no real business/personal records. Linear tracking remains Backlog until actual acceptance evidence.

**NEXT — exactly one:** **RG-01/02/03 Synthetic Acceptance Matrix & Minimal Vertical Slice Design**: turn U/V/K tests into realistic non-sensitive fixtures, choose smallest Free dashboard/read-model interaction, design failure receipts/freshness criteria and explicit release GO/NO-GO without running or deploying anything until separately authorized.
