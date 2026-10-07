# SFR — Session Frame Runtime

- **Original author:** Saffi Hartal
- **Status:** CURRENT EXPERIMENTAL RUNTIME / EXPLICIT-INVOCATION ONLY
- **Purpose:** keep substantial work attached to its Root obligation while attention moves, so useful reasoning can change focus without accidental drift and can return with the material result integrated into the right parent context.

SFR is a lightweight semantic attention runtime. It is not a planner, reasoning framework, task graph, workflow engine, or context-isolation mechanism.

SFR owns Root/focus continuity, bounded attention departure, semantic return, route recovery, and Root closure only. User, task, environment, safety, verification, planning, method, tool, and other governing authority remain external.

## Invocation

Formal invocation:

`SFR: <task or continuation instruction>`

Explicit equivalents include `use SFR`, `continue under SFR`, and `execute this under SFR`.

On invocation or recovery:

1. Read this exact current SFR runtime artifact as selected by the governing environment.
2. Bind the best current Root obligation/DONE, current valid focus, compact current state, blockers, parked material issues, and any decision-relevant route or continuation reference.
3. Recover the real frontier from authoritative sources, durable continuation material, evidence, and observable state when the session has drifted or become confused.
4. Treat handoffs and summaries as navigation/continuation material rather than authority over the sources they reference.
5. Preserve established completed work unless new evidence materially invalidates what its acceptance depended on.
6. If no valid current focus can be established, do not invent one. Return the smallest unresolved focus/route question to its exact owner, or expose the actual blocker when no valid resolving action remains.

SFR does not choose reasoning methods, tools, agents, or other capabilities. Those may operate naturally inside the current focus under their own authority.

## Core model

Maintain one logical Root Frame:

```text
ROOT
  obligation / DONE
  current focus
  compact current state
  blockers
  parked material issues
  route / continuation reference when needed
```

A substantial necessary attention departure may create a Child Frame:

```text
CHILD
  bounded obligation / DONE
  current focus
  parent return point
  relevant compact state + references
```

Exactly one frame is active for execution:
- Root when no Child is open;
- otherwise the deepest open Child.

Current focus is the smallest stable semantic obligation or question whose ordinary reasoning and actions can proceed without materially leaving it. Do not make the whole Root the focus by default when that would hide drift, and do not make every action its own focus.

Active Frame is derived from the existing parent/return links. Do not add a separate stack registry or lifecycle machine.

Current state is rewritten from present relevance rather than appended as history. Keep only what can materially change correct continuation: established conclusions or working position, completed work that constrains what must not be repeated, live uncertainty, material qualifications, unresolved dependencies, governing consequences, blockers, and decisive references.

Keep raw logs, large evidence bodies, detailed Child work, rejected alternatives, resolved uncertainty, and recoverable chronology outside active state unless their consequence remains material.

Compaction must preserve claim strength, tested scope, uncertainty, contradiction, and negative-claim limits.

## Current-focus rule

Ordinary reasoning and action inside the current focus require no SFR transition or per-action classification.

Current focus may advance without creating a Child only when:
- the prior focus completed, or was superseded or invalidated; and
- the successor focus is validly established by the current governing route/process, evidence interpreted within authority already held, or governing authority.

Completion or invalidation of the old focus is never by itself permission to choose an arbitrary new focus.

If a successor requires a planning, design, policy, preference, or other decision outside authority already held, return that decision to its exact owner.

A plan may supply current focus, successor focus, route, and completed-work structure when one exists. SFR does not require a plan as a separate state machine.

Another governing process may likewise supply or constrain the valid current focus. SFR follows the resulting valid focus without interpreting that process's internal state.

## Attention Gate

Use the Attention Gate only when an issue, opportunity, blocker, uncertainty, tool failure, or proposed work would materially pull execution away from a still-pending current focus.

Ask:

> Would leaving this unresolved materially affect valid completion of the current focus or Root DONE?

**NO** — Park it and continue the current focus.

**UNCLEAR** — Run a bounded Probe only far enough to classify materiality. A Probe does not authorize solving the discovered subject.

**YES** — Resolve inline when tiny and local; otherwise Push a Child Frame for the smallest decision-relevant obligation.

A parked item is reconsidered only when later evidence changes its materiality, or at Close for changed materiality.

Do not create a Child merely because a plan, method, or reasoning process contains several steps.

## Child Frame

A Child owns the smallest bounded question or obligation needed by its parent.

When a Child is active, the same Current-focus rule and Attention Gate apply inside it.

A substantial material departure inside a Child may Push a narrower Child. Existing parent/return links define the nested chain.

Do not widen a Child into the whole discovered subject unless established evidence shows the broader work is actually required by the parent.

Tool output, search results, tests, reasoning results, method results, implementation results, and Child results are candidate material. They do not directly mutate parent state and do not by themselves establish Root completion.

A Child must return every result that can materially change a parent premise, current focus, route, blocker, uncertainty, or DONE interpretation. Leave non-material detail below.

## Integrate → Return → Reconsider

When Child or bounded interruption work finishes:

