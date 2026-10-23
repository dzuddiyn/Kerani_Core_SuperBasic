# Kerani AI — WhatsApp V1 → V2 Queue-Ready Migration Contract (D-064 / L-050)

**Status: OWNER LOCKED — CONDITIONAL PILOT ARCHITECTURE STRATEGY + COMPATIBILITY INVARIANTS ONLY**  
**Owner approval:** 2026-10-24 (“lock & commit; condong kepada A untuk pilot kecil, direka supaya serasi dengan B; jika Apps Script kerap timeout atau webhook ACK berisiko kehilangan kerja, terus pilih B sebelum penggunaan sebenar”).  
**Scope:** WhatsApp ingress/dispatch/reply integration for a *small pilot*, not the whole Kerani/Core control plane and not PRE-ARCH deployment selection.  
**GitHub source of truth:** `dzuddiyn/Kerani_Core_SuperBasic` `main`, canonical ZASS D-064/L-050.  
**Tracking:** Existing Linear KAI-8 (WhatsApp transport, channel credits and resiliency).  
**Approval bounds:** Documentation & LOCK of **decision strategy**; **NO execution**, secrets, provider calls, account provisioning, real customers, deployments, production sends, architecture benchmark PASS or product maturity upgrade.

## 1. Locked owner decision: prefer A, design for B

- **V1 / Option A (small pilot preferred):** `WhatsApp Cloud API → Cloudflare Worker (verified webhook/adapter, planned quota guard) → protected Google Apps Script processJob() → Worker-controlled outbound WhatsApp gate`. Prefer synchronous, minimal dependencies **only if evidence proves Meta webhook ACK, data consistency, retries and latency are safe**.
- **Queue-ready from Day 1:** V1 MUST send a stable, versioned **Job Envelope** through one dispatcher interface, enforce trusted identity and tenant authorization, persist **same-event idempotency** and real processing/commit receipts, and use **one shared outbound/quota path**. Apps Script's business logic MUST NOT couple to whether dispatcher uses direct HTTP or Queue.
- **V2 / Option B (safety fallback before live use):** `WhatsApp → same Worker webhook URL → durably accepted Cloudflare Queue → Queue consumer → the same protected Apps Script processJob() → same Worker-controlled outbound guard`.
- **Escalation gate:** If synthetic/pilot tests find repeated Apps Script timeout, webhook acknowledgment would precede durable acceptance, loss-of-message exposure, non-idempotent writes, or other **unacceptable reliability risk**, STOP V1 release and **choose/test Option B before exposing real users**. Do not claim specific numeric timeout count or automatic promotion threshold yet; define measurable go/no-go in CF-WA-QG-01B testing.
- **No reset/overhaul goal:** Existing Business ID/User ID, canonical record schema, job identifiers, chatbot endpoint, validation/authorization rules and customer data remain the same. Only the **transport/dispatch implementation** changes. Real migration is still a code/config rollout with queue consumer, state and recovery tests; it is **not literally zero changes**, and avoiding data reset requires proof of idempotency and state carryover.

This LOCK **supersedes only** D-063's undecided **V1-vs-V2 pilot preference** for this WhatsApp slice. D-063's proposed thresholds 950/990, D1 vs Durable Objects, exact quotas, commercial terms, provider choice and other candidate architecture choices remain **NOT LOCKED**. Existing LOCKED D-025/L-019 Free WhatsApp vs Telegram roles and D-027/L-021 channel meters remain authoritative. The generic E-016 whole control-plane challenge stays OPEN: this LOCK selects a *pilot sequencing strategy* only, NOT a production-wide hosting framework.

## 2. V1 / V2 boundary diagram

```text
                     SAME WHATSAPP NUMBER + SAME WEBHOOK URL
                                 │
                         META VERIFIED WEBHOOK
                                 │
                                 ▼
                       CLOUDFLARE WORKER
                   auth · routing · event ID
                                 │
                          dispatch(job)
                   ┌─────────────┴─────────────┐
                   │ V1: DIRECT mode           │ V2: QUEUE mode
                   ▼                           ▼
             protected HTTP             durable Queue send()
                   │                           │
                   │                    Queue consumer
                   │                           │
                   └─────────────┬─────────────┘
                                 ▼
                  SAME protected processJob()
                  Apps Script: validate/authorize
                   SAME authoritative Core SoT
                                 │
                                 ▼
                        outbound proposal
                                 │
                                 ▼
                SAME Worker outbound quota gate
                                 │
                                 ▼
                    WhatsApp Cloud Send API
```

