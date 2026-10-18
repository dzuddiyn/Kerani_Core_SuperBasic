# Kerani AI / Kerani Core SuperBasic — Repository Agent Instructions

Read the repository's verified project authority before proposing or changing work:

1. `ZASS_Kerani_Core_SuperBasic.md` — owner decisions, LOCKED contract, project evidence and governance.
2. `ZASSIMPLE/DESIGN.md`, `ZASSIMPLE/ACTION_PLAN.md`, `ZASSIMPLE/TASKS.md` — current design, canonical plan and atomic execution queue.
3. `docs/DEV_WORKFLOW.md` — TEST/production isolation, Git approval and safe extraction workflow.
4. **`docs/LINEAR_DEVELOPMENT_TRACKING_CONTRACT.md` — mandatory GitHub-first, non-authoritative Linear tracking policy for authorised Kerani AI session commits.**

## Authority

- **GitHub is the technical Source of Truth.** Linear never overrides GitHub evidence, code/tests or owner-LOCKED decisions.
- **Owner approval governs** architecture, scope, production changes, release, team/project restructuring and risky/destructive actions.
- Do not treat OpsMate BSE material as generic Core until evidence-backed extraction and reuse prove it.
- Do not copy production secrets or private/customer data into GitHub issues, test fixtures, AI prompts or Linear.

## After every successful Git commit in an active Kerani AI session

1. **Verify** the real SHA, commit message, branch, files, remote/push state, and actual test result.
2. **Search** the authorised Linear Kerani AI project for an existing matching issue; avoid duplicates.
3. **Update** that issue with full SHA/link, factual changes, branch, commit/test/verification states, blockers, date and **one NEXT**.
4. **Read back** the issue/comment and report `LINEAR SYNC: VERIFIED` only on a confirmed match.
5. If the Linear target is missing, access is blocked, or update/read-back fails, report `LINEAR SYNC: FAILED/PENDING` with a factual **TRACKING GAP**; allow GitHub work to continue and reconcile later idempotently by full SHA.

**Do not automatically create new issues for each commit or fabricate Linear IDs.** The owner approved one starter issue and a project **within a team named `Kerani_AI`**, not inside the unrelated existing `DZU` team. On 2026-10-18 the available Linear connector could not create/rename/delete teams; do not delete DZU or use it as an unauthorised substitute. Wait for the named team to exist before creating the approved project/issue.

This is **in-session connector-based synchronization**; do not imply a background daemon/webhook has been deployed or that every out-of-session GitHub commit is monitored.

## Completion report

```text
KERANI AI — DEVELOPMENT UPDATE
GitHub: COMMITTED / PUSHED / MERGED / NO COMMIT
Linear: VERIFIED / PENDING / FAILED
Issue: <verified identifier or TRACKING GAP>
Tests: PASS / FAIL / NOT RUN
Blocker: None / <specific reason>
NEXT: <exactly one action>
```
