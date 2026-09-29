# ZASS — Kerani_Core_SuperBasic

**ZASS baseline:** v0.3.2  
**Project status:** DECIDING — first extraction evidence recorded  
**Owner:** Project Owner  
**Updated:** 2026-09-29  
**Repository:** dzuddiyn/Kerani_Core_SuperBasic  
**Project Source of Truth:** this file  
**Method baseline:** https://github.com/dzuddiyn/ZASS-Zero-to-Architecture-Structured-Sprint/blob/main/ZASS.md

> **Motto:** **Genericity is Generosity.**
>
> We earn genericity through evidence and reuse, then share the useful stack openly so small teams can build on proven work instead of rebuilding it alone.

This project follows the operating semantics of **ZASS v0.3.2**:

1. **Bukan potong fikir; potong ulang fikir.**
2. **Fikir bebas. Rekod keputusan. Kunci yang pasti. Bina dari yang terkunci.**
3. **AI menghasilkan kemungkinan. Evidence menguji. Manusia memutuskan. Architecture mematuhi keputusan.**

If this project file and the official ZASS baseline differ, use:
- this file for **project facts, questions, risks, candidates, decisions, evidence and readiness**;
- the official ZASS v0.3.2 baseline for **workflow/command semantics**.

Only the project owner may make a decision **LOCKED**. A suggestion, AI output, model agreement, experiment PASS, or implementation detail is not automatically a decision.

---

# 0. AI OPERATING RULES

AI may:
- generate ideas and alternatives;
- challenge assumptions;
- identify risks;
- propose experiments;
- map OpsMate evidence;
- compare architecture candidates;
- propose candidate decisions;
- update this file when authorised.

AI may NOT:
- silently change a LOCKED decision;
- invent requirements or evidence;
- treat multi-model agreement as evidence;
- confuse implementation with contract;
- promote ACTION PLAN execution state into a decision;
- generate confirmed architecture while critical decisions remain unresolved;
- override the project owner.

Decision states:

**RAW → CANDIDATE → TESTING → DECIDED → LOCKED**

Other states:

**REJECTED · DEFERRED · SUPERSEDED**

Project execution state, if ACTION_PLAN.md is later created, must use the separate ACTION PLAN states from ZASS v0.3.2 and must not become a second decision ledger.

---

# 1. RAW IDEA

## Original Idea

After relevant OpsMate BSE behaviour and regression tests become stable, inspect the working implementation and extract only the parts that are genuinely reusable for small conversational applications:

**Telegram → Apps Script → AI → data/workspace → response**

The result must come from a tested system, not an imagined framework.

## Why I Want This

- Avoid rebuilding useful infrastructure for every future application.
- Preserve lessons already paid for through real OpsMate bugs, tests and operating experience.
- Separate reusable infrastructure from farm/BSE-specific logic.
- Create a small, understandable foundation that a single maintainer can own.
- Share a proven and safe stack openly when publication requirements are satisfied.

## Provenance

The statements above are inherited from the existing project SoT. They are project context, not new evidence created by this migration.

---

# 2. GOALS

1. Identify which OpsMate components are genuinely reusable.
2. Extract reusable behaviour without farm, BSE, plot, inventory, claim or SME assumptions.
3. Preserve proven behaviour through regression tests and explicit contracts.
4. Define a small configuration/extension contract.
5. Prove the core can run with a non-farm module.
6. Build one independent second application or module composition that demonstrates reuse.
7. Reproduce selected OpsMate behaviour using the new composition.
8. Publish the stack openly only when security, redaction, documentation and licensing are ready.
9. Keep future domain applications as consumers of the core rather than allowing them to silently redefine it.

---

# 3. NON-GOALS

- Building Kerani Core SME in this repository.
- Replacing or redesigning OpsMate while the relevant behaviour is still unstable.
- Building a farm-management system inside the generic core.
- Treating BSE configuration as the generic schema.
- Home Assistant, local LLM, workstation, remote-desktop or hardware work.
- A fully autonomous agent with unrestricted access to business systems.
- A broad platform designed from speculation.
- Locking a final architecture before extraction evidence exists.

---

# 4. CONSTRAINTS

## Budget / Operating Model

- Prefer a small, maintainable stack suitable for a single maintainer.
- Avoid abstraction that is not justified by at least two demonstrated uses.

## Initial Runtime

- Google Apps Script.

## Initial Chat Interface

- Telegram.

## Initial AI Provider

- Gemini API.

These are initial implementation constraints, not proof that the final reusable contract must remain provider- or channel-specific.

## Security / Privacy

- Secrets must remain outside source control and public examples.
- TEST and production behaviour/data must remain isolated.
- A coding agent must not receive direct production Telegram credentials or unrestricted production-message access.
- Human/operator controls TEST injection and live deployment boundaries.
- Open-source publication requires security review, redacted examples and an explicit licence.

## Domain Boundary

