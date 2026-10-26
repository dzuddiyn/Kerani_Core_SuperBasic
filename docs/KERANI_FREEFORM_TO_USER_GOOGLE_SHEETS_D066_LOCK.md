# Kerani AI — Freeform Data → Google Sheets Export That Users Control

**ZASS D-066 / L-052 — OWNER LOCKED PRODUCT PRINCIPLE, 2026-10-26**  
**User directive:** "bagi memudahkan software, tiada logic algorithm rumit. user boleh masukkan apa saja data, data akan terus diekstrak daripada database ke dalam sheet yang boleh diakses dalam Google drive. pengguna bebas lampirkan sheet tersebut untuk dianalisis oleh AI lain atau edit sendiri atau padam. ini idea utama. lock"

**Scope:** A central product/user-ownership principle, not selected database/Google OAuth implementation, not a promise that unrestricted binary uploads or sensitive third-party data are acceptable, and not actual Drive permission to act. **Linear:** KAI-13.  
**State:** Documentation/decision only, implementation and all acceptance tests **NOT RUN**.

## 1. Owner intent: software small, useful, portable

1. **Input broadly, with minimum friction.** Users can enter their own business notes, transactions, observations, quantities, free text and other useful record content. Keep the **raw original input** plus minimal metadata (`record_id`, verified tenant/user, time, source, status), before any optional business classification; do not demand complex domain algorithms for everyday capture.
2. **Database → Google Sheet automatically.** Authoritative Kerani Core stores accepted/committed records; a **rebuildable, exported table/projection** can then be created/updated in a Google Sheet accessible from the user's authorised Google Drive. Show actual sync status, source version/watermark, errors and last-updated time. **The direct export should be nearly live where feasible**, not assume 100% real-time or guarantee a fixed latency before measurement.
3. **Real user ownership.** A user can download, copy, attach, edit, share or delete **their Google Sheet file** on their own terms, or open it in other AI tools for their own analysis. Free baseline portability must not be held hostage to Kerani Premium or special Kerani AI reasoning.
4. **Don't build an accounting engine to merely hold notes.** Keep only indispensable validation, security, permissions, reliable commit, audit/idempotency and truthful data export. Optional AI classification or structured extraction must be correctable, never turn ambiguous free text into invented numbers or irreversible business actions.
5. **Single-authority clarity.** The **Google Sheet is an export/projection, not Kerani's authoritative mutable database**; its deletion or modification must not silently erase/modify accepted Core records, and deleting a Core record must follow separate deliberate authenticated Core data-rights workflow.

**LOCK level:** value/behavior/ownership principle, **NOT** exact API protocol, spreadsheet layout, Google Drive storage location, webhook mode, provider quota, cost, rich dashboard selection or release dates.

## 2. Simple intended journey

```text
User: "Hari ini terima tempahan roti 20 kotak, catat ya."
             │
             ▼
Kerani minimal trusted intake:
  verified Business ID/User ID
  preserve raw message, minimal fields + status
  confirmation/validation where required
             │
             ▼
AUTHORITATIVE COMMIT (Kerani Core)
             │
             ├─ Free basic recent-record view / read model (D-065 RG-02/RG-03)
             │
             └─ export/sync job (retriable, idempotent)
                           │
                           ▼
              Google Sheet in consented Drive
              rows + original text + date/status
              source ID + export watermark
                           │
            ┌──────────────┴──────────────────┐
            ▼                                 ▼
      User reads/copies                 User attaches Sheet
      edits or deletes                  to external AI tool
```

**Critical warning:** Some external AI services may retain/train on uploaded data or disallow particular confidential/personal data under their terms. Kerani must not automatically transmit the user's content to external AI or claim that user consent overrides third-party rules; transferring the Sheet is a user-chosen separate action.

## 3. The manual-edit vs automatic-refresh conflict (explicitly OPEN)

This is the most important design question. The owner wants both **automatic updates to a Sheet** and **freedom to edit/delete that Sheet**. Those behaviours collide if Kerani automatically rewrites user-edited cells.

**LOCKED invariant:** No silent overwrite of user-made changes; no silent recreation after deliberate file deletion; no silent two-way sync from Sheet edits into Core. **The exact conflict model is NOT chosen.** Two feasible designs for later testing:

| Design candidate | User freedom | Sync behaviour | Risk |
|---|---|---|---|
| **M1 Managed export + detachable personal copy (simple preferred hypothesis)** | User may copy/detach/edit/delete their copy and may revoke/delete managed export; copies are 100% under user control | Managed Sheet is a renewable data projection; personal copy no longer auto-updates unless opted into proven policy | User may not realise copy stops live updates; must explain |
| **M2 One user-editable live Sheet with clearly reserved generated range** | User edits their own columns and/or copies, or intentionally stops sync; delete anytime | Kerani updates only protected/disjoint generated range with proven conflict detection | More complexity; potential permissions/conflicts and accidental overwrites |

**NO DEFAULT CHOICE LOCKED.** Design should preserve user agency rather than sneak in an unwanted sync workflow. For user-requested deletion of the export, mark connection/deletion/re-auth as `DISCONNECTED` or `EXPORT REMOVED`, not a failure of authoritative Core nor permission to recreate file.

## 4. Compatibility with prior Kerani LOCKs

