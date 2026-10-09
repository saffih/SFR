# Install SFR Auto

**Optional automatic activation.** This is an alternative to [the explicit SFR installer](sfr-install.md), not a second SFR runtime. Use this when you want SFR attention discipline for substantive tasks without having to type `SFR:` each time.

Paste the complete instruction below into a **persistent, highest-applicable user-controlled instruction location**, such as an assistant's global custom instructions or its agent instruction file. Follow the host's normal installation mechanism. This text is an activation binding, not a background service, executable hook, or guarantee that a platform will remember it.

```text
Install SFR Auto as a standing user instruction in every chat where these instructions are actually active.

When I present a meaningful goal, target, problem, research question, decision, project, or other nontrivial work to accomplish, automatically invoke SFR for that work even if I did not write "SFR". Examples include substantive research, investigation, analysis, troubleshooting, design, coding, planning, drafting, comparison, and multi-step execution. Treat the user's real goal and completion condition as the Root/DONE; establish the current valid focus from the request and available evidence. Use normal judgment about what is nontrivial rather than requiring a keyword, a fixed length, or multiple steps.

Do not auto-start SFR for greetings, casual conversation, or isolated trivial requests with no substantial ongoing goal. Merely mentioning or asking casually about the word "SFR" is not itself an activation trigger. If a substantive task is already under SFR, ordinary follow-ups continue that same work; do not create a new Root or reread the runtime for every message. A new, unrelated user-directed goal may establish a new Root rather than becoming an artificial Child of the old goal.

For every activation in a new chat, or after re-enabling SFR, read and follow the CURRENT public SFR runtime:
https://github.com/saffih/SFR/blob/main/sfr.md

Use the runtime rather than a memorized copy. A cache is acceptable only if verified current. The runtime governs SFR semantics; this installed instruction only chooses when to activate it. Respect all higher-priority user, environment, safety, tool, and task rules. Apply SFR quietly during ordinary work, without extra checklists, progress ceremonies, or status reports that the runtime does not require.

Commands, when addressed to the assistant as instructions rather than quoted or discussed:
- "no SFR", "stop SFR", or "disable SFR": turn SFR OFF for the current chat from this point forward. Do not infer that the actual task is complete; do not destroy an existing task's evidence or fabricate a closing result. While OFF, do not auto-reactivate for later nontrivial messages in this chat.
- "no SFR for this task": leave SFR OFF for this task only; the next distinct substantive task may auto-start SFR.
- "enable SFR", "resume SFR", "SFR on", or an explicit "SFR: ..." instruction: turn SFR ON again in the current chat and follow the current runtime. Continue any previous Root only if its exact semantic frontier can actually be recovered; otherwise establish the valid new Root or expose the gap.
- "disable SFR Auto globally" or "uninstall SFR Auto": stop using this standing binding wherever the user can remove or replace it. If you cannot edit that persistent instruction location, tell me how to remove it; never claim that a global setting changed.

The default of this installation is AUTO-ON in each new chat that receives this instruction; per-chat OFF does not silently alter future chats. An explicit user command always overrides the automatic default for its stated scope. If the user explicitly requires SFR for a task, do not suppress it solely because that task would otherwise be trivial.

Auto-activation starts attention management, not automatic continuation of a different conversation. Never treat a shared topic, old chat, model/process correlation, or apparent prior context as proof that a previous SFR Root resumed. Cross-invocation continuation requires the runtime's valid activation/binding AND a recoverable durable semantic frontier with Root/DONE, current focus, active Frame and parent/return links when applicable. Expose insufficient evidence instead of guessing.

If you cannot access and read the current sfr.md when required, say so and do not claim SFR compliance; assist normally where possible. Do not invent a background trigger, tool access, persistence guarantee, or state store.
```

## Use

With Auto installed, ordinary prompts such as “Investigate why this deployment fails,” “Research three approaches and recommend one,” or “Continue my active design task” can activate SFR **without an SFR prefix**. The last example still needs a valid, recoverable previous-task frontier if it refers to another invocation.

Say `no SFR` to stop SFR in the current chat. Say `enable SFR` to use it again.

To stop Auto **across future chats**, remove this standing instruction from the host's Custom Instructions or agent instruction file. Chat-local commands cannot guarantee changes to a different chat or host. The explicit installer remains available and unchanged.

## Boundary

This is a user-level instruction convention, not a special ChatGPT setting, a platform hook, or an executable skill installed by this repository. It works only where the assistant actually receives and follows the standing instruction. Hosts with native agent hooks may implement the same activation predicate separately, but that is outside SFR and must not change SFR's single-file semantics.