- Domain logic belongs in an application/module layer, not silently inside the generic core.

## Evidence Constraint

- Genericity must be demonstrated through stable behaviour, extraction and reuse.
- No component becomes generic merely because it sounds reusable.

---

# 5. IDEA BLAST

Nothing in this section is automatically approved.

| ID | Idea | Source | Status |
|---|---|---|---|
| I-001 | Extract a small generic conversational-app foundation from proven OpsMate behaviour. | Existing project SoT | RAW |
| I-002 | Separate generic core behaviour from agriculture-domain behaviour and BSE configuration. | Existing project SoT | RAW |
| I-003 | Use a tiny non-farm module as a proof that Core SuperBasic is genuinely generic. | Existing project SoT | RAW |
| I-004 | Publish the proven stack openly after security, redaction, documentation and licensing review. | Existing project SoT | RAW |

---

# 6. QUESTIONS / UNKNOWNS

| ID | Question | Why It Matters | Status |
|---|---|---|---|
| Q-001 | Which OpsMate files/functions implement genuinely reusable behaviour? | Defines extraction scope. | OPEN |
| Q-002 | What configuration contract can express a new application without editing core code? | Tests whether reuse is real. | OPEN |
| Q-003 | Which storage abstractions are necessary and which are over-abstraction? | Prevents speculative framework design. | OPEN |
| Q-004 | Which parts should intentionally remain Apps-Script-specific in v0.x? | Controls scope and portability claims. | OPEN |
| Q-005 | How should prompts, schemas and validation be separated from runtime core behaviour? | Protects provider/domain boundaries. | OPEN |
| Q-006 | What is the smallest meaningful second application for proof of reuse? | Required to earn genericity. | OPEN |
| Q-007 | What must be redacted or redesigned before public release? | Protects security and privacy. | OPEN |
| Q-008 | Does this repository deserve a permanent public name after reuse is demonstrated? | Naming must follow demonstrated function. | OPEN |
| Q-009 | Can a module be removed without damaging Core? | Tests module independence. | OPEN |
| Q-010 | Can Core run a non-agricultural module? | Tests genericity. | OPEN |
| Q-011 | Can Telegram be replaced without changing business logic? | Tests channel boundary. | OPEN |
| Q-012 | Can BSE configuration be replaced by another client/farm configuration? | Tests configuration/domain separation. | OPEN |
| Q-013 | Can parser or AI provider change behind the same behaviour contract? | Tests model/provider portability. | OPEN |
| Q-014 | Are raw messages, candidate records and authoritative records clearly distinct? | Protects auditability and state correctness. | OPEN |

---

# 7. RISKS & FAILURE SCENARIOS

| ID | Failure / Risk | Impact | Possible Mitigation | Status | 🚨 Early warning signal |
|---|---|---|---|---|---|
| R-001 | Premature abstraction | Core becomes speculative and difficult to maintain. | Extract only after stable OpsMate evidence. | OPEN | Interfaces appear before a second demonstrated use. |
| R-002 | Hidden OpsMate assumptions | Generic core fails outside BSE/OpsMate. | Behaviour map + reuse ledger + regression tests. | OPEN | BSE vocabulary or sheet-column assumptions appear in core contracts. |
| R-003 | Core becomes Kerani Core-specific | Reuse claim becomes false. | Keep domain code/config in consumer modules. | OPEN | Core requires agriculture concepts to run. |
| R-004 | Over-engineering | Cost and complexity exceed value. | Prefer smallest interface demonstrated by two uses. | OPEN | New abstractions exist with no evidence-backed consumer. |
| R-005 | Regression during extraction | Proven behaviour is lost. | Preserve/port relevant harness tests before refactor. | OPEN | New composition cannot reproduce a selected baseline test. |
| R-006 | Secret or private-data exposure | Unsafe public release. | No secret commits; redacted fixtures; publication review. | OPEN | Real token, chat ID or operational record appears in repo fixtures. |
| R-007 | Public stack is confusing or unsafe | Users deploy incorrect defaults or misunderstand scope. | Clear scope, examples, threat notes and versioning. | OPEN | Documentation implies production safety that has not been tested. |
| R-008 | Architectural drift | Implementation silently overrides project decisions. | This ZASS file remains authoritative; use change control. | OPEN | Code or docs contradict an L-xxx record. |

---

# 8. METHOD REVIEWS

## MR-001 — Evidence-led extraction review

**Method:** First principles + Maintainability + Minimal viable experiment  
**Scope:** OpsMate BSE → Kerani_Core_SuperBasic extraction strategy  
**Reviewer / Model:** AI-assisted project review  
**Date:** 2026-09-29

### Findings

- OpsMate should be treated as a **reference implementation and evidence source**, not as an architecture template.
- Audit should begin from observable behaviour, not source-file names.
- Behaviour contracts should be defined before implementation is copied.
- Generic infrastructure, agriculture-domain behaviour and BSE-specific configuration need separate classifications.
- A non-farm module is a stronger genericity test than renaming farm concepts.
- Equivalent tested behaviour is more important than identical source code.

