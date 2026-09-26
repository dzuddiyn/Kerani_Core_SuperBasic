# Development Workflow

This file governs how this repository is developed. It is deliberately separate from `ZASS.md`: tooling and team workflow must not be mistaken for product architecture.

## 1. Purpose

Use a controlled, evidence-led workflow to extract and validate a small generic Telegram–Apps Script–Gemini core from OpsMate BSE.

The workflow protects three things:

1. **Production safety** — no agent or test may act on live Telegram or business data by default.
2. **Architectural clarity** — implementation follows recorded decisions and tests.
3. **Open-source readiness** — public contributions never accidentally publish secrets, private logs or operational data.

## 2. Roles and boundaries

| Role | May do | Must not do without explicit owner approval |
|---|---|---|
| Owner/operator | Defines intent, supplies approved TEST inputs, approves decisions and deployments | Assume an AI suggestion is a decision |
| Coding agent | Read repository guidance, edit code/docs, run permitted tests, prepare commits | Access Telegram credentials, inject live messages, access production data, expose secrets |
| Reviewer | Inspect diff, tests, architecture and security implications | Merge an unreviewed risky change |
| Runtime | Process only configured environment inputs | Cross TEST/production boundaries silently |

## 3. Environment separation — LOCKED

| Concern | TEST | Production |
|---|---|---|
| Telegram messages | Owner-supplied mock or explicitly authorised TEST traffic | Real users and real operational data |
| Credentials | Separate TEST secret/config | Separate production secret/config |
| Data store | Test sheet/store | Production sheet/store |
| Logs | Sanitised and reviewable | Protected operational log |
| Deployment | Safe to experiment within agreed scope | Explicit owner approval required |

Rules:

- `production_write=false` is the default posture for any unproven workflow.
- Never use production secrets in repository files, fixtures, screenshots or public examples.
- Never copy a production Telegram update/log into a public test fixture without redaction and approval.
- A test must make its environment explicit.

## 4. Standard change loop

1. Read `ZASS.md`, relevant decision records and existing tests.
2. State the change hypothesis and the affected boundary.
3. Make the smallest coherent change.
4. Run syntax checks and targeted regression tests.
5. Inspect the diff for domain leakage, secrets and unintended files.
6. Record evidence: test command/result and any remaining uncertainty.
7. Commit with a narrow, descriptive message.
8. Push/merge/deploy only under the approval boundary below.

No “clean-up” or architectural expansion is bundled into an unrelated functional fix.

## 5. Extraction workflow from OpsMate

When OpsMate is ready:

1. Copy no code immediately; first map component, dependencies, tests and domain terms in `docs/EXTRACTION_LEDGER.md`.
2. Classify each component: `GENERIC`, `OPSMATE-SPECIFIC`, or `UNCERTAIN`.
3. Preserve a behaviour test before modifying a candidate component.
4. Extract one small vertical slice at a time.
5. Replace domain-specific names only after its behaviour is protected by tests.
6. Keep consumer/domain implementation outside the core.
7. Build a second small application as the reuse proof.
8. If the second application demands a core change, record the trade-off as a ZASS candidate decision—do not silently generalise.

## 6. Git and review policy

- Keep commits narrow and reversible.
- Commit message format: `type: concise outcome` — for example, `docs: add generic-core ZASS`.
- Before a commit, check: changed files, secret exposure, tests run and documented reason.
- A coding agent may prepare a commit only within the owner-approved scope.
- Pushing, merging to protected branches, changing repository visibility, releases and deployment require explicit owner approval at the time of action.
- Never rewrite shared history or use destructive Git commands without explicit owner direction.

## 7. Public-stack publication gate

The motto **“Genericity is Generosity”** requires good stewardship.

Before public release, verify:

- no API keys, tokens, chat IDs, personal data or business data remain in history or current files;
- sample configuration is safe and clearly marked as example-only;
- fixtures/logs are synthetic or fully redacted;
- installation, TEST setup and security boundaries are documented;
- licence, contribution policy and versioning approach are explicit;
- the project scope states what it does *not* guarantee; and
- the release has been reviewed by the owner.

## 8. Evidence standard

Use these labels in PR/commit notes, extraction ledger and architecture discussions:

| Label | Meaning |
|---|---|
| `OBSERVED` | Directly seen in working OpsMate behaviour, code or test result |
| `INFERRED` | Reasonable conclusion needing confirmation |
| `CANDIDATE` | Proposed direction, not yet a decision |
| `TESTED` | Reproduced by a defined test/harness |
| `LOCKED` | Owner-approved decision recorded in ZASS |

AI consensus is not evidence. Disagreement becomes a question, experiment, trade-off or candidate decision.

## 9. Minimum handover for every meaningful change

Record concisely:

- **What changed**
- **Why**
- **Tests run and result**
- **Known risk or uncertainty**
- **Next owner decision**, if any

That makes the project understandable by the owner, a future contributor and the public—without relying on chat memory.
