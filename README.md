# SFR — Session Frame Runtime

**Original author:** Saffi Hartal

SFR is a lightweight attention-continuity runtime for substantial AI work.

Its job is simple: keep work attached to the Root obligation while attention changes, so necessary reasoning can move elsewhere and return without accidental drift.

## Why SFR exists

AI agents may solve individual problems well yet lose track of the larger job during extended work. They can follow an interesting detour, forget an accepted commitment, repeat preparation that no longer helps, or fail to return after an interruption. The challenge is not always insufficient intelligence; it can be unreliable direction of that intelligence over time.

A rough analogy is **executive-function difficulties sometimes associated with ADHD**: sustaining a goal, managing distractions, keeping obligations in mind, and returning to an intended activity. This is an explanatory analogy, not a claim that AI agents have ADHD or that SFR works like medication.

**SFR is an engineering approach intended to remedy these AI-workflow failures.** Its lightweight guards are designed to preserve the governing objective and accepted obligations, allow justified detours, bring unfinished work back into focus, and prevent unsupported claims of completion.

SFR does not add intelligence, independently enforce behavior, provide a planner or memory store, or guarantee recovery when required context is unavailable. Its added effectiveness over native goal features has not yet been established by independent comparative tests.

## Install — choose an activation mode

SFR has **one runtime**, [`sfr.md`](sfr.md), and two optional ways to activate it. Choose **one** in each persistent instruction scope; do not stack conflicting activation bindings.

- **Explicit activation:** [`INSTALL.md`](INSTALL.md) — install once, then request `SFR: <task>`, `use SFR`, or `use SFR for <task>` when needed.
- **Automatic activation:** [`INSTALL-AUTO.md`](INSTALL-AUTO.md) — copy its instruction block into your assistant's persistent user-controlled instructions. It invokes SFR automatically for substantial tasks without an `SFR:` prefix, but skips greetings and simple queries.

For ChatGPT, use the available **Custom Instructions** field. If an explicit-only SFR instruction already occupies that scope, **replace** it with Auto rather than adding a second competing rule. Keep other unrelated instructions unchanged. Save the setting and test with a new chat; the document alone does not install anything.

**Auto controls:** `no SFR` turns Auto off for the current chat; `no SFR for this task` suppresses one task; `enable SFR` turns it back on. To disable Auto across future chats, remove its standing instruction from the host's settings. A chat-local toggle does not change other chats.

These are instruction bindings, **not** native triggers, background services, or guarantees of cross-chat continuity. Each actual activation must bind the current runtime, and cross-chat continuation still requires a recoverable SFR frontier.

For workspace/account-specific installation and verification, see [`INSTALL-BINDINGS.md`](INSTALL-BINDINGS.md) and [`ACCOUNT.md`](ACCOUNT.md).

## Minimal core

SFR keeps:

- the Root obligation / DONE;
- exactly one current focus per active frame;
- bounded Child attention departures;
- Park / Probe for side issues;
- material Child Return, including unresolved blockers without false DONE;
- **Return → Interpret → Integrate → Reconsider**;
- Resume only when the saved return point is still valid;
- route/blocker discipline and Root Close.

**Observability is ON by default** while SFR is active, using bounded checks at meaningful transitions. Optional observation can be turned off for the stated scope; a tracker, persistent logging, or independent reviewer is not required. Required verification remains required.

Reasoning methods, planning systems, tools, agents, and other capabilities remain external. They may operate naturally inside the current focus or supply the next valid focus under their own authority; SFR does not need to know their internals.

This lets SFR work alongside methods such as DesignSkeptic while keeping separation of concerns: the method owns semantic reasoning and SFR owns attention continuity.

## Runtime

`sfr.md` is the current maintained SFR runtime and semantic authority distributed by this repository. Maintained status does not establish independently verified cross-host or cross-invocation reliability.

`INSTALL.md` installs only a binding to the current runtime. It does not replace or copy SFR authority.

The canonical development source is maintained in Hartal and synchronized one-way into this repository. The external repository does not silently become upstream authority.

## License

MIT.