### Contradictions

- The previous Section 16 used several **AC-xxx** IDs for process/evidence proposals, while ZASS v0.3.2 reserves **AC-xxx** for Architecture Candidates. This migration preserves traceability but moves the canonical records to D/E entries where appropriate.

### New Questions

- Q-009 through Q-014.

### New Risks

- Existing risks R-001 through R-008 are retained; no additional risk is promoted solely by this migration.

### Experiments Suggested

- E-001 through E-006.

### Candidate Decisions

- D-006 through D-009.

---

# 9. MULTI-AI REVIEW RULES

Agreement between AI models is not evidence.

Disagreement must be converted into a question, experiment, trade-off or candidate decision.

No significant multi-AI disagreement is currently recorded in this project SoT.

| ID | Topic | Model / Reviewer Views | What Must Be Resolved | Result |
|---|---|---|---|---|
| MA-001 | — | — | — | OPEN / unused |

---

# 10. OPTIONS

## Decision Topic — How to derive the reusable core

### Option A — Evidence-led extraction

**Description:** Freeze proven OpsMate behaviour, map observable workflows, classify reuse, define contracts, then implement and test a clean composition.

**Advantages:**
- grounded in working behaviour;
- preserves regression evidence;
- reduces hidden BSE assumptions;
- supports model/provider independence.

**Disadvantages:**
- slower than copying source directly;
- requires careful baseline and behaviour mapping.

**Risks:**
- can still over-generalise if evidence is weak.

**Evidence:**
- strategy review and existing OpsMate regression practice; full extraction proof is still pending.

### Option B — Direct refactor / rename of OpsMate

**Description:** Refactor the existing OpsMate structure directly into a reusable core.

**Advantages:**
- superficially faster;
- reuses existing source layout.

**Disadvantages:**
- likely carries hidden domain and implementation coupling;
- can mistake current Apps Script structure for intended architecture.

**Risks:**
- produces “OpsMate without BSE” rather than a genuinely reusable core.

**Decision state:** No new owner decision is created by this comparison. D-002 already locks the principle that genericity must be earned through extraction and reuse.

---

# 11. ARCHITECTURE CANDIDATES

Create AC entries only for genuine architecture arrangements.

## AC-005 — Candidate runtime/module boundary

**Status:** CANDIDATE  
**Origin:** legacy Section 16.6; retained as AC because it is an actual architecture boundary candidate.

**Summary:**

**Channel adapter → Client runtime → Durable inbox → Core SuperBasic → Module contract → Domain module/config**

**Key characteristics:**
- channel boundary before business logic;
- a durable intake boundary is proposed;
- Core performs generic orchestration;
- domain behaviour is supplied through a module contract;
- BSE becomes configuration/test data rather than the generic schema.

**Candidate Core responsibilities:**
- normalise;
- route;
- validate generic state/contract rules;
- dispatch modules;
- manage generic approval states where applicable;
- emit audit/events;
- produce safe responses.

**Dependencies:**
- behaviour evidence from OpsMate;
- contract definitions;
- a non-farm module test;
- storage/durable-inbox evidence.

**Advantages:**
- separates channel, runtime, core and domain concerns;
- supports testing genericity independently.

**Trade-offs:**
- Durable Inbox and approval semantics may be over-generalised and remain unproven.

**Critical risks:**
- R-001, R-002, R-003, R-004.

### Candidate Comparison

No second genuine architecture candidate has yet been recorded. Do not invent AC-002/AC-003 merely to fill a comparison table.

---

# 12. DECISION LEDGER

## D-001 — Repository purpose

**Status:** LOCKED

**Problem:** Prevent reusable infrastructure work from becoming mixed with the Kerani Core SME product domain.

**Options considered:** Generic extraction repository / Kerani Core SME repository.

**Decision:** This repository is an OpsMate-derived generic-core extraction, not Kerani Core SME.

**Reason:** Separate reusable infrastructure from the SME product domain.

**Trade-offs:** Requires later integration with domain modules rather than embedding them here.

**Evidence / experiment:** Existing project scope and owner-approved SoT.

**Related risks:** R-002, R-003.

---

## D-002 — Genericity principle

**Status:** LOCKED

**Decision:** Genericity is earned through extraction and reuse, not assumed during design.

**Reason:** Prevent speculative abstraction.

**Consequences:** UNCERTAIN behaviour remains in the reference implementation until evidence supports extraction.

**Revisit trigger:** Only owner-approved evidence showing this principle blocks necessary, demonstrated reuse.

---

## D-003 — Guiding motto

**Status:** LOCKED

**Decision:** The guiding motto is **“Genericity is Generosity.”**

**Reason:** A proven, safe stack should be shareable for others to build upon.

**Consequences:** Openness is a goal, not permission to broaden the core without evidence.

