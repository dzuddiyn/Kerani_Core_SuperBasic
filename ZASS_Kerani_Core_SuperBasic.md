# ZASS — Kerani_Core_SuperBasic

**ZASS baseline:** v0.3.6  
**Project status:** DECIDING — evidence harvesting planned; substantive Core build parked  
**Owner:** Project Owner  
**Updated:** 2026-10-06  
**Repository:** dzuddiyn/Kerani_Core_SuperBasic  
**Project Source of Truth:** this file  
**Method baseline:** https://github.com/dzuddiyn/ZASS-Zero-to-Architecture-Structured-Sprint/blob/main/ZASS.md

> **Motto:** **Genericity is Generosity.**
>
> We earn genericity through evidence and reuse, then share the useful stack openly so small teams can build on proven work instead of rebuilding it alone.

This project follows the operating semantics of **ZASS v0.3.6**:

1. **Bukan potong fikir; potong ulang fikir.**
2. **Fikir bebas. Rekod keputusan. Kunci yang pasti. Bina dari yang terkunci.**
3. **AI menghasilkan kemungkinan. Evidence menguji. Manusia memutuskan. Architecture mematuhi keputusan.**
4. **Tangkap luas, tumpu dengan sengaja:** bentuk candidate dahulu, kemudian research hanya soalan yang boleh mengubah pilihan; silang evidence, LOCK keputusan, dan biarkan architecture muncul daripada keputusan itu.

If this project file and the official ZASS baseline differ, use:
- this file for **project facts, questions, risks, candidates, decisions, evidence and readiness**;
- the official ZASS v0.3.6 baseline for **workflow/command semantics**.

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

Project execution state in ACTION_PLAN.md must use the separate ACTION PLAN states from ZASS v0.3.6 and must not become a second decision ledger.

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
10. Keep the SuperBasic core useful for micro-SME operations through five generic record families: **Purchase, Sale, Inventory, Observation and Task**, with receipt capture as an input capability.
11. Demonstrate the generic core across exactly three planned domain modules: **Agro, Servis Teknikal, and Makanan & Tempahan**.
12. Keep full natural-language conversation outside SuperBasic as a premium Kerani AI capability so basic operation does not depend on premium model usage.
13. Support **minimum constrained natural-language intake** in SuperBasic so users can type ordinary short operational sentences while preserving deterministic validation and human authority before any authoritative record is written.
14. Keep the free Core genuinely useful on its own: basic receipt capture, purchase/sale/inventory records, operational observations/notes, tasks, basic retrieval/reporting and summary of operational logs.
15. Monetise higher-value intelligence and domain automation through explicit Credit Pass / pay-per-capability rather than making a recurring subscription the primary access model.
16. Keep user business/operational data portable; paid value comes from convenience, domain intelligence, automation, traceability and ready-formatted outputs rather than artificial data lock-in.

---

# 3. NON-GOALS

- Building Kerani Core SME in this repository.
- Replacing or redesigning OpsMate while the relevant behaviour is still unstable.
- Building a farm-management system inside the generic core.
- Treating BSE configuration as the generic schema.
- Home Assistant, local LLM, workstation, remote-desktop or hardware work.
- A fully autonomous agent with unrestricted access to business systems.
- A broad platform designed from speculation.
- Additional domain modules beyond **Agro, Servis Teknikal, and Makanan & Tempahan** within the current SuperBasic scope.
- Full premium natural-language conversation as a mandatory SuperBasic capability; constrained natural-language intake for intent suggestion and candidate extraction remains in scope.
- Requiring a dedicated self-hosted server for the SuperBasic baseline.
- Locking a final architecture before extraction evidence exists.
- Artificially restricting export/access to user data in order to force purchase of premium intelligence.
- Making recurring subscription the primary monetisation requirement for current SuperBasic scope.

---

# 4. CONSTRAINTS

## Budget / Operating Model

- Prefer a small, maintainable stack suitable for a single maintainer.
- Avoid abstraction that is not justified by at least two demonstrated uses.
- Control paid AI/API-credit usage; ordinary SuperBasic record operations must not require premium conversational processing.
- Minimum natural-language intake should use the smallest practical model/prompt path and must fall back to clarification rather than consume extra reasoning to guess intent.
- Keep the Apps Script implementation modular enough that new domain behaviour does not collapse into special-case branching or spaghetti code.
- Free/basic capability and metered/premium capability must be distinguishable by capability/entitlement policy rather than scattered feature-specific conditionals.
- Premium capability must disclose its credit cost before execution when a charge applies.
- Failed provider/system execution must not be treated as a successfully consumed paid service.

## Initial Runtime

- Google Apps Script.
- The SuperBasic baseline does not require a dedicated self-hosted server.

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
- The planned domain-module set is intentionally limited to **Agro**, **Servis Teknikal**, and **Makanan & Tempahan**.
- **Agro** covers agriculture broadly, including crops/planting, aquaculture/fish and livestock/poultry; it replaces the narrower project term “Kebun” for the reusable domain layer.
- **Servis Teknikal** covers small technical-service operations such as workshop/repair, domestic electrical wiring, computers, air-conditioning and similar technician jobs.
- **Makanan & Tempahan** covers food stalls/warung/burger operations together with small bakery, made-to-order food and small catering.
- Additional modules are outside the current SuperBasic scope unless the owner later creates a new explicit decision.
- Natural-language interpretation may suggest routing into Core or a domain module, but the target module's deterministic guard/validator remains authoritative for fields and business rules.

