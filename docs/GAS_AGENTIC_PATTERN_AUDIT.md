# Public GAS Agentic Pattern Audit — Evidence Input for Kerani Challenge

**Status:** EVIDENCE INPUT ONLY — no runtime selected  
**Date:** 2026-10-11  
**Project:** Kerani Core SuperBasic  
**Purpose:** Extract implementation patterns from three public Google Apps Script + Gemini repositories for the upcoming Architecture Assumption + Boundary Challenge.  
**Important:** These repositories demonstrate implementation feasibility/patterns. They do **not** prove Kerani's multi-tenant production scale, security model, latency target or business-authority model.

## Sources audited

1. `tanaikech/adk-gas`
2. `tanaikech/GeminiWithFiles`
3. `mhawksey/GeminiApp`

No library is adopted by this audit.

---

## 1. Pattern extraction summary

| Public implementation | Source-supported pattern | Kerani interpretation |
|---|---|---|
| **adk-gas** | Native GAS tools, phase-separated orchestration, fast-track bypass, hard timeout before GAS execution limit, LockService-based state protection, logging, token/session safeguards, HITL suspend/resume | Strong evidence that GAS can host bounded tool orchestration and human-gated execution, but its full planner/DAG/A2A/MCP design is broader than Kerani V1 needs |
| **GeminiWithFiles** | Gemini function/custom functions, tool configuration, chat history, token tracking, Agent Skills, model-selected tools and dynamic workflows | Strong evidence for Gemini-driven language → tool selection in GAS; dynamic/autonomous execution surfaces are not automatically suitable for Kerani |
| **GeminiApp** | Minimal Gemini function calling, multi-turn chat, `functionCalls()` / `functionResponse`, Gemini requests through `UrlFetchApp.fetch` | Useful minimal baseline showing that function calling does not require Python, Node, n8n or a full agent framework |

---

## 2. Patterns to EXTRACT for challenge

These are patterns to evaluate, not implementation commitments:

- fixed approved tool registry;
- function schema / structured arguments;
- model-selected tool routing;
- deterministic fast-track / bypass for work that does not need full orchestration;
- pre-tool authorization/policy hook;
- Human-in-the-Loop suspend/resume for sensitive actions;
- hard timeout / execution-budget guard;
- state protection / concurrency guard;
- token/session budget;
- payload-size guard;
- structured tool/execution logging;
- tool and runtime latency telemetry;
- clean separation between model decision and actual function execution.

## 3. Patterns to PARK or AVOID for V1

- unrestricted dynamic JavaScript execution;
- arbitrary tool loading without explicit authority review;
- autonomous unrestricted replanning;
- full DAG planner unless evidence requires it;
- MCP everywhere;
- A2A agent hierarchy;
- subagents by default.

Kerani V1 is intended to be **bounded business tool orchestration**, not a general autonomous-agent framework.

---

## 4. Central Control Plane vs Customer-Owned Apps Script Edge

This audit strengthens a distinction that must be challenged explicitly.

### A. Central Control Plane

Potential responsibilities:

~~~text
channel ingress
→ tenant identity
→ authorization / scope
→ quotas / entitlement
→ language / tool routing
→ shared AI policy
→ central audit / telemetry
→ cross-channel coordination
~~~

Central control-plane candidates remain the existing E-016 four-way benchmark:

1. Central Apps Script
2. Cloudflare Workers + D1
3. Cloud Run stack
4. OCI A1 VM

No winner is selected.

### B. Customer-Owned Apps Script Edge

A separate role may exist for Premium/customer-owned Google integration:

~~~text
Kerani Central
      ↓
customer-owned Apps Script Web App / execution edge
      ↓
customer-owned Google resources
Sheets / Drive / Workspace APIs / optional customer-owned AI
~~~

This is **not automatically a fifth central control-plane candidate**.

