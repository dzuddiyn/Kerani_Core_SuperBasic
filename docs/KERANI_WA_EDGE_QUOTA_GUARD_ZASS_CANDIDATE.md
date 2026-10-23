# Kerani AI — WhatsApp Edge Quota Guard & Fast Scheduler

**ZASS:** D-063 — **CANDIDATE / PREVIEW SAVED, NOT LOCKED**  
**Captured:** 2026-10-24, user-approved **documentation-only** SAVE and COMMIT  
**Tracker:** Linear KAI-8 (existing channel credits, AI scale and resilience concept)  
**Scope:** WhatsApp Business Platform inbound/outbound quota guard and timely event-driven work, while Google Apps Script may remain the early Kerani business backend. This is **NOT** a selected PRE-ARCH, implementation, pricing/entitlement change, working prototype, or deployment.

## 1. User DUMP, desired business outcome

- **Idea A:** place an inexpensive Cloudflare Worker as an adapter between WhatsApp Cloud API and Google Apps Script to intercept messages before the backend and prevent accidental paid service-message sends when nearing a monthly free allocation of **1,000 per WhatsApp business phone number**.
- **Suggested thresholds:** at **95% (950)** provide warning / conservation; at **99% (990)** stop routine outbound service messages and retain a **10-message safety buffer** for separately approved purposes. The exact meter, buffer use, warning UX and entitlement details remain **CANDIDATE**.
- **Idea B:** Cloudflare Worker plus a Cloudflare “scheduler” to avoid Apps Script's 60-second minimum **time-driven trigger polling** and improve chatbot response/async retry. Distinguish event-driven webhook arrival from scheduling delayed work.
- **Cost rule:** Free must stay genuinely useful; avoid introducing heavyweight cloud infrastructure merely for a small monthly traffic allowance. Telegram remains the economic/high-usage Free route (D-025/L-019 LOCKED). Do not silently replace that policy.
- **Primary preservation:** No bot/WhatsApp credential, real message, Cloudflare account change, Apps Script code, API deployment, paid setup, real data, or AI call is authorised by this documentation capture.

## 2. VERIFIED public platform facts (as of 2026-10-24; subject to future changes)

| Platform fact | Evidence | Meaning |
|---|---|---|
| **Meta WhatsApp Business Platform**: effective **2026-10-01**, each business phone number gets the first **1,000 service messages/month free**; charging starts at the 1,001st. This is **not 1,000 incoming + outgoing messages**; non-template service reply is one category, other template categories can incur charges separately. | Official WhatsApp Business FAQ: https://whatsappbusiness.com/resources/faq/ | Budget guard should meter **outbound service delivery**, not webhook events or all messages; reconcile Meta actual delivery/billing. |
| **Google Apps Script** installable time-driven trigger minimum is **every 1 minute**; its web-app `doPost(e)` responds to external HTTP POST without polling. | Google: https://developers.google.com/apps-script/guides/triggers/installable and https://developers.google.com/apps-script/guides/triggers | The 60-second limitation is for the selected **polling architecture**, not for all Apps Script work. |
| **Cloudflare Cron Triggers** use a 5-field minute-resolution cron syntax, minimum typical `* * * * *` every minute. | https://developers.cloudflare.com/workers/configuration/cron-triggers/ | Cron is not the correct instrument for guaranteed sub-minute dispatch. |
| **Cloudflare Queues** is event-driven; `max_batch_timeout` defaults 5 s, minimum 0 s; retries/delays supported, no guaranteed exact wall-clock response-time SLA. | https://developers.cloudflare.com/queues/configuration/batching-retries/ | Candidate for durable background work; compare fast path first. |
| **Cloudflare Durable Object Alarms** can schedule sub-minute future wake-ups, at-least-once delivery, retries; only one active alarm per Durable Object and timing is not a hard SLA. | https://developers.cloudflare.com/durable-objects/api/alarms/ | Candidate for scoped delayed retry and timers, not for replacing direct webhook responses. |
| **Cloudflare Workers Free** docs list 100,000 requests/day and 10 ms CPU per invocation; Free Queues offers 10,000 queue operations/day with a 24 h retention cap; D1/DO quotas and service costs require measurement. | https://developers.cloudflare.com/workers/platform/limits/ and https://developers.cloudflare.com/changelog/post/2026-02-04-queues-free-plan/ | A small proof is plausible, but no cost-free production guarantee. |