## Evidence Constraint

- Genericity must be demonstrated through stable behaviour, extraction and reuse.
- No component becomes generic merely because it sounds reusable.
- OpsMate remains the primary reference implementation for harvesting reusable mechanisms and Agro-domain operational lessons.
- BSE/OpsMate-specific assumptions must not be promoted into the generic Core merely because they are already implemented.

## Near-Term Execution Constraint — October 2026

- Target **10 October 2026** to freeze a stable OpsMate reference baseline for extraction evidence.
- Pilot observations after the freeze should be captured as bug, gap and requirement evidence; they do not automatically reopen or expand the frozen reference scope.
- From **10–15 October 2026**, the priority for this repository is evidence harvesting and minimal skeleton preparation, not substantive Core implementation.
- The evidence-harvesting window should maximise learning from the frozen OpsMate reference through behaviour maps, pilot findings, reuse classification and candidate contracts.
- After the 15 October review, substantive Kerani_Core_SuperBasic implementation is **PARKED** until the owner explicitly restarts the build with suitable local agentic-coding resources.
- Critical safety, integrity or reference-invalidating defects may justify revisiting the freeze; ordinary pilot improvements should remain recorded evidence rather than causing uncontrolled scope churn.

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
| Q-014 | Are raw messages, candidate records and authoritative records clearly distinct? | Protects auditability and state correctness. | OPEN — early positive evidence from E-001A/E-001B |
| Q-015 | Which layer owns routing between direct/read requests and stateful/mutation workflows? | Prevents transport, runtime and domain routing responsibilities from collapsing into one layer. | OPEN |
| Q-016 | Which classes of request require a Durable Inbox, and which should bypass it? | Prevents forcing every request through durable queue infrastructure. | OPEN |
| Q-017 | Is human confirmation a mandatory Core responsibility, an optional Core capability, or application/module policy? | Prevents approval workflow from being over-generalised into Core. | OPEN |

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
| R-009 | Linear pipeline over-generalisation | Read/query requests are forced through queue, AI or human approval even when unnecessary. | Classify request behaviour before selecting an execution path; test direct/read and stateful/mutation paths separately. | OPEN | Commands such as report/history/lookup/status begin requiring LLM or approval without evidence that they need it. |
| R-010 | Overconfident natural-language routing | AI guesses an intent/category or fields and causes the wrong record type or wrong business meaning to reach persistence. | AI may only suggest intent/candidate; low/ambiguous confidence must trigger clarification; require human confirmation and deterministic domain validation before authoritative write. | OPEN | Ambiguous free text is silently converted into a saved record or a domain writer receives unconfirmed/unvalidated AI output. |

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

Evidence now suggests that the runtime/module boundary may require more than one interaction path rather than one universal linear pipeline:

~~~text
Channel Adapter
      ↓
Request Router
      │
      ├── Direct / Read Path
      │       ↓
      │   controlled handler
      │
      └── Stateful / Mutation Path
              ↓
         Durable Inbox
              ↓
          Core Pipeline
              ↓
        Module Contract
              ↓
         Domain Module
~~~

**Key characteristics:**
- channel boundary before business logic;
- constrained free-text mutation requests may pass through an intent-suggestion/candidate stage before module dispatch, but D-015 does not by itself LOCK where that router is implemented;
- request routing is explicit and its ownership remains unresolved (Q-015);
- Durable Inbox appears relevant to stateful/mutation workflows but is not yet proven as universal (Q-016);
- Core performs generic orchestration;
- domain behaviour is supplied through a module contract;
- human confirmation may be mandatory, optional, or application/module policy and remains unresolved (Q-017);
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
- Request routing may itself become over-generalised if ownership is assigned too early.
- Durable Inbox and approval semantics may be over-generalised and remain unproven.

**Critical risks:**
- R-001, R-002, R-003, R-004, R-009.

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

**Evidence / experiment:** E-001A mapped the Input Usage / Inventory workflow from observable behaviour to implementation locations using an OpsMate TEST snapshot. E-001B then verified the actual worker runtime and corrected the map where it had mistaken a regression parser for the primary runtime parser.

**Decision:** PENDING.

---

## D-008 — Four-way reuse classification

**Status:** TESTING  
**Migrated from:** legacy AC-003.

**Candidate decision:** Classify extraction findings as **GENERIC**, **AGRO-GENERIC**, **OPSMATE/BSE-SPECIFIC**, or **UNCERTAIN**.

**Reason:** Preserve a domain layer between generic core and client-specific configuration.

**Evidence / experiment:** E-001A showed that the four-way classification is useful when applied to behaviour-level stages; one source file can contain mixed generic, domain and BSE-specific concerns. E-001B reinforced that classification should target responsibilities such as extract → guard → validate rather than assuming a particular parser implementation is generic.

**Decision:** PENDING.

---

## D-009 — Contract before source code

**Status:** TESTING  
**Migrated from:** legacy AC-004.

**Candidate decision:** Define minimum input/output/state promises before copying implementation.

**Reason:** Behaviour contracts should survive changes in regex, deterministic parser, Gemini, GPT or future local models.

**Evidence / experiment:** E-001A exposed a candidate request → candidate → human decision → authoritative TEST domain result → response/event contract without requiring the current Apps Script implementation to become the contract. E-001B strengthened this by separating AI extraction, deterministic guard and domain validation as distinct responsibilities.

**Decision:** PENDING.

---

