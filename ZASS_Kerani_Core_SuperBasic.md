# ZASS — Temporary Generic Telegram–Apps Script–Gemini Core

> **Motto:** **Genericity is Generosity.**
>
> We earn genericity through evidence and reuse, then share the useful stack openly so small teams can build on proven work instead of rebuilding it alone.

## 0. Status

| Field | Current value |
|---|---|
| Repository | `Kerani_Core_SuperBasic` |
| Public identity | **Temporary — not LOCKED** |
| Current role | Landing zone for a generic-core extraction from OpsMate BSE |
| Source implementation | OpsMate BSE |
| Extraction timing | Only after the relevant OpsMate behaviour and regression tests are stable |
| Current code status | No generic runtime has been extracted yet |
| Intended availability | Open public stack when the extracted foundation is safe to publish |

This repository is **not Kerani Core SME**. It may later become a reusable foundation for Telegram → Google Apps Script → Gemini API applications, including Kerani Core, but that must be proven first.

---

## 1. Raw idea

After OpsMate BSE reaches its agreed Definition of Done, inspect its working implementation and extract only the parts that are genuinely reusable for small conversational applications:

`Telegram → Apps Script → AI → data/workspace → response`

The result must come from a tested system, not an imagined framework.

---

## 2. Why this exists

OpsMate may contain useful infrastructure that should not be rebuilt for every future application:

- receiving and normalising Telegram messages;
- routing a request through an Apps Script workflow;
- calling Gemini safely;
- controlled clarification, validation and confirmation;
- queueing, logging and human review;
- deterministic replies and error handling;
- TEST/production isolation; and
- regression tests around the workflow.

If those pieces can serve a second application without a major rewrite, they become a small shared stack. Sharing that proven stack publicly is the project’s act of generosity—not a promise to generalise prematurely.

---

## 3. Goals

1. Identify which OpsMate components are genuinely reusable.
2. Extract them without farm, BSE, plot, inventory, claim or SME assumptions.
3. Preserve proven behaviour through regression tests.
4. Define a small, explicit configuration/extension contract.
5. Build one independent, tiny second application on the extracted core.
6. Publish the stack openly when security, documentation and licensing are ready.
7. Let future domain applications consume the core rather than silently changing it.

---

## 4. Non-goals

- Building Kerani Core SME in this repository.
- Replacing or redesigning OpsMate while it is still being completed.
- Building a farm-management system.
- Home Assistant, local LLM, workstation, remote-desktop or hardware work.
- A fully autonomous agent with unrestricted access to business systems.
- A broad “platform” designed from speculation.

---

## 5. Core extraction principle — LOCKED

> **Genericity is earned through extraction and reuse, not assumed during design.**

Operational rule:

1. Finish and stabilise the relevant OpsMate behaviour.
2. Classify each component as `GENERIC`, `OPSMATE-SPECIFIC`, or `UNCERTAIN`.
3. Extract only `GENERIC` components; leave `UNCERTAIN` in OpsMate until evidence exists.
4. Remove domain vocabulary and hidden domain assumptions only where behaviour remains covered by tests.
5. Prove reuse with a second application.

“Genericity is Generosity” does **not** mean accepting every requested feature into the core. The core stays small, explicit, tested and safe; generosity happens through clear interfaces, documentation and open sharing.

---

## 6. Candidate generic surface — NOT LOCKED

The following is a candidate list to audit against OpsMate. It is not a build plan.

| Candidate surface | Evidence needed before extraction |
|---|---|
| Telegram adapter | Works without OpsMate-specific message or identity assumptions |
| Apps Script runtime boundary | Portable deployment/configuration contract |
| Gemini adapter | Domain-neutral prompt/input/output boundary and safe error handling |
| Request pipeline | Reusable stages that do not encode farm or SME workflow |
| Queue and worker | Generic state transitions and retry/review semantics |
| Parser/normaliser | Input contract independent of an OpsMate record type |
| Reply engine | Deterministic response contract and safe fallback replies |
| Logging/evidence | Generic event schema with protected-data rules |
| Configuration/secrets boundary | No credentials in source; app-specific settings separated |
| Test harness | Reproducible tests that can run without live Telegram production traffic |

---

## 7. Initial constraints

