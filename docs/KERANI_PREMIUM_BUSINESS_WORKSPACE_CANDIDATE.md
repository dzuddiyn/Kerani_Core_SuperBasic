# Kerani Premium Business Workspace — Design Candidate

**Status:** **CANDIDATE — DESIGN/DISCOVERY ONLY; NOT LOCKED; NOT IMPLEMENTED**  
**Owner direction:** 2026-10-19 — Save as a formal candidate and track in Linear.  
**Tracking:** [KAI-7](https://linear.app/dzuddiyn/issue/KAI-7/kerani-premium-business-workspace-candidate-concept) — `Backlog`.  
**Source of Truth:** `ZASS_Kerani_Core_SuperBasic.md`, D-059 candidate; current ZASSIMPLE design.  
**No authority granted for:** PRE-ARCH, provider choice, repo/application implementation, paid entitlement or pricing, production deployment, Google Drive OAuth, external task writes, new cross-product shell or customer-data access.

## 1. Product thesis / intended value

Offer each business/tenant a **lightweight Premium Business Workspace** reachable from Kerani's Telegram bot. The bot should explain a requested business summary clearly in natural text, with a contextual **Open Dashboard** button linking to a tenant-scoped interactive web view for exploration. Rich graphs/tables, filters/search, forecast, document links and task workflow should remain optional, evidence-earned premium conveniences; Free Core's basic records, task, search/retrieval and basic reports are not removed.

**One authoritative backend, multiple presentation surfaces.** Kerani Free deterministic Telegram Mini App was already approved as a *first-class UI principle* under D-057/L-047; the Premium workspace is a *candidate higher-value experience layered onto that shared business authority*, not a replacement Free UI and not a separate authoritative system.

### Candidate user journey

1. User asks in Telegram chat: “Ringkaskan jualan, belanja dan kerja minggu ini.”
2. Kerani checks identity, active tenant, entitlement, time range and source-data availability.
3. Backend computes factual metrics, record links and data freshness from authorised data; AI may **describe** the verified result in useful language. If the report is basic Free scope, it remains accessible without Premium charges.
4. Telegram sends a readable short text summary with provenance/time window and a **Buka Dashboard Interaktif** button when authorised/available. Do not invent totals, explain limitations, or promise a successful operation before receipts exist.
5. The dashboard opens scoped to that user and tenant. User may change filters, view charts/tables, inspect source rows, search and optionally request premium analysis/forecast.
6. Browser/PWA and Telegram Mini App should map to the *same Kerani tenant and records*, with each entry surface performing its appropriate login. Never put access tokens, sensitive IDs or privileged context into shared links.
7. Data mutations, task actions and integrations obey ordinary scope, deterministic validation, explicit approvals where relevant, idempotency and audit.

## 2. Candidate dashboard capabilities

| Capability | Possible value | Gate / boundary |
|---|---|---|
| Business-specific home | KPIs, relevant summaries and key actions for Agro / Servis Teknikal / Makanan & Tempahan | Configure views using actual domain/tenant contracts; **do not** claim an already proven universal dashboard renderer |
| Interactive charts and tables | View sales/expenses, activity, inventory, trends and drill down to source records | Calculations originate from authoritative records; chart figures and table rows agree; annotate missing/incomplete data |
| Search, filters and history | Filter by dates, activity, transactions, tasks and authorised documents | Tenant-scoped server-side search, pagination and access control; basic Free retrieval still Free |
| Analysis and forecasts | Premium correlation, pattern explanation, forecasts and recommendations | D-051 remains **CANDIDATE**; disclose available history, assumptions, uncertainty, error and cost; suppress unsupported forecasts |
| Work tasks and reminders | See Kerani Task status, task breakdown, follow-up and authorised actions | Core basic Task Free; scheduled reminders/automation may be Premium candidate D-050; approvals and audit apply |
| Google Drive link / documents | Jump to user's own authorised folder/files, attach relevant record provenance | Start with explicit user-provided links/permissions; no general Drive browsing/sync or OAuth token handling by default |
| External task sync | Future link/sync with Google Tasks or other task system | **DEFER** until real demand. Read-only discovery first; if proven, one-way bounded sync with authoritative source, consent, dedup, conflict policy, retries, audit, revocation; no two-way auto-write as starting assumption |
| Android Home Screen access | One-touch dashboard shortcut; possible installable PWA | **CANDIDATE**; Telegram Mini App in a Telegram WebView and standalone browser/PWA are different launch/auth contexts. Evaluate manifest/installability and browser session login without trusting Telegram initData outside Telegram |

**Forecasts and analysis:** deterministic/analytics backend derives metrics and provenance; AI may interpret/explain but must not fabricate datasets, business totals or causal inference. Display source, period and last-updated time, forecast confidence/interval/method when supported, and clear **INSUFFICIENT DATA** when not.

## 3. Candidate interface/identity pattern (not selected architecture)

~~~text
Telegram Chat (natural language)
    → verified tenant-scoped summary / action receipt
    → [Buka Dashboard] contextual button
           ↓
   HTTPS Premium Business Workspace (interactive web UI)
      ↗                         ↖
 Telegram Mini App         Browser / Android PWA
 verified initData         separately authorised session
       └───────→ Same Kerani Core / Premium APIs ←──────┘
                      ↓
   trusted tenant + roles + entitlement + business rules
             authoritative records / analytics
                      ↓
           optional approved integrations
~~~

- Do not duplicate business logic or authoritative data in frontend, Telegram bot or Google Drive.
- Telegram Mini App backend must verify signed `initData`, time validity, scope and permissions. External browser/PWA sessions need a **separate verified authentication/binding design**, not implicit trust of Telegram WebApp data.
- A dashboard link must not grant tenant access by itself. Any deep link should only carry bounded, non-secret view context with permission rechecked at backend.
- Each business sees only permitted tenant/domain data, including drive links, tasks, history and analytics. Tenant switching, roles, shared devices and token/session expiry require deliberate tests.
- Dashboard/AI requests must have measured latency, cost/quota/entitlement rules, safe failed actions and truthful `NOT AVAILABLE`/expired/permission error states.
- Reuse existing UI/domain contracts when proven; do not pre-build CrossAI/Kerani/Temaya generic Mini-App shell.

## 4. Free vs Premium principle

**Free remains independently useful:** ordinary record creation, basic manual reports/retrieval, task tracking, basic receipt/manual input and D-057 deterministic Mini App. Premium should charge only for demonstrated additional convenience/intelligence/automation, never block already-LOCKED Free baseline just to make the dashboard appealing. Detailed feature gating, billing and Credit Pass prices **remain OPEN**.

**Google Drive distinction:** One-click links to a tenant-authorised Drive resource are a lightweight feature hypothesis; optional user-owned Drive OAuth storage/integration is an existing unproven challenge under D-053. Neither requires Premium owned Apps Script edge; that separate architecture is deferred.

## 5. VALID-first minimal experiment (future only, not authorised now)

**First possible experiment:** With consented realistic/synthetic-labelled records and a small pilot audience, test exactly one slice:

`Ask summary → factual concise Telegram reply → Open Dashboard → chart/table → inspect underlying records`

Acceptance hypotheses to **test**, not claim:
- Pilot user can understand the summary and independently confirm one displayed metric from source records.
- Deep link correctly authorises only the intended user's tenant; denies unauthorised cross-tenant access.
- Dashboard correctly represents empty/partial/stale data, missing permissions and disconnected AI.
- Page and summary feel responsive with recorded P50/P95 + error/cost/abandonment metrics.
- Actual users report that the dashboard meaningfully improves their real decision/task compared to basic text-only reporting.

**Progression only if earned:** filter/search → domain-specific slice → one bounded insight/forecast → Drive link → internal Task dashboard → external task-sync feasibility → Android PWA installation. Do not make every listed feature a compulsory MVP.

## 6. Unresolved decisions / STOP rules

- **Open:** intended Premium cohort and first domain, key dashboard question, data availability, which charts/metrics add value, user authorization flow, task integration source of truth, Google Drive data permission model, Telegram Mini App vs independent PWA UX, price/credits, hosting/runtime/provider, analytics/model boundaries, actual adoption.
- **STOP:** no product or architecture LOCK, no claim of evidence from a mock, no direct customer data/production access, no OAuth consent prompt, no write-back/task sync, no new infra/deployment, no current E-016 or Agro Demo critical-path task.
- **Timing:** preserve OpsMate PILOT_REAL handover and independent clean Agro Demo as priority; revisit Premium only once real user value justifies a narrow trial. Premium customer-owned Apps Script Edge is a separate future ZERO → ARCHITECTURE decision, not selected here.

## 7. Existing lineage (unchanged)

- **D-057/L-047 LOCKED:** Telegram Mini App as first-class *Free* deterministic UI (core product principle only).
- **D-050/D-051 CANDIDATE:** Premium Operations (Alert/Remind/Report/Ask) and Intelligence (Analysis/Correlation/Graph/Proposal/Forecast).
- **D-053/L-044 LOCKED:** minimum user-value delivery gate; optional customer-owned Google Drive OAuth challenge.
- **D-054/L-045 LOCKED:** convenience-first and evidence-led Premium.
- **D-055/L-046 LOCKED:** Free independent usefulness, AI optional for basic operations.
- **D-058/L-048 LOCKED:** 8V VALID-first iterative real-use evidence discipline.
- **D-059 CANDIDATE:** this *Premium Business Workspace* presentation concept; not a new LOCKED decision, Premium entitlement or architecture.
- **KAI-7:** non-authoritative Linear tracker, not an alternate SoT.

**Capture result:** This is a documentation-only candidate and planning reference. **No prototype, validation result, runtime selection or implementation is claimed.**
