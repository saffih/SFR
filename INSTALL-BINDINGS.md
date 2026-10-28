# Install SFR bindings

This is a portable installation guide, not an SFR runtime or an automatic host hook. Source: [runtime](sfr.md), [account profile](ACCOUNT.md), [observation profile](OBSERVE.md).

## Portable request

> Install SFR for my normal work and handoffs. Follow https://github.com/saffih/SFR/blob/main/INSTALL-BINDINGS.md and https://github.com/saffih/SFR/blob/main/ACCOUNT.md. Use this environment's supported persistent instruction mechanism, verify what is saved, and report any unavailable capability instead of claiming success.

## Installation procedure

1. Establish the intended scope (user account, workspace, project, repository, agent, or session), the host's actual instruction priority and writable persistence mechanisms. Do not guess.
2. Install the smallest binding that reaches the intended work: user-controlled custom instructions, project/workspace rules, or applicable agent instructions such as `AGENTS.md`, according to the host. A memory preference is supplementary, not evidence that persistent execution instructions are installed. Edit only authorized locations and preserve unrelated instructions.
3. Bind [ACCOUNT.md](ACCOUNT.md) as the opt-in account/workspace profile and the current [sfr.md](sfr.md) as the sole SFR runtime. Its selected [OBSERVE.md](OBSERVE.md) profile measures material behavior. If a private source or tracking store is authorized, keep its binding private and separately configured.
4. Read back the actual installed instruction or file, record its effective scope, and test a new invocation if available. Independently test the receiving invocation before claiming handoff correctness. Where persistent settings, memory, agent files or tools cannot be changed, provide the precise instruction for the user to place manually. Never claim an unverified write or installation.
5. Avoid conflicting activations: account-wide SFR is opt-in and should not compete with another standing SFR Auto or explicit-only profile in the same scope. Direct user opt-out governs its stated scope. To uninstall, change the actual persistent instruction location. Do not assert a chat command changed other sessions.

## Persistent instruction

```text
Use SFR for my ordinary work in this instruction's scope. At the start of each workstream and after each same-workstream handoff, read and follow https://github.com/saffih/SFR/blob/main/ACCOUNT.md, including the linked current SFR runtime and observation rules. Use any separately authorized private configuration for source and tracking. Keep ordinary work lightweight. Disclose unavailable sources, persistence, or logging; never claim unobserved cross-handoff success. Follow my explicit task-scoped opt-outs.
```

**Host limitations:** Writing memory requires an available and permitted host mechanism; it is not achieved by merely asking in a chat. Agent files apply only within their documented scope. This installer cannot monitor inaccessible chats or supply missing tools. [sfr.md](sfr.md) governs how SFR operates; the binding only selects when and where it runs.
