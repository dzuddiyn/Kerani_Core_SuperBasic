# ZASSIMPLE DESIGN — Kerani Core SuperBasic

**Status:** DRAFT READY FOR CHALLENGE  
**Design Progress:** 4/4 — purpose / main flow / main elements / relevant LOCKED decisions  
**Authority:** Current ZASSIMPLE design surface. It must preserve existing LOCKED project lineage and verified evidence; Full ZASS is retained for governance/history and escalation when materially required.

**Project state:** 65% — DECIDING  
**Evidence confidence:** LOW  
**Pre-confirmation challenge:** NOT RUN  
**Challenge count:** 0  
**Architecture impact of this distillation:** NONE  
**Execution baseline:** NOT LOCKED  
**PRE-ARCH version/reference:** none

> **Show the project, not the repository.**

This file distils retained project truth into the current ZASSIMPLE human-facing design view. It does **not** add, remove, confirm, supersede or re-score any architecture/product decision.

**Method baseline:** ZASS SYSTEM v0.2.2 · ZASSIMPLE v0.3.3 · Full ZASS v0.3.11 (escalation/governance when required).

## Purpose

Kerani Core SuperBasic is a deliberately small generic micro-SME core that should remain useful on its own for basic operational record keeping.

Its Free baseline centres on:
- Purchase;
- Sale;
- Inventory;
- Observation;
- Task;
- receipt capture/input where available;
- basic retrieval, summaries and reports.

The product should stay lightweight, affordable and portable. Domain depth, richer automation and higher-order intelligence sit outside the generic Free Core rather than turning Core into a large special-case system.

## Main flow

### Locked user-facing record flow

1. User interacts through a supported channel.
2. Channel resolves to a persistent Kerani tenant identity.
3. For short operational free text, Kerani may suggest intent/category and extract a structured candidate.
4. Ambiguous input must trigger clarification rather than silent guessing.
5. The user reviews the candidate and may confirm, correct or cancel.
6. Deterministic/domain validation runs before an AI-interpreted mutation becomes authoritative.
7. Authoritative records can then be retrieved, summarised and reported.
8. When a request crosses the Free boundary, Kerani should clearly surface the relevant Premium capability rather than silently failing.

### Candidate runtime shape — not LOCKED

The current runtime candidate separates direct/read work from stateful/mutation work, with channel adaptation before business logic and a Core ↔ Domain Module boundary.

Whether routing ownership, Durable Inbox usage and confirmation responsibility belong universally in Core remains unresolved.

**Lineage:** D-015 · AC-005 · Q-015 · Q-016 · Q-017

## Main elements

| Layer | Current distilled truth |
|---|---|
| **Experience** | WhatsApp, Telegram and future interfaces are channels/bindings, not the identity of Kerani or the tenant. |
| **Identity & data** | One persistent tenant identity; tenant-isolated history; channel migration without data migration; user export rights preserved. |
| **Free Core** | Purchase · Sale · Inventory · Observation · Task · receipt input · basic retrieval · basic summaries/reports. |
| **Domain modules** | Exactly three planned modules: Agro · Servis Teknikal · Makanan & Tempahan. |
| **Premium domain solution** | OpsMate-grade validated operational workflows may require structured onboarding, domain contracts and controlled validation/persistence. |
| **Premium Operations — CANDIDATE** | Alert · Remind · Report · Ask. |
| **Premium Intelligence — CANDIDATE** | Analysis · Correlation · Graph · Proposal · Forecast. |
| **AI boundary** | Deterministic-first where AI adds no value; constrained natural-language convenience may exist in Free; rich/open-ended conversation remains Premium. |
| **Free channels** | Telegram is the economic/high-usage Free channel; shared WhatsApp is a controlled convenience/discovery channel. |
| **Premium channel path** | Dedicated/owned WhatsApp and optional customer-owned Google/Apps Script/AI may be configured later without changing tenant identity. |
| **Reliability** | OpenClaw is a replaceable external synthetic reliability/audit harness, not Kerani business authority or the production control plane. |
| **IoT safety boundary** | Kerani may add context, history, notification and escalation; a critical device/PLC/HA alarm must not depend solely on Kerani/LLM/cloud. |
| **POS / ERP growth** | Future adapter/contract path; established ERP-owned records remain authoritative in the ERP. |
| **Government/programme bridge** | Optional; sponsor funding does not grant blanket data authority; agency/programme remains authority for eligibility/approval/status. |
| **Growth model** | Evidence-first, low-cost-at-low-usage, controlled scale, replaceable partners, V-Road maturity. |

