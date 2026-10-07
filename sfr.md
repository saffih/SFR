# SFR — Session Frame Runtime

- **Original author:** Saffi Hartal
- **Status:** CURRENT EXPERIMENTAL RUNTIME / EXPLICIT-INVOCATION ONLY
- **Purpose:** keep one active root work session attached to an already-understood obligation and usable plan while allowing necessary discovery, interruption, and replanning without losing the parent work.

SFR is a lightweight execution-focus runtime. It is not TP, not a task graph, not a workflow engine, and not a fresh-context mechanism.

SFR owns execution-focus semantics only. It has no mandatory dependency on another method for standalone use. A governing environment may additionally supply composition, context-transfer, repository, safety, verification, or tool authority; those authorities remain external and govern only their own scope.

## Invocation

Formal invocation:

`SFR: <task or continuation instruction>`

Explicit equivalents include `use SFR`, `continue under SFR`, and `execute this plan under SFR`.

On invocation:

1. Read this exact current SFR runtime artifact as selected by the governing environment; do not substitute memory, summaries, or a different copy.
2. Bind the best current task authority, root obligation/DONE, governing plan or plan reference, compact current state, current plan step, blockers, and relevant parked discoveries.
3. If the session has already drifted or become confused, recover the real frontier from current authoritative sources, durable continuation material, evidence, and observable task state before doing new substantive work.
4. Treat any existing handoff as navigation and continuation material, not as authority over the sources it references.
5. Preserve established completed work unless new evidence materially invalidates the acceptance or result it depended on.
6. If a usable current plan/current step cannot be established, return the planning question to the role that owns it before substantive execution.

SFR does not automatically invoke Skeptic, DesignSkeptic, TP, Lead, or another framework. If the governing task requires one, use its current authority and treat its result as candidate material until its consequence is integrated into the Root state.

## Optional method execution-control profile

SFR can optionally compose with a governing method through a method execution-control profile. For SFR's side of that boundary, the governing method owns and exposes its current executable obligation and authoritative interpretation of method-owned continuation state; SFR controls execution around that obligation, preserves only the minimum continuation state or resolvable reference needed for correct continuation, and treats that state as opaque except for identity, persistence, routing, and equality facts the method explicitly exposes. A governing environment may impose a stronger composition contract, which remains authoritative for composition semantics.

The profile activates only when the current composition binding explicitly activates it—including a governing invocation that asks SFR to execute a conforming method. Mere co-presence or support does not activate the profile.

While the profile is active, the governing method's current executable obligation is the effective active obligation inside whichever SFR frame is active. The Root current plan step or Child bounded DONE remains that frame's terminal obligation. When the method completes or replaces its executable obligation and exposes a successor, refresh the effective active obligation and compact control state to the successor before dependent execution. This is ordinary method progression, not Interruption, Child, or Replan, and does not require per-action polling, a new Method Frame, or a new SFR plan step.

If a method-governed obligation is interrupted, preserve that opaque continuation state or reference with the parent return point.

When material interruption or Child work returns, give the material result or blocker to the governing method before dependent continuation. If a material blocker is established directly against the method-governed active obligation, surface it immediately and return the blocker fact to the governing method before taking any alternative route whose validity depends on method state. Resume the stored method frontier only if the governing method leaves it valid; otherwise follow the replacement, reset, or upstream-return obligation the method exposes. Any remaining alternative-route search still follows SFR's blocker and authority rules.

This profile is optional. SFR remains independently usable without it, does not automatically invoke a governing method, and does not interpret, advance, reset, qualify, or complete another method.

## Root Frame

Maintain one compact logical Root Frame:

```text
ROOT
  obligation / DONE
  governing plan reference
  current state
  current plan step
  blockers
  parked discoveries
```

At any moment exactly one frame is active for execution:

- Root when no Child is open; its terminal obligation is the current plan step.
- Otherwise the deepest open Child; its terminal obligation is that Child's bounded DONE.
- If the active Root or Child is method-governed under the activated profile, the governing method's current executable obligation is the effective active obligation inside that same frame.

