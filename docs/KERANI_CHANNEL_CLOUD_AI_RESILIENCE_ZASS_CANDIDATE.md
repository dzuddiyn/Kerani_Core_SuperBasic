# Kerani AI — Channel Credits, Cloud Ownership, AI Privacy & Concurrency
## ZASS Discussion Reconciliation — 2026-10-22

**Classification:** **ZASS REVIEWED — CANDIDATE / DESIGN CHALLENGE INPUT ONLY**  
**Decision ID:** D-060 (CANDIDATE, **not** a LOCKED architectural or commercial decision)  
**Linear:** [KAI-8](https://linear.app/dzuddiyn/issue/KAI-8/zass-channel-credits-cloud-ownership-and-ai-scale-candidate) (BACKLOG)  
**Authoritative project:** `dzuddiyn/Kerani_Core_SuperBasic`; `ZASS_Kerani_Core_SuperBasic.md`.  
**Discussion source:** owner Kerani AI planning conversation on 2026-10-22, building on earlier D-016–D-059 product decisions.  
**Excluded from this artifact:** Claude/agent industry announcements; competitor landscape, **Krani.ai**, brand naming and trademark comparisons. Those belong in a separate discussion/decision if requested.

> **Owner direction:** Kerani backend remains the centre; optionally connect a customer's own Google Drive, make WhatsApp cost-reflective after a small onboarding free credit, prefer economical Telegram, charge for additional hosted cloud, offer an explicit choice of AI processing tiers, and ensure database/API service does not jam with concurrent users.
>
> **ZASS guardrail:** User proposals and assistant analyses are not evidence of costs, provider policy, legal compliance, throughput or customer willingness to pay. **This note authorises documentation only**, not an architectural LOCK, production deployment or price activation.

## 1. DUMP — Raw demands preserved (not automatically adopted)

| Raw proposal / concern | Source meaning | Status after review |
|---|---|---|
| One Kerani backend | Keep tenant, business logic and validation centralized even when customers use another storage or AI service | Aligned with LOCKED D-023/D-030/D-057; implementation **OPEN** |
| Customer Google Drive | Allow customers to use their own Drive; reduce Kerani's hosted file cost while retaining core backend | **CANDIDATE**; scope/permission/latency and API failure behaviour untested |
| WhatsApp bonus only at onboarding | Give small initial trial credits; subsequent WhatsApp message transport requires credit priced to true cost; Telegram should be cheaper | **CANDIDATE commercial change**; conflicts with possible interpretation of D-025 continuing Free shared WhatsApp allowances; no silent supersession |
| Cloud trial only then pay | Customer pays for substantial Kerani-hosted storage if not using own Drive | **CHALLENGED** by LOCKED D-016/D-020/D-024/D-055 and portability. Minimum durable Free record/storage must remain usable |
| AI Free / Paid choice | Low-cost AI with transparent conditions vs paid processing with stronger specified data controls and better capacity | **CANDIDATE**; provider-specific policies, legal/data categories and exact premium protections require evidence |
| High concurrency | Database and AI API must remain responsive; large bursts must not lose/duplicate business records or create unbounded cost | Existing risk Q-016/Q-036/R-013/R-026/R-035 etc; **CANDIDATE control design** pending E-016/E-018 proof |
| Keep user interface easy | Do not turn choices into complicated onboarding or forced bundles | Reinforces LOCKED D-054; simple defaults and transparent later upgrade choices |

## 2. DISTILL — Product principle and boundaries

**Candidate product thesis:** `One Kerani Backend + User-Chosen Channels + Portable Files + Transparent Usage Entitlements + Trustworthy Bounded AI`.

Five independent commercial/control dimensions, not five separate apps:
1. **Channel transport:** WhatsApp message economics vs Telegram transport; credentials/tenant identity separate from message delivery.
2. **Core data vs attachments:** authoritative live operational transactional records plus indexed metadata remain consistently controlled by Kerani Core; attachments, receipt images, documents, export/backup may use tenant-authorised storage with a Drive adapter. Data ownership and export rights preserved. **Drive alone is not assumed to be an OLTP database.**
3. **Hosted storage capacity:** a durable, genuinely useful Free baseline vs paid larger data/media retention/backup and related support; never suddenly lock users out of their own records at trial expiry.
4. **AI processing tier:** deterministic/no-AI baseline always available; limited AI routes only where provider terms and data classifications permit; paid AI routes with separately verifiable contractual data controls and costs.
5. **Premium capabilities:** forecast, richer dashboard/analysis, automation and domain workflows are still separate D-050/D-051/D-059 candidates, not automatically bundled or LOCKED via a cloud-credit decision.

**Metering:** internal ledger should distinguish transport, storage/media, AI processing, query/report capacity and premium credits. A unified wallet UX may exist but must present a truthful, legible price before charged actions; infrastructure costs do not imply charging for a failed/undelivered action (D-017).

## 3. DECIDE — Candidate outcomes, conflicts, and stop rules

### Direction A — WhatsApp onboarding credit, then metered transport
- **Proposed:** One-time bounded welcome allowance on shared WhatsApp; after exhaustion users purchase transport credits or move to Telegram; Telegram has lower channel overhead where provider terms permit.
- **Keep distinct:** A premium AI action costs the same capability credits regardless of channel under LOCKED D-025; transport surcharge is separately attributable to channel.
- **Conflict gate:** D-025 currently LOCKS shared WhatsApp as a controlled Free discovery channel, with top-up/migration choices. An onboarding-only allowance *could* be one implementation of a finite Free allowance; however an unconditional ban on any future Free WhatsApp allocation would be a commercial policy change and **requires specific owner supersession approval**.
- **Open:** Official Meta and any BSP billing/pricing, effective dates, category/service message fees, Malaysia/recipient market rules, currency, per-number usage pooling, customer price/markup, attribution, provider contract and abuse controls. **No current numeric costs verified in this document.**

### Direction B — Optional customer-owned Google Drive, Kerani backend stays
- **Proposed:** Minimum customer-approved `drive.file`-type limited access, or simple user-supplied document links first; optional customer-owned Drive for receipts, photos, documents, exports and backups.
- **Core boundary:** Transactions, tenant identity, permissions, audited mutations, idempotency keys, authoritative task state and hot query indexes remain with the selected Kerani business storage contract. Exactly which attachments/metadata are owned where is **OPEN**; no accidental dual Source of Truth.
- **Edge cases to prove:** consent/revocation, token refresh and encrypted token handling, orphaned files, Drive/API 429/403, customer storage exhausted, inaccessible Drive, customer deleting/modifying file, account disconnect, offline provider, backup/restore and migrating from Kerani Cloud to Drive/back.
- **Privacy:** Access only tenant-authorised folders/files and scope; don't request access to the user's entire Drive by default. OAuth and customer data access are **NOT AUTHORISED now**.
- **Conflict gate:** D-024 first record without creating a Drive account/layout; D-053 Drive OAuth is a hypothesis; D-030 channel-independent tenant storage remains LOCKED.

### Direction C — Free durable baseline and paid hosted cloud growth
- **Reject for now:** A model where all cloud storage is merely a time-limited onboarding sample and a nonpaying user then cannot record, retrieve or export their own data.
- **Aligned candidate:** Permanent small but practical quota for core records and basic operations; optional paid media/storage expansion, backup/retention, higher service capacity, and optional customer-owned Drive for supported files.
- **Pricing and enforcement OPEN:** evidence-based storage quantity, retention period, paid tiers, what happens at quota ceiling (controlled reject or archive policy), export continuity, late billing/cancellation and non-destructive migration. No arbitrary deletion on trial expiry.

### Direction D — AI Free policy vs paid processing
- **Minimum:** Deterministic/no-AI business paths always work (D-055); model failure cannot make records unavailable or automatically authorize writes.
- **Proposed Free AI:** Only route data after verifying *that provider, API endpoint, tier, processing terms, region and data category* permit the content, with transparent consent where valid. **User consent to model training or data retention cannot override a provider's prohibition on uploading confidential/personal/sensitive data, nor statutory privacy requirements.** Redact/minimise by default where useful.
- **Proposed Paid AI:** Offer explicitly defined processing protections, contract/data training use conditions, limits, performance priority and cost; don't claim all paid providers guarantee zero retention, no training, regional residency or uptime. Separate capability cost from WhatsApp transport cost.
- **Fallback:** Free API/paid API are **not interchangeable** for a customer's confidential records. Permitted-provider allowlist, data-classification policy, per-tenant privacy selection and explicit fail-closed route; if no compliant AI route available, offer deterministic forms/history and honest `AI UNAVAILABLE` rather than violating the policy.
- **Provider comparison, current ToS, training and retention conditions:** OPEN and date-sensitive; require live official evidence before LOCK. No provider named/selected.

### Direction E — Concurrent database/API resilience
- **Goal:** Many tenants can read/write independently; a slow provider, one heavy tenant or a failed queue worker cannot stop the whole service, falsely mark a write saved or create unlimited cost.
- **Candidate request classes:**
  - `FAST READ`: authorised simple record/status/basic report queries bypass AI and unnecessary queueing when safe; indexed/paginated storage queries, bounded caching and limits.
  - `CONTROLLED MUTATION`: state-changing operations use validation, human confirmation if required, idempotency key, transaction/consistency contract, durable receipt/admission control where evidence justifies it; do not assume *all* writes must traverse one universal queue.
  - `AI INTERACTIVE`: bounded concurrency/token budget/provider access, per-tenant and global fairness, timeouts/deadlines, appropriate retry-after/backoff/jitter/circuit-breaker semantics, policy-compliant limited fallback.
  - `BACKGROUND`: OCR, forecasts, bulk exports, scheduled reports and noncritical jobs get bounded queues and lower priority, without starving Core.
- **Controlled saturation:** bounded queue depth, traffic shedding/backpressure, `ACCEPTED/PENDING/COMMITTED/FAILED` semantics for supported paths; only assert SAVE after authoritative commit/read-back or valid receipt. Persistence on backend restart and duplicate delivery depends on actual queue/database semantics and must be tested.
- **Testing/observability:** D-052 request-stage P50/P95/P99 for ingress, auth, DB read/write, queue wait, AI time, retry, delivery; rate/429/5xx/timeout; success vs error; lost/duplicate/cross-tenant record detection; per-tenant unit cost; backup/restore and failure recovery. Benchmark 10/50/100/500 simultaneous actors only as **synthetic test scenarios**, not capacity claims or default release targets.
- **Keep options OPEN:** Apps Script, Cloudflare Workers/D1, Cloud Run/Firestore, OCI or minimal VM remain challenge inputs (E-016); no Kubernetes/Redis/microservices/database/queue/provider LOCK.

## 4. ZASS OPTIONS — Explicit pros/cons / kill-critics

| Option | Pros | Cons / risk | Verdict |
|---|---|---|---|
| **A. All-inclusive monthly Premium** | Simple package and predictable UX | Cross-subsidizes high-cost WA/AI; conflicts with credit-first direction; user forced into bundle | **NOT SELECTED** |
| **B. Independent usage-led dimensions** | Transparent cost; users buy only WhatsApp transport, extra cloud, AI tier and high-value features needed | Wallet and quota UX can become complicated; many billing edge cases | **PREFERRED CANDIDATE**, validate user comprehension and revenue |
| **C. Customer Drive as full live database** | Perceived provider independence; potentially less hosted storage cost | Latency, API/quota, consistency, optimistic sync and identity complexity for concurrent business transactions | **REJECT as default assumption**, evidence required for any scoped exception |
| **D. Managed operational DB + optional tenant Drive attachment/export** | Responsive indexed records + portability for large objects | Kerani still pays minimal DB and backup; auth/reconciliation integration needs work | **PREFERRED CANDIDATE**, not tech selection |
| **E. Universal queue for all traffic** | Superficially simple routing story | High latency, head-of-line blocking, complex failures and retry amplification for simple reads | **REJECT as universal rule** (existing Q-016 open) |
| **F. Bounded fast-path + class-specific durability** | Preserves responsiveness under AI load and protects writes | Needs correct routing, consistency, fairness tests | **PREFERRED CANDIDATE**; benchmark required |
| **G. Send every Free user's real confidential data to any free AI API after checkbox consent** | Low marginal AI bill | May violate provider ToS/privacy law, harms trust; no privacy-preserving failover guarantee | **REJECT**; policy/data categorisation is mandatory |

## 5. DESIGN — Illustrative boundaries (NOT architecture)

~~~text
Telegram / WhatsApp / Future Web Dashboard
            |
        Kerani Entry
      tenant/role/auth
      quota/credit/consent
            |
      Classify Request
       /           \
 FAST DATA READ    BOUNDED ACTION
      |                 |
 Auth+index          state-changing? → confirm / validate / idempotency
      |                 |
  trusted DB      durable admission/queue ONLY where needed
      |                 |
      +----------> Core business commit/receipt <---------+
      |                                                    |
 optional authorised Drive attachment adapter       bounded AI Gateway
 (files/export/backup not hot OLTP)               model policy & budget
                                                   fail-closed/fallback
~~~

This is an **interaction/authority sketch**, not a selected implementation topology. The storage engine, gateway software, queue, cloud vendor, contracts, security review and credentials are NOT selected. A drawing is not evidence of real throughput or security.

## 6. DO IT? / DELIVERED! — Status and future proof gates

**This operation:** documentation/reconciliation only. No implementation authorisation, no secret/OAuth/token, production business write, customer payment, database creation, load test, AI API call or deployment.

**Challenge groups before decision LOCK:**
1. **COMMERCIAL:** Costed official WhatsApp/BSP transport versus Telegram at real request mix; first-value conversion after one-time welcome credit, per-channel surcharge, prepaid ledger and failed-transaction refund/charge semantics.
2. **STORAGE:** Free baseline survives bonus expiry; Drive link → scoped OAuth trial only with consent and real demand; data durability/restore/revoke, independent hot transactional records and export/recovery.
3. **AI POLICY:** Written dated model-specific Free/Paid API terms, confidential-data eligibility, redaction/security controls, notice/consent, fallback and clearly defined paid protections.
4. **CONCURRENCY / RESILIENCE:** E-016/E-018 synthetic multi-tenant traffic; steady/burst load, injected 429/502/timeouts, DB hotspot/contended-write tests, queue failure/replay, idempotency, TTL/retry fairness, cost caps and backup/restore.
5. **UX / VALID:** Pilot with small business users: simple default Telegram+permanent Free Core, explain transport/storage/AI upsell without violating D-054; measure useful completed actions and actual willingness to pay.

**Required evidence receipts:** real official provider policy and pricing citation with checked date; user-tested pricing comprehension; tenant-scoped unit costs; P50/P95/P99; completed useful workflows; exception/failure receipts; proof of zero undetected lost/duplicate authoritative writes under tested workload; full backup/restore and scoped permissions. Thresholds remain *to be defined from evidence*, not invented here.

**Explicit supersession gate:** Any proposal making *all* WhatsApp transport chargeable after onboarding must reconcile D-025, and any proposal eliminating the evergreen Free basic record/storage capability must be **rejected or expressly change D-016/D-020/D-024/D-055** with user approval. Do not modify those LOCKED decisions merely because this candidate has been saved.

**Owner review point / NEXT:** Decide which parts deserve commercial-policy proposals after challenge, separately from technical PRE-ARCH and load-test evidence. Keep everything else **CANDIDATE/OPEN**.

## 7. Traceability and boundaries

- **Aligned LOCKED:** D-016 (Free usefulness); D-017 (Credit Pass); D-018 (portability); D-020 (Free first); D-023 (tenant independent of channel); D-024 (onboarding without BYO creds); D-025–D-031 (channels/quotas/storage); D-052/053 (observability/delivery); D-054/055 (convenience/no-AI); D-057 (Free Mini App); D-058 (VALID first).
- **Candidate:** D-050/051 (Premium operations/intelligence), D-056 (AI-first UX trial), D-059 (Premium Business Workspace), **D-060 (this review)**.
- **Open challenge:** Q-015/Q-016/Q-018/Q-019/Q-020/Q-025/Q-028/Q-032/Q-033/Q-036/Q-037/Q-038; E-016 (infrastructure), E-018 (spike), D-019 price calibration and new questions logged in SoT.
- **Scope exclusion:** NO Claude industry news, NO other AI agents, NO brand/trademark/pioneer/competitor claims included.

**EVIDENCE STATUS:** This is a source-grounded ZASS design synthesis of user discussion plus existing project SoT. It is **not** a fresh legal review of privacy rules or official vendor pricing, and is **not** a stress-test receipt. All rates and provider terms require current external verification before any commercial implementation.
