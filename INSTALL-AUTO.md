# Install SFR Auto

**Optional automatic activation.** This is an alternative to [the explicit SFR installer](INSTALL.md), not a second SFR runtime. Use this when you want the public SFR attention runtime to activate for substantive tasks without typing `SFR:` each time.

Paste the complete instruction below into a **persistent, highest-applicable user-controlled instruction location**, such as an assistant's global custom instructions or its agent instruction file. Follow the host's normal installation mechanism. This text is an activation binding, not a background service, executable hook, or guarantee that a platform will remember it.

```text
SFR Auto ON in chats receiving this instruction. Invoke for substantial goals, research, investigations, decisions, design, implementation, planning, or nontrivial questions without "SFR". Skip greetings, simple facts and incidental mentions. For ordinary follow-ups, keep the active Root; unrelated goals start new Roots. Bind Root/DONE to my actual goal; do not invent work.

On the first actual SFR activation in each conversation, and after explicit re-enablement, read and follow the CURRENT public SFR runtime:
https://github.com/saffih/SFR/blob/main/sfr.md
This opt-in controls WHEN; runtime controls HOW, despite its standalone "explicit-invocation only" default. No extra ceremony.

For the same Root reuse the read runtime. Before a new, unrelated Root, verify current Git blob SHA; reread if changed, lost, or unverifiable. Fresh authoritative read suffices without SHA. Respect stricter source rules of other methods.

"No SFR"/"SFR off": OFF this chat until re-enabled. "no SFR for this task": OFF only this task. "SFR on"/"enable SFR"/"use SFR"/"SFR: ...": ON. Explicit overrides govern their scope. Disable globally by removing this instruction.

Never treat a shared topic, old chat, or executor as proof of cross-chat resumption. Require valid SFR binding and recoverable Root/DONE, focus, active Frame and parent/return links, blockers and references. If source is unavailable, disclose and do not claim compliance.
```

The copyable instruction is designed to fit ChatGPT's 1,500-character Free/Go limit (and the 5,000-character limit on paid plans). If the field already contains other instructions, the **combined** length must fit. Do not delete unrelated user instructions without permission. Copying text or publishing this file does not itself enable SFR globally; save it in the host's persistent Custom Instructions and test activation in a fresh chat. Static tests cannot prove host behavior.

## Use

With Auto installed, ordinary prompts such as “Investigate why this deployment fails,” “Research three approaches and recommend one,” or “Continue my active design task” can activate SFR **without an SFR prefix**. The last example still needs a valid, recoverable previous-task frontier if it refers to another invocation.

Say `no SFR` to stop SFR in the current chat. Say `enable SFR` to use it again.

To stop Auto **across future chats**, remove this standing instruction from the host's Custom Instructions or agent instruction file. Chat-local commands cannot guarantee changes to a different chat or host. The explicit installer remains available and unchanged.

## Boundary

This is a user-level instruction convention, not a special ChatGPT setting, a platform hook, or an executable skill installed by this repository. It works only where the assistant actually receives and follows the standing instruction. Hosts with native agent hooks may implement the same activation predicate separately, but that is outside SFR and must not change SFR's single-file semantics.
