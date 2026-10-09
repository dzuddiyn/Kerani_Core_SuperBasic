# ZASSIMPLE TASKS — Kerani Core SuperBasic

**Status:** EXECUTION QUEUE — SKELETON  
**Authority:** Tasks execute the plan. They do not rewrite LOCKED decisions.

> This file was created by the ZASSIMPLE surface migration. No architecture decision was moved or changed by creating this queue.

## Current task

**NONE — migration skeleton only.**

A current task should be added only after the canonical ZASSIMPLE Action Plan is reviewed/distilled enough to identify one bounded executable outcome.

## Atomic readiness

A task is READY only when it has:
- one primary outcome;
- bounded scope;
- explicit dependencies/inputs;
- clear allowed/forbidden scope;
- observable acceptance criteria;
- tests/regressions;
- evidence expectations;
- no unresolved architecture judgment.

If the worker must choose between materially different designs, return the item to ZASSIMPLE ACTION PLAN / DESIGN. Escalate to retained Full ZASS governance only when materially stronger governance is actually required.

## Task template

<!--
T-001 | READY
Phase: PRE-ARCH EVIDENCE / RELEASE BUILD / ORDINARY EXECUTION
Primary outcome: ...
Source / lineage: AP-xxx / D-xxx / DESIGN section
Dependencies: ...
Inputs: ...
Allowed scope: ...
Allowed files/modules: ...
Forbidden scope: ...
Do: ...
Why: ...
Acceptance criteria: ...
Tests: ...
Regression requirements: ...
Evidence required: ...
Commit expectation: ...
STOP & ESCALATE: architecture/LOCKED-decision impact returns to governed review
Then: T-xxx / next-step label
Result: ...
Architecture impact: NO ARCH IMPACT / TASK-PLAN ISSUE / PRE-ARCH REVIEW REQUIRED / LOCKED DECISION IMPACT
Reviewer disposition: PENDING / PASS / REWORK / REVISE PRE-ARCH / BLOCK OWNER DECISION
-->

## Queue

<!-- Keep future tasks concise. Surface one current task to the user by default. -->

## Result → PRE-ARCH review rule

Completion of a task does not automatically authorize architecture change. Material architecture impact returns to governed review; LOCKED-decision impact returns to the owner.

## Release-build rule

After confirmed technical design/architecture, create a fresh RELEASE BUILD queue from the rebuilt canonical Action Plan.

Do not mark `DELIVERED !!` merely because tasks were attempted.

## Delivered evidence

Not applicable yet.