## Product ladder

| Layer | What the user gets |
|---|---|
| **Free Core** | Record · retrieve · basic summary/report |
| **Premium Operations — CANDIDATE** | Alert · Remind · Scheduled Report · Interactive Ask/Retrieval |
| **Premium Intelligence — CANDIDATE** | Analysis · Correlation · Graph · Proposal · Forecast |
| **Premium Domain Solution** | OpsMate-grade validated workflows with structured onboarding/domain rules |

Exact Credit Pass values, quotas, bundle design and premium capability pricing remain deferred.

## Current architecture candidates

### Runtime / module boundary

**AC-005 — CANDIDATE**

Current evidence supports testing an explicit channel boundary, request routing, generic Core orchestration and separate Domain Module contracts. Direct/read and stateful/mutation paths may differ.

Still unresolved:
- who owns request routing;
- which requests truly need a Durable Inbox;
- whether human confirmation is universally Core-owned or policy/module-owned.

### Tenant-centric hosted-Free → owned-Premium

**AC-006 — CANDIDATE**

Tenant identity and history remain independent from channel/provider choices. Shared Free infrastructure may later transition to owned/dedicated Premium infrastructure without tenant/data migration.

### V1 control-plane candidates

No provider is selected or LOCKED.

| Option | Current role |
|---|---|
| **Central Apps Script** | Simplicity baseline for E-016 |
| **Cloudflare Workers + D1** | AC-010 lightweight low-entry-cost candidate |
| **Cloud Run + Firestore + Secret Manager + basic Monitoring** | AC-007 scalable serverless candidate |

**E-016** must compare setup/maintenance burden, entry/billing friction, webhook behaviour, latency/concurrency, tenant/quota/waitlist handling, secrets, scheduling/async needs, observability, failure recovery, low-traffic economics, scale-up and migration/rollback.

The owner's current approximately RM200 Google Cloud billing/onboarding barrier is a practical account-side constraint only; it is not treated as a universal Cloud Run fee.

### Programme and scale candidates

- **AC-008 — CANDIDATE:** sponsor-funded assistance/outcome bridge with user-controlled/minimum-necessary data sharing.
- **AC-009 — CANDIDATE:** pilot → proof → just-enough infrastructure → event/viral readiness → replaceable partner-backed scale.
- Named event, agency, vendor, client-reference and grant details remain external/deferred until real evidence/approval exists.

## Constraints from LOCKED decisions

The design must preserve these boundaries:

- **Free must remain genuinely useful.** Premium adds higher-order intelligence, domain capability, automation and convenience rather than blocking basic access.
- **Genericity is earned.** OpsMate supplies evidence; reusable mechanisms may feed Core, agriculture behaviour may feed Agro, and BSE-specific rules stay outside generic Core.
- **Human authority remains explicit.** AI-interpreted mutations require review/confirmation and deterministic/domain validation before authoritative write.
- **No artificial data lock-in.** Users may access/export their own data.
- **Tenant identity is channel-independent.** Moving between WhatsApp, Telegram or future channels must not require a new tenant/history.
- **Quotas are independent.** Transport, storage/media, AI/processing, report/retrieval fair-use and Premium credits are separate controls.
- **Deterministic-first Free processing.** Free onboarding does not require BYO Gemini.
- **OpenClaw is not business authority.** Synthetic monitoring must not bypass normal controls or contaminate customer truth.
- **Critical IoT alarm path stays local/deterministic.** Kerani may augment it, not become the sole safety dependency.
- **Sponsor ≠ data authority.** Programme sharing is minimum-necessary and purpose-bound; agency remains programme authority.
- **Growth must be evidence-led.** Pilot proof precedes public-scale claims; viral readiness requires load, cost, reliability, fallback and observability evidence.
- **Infrastructure/partners must remain replaceable.** Core, tenant identity, portability and business authority cannot be surrendered to one provider/partner.
- **Real field evidence comes early.** When real samples exist they are first-class execution evidence; missing real samples must be marked UNVALIDATED rather than field-proven.
- **V-Road applies:** Value → Verbal → Volume → Viral → Vary → Venture → Versatile. Every V must be earned through evidence.

