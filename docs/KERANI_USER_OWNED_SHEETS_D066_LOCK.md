# Kerani AI — Flexible Capture → User-Owned Google Sheets → Any AI

**Decision:** D-066 / L-052 — **OWNER LOCKED PRODUCT PRINCIPLE**, 2026-10-26.  
**Owner's core idea:** “bagi memudahkan software, tiada logic algorithm rumit. user boleh masukkan apa saja data, data akan terus diekstrak daripada database ke dalam sheet yang boleh diakses dalam Google drive. pengguna bebas lampirkan sheet tersebut untuk dianalisis oleh AI lain atau edit sendiri atau padam. ini idea utama.”  
**Status:** Decision approved/locked; implementation/interface/Google permissions/Cloudflare/Apps Script choices **NOT selected**, tests **NOT RUN**, no actual customer Drive/Sheets modified.  
**SoT:** `ZASS_Kerani_Core_SuperBasic.md` D-066/L-052; Linear KAI-14 (tracking only).

## 1. The LOCK: usefulness without trapping the user's data

1. **Capture-first, flexible input.** People can submit diverse business/operational data in natural chat or simple structured entry without mastering an elaborate form/workflow/algorithm. Preserve original submitted content and basic trustworthy metadata where feasible; recognize structured fields only when supported. “Apa saja data” is the product's *inclusive input philosophy*, **not** a guarantee of unlimited file types/sizes, arbitrary binary-to-cell rendering, trusted accounting totals from incomplete data or skipped authorization/validation.
2. **One authoritative Kerani Core source of business records.** A validated/authorized record receives a stable tenant-scoped ID and truthful commit receipt. Keep essential deterministic checks, consent for material writes where applicable, audit and transport retry idempotency. Do not make essential user data depend on a model's interpretation or on an editable Google Sheet.
3. **User-accessible Google Sheets copy in user's Google Drive.** Following an **authoritative committed** eligible record, support a transparent export/projection into a readable Google Sheet that the user controls in their chosen Drive. Intended experience: simple ongoing refresh toward near-live visibility, clear export state/last synced time and source record linkage. Exact synchronization timing, setup/consent, Drive ownership, Google API/Apps Script/OAuth approach and data layout must be proven before promised as working.
4. **True independent freedom:** User may view, copy, download, share/attach to another AI, edit or delete the Sheet. Kerani cannot prohibit normal user control of that copy, lock users into its AI, automatically ingest a modified external Sheet as authoritative facts or erase original Core records merely because that Sheet is deleted.
5. **The user chooses any external AI.** Kerani generates/keeps an understandable user-controlled data copy; **user explicitly decides** whether to upload/share that Sheet elsewhere. Kerani does not forward confidential records to third-party models as an automatic default or claim outside tools are confidential/approved without provider-specific checking.
6. **Simple product, not weak data integrity.** Avoid unnecessary bespoke algorithms, complex rule trees, forced accounting schemas and oversized dashboard stacks. Mandatory tenant security, accurate record identities, scope, validation, export integrity and recovery are the *minimum safety core*; complexity cannot be removed by silently discarding them.

**Plain-language promise:** “Rekod dengan mudah. Data tetap milik anda. Lihat dan guna sendiri dalam Google Sheets, atau analisis menggunakan AI pilihan anda.”

## 2. Authoritative records vs editable Sheet vs internal read model

```text
  Free chat / structured input / attachments (supported)
                        |
         Tenant auth + minimum validation
                        |
                 CORE COMMIT
       immutable receipt / record id / version
                        |
               ONE SOURCE OF TRUTH
                  /             \
                 /               \
    Internal read model          USER-CONTROLLED EXPORT
  (D-065 RG-02 / RG-03)       Google Sheet in own Drive
   Free dashboard/AI              read / edit / delete
                                          |
                                attach/share manually
                                          |
                                     Other AI
```

| Component | Role | Can user edit/delete? | Does it change Core records? |
|---|---|---|---|
| Core authoritative records | Validated record, tenant ID, event/commit receipts and audit | Through separately authorized Kerani edit/delete workflows if offered | **Yes only via authorized Core operations** |
| Kerani internal indexed read model | Fast Free dashboard + tenant-scoped grounded AI summaries, derived/rebuildable from Core | Not directly authoritative | No; rebuildable |
| Google Sheet in user's own Drive | Derived portable editable/export copy | **Yes**, including delete/share/copy | **No automatic reverse sync or Core deletion** |
| External AI context | User-supplied data for independent tools | User decides what to attach | **No**, unless a future separate explicit import-proposal workflow is approved |

**Crucial conflict resolution:** “User can edit or delete Sheet” + “Kerani keeps it continuously fresh” cannot be implemented as a naive bidirectional overwrite. **LOCKED invariant:** user edits may not be silently overwritten by Kerani background refresh. The actual UX (new versioned snapshot; append-only generated tab with separate user-edit tab; explicit opt-in refresh; conflict detection/pause-and-review) is **OPEN / needs design and usability proof**. On file delete/revoke, respect user's intent: suspend that destination and notify through permitted UI; no silent recreation/reconnection without fresh user authorization. Retaining Core does **not** prevent the user from requesting a separately authorized Core deletion/export deletion later.

## 3. Directness and eventual consistency

**User says data “terus diekstrak”; locked intention is simple prompt availability of a trustworthy Sheet copy after Core commit.** Do not promise synchronous Google delivery or a fixed time from this decision alone.