**Explicit non-verified assumptions:** Meta's specific per-market rates, BSP markup, current *account*-level delivery/billing reconciliation and reset-time, counter atomicity under load, use of D1 vs Durable Objects for global quota enforcement, Apps Script webhook latency, actual WhatsApp retry behaviour, and reliable under-60-s end-to-end completion are **NOT TESTED** here.

## 3. ZASS DISTILL — two separate problems

**Problem 1: Channel spend / entitlement leakage.** A pooled WhatsApp number may serve many tenants. Outbound billable class matters; incoming webhooks are not charge units. The guard may provisionally reserve capacity before outbound messages and reconcile *accepted/delivered/failed/unknown* status. Provider billing and status can lag, so an internal counter is **not** the definitive Meta bill. Another sender/BSP operating on the same number can bypass this Worker: no zero-charge guarantee unless all outbound paths are governed, provider-account access is controlled, and metrics reconciled. Template sending must have a separate classification and permission/charging rule, not share the service-message allowance automatically.

**Problem 2: Fast wake-up / worker polling latency.** A webhook delivered to an HTTP Worker can invoke a backend immediately. Apps Script `doPost()` can also be invoked directly via webhook, so Worker is **not necessary purely to bypass the 1-minute clock trigger**. Workers add practical value as a shared verification/quota/routing/quick-ACK layer. For asynchronous work, `waitUntil()` only extends work briefly and is **not reliable durable storage**; use an acknowledged persisted job / queue when record truth must survive crashes. Cron should be reserved for scheduled reconciliation/housekeeping. DO Alarms and Queue consumer delays can be fine-grained but timing is best-effort, not deterministic delivery under a certain number of seconds.

## 4. Candidate end-to-end flow — no selected topology

```text
Customer WhatsApp message
  -> Meta webhook
  -> CF Worker: verify Meta signature, message ID, trusted phone/tenant routing, basic abuse limits
      -> option A: direct protected Apps Script doPost on fast path
      -> option B: persist inbound event + enqueue, then ACK webhook
           -> Queue consumer -> protected Apps Script doPost
  -> Apps Script: tenant authorization, candidate/validation/confirmation, authoritative write/READ
  -> proposed reply -> CF outbound guard
      -> atomic quota reservation by WhatsApp phone number and billing period
      -> classify service vs template; enforce 95% warning/99% normal stop
      -> WhatsApp Cloud Send API -> delivery status reconciliation and truthful user/record receipt

Retry at 5–30s ONLY where justified:
  Queue retry/delay or scoped Durable Object Alarm
Housekeeping:
  Cloudflare Cron (minute-level) for reconciliation; never rely on Cron alone for monthly reset
```

**Security rules:** Do not expose a direct unguarded Apps Script write/send endpoint. Worker→Apps Script calls need authenticated, expiring, replay-resistant envelopes or equivalent server-to-server trust; Apps Script must enforce actual tenant/resource authorization. Verify Meta webhook authenticity and per-event idempotency. Tokens/secrets kept out of GitHub/Linear; don't send business data to AI provider without allowed data-processing basis. Do not claim `200 OK` to Meta is an authoritative business SAVE receipt: ACK ingress only after durable acceptance, or finish verified synchronous work first.

## 5. 95% / 99% quota candidate: policy state machine

- **NORMAL**: reserved + confirmed service messages below 950; process eligible outbound replies within applicable customer-service window.
- **WARN / CONSERVE**: at/above 950 and below 990; issue a *single* user/owner warning only if there is an authorised free/quota-compliant route, prefer one concise response and suggest Telegram. Do not send extra cost-bearing messages solely to announce quota.
- **STOP_NORMAL**: at/above 990; deny routine service-message sends before calling Meta (including retries that lack a valid reservation). Keep 10 units as an **unapproved policy reserve** for exceptional/admin cases; do not consume without later explicit business policy. Do not promise that this prevents external/BSP charges.
- **UNKNOWN / reconciliation conflict**: fail closed for no-extra-cost modes; do not blindly resend if Meta acceptance/delivery status is uncertain. Idempotency token + outbox state and delivery status reconciliation needed.
- **Billing window**: meter per phone-number and provider-defined monthly service allowance; current time/period must be computed on each checked request; do not rely on hourly/minute Cron reset; calendar/timezone and BSP delivery semantics must be verified.
- **Data correctness**: When a message is blocked, never claim its underlying business request was saved. If it had already been committed before outbound failure, retain record truth and offer legitimate alternate notification/retrieval, not duplicate commits.

