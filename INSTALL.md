# Install SFR

Paste the instruction below once into your assistant.

```text
Install this as a persistent global/cross-chat instruction wherever your environment supports persistent instructions or memory:

When I use SFR as an instruction — including a bare message "SFR", "use SFR", "use SFR for <task or continuation instruction>", "continue under SFR", or "SFR: <task or continuation instruction>" — read and follow the current public SFR runtime:

https://github.com/saffih/SFR/blob/main/sfr.md

Do not trigger SFR merely because I mention, discuss, or ask a question about SFR.

For every SFR invocation, read the current sfr.md rather than relying on memory, a summary, or an older version.

A cached copy may be used only when it can be established as current. Use its Git blob SHA when available, but lack of a SHA alone must not block SFR if the current source itself can be accessed and read.

When I say "use SFR for <task>", treat <task> as the Root task or continuation instruction and use SFR to keep the session attached to that work while allowing necessary changes of attention and correct return.

A bare "SFR" or "use SFR" applies SFR to the current active task or continuation when one can be validly established.

The current sfr.md always overrides this stored instruction.

If persistent global/cross-chat instructions or memory are available, store this binding there now so SFR works in future sessions without reinstalling it. Store the binding, not a copy of SFR.

If persistent storage is unavailable, keep this binding active for the current conversation/session and tell me that it will not persist to future sessions.

If you cannot access and read the current sfr.md for an invocation, say so and do not claim SFR compliance.
```

After installation, ordinary use can be as short as:

```text
use SFR for investigate why this deployment keeps failing and fix it
```

or:

```text
SFR: continue the current design work until the open issue is resolved
```

SFR maintains the session focus; it does not require a separate planning or reasoning framework.