Potential advantages to test:
- natural access to customer-owned Google resources;
- stronger customer-side data ownership/isolation;
- no customer-managed server/OS;
- useful execution surface for approved Google-specific tools;
- possible BYO Google/Gemini edge.

Potential disadvantages to test:
- per-customer deployment/update/version management;
- Apps Script quotas and execution limits;
- synchronous/blocking networking constraints;
- lower runtime/queue control than a general server;
- observability fragmentation across customer-owned deployments;
- auth/delegation complexity;
- inconsistent tenant environments/configurations.

### Key challenge question

> Should Kerani separate **central coordination/control** from **customer-owned Google execution/data edge**, rather than forcing one runtime to perform both roles?

This must be answered by evidence, not preference.

---

## 5. Important implementation evidence from adk-gas

The audited repository explicitly designs around Google Apps Script constraints rather than treating GAS like Node.js.

Relevant implementation patterns include:
- a fast-track path that bypasses unnecessary execution/synthesis;
- sequential execution appropriate to synchronous GAS networking;
- hard abort before the GAS execution ceiling;
- `LockService` for protected state;
- Native GAS functions as tools;
- Human-in-the-Loop suspension before a tool, persistence of session state, and later resume after approval;
- structured logging and token/session safeguards.

For Kerani, the strongest relevance is not the full planner. It is proof that **tool execution + policy hook + human suspend/resume** can live inside GAS.

---

## 6. Important implementation evidence from GeminiWithFiles

The audited repository exposes:
- custom function definitions;
- tool configuration;
- chat history;
- token usage;
- Agent Skills / model-selected capabilities.

For Kerani, this supports the feasibility of:

~~~text
natural language
→ Gemini selects an approved function/tool
→ application executes the tool
→ result returns to the model/user
~~~

The repository's more autonomous/dynamic execution features are **not** accepted as Kerani authority patterns without separate challenge evidence.

---

## 7. Important implementation evidence from GeminiApp

The audited repository provides a smaller function-calling surface:
- declare function schema;
- add function to chat/model;
- inspect model `functionCalls()`;
- pass back `functionResponse`;
- perform Gemini HTTP requests through Apps Script `UrlFetchApp.fetch`.

For Kerani, this is useful as the minimal proof that a bounded tool router can be implemented in GAS without adopting a large agent framework.

---

## 8. Challenge implications

The Architecture Assumption + Boundary Challenge should use this audit to test:

1. **Runtime/module boundary**  
   Whether Apps Script is better treated as central runtime, customer edge, both in different tiers, or neither.

2. **Latency/dynamic-language viability**  
   Whether AI-at-entry latency remains acceptable and where fast-path bypass is justified; Day-1 latency observability remains LOCKED.

3. **4-way central control plane**  
   Keep the existing E-016 comparison unchanged; do not silently add customer-owned GAS edge as a fifth central candidate.

4. **Agentic Tool Boundary**  
   Public patterns prove tool/function calling and HITL are feasible in GAS, but Kerani must still define its own READ / PROPOSE / CLARIFY / VALIDATE / MUTATE / SYSTEM authority model, trusted tenant scope, idempotency and audit.

5. **Central-vs-edge role split**  
   Test whether central policy/identity/routing should remain hosted while Google-specific/private data operations execute in a customer-owned Apps Script edge.

---

## 9. Evidence posture

**Supported by audited repositories:**
- GAS can call Gemini and support function/tool calling;
- GAS can expose native functions as tools;
- GAS can support HITL-style suspend/resume patterns;
- GAS implementations need explicit handling for runtime, quota, timeout, concurrency and payload constraints.

**Not proven by these repositories:**
- Kerani production scale;
- thousands of concurrent tenants;
- Kerani security/isolation correctness;
- Kerani latency target;
- superiority of Apps Script over Cloudflare/Cloud Run/OCI;
- production viability of a customer-owned edge at scale.

Therefore this audit raises feasibility confidence but does not select architecture.
