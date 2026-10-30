# SFR Observability Profile — optional

**Status:** Optional, public, standalone companion to [SFR](sfr.md). **Not** a second SFR runtime, activation rule, persistence engine, account integration, or requirement for using SFR.

## Purpose and boundary

Observe whether an explicitly activated SFR workstream preserves its actual Root, current focus, bounded Child/parent return semantics and continuity across real handoffs during ordinary work. Distinguish model assertions, document-level inspection, scripted examples, and independently observed receiver behavior.

This profile defines **what to observe and how to label evidence**. The SFR runtime alone remains sufficient for standalone SFR use and retains all semantic authority for attention and return. This profile neither grants tools or account permissions nor changes Root DONE, action authorization, the current focus, or SFR activation. Use only when separately selected by the user or an authorized environment instruction. Do **not** load it merely because SFR is mentioned.

## Sampling: nearly invisible in normal work

Observe only decision-relevant boundaries that actually occur:
- **Activation/recovery:** explicit SFR invocation and actual source binding; initial Root, DONE, active Frame and focus recoverable.
- **Material transition:** focus supersession, Child opening, Child return, blocker/route revision, or claimed Root Close.
- **Generated handoff:** handoff prompt created for the same workstream versus a distinct bounded delegate; current frontier and receiver activation instructions.
- **Receiver continuation:** a *separate real invocation* receives an unedited handoff and independently binds its source, Root, active Frame/return chain, completed work and first valid action.
- **Contradiction or miss:** drift, stale or invalid source, lost activation, wrong return, repeated settled work, unjustified Close, or excessive tracking burden.
- **Human visibility (when sampled):** for substantial starts/recoveries, did the user receive a correct compact Root/Frame-path/focus/next-action orientation? For material work and Frame changes, were the actual action, reason, finding and consequence communicated without redundant tool-by-tool narration? Inspect the user-visible record, not an assistant's claim of having communicated. Score **communication sufficiency separately from semantic SFR correctness**; a polished status display alone is not proof that the correct frontier was maintained.

Do not insert observation checkpoints into every message or use tracking to create an SFR Child. No sampling or automation is implied for workstreams/chats the observer cannot actually access. When an observation opportunity occurs but logging is unavailable, keep work moving; give a compact optional observation only where it is useful and truthful.

## Evidence and outcomes

Every recorded event distinguishes:
- **OBSERVED_PASS:** a specific bounded behavioral expectation was directly observed with sufficient evidence for that event. Self-report alone is insufficient for independently verified behavior.
- **OBSERVED_FAIL:** a specific contradiction was directly observed with an evidence reference.
- **UNVERIFIED:** partial, ambiguous, scripted, self-assessed, inaccessible, or absent evidence. May add reason `NOT_RUN`, `SOURCE_UNAVAILABLE`, `INHERITANCE_UNKNOWN`, `NO_RECEIVER_TRANSCRIPT`, or `WRITE_UNVERIFIED`.
- **NOT_APPLICABLE:** the condition genuinely did not occur in the sampled event.

For each event, retain only what can change its interpretation:
`event_id`, `observed_at_utc`, `workstream_ref`, `event_type`, `handoff_pair_ref` (when any), `runtime_source_ref_or_blob`, `observer_role` (`sender`/`receiver`/`independent_evaluator`), `expected_invariant`, `actual_observation`, `verdict`, `evidence_ref`, `limitation_or_confound`, `follow_up`.

The observation record is **evidence**, not the semantic SFR frontier or source of truth. Avoid full transcripts by default. References to private conversations or internal URLs belong **only in the private log**, never in this public profile or public repository. Do not record credentials, sensitive task contents, or private file bodies. Preserve existing access controls; no automatic sharing.

## Handoff correctness: two-sided observation

**Sender observation:** assess whether the *actual, unedited* emitted same-workstream prompt explicitly instructs the receiver to continue under SFR, carries a source locator, Root/DONE, the single active Frame and existing return links, current focus/first valid action, completed work, material blockers and evidence references, and signals that it can be stale. A separate bounded delegate must not inherit SFR merely because its parent uses SFR.

**Receiver observation:** do not infer success from the sender's prompt. Observe a genuinely fresh receiver binding the applicable runtime and recovering the correct current frontier; its first justified action must match current authority and evidence. Score source access and semantic recovery separately. A receiver with only a predecessor runtime cannot claim it loaded the new one.

**Recursive observation:** use actual unaltered A→B and B→C handoffs. If B's work changes the focus or Child status, verify that C resumes from the *updated* frontier, not A's earlier snapshot. Freeze outputs before evaluation; do not supply the evaluator's expectations to participants. A same-context simulation, replay, or generated example is **UNVERIFIED** for independent cross-handoff reliability regardless of static assertions passed.

## Optional private log and account guidance

For everyday ChatGPT use, keep a privately controlled durable event table (for example a Google Sheet), with the fields above, and expose its exact authorized reference to an observing assistant only if needed. An observing assistant may append only with tool access and appropriate user authorization; verify the written row by readback before claiming it persisted. Failed or ambiguous writes remain `WRITE_UNVERIFIED`. Deduplicate by event ID; do not reconstruct past unobserved events from memory.

An optional ChatGPT Custom Instruction may say:

> When I explicitly use SFR, consult the current SFR source and, if accessible and authorized, its optional Observability Profile. At material transitions or handoffs, check Root/DONE, active Frame, current focus, Child returns, handoff activation, source identity and the first justified next action. Distinguish OBSERVED_PASS, OBSERVED_FAIL and UNVERIFIED; do not infer independent success from a simulation. Log minimal evidence to my private tracker only when connected, permitted and readback-verified. Never auto-activate SFR in unrelated work or interrupt normal work for per-message tracking.

Account Memory is a preference/retrieval aid, **not** an event store, cross-chat monitor, or guarantee that every SFR chat will be visited. ChatGPT Custom Instructions can supply a general preference, but cannot guarantee access to other chats or automatic writes. Neither this public profile nor account guidance may claim always-on surveillance, hidden invocation identities, or inherited state without evidence.

## Reporting and assessment

When requested, summarize a specified **observed sample** by event type, source version, and observer independence. Show counts of PASS, FAIL, UNVERIFIED and NOT_APPLICABLE and the evidence coverage. Report rates only with an explicit denominator of eligible **observed and verifiable** events, and separately disclose unobserved exposure. Never present sampled pass rate as a reliability estimate for all chats when selection bias or missing coverage is unbounded.

Escalate a concrete SFR-behavior failure for separate Skeptic/design analysis with exact evidence. A tracker finding never edits the SFR runtime or closes the observed Root. A new version of this profile follows its own owner/source/publication process; it is not silently substituted for the runtime.

**Stop condition for the profile:** observe the material boundary if evidence is accessible, record the smallest truthful result when authorized, and return to the user's original work. Do not let observation overhead displace the active SFR focus.