---

## D-004 — Public-release gate

**Status:** LOCKED

**Decision:** Public release happens only after security review, redaction, documentation and explicit licence.

**Reason:** Openness must not expose secrets, operational data or unsafe defaults.

**Related risks:** R-006, R-007.

---

## D-005 — Permanent project name

**Status:** DEFERRED

**Decision:** PENDING.

**Decision drivers:** Demonstrated function and reuse.

**Options considered:** Keep temporary name / rename after proof.

**Revisit trigger:** Reuse proof stage passes.

---

## D-006 — Freeze a reference baseline before extraction

**Status:** CANDIDATE  
**Migrated from:** legacy AC-001.

**Problem:** Later extraction needs a stable comparison point.

**Candidate decision:** Freeze a clean OpsMate checkpoint with tested workflows, regression tests, redacted sample inputs, expected outputs and known limitations before extracting relevant behaviour.

**Evidence / experiment:** E-001 and actual OpsMate regression evidence required.

**Decision:** PENDING.

---

## D-007 — Behaviour-first audit

**Status:** TESTING  
**Migrated from:** legacy AC-002.

**Candidate decision:** Audit observable workflows first, then locate the implementation that performs each stage.

**Reason:** Avoid copying Apps Script/BSE structure as architecture.

**Evidence / experiment:** E-001A mapped the Input Usage / Inventory workflow from observable behaviour to implementation locations using an OpsMate TEST snapshot.

**Decision:** PENDING.

---

## D-008 — Four-way reuse classification

**Status:** TESTING  
**Migrated from:** legacy AC-003.

**Candidate decision:** Classify extraction findings as **GENERIC**, **KEBUN-GENERIC**, **OPSMATE/BSE-SPECIFIC**, or **UNCERTAIN**.

**Reason:** Preserve a domain layer between generic core and client-specific configuration.

**Evidence / experiment:** E-001A showed that the four-way classification is useful when applied to behaviour-level stages; one source file can contain mixed generic, domain and BSE-specific concerns.

**Decision:** PENDING.

---

## D-009 — Contract before source code

**Status:** TESTING  
**Migrated from:** legacy AC-004.

**Candidate decision:** Define minimum input/output/state promises before copying implementation.

**Reason:** Behaviour contracts should survive changes in regex, deterministic parser, Gemini, GPT or future local models.

**Evidence / experiment:** E-001A exposed a candidate request → candidate → human decision → authoritative TEST domain result → response/event contract without requiring the current Apps Script implementation to become the contract.

**Decision:** PENDING.

---

# 13. LOCKED DECISIONS

This section is authoritative. Architecture and implementation must not contradict these records.

## L-001

**Source Decision:** D-001  
**Decision:** This repository is an OpsMate-derived generic-core extraction, not Kerani Core SME.  
**Locked by:** Project Owner  
**Date:** inherited from pre-v0.3.2 project SoT  
**Supersedes:** None

## L-002

**Source Decision:** D-002  
**Decision:** Genericity is earned through extraction and reuse, not assumed during design.  
**Locked by:** Project Owner  
**Date:** inherited from pre-v0.3.2 project SoT  
**Supersedes:** None

## L-003

**Source Decision:** D-003  
**Decision:** The guiding motto is “Genericity is Generosity.”  
**Locked by:** Project Owner  
**Date:** inherited from pre-v0.3.2 project SoT  
**Supersedes:** None

## L-004

**Source Decision:** D-004  
**Decision:** Public release requires security review, redaction, documentation and explicit licence.  
**Locked by:** Project Owner  
**Date:** inherited from pre-v0.3.2 project SoT  
**Supersedes:** None

---

# 14. REJECTED IDEAS

No project idea is newly marked REJECTED by this migration.

| ID | Idea | Reason Rejected | Related Decision |
|---|---|---|---|
| — | — | — | — |

---

# 15. DEFERRED ITEMS

| ID | Item | Why Deferred | Revisit Trigger |
|---|---|---|---|
| D-005 | Permanent project name | Function has not yet been proven through reuse. | Proof stage passes. |
| E-001 | Classify completed OpsMate components | Relevant OpsMate baseline must be stable first. | Stable reference checkpoint exists. |
| E-002 | Extract one candidate component | Classification and contract evidence are not ready. | E-001 produces an evidence-backed candidate. |
| E-003 | Assemble minimum generic workflow | Generic components have not yet been extracted. | E-002 passes. |
| E-004 | Build a second tiny application | Core reuse contract not yet proven. | E-003 passes. |
| E-005 | Public-release review | Stack is not yet proven or publication-ready. | Reuse proof is complete. |
| E-006 | OpsMate reproduction test | New composition does not yet exist. | Core + Kebun + BSE test config + adapter can be integrated. |

---

# 16. OPEN LOOPS

Architecture freeze is blocked by the following:

- [ ] Freeze a stable OpsMate reference checkpoint.
- [x] Map at least one complete observable OpsMate workflow. Behaviour Map #1 (Input Usage / Inventory) is recorded in E-001A.
- [ ] Populate the evidence-backed reuse matrix.
- [ ] Resolve whether Durable Inbox is a generic requirement or an OpsMate-specific implementation choice.
- [ ] Define minimum Core ↔ Module contract.
- [ ] Prove Core can run a non-farm module.
- [ ] Determine the boundary between generic validation and domain validation.
- [ ] Test parser/provider substitution behind a stable contract.
- [ ] Run the OpsMate reproduction test.
- [ ] Complete public-release safety review before any open release.
- [ ] Resolve or deliberately defer critical architecture questions before confirmation.

---

# 17. EXPERIMENTS / EVIDENCE

## E-001 — Classify completed OpsMate components

**Status:** DEFERRED

**Question being tested:** Can completed OpsMate behaviour be separated into evidence-backed reuse classes?

**Hypothesis:** Stable OpsMate behaviour will reveal components that can be classified without speculative abstraction.

**Method:** Freeze baseline, map behaviour, then build the extraction ledger.

**Success criteria:** Ledger contains evidence-backed classification and links to tests/behaviour.

**Result:** PENDING.

**Conclusion:** PENDING.

**Affected decisions:** D-006, D-007, D-008.

---

## E-001A — One Workflow Extraction Audit: Input Usage / Inventory

**Status:** PASS — workflow slice only; parent E-001 remains incomplete.  
**Date:** 2026-09-29  
**Source snapshot:** `BSE-dzuddiyn01gmail/BSE-OpsMate-TEST` main at commit `10e20cd601421bb114ff3bfd7edf9e3f5e8160c4`.

**Evidence files reviewed:**
- `docs/ARCHITECTURE.md`
- `docs/DEVELOPMENT_STATUS.md`
- `InventoryReviewTest.js`
- `TelegramWorkerTest.js`
- `TelegramQueueTest.js`
- `TelegramApprovalUiTest.js`
- `GeminiUnifiedTest.js`

**Question being tested:** Can one proven OpsMate workflow be mapped behaviour-first, classified without treating source-file structure as architecture, and expressed as an implementation-independent contract candidate?

**Input example:**

~~~text
PENGGUNAAN BAHAN
Item: Sarung tangan pakai buang
Kuantiti: 2 kotak
~~~

### Behaviour Map #1

| Stage | Observed behaviour | Current implementation evidence | Initial classification |
|---|---|---|---|
| 1 | Receive Telegram message | `receiveBseTelegramTest()` | `GENERIC` candidate — channel adapter |
| 2 | Persist raw request durably | `TELEGRAM_TEST_QUEUE` | `GENERIC` candidate |
| 3 | Recognise Input Usage / inventory meaning | `bseInventoryParseMessage_()` | `KEBUN-GENERIC` |
| 4 | Extract item, quantity and unit | inventory parser + quantity regressions | quantity parsing: `GENERIC` candidate; inventory semantics: `KEBUN-GENERIC` |
| 5 | Validate required fields, date and unit | `bseInventoryValidateResult_()` | generic validation pattern + domain rules |
| 6 | Persist candidate representation | worker `candidate_json` | `GENERIC` candidate |
| 7 | Route actionable PASS to human review | queue → `NEEDS_HUMAN_REVIEW` | `GENERIC` candidate |
| 8 | Send confirmation card as reply to original message | `bseTelegramApprovalEnsureCard_()` | `UNCERTAIN` — possible generic capability |
| 9 | Bind Benar / Betulkan / Buang to original reporter | reporter confirmation core | `UNCERTAIN` |
| 10 | Benar invokes domain writer boundary | `bseInventoryApprovalBoundaryCore_()` → `bseInventoryReviewCore_()` | `KEBUN-GENERIC` |
| 11 | Write approved TEST domain record | `TEST_INVENTORY_EVENT` | behaviour: `KEBUN-GENERIC`; Sheet/schema: `OPSMATE/BSE-SPECIFIC` |
| 12 | Write review/audit evidence | `TEST_INVENTORY_REVIEW` | audit concept: `GENERIC`; representation: `OPSMATE/BSE-SPECIFIC` |
| 13 | Move queue to terminal inventory TEST state | `INVENTORY_APPROVED_TEST` / reject counterpart | domain state |
| 14 | Close card and emit reporter/owner notification | Telegram approval UI | notification behaviour: generic candidate; transport: Telegram-specific |

### Observed state distinction

~~~text
RAW TELEGRAM MESSAGE
        ↓
durable queue
        ↓
parse / classify / validate
        ↓
candidate_json
        ↓
NEEDS_HUMAN_REVIEW
        ↓
human confirmation
        ↓
authoritative TEST domain record + audit
        ↓
terminal state + response/event
~~~