**No Queue in V1 unless proof demands it.** Existing Apps Script `doPost` accepts webhook HTTP without a 60-second clock trigger. Cloudflare Cron is minute based and is not a fast response substitute; Queues/DO alarms are for asynchronous/delayed jobs when warranted. Worker can control HTTP status and Meta signature verification, but does **not** eliminate Apps Script latency/quotas by itself.

## 3. Stable Job Envelope — design contract vs example fields

**LOCKED invariant:** One **versioned, authenticated, transport-neutral job envelope**, created by the verified adapter, is the ONLY format passed to `processJob(job)` in V1/V2. Worker maps trusted WhatsApp sender/phone/event ID to authorized Kerani identities; payload-supplied tenant IDs are not authority.

Illustrative shape (**SCHEMA FIELD NAMES = DESIGN PROPOSAL, NOT SPEC-FINAL LOCK**):
```json
{
  "schema_version": "1.0",
  "job_id": "wa:<verified-phone-id>:<verified-meta-message-id>",
  "source": {
    "channel": "whatsapp",
    "phone_number_id": "<verified-phone-id>",
    "provider_message_id": "<verified-meta-message-id>"
  },
  "context": {
    "business_id": "<server-resolved-business-id>",
    "user_id": "<server-resolved-user-id>"
  },
  "intent": "PROCESS_MESSAGE",
  "payload": { "text": "Beli baja RM120" },
  "trace": { "received_at": "<ISO-8601>", "correlation_id": "<opaque-id>" }
}
```

**Privacy:** Fields above are synthetic; implementation minimizes PII in Queue, logs and retention, and preserves data-class-specific restrictions. Never expose secrets in repo/Linear. Server-to-server calls must authenticate the Worker and guard against replay (signed request/nonce/timestamp or equivalent), using an Apps Script-compatible verified pattern rather than assuming Apps Script has full inbound header control.

**Identity:** Stable `job_id` should derive from a verified Meta phone/event ID and event type as relevant, with channel namespace; exact canonicalization, collision/replay policy, retention and work-item semantics remain to be designed and tested. The caller cannot choose another tenant. No AI-based semantic merging of different worker reports in Free (D-061/L-049).

## 4. Dispatcher interface and statuses

**LOCKED invariant:** Both dispatch modes feed the same `processJob(envelope)` semantics; modes must not alter data rules or invent success. **Mode name/response envelope are DRAFT, not fixed API.**

```js
async function dispatch(job, runtime) {
  if (runtime.mode === "QUEUE") {
    await runtime.queue.send(job);           // durable admission, NOT business SAVE
    return { state: "ACCEPTED", job_id: job.job_id };
  }
  return await runtime.protectedAppsScript(job); // may return COMMITTED or PENDING/FAILED
}
```

Illustrative processing states:
- `RECEIVED` → `ACCEPTED` (durable ingress/queue for V2) → `PROCESSING` → `COMMITTED` / `REJECTED` / `FAILED_RETRYABLE` / `UNKNOWN`.
- Outbound statuses are **separate**: `NOT_SENT`, `RESERVED`, `SUBMITTED`, `DELIVERED`, `FAILED`, `UNKNOWN`.
- **Never equate** Meta webhook `HTTP 200`, Queue `send()` success, Apps Script HTTP success, Meta Send API accepted or outbound delivered with **authoritative business COMMITTED**.
- V1 acknowledgment may only be returned after demonstrably safe synchronous completion or durable intake; if provider callback SLA and durable requirements cannot both be met, **V1 fails release gate → V2**. If V1 cannot offer durable ACK and is unsafe, do not silently ACK and `waitUntil()` the critical save.
- A terminal result must be reconciled against the authoritative Core record SoT; a timeout leaves `UNKNOWN` until checked, not blindly sent again.

## 5. Idempotency, ordering and outbound budget

- **LOCKED:** Duplicate delivery of a single Meta event, retry of same Job Envelope and transitional dual-path replay **must not create two business records**. Protect at authoritative commit boundary, keyed by the trusted unique event/job identity. Distinct workers' independent reports remain distinct (no semantic Free dedup).
- **LOCKED:** All WhatsApp outbound sends follow one authenticated **quota/approval gate** and stable outbound attempt/idempotency semantics in V1 and V2; a successful business COMMIT with outbound delivery failure remains committed without an invented second SAVE.
- **NOT LOCKED:** Exact Meta free-capacity enforcement thresholds (950 warning/990 routine stop are still D-063 *candidates*), chosen D1 vs Durable Object reservation technology, tenant seat quotas, charged template rules and Meta/BSP reconciliation mathematics.
- **Queue ordering:** Cloudflare Queues is at-least-once, with no blanket order guarantee. Order-sensitive stock mutations require version/concurrency checks or ordering domain rules; do not assume Queue FIFO prevents conflicts.
- **Dead letters/recovery:** Consumer retries and DLQ/persistent audit trail must preserve status and avoid permanently dropping a valid record when Queue retention expires. A Queue is **not** long-term archive nor second business SoT.
- **External senders:** A bypass sender on the same WhatsApp number can cause charges without passing our gate; “zero charge guaranteed” is not an approved claim.

