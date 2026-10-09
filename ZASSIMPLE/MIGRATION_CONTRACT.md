# ZASSIMPLE Migration Contract — Kerani Core SuperBasic

**Version:** 0.2  
**Status:** OWNER APPROVED — COMMITTED  
**Approved:** 2026-10-09  
**ZASS SYSTEM baseline:** v0.2.2  
**Full ZASS baseline:** v0.3.11  
**Primary project method:** ZASSIMPLE v0.3.3  
**Migration type:** method + presentation/workflow surface migration  
**Architecture impact:** NONE by itself

> **Kerani Core SuperBasic operates primarily under ZASSIMPLE. Existing Full ZASS artifacts remain retained governance/evidence lineage and an escalation capability when stronger governance is materially required.**

> **Show the project, not the repository.**

> **Complexity may exist underneath; complexity must earn the right to appear on the surface.**

> **GitHub is the System of Truth. Chat is the System of Understanding.**

## 1. Authority boundary

ZASSIMPLE is the primary project operating method and human-facing design/planning/execution surface. It must preserve existing LOCKED project lineage and must not silently rewrite retained governance/evidence.

| Concern | ZASSIMPLE | Retained Full ZASS lineage |
|---|---|---|
| Current status/focus | **Primary** | Historical/governance reference |
| NEXT exact action | **Primary** | Consult when governance impact exists |
| Design/architecture | **Current DESIGN surface** | Existing AC/D/evidence lineage retained |
| Action Plan | **Canonical planning artifact** | Existing decisions constrain planning |
| Atomic tasks | **Canonical execution queue** | Existing locks/evidence constrain execution |
| Existing LOCKED decisions | Must honour them | Retained authoritative lineage |
| Questions/risks/experiments | Surface only what is currently useful | Full historical ledger retained |
| Evidence/receipts | Current execution summary/receipts | Historical evidence retained |
| Escalation | Starts in ZASSIMPLE | Full ZASS used when materially stronger governance is required |

**Conflict rule:** verified Git state and existing LOCKED project lineage win. Current workflow/command semantics follow ZASS SYSTEM v0.2.2 + ZASSIMPLE v0.3.3; Full ZASS v0.3.11 is used when escalation requires it.

## 2. Repository mapping

~~~text
Kerani_Core_SuperBasic/
├── ZASS_Kerani_Core_SuperBasic.md
│   └── retained Full ZASS governance/evidence lineage + escalation reference
├── ACTION_PLAN.md
│   └── compatibility pointer only
└── ZASSIMPLE/
    ├── MIGRATION_CONTRACT.md
    ├── DESIGN.md
    ├── ACTION_PLAN.md
    └── TASKS.md
~~~

## 3. Artifact contract

### ZASSIMPLE/DESIGN.md
Human-readable current design projection.

It may distil current design/architecture later, but this migration commit intentionally does **not** copy or alter architecture decisions.

### ZASSIMPLE/ACTION_PLAN.md
Canonical planning artifact after this migration.

It may feed design and execution but cannot silently revise architecture or override LOCKED decisions.

The pre-migration root `ACTION_PLAN.md` content is preserved inside the new canonical file so planning lineage is not lost.

### ZASSIMPLE/TASKS.md
Atomic execution queue.

Default human surface should expose only the current task / NEXT exact action. Future queue detail may remain internal.

### Root ACTION_PLAN.md
Compatibility pointer only. No planning state may be maintained there after migration.

## 4. Human-facing UI contract

Default progression:

~~~text
GLANCE
status + focus + next
   ↓
REVIEW
options + evidence + trade-off
   ↓
DETAIL
contracts + architecture + tests
   ↓
HISTORY
D/L/Q/R/E + superseded + changelog
~~~

Presentation rules:

1. Human concept before internal ID.
2. One primary idea per screen by default.
3. Progressive disclosure instead of repository dumps.
4. Raw ASCII architecture is not the default user UI.
5. Tables/cards/clear visual hierarchy are preferred for normal review.
6. Repository formatting is an export/storage representation, not the primary user interface.
7. Internal lineage IDs may appear as compact secondary context, e.g. `Lineage: AC-010 · Q-032 · E-016`.

## 5. Write-through contract

~~~text
ZASSIMPLE proposal
→ owner PROCEED
→ method/governance-compatible update prepared
→ owner COMMIT
→ update affected ZASSIMPLE artifacts
→ update retained Full ZASS lineage only when the change materially touches its governed decisions/evidence/history
→ atomic Git commit
→ verify real SHA
→ report factual persistence
~~~

ZASSIMPLE must never report a decision as persisted when Full ZASS/Git state does not support that claim.

## 6. Sync / stale rule

ZASSIMPLE artifacts are derived from current project truth.

If the ZASSIMPLE surface is stale relative to verified repository state or retained LOCKED project lineage:

> **ZASSIMPLE STATUS: STALE — refresh project truth before decision/execution.**

Do not silently overwrite retained governance/evidence records from the simplified surface.

## 7. Escalation rule

Start DESIGN in ZASSIMPLE. Escalate to Full ZASS only when materially stronger governance is needed, such as a material architecture contradiction, safety/security impact, authority change, evidence conflict with a LOCKED decision, multiple materially different architecture choices, or another irreversible/high-cost decision.

No automatic migration/escalation is allowed. After any Full ZASS review, distil the governed result back into ZASSIMPLE.

## 8. Acceptance criteria

Migration succeeds only if:

- zero governance/evidence information is lost;
- the user can understand the current project without reading the full D/Q/R/E ledger;
- NEXT exact action remains clear;
- simplified claims are traceable to Full ZASS;
- COMMIT updates the relevant backplane/surface artifacts atomically;
- ZASSIMPLE remains the primary operating method while Git remains the durable Source of Truth;
- existing architecture readiness, evidence confidence and decision states do not change merely because of this migration.

## 9. Scope of this commit

This commit:
- persists this migration contract;
- creates ZASSIMPLE `DESIGN.md`, `ACTION_PLAN.md`, and `TASKS.md`;
- moves canonical planning authority from the root Action Plan to `ZASSIMPLE/ACTION_PLAN.md` while preserving the prior plan content;
- converts root `ACTION_PLAN.md` into a compatibility pointer;
- does **not** migrate, modify, confirm, supersede or re-score architecture decisions.


## 10. Current technical execution baseline

For substantial technical work, use the current shared method flow:

~~~text
DESIGN
→ CHALLENGE DESIGN / ARCHITECTURE
→ controlled revision
→ YA, LOCK PRE-ARCH
→ EXECUTION REALITY CHECK
→ real artifact/sample pack + execution-surface map
→ detailed ACTION PLAN ↔ PRE-ARCH
→ evidence-bounded vertical atomic task
→ result/proof
→ delta planning + PRE-ARCH review
→ next unresolved task only
→ sufficient evidence
→ LAST DESIGN / ARCHITECTURE CHALLENGE
→ final improvement/revision
→ YA, CONFIRM DESIGN / ARCHITECTURE
→ rebuild RELEASE ACTION PLAN
→ fresh release atomic tasks
→ release acceptance
→ DELIVERED !!
~~~

Real artifacts/samples should be used as early as reasonably, safely and legitimately obtainable. Synthetic substitutes must be marked provisional when they stand in for unavailable real evidence.

## 11. Baseline correction note

This v0.2 correction changes method/surface semantics only. It does not alter any Kerani architecture/product decision, readiness score or evidence state.

Current baseline:
- ZASS SYSTEM v0.2.2
- Full ZASS v0.3.11
- ZASSIMPLE v0.3.3
