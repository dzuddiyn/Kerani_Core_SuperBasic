# ZASSIMPLE Migration Contract — Kerani Core SuperBasic

**Version:** 0.1  
**Status:** OWNER APPROVED — COMMITTED  
**Approved:** 2026-10-09  
**ZASSIMPLE baseline:** v0.3.3  
**Migration type:** presentation + workflow surface migration  
**Architecture impact:** NONE by itself

> **Full ZASS remains the governance/evidence backplane. ZASSIMPLE becomes the primary human-facing operating surface.**

> **Show the project, not the repository.**

> **Complexity may exist underneath; complexity must earn the right to appear on the surface.**

> **GitHub is the System of Truth. Chat is the System of Understanding.**

## 1. Authority boundary

ZASSIMPLE is a simplified projection and execution surface. It must never become a second architecture/decision authority.

| Concern | ZASSIMPLE | Full ZASS |
|---|---|---|
| Current status/focus | Primary human display | Backing authority/evidence |
| NEXT exact action | Primary human display | Must remain governance-compatible |
| Design/architecture summary | Human-readable projection | AC/D/evidence authority |
| Action Plan | Canonical planning artifact | Constrained by LOCKED decisions |
| Atomic tasks | Canonical execution queue | Must obey governance/evidence gates |
| Locked decisions | Summarised only when relevant | Authoritative |
| Questions/risks/experiments | Active/current subset only | Full Q/R/E ledger |
| Evidence/receipts | Summary/status | Full durable evidence |
| Superseded history/changelog | Hidden by default | Preserved permanently |

**Conflict rule:** verified Full ZASS + Git state wins.

## 2. Repository mapping

~~~text
Kerani_Core_SuperBasic/
├── ZASS_Kerani_Core_SuperBasic.md
│   └── Full ZASS governance/evidence backplane
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
→ governance-compatible update prepared
→ owner COMMIT
→ update affected Full ZASS + ZASSIMPLE artifacts
→ atomic Git commit
→ verify real SHA
→ report factual persistence
~~~

ZASSIMPLE must never report a decision as persisted when Full ZASS/Git state does not support that claim.

## 6. Sync / stale rule

ZASSIMPLE artifacts are derived from current project truth.

If the simplified surface is stale relative to Full ZASS or verified repository state:

> **ZASSIMPLE STATUS: STALE — refresh from Full ZASS before decision/execution.**

Do not silently overwrite governance records from the simplified surface.

## 7. Escalation rule

Escalate from ZASSIMPLE to Full ZASS Architecture Challenge when there is a material architecture contradiction, safety/security impact, authority change, evidence conflict with a LOCKED decision, multiple materially different architecture choices, or another irreversible/high-cost decision.

After review, distil the result back into ZASSIMPLE.

## 8. Acceptance criteria

Migration succeeds only if:

- zero governance/evidence information is lost;
- the user can understand the current project without reading the full D/Q/R/E ledger;
- NEXT exact action remains clear;
- simplified claims are traceable to Full ZASS;
- COMMIT updates the relevant backplane/surface artifacts atomically;
- ZASSIMPLE remains a projection/planning/execution surface, not a second Source of Truth;
- existing architecture readiness, evidence confidence and decision states do not change merely because of this migration.

## 9. Scope of this commit

This commit:
- persists this migration contract;
- creates ZASSIMPLE `DESIGN.md`, `ACTION_PLAN.md`, and `TASKS.md`;
- moves canonical planning authority from the root Action Plan to `ZASSIMPLE/ACTION_PLAN.md` while preserving the prior plan content;
- converts root `ACTION_PLAN.md` into a compatibility pointer;
- does **not** migrate, modify, confirm, supersede or re-score architecture decisions.