- **Commit first:** only Core-confirmed entries become exports (or optionally visible clearly marked drafts if future explicit design).
- **Export status:** `QUEUED / SYNCING / EXPORTED / FAILED / DISCONNECTED` are *illustrative status names*, not locked schema. Show source revision, last successful export and Google destination identity to the authorized owner.
- **Reconcile/retry:** Google Drive outage, quota, duplicate webhook, concurrent writes, permission revocation and rate-limiting must never change Core's authoritative transaction result; use bounded retry with no duplicate rows or corrupted user edits.
- **Free dashboard separate:** D-065/L-051 RG-02 Free committed-data visibility is not allowed to become dependent on the user connecting Google Drive or leaving a Sheet undeleted. Kerani's internal Free dashboard/read model remains usable.
- **Incremental/projection scope:** must be tenant-specific and least-privilege. Filter sensitive columns and preserve record identifiers/time/range/data provenance. Do not export other businesses' data from shared multi-tenant accounts.
- **Non-tabular/large data:** Sheet may contain safe summaries, structured fields and links to separately authorized attachments; not every input can or should be coerced into a single cell. Partial/support status must be truthful.

## 4. Free/Premium, privacy and implementation boundaries

- **LOCKED product principle:** an adequate **Free user-controlled export/portability path** for their own supported basic records; not a Premium hostage. Specific automatic Google Drive sync costs/quotas and optional hosted extras remain separately tested product/commercial decisions.
- **Not forced Google connection:** user may decline Google permissions; a usable Free record/retrieval/dashboard and portable download/export alternative must remain available, subject to approved minimum export design. Real Google Sheets-in-own-Drive creation needs appropriate user permissions and auth/integration, not assumptions about existing app access.
- **External sharing:** when users copy/share a Sheet with another AI, that service may receive the data; disclose risks and let users select content. Kerani does not certify other providers' retention, training or confidentiality.
- **Tenant/auth:** Google file permission is separate from a Kerani Business ID; OAuth tokens/scopes, destination ownership, edits conflict and revoke flows remain unselected. Do not store credentials in GitHub or Linear.
- **Legal/delete:** deleting an exported file must not silently purge Core, and conversely a separately approved Core deletion/privacy request must have a designed downstream exported-copy handling policy so revoked users' privacy rights aren't ignored.
- **Rate/scale:** Google Sheet, Apps Script and APIs have size/throughput limits; “any data” means supported input with explicit limits, no unbounded Free storage or guarantee every file is transformed to cells.

## 5. Lineage / reconciled decisions

- **D-018** data portability/no lock-in: strengthened as first-class, user-controlled Sheet/export rather than a slogan.
- **D-016/L-011, D-055/L-046** genuinely useful no-AI Free records, reports and independent ownership continue.
- **D-023** durable tenant identity/authorization independent of channel and Sheet file IDs.
- **D-053/L-044** Google user-owned storage needs consent and evidence; this product LOCK **does not silently approve new OAuth scopes**.
- **D-060 CANDIDATE** optional customer-controlled Drive and modular cloud economics: user-owned Google Sheet output is now owner-LOCKED as a **product data-portability principle**; exact technology/plan/free automatic-sync economics remain OPEN; tenant-owned document storage as general hot database remains rejected assumption.
- **D-057/L-047, D-061/L-049** Free first-class Mini App/dashboard plus Chat-First; Sheet is an additional portable surface, **not** substitute for product-visible records.
- **D-065/L-051** RG-01 version upgrade and mock isolation, RG-02 committed Free visibility with freshness and RG-03 bounded grounded internal AI read model remain authoritative. **External Sheet is not RG-03's trusted knowledge source by default**, because it can be edited externally.
- **D-064/L-050** WhatsApp queue-ready V1/V2 unchanged; webhook ACK/Queue admission is not Core COMMIT or successful Sheet export.
- **D-059 CANDIDATE** premium advanced dashboard remains candidate; user freedom and basic Free exports are not a paid-only analytics feature.
- **D-062 CANDIDATE** RekodUntung.ai brand unchanged.

## 6. Suggested future design/acceptance (NOT RUN)

| Case | Synthetic proof needed |
|---|---|
| P01 | Generic text/operation report with unfamiliar fields is captured without silent loss; unsupported data is clearly flagged; domain validation still holds. |
| P02 | Core COMMITTED record projects into only the correctly authorized user's Drive Sheet, record IDs and source timestamps match and are visible. |
| P03 | Same event redelivered, Google export retries or Google errors: one logical Core record, no duplicate Sheet rows, clear SYNC status. |
| P04 | User edits or deletes exported Sheet: no silent overwrite/recreate and Core record unchanged; explicit permission reconciliation. |
| P05 | User attaches/downloads a Sheet to independently chosen AI: app does not secretly transfer records; sensitive-field sharing warnings where needed. |
| P06 | No Google account permission/Drive revoked: Free chat, dashboard, basic report and an alternative portable export path remain usable. |
| P07 | Export is stale, failed or partially updated: customer sees accurate source watermark, can recover and can still query internal read model. |
| P08 | Two businesses, sharing mistakes, external link disclosure: no unauthorized cross-tenant data export or file link leakage. |
| P09 | Core privacy deletion/export expiry: policy for previously exported user-controlled copies is explicit; no false guarantee of deleting third-party copies. |

**All P01–P09: NOT EXECUTED.** No code/Google Drive OAuth, file creation, new cloud resources, live tenant data or automated export is authorized in this commit.

## 7. One NEXT

**D-066 — User-Owned Sheets Export Contract (READ-ONLY DESIGN):** specify minimum captured-record envelope, Source-of-Truth/export one-way API, edit/delete/refresh conflict handling, Google authentication and non-Google fallback, privacy and supported Free capacity. Submit for review before implementation or provider connection.
