# OpsMate vs Kerani AI Agentic Tool — Architecture Comparison Note

**Status:** Supporting architecture finding/comparison  
**Date:** 2026-10-11  
**Project:** Kerani Core SuperBasic  
**Scope:** Compare the observed OpsMate interaction/data-flow style with the current Kerani AI bounded Agentic Tool candidate.  
**Authority:** This note does not LOCK AC-012, run Challenge Design, or replace ZASSIMPLE/DESIGN.md. It supports the upcoming Architecture Assumption + Boundary Challenge.

---

## 1. Executive summary

### OpsMate

> **Flow first, AI in the middle.**

OpsMate is primarily a governed workflow/pipeline system. The code already determines much of the route. AI assists classification/extraction inside that route, while guards, domain validation, human review and controlled writers preserve business authority.

### Kerani AI Agentic Tool

> **Capability first, AI chooses the capability.**

Kerani AI may move toward a bounded tool/capability model where natural language is translated into an allowed tool call. The AI may select and parameterise a tool, but authority remains governed. READ, PROPOSE, CLARIFY, VALIDATE, MUTATE and SYSTEM/AUTOMATION remain distinct authority classes.

---

## 2. OpsMate — observed action / mutation flow

~~~text
┌──────────────┐
│ User message │
└──────┬───────┘
       │
       ▼
┌──────────────────┐
│ Telegram ingress │
└──────┬───────────┘
       │
       ▼
┌──────────────────────┐
│ Queue / pending job  │
└──────┬───────────────┘
       │
       ▼
┌──────────────────────┐
│ Unified process      │
│ main workflow path   │
└──────┬───────────────┘
       │
       ▼
┌──────────────────────┐
│ Gemini parse         │
│ classify / extract   │
└──────┬───────────────┘
       │
       ▼
┌──────────────────────┐
│ Guard / safety check │
└──────┬───────────────┘
       │
       ▼
┌──────────────────────┐
│ Domain validator     │
└──────┬───────────────┘
       │
       ▼
┌──────────────────────┐
│ Candidate record     │
└──────┬───────────────┘
       │
       ├──────────────► if information missing
       │                  ┌──────────────────────┐
       │                  │ Clarification needed │
       │                  └──────────┬───────────┘
       │                             │
       │                             ▼
       │                       back to workflow
       │
       ▼
┌──────────────────────┐
│ Human review         │
│ approval card        │
└──────┬───────────────┘
       │
       ▼
┌──────────────────────┐
│ Benar / Betulkan     │
│ / Batal              │
└──────┬───────────────┘
       │
       ▼
┌──────────────────────┐
│ Authoritative write  │
└──────┬───────────────┘
       │
       ▼
┌──────────────────────┐
│ Audit / log          │
└──────┬───────────────┘
       │
       ▼
┌──────────────┐
│ User reply   │
└──────────────┘
~~~

**Finding:** OpsMate's strongest property is governance around mutation. Its weakness is that the user experience and routing are relatively workflow-centric, with AI embedded inside a larger predefined pipeline.

---

## 3. OpsMate — observed read / retrieval flow

~~~text
┌──────────────┐
│ User command │
└──────┬───────┘
       │
       ▼
┌──────────────────────┐
│ Command / route      │
│ recognition          │
└──────┬───────────────┘
       │
       ▼
┌──────────────────────┐
│ Specific retrieval   │
│ function             │
└──────┬───────────────┘
       │
       ▼
┌──────────────────────┐
│ Sheet / stored data  │
└──────┬───────────────┘
       │
       ▼
┌──────────────┐
│ User reply   │
└──────────────┘
~~~

**Finding:** direct/read work can avoid the full mutation path, but the UX may remain tied to commands or coded routes such as status/report/history functions.

---

## 4. Kerani AI — candidate high-level Agentic Tool flow

~~~text
┌──────────────┐
│ User message │
└──────┬───────┘
       │
       ▼
┌──────────────────────┐
│ Channel adapter      │
│ Telegram / WhatsApp  │
└──────┬───────────────┘
       │
       ▼
┌──────────────────────┐
│ Tenant identity      │
│ scope / access       │
└──────┬───────────────┘
       │
       ▼
┌────────────────────────────┐
│ Language / Tool Router     │
│ AI understands intent      │
└──────┬───────────┬─────────┘
       │           │
       │           │
       ▼           ▼
   READ PATH    ACTION PATH
~~~

**Candidate principle:** natural language becomes the front door, while tools remain bounded capabilities with explicit authority metadata.

---

## 5. Kerani AI — candidate READ path

~~~text
┌────────────────────────────┐
│ Natural language question  │
│ "blok 7 kali terakhir      │
│  baja bila?"               │
└──────────────┬─────────────┘
               │
               ▼
┌────────────────────────────┐
│ AI chooses READ tool       │
│ retrieve_history()         │
│ retrieve_report()          │
│ lookup_status()            │
└──────────────┬─────────────┘
               │
               ▼
┌────────────────────────────┐
│ Deterministic query        │
│ tenant-scoped retrieval    │
└──────────────┬─────────────┘
               │
               ▼
┌────────────────────────────┐
│ Structured result          │
└──────────────┬─────────────┘
               │
               ▼
┌──────────────┐
│ User reply   │
└──────────────┘
~~~

**Key change:** the user no longer needs to know rigid retrieval syntax. AI may translate natural language into tool arguments, while the actual data query remains deterministic and tenant-scoped.

---

## 6. Kerani AI — candidate ACTION / mutation path

~~~text
┌────────────────────────────┐
│ Natural language report    │
│ "beli racun 3 botol RM90"  │
└──────────────┬─────────────┘
               │
               ▼
