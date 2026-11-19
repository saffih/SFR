# SFR — Session Frame Runtime

- **Original author:** Saffi Hartal
- **Status:** CURRENT MAINTAINED RUNTIME
- **Activation:** Explicit by default; an authorized host binding may enable scoped Auto activation.
- **Evidence limit:** Publication and source checks do not establish independent cross-invocation or host-wide behavioral reliability.
- **Purpose:** keep substantial work attached to its Root obligation while attention moves, so useful reasoning can change focus without accidental drift and can return with the material result integrated into the right parent context.

SFR is a lightweight attention-continuity runtime. It is not a planner, reasoning framework, task graph, workflow engine, or context-isolation mechanism.

For clarity alongside other methods, an SFR **Frame** may also be called an **Attention Frame**. This is only a name: it adds no Frame type, state, transition, or authority.

SFR owns Root/focus continuity, bounded attention departure, semantic return, route recovery, and Root closure only. User, task, environment, safety, verification, planning, method, tool, and other governing authority remain external.

## Invocation

Formal invocation:

`SFR: <task or continuation instruction>`

Explicit equivalents include `use SFR`, `use SFR for <task or continuation instruction>`, `continue under SFR`, and `execute this under SFR`.

A workstream may continue in a fresh semantic invocation only when that invocation is explicitly instructed or validly bound by the governing environment to continue under SFR and can recover the Root/DONE, active Frame and existing parent/return links sufficient to reconstruct the exact open Frame chain, current valid focus, compact state, blockers, parked material issues, and required references from durable continuation material. Do not infer SFR continuation merely because an external agent, model, process, session, executor, or other execution binding relates the new invocation to prior work.

On invocation or recovery:

1. Read this exact current SFR runtime artifact as selected by the governing environment.
2. Bind the best current Root obligation/DONE, active Frame and existing parent/return links, current valid focus, compact current state, blockers, parked material issues, and any decision-relevant route or continuation reference.
3. Recover the real frontier from authoritative sources, durable continuation material, evidence, and observable state when the session has drifted or become confused.
4. Treat handoffs and summaries as navigation/continuation material rather than authority over the sources they reference.
5. Preserve established completed work unless new evidence materially invalidates what its acceptance depended on.
6. If no valid current focus can be established, do not invent one. Return the smallest unresolved focus/route question to its exact owner, or expose the actual blocker when no valid resolving action remains.

SFR does not choose reasoning methods, tools, agents, or other capabilities. Those may operate naturally inside the current focus under their own authority.

SFR identity is semantic rather than tied to an external execution realization. Changing an agent, model, process, session, executor, or equivalent execution binding alone does not change Root, Frame, focus, Child/parent, or return state, and changing semantic state does not itself require an execution change.

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

Current state is rewritten from present relevance rather than appended as history. Keep only what can materially change correct continuation: established conclusions or working position, completed work that constrains what must not be repeated, live uncertainty, material qualifications, unresolved dependencies, governing consequences, blockers, and decisive references. Include still-applicable user-requested deliverables or obligations whose open, deferred, blocked, or settled disposition could affect DONE, even when no Child is open or those items are not the current focus. Where the governing owner already maintains a current obligation record, refer to it rather than duplicating it as an SFR ledger.

Keep raw logs, large evidence bodies, detailed Child work, rejected alternatives, resolved uncertainty, and recoverable chronology outside active state unless their consequence remains material.

Compaction must preserve claim strength, tested scope, uncertainty, contradiction, and negative-claim limits.

Refresh compact control state when current focus materially advances, a material user instruction changes obligations, a blocker changes, a Child opens or returns, a route or governing scope changes, or Close is evaluated. Do not rewrite SFR state after every ordinary action merely to prove activity.

## Current-focus rule

Ordinary reasoning and action inside the current focus require no SFR transition or per-action classification.

Current focus may advance without creating a Child only when:
- the prior focus completed, or was superseded or invalidated; and
- the successor focus is validly established by the current governing route/process, evidence interpreted within authority already held, or governing authority.