This provides early positive evidence for Q-014: the current workflow distinguishes the raw message, candidate state and authoritative TEST domain record. Q-014 remains OPEN until this separation is checked across additional workflows.

### Candidate contract exposed by the workflow

~~~text
REQUEST
- source reference
- actor/reporter
- channel context
- received_at
- original text

→ CANDIDATE
- intent/domain
- extracted fields
- validation state
- missing fields
- original evidence
- production boundary

→ HUMAN DECISION
- confirm
- correct
- discard

→ AUTHORITATIVE DOMAIN RESULT
- approved domain record
- audit record
- terminal state

→ RESPONSE / EVENT
~~~

This is a contract candidate only. It does not make Telegram, Apps Script, Google Sheets, the inventory parser, or the current approval UI part of the generic Core by default.

### Result

**Observed result:** PASS for this workflow slice. One real OpsMate workflow can be mapped behaviour-first and separated into generic candidates, domain behaviour, BSE-specific representation and uncertain boundaries.

**Learning:** Classification should be applied to small behaviours/contracts rather than whole files. A single OpsMate source file can mix generic mechanism, domain semantics and BSE-specific persistence.

**Uncertain boundary:** Human confirmation/approval appears reusable, but this experiment does not prove whether it belongs in Core, is an optional Core capability, or belongs to the application/module policy.

**Impact:** **PROCEED**.
- D-007 → `TESTING`
- D-008 → `TESTING`
- D-009 → `TESTING`
- D-006 remains `CANDIDATE`
- parent E-001 is **not PASS**; a complete evidence-backed component ledger still requires a frozen reference baseline and broader workflow coverage.

---

## E-002 — Extract one candidate component

**Status:** DEFERRED

**Question being tested:** Can one GENERIC candidate be extracted without breaking its proven behaviour?

**Success criteria:** Relevant OpsMate-derived regression tests pass against the extracted implementation.

**Result:** PENDING.

**Affected decisions:** D-009.

---

## E-003 — Assemble minimum generic workflow

**Status:** DEFERRED

**Question being tested:** Can Core SuperBasic execute a domain-neutral workflow?

**Success criteria:** TEST workflow runs without farm/BSE vocabulary, domain code forks or hidden client assumptions.

**Additional pass signal:** Core can run a non-farm dummy module such as Echo or Todo.

**Result:** PENDING.

**Affected architecture candidate:** AC-005.

---

## E-004 — Build a second tiny application

**Status:** DEFERRED

**Question being tested:** Is the extracted core reusable without a major rewrite?

**Success criteria:** A second application works through configuration/extension points.

**Result:** PENDING.

**Affected decisions:** D-002, D-009.

---

## E-005 — Public-release review

**Status:** DEFERRED

**Question being tested:** Is the stack safe and understandable enough to publish?

**Success criteria:** No secrets/private data; safe examples; documentation; threat notes; explicit licence.

**Result:** PENDING.

**Affected decision:** D-004.

---

## E-006 — OpsMate reproduction test

**Status:** DEFERRED  
**Migrated from:** legacy AC-006.

**Question being tested:** Can the new composition reproduce selected, documented OpsMate workflows?

**Proposed composition:**

**Kerani_Core_SuperBasic + Kerani_Kebun + BSE test configuration + Telegram adapter**

**Pass signal:** Selected OpsMate workflows pass the same behaviour contracts using the new composition.

**Failure signals:**
- Core cannot run a non-farm module.
- Removing a module damages Core.
- BSE-specific assumptions leak into Core.
- Changing channel/parser/provider requires business-logic rewrite.
- Raw messages are confused with authoritative records.

**Result:** PENDING.

**Affected architecture candidate:** AC-005.

---

# 18. ARCHITECTURE READINESS

ZERO → ARCHITECTURE measures readiness to form and confirm architecture. It is not coding progress.

| Criterion | Weight | Score | Contribution | Reason |
|---|---:|---:|---:|---|
| Purpose/problem clear | 10% | 1 | 10% | Extraction purpose is explicit. |
| Users/stakeholders and desired outcomes clear | 10% | 0.5 | 5% | Future small teams/maintainers are implied; primary consumer is not yet formally proven. |
| Scope and non-goals clear | 10% | 1 | 10% | Scope and exclusions are explicit. |
| Constraints and quality attributes known | 10% | 1 | 10% | Runtime, channel, provider, security and maintainability constraints are documented. |
| Options and trade-offs compared | 10% | 0.5 | 5% | Evidence-led extraction vs direct refactor is compared, but architecture alternatives are not yet tested. |
| Critical assumptions closed or have experiments | 15% | 0.5 | 7.5% | E-001A executed one workflow slice; major assumptions remain open. |
| Major risks addressed | 10% | 0.5 | 5% | Guardrails exist; evidence of effectiveness is pending. |
| Main system flows clear | 10% | 0.5 | 5% | Candidate flow is known and one OpsMate workflow has been mapped; broader flow evidence is still incomplete. |
| Major decisions LOCKED | 10% | 0.5 | 5% | Principles are locked; core boundary/build choices remain candidate. |
| No critical architecture blockers | 5% | 0 | 0% | Evidence baseline, contracts and reproduction proof are still missing. |

