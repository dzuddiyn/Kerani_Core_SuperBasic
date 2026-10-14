# Evoxt Malaysia VPS — Paid Server Contingency / Last Choice

**Recorded:** 2026-10-14  
**Status:** CANDIDATE — BACKUP / LAST CHOICE ONLY, NOT ARCHITECTURE LOCK  
**Evidence category:** Vendor marketing + owner-supplied user experience (ANECDOTAL); requires independent verification  
**Scope:** E-016 V1 control-plane feasibility / future contingency. Does not expand the active four-way E-016 benchmark.

## Why retain

Evoxt Malaysia VPS may provide a low-entry-cost **paid self-managed VM fallback** if free serverless or free-VM options cannot meet Kerani's observed operational needs at sustainable cost/maintenance. This is a contingency **server/runtime**, **not** AI-model fallback and **not** the default hosting commitment.

## Initial source evidence, not benchmark proof

- Owner-shared Evoxt social advertisement (2026-10-14) markets Malaysia VPS from **USD 2.99/month** and an **up to 6.0 GHz** turbo-frequency claim. This promotional CPU figure does **not** establish guaranteed sustained vCPU speed, dedicated physical cores, superior real-world workload performance, or a sufficient VM configuration.
- A user identified by the owner as **Akmal “Shan0h” Fauzi** reported having used Evoxt himself and commented that **bandwidth/transfer allowance was limited** and **entry-level RAM was small** for hosting multiple services; a one-year term felt more worthwhile. This is one user's experience, **not** an independently measured capacity/reliability verdict.
- Vendor reference: https://evoxt.com/vps-malaysia/ . Specifications, location, included traffic, vCPU allocation, renewal/annual pricing, SLA, backup details and terms **must be rechecked when test/purchase becomes relevant**.
- Earlier comparative research discussed VM tiers such as **2 GB RAM / USD 5.99 per month** and **4 GB RAM / USD 11.99 per month** as **indicative**, not owner-approved SKU/pricing commitments.

## Intended role / activation rules

1. **Prefer the selected free/low-fixed-cost central control plane if pilot workload proves it sufficient.** Existing E-016 active candidates remain: Central Apps Script, Cloudflare Workers+D1, Cloud Run/Firestore, and OCI A1 Always Free.
2. **Evaluate Evoxt only as paid contingency** if a measurable operating blocker remains (e.g., free quotas/capacity, predictably unacceptable latency/recovery, need for OS/process/worker control, or unworkable free-resource availability), and a VPS solves it within an acceptable fixed monthly budget and one-maintainer maintenance envelope.
3. **Do not buy to accelerate the Kerani Agro Basic Demo** unless its existing validated runtime is demonstrably inadequate. A paid VPS is not a prerequisite for the first Wan/Hamidun demo.
4. If triggered, run **one small time-limited test** with synthetic workloads and no production secrets/data, comparing realistic Telegram webhook latency (P50/P95/P99), CPU throttling, RAM at peak, monthly transfer usage versus plan allowance, uptime/restarts, OS patching, TLS/secrets, backup/restore, monitoring, AI upstream latency, and estimated total cost.
5. **Monthly pilot before annual commitment.** Any annual discount or long-term pricing must be verified; do not pay in advance solely on the basis of an anecdotal recommendation.
6. Only architecture-challenge evidence + explicit owner PRE-ARCH approval can promote a VPS into the chosen central runtime. The provider must remain replaceable; use stable Kerani contracts/tenant identity/data portability.

## Guardrails

- A self-managed VPS has **continuous operations/security/backup responsibility**, unlike managed serverless; low monthly sticker price is not the full operating cost.
- CPU GHz advertising cannot directly accelerate external Gemini/Workers AI inference.
- Bandwidth can mean **transfer quota** rather than port speed; evaluate both separately.
- No change to D-055 Free Core independence, D-056 AI-first UX candidate, deterministic domain authority, privacy, existing confirmation/idempotency or TEST/PROD isolation.
- E-016 remains a **four-way active candidate comparison**. Evoxt is a **conditional paid escape hatch**, not a fifth immediate build/prototype, and does not reopen OpsMate Purchase regressions.

**Owner direction:** "ya simpan sebagai calon back up/last choice server etc. commit" — 2026-10-14.  
**Execution status:** No provider signup, charge, server deployment, benchmark, product build or PRE-ARCH change authorized by this note.
