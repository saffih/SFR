# SFR — Session Frame Runtime

**Original author:** Saffi Hartal

SFR is a lightweight execution-focus runtime for substantial AI work. It keeps execution attached to the root obligation while allowing necessary interruption, bounded child work, replanning, blocker handling, and exact return to the parent task.

## Runtime

`sfr.md` is the complete standalone SFR runtime.

Use it by supplying the exact current runtime to the AI environment and invoking one of:

- `SFR: <task or continuation instruction>`
- `use SFR`
- `continue under SFR`
- `execute this plan under SFR`

SFR is intentionally small. It does not require DesignSkeptic, Skeptic, WELL, TP, or Hartal-specific repository paths for standalone use.

## Publication model

This repository is a distribution view of the canonical SFR runtime maintained in Hartal development. Publication is one-way into this repository; external repository state does not silently become source authority.

The synchronized source surface is intentionally limited to `sfr.md`. This README and the repository license are maintained at the destination.

## License

MIT.