**ZERO → ARCHITECTURE score:** **62.5% → 63%**

**Status:** **DECIDING**

**Progress bar:** **[██████░░░░] 63% — DECIDING**

**Readiness gate:** **NOT READY**

Architecture blockers:
- no frozen reference evidence package;
- only one behaviour map is completed; broader reference-baseline and contract evidence remain incomplete;
- no validated Core ↔ Module contract;
- AC-005 is untested;
- no non-farm genericity proof;
- no reproduction-test result.

A DRAFT ARCH may be proposed only after readiness reaches at least 70%. Architecture confirmation requires the full ZASS v0.3.2 BUILD gate and the exact owner response **YA, CONFIRM ARCHITECTURE**.

---

# 19. ARCHITECTURE GENERATION INSTRUCTION

Current state: **NOT READY FOR CONFIRMED ARCHITECTURE**.

When readiness later becomes READY, architecture must be generated only from:
1. Goals
2. Constraints
3. LOCKED decisions
4. Required workflows
5. Known risks
6. Validated evidence
7. Explicitly accepted trade-offs

Any missing major decision must be returned as an **ARCHITECTURE BLOCKER**, not silently assumed.

---

# 20. CHANGE CONTROL

After architecture exists:

~~~
New idea
↓
CANDIDATE
↓
Impact analysis
↓
DECISION
↓
Human approval
↓
LOCK
↓
Architecture update
~~~

If a LOCKED decision must change:
1. create a new decision entry;
2. explain why the previous decision is no longer valid;
3. perform impact analysis;
4. mark the old decision SUPERSEDED;
5. LOCK the replacement decision;
6. update architecture only after the replacement is locked.

## v0.3.2 semantic migration note

The previous Section 16 used AC-001 through AC-006 for a mixture of process proposals, architecture boundary and test strategy. Under ZASS v0.3.2, AC means **Architecture Candidate** only.

Canonical migration:

| Legacy ID | Previous meaning | Canonical v0.3.2 record |
|---|---|---|
| AC-001 | Reference implementation baseline | D-006 (CANDIDATE) |
| AC-002 | Behaviour-first audit | D-007 (CANDIDATE) |
| AC-003 | Four-way reuse matrix | D-008 (CANDIDATE) |
| AC-004 | Contract before source code | D-009 (CANDIDATE) |
| AC-005 | Candidate runtime/module boundary | AC-005 retained |
| AC-006 | Reproduction test | E-006 |

This mapping preserves historical traceability and prevents future misuse of AC IDs.

---

# 21. RECOMMENDED PROJECT STRUCTURE

Before extraction, keep the repository deliberately small.

Current/near-term authority structure:

~~~
Kerani_Core_SuperBasic/
├── ZASS_Kerani_Core_SuperBasic.md    ← project SoT
├── docs/
│   └── DEV_WORKFLOW.md
└── README.md                         ← when/if present
~~~

When evidence justifies growth:

~~~
Kerani_Core_SuperBasic/
├── ZASS_Kerani_Core_SuperBasic.md
├── ACTION_PLAN.md                    ← optional; execution only
├── ARCHITECTURE.md                   ← only after architecture is built
├── README.md
├── src/
├── tests/
├── config/
└── docs/
    ├── DEV_WORKFLOW.md
    ├── EXTRACTION_LEDGER.md
    ├── adr/
    ├── experiments/
    └── reviews/
~~~

Do not create code, abstractions or folders merely to make the project look mature.

Authority hierarchy:

1. GitHub project ZASS file — project facts/decisions/readiness.
2. Official ZASS v0.3.2 — workflow semantics.
3. ACTION_PLAN.md — execution/progress only, if later created.
4. ARCHITECTURE.md — confirmed/draft architecture representation when applicable.
5. Local repository — working copy.
6. AI project workspace / memory / chat — context only.

---

# 22. STANDARD ZASS COMMANDS

This project inherits ZASS v0.3.2 command semantics.

- **ZASS / ZASS!!** — full structured exploration; do not change LOCKED decisions.
- **ZASS REVIEW** — challenge using a named method/perspective.
- **ACTION PLAN** — show/update execution state only; never LOCK a decision.
- **ZASS CHALLENGE** — attack assumptions, edge cases and contradictions.
- **ZASS DECIDE** — show unresolved candidate decisions and trade-offs.
- **PROCEED** — owner accepts the latest unopposed ZASS proposals; any proposal explicitly marked for LOCK becomes LOCKED. PROCEED does not commit or push.
- **COMMIT** — after approval, commit and push the approved project-file changes atomically and report the real commit SHA.
- **DRAFT ARCH** — prepare/revise a working architecture draft from authoritative state; does not confirm architecture.
- **BUILD ARCHITECTURE** — run the confirmation gate; if READY, request exact owner response **YA, CONFIRM ARCHITECTURE**.
- **ZASS AUDIT** — audit architecture against ZASS state.
- **ZASS IMPACT** — analyse impact before changing architecture.