## D-010 — SuperBasic core product scope

**Status:** LOCKED  
**Owner approval:** 2026-10-01

**Decision:** Kerani_Core_SuperBasic is a deliberately small generic micro-SME core centred on **Purchase, Sale, Inventory, Observation and Task** records. Receipt scanning/capture is an input capability that produces a reviewable structured record; it is not a separate business domain.

**Operating boundary:** The baseline must remain useful without a dedicated self-hosted server and without premium natural-language processing.

**Reason:** Keep the core small, understandable, low-cost and broadly useful across micro-SME operations.

**Consequences:** Domain-specific schemas and workflows belong in modules; premium conversational AI must not become a dependency of basic record keeping.

---

## D-011 — Planned domain-module set

**Status:** LOCKED  
**Owner approval:** 2026-10-01

**Decision:** The current SuperBasic product scope contains exactly three planned domain modules:

1. **Agro** — crops/planting, aquaculture/fish, livestock/poultry and related small agricultural operations.
2. **Servis Teknikal** — workshop/repair, domestic wiring, computers, air-conditioning, machinery and related technician services.
3. **Makanan & Tempahan** — stalls/warung/burger businesses, small bakery, made-to-order food and small catering.

**Reason:** These three represent materially different, common micro-SME operating patterns while remaining small enough to test genericity without turning the project into a large platform.

**Consequences:** “Kebun” is replaced by **Agro** as the reusable agriculture-domain name.

---

## D-012 — Module simplicity and stop rule

**Status:** LOCKED  
**Owner approval:** 2026-10-01

**Decision:** Do not add further domain modules to the current SuperBasic scope after Agro, Servis Teknikal and Makanan & Tempahan. Each module must remain separable and simple enough that the Apps Script codebase does not degrade into special-case branching or spaghetti code.

**Early warning signal:** Repeated module-name conditionals, duplicated pipelines, or cross-module dependencies begin appearing in Core.

**Consequence:** A future domain that requires substantial special handling should become a separate application/project or require a new owner decision rather than being forced into SuperBasic.

---

## D-013 — Premium natural-language boundary

**Status:** LOCKED  
**Owner approval:** 2026-10-01

**Decision:** Full, natural conversational interaction belongs to **Kerani AI Premium**, not Kerani_Core_SuperBasic. The premium layer may use OpenAI and paid API/subscription credits; SuperBasic must remain functional without this premium capability.

**Reason:** Protect basic affordability and allow explicit control of paid AI-credit consumption.

**Consequences:** SuperBasic may use constrained extraction/OCR/AI where justified, but rich open-ended conversation is a separate premium product capability.

---

## D-014 — OpsMate extraction role

**Status:** LOCKED  
**Owner approval:** 2026-10-01

**Decision:** Continue extracting as much proven, reusable learning as practical from OpsMate. Reusable mechanisms feed Core candidates; agriculture-operational behaviour feeds the **Agro** module; BSE-specific assumptions remain reference/configuration evidence rather than Core behaviour.

**Reason:** OpsMate contains working behaviour already paid for through implementation, regression tests and pilot use.

**Consequences:** Evidence harvesting remains behaviour-first and contract-first; source files are not copied wholesale as architecture.

---

## D-015 — Minimum constrained natural-language intake

**Status:** LOCKED  
**Owner approval:** 2026-10-01

**Decision:** Kerani_Core_SuperBasic supports a **minimum constrained natural-language intake** for short operational free text. AI is allowed to:
1. suggest the user's likely intent/category;
2. extract a structured candidate;
3. provide a confidence/ambiguity signal.

AI is **not** allowed to decide or persist the authoritative record by itself.

**Required behaviour:**

~~~text
FREE TEXT
   ↓
INTENT SUGGESTION
   ↓
candidate category + confidence
   │
   ├── sufficiently clear
   │       ↓
   │   candidate preview
   │
   └── ambiguous / low confidence
           ↓
      ask category / clarification
           ↓
      candidate preview
           ↓
 [Benar] [Betulkan] [Buang]
           ↓
 deterministic domain guard / validator
           ↓
 authoritative structured record
~~~

**Safety rule:** Low or ambiguous confidence produces a question, not an AI guess.

**Authority rule:** Human confirmation and deterministic domain validation are mandatory before an AI-interpreted mutation becomes authoritative.

**Two-stage interpretation:** Prefer a small intent-routing step (“what is the user trying to do?”) followed by the relevant Core/domain parser (“what fields are required?”), instead of one monolithic prompt that attempts every domain simultaneously.

**Premium boundary:** This does not change D-013. Open-ended conversation, long-context reasoning and rich assistant behaviour remain Kerani AI Premium.

**Reason:** Give SuperBasic practical natural-language convenience without allowing probabilistic interpretation to silently corrupt business records or inflate premium AI-credit usage.

**Related risk:** R-010.

---

## D-016 — Free Core and premium intelligence boundary

**Status:** LOCKED  
**Owner approval:** 2026-10-06

**Decision:** Kerani_Core_SuperBasic must remain a genuinely useful free product. The free baseline includes:
- basic receipt capture/extraction where available;
- Purchase, Sale and basic Inventory records;
- Observation / operational note capture;
- Task;
- basic record retrieval and basic business reports;
- summary/retrieval of operational logs.

Free Core may summarize what is already recorded, but it does **not** need to perform higher-order correlation, causality, forecasting or domain intelligence across business and operational data.