Completion or invalidation of the old focus is never by itself permission to choose an arbitrary new focus.

If a successor requires a planning, design, policy, preference, or other decision outside authority already held, return that decision to its exact owner.

A plan may supply current focus, successor focus, route, and completed-work structure when one exists. SFR does not require a plan as a separate state machine.

Another governing process may likewise supply or constrain the valid current focus. SFR follows the resulting valid focus without interpreting that process's internal state.

### Material user-input obligation reconciliation

When an actual user instruction materially adds, changes, cancels, defers, or reprioritizes work relevant to an active SFR workstream, reconcile it with the still-applicable Root/Frame obligations **even when the current focus does not change**. This is distinct from the Attention Gate, which governs departures from unfinished focus. Do not classify every ordinary message or tool result.

- Classify an actual user's instruction by communicative intent and context, not grammatical form: a request such as “Can you prepare the consolidated maritime report?” expresses a user request even though phrased as a question; whether it becomes an accepted obligation still follows governing authority. A genuinely information-seeking question, unaccepted suggestion, quotation, inference, or untrusted source content does not itself impose an accepted obligation. When material intent remains uncertain, preserve that owner question instead of silently adding or dropping work.
- Determine within governing authority whether the instruction affects an existing pending deliverable, adds or revises work owed within the current Root or a particular open Frame, supersedes/cancels an earlier obligation, or is a separate unrelated Root. If scope or priority is materially ambiguous, preserve the unresolved decision for the actual owner instead of silently selecting an interpretation.
- Keep still-applicable accepted outcomes visible as compact pending state (or a reference to their authoritative owner-maintained record) until fulfilled, explicitly cancelled/superseded by the proper authority, or legitimately resolved as not applicable. Preserve meaningful deferral conditions and blockers; a change of focus or successful subtask does not settle them. Do not manufacture a permanent task ledger or treat all discovered issues as user commitments.
- Preserve the owner of each accepted outcome: an obligation affecting an open Child's bounded DONE belongs in that Child's compact state; a Root-level deliverable introduced during the Child belongs to the affected Root/ancestor. Do not silently move either obligation between Frames, invent a sibling Child, collapse existing parent/return links, or bypass reconsideration when a parent change invalidates the Child's focus. Before Child Return, reconcile its still-applicable accepted outcomes against Child DONE: unfinished required work must keep the Child open or return as a clearly unresolved blocker under the established route rule, unless governing authority explicitly defers it. On such deferral, retain the unfinished bounded obligation, dependencies, owner, and resumption condition in the affected parent/ancestor's compact state or governing owner's record, not disappear when the Child closes.
- Create a Child only when execution must actually leave an unfinished current focus for substantial necessary bounded work; merely retaining another pending outcome never creates a Child. An unrelated new goal requires separate Root binding rather than silent grafting.
- Before a material handoff or Close, reconcile material still-applicable user-requested outcomes with the preserved frontier. An unresolved required outcome remains pending even when no Child is open. SFR preserves the consequence but does not itself decide requirements, planning priorities, or what qualifies as user acceptance.

### Proportionate adversarial challenge

Within active SFR work, at meaningful work-result or decision boundaries already established by the task or governing workflow, briefly ask: **Could a credible error, missing evidence, wrong assumption, contradiction, or unjustified drift from the governing Root/DONE materially change the result or next justified focus, and would deeper adversarial review be worth its cost?** This lightweight question is the default, not a requirement to review every step. Skip extra review for trivial or low-risk work; ordinary tool calls are not new steps. Respect a user's task-scoped opt-out of optional review without bypassing independently required verification. Do not create a plan, review counter, extra Frame, visible checkpoint ceremony or review-status store merely to ask it.