Active Frame is a derived designation from existing parent/return links, not a separate stack object or lifecycle state.

Current state is rewritten from present relevance, not appended as history.

Keep only what can materially change correct continuation: established conclusions or working position, established completed work that constrains what must not be repeated, live uncertainty, material qualifications, unresolved dependencies, governing consequences, blockers, and decisive references.

Keep raw logs, large evidence bodies, detailed child work, rejected alternatives, resolved uncertainty, and recoverable chronology outside the active frame unless their consequence is still material.

Compaction must preserve claim strength, tested scope, uncertainty, contradiction, and negative-claim limits.

A separate SFR state file is not required when the current project already has sufficient continuation material. Do not create a competing handoff or state authority merely for SFR.

## Default

Follow the current valid plan while Root is active. When a Child is active, preserve and pursue that Child's bounded terminal obligation. When the active frame is method-governed under the optional profile, follow the governing method's current executable obligation as the effective active obligation inside that frame.

Ordinary work inside the effective active obligation needs no SFR transition and no per-action classification.

Refresh the compact Root state only when a material boundary makes stale control state capable of changing the next valid action, such as a material plan-step completion, a governing-method frontier change under the optional profile, blocker change, Child Push/Pop, Replan, authoritative scope change, or immediately before Close.

## Interruption Gate

Use the gate only when a discovery, issue, opportunity, blocker, tool failure, uncertainty, or proposed work would pull execution away from the active obligation.

Ask:

> Would leaving this unresolved materially affect valid completion of the active obligation or Root DONE?

**NO** — Park it and continue the governing plan.

**UNCLEAR** — Run a bounded Probe only far enough to classify materiality. A Probe does not authorize solving the discovered subject.

**YES** — Resolve inline when tiny and local; otherwise Push a Child Frame.

A parked item is reconsidered when later evidence changes its materiality and is checked at Close only for changed materiality.

## Child Frame

A Child Frame owns the smallest decision-relevant question or obligation required by its parent.

```text
CHILD
  bounded obligation / question
  DONE
  parent return point
  only relevant state + references
```

Do not create a child merely because a plan has multiple steps.

When a Child is active, the same Interruption Gate applies to that Child's active obligation. A substantial material interruption may Push another Child only for the smallest decision-relevant question. Existing parent/return links define the nested chain; do not add a separate stack registry.

Do not widen a child into the whole discovered subject unless established evidence shows the broader work is required by the parent.

Tool output, search results, tests, Skeptic findings, implementation results, and child results are candidate material. They do not directly mutate the parent state and do not by themselves establish Root completion.

If a child discovers something that materially changes a parent premise, route, blocker, or DONE interpretation, surface that truth upward.

## Integrate → Pop → Resume

When interruption or child work finishes:

1. Determine what the result actually establishes.
2. Integrate only the material consequence into the parent Current State.
3. Close the child.
4. Resume the exact parent/current-plan return point.
5. Replan instead only when the integrated evidence requires a route change.

The purpose of the child is to return control to the parent, not to become the new mission.

## Replan

Replan when established evidence makes the current route materially invalid, infeasible, or materially dominated for achieving Root DONE.

Replace the affected route rather than appending a correction chain, and preserve unaffected established state and evidence.

SFR may repair the route only within planning authority already held by the current task role. Otherwise return the planning/design choice to the exact owner.

Root obligation/DONE changes only when the user or another governing authority actually changes the requirement. A new user instruction that materially changes scope or DONE is a Root rebind, not an ordinary Replan.

## Material blocker and alternative route

When a material blocker to the active obligation is established, surface it promptly before beginning any non-trivial alternative-route search. State concisely:

- the blocked route;
- the established evidence;
- what the blocker prevents;
- whether an already-authorized valid alternative is known.

If a material blocker, repeated failure, or material inefficiency could materially weaken a route selected by an active governing method, return that evidence to the method for route re-evaluation before non-trivial workaround search; if that method is InnoSkeptic, this reopens candidate comparison.