When a user requests a capability outside the free boundary, the product must respond explicitly that the requested analysis/automation is a premium capability and offer the relevant paid action; it must not silently fail, hang, or return a generic error merely because the feature is gated.

**Premium candidates include:** forecasting, cross-data intelligence, deeper domain analysis, advanced natural-language reasoning, government/domain document generation, and richer automation.

**Reason:** Keep the generic Core independently useful while making paid value come from additional intelligence and automation rather than from basic access to the user's own records.

---

## D-017 — Credit Pass / pay-per-capability model

**Status:** LOCKED  
**Owner approval:** 2026-10-06

**Decision:** The current primary monetisation direction is **not a mandatory recurring subscription**. Paid capabilities are metered using **Credit Pass / pay-per-capability**.

Required rules:
- show the credit cost before executing a charged capability;
- allow domain modules to expose metered premium capabilities;
- a domain-module onboarding/allowance model may exist, but its exact commercial structure and quota values remain deferred;
- when included/free allowance is exhausted, additional usage may consume Credit Pass;
- a provider/system failure must not be recorded as a successfully delivered paid capability.

**Reason:** Align payment with actual higher-cost/higher-value usage, keep the free Core accessible, and retain flexibility across AI providers whose cost structures may change.

**Deferred:** exact credit prices, monthly allowances, onboarding cost and credit-to-currency economics.

---

## D-018 — Data portability and no artificial lock-in

**Status:** LOCKED  
**Owner approval:** 2026-10-06

**Decision:** Kerani must not depend on artificial data lock-in as its monetisation mechanism. Users may access/export their own stored data and may analyse it independently using ordinary tools or external AI applications.

**Paid value proposition:** convenience, structured workflow, domain contracts, forecasting/intelligence, automation, traceability, and ready-formatted outputs.

**Reason:** A technically capable user being able to export a file and analyse it elsewhere is acceptable; Kerani should win on workflow quality and domain capability rather than blocking access to user data.

---

## D-019 — Credit values and commercial calibration

**Status:** DEFERRED  
**Owner approval:** 2026-10-06

**Candidate examples discussed — NOT LOCKED pricing:**

| Capability | Candidate credit value |
|---|---:|
| Forecast / advanced analysis | 5 credits |
| Richer domain/service forecast or analysis | 10 credits |
| Domain/module onboarding | 100 credits |
| MyGAP-style report generation | 20 credits |

**Decision:** Exact credit values are not approved yet.

**Before pricing is locked, evaluate:** actual model/API cost, number of calls/retries, provider failure rate, document-generation cost, operational overhead, value to user, included allowance, and safety margin.

**Revisit trigger:** SuperBasic architecture is stable enough to identify capability boundaries and representative workloads can be costed/tested.

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

## L-005

**Source Decision:** D-010  
**Decision:** SuperBasic is a small generic micro-SME core for Purchase, Sale, Inventory, Observation and Task, with receipt capture as an input capability; no dedicated self-hosted server or premium natural-language processing is required for baseline operation.  
**Locked by:** Project Owner  
**Date:** 2026-10-01  
**Supersedes:** None

## L-006

**Source Decision:** D-011  
**Decision:** The planned domain-module set is exactly Agro, Servis Teknikal and Makanan & Tempahan; Agro replaces the narrower reusable-domain name Kebun.  
**Locked by:** Project Owner  
**Date:** 2026-10-01  
**Supersedes:** None

## L-007

**Source Decision:** D-012  
**Decision:** No additional domain modules are in the current SuperBasic scope; modules must remain simple and separable enough to avoid Apps Script spaghetti.  
**Locked by:** Project Owner  
**Date:** 2026-10-01  
**Supersedes:** None

## L-008

**Source Decision:** D-013  
**Decision:** Full natural-language conversation belongs to Kerani AI Premium using paid AI/API capability; SuperBasic must remain usable without it.  
**Locked by:** Project Owner  
**Date:** 2026-10-01  
**Supersedes:** None

## L-009

**Source Decision:** D-014  
**Decision:** OpsMate remains the primary evidence source: reusable mechanisms feed Core, agriculture behaviour feeds Agro, and BSE-specific assumptions do not become generic Core behaviour.  
**Locked by:** Project Owner  
**Date:** 2026-10-01  
**Supersedes:** None

## L-010

**Source Decision:** D-015  
**Decision:** SuperBasic includes constrained natural-language intake using intent suggestion + candidate extraction + confidence, with clarification for ambiguity, explicit human confirmation and deterministic domain validation before any authoritative AI-interpreted write.  
**Locked by:** Project Owner  
**Date:** 2026-10-01  
**Supersedes:** None; clarifies the boundary in D-013/L-008.

## L-011

**Source Decision:** D-016  
**Decision:** Free Core remains independently useful for basic records, receipt capture where available, retrieval/basic reporting and operational-log summary; higher-order correlation, forecasting, domain intelligence and advanced automation may be premium, and gated requests must be explained explicitly rather than silently failing.  
**Locked by:** Project Owner  
**Date:** 2026-10-06  
**Supersedes:** None

## L-012

**Source Decision:** D-017  
**Decision:** The primary paid model is Credit Pass / pay-per-capability rather than mandatory recurring subscription; charged capability cost is shown before execution, and failed delivery is not treated as a successful paid service.  
**Locked by:** Project Owner  
**Date:** 2026-10-06  
**Supersedes:** None

## L-013

