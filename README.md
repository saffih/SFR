# SFR — Session Frame Runtime

**Original author:** Saffi Hartal

SFR is a lightweight semantic-attention runtime for substantial AI work.

Its job is simple: keep work attached to the Root obligation while attention changes, so necessary reasoning can move elsewhere and return without accidental drift.

## Install

Choose **one** installation mode (both use the same `sfr.md` runtime):

- **[Explicit SFR](INSTALL.md)** — invoke SFR by typing `SFR:` or `use SFR`.
- **[SFR Auto](INSTALL-AUTO.md)** — opt in to automatic SFR activation for meaningful goals, substantive research, and other nontrivial tasks. Say `no SFR` or `disable SFR` to stop it in the current chat; `enable SFR` to resume. Install the standing instruction in a host-supported persistent instruction location to use it in future chats.

For explicit mode, use SFR naturally:

```text
use SFR for investigate why this deployment keeps failing and fix it
```

or:

```text
SFR: continue the current design work until the open issue is resolved
```

A bare `SFR` or `use SFR` applies SFR to the current active task when one can be validly established.

## Minimal core

SFR keeps:

- the Root obligation / DONE;
- exactly one current focus per active frame;
- bounded Child attention departures;
- Park / Probe for side issues;
- material return upward;
- **Integrate -> Return -> Reconsider**;
- Resume only when the saved return point is still valid;
- route/blocker discipline and Root Close.

Reasoning methods, planning systems, tools, agents, and other capabilities remain external. They may operate naturally inside the current focus or supply the next valid focus under their own authority; SFR does not need to know their internals.

This lets SFR work alongside methods such as DesignSkeptic while keeping separation of concerns: the method owns semantic reasoning and SFR owns attention continuity.

## Runtime

`sfr.md` is the current SFR runtime and semantic authority distributed by this repository.

`INSTALL.md` and `INSTALL-AUTO.md` are alternative activation bindings to the current runtime, not copies or competing runtime authority. Auto behavior depends on the assistant actually receiving and honoring the installed user instruction; it is not a platform-level always-on switch.

The canonical development source is maintained in Hartal and synchronized one-way into this repository. The external repository does not silently become upstream authority.

## License

MIT.