If an already-authorized Root-relevant route with meaningful expected gain is known, follow it under the proper authority.

If the validity of an alternative route is unclear, run only a bounded Probe sufficient to establish whether it is Root-relevant, within held authority or properly returnable to its exact owner, and has meaningful expected gain relative to its cost. The Probe does not authorize solving the alternative subject.

Repeated retries, widening workaround search, or creation of new infrastructure require new evidence or a materially changed condition that increases expected decision value. Do not keep searching merely because another workaround can be imagined.

### Break glass

Use break-glass only when the accountable owner explicitly authorizes break-glass routing for the active obligation, the normal route is materially blocked, and current evidence establishes that the blocking failure does not discriminate the relevant claim or governing verification authority permits an equivalent smaller evidence route. Owner authorization selects the route; it does not supply missing evidence or make an unsupported claim true.

Then:
- use the smallest already-authorized Root-relevant alternative;
- preserve every semantic, safety, authority, and DONE invariant;
- state which normal route is bypassed and the evidence establishing why its failure is non-discriminating;
- perform only the cheapest independent postflight that can catch a material false positive or false negative;
- keep any residual unproved qualification explicit.

Break-glass expires after that bounded route and does not become the new default. It does not authorize bypassing a mandatory semantic, safety, authority, or DONE gate; inventing new authority; weakening the claim; or beginning another workaround search.

If no already-authorized valid continuation is known and the bounded route Probe does not establish one, report or escalate the blocker and safe options to the exact planner, design owner, user, or other governing authority, then stop execution of that active obligation.

Do not substitute unrelated useful work merely because the required path is blocked.

## Blocked

A failed tool, unavailable route, or unresolved local issue does not by itself make the task BLOCKED.

Root is BLOCKED only when it remains unsettled and, after the applicable bounded route check, no currently valid action with meaningful expected gain remains.

A failed route is not permission for silent workaround hunting, and failure to establish a valid continuation must remain visible as escalation rather than hidden effort.

## Close

Before claiming terminal completion, compare observable reality against Root DONE and check:

- required integration
- required validation
- unresolved blockers
- parked items whose materiality may have changed
- whether any local success is being mistaken for task completion

If Root DONE is not satisfied, continue or report the actual blocker.

## Context and boundaries

SFR governs one active root work conversation or control thread. It does not claim that every subordinate operation remains in one model invocation.

SFR does not define a general context-transfer protocol. When work crosses a real invocation, delegation, resumption, or handoff boundary, follow the governing environment's context rules when present while preserving Root control and exact return semantics. If no external context contract applies, preserve enough decision-critical state or resolvable references for correct continuation across the chosen boundary.

A Child Frame is a semantic scope; it is not proof of fresh context, isolation, delegation, or a separate process.

SFR does not claim to reclaim consumed context, know hidden remaining capacity, or infer fresh-context or isolation properties that are not observable.

## Status

During sustained active work, preserve human steerability when the environment permits incremental user-visible communication. At a natural substantive-work boundary, if more substantive work remains and the user has not otherwise received meaningful visibility into that work, surface a concise progress signal before continuing. Also surface a material change in interpretation, route, blocker, or next action before substantial dependent continuation when user feedback could affect the route.

A progress signal normally states only the active obligation, what materially changed since the prior signal or that nothing material changed, decision-relevant uncertainty or blocker when useful, and the next action. Do not emit a tool transcript, hidden reasoning trace, repetitive heartbeat, or new SFR checkpoint merely to prove activity. Progress signaling is derived communication only and creates no new SFR state, timer, tool-count schedule, planning authority, or completion authority.

At a material pause, recovery point, blocker, or user status request, be able to state concisely:

- Root DONE
- established completed work
- current plan step
- current blocker, if any
- parked material issues, if any
- next valid action
- when a Child is active: that active Child's obligation and its parent return point
- when the active frame is method-governed: the governing method's current executable obligation, plus an opaque continuation reference only when needed to identify or resume that exact frontier

Do not emit a process transcript merely to prove SFR use.
