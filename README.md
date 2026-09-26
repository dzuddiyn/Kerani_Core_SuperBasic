# Kerani Core SuperBasic

> A small, evidence-led foundation for conversational applications built around **Telegram → Google Apps Script → Gemini API**.
>
> **Motto:** *Genericity is Generosity.*

## Status

**Extraction project — no generic runtime has been extracted yet.**

This repository is a landing zone for discovering reusable infrastructure inside the completed, tested parts of **OpsMate BSE**. It is not Kerani Core SME, not a farm-management system, and not yet a framework claim.

The intended outcome is a small public stack that helps people build safe, testable conversational workflows without rebuilding the same messaging, routing, AI, logging and test foundations from scratch.

## Why this project exists

OpsMate may contain reusable building blocks such as:

- Telegram message intake and normalisation;
- Apps Script request/response workflow;
- Gemini API boundary and safe failure handling;
- clarification, validation and confirmation stages;
- queue/worker and human-review patterns;
- deterministic replies, logging and evidence;
- TEST/production isolation; and
- regression-test harnesses.

Those components become part of this core only when their behaviour is proven reusable—not simply because they look generic.

## Extraction principle

> **Genericity is earned through extraction and reuse, not assumed during design.**

The sequence is deliberately strict:

1. Stabilise the relevant OpsMate behaviour and regression tests.
2. Classify each component as `GENERIC`, `OPSMATE-SPECIFIC`, or `UNCERTAIN`.
3. Extract only evidence-backed generic pieces.
4. Remove domain assumptions while preserving test-covered behaviour.
5. Prove the result with a second, independent small application.
6. Prepare a safe public release: security review, redaction, documentation and licence.

## What it is not

- **Not** the Kerani Core micro-SME application itself.
- **Not** a replacement or speculative redesign of OpsMate.
- **Not** a Home Assistant, local-LLM, workstation or hardware project.
- **Not** an autonomous agent with unrestricted access to business systems.
- **Not** a large platform designed before two real use cases demand it.

## Current boundaries

| Area | Current position |
|---|---|
| Chat interface | Telegram, initially |
| Runtime | Google Apps Script, initially |
| AI provider | Gemini API, initially |
| Production writes | Disabled by default for unproven workflows |
| Secrets | Never committed; kept outside source and public examples |
| TEST vs production | Separate credentials, data stores, logs and deployment controls |
| Core vs domain | Domain logic stays in consumer applications |
| Public release | Only after review, redaction, documentation and explicit licence |

## Documentation

| Document | Purpose |
|---|---|
| [ZASS — project source of truth](./ZASS_Kerani_Core_SuperBasic.md) | Scope, decisions, risks, experiments and Definition of Done |
| [Development workflow](./docs/DEV_WORKFLOW.md) | TEST/production boundaries, agent roles, extraction process and Git/public-release safeguards |

## Repository growth

The repository stays intentionally small until the evidence exists. When extraction begins, the expected additions are:

`src/` · `tests/` · `config/` · `docs/EXTRACTION_LEDGER.md` · `docs/ARCHITECTURE.md`

No folders or abstractions are added merely to make the project appear mature.

## Future users and contributors

This stack is planned as an open public resource, but it is not ready for installation or production use today. Before contributing or consuming it, wait for the extraction proof stage, licence and safe example configuration.

Until then, the most useful contribution is disciplined evidence: stable OpsMate behaviour, regression tests, clear boundaries and honest notes about what is still uncertain.