## Open assumptions / unresolved boundaries

These remain open; this design projection does not resolve them:

1. **Routing ownership** between direct/read and stateful/mutation paths — Q-015.
2. **Durable Inbox scope** — Q-016.
3. **Confirmation ownership**: Core-mandatory vs optional capability vs module/application policy — Q-017.
4. **Minimum Core ↔ Module contract**.
5. **Generic validation vs domain validation boundary**.
6. **Provider/parser substitution** behind a stable behaviour contract.
7. **V1 control-plane selection** — E-016; Apps Script vs Cloudflare vs Cloud Run.
8. **Exact Free quotas / shared-WA limits / OCR allowance** — pilot-calibrated.
9. **Premium Operations Pack** — candidate only; needs OpsMate/reuse/cost/safety evidence.
10. **Premium Intelligence Pack** — candidate only; needs real-data usefulness, uncertainty/error and unit-economics evidence.
11. **Government-programme bridge / event-scale / partner-scale** — planned experiments/evidence still incomplete.

## Evidence posture

Current confidence remains **LOW**.

What is materially stronger:
- one OpsMate workflow has direct runtime verification;
- locked product/tenant/channel/data/authority boundaries are coherent;
- real-field-evidence-first execution method is approved.

What is still not proven enough:
- generic Core extraction across multiple workflows/domains;
- non-farm reuse;
- quota/isolation/migration behaviour at scale;
- V1 control-plane winner;
- Premium Operations/Intelligence reuse/economics;
- viral/event-scale behaviour;
- partner/programme operational evidence;
- OpenClaw end-to-end reliability on real Kerani ingress.

## Challenge gate

Design coverage is now **4/4**, so the next design gate is challenge, not confirmation.

**Recommended challenge:** Architecture Assumption + Boundary Challenge.

**Why:** the product/design surface is coherent, but several material architecture boundaries and the V1 control-plane choice remain candidates.

A challenge PASS does not automatically confirm final architecture. For this technical project it should lead toward a reviewed PRE-ARCH candidate and explicit owner gate when the evidence is sufficient. After PRE-ARCH lock, run Execution Reality Check before detailed task slicing, using real artifacts/samples and execution-surface mapping before evidence-bounded vertical atomic tasks.

## Final challenge lineage

Not run.

## Challenge / revision lineage

None yet.

Do not silently revise a LOCKED decision. Material architecture findings must return to governed review.

## PRE-ARCH execution baseline

- **Status:** NOT LOCKED
- **Baseline version/reference:** none
- **Challenge summary:** not run
- **Owner approval:** none
- **Evidence still required before final confirmation:** governed by Full ZASS experiments/open loops
- **Supersedes / superseded by:** none

## Lineage

Human-facing compact lineage only:

- **Core/product:** D-010–D-022
- **Tenant/channel/quota/reliability:** D-023–D-033
- **Programme/growth/partner:** D-035–D-049
- **Premium candidates:** D-050 · D-051
- **Architecture candidates:** AC-005–AC-010
- **Current control-plane evidence gate:** E-016
- **Retained Full ZASS lineage / escalation reference:** `../ZASS_Kerani_Core_SuperBasic.md`
- **Method baseline:** ZASS SYSTEM v0.2.2 · ZASSIMPLE v0.3.3 · Full ZASS v0.3.11
- **Migration contract:** `MIGRATION_CONTRACT.md`