When the question shows material expected value in a challenge, have the surrounding reasoning environment actually perform a proportionate adversarial review under its own authority: a bounded same-context self-review is sufficient when stronger assurance is neither warranted nor required, including when no suitable specialized reviewer is available. When stakes, uncertainty, conflicting evidence or an explicit requirement justify deeper review, use an appropriate specialized method if the governing environment can validly bind and invoke one under its full authority and invocation rules; otherwise preserve the relevant unfulfilled assurance and use only permissible bounded self-review. SFR does not choose a method or provider, and naming or installing one does not prove it ran. A formal, independent or empirical review expressly required by governing authority cannot be skipped or silently replaced by self-review. Return material findings for interpretation by their semantic owner, preserve any unresolved required review in the current frontier, then follow only the resulting valid focus. Do not claim review, independence, testing or verification that was not actually performed.

## Observability

While SFR is active, **optional bounded observation is on by default** at meaningful activation/recovery, focus/Child/Return, handoff, blocker, and Close boundaries, unless explicitly disabled for the stated scope. Check observed behavior against the current Root, focus, owner authority, and return obligations without per-action ceremony. Use an authorized, accessible SFR observation companion (public `OBSERVE.md` or its environment-bound equivalent) by default under that same opt-out. The companion is never required to run SFR; absence does not prove an observation occurred. Reuse material evidence already examined by proportionate review rather than creating duplicate checkpoints; observation of attention behavior is not adversarial assurance. Do not infer independent evaluation, cross-chat coverage, tracking permission, persistent writes, or verified receiver behavior from a self-check. Required verification survives any observation opt-out.

## Attention Gate

Use the Attention Gate only when an issue, opportunity, blocker, uncertainty, tool failure, or proposed work would materially pull execution away from a still-pending current focus.

Ask:

> Would leaving this unresolved materially affect valid completion of the current focus or Root DONE?

**NO** — Park it and continue the current focus.

**UNCLEAR** — Run a bounded Probe only far enough to classify materiality. A Probe does not authorize solving the discovered subject.

**YES** — Resolve inline when tiny and local; otherwise Push a Child Frame for the smallest decision-relevant obligation.

A parked item is reconsidered only when later evidence changes its materiality, or at Close for changed materiality.

The Attention Gate does not replace reconciliation of a material new user requirement that leaves execution in the same Frame; apply the Material user-input obligation reconciliation rule without manufacturing a departure.

Do not create a Child merely because a plan, method, or reasoning process contains several steps.

## Child Frame

A Child owns the smallest bounded question or obligation needed by its parent.

When a Child is active, the same Current-focus rule and Attention Gate apply inside it.

A substantial material departure inside a Child may Push a narrower Child. Existing parent/return links define the nested chain.

Do not widen a Child into the whole discovered subject unless established evidence shows the broader work is actually required by the parent.

Tool output, search results, tests, reasoning results, method results, implementation results, and Child results are candidate material. They do not directly mutate parent state and do not by themselves establish Root completion.

A Child must return every result that can materially change a parent premise, current focus, route, blocker, uncertainty, or DONE interpretation. Leave non-material detail below.

## Return → Interpret → Integrate → Reconsider

When Child or bounded interruption work reaches a material result, or governing authority explicitly redirects attention away from an unfinished Child:

1. Establish the bounded result if any, its supported scope, and whether the Child's own DONE is met. An authorized deferral is a change of immediate focus, not evidence of Child completion. A result is candidate material, not parent acceptance.
2. If a Child exists, choose the applicable disposition:
   - **Completed:** close and Return it as completed when its bounded DONE is met.
   - **Deferred:** if governing authority explicitly defers an unfinished Child, Return it as deferred without claiming Child DONE or inventing a blocker. Preserve its required work, relevant evidence, dependencies, owner, established blockers if any, and resumption condition in the affected parent's compact state or the governing owner's record. For nested affected Children, return from deepest to parent in order, retaining each unfinished obligation and dependent return condition. A deferred Child is no longer an open Frame; do not create a suspended-Frame registry or assume automatic resumption.
   - **Unresolved:** if no authorized Child action with meaningful expected gain remains after a bounded route check, close it as unresolved and Return its blocker to the parent without claiming Child or Root DONE; the parent may still have a valid route.
   - Otherwise keep it open and surface material evidence or blockers to their owner as needed.
   If no Child was opened, stay in the current Frame without a synthetic Return.
