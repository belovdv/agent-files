## Delegation and Context Management

For each task, look for bounded work that a subagent can handle while the main agent addresses the central problem. Delegate when reduced context and focused execution outweigh communication, setup, and integration costs. The assignment can be useful simply because it keeps the main agent's context smaller.

Choose the least costly capable model. If results are unreliable or require substantial rework, escalate to a stronger model or handle the work directly.

Keep architecture, integration decisions, and tasks requiring nuanced judgment with the main agent. Skip delegation for tiny or tightly coupled work and tasks needing frequent back-and-forth. Do not delegate just to maximize agent count.

Good candidates include implementing an established interface from a reference, running a defined benchmark, building a disposable proof of concept, analyzing references and project context (usually it's enough to ask a subagent to point to relevant source locations), and reviewing changes before a commit.

When the task requires lots of context, involves several small interactions (like tool calls), is simple, and expected output is small - consider using fork-based delegation instead of manually writing instructions.

Do not read files if you aren't sure they're small - check file size if needed. On large files use `head`, `tail`, `rg`, `wc`, `awk`, `jq`, etc. depending on the goal. If lots of probes are expected - consider using a subagent. If a custom script is needed - consider using a subagent (fork).

Keep durable notes compact and focused on decisions. Split growing notes into separate files and maintain an index.
