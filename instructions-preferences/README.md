# User preferences

This covers everything that goes into `~/AGENTS.md` and does not need higher priority than the user's messages in the model's view: personal preferences and agent optimizations.

[Personality](agents.personality.md): modern models are trained to be polite and tolerant to the extent this costs efficiency. This prompt attempts to mitigate this.

[Delegation-and-Context](agents.delegation-and-context.md): encourage the agent to delegate more. This is the most influential single optimization for context clarity (and thus model effectiveness) and token consumption efficiency (less context each round).
- Note: in some environments there isn't a meaningfully lower-cost model - adjust if needed

[Responding](agents.responding.md): addresses a personal pain point: I ask a small or less important question and expect a quick answer (or an explanation of why one is unavailable), but the agent starts digging for minutes. It costs tokens, but it saves time.

[Code-and-Tests](agents.code-and-tests.md): modern agents tend to produce bloated code. This attempts to address some common sources.

[Local-Workspace](agents.workspace.md): tells the agent to check paths containing local agent files.