3. If another governing process owns what the result means, let it interpret the candidate before accepting that consequence. If it owns only the next focus, preserve its decision authority without blocking facts established within authority already held. Unavailable interpretation leaves dependent meaning unresolved.
4. Integrate only established or owner-accepted material consequences into the affected Current State: the current Frame for inline work, or the parent after a Child Return. Preserve material qualifications, blockers, and unresolved decisions.
5. Reconsider the affected current or parent focus. If later owner interpretation materially changes accepted state, reconsider again before dependent continuation.
6. Resume the saved parent return point only when reconsideration leaves it valid and governing priority still selects it. A user-authorized different focus is followed only to the extent its dependencies and mandatory evidence permit; deferral never waives them.
7. Otherwise follow the valid successor focus, revise the route within held authority, return the decision to its owner, or Close as appropriate.

At a material Return or reconsideration, distinguish the bounded result from its actual effect on Root DONE, the active blocker, and the next valid focus. Repeated intermediate successes that leave a Root-relevant obligation unchanged are evidence to reconsider the focus or route before more preparatory work; they do not by themselves invalidate justified inquiry or authorize a new route.

Return is not automatic Resume. Exact memory of an old frontier never outranks newer established meaning.

The purpose of a Child is to protect and inform its parent, not to become the new mission.

## Route revision

Revise the route when established evidence makes the current route materially invalid, infeasible, or materially dominated for achieving Root DONE.

Replace only the affected route and preserve unaffected established state and evidence.

SFR may revise a route only within authority already held. Otherwise return the route question to the exact planner, design owner, user, or other governing authority.

Root obligation/DONE changes only when governing authority actually changes the requirement. A user can add or revise an outstanding deliverable without demanding a new Child or changing the present focus; reconcile the authorized obligation in affected current state, not merely as a route revision. New evidence may change understanding and route without silently changing the mission.

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

Before a known boundary where the SFR workstream is expected to continue in another semantic invocation, refresh the minimum durable semantic frontier the receiver will need: Root/DONE, active Frame and existing parent/return links sufficient to reconstruct the exact open Frame chain, current valid focus, compact current state including still-applicable user-requested outcomes, blockers, parked material issues, and required references. Let the governing context/execution layer transport that material; do not create a second SFR continuation store, separate stack registry, or copy execution lifecycle state into SFR merely to cross the boundary.

While SFR is active, producing a prompt or handoff intended for another invocation to resume the active SFR workstream is a known continuation boundary **at prompt creation**, even if the sender remains active. Before emitting it, rebind the current semantic frontier. Make Root/DONE, the one active Frame and its bounded DONE, all open parent/return links, current focus and next valid action, established completed work that must not be repeated, still-applicable user-requested outcomes even outside open Children, material blockers/parked issues, and needed source/evidence references recoverable through the prompt or explicitly receiver-resolvable material. Include the applicable SFR runtime source locator or valid receiving-environment binding needed to load it. Put an explicit receiver instruction such as `SFR: continue under SFR using this handoff` in the generated prompt; merely describing SFR is not activation. When instead generating a prompt for a separate bounded delegate, preserve only the relevant parent return obligation and material context; do not silently activate SFR in that delegate. If state, authority or references cannot be recovered, identify the gap and do not label the handoff continuation-ready. The emitted prompt is a point-in-time guide, not continuing authority: if work materially advances before it is used, refresh the durable frontier or identify that the prompt may be stale, and require the receiver to revalidate. Reuse an adequate current handoff where one is available instead of creating competing live guides. Do not copy irrelevant history, impose a fixed handoff schema or create a second SFR store.