**Source Decision:** D-018  
**Decision:** User data remains accessible/exportable; Kerani does not use artificial data lock-in to force premium purchase. Paid value comes from workflow, domain intelligence, automation, traceability and ready-formatted outputs.  
**Locked by:** Project Owner  
**Date:** 2026-10-06  
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
| E-006 | OpsMate reproduction test | New composition does not yet exist. | Core + Agro + BSE test config + adapter can be integrated. |
| D-019 | Exact Credit Pass values / commercial calibration | Unit economics and representative workloads are not yet validated. | Stable capability boundaries + measured provider/API costs and workload tests. |

---

# 16. OPEN LOOPS

Architecture freeze is blocked by the following:

- [ ] Freeze a stable OpsMate reference checkpoint.
- [x] Map at least one complete observable OpsMate workflow. Behaviour Map #1 (Input Usage / Inventory) is recorded in E-001A.
- [ ] Populate the evidence-backed reuse matrix.
- [ ] Resolve Q-015: ownership of routing between direct/read and stateful/mutation paths.
- [ ] Resolve Q-016: which request classes require Durable Inbox rather than treating it as universal.
- [ ] Resolve Q-017: whether human confirmation is Core-mandatory, optional capability, or module/application policy.
- [ ] Define minimum Core ↔ Module contract.
- [ ] Prove Core can run a non-farm module.
- [ ] Determine the boundary between generic validation and domain validation.
- [ ] Test parser/provider substitution behind a stable contract.
- [ ] Validate D-015 with clear, ambiguous and misrouted free-text cases: AI suggestion → clarification/preview → human confirmation → deterministic domain validation → authoritative record.
- [ ] Run the OpsMate reproduction test.
- [ ] Complete public-release safety review before any open release.
- [ ] Resolve or deliberately defer critical architecture questions before confirmation.
- [ ] After SuperBasic architecture is available, cross-audit it against the existing Kerani Core discussions/designs and adopt only capabilities that remain lightweight, generic and maintainable.
- [ ] Before locking Credit Pass prices, measure representative AI/OCR/document/forecast workloads and derive unit economics; do not infer prices from token cost alone.

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
| 3 | Interpret/extract a structured candidate from the queued report | `bseUnifiedProcess_()` using Gemini 3.1 Flash Lite | extraction responsibility: `GENERIC` candidate; current Gemini implementation: implementation detail |
| 4 | Apply deterministic contract guard to model output | `bseUnifiedGuard_()` and domain-specific guard helpers | guard responsibility: `GENERIC` candidate; individual domain rules vary |
| 5 | Apply inventory-domain validation and canonicalisation | `bseInventoryValidateResult_()` | validation mechanism may be generic; inventory/date/unit semantics are `AGRO-GENERIC` / domain-specific |
| 6 | Persist candidate representation | worker `candidate_json` | `GENERIC` candidate |
| 7 | Route actionable PASS to human review | queue → `NEEDS_HUMAN_REVIEW` | `GENERIC` candidate |
| 8 | Send confirmation card as reply to original message | `bseTelegramApprovalEnsureCard_()` | `UNCERTAIN` — possible generic capability |
| 9 | Bind Benar / Betulkan / Buang to original reporter | reporter confirmation core | `UNCERTAIN` |
| 10 | Benar invokes domain writer boundary | `bseInventoryApprovalBoundaryCore_()` → `bseInventoryReviewCore_()` | `AGRO-GENERIC` |
| 11 | Write approved TEST domain record | `TEST_INVENTORY_EVENT` | behaviour: `AGRO-GENERIC`; Sheet/schema: `OPSMATE/BSE-SPECIFIC` |
| 12 | Write review/audit evidence | `TEST_INVENTORY_REVIEW` | audit concept: `GENERIC`; representation: `OPSMATE/BSE-SPECIFIC` |
| 13 | Move queue to terminal inventory TEST state | `INVENTORY_APPROVED_TEST` / reject counterpart | domain state |
| 14 | Close card and emit reporter/owner notification | Telegram approval UI | notification behaviour: generic candidate; transport: Telegram-specific |

### Observed state distinction

~~~text
RAW TELEGRAM MESSAGE
        ↓
durable queue
        ↓
AI extraction
        ↓
deterministic guard
        ↓
domain validation
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

This provides early positive evidence for Q-014: the current workflow distinguishes the raw message, candidate state and authoritative TEST domain record. E-001B later strengthened this finding by showing that candidate representation can also differ from authoritative persistence representation. Q-014 remains OPEN until this separation is checked across additional workflow families.

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

**Learning:** Classification should be applied to small behaviours/contracts rather than whole files. A single OpsMate source file can mix generic mechanism, domain semantics and BSE-specific persistence. The initial map also over-associated the regression helper `bseInventoryParseMessage_()` with runtime parsing; E-001B corrected this and reinforced that source helpers must not be mistaken for runtime architecture.

**Uncertain boundary:** Human confirmation/approval appears reusable, but this experiment does not prove whether it belongs in Core, is an optional Core capability, or belongs to the application/module policy.

**Impact:** **PROCEED**.
- D-007 → `TESTING`
- D-008 → `TESTING`
- D-009 → `TESTING`
- D-006 remains `CANDIDATE`
- parent E-001 is **not PASS**; a complete evidence-backed component ledger still requires a frozen reference baseline and broader workflow coverage.

---

## E-001B — Behaviour Map #1 Runtime Verification