┌────────────────────────────┐
│ AI chooses PROPOSE tool    │
│ prepare_candidate()        │
└──────────────┬─────────────┘
               │
               ▼
┌────────────────────────────┐
│ Candidate object           │
│ non-authoritative          │
└──────────────┬─────────────┘
               │
               ├──────────────► if information missing
               │                  ┌──────────────────────┐
               │                  │ ask_clarification() │
               │                  └──────────┬───────────┘
               │                             │
               │                             ▼
               │                        back to candidate
               │
               ▼
┌────────────────────────────┐
│ Preview to user            │
│ "Betul?"                   │
└──────────────┬─────────────┘
               │
               ▼
┌────────────────────────────┐
│ Human confirmation         │
└──────────────┬─────────────┘
               │
               ▼
┌────────────────────────────┐
│ Deterministic / domain     │
│ validation                 │
└──────────────┬─────────────┘
               │
               ▼
┌────────────────────────────┐
│ Controlled write           │
│ authoritative record       │
└──────────────┬─────────────┘
               │
               ▼
┌────────────────────────────┐
│ Audit / log / receipt      │
└──────────────┬─────────────┘
               │
               ▼
┌──────────────┐
│ User reply   │
└──────────────┘
~~~

**Key change:** AI selects or prepares a bounded capability, but does not acquire free mutation authority.

---

## 7. 1:1 comparison

| Concern | OpsMate | Kerani AI Agentic Tool |
|---|---|---|
| System style | Workflow/pipeline-centric | Tool/capability-centric |
| User interaction | More route/command dependent | Natural-language first |
| AI role | Parse/classify/extract inside predefined flow | Understand intent + select/parameterise bounded tool |
| Retrieval | Specific command/route/function | `retrieve_history()`, `retrieve_report()`, `lookup_status()` |
| Record preparation | Candidate inside workflow | `prepare_candidate()` as PROPOSE |
| Clarification | Workflow-specific logic | Bounded CLARIFY capability |
| Validation | Guard + domain validator | Guard/domain validator retained |
| Human confirmation | Present in governed mutation flow | Retained where mutation authority requires it |
| Write authority | Controlled writer | Controlled writer; AI does not get free mutation authority |
| Adding use cases | Often new branch/route/workflow | Candidate: add bounded tool + schema + authority contract |
| Language flexibility | More rigid | Higher natural-language flexibility |
| Main strength | Proven governance discipline | Natural UX + modular capability routing |
| Main risk | Long/heavy pipeline and rigid UX | Tool authority creep, AI latency/cost, unsafe routing if boundaries are weak |

---

## 8. What Kerani should KEEP from OpsMate

These are valuable governance lessons and should not be discarded merely because Kerani becomes more agentic:

- candidate is not an authoritative record;
- human confirmation for governed mutation;
- deterministic validation;
- domain validation;
- audit trail / receipt;
- idempotency;
- retry awareness and truthful failure state;
- TEST / production separation;
- read paths should not be forced through a mutation pipeline without need.

---

## 9. What Kerani may REFACTOR into bounded tools

### READ candidates

- `retrieve_history()`
- `retrieve_report()`
- `lookup_status()`

### PROPOSE candidate

- `prepare_candidate()`

### CLARIFY candidate

- `ask_clarification()`

### VALIDATE candidates

- `validate_candidate()`
- domain-specific validators such as inventory/business-rule validation where appropriate

These remain candidates until challenged and backed by real execution evidence.

---

## 10. What AI must NOT receive as free authority

Examples:

- `commit_record()`
- `delete_record()`
- `approve_expense()`
- `change_inventory_truth()`

Canonical boundary:

~~~text
GENERIC
≠ automatically TOOL

TOOL
≠ automatically WRITE

WRITE
≠ automatically AI authority
~~~

A MUTATE capability must remain behind explicit authority design, tenant scope, human confirmation where applicable, deterministic/domain validation, idempotency and audit.

---

## 11. Core architecture distinction

### OpsMate

~~~text
User
 ↓
Fixed workflow
 ↓
AI parse
 ↓
Guard
 ↓
Validation
 ↓
Approval
 ↓
Write
~~~

### Kerani AI Agentic Tool

~~~text
User
 ↓
AI understands intent
 ↓
Choose bounded tool
 ↓
Tool output
 ↓
Authority gate
 ↓
If READ → answer
If MUTATION → confirm + validate + controlled write
~~~

---

## 12. Final finding

OpsMate should be treated as a **reference system and teacher**, not as the blueprint that Kerani must inherit.

OpsMate provides strong evidence about:
- safe mutation boundaries;
- candidate vs authoritative truth;
- human approval;
- validation;
- audit;
- failure/retry behaviour.

Kerani AI can therefore become architecturally different:

> **OpsMate = workflow-centric operational system.**  
> **Kerani AI = governed capability/tool system with a natural-language front end.**

The intended evolution is not "make OpsMate more agentic." It is to **retain OpsMate's governance lessons while allowing Kerani to use a different interaction and orchestration architecture**.

---

## 13. Challenge implications

This comparison should feed the mandatory **Agentic Tool Boundary** dimension of the upcoming Architecture Assumption + Boundary Challenge.

The challenge should classify each relevant OpsMate behaviour as one of:

- **KEEP**
- **REFACTOR INTO TOOL**
- **DOMAIN-ONLY**
- **REJECT**

and verify that any proposed tool declares:
- whether it is genuinely generic;
- whether it is actually tool-worthy;
- its authority class;
- its human gate;
- its deterministic/domain gate;
- its tenant/audit/idempotency requirements.

**Challenge Design has not been run by this note. AC-012 remains CANDIDATE.**