## 6. V1 → V2 controlled migration without reset

| Migration phase | Change | Expected invariant / proof |
|---|---|---|
| V1 pilot proof | Worker verifies Meta, maps tenant/job, protected `processJob`, idempotency + outbound guard; no queue | Stable job ID, same business SoT; compare direct handling latencies/ACK safety |
| V1.1 synthetic staging | Introduce Queue consumer using **same envelope** with only synthetic traffic | Consumer uses same `processJob`, proofs for retry/dup and replay |
| V1.2 canary | Enable dispatcher flag for selected synthetic/approved pilot traffic; never concurrently process both routes for one event | One owner of each job ID, documented route epoch/cutover, outbox/ledger reconciliation |
| V2 rollout | Move qualifying ingress to Queue **only after** durable ACK, authorization, replay safety, cost, latency and recovery tests pass | Same WhatsApp number/webhook/business IDs, no customer data reset, no dual writes |
| Rollback / incident | Stop enqueueing new jobs, drain/reconcile pending IDs, route only idempotently safe jobs back, preserve durable backlog | Do not drop queued jobs or re-commit existing records |

**No-overhaul preconditions:** source-truth storage is not changed, Apps Script has a stable processJob boundary, canonical IDs are durable, and queue envelope version is backward compatible. If these conditions are violated, migration can still require major work; never guarantee otherwise.

## 7. Mandatory gates before real users (all NOT RUN)

- **CF-WA-QG-01A / 01B — synthetic**: webhook GET verification; HMAC signature using actual raw body; request headers/status/redirect handling; Google Apps Script 302→`script.googleusercontent.com` and timeout; per-request P50/P95/P99; webhook ACK with/without durable receipt.
- **At-least-once/recovery:** duplicate Meta webhook, Apps Script timeout AFTER authoritative commit, ten concurrent send attempts around quota 989/990, cross-tenant denial, forged internal request, same-job dual path during canary, Queue retention/DLQ and unknown delivery reconciliation.
- **GO for V1 (pilot only):** all mandatory correctness/security/ACK and bounded-latency tests PASS with real evidence, including a documented timeout/error budget. No numerical values invented in this LOCK.
- **FAIL/ESCALATE V1 → B pre-release:** repeated timeouts, inability to provide safe ACK before Meta retry deadline, lost events, idempotency failure or insufficient retry/durability evidence. **Stop V1 live rollout**, test Queue alternative and only deploy with separate owner release approval.
- **STOP all release:** missing trustworthy tenant authentication, false SAVE receipts, business double commits or unbounded charge risk; do not treat merely adding a Queue as an automatic PASS.
- **D-063 synthetic CF-WA-QG-01 T01–T08** remains NOT RUN. No fixtures/tests/provisioning in this documentation commit.

## 8. Compatibility & scope matrix

| Concern | This LOCK | Not selected |
|---|---|---|
| V1 small-pilot preference | **Worker + Apps Script, Queue-ready** conditional on proof | Immediate live deployment |
| V2 escape path | **Add Queue/consumer without changing business contract, before live if V1 unsafe** | Mandatory Queue from day 1 without evidence |
| Core authoritativeness | **Single business source of truth + versioned envelope + idempotent commit** | New authoritative business DB in Queue/D1 |
| Edge quota guard | **Same outbound-gateway invariant across V1/V2** | Fixed 950/990 threshold or legal/billing guarantee |
| Larger platform | **Only WhatsApp slice sequence LOCKED** | Global E-016 PRE-ARCH or hosting decision |
| Brand/product name | Kerani AI remains; D-062 RekodUntung candidate | Brand rename or domain purchase |

**NEXT — exactly one:** **CF-WA-QG-01B — Queue-Ready Contract & Synthetic Reliability Challenge (READ-ONLY design first)**. Formalize envelope/auth/idempotency/dispatcher test matrix and synthetic gates; request separate owner authorization before executing tests, provisioning Cloudflare or modifying Apps Script.