**Status:** PASS — audit found and corrected a material mapping error.  
**Date:** 2026-09-29  
**Verified source:** `BSE-dzuddiyn01gmail/BSE-OpsMate-TEST` main at commit `a6b504aff254935023ea19d6a1ce90dff597deb2`.  
**Compared against E-001A snapshot:** `10e20cd601421bb114ff3bfd7edf9e3f5e8160c4`.

**Question being tested:** Does Behaviour Map #1 accurately describe the effective runtime path for Input Usage / Inventory?

### Result

The lower half of Behaviour Map #1 remains supported: durable queue, candidate state, human review, reporter confirmation, domain writer, authoritative TEST record, audit and response/notification.

A material error was found in the parser/runtime section. The ordinary Telegram worker does not primarily call `bseInventoryParseMessage_()`. The effective runtime path is:

~~~text
Telegram intake
→ request routing
→ TELEGRAM_TEST_QUEUE for report workflow
→ processBseTelegramTestQueue()
→ bseUnifiedProcess_()
→ Gemini extraction
→ bseUnifiedGuard_()
→ domain-specific guards
→ bseInventoryValidateResult_()
→ candidate_json
→ clarification / NEEDS_HUMAN_REVIEW
→ reporter confirmation
→ domain writer
→ authoritative TEST record + audit
→ response / notice
~~~

`bseInventoryParseMessage_()` remains useful deterministic logic and regression evidence, but this experiment does not treat it as the primary runtime parser.

### Additional source-derived findings

1. The current OpsMate intake now has direct command/retrieval branches such as report/history/record/plot retrieval before an ordinary report is queued.
2. Therefore not every request passes through the same queue → AI → approval path.
3. Candidate representation can differ from authoritative persistence representation. For example, an Input Usage candidate may be represented as `Input_Usage_Log` / `INPUT_USAGE`, while the inventory approval boundary persists the approved TEST domain result through the inventory event writer.
4. `TelegramApprovalUiTest.js` contains repeated function definitions from implementation history; the final effective definition wins in Apps Script/JavaScript. This is additional evidence that file-level copying is not a safe extraction method.
5. The user-facing reject/discard label changed from `Buang` to `Batal` in the current repo while the internal terminal state remains `DISCARDED_BY_REPORTER`; this is a UI wording change rather than a contract-level behaviour change.

### Learning

- **AI extraction ≠ deterministic guard ≠ domain validation.**
- The reusable candidate is the responsibility/contract boundary, not Gemini, regex or a specific parser function.
- **source file ≠ behaviour ≠ contract ≠ architecture**.
- The runtime may need at least two interaction families: a direct/read path and a stateful/mutation path.
- Durable Inbox and human approval should not be assumed to be universal.

### ZASS impact

- D-007 remains `TESTING` with stronger evidence.
- D-008 remains `TESTING` with stronger evidence.
- D-009 remains `TESTING` with stronger evidence.
- AC-005 remains `CANDIDATE` and is refined to include direct/read vs stateful/mutation paths.
- Q-014 remains OPEN but has stronger evidence.
- Add Q-015, Q-016 and Q-017.
- Add R-009.
- D-006 remains `CANDIDATE`.
- Parent E-001 remains incomplete.
- No decision becomes LOCKED.

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

**Kerani_Core_SuperBasic + Kerani_Agro + BSE test configuration + Telegram adapter**

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
| Critical assumptions closed or have experiments | 15% | 0.5 | 7.5% | E-001A and E-001B tested one workflow family and corrected the runtime map; major assumptions remain open. |
| Major risks addressed | 10% | 0.5 | 5% | Guardrails exist; evidence of effectiveness is pending. |
| Main system flows clear | 10% | 0.5 | 5% | One stateful workflow is mapped and a direct/read path is now observed, but ownership and broader cross-workflow evidence remain incomplete. |
| Major decisions LOCKED | 10% | 0.5 | 5% | Product scope, module limits and premium boundary are now locked; core runtime/module boundary choices remain candidate. |
| No critical architecture blockers | 5% | 0 | 0% | Evidence baseline, contracts and reproduction proof are still missing. |

**ZERO → ARCHITECTURE score:** **62.5% → 63%**

**Status:** **DECIDING**

**Progress bar:** **[██████░░░░] 63% — DECIDING**

**Readiness gate:** **NOT READY**

Architecture blockers:
- no frozen reference evidence package;
- one behaviour map is corrected and a second interaction family is observed, but broader reference-baseline and cross-workflow contract evidence remain incomplete;
- no validated Core ↔ Module contract;
- AC-005 is untested;
- no non-farm genericity proof;
- no reproduction-test result.

A DRAFT ARCH may be proposed only after readiness reaches at least 70%. Architecture confirmation requires the full ZASS v0.3.6 BUILD gate and the exact owner response **YA, CONFIRM ARCHITECTURE**.

## Evidence Confidence

**Evidence Confidence:** **LOW**

**Reason:** Direct OpsMate evidence exists for one mapped workflow family and its runtime verification, but the frozen reference package, broader workflow coverage, module-contract proof, non-Agro proof, constrained-NL edge-case validation and reproduction test are still incomplete. Product and monetisation boundaries are clearer, but Credit Pass unit economics and scale/provider behaviour are not yet empirically validated.

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

## v0.3.6 project semantic alignment note

