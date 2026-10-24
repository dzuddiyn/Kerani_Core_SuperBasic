# Kerani AI — OpsMate Lessons to Mandatory Release Gates (D-065 / L-051)

**Status:** **OWNER LOCKED — P0 RELEASE / EVIDENCE CONTRACT ONLY**  
**Approval:** 2026-10-24 — explicit `LOCK D-065/L-051 & COMMIT`.  
**Source of Truth:** `ZASS_Kerani_Core_SuperBasic.md` D-065 / L-051, with ZASSIMPLE DESIGN/ACTION_PLAN projection.  
**Linear tracker:** [KAI-12](https://linear.app/dzuddiyn/issue/KAI-12/d-065l-051-opsmate-lessons-mandatory-kerani-release-gates), Backlog until actual acceptance evidence.  
**This authorization:** Documentation, decision LOCK and linked commit tracking **only**; **NO** runtime implementation, schema/data migration, production/Cloudflare/Apps Script change, real customer access or test PASS claim.

## 1. Direct owner lessons from OpsMate (observations, NOT root-cause findings)

After approximately 1.5 months developing OpsMate, the owner reported:

1. **Version / fixture fragility:** Progressing test versions to stable versions frequently caused functions to disappear/break after mock records were cleared from Sheets/database.
2. **No visible value:** Without a dashboard/UI, users must guess what happened to the records they entered, which threatens adoption. Candidate surfaces: optimized Google Sheet for admin, Telegram Web UI / Mini App, free/open-source template or purpose-built responsive web, later Android Home Screen app icon / PWA. All displayed data must reflect the live authoritative database **almost in real time**, with correct freshness semantics.
3. **AI data retrieval inefficiency:** AI should consume a clearly structured knowledge/read model instead of scanning dozens of spreadsheet tabs for each question.

**Important evidence boundary:** These are owner-reported pain points and UX hypotheses, not a completed code audit of OpsMate or a measured Kerani defect rate. We do **not** assert mock clearing is the proven sole cause. RG-01 demands validation rather than inventing a diagnosis.

## 2. OWNER LOCK D-065/L-051 — three release blockers

**Overall commitment:** Kerani AI cannot be called stable/ready for a scoped user release when upgrading breaks existing functionality, users cannot readily see saved data, or released AI/summary features cannot obtain reliable, permission-scoped structured data. Gates are evaluated for the actual release surface and use cases. No data is marked committed/visible until authoritative receipt exists.

| Gate | P0 outcome / meaning | Applies to |
|---|---|---|
| **RG-01 Upgrade Integrity** | Promote a new version without dropping baseline functions, breaking schema/config after mock deletion or harming data, with tested rollback. | Every real/pilot release and version migration |
| **RG-02 Free Visible Value** | Basic tenant-safe records, recent activity, tasks and truthful business summaries visibly available with near-live freshness; no paid AI required to see what user entered. | Every real/pilot Free release; any channel needs a usable supported view, not necessarily all future UI surfaces |
| **RG-03 Knowledge-Ready Read Model** | Derived, versioned, tenant-scoped structured read model feeds dashboard and any AI/summary/query layer with provenance, deterministic totals, missing/stale indicators and minimal tab access. | All released data summaries; AI-specific tests mandatory when AI-query capability is in release scope; **AI itself is not a prerequisite for Free Core** |

### RG-01 — Upgrade Integrity

**Required separation:** `DEV/MOCK` (synthetic fixtures), `STAGING` (version-upgrade test), `PILOT/PROD` (real tenant records) have independent data lifecycle and configuration/credentials. Existing Apps Script/Sheets constraints may require logical isolation, but the proof must show no accidental cross-environment deletion. Necessary seed/config/lookup tables **are versioned schema/seed**, never disposable mock data.

**Required evidence before PASS:**
- Tests of empty dataset, missing optional business history, mock records cleaned, seeded configuration present, and fresh tenant onboarding.
- Test old→new version on representative versioned schema with known before/after record counts, foreign keys/references, permissions and audit trail (as applicable).
- Regression of Free Purchase/Sale/Inventory/Observation/Task, basic retrieval/report, CRUD, Telegram Mini App (where shipped), and authentic receipt/commit status.
- Rollback or forward-recovery drill restoring a verified usable state without customer-record reset/loss; record migration version and backup/restore proof.
- Confirm no source-code behavior depends on row positions, known mock IDs, optional sample tabs or disposable fixtures.

**FAIL/STOP:** clearing mock data breaks functions; legitimate seed/config is lost; upgrade silently removes a supported workflow; real records disappear/change; rollback corrupts or duplicates records. The specific OpsMate root cause remains **UNVERIFIED**, so the first test is to reproduce and classify this behavior using controlled synthetic data.

### RG-02 — Free Visible Value + near-live fidelity

**LOCKED Free experience:** Free includes an **easily accessible basic visible data view**, not only a chat transcript or a paywalled dashboard. Recommended reuse: one responsive tenant-specific UI inside the already LOCKED Telegram Mini App D-057/L-047, with recent saved records, simple factual purchase/sale/stock/activity/task summary, record status and last-updated timestamp. It must remain usable without AI. If initial launch is chat-first per D-061/L-049, do not gate the *first experimental chat slice* on a large dashboard implementation; however **do not call the Free product ready for general release until a minimum supported visibility view exists**. User's benefit is seeing the results of entry without repeatedly asking an AI to regenerate them.

**Free/Premium boundary:** Basic visible current records, task status, factual KPIs and basic retrieval/report are **Free**. Rich filtering/charts, advanced analysis/correlation/forecast, expanded automation and cross-domain intelligence remain D-059/D-050/D-051 **Premium CANDIDATES**; no premium tier, price or gating is selected here. Do not promote D-059's entire Business Workspace to Free.

**Candidate UI strategy (NOT architecture lock):** Google Sheets summary for admin/audit or first prototype; a lean shared responsive web UI serving Telegram Mini App first; optional template/open-source visual components; later external PWA/Home Screen icon with separate browser-session authentication. **Do not build 4 separate dashboards**, and do not assume Telegram `initData` authenticates arbitrary browser sessions.

**Freshness acceptance:**
- After a verified authoritative `COMMITTED` record, its corresponding row, KPI/summary and source drill-down are correct, tenant-isolated and eventually visible without manual re-entry or AI regeneration.
- UI labels `PENDING`, `COMMITTED`, `SYNCING`, `STALE`, `ERROR`, `EMPTY` where appropriate, with data version/watermark and `last_updated_at` or equivalent. Never show stale cached totals as if current.
- **Initial pilot measurement hypothesis:** P95 of `Core commit receipt → visible current dashboard record` **≤5 seconds** under defined sample load. This is **NOT an approved SLA, measured result or frozen universal cutoff**. If not achieved, report distribution and root cause; propose user-acceptable threshold for owner approval before release.
- Include tests for multi-tenant ACL, no-data state, simultaneous updates, pending projection, browser vs Telegram auth boundaries (if those surfaces exist), non-AI usability and source-row reconciliation.
- Trigger projection in the authoritative commit/outbox path, not solely via Google Sheets `onEdit()` (script/API writes do not trigger onEdit). Reconciliation repairs missed projection updates.

**FAIL/STOP:** saved record cannot be located; displayed total mismatches underlying scoped authoritative data; one tenant can see another's data; stale numbers masquerade as current; no usable supported Free basic view; critical screen fails due only to AI being unavailable.

### RG-03 — Structured Knowledge-Ready Data

**Three logical layers, not three competing sources of business truth:**

```text
One AUTHORITATIVE RECORDS / Core SoT
  validated purchases · sales · inventory · observations · tasks · audit · event/commit IDs
                │ published/reconciled derived updates
                ▼
Rebuildable STRUCTURED READ MODEL
  tenant-scoped recent records · totals · stock · tasks · date/period views
  source record IDs · commit version / freshness watermark · consistency markers
           ┌───────────────┴────────────────┐
           ▼                                ▼
Basic Free dashboard/retrieval     AI KNOWLEDGE CONTEXT
                                     permitted bounded read tools
                                     summaries + source refs + missing-data flags
                                     natural language interpretation, NOT business authority
```

- Authoritative mutations require deterministic/domain validation and tenant authorization. Derived metrics (including spending, revenue, stock) computed deterministically, with source IDs and data freshness; **do not label `sales - purchases` as verified net profit** without all necessary costs.
- A query tool such as `getWeeklyActivitySummary(tenant, range)` or `getStockBalance(...)` is **a design example**, not an implemented endpoint. Query scopes must be server-verified, bounded, indexed/paginated where appropriate and retain permission filtering.
- Read-model updates may be synchronous for small V1, asynchronous/outbox/Queue for proven needs, but must be **rebuildable/reconcilable** from the same Core SoT and must never fabricate `SAVED`. A failed/late projection is marked stale, not silently accepted.
- AI consumes only necessary structured, versioned, authorised knowledge context and source references rather than reading all Sheets tabs per request. AI must distinguish no data, stale data, missing costs, unsupported inference and access denial; must not invent totals or gain mutation rights.
- No vector database/RAG mandatory in Free. Add embeddings/full-text/RAG only after narrow field evidence and privacy/cost justification; no private business data sent to unapproved AI endpoint.

**FAIL/STOP:** AI accesses cross-tenant data; outputs invented or untraceable business totals; structured summary cannot be reconciled with source; a production request scans dozens of tabs without bounded plan; Free core stops working when AI is off.

## 3. Minimal acceptance matrix (proposed test IDs; ALL NOT RUN)

| ID | Gate | Synthetic / pilot evidence | Expected PASS proof |
|---|---|---|---|
| `RG01-T01` | RG-01 | Empty fresh DB and missing optional tabs | Seed/config survive; truthful empty state; baseline functions work |
| `RG01-T02` | RG-01 | Populate isolated mock fixtures, then delete **only mock** | No function/config/schema regression; CRUD/reports work |
| `RG01-T03` | RG-01 | Existing schema/version → new version; rollback/restore | Record identity and counts, audit, access and commit semantics preserved |
| `RG01-T04` | RG-01 | Feature regression after migration | All supported Free workflows and shipped UI pass |
| `RG02-T01` | RG-02 | Commit purchase/sale/activity/task and open Free UI | Correct recent record, totals/status, provenance and tenant isolation |
| `RG02-T02` | RG-02 | Concurrent SAVE; projection delay/error; stale cache | Visible freshness markers, reconciliation and measured P50/P95/P99 |
| `RG02-T03` | RG-02 | No-AI, empty data, no permissions, mobile entry | UI remains usable; no data leak or false success |
| `RG03-T01` | RG-03 | Ask a bounded weekly summary using structured read tools | Correct period/scope/derived figures with source IDs and watermark |
| `RG03-T02` | RG-03 | Missing price/cost/data, stale projection, AI 429/5xx | No hallucinated accounting; truthful insufficiency; no-AI basic access |
| `RG03-T03` | RG-03 | 30-tab Sheets fixture versus bounded read model | No blanket live tab-scan; reproducible query/refresh and cost evidence |
| `RG03-T04` | RG-03 | Tampered tenant ID, cross-tenant record, revoked identity | Fail closed; no leakage; audit outcome |

**All acceptance thresholds other than correctness and safety remain pilot-calibration hypotheses.** The initial RG-02 5-second P95 is an experiment, not an implicit release PASS. Record actual before/after test evidence, IDs, timestamp, environment, source commit, scope and failure receipts. Review real-user benefit (can user independently find record and understand value?) before calling VALID successful.

## 4. Cross-decision reconciliation (preserve these authorities)

| Existing ZASS | D-065/L-051 effect |
|---|---|
| **D-016/L-011** | Strengthens useful basic records, tasks, retrieval and reporting as a Free visible experience; no AI required |
| **D-055/L-046** | AI optional; structured Free read model and dashboard must work without AI |
| **D-057/L-047** | First-class deterministic Telegram Mini App is preferred Free presentation surface; exact screens/hosting remain candidates |
| **D-061/L-049** | Chat-first first slice remains; minimum visible view required by broader Free release, not compulsory full dashboard form for each chat |
| **D-059 CANDIDATE** | Premium advanced interactive Workspace remains candidate; baseline record visibility is not paywalled |
| **D-052** | Add `commit→projection→visible` latency/freshness/real user result to existing P50/P95/P99 observations |
| **D-064/L-050** | Same stable versioned job identity and Core SoT through Worker direct→Queue; no false ACK-to-SAVE; dashboard projection awaits actual COMMIT |
| **D-060/063 CANDIDATES** | No automatic provider/queue/data-store choice; WhatsApp quota thresholds unchanged |
| **D-062 CANDIDATE** | Brand `RekodUntung.ai` remains NOT LOCKED, and nothing here implies verified net-profit functionality |
| **E-016/E-018** | Architecture still evidence-led; benchmark only unproven deltas, with no full project PRE-ARCH lock |

## 5. Governance and STOP

- **LOCKED now:** release obligations RG-01, RG-02, RG-03, one authoritative business source, basic Free visibility and AI-safe scoped derived knowledge, fail-closed/stale-truthful receipts.
- **NOT LOCKED now:** Google Sheets vs Cloudflare storage/DB, projection technology, UI framework/theme/open-source template, precise dashboards/screens, PWA/widget install, RAG/vector DB, specific time/cost SLA, test fixture implementation, global cloud PRE-ARCH and release.
- **NO ACTUAL PASS:** No OpsMate source code audit, clean-up regression, UI freshness timing, AI-query acceptance or production test executed as part of this commit.
- **One NEXT:** `RG-ACCEPTANCE-01 — READ-ONLY Fixture & Evidence Matrix Design`: map existing OpsMate baselines and Kerani Core contracts to synthetic fixtures and objective PASS/FAIL criteria, then obtain separate approval before writing or executing tests.