- **D-018 data portability:** directly strengthened. Users can independently inspect and analyse their own exported data; this does not remove Kerani's value for safe intake.
- **D-016/D-055:** no-AI Free baseline remains useful; simple entry/history/export must not require paid inference to work.
- **D-015/D-061:** freeform entry does **not** bypass tenant auth, minimum validation/confirmation for authoritative record types or technical dedup/idempotency. A vague note can be stored faithfully as a note/draft without pretending a completed Sale/Inventory mutation.
- **D-023 tenant identity:** each export must be scoped to the verified business membership; no guessing permissions from sheet URL or supplied IDs.
- **D-060 optional user-owned Drive CANDIDATE:** this D-066 **LOCKS the customer-facing output/ownership principle only**; whether and how to obtain OAuth, pay for storage or use Drive as receipts store remains candidate/unknown. It does **not** turn Drive into transactional Kerani DB.
- **D-065/L-051 RG-01:** generated sheets, mock rows, required settings, user files and actual Core records remain cleanly separated across environments/releases.
- **D-065/L-051 RG-02:** a Google Sheet export **can complement** the basic Free visible-value dashboard, but it is **not automatically a substitute for a usable mobile Free summary**. Sheet export and UI must both be honest about lag and authoritative record status.
- **D-065/L-051 RG-03:** the export is an external, user-facing representation of a safe bounded read model; it does **not** license unrestricted AI full-tab scraping as the internal grounded query architecture. Do not create a second mutable business SoT.
- **D-057/L-047 Mini App** remains the first-class default deterministic Free UI; exact export-link placement is design-open.
- **D-064/L-050 WhatsApp Queue-ready strategy:** direct vs queued transport does not affect Core-owned authoritative records or ability to sync Google Sheet after COMMIT.
- **D-059 Premium Workspace:** deeper interactive analytics, forecasts and automation remain separate candidate paid conveniences; no artificial paywall for basic export.
- **D-062 RekodUntung.ai** remains unverified brand candidate. No rename.

## 5. Minimum data/export contract — PROPOSAL, NOT IMPLEMENTED

Recommended fields for the earliest synthetic test only:
- `record_id`, `business_id` (or safe tenant reference), `created_at`, `source_channel`, `raw_text`, `record_type` (may be `note`/`unclassified`), `processing_status`, `source_revision`, `last_exported_at`.
- `raw_text` remains untouched by guesses; optional extracted columns include `confidence`/human-correction status; never overwrite raw evidence.
- Stable record ID and revision permit replay-safe append/update **only after committed acceptance**. Expiring/revoked Drive access produces traceable `EXPORT_PENDING`/`DISCONNECTED` not lost authoritative data.
- No public sharing by default. **A user choosing to share the Sheet with external AI/others is distinct from the Kerani app automatically uploading private business information to third parties.**
- Structured data CSV/XLSX downloadable fallback should be examined if consented Google Drive connection fails; exact availability remains design-open, but portability principle is locked.

## 6. Pre-release / synthetic acceptance evidence (NOT RUN)

| Test | Synthetic fixture | Must show |
|---|---|---|
| S01 | Free text with unknown schema | Authenticated raw business note stored exactly with minimal metadata, no forced false classifications |
| S02 | Plain Purchase/Sale entry + optional correction | Core validation where needed, true COMMIT, no duplicate row, no hallucinated amounts |
| S03 | Commit → Google Sheet export | Correct tenant-owned intended rows, IDs/provenance and recent watermark, with measured lag and permission |
| S04 | Repeated sync, timeout, revoke/expired OAuth | Idempotent incremental/rebuild/failed export state without corrupting or deleting Core records |
| S05 | User edits generated cell/adds note then next sync | **No silent overwrite**; chosen managed-vs-detached conflict UX is explicit and tested |
| S06 | User deletes exported Sheet | No silent recreation, no loss of Core records; truthful disconnected/reconnect path |
| S07 | User uploads a Sheet to other AI manually | Export stands alone with understandable headers, user control, no automatic transmission by Kerani |
| S08 | Cross-tenant actor obtains a Sheet URL but not permission | No unauthorized read/sharing or later cross-tenant data leak |
| S09 | OpsMate-style mock purge + version upgrade | RG-01/02/03 invariants preserved; export fully rebuildable from Core without fixture dependency |
| S10 | Drive/Sheets API cost/quota/timeouts + mobile usage | No implied infinite storage/real-time SLA; user sees status and safe fallback |

**Release STOP:** silent user-edit loss on refresh, public/shareable-by-anyone by default, unauthorized Drive creation or OAuth, user file deletion inadvertently deleting Core, freeform note falsely converted into accounting mutation, wrong tenant export, or export status falsely showing SAVED.

## 7. Governance

**Saved/LOCKED principle:** Allow broad user input → preserve and own committed Core record → convenient Google Sheet export/projection accessible in authorized user Drive → freedom to share/attach to other AI, edit, copy, delete independently. **Minimal logic, reliable records and transparent ownership** are the strategic product distinction.

**NOT LOCKED/NOT DONE:** actual Google Drive/Sheets integration, how file ownership is implemented, Drive OAuth scopes, paid API/data processing, export automatic interval, schema mapping beyond proposed minimal record metadata, permissions UX, automatic conflict detection, selected managed/personal-copy mode, Google API quota/costs, tests or deployment.

**NEXT — exactly one:** **D-066 Sheet Sync & User Edit/Delete Conflict Contract (READ-ONLY)** — prove whether managed export + detachable copy or restricted generated-range is simpler, and define safe auth, no-overwrite, refresh latency and rebuild/error semantics before implementation.