The project baseline was aligned on 2026-10-01 from v0.3.2 to **v0.3.6**. Current project operation therefore also follows:
- the ZASS Convergence Loop principle;
- explicit `PROPOSED FOR PROCEED` approval sets;
- Architecture Readiness and qualitative Evidence Confidence as separate axes;
- the current Full-ZASS command surface `ZASS!! / PROCEED / PIVOT / COMMIT`; `PARKED` remains a state, not a Full-ZASS command.

Historical v0.3.2 migration notes above remain as provenance.

## ZASS SYSTEM UI/UX alignment — 2026-10-01

The official ZASS SYSTEM UI/UX contract is also active for this project. This is a presentation/product-surface alignment, not a new architecture decision and not a method-version bump.

**Applicable system rules:**
- **Present only the next meaningful human action.**
- Keep local ZASS tooling first-class; future AI-SYNC Web is a UX/automation/projection layer, not the authority layer.
- GitHub project files and Git history remain the engineering Source of Truth.
- Prefer progressive disclosure: hide internal IDs, full ledgers and validator codes during ordinary work unless review/audit requires them.
- Human-facing work should prefer a compact Project Pulse rather than exposing the whole lifecycle continuously.
- Contextual surfaces may include **Ready to Lock**, **Architecture Forming**, **Current Task**, **Delivered**, and escalation notice only when a human action is useful.
- ACTION_PLAN / ARCHITECTURE / TASKS may be projected into human-facing views, but the projections do not become authority.
- SAVE/sync status must be factual: authoritative persistence requires a real Git commit/receipt; generated Markdown alone is not SAVED.
- Future web presentation must reuse the same validator/core semantics rather than duplicate rule logic.
- Full ZASS remains an escalation/governance capability; no automatic migration or invented complexity score is permitted.

**Project-specific consequence:** ordinary chat/project updates should stay compact and action-oriented while preserving full lineage in the repository for review when needed.

---

# 21. RECOMMENDED PROJECT STRUCTURE

Before extraction, keep the repository deliberately small.

Current/near-term authority structure:

~~~
Kerani_Core_SuperBasic/
├── ZASS_Kerani_Core_SuperBasic.md    ← project SoT
├── ACTION_PLAN.md                    ← current execution plan only
├── docs/
│   └── DEV_WORKFLOW.md
└── README.md
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
2. Official ZASS v0.3.6 — workflow semantics.
3. ACTION_PLAN.md — current execution/progress plan only; it does not decide architecture.
4. ARCHITECTURE.md — confirmed/draft architecture representation when applicable.
5. Local repository — working copy.
6. AI project workspace / memory / chat — context only.

---

# 22. STANDARD ZASS COMMANDS

This project inherits ZASS v0.3.6 command semantics.

- **ZASS / ZASS!!** — full structured exploration; do not change LOCKED decisions.
- **ZASS REVIEW** — challenge using a named method/perspective.
- **ACTION PLAN** — show/update execution state only; never LOCK a decision.
- **ZASS CHALLENGE** — attack assumptions, edge cases and contradictions.
- **ZASS DECIDE** — show unresolved candidate decisions and trade-offs.
- **PROCEED** — approve exactly the explicit `PROPOSED FOR PROCEED` set shown in the latest ZASS mapping. Unlisted items are excluded; proposals marked for LOCK become LOCKED. PROCEED does not commit or push.
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

**OpsMate BSE → evidence baseline → actual behaviour map → reuse matrix → contracts → Core SuperBasic → Agro module → integration → reproduction test**

Target:

**proven behaviour → contracts → boundaries → tests → architecture → clean implementation**

## Four-way reuse matrix

| Classification | Meaning | Typical destination |
|---|---|---|
| GENERIC | Meaningful without farm/business domain. | Core candidate |
| AGRO-GENERIC | Reusable agriculture-domain behaviour across crops, aquaculture or livestock, not generic infrastructure. | Kerani Agro candidate |
| OPSMATE/BSE-SPECIFIC | Tied to BSE/site/plot convention/columns/history. | Config, reproduction fixture or PARK |
| UNCERTAIN | Evidence is insufficient. | Remain in reference implementation; create Q/R/E |

Quick heuristic: if removing the agriculture context leaves the behaviour meaningful, it may be a Core candidate. If its meaning depends on agriculture but not BSE, it may be an Agro candidate. This heuristic does not replace evidence.

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
6. Build Kerani Agro from AGRO-GENERIC findings.
7. Integrate Core + Agro + BSE test configuration + adapter.
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

## 2026-10-06 — Free Core + Credit Pass product model LOCK

- LOCKED D-016/L-011: Free Core must remain useful standalone for basic records, receipt capture where available, basic retrieval/reporting and operational-log summary; higher-order intelligence/forecasting/domain automation may be premium.
- LOCKED explicit premium-gate UX: gated requests must explain the premium capability rather than silently failing or returning an unrelated error.
- LOCKED D-017/L-012: primary paid direction is Credit Pass / pay-per-capability rather than mandatory recurring subscription; credit cost is shown before charged execution.
- LOCKED failed-delivery guardrail: provider/system failure is not treated as a successfully delivered paid capability.
- LOCKED D-018/L-013: user data stays accessible/exportable and artificial data lock-in is not the business model.
- DEFERRED D-019: exact values such as 5/10/20/100 credits, module allowance/onboarding pricing and credit economics require measured unit economics.
- Added a post-architecture dependency: cross-audit SuperBasic against prior Kerani Core work and adopt only lightweight/generic/maintainable capabilities.
- ZERO → ARCHITECTURE remains 63% and Evidence Confidence remains LOW; these product decisions do not substitute for runtime evidence.

