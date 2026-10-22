# Kerani AI — Free Chat-First and User-Created Telegram Group UX

**Decision:** **D-061 / L-049 — OWNER LOCKED PRODUCT/UX SCOPE** (2026-10-23)  
**Tracking:** [KAI-9](https://linear.app/dzuddiyn/issue/KAI-9/d-061-lock-free-chat-first-and-user-created-telegram-group-ux)  
**Authority:** `ZASS_Kerani_Core_SuperBasic.md` D-061/L-049; `ZASSIMPLE/DESIGN.md` is an active design projection.  
**Limits:** No Telegram group test has been run in this work; no bot configured, no runtime/architecture selection, no provider credentials, no production coding or feature delivery. **Product direction LOCKED; exact @mention delivery and group UX are NOT VERIFIED.**

## 1. Owner-confirmed problem statement (DUMP → DISTILL)

Kerani AI Free should work simply as a **personal 1-to-1 chatbot**, without inheriting the expensive and complicated OpsMate-style group-role/approval coordination. A single company may have multiple Free user registrations; if two workers independently report one real event, their messages may both be recorded. **The owner expressly rejected AI-based semantic comparison and cross-worker de-duplication** in the Free product because it uses too much processing and server capacity.

The Free system only needs to **warn** when **multiple active Free users are verified to be attached to the same Business ID**, that independent records may overlap, then provide practical tips for creating a Telegram group and adding/addressing the bot. Keep cheap source-event/retry idempotency and ordinary business-data validation regardless of plan; do not confuse *Telegram retry of one message* with *two different human reports about similar events*.

Free should not have formal company admin/owner/supervisor/worker roles, group creation/provisioning, broad member management or approval workflows. Premium/domain solutions can add multi-worker team operations based on actual demand, in a **separate authorised scope**.

## 2. Onboarding and identity contract (LOCKED product principle)

- Collect the business/company name during onboarding; assign immutable **Kerani Business ID** and **Kerani User ID**.
- Link the authenticated Telegram user to a Kerani User ID and authorised Business ID in backend, independent of WhatsApp/Telegram channel binding (existing D-023).
- If another user enters an existing Business ID, **knowledge of the ID is insufficient authorization**: require owner-approved/verified join or a bounded invitation/verification process. No role hierarchy is implied by this requirement; only minimum safe tenant membership.
- More than one verified *active Free user* linked to the same Business ID is sufficient to show a **non-blocking informational warning** (e.g. after onboarding or appropriate reminder): “Beberapa pengguna Free berdaftar dengan perniagaan ini. Laporan berasingan mungkin bertindih. Untuk koordinasi, cipta group Telegram sendiri, tambah bot Kerani dan tujukan arahan kepada bot.” Avoid incessant repeated warnings.
- No per-business scanning of transaction content, no fuzzy/semantic similarity AI, no auto-dedup/merge across worker-originated reports, no automatic discard or mutation due to a warning.
- **Technical idempotency remains non-negotiable:** identical provider update/retry must not create a second authoritative effect. Use scoped transport event ID/idempotency key + normal record commit validation and truthful response receipts. Specific key/transaction shape remains an engineering decision.

## 3. User-created Telegram group — UX priority, not unproven guarantee

**The owner creates and administers the Telegram group** and adds KeraniBot. Kerani only binds a selected, verified group ID to an authorised Business ID with minimum scope/permission checks. No automatic creation of groups or enforcement of user hierarchy. Group link/join must not expose company records merely because the group or a Business ID is known. Reports requested in group may reveal data to group members, so group binding, query permission and any tenant information disclosure need explicit security/UX validation.

**Preferred natural syntax (required to try first, NOT technically confirmed):**

`@KeraniBot rekod Baja out N M1P12 1 set`

`@KeraniBot jana report bulan ni`

**Caution:** Under default Telegram Privacy Mode, the official FAQ guarantees bot-directed commands, messages sent via the bot, and replies to its messages, **not a reliable delivery promise for ordinary plain-text @mentions**. A bot admin or privacy-OFF may receive all group messages, but those are higher-exposure modes and are not authorised by the product LOCK. **A live synthetic group test is required.** Do not promise that normal @mention works under privacy ON or silently switch privacy OFF.

**Fallback when plain @mention fails:**

1. Member types `/`, chooses `/rekod@KeraniBot` or `/report@KeraniBot` from Telegram's command menu.
2. Telegram **sends** the selected slash command. A native Telegram slash-command option to merely prefill the composer without send is **not a supported Bot API guarantee**; do not promise it.
3. Bot replies with targeted `ForceReply`: e.g. “Balas mesej ini dengan maklumat rekod/report”; mobile client presents reply composition. A natural private-chat style response should require no extra slash command.
4. User replies: `Baja out N M1P12 1 set` or `Jana report bulan ni`.
5. Backend matches **group/chat ID + Telegram user ID + bot prompt message ID + request state** to avoid two workers' interleaved replies being confused, then executes ordinary tenant-scoped candidate/validation/confirmation/authoritative write or READ as appropriate.
6. Report only verified save/query result. Timeouts, missing user authorization, unrelated replies and expired prompts must fail safely with helpful actionable messages.

**Optional exploration:** Telegram Inline Mode can prefill `@KeraniBot <query>` in the input via inline keyboard switch; selecting an inline result is a separate interaction pattern, not direct message text intake. Only retain if it actually improves the user journey and does not add a new complexity burden.

## 4. Mini App vs chat (LOCKED sequencing, existing LOCK unchanged)

- **Chat-first** means Free users begin with personal natural-language bot messages and Free Core record/retrieve/report; they are not forced to fill Telegram Mini App forms during normal chat.
- **D-057/L-047 remains LOCKED:** Telegram Mini App is a first-class *deterministic Free* thin UI surface for explicit forms/history/receipts/basic summaries, independent of AI availability. It is a separate web view inside Telegram, not an always-required chat form.
- Implement Mini App as a subsequent permitted slice rather than a first-launch blocker. This is **launch priority**, not repeal of D-057, no proof that Mini App already exists.
- **Premium group/team operations** remain future scope: advanced members, roles, formal approvals, automatic reconciliation, alert workflows, dashboards. Do not import them into Free.

## 5. Official Telegram evidence (DOCUMENTATION VERIFIED, BOT NOT TESTED)

- [Telegram Bot Features — Group Privacy Mode and commands](https://core.telegram.org/bots/features): privacy-ON accepts bot-directed commands and replies; bot admins or privacy-OFF receive broader group messages.
- [Telegram Bots FAQ — message visibility in groups](https://core.telegram.org/bots/faq): explicit `/command@bot`, bot inline messages and replies; plain mention is not listed as reliably delivered in the privacy-ON baseline.
- [Telegram Bot API — ForceReply](https://core.telegram.org/bots/api#forcereply): clients show reply composition to user; `selective` permits targeting of a reply-sender in group.
- [Telegram Bot Guidelines — slash command interaction](https://core.telegram.org/bots/guidelines): command shortcuts can be sent directly, slash menu/command UX can be clunky; bot should provide more approachable keyboard/reply interfaces.
- [Telegram Inline Bots](https://core.telegram.org/bots/inline): inline queries require inline-mode UX and a returned result selection; not a guarantee that an ordinary `@mention` chat message will be delivered.

These are **API/documentation capabilities**, not acceptance results for a running KeraniBot.

## 6. ZASS CHALLENGE → future six-test synthetic proof matrix (PENDING)

| Case | Exact test | PASS evidence sought | Current verdict |
|---|---|---|---|
| T01 | Plain `@KeraniBot rekod ...` with Privacy ON in ordinary user-created group | Received Update contains the exact message, correct actor/chat context; produces expected valid response | **NOT TESTED** |
| T02 | Same mention, Privacy OFF only in isolated fixture group | Compare message deliveries/security exposure, with no production privacy-mode change | **NOT TESTED** |
| T03 | Slash menu/command `/rekod@KeraniBot` | Auto-send behaviour seen; bot receives directed command, no special group admin setup | **NOT TESTED** |
| T04 | `ForceReply` after slash command | Client opens reply UX targeted to author; bot receives reply with expected linkage in Privacy ON | **NOT TESTED** |
| T05 | Two worker accounts reply to two bot prompts concurrently | Actor/prompt/group isolated; no reply mix-up; same event retry idempotent; semantic dedup **NOT** required | **NOT TESTED** |
| T06 | Inline keyboard prefill vs ForceReply | User-step/time/privacy comparison proves whether optional Inline Mode meaningfully helps | **NOT TESTED** |

**Falsification/stop:** no fake PASS from documentation; privacy OFF/admin access is not the automatic solution; accidental cross-tenant read/write or actor mix-up is HARD STOP; no AI semantic duplicate detection is introduced. Capture both positive and negative message delivery, Telegram app/client version and real update receipts.

## 7. ACCEPTANCE vs NOT LOCKED

**LOCKED product direction now:** Free personal bot first; simple ID-based onboarding; warning-only multi-Free overlap; no cross-user content comparison; user-created group as optional coordination strategy; preferred `@mention` to test; slash-command → ForceReply as viable fallback candidate; no OpsMate group governance; Mini App still a first-class separate Free surface later in delivery sequencing.

**NOT LOCKED / NOT DONE:** whether plain @mention works in privacy ON; bot credentials/privacy-mode settings; whether ForceReply UX is pleasant on targeted phone models; implementation routing/token/group binding design; formal security model; exact group entitlement/pricing; live production group processing; architecture/PRE-ARCH; any tests. This LOCK may not be interpreted as a test PASS.

**NEXT — exactly one:** **D-061 Telegram Group UX Proof (T01–T06)** with a synthetic bot/group after separate execution approval; choose the least-complex verified interaction path and retain Free chat simplicity.

## 8. Lineage

D-016/L-011 (basic Free workflow), D-015/L-010 (authority/validation), D-023 (channel-neutral tenant identity), D-055/L-046 (Free independent of AI), D-057/L-047 (Telegram deterministic Free Mini App), D-059 (Premium Business Workspace CANDIDATE), D-060 (resilience/cost candidate). D-061/L-049 **does not replace** any of these existing LOCKED principles.