**Arithmetic example only:** 1,000 allocation → warning at **950** = 95%; normal hard stop at **990** = 99%; **10** reserved. This is **user-proposed operating policy**, not Meta's mandatory free-tier cutoff or a locked Kerani entitlement.

## 6. Architecture options — E-016 delta-only challenge

| Choice | Upside | Critical weakness | Verdict |
|---|---|---|---|
| A. Central Apps Script `doPost` + LockService/ledger | Fewer systems; event-driven direct, no clock polling needed | Concurrency, response-time, webhook trust, shared retry/ledger semantics need proof | **BASELINE**, do not assume it fails |
| B. CF Worker ingress/egress + Apps Script | Single guard for signatures, routing, quota/outbound; avoids polling and can fast-ACK where durable work exists | Adds secret boundary and another failure path; atomic counter/durability still needs design | **PREFERRED PILOT CANDIDATE** |
| C. CF Worker + D1 or Durable Object + optional Queue + Apps Script | Durable admission/retries and serialization/atomic quota guard if correctly implemented | More moving parts, limits and storage bills; risk of dual SoT or false ACK | **PRODUCTION CANDIDATE ONLY IF TESTS JUSTIFY** |

D1 vs Durable Objects is **NOT LOCKED**: use D1's serialized per-database writes with a properly conditional update/transaction or a single Durable Object per WhatsApp phone number, then demonstrate concurrent increment invariants in a fixture. KV eventual consistency alone should not be used for a hard quota cap. Keep Apps Script / authoritative Core record storage independent of channel delivery ledger; **no second business SoT**.

## 7. CF-WA-QG-01 — future SYNTHETIC challenge, NOT RUN/NOT APPROVED FOR DEPLOYMENT

| Case | Fixture and proof |
|---|---|
| T01 | 10 concurrent candidate sends when count/reservations sit at 989/990 → no more than permitted normal messages accepted; no lost reservation/negative credit. |
| T02 | Duplicate Meta webhook IDs + worker retries → one logical inbound processing/authoritative business side effect, truthful cached receipt. |
| T03 | Apps Script timeout, unavailable API and ambiguous response → record pending/error, avoid duplicate commit/send, retry safely; distinguish durable ACK from final SAVE. |
| T04 | 5–30 second delayed work via Queues or DO Alarm; compare with direct webhook and Apps Script time trigger; measure P50/P95/P99, not a guaranteed sub-minute SLA. |
| T05 | Quota period boundary, 950 warning once, 990 normal stop, template categories and non-Worker sender path; reconcile Meta delivery status with internal reservation ledger. |
| T06 | Worker→Apps Script forged request/replay/tenant mismatch; bad Meta signature; protection/no leakage. |
| T07 | Interrupted queue processing and message retention exhausted; DLQ/recovery, one business SoT, no false delivered receipt. |
| T08 | Cost/complexity benchmark versus Apps Script-only for realistic tenant count, burst, AI downtime, storage and provider send fees. |

**PASS is NOT claimed.** Measure real Cloudflare / Google quotas, failure modes, operational complexity, provider changes and charges with synthetic-only data and explicit owner execution approval before selecting architecture or building tasks.

## 8. Governance / lineage

- **Preserved LOCKED:** D-015 record/validation, D-016 Free usefulness, D-023 independent tenant identity, **D-025/L-019** Telegram high-usage Free + controlled shared WhatsApp, **D-027/L-021** separate transport/AI/storage/retrieval meters, D-052 idempotent timing, D-055/L-046 Free no-AI, D-057/L-047 Mini App, D-061/L-049 chat-first identity.
- **Complementary candidate:** D-060 cost/cloud/AI concurrency — separate proposal; no silent replacement/architecture.
- **Do not change:** D-062 RekodUntung.ai PRIMARY BRAND CANDIDATE, NOT LOCKED; unaffected by this study.
- **No implementation:** no Cloudflare Worker, Queue, Durable Object, D1, Apps Script config, WhatsApp credentials or customer message changes in this task.

**NEXT — exactly one:** **CF-WA-QG-01 — ZASS Synthetic Architecture Challenge** (compare A/B/C and T01–T08), only with separate owner execution approval; then decide if a CF edge guard provides better evidence than `doPost()` Apps Script baseline.