## 2026-10-01 — ZASS SYSTEM UI/UX contract sync

- Synced the project with the official locked ZASS SYSTEM UI/UX contract without changing Full ZASS v0.3.6 method semantics.
- Adopted the primary UX rule: **Present only the next meaningful human action.**
- Added progressive-disclosure guidance, compact Project Pulse, contextual action cards, factual Git-backed SAVE receipts and artifact projection semantics.
- Recorded the system split: local first-class tooling remains independently usable while future AI-SYNC Web is the UX/automation/projection layer over the same authority.
- Kept GitHub as engineering Source of Truth and prohibited duplicate validator semantics in future web presentation.
- No LOCKED project decision, architecture candidate, readiness score or Evidence Confidence value changed.

## 2026-10-01 — Minimum constrained natural-language intake LOCK

- LOCKED D-015/L-010: SuperBasic includes minimum constrained natural-language intake.
- AI authority is limited to intent suggestion, candidate extraction and confidence/ambiguity signalling.
- Ambiguous or low-confidence input must trigger category selection/clarification rather than guessing.
- AI-interpreted mutations require candidate preview, explicit human confirmation and deterministic Core/domain validation before authoritative persistence.
- Preserved D-013/L-008: rich/open-ended natural-language conversation remains Kerani AI Premium.
- Added R-010 for overconfident natural-language routing.
- Refined AC-005 only as a candidate to acknowledge an intent-suggestion stage without locking router ownership.
- ZASS baseline remains v0.3.6; ZERO → ARCHITECTURE remains 63% and Evidence Confidence remains LOW because no new runtime validation evidence was added.

## 2026-10-01 — SuperBasic product scope LOCK + ZASS v0.3.6 alignment

- LOCKED D-010/L-005: five generic record families — Purchase, Sale, Inventory, Observation and Task — with receipt capture as an input capability and no dedicated self-hosted-server requirement.
- LOCKED D-011/L-006: exactly three planned domain modules — Agro, Servis Teknikal and Makanan & Tempahan; Agro replaces the narrower reusable-domain name Kebun.
- LOCKED D-012/L-007: no additional domain modules in current SuperBasic scope; module simplicity and anti-spaghetti are explicit stop rules.
- LOCKED D-013/L-008: full natural-language conversation is Kerani AI Premium and must not be required for basic SuperBasic operation.
- LOCKED D-014/L-009: OpsMate remains the primary evidence source; reusable mechanisms feed Core, agriculture behaviour feeds Agro, and BSE-specific assumptions remain outside generic Core.
- Updated the project method baseline from ZASS v0.3.2 to v0.3.6 semantics.
- Added Evidence Confidence = LOW while ZERO → ARCHITECTURE remains 63% — DECIDING.
- No architecture candidate was promoted or confirmed.

## 2026-09-29 — Near-term evidence-harvesting plan

- Approved a time-boxed execution plan around an OpsMate reference freeze targeted for 10 October 2026.
- Pilot outcomes are to be captured as bug/gap/requirement evidence rather than automatically expanding the frozen reference scope.
- Set 10–15 October 2026 as an evidence-harvesting window: freeze metadata, pilot findings, 3–5 behaviour maps, reuse matrix, candidate contracts and minimal repository skeleton preparation.
- Added `ACTION_PLAN.md` as the execution authority for this window.
- Substantive Kerani_Core_SuperBasic implementation is PARKED after the review until the owner explicitly restarts the build with suitable local agentic-coding resources.
- This planning change does not alter LOCKED decisions and does not increase ZERO → ARCHITECTURE readiness; it remains 63%.

## 2026-09-29 — Runtime verification / E-001B

- Verified Behaviour Map #1 against OpsMate TEST main at `a6b504aff254935023ea19d6a1ce90dff597deb2`.
- Corrected the runtime parser path: ordinary report processing uses `bseUnifiedProcess_()` → Gemini → `bseUnifiedGuard_()` → domain validation, not `bseInventoryParseMessage_()` as the primary worker parser.
- Added Q-015, Q-016 and Q-017.
- Added R-009 for linear-pipeline over-generalisation.
- Refined AC-005 to distinguish direct/read and stateful/mutation paths while keeping it `CANDIDATE`.
- Kept D-007, D-008 and D-009 at `TESTING`; no LOCKED decision changed.
- ZERO → ARCHITECTURE remains 63%.

## 2026-09-29 — Behaviour Map #1 / E-001A

- Recorded the first evidence-backed workflow map using OpsMate TEST commit `10e20cd601421bb114ff3bfd7edf9e3f5e8160c4`.
- Added E-001A for Input Usage / Inventory.
- Moved D-007, D-008 and D-009 from `CANDIDATE` to `TESTING`.
- Kept D-006 as `CANDIDATE` and parent E-001 incomplete.
- Updated open loops and readiness wording; ZERO → ARCHITECTURE remains 63% because one workflow slice does not close the major architecture blockers.
- No LOCKED decision changed.

---

# CURRENT ZASS FOOTER STATE

[🧠 ZASS!!] -- [▶️ PROCEED] -- [🔄 PIVOT] -- [📦 COMMIT]

🏗️ ZERO → ARCHITECTURE: [██████░░░░] 63% — DECIDING
🔬 EVIDENCE CONFIDENCE: LOW — direct OpsMate evidence exists, but broader workflow/module validation remains incomplete.

✅ ZASS UP TO DATE — v0.3.6
