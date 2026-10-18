# Kerani AI — Linear Development Tracking Contract

**Mode:** GitHub-First + Linear Progress Tracking  
**Project:** Kerani AI  
**Status:** PILOT — NON-AUTHORITATIVE TRACKING  
**Owner approval:** 2026-10-18  
**Applies:** Work on the approved Kerani AI project and `dzuddiyn/Kerani_Core_SuperBasic` documentation/development. Do not silently extend this contract to unrelated repositories/projects.  
**Authority order:** GitHub verified technical truth and existing owner-LOCKED decisions > owner scope/approvals > Linear progress projection.  
**Operating principle:** **GitHub holds the truth. Linear tracks the work. AI reconciles both.**

## 1. Purpose

Use the connected Linear app/plugin as **lightweight, non-authoritative** development tracking. After **every successful Git commit made during an active assisted Kerani AI session**, update the matching approved Linear issue **in that same session** without waiting for new permission for routine tracking. This is an *in-session post-commit workflow*, not a guarantee of unattended/background syncing outside a session.

Do not make Linear a code, build, deploy, task-definition or business-data dependency. If unavailable or unconfigured, development may continue with an explicit pending-sync record and later idempotent reconciliation.

## 2. Ownership and data boundaries

- **GitHub:** code, architecture, decisions, implementation tasks, commits, PRs, tests and evidence are authoritative.
- **Linear:** issue progress, blockers, milestones, verification and exactly one NEXT; only a reflection of GitHub work.
- **Owner:** scope changes, LOCKED/architectural decisions, team/project setup, approvals and releases.
- Never move a LOCKED decision from GitHub to Linear or mark an architectural recommendation approved because it appears in an issue.
- No credentials, secrets, tokens, production customer data or sensitive evidence in Linear.
- No mass deletion/archive, team restructuring, paid actions, production changes or workspace-setting changes via routine sync.

## 3. Initial Linear target (PENDING until verified)

**Requested team:** `Kerani_AI` (owner approved replacing/renaming existing `DZU` or creating the new team and retiring `DZU`).  
**Requested project:** `Kerani AI`.  
**Requested starter issue:** one issue describing this tracking contract.  
**Issue IDs:** use whatever identifier Linear actually issues; do not invent `KAI-XXX` if its team key is not `KAI`.

**Discovery evidence 2026-10-18 (session check):** workspace `dzuddiyn`; existing team `Dzuddiyn` (key `DZU`); four onboarding issues DZU-1 through DZU-4; **no project or Kerani AI issue**. The available Linear connector has get/list-team methods but **no create/update/delete-team action**, so the owner-requested `Kerani_AI` team cannot currently be created or renamed through that connector. **Do not create Kerani AI under the unintended DZU team as a workaround.** Do not delete DZU or its onboarding issues. Once the team exists via authorised Linear UI/workspace action, create the approved project and one tracking issue and verify their IDs.

## 4. Required post-commit workflow (per successful commit)

### A — Verify Git

- Verify the actual commit exists. Capture exact SHA, commit message, branch and changed files.
- Record tests **actually run**: `PASS`, `FAIL`, `NOT RUN`; distinguish docs/read-back from application regression tests.
- Distinguish `LOCAL`, `PUSHED`, `MERGED`, using actual evidence. For GitHub connector commits on `main`, verify the remote SHA before reporting PUSHED.
- Record PR link only if it exists; do not fabricate.

### B — Identify matching issue

- Search the approved `Kerani AI` project before creating or commenting.
- One issue can contain multiple commits for one work item; never create an issue for each commit.
- If no matching issue exists, report **TRACKING GAP**, do not invent an issue or reuse unrelated onboarding issues.
- Creating the explicitly authorised **single starter issue** is permitted after the requested team/project exist. Further issue creation requires appropriate permission.

### C — Update Linear

Append a concise comment or adjust the appropriate issue fields, without changing architecture decisions:

```text
COMMIT UPDATE
Issue: <actual issue identifier>
Commit: <full SHA>
Branch: <actual branch>
Changes: <factual summary>
GitHub: <verified commit/PR URL or LOCAL ONLY>
Commit status: LOCAL / PUSHED / MERGED
Tests: PASS / FAIL / NOT RUN
Verification: PASS / PENDING / FAILED
Blocker: None / <actual blocker>
NEXT: <one precise action>
Updated: <date>
```

Preserve proper status semantics:
- **Backlog:** not started.
- **In Progress:** development ongoing.
- **Blocked:** actual blocking dependency exists.
- **In Review:** review/verification pending.
- **Done:** acceptance criteria and verification evidence completed; never merely because a commit exists.

Use the team's actual available workflow states; map meaning carefully rather than creating new states without permission.

### D — Read-back and idempotency

- Re-read the issue/comment after save; confirm commit SHA, status, test evidence, blocker and NEXT.
- Report **`LINEAR SYNC: VERIFIED`** only after successful read-back.
- Report **`LINEAR SYNC: FAILED/PENDING`** if save, permissions, team/project configuration or read-back fails.
- Before retry/reconciliation, search existing comments by full commit SHA to avoid duplicate updates.
- An unavailable team/project or issue produces an explicit **TRACKING GAP**, not fictional synchronization.

## 5. End-of-task status receipt

```text
KERANI AI — DEVELOPMENT UPDATE
GitHub: COMMITTED / PUSHED / MERGED / NO COMMIT
Linear: VERIFIED / PENDING / FAILED
Issue: <real issue ID or TRACKING GAP>
Tests: PASS / FAIL / NOT RUN
Blocker: None / <real blocker>
NEXT: <exactly one action>
```

## 6. Startup/sync reconciliation rule

When a Kerani AI session begins and Linear is connected:
1. Check workspace/team/project availability, then search issues related to the current GitHub work.
2. If the approved target exists, reconcile *documented pending commits* without duplication.
3. Do not import all repository history or flood Linear automatically.
4. If an owner action is needed for `Kerani_AI` team setup, request the smallest UI action; do not substitute DZU or delete data.
5. If connector cannot operate, leave GitHub development unblocked and maintain a truthful pending-sync receipt.

## 7. Scope of this documentation activation

The owner explicitly authorised: create Linear project `Kerani AI` **under team `Kerani_AI`**, one initial issue, and commit this contract into repository documentation and agent instructions. This authorisation does not create a team through an unavailable tool, permit an unrelated-team workaround or allow destructive workspace edits.

**Current Linear bootstrap status (2026-10-18):** `PENDING — TEAM SETUP REQUIRED`. GitHub contract documentation is valid in the meantime; successful Linear sync has **not** been claimed.