1. Determine what the result actually establishes.
2. Integrate only the material consequence into the parent Current State.
3. Close the Child.
4. Return to the parent semantic context.
5. Reconsider the parent's current valid focus using the updated state.
6. When another governing process owns the meaning or validity of that focus, let that owner interpret the returned material and establish the valid continuation before dependent execution; SFR does not infer or mutate the owner's internal state.
7. Resume the saved parent return point only when reconsideration leaves it valid.
8. Otherwise follow the valid successor focus, revise the route within held authority, return the decision to its owner, or Close as appropriate.

Return is not automatic Resume. Exact memory of an old frontier never outranks newer established meaning.

The purpose of a Child is to protect and inform its parent, not to become the new mission.

## Route revision

Revise the route when established evidence makes the current route materially invalid, infeasible, or materially dominated for achieving Root DONE.

Replace only the affected route and preserve unaffected established state and evidence.

SFR may revise a route only within authority already held. Otherwise return the route question to the exact planner, design owner, user, or other governing authority.

Root obligation/DONE changes only when governing authority actually changes the requirement. New evidence may change understanding and route without silently changing the mission.

## Material blocker and alternative route

When a material blocker to the current focus is established, surface it promptly before non-trivial workaround search. State concisely:
- the blocked focus or route;
- the established evidence;
- what the blocker prevents;
- whether an already-authorized valid alternative is known.

If a blocker, repeated failure, or material inefficiency materially weakens the basis of the current focus or route, integrate that evidence and reconsider the affected focus before dependent alternative work.

If an already-authorized Root-relevant route with meaningful expected gain is known, follow it under proper authority.

If an alternative route's validity is unclear, run only a bounded Probe sufficient to establish whether it is Root-relevant, within held authority or properly returnable to its owner, and has meaningful expected gain relative to cost.

Repeated retries, widening workaround search, or new infrastructure require new evidence or a materially changed condition that increases expected decision value. Do not keep searching merely because another workaround can be imagined.

### Break glass

Use break-glass only when:
- the accountable owner explicitly authorizes break-glass routing for the active obligation;
- the normal route is materially blocked; and
- current evidence establishes that the blocking failure does not discriminate the relevant claim, or governing verification authority permits an equivalent smaller evidence route.

Owner authorization selects the route; it does not supply missing evidence or make an unsupported claim true.

Then:
- use only the smallest already-authorized Root-relevant alternative;
- preserve every semantic, safety, authority, evidence, and DONE invariant;
- state the bypassed route and evidence supporting non-discrimination or equivalent verification;
- perform only the cheapest independent postflight sufficient to catch a material false positive or false negative;
- keep residual unproved qualification explicit.

Break-glass expires after that bounded route and does not become the new default. It never authorizes bypass of a mandatory semantic, safety, authority, evidence, or DONE gate; invention of authority; silent weakening of the claim; or repeated workaround search.

If no valid continuation can be established, report or escalate the blocker and safe options to the exact owner, then stop execution of that active obligation.

Do not substitute unrelated useful work merely because the required path is blocked.

## Blocked

A failed tool, unavailable route, or unresolved local issue does not by itself make the Root BLOCKED.

Root is BLOCKED only when Root remains unsettled and, after the applicable bounded route check, no currently valid action with meaningful expected gain remains.

A failed route is not permission for silent workaround hunting.

## External composition and context

SFR remains independently usable without another method or composition layer.

When the governing environment activates a stronger composition contract, follow that contract at the boundary. Another component may expose a current/successor obligation, opaque continuation state or reference, or authoritative interpretation of returned evidence/blockers; SFR treats the resulting valid obligation as current focus and does not interpret or mutate component-owned state.

When work crosses a real invocation, delegation, resumption, or handoff boundary, follow the governing environment's context rules when present while preserving Root, current-focus, and return semantics.

A Child Frame is a semantic scope. It is not proof of fresh context, isolation, delegation, or a separate process.

SFR does not claim to reclaim consumed context, know hidden remaining capacity, or infer unobservable context/isolation properties.

## Close

Before claiming terminal completion, compare observable reality against Root DONE and check:
- required integration;
- required validation;
- unresolved blockers;
- parked items whose materiality may have changed;
- whether local success is being mistaken for Root completion.

If Root DONE is not satisfied, continue from the valid current focus or report the actual blocker.

## Status and steerability

At a material pause, recovery point, blocker, or user status request, be able to state concisely:
- Root DONE;
- current focus;
- established completed work;
- current blocker, if any;
- parked material issues, if any;
- next valid action;
- when a Child is active: that Child's bounded DONE and parent return point;
- any continuation reference required by an activated external contract.

During sustained work, surface a concise progress signal at a natural substantive boundary when more substantive work remains and the user has not otherwise received meaningful visibility. Also surface a material change in interpretation, route, blocker, or next action before substantial dependent continuation when user feedback could affect the route.

Progress/status is derived communication only. Do not create a timer, periodic checkpoint, work board, transcript, progress percentage, or new SFR state merely to prove activity.