- Initial runtime: Google Apps Script.
- Initial chat interface: Telegram.
- Initial AI provider: Gemini API.
- Secrets must remain outside source control and outside public examples.
- TEST and production behaviour/data must remain isolated.
- A coding agent has no direct Telegram credential or production-message access.
- Human/operator controls TEST injection and live deployment boundaries.
- Domain logic belongs in an application layer, not silently in generic core code.
- Open-source publication requires a security review, redacted examples and an explicit licence.

---

## 8. Questions to answer with evidence

- Which OpsMate files/functions are truly reusable?
- What configuration contract can express a new application without editing core code?
- Which storage abstractions are necessary, and which are over-abstraction?
- Which parts should intentionally remain Apps-Script-specific in v0.x?
- How are prompts, schemas and validations separated from the runtime core?
- What is the smallest meaningful second application for proof of reuse?
- What must be redacted or redesigned before public release?
- Does this repository deserve a new permanent name after the proof stage?

---

## 9. Risks and guardrails

| Risk | Guardrail |
|---|---|
| Premature abstraction | Extract after stable OpsMate evidence only |
| Hidden OpsMate assumptions | Component ledger plus regression tests |
| Core becomes Kerani Core-specific | Domain code/config stays in consumer application |
| Over-engineering | Prefer the smallest interface demonstrated by two uses |
| Regression during extraction | Preserve/port relevant harness tests before refactor |
| Secret exposure | No secret commits; redacted fixtures and publication review |
| Public stack misused or confusing | Clear scope, examples, threat notes and versioning |
| Architectural drift | ZASS/decision ledger are authoritative; changes follow state control |

---

## 10. Extraction ledger

Create and maintain `docs/EXTRACTION_LEDGER.md` only when extraction begins.

| Component | OpsMate source | Classification | Dependencies | Extraction status | Evidence / test | Notes |
|---|---|---|---|---|---|---|
| — | — | `GENERIC` / `OPSMATE-SPECIFIC` / `UNCERTAIN` | — | Not started | — | — |

No component becomes generic merely because it sounds reusable.

---

## 11. Experiments

| ID | Experiment | Success condition | Status |
|---|---|---|---|
| E-001 | Classify the completed OpsMate components | Ledger has evidence-backed classification | Deferred |
| E-002 | Extract one candidate component | Relevant OpsMate-derived regression tests pass | Deferred |
| E-003 | Assemble minimum generic workflow | TEST workflow runs without domain vocabulary or code forks | Deferred |
| E-004 | Build a second tiny application | Works through configuration/extension points | Deferred |
| E-005 | Public-release review | No secrets/private data; docs, licence and safe examples ready | Deferred |

---

## 12. Definition of Done for the proof stage

`OpsMate behaviour complete and stable`
→ `components classified with evidence`
→ `generic components extracted`
→ `relevant regression tests pass`
→ `second independent application works`
→ `no major core rewrite needed for that second app`
→ `public-release safety review passes`
→ `generic core is proven enough to name/version publicly`

Until then, this remains an extraction project—not a framework claim.

---

## 13. Decision ledger

| ID | Decision | State | Rationale / evidence |
|---|---|---|---|
| D-001 | This repo is an OpsMate-derived generic-core extraction, not Kerani Core SME. | LOCKED | Separate reusable infrastructure from the SME product domain. |
| D-002 | Genericity is earned through extraction and reuse, not assumed during design. | LOCKED | Prevents speculative abstraction. |
| D-003 | The guiding motto is “Genericity is Generosity.” | LOCKED | A proven, safe stack should be shared openly for others to build upon. |
| D-004 | Public release happens only after security review, redaction, documentation and explicit licence. | LOCKED | Openness must not expose secrets, operational data or unsafe defaults. |
| D-005 | Permanent project name is deferred until reuse is demonstrated. | DEFERRED | Name must describe demonstrated function, not aspiration. |

---

## 14. Change control

All significant decisions and experiments use:

`RAW → CANDIDATE → TESTING → DECIDED → LOCKED`

Alternative terminal/exception states:

`REJECTED` · `DEFERRED` · `SUPERSEDED`

A suggestion, AI output or multi-model agreement is not a decision. It becomes a decision only when its evidence, trade-offs and owner approval are recorded here or in a linked decision record.

---

## 15. Repository growth rule

Keep the repository deliberately small before extraction:

`ZASS.md`
`docs/DEV_WORKFLOW.md`

When evidence justifies it, add:

`src/`
`tests/`
`config/`
`docs/EXTRACTION_LEDGER.md`
`docs/ARCHITECTURE.md`

Do not create code, abstractions or folders merely to make the project look mature.