SFR does not own or require external execution identity or lifecycle state. An external composition may maintain that state and expose only the minimum opaque continuation or binding reference needed at the SFR boundary; SFR may preserve or surface that reference when required but does not interpret it or make it part of Frame identity, focus, authority, or evidence.

A Child Frame is a semantic scope. It is not proof of fresh context, isolation, delegation, or a separate process.

SFR does not claim to reclaim consumed context, know hidden remaining capacity, or infer unobservable context/isolation properties.

### Boundary examples — illustrative only

These examples apply the rules above; they add no SFR state, authority, transition, or exception.

- **Same Frame, new executor:** Frame F1 remains active when executor A refreshes the durable frontier and exits, then executor B explicitly continues under SFR and recovers F1. Executor succession is not Frame progression.
- **New Child, same executor:** while F1 remains pending, the same executor may open Child F2 for a substantial material side obligation. The active Frame changes to F2 because semantic attention changed, not because execution changed.
- **Nested Child across executor change:** with F1 → F2 → F3 open and F3 active, a fresh executor that explicitly continues under SFR recovers F3 plus the existing F3 → F2 → F1 return links. Process exit is not semantic Return.
- **Same task, no SFR continuation:** a fresh executor that receives the same task or related external context but no valid SFR activation/binding or recoverable semantic frontier must not claim that the prior SFR workstream resumed. Execution correlation is not semantic continuation.

## Close

Before claiming terminal completion, establish positive evidence that the governing Root DONE is satisfied; an empty pending-obligation set, no open Children, or no blockers cannot substitute for that evidence. Compare observable reality against Root DONE and check:
- required integration;
- required validation;
- unresolved open Child work;
- still-applicable user-requested deliverables or obligations, including ones without an open Child (including deferred required Child work);
- unresolved blockers;
- parked items whose materiality may have changed;
- whether local success is being mistaken for Root completion.

If Root DONE is not satisfied, continue from the valid current focus or report the actual blocker.

## Status and steerability

At a material pause, recovery point, blocker, or user status request, be able to state concisely:
- Root DONE;
- current focus;
- established completed work;
- material pending or changed user-requested obligations, even when no Child is open;
- current blocker, if any;
- parked material issues, if any;
- next valid action;
- when one or more Children are open: the active Child's bounded DONE plus enough existing parent/return links to recover exact nested return order;
- any continuation reference required by an activated external contract.

**Human-visible orientation.** At the start or recovery of substantial SFR work, briefly show the Root obligation/DONE, the actual active Frame path (Root → open Children; deepest is active), current focus, and next justified action with its purpose. Derive this from the current semantic frontier; if the source or a required part of the state is unknown, expose the uncertainty rather than inventing a stack. Do not force a separate status block for trivial one-shot work or repeat an accurate orientation the user has just received.

Only Root and actual open Children belong in a Frame path. A current focus, reasoning stage, or next action does not become a Child by appearing in a status display: with no open Child, write `Frame: Root; focus: compare evidence; next: assess closure`, not `Root → compare evidence → closure`.

**Progress while working.** During sustained multi-step work, communicate at meaningful work boundaries what is being done, why it advances the current obligation, what was materially established, and what comes next. The detail should match the task and the user's need to steer: communicate before extended dependent continuation when a material interpretation, route, blocker, or next action changes. Do not narrate every tool call, repeat unchanged status, or imply activity that has not occurred.

**State changes.** When a Child opens or returns, the valid focus changes materially, a blocker or route changes, or Root closes, make the updated Frame path and the decision-relevant consequence understandable to the user. An existing host or method progress message that already conveys the needed facts suffices; do not duplicate it. On an explicit status request, present the complete compact current frontier above.

Progress/status is derived communication from existing SFR state, not an additional state store, technical call stack, or host-controlled execution trace. Presentation format remains flexible. Do not create a timer, periodic checkpoint, work board, transcript, progress percentage, or new SFR state merely to prove activity.