When the user intentionally invokes ZASS or ZASS!!, check the project baseline against the latest official ZASS repository when access is available.

---

# APPENDIX A — CANDIDATE GENERIC SURFACE

This remains a candidate audit surface, not a build plan.

| Candidate surface | Evidence needed before extraction |
|---|---|
| Telegram adapter | Works without OpsMate-specific message or identity assumptions. |
| Apps Script runtime boundary | Portable deployment/configuration contract. |
| Gemini adapter | Domain-neutral prompt/input/output boundary and safe error handling. |
| Request pipeline | Reusable stages that do not encode farm or SME workflow. |
| Queue and worker | Generic state transitions and retry/review semantics. |
| Parser/normaliser | Input contract independent of an OpsMate record type. |
| Reply engine | Deterministic response contract and safe fallback replies. |
| Logging/evidence | Generic event schema with protected-data rules. |
| Configuration/secrets boundary | No credentials in source; app-specific settings separated. |
| Test harness | Reproducible tests without live Telegram production traffic. |

---

# APPENDIX B — EVIDENCE-LED EXTRACTION ROUTE

**State:** CANDIDATE strategy; not a final architecture.

Do not refactor OpsMate directly into Kerani. Treat OpsMate BSE as a proven reference implementation and test the route:

**OpsMate BSE → evidence baseline → actual behaviour map → reuse matrix → contracts → Core SuperBasic → Kebun module → integration → reproduction test**

Target:

**proven behaviour → contracts → boundaries → tests → architecture → clean implementation**

## Four-way reuse matrix

| Classification | Meaning | Typical destination |
|---|---|---|
| GENERIC | Meaningful without farm/business domain. | Core candidate |
| KEBUN-GENERIC | Reusable agriculture-domain behaviour, not generic infrastructure. | Kerani Kebun candidate |
| OPSMATE/BSE-SPECIFIC | Tied to BSE/site/plot convention/columns/history. | Config, reproduction fixture or PARK |
| UNCERTAIN | Evidence is insufficient. | Remain in reference implementation; create Q/R/E |

Quick heuristic: if removing the word **kebun** leaves the function meaningful, it may be a Core candidate. If its meaning depends on agriculture but not BSE, it may be a Kebun candidate. This heuristic does not replace evidence.

## Contract questions

For every extraction candidate, define:
- accepted input and context;
- normalised/candidate output;
- validation/confidence/failure states;
- authority transition and required human approval;
- reply/audit event;
- behaviour tests that must remain stable.

## Candidate delivery sequence

This sequence is a candidate plan, not a LOCKED decision:

1. Freeze reference baseline.
2. Map actual behaviour.
3. Build reuse matrix.
4. Define behaviour contracts.
5. Extract and test Core SuperBasic alone.
6. Build Kerani Kebun from KEBUN-GENERIC findings.
7. Integrate Core + Kebun + BSE test configuration + adapter.
8. Run E-006 OpsMate reproduction test.
9. Run ZASS review before any architecture boundary becomes DECIDED or LOCKED.

---

# DEFINITION OF DONE — PROOF STAGE

**OpsMate behaviour complete/stable enough for selected scope**  
→ **components classified with evidence**  
→ **generic components extracted**  
→ **relevant regression tests pass**  
→ **Core runs a non-farm module**  
→ **second independent use works**  
→ **no major core rewrite is required for reuse**  
→ **selected OpsMate behaviour is reproduced by the new composition**  
→ **public-release safety review passes**  
→ **generic core is proven enough to name/version publicly**

Until then, this remains an extraction proof project, not a framework claim.

---

# PROJECT ZASS CHANGELOG

## 2026-09-29 — Behaviour Map #1 / E-001A

- Recorded the first evidence-backed workflow map using OpsMate TEST commit `10e20cd601421bb114ff3bfd7edf9e3f5e8160c4`.
- Added E-001A for Input Usage / Inventory.
- Moved D-007, D-008 and D-009 from `CANDIDATE` to `TESTING`.
- Kept D-006 as `CANDIDATE` and parent E-001 incomplete.
- Updated open loops and readiness wording; ZERO → ARCHITECTURE remains 63% because one workflow slice does not close the major architecture blockers.
- No LOCKED decision changed.

---

# CURRENT ZASS FOOTER STATE

[🧠 ZASS!!] -- [▶️ PROCEED] -- [🔄 PIVOT] -- [🅿️ PARK] -- [📦 COMMIT]

🏗️ ZERO → ARCHITECTURE: [██████░░░░] 63% — DECIDING

✅ ZASS UP TO DATE — v0.3.2
