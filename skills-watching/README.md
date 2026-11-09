# Safeguard skills

Safeties that ideally should be checked for each message in parallel by single-purpose supervisors with only the context needed for their check. In a conventional harness they can only be expressed as ordinary skills though (they aren't put in prompt since each check can be rather sophisticated).

These specifications can also serve as independent safeguards. This repository does not prescribe or configure the mechanism used by a harness.

[Commit-Gate](commit-gate/SKILL.md).

[Code-Present](code-present/SKILL.md): checks before presenting code to the user.
Deferred: generalizing this checklist beyond code. Keep its coding scope until concrete non-code review needs justify a separate or broader checklist.

[Scope-Creep](scope-creep/SKILL.md): make sure we didn't sidetrack from the session's objective.
Use at explicit checkpoints when continuous supervision is unavailable; examples follow.

[Session-Handoff](session-handoff/SKILL.md): make sure agent files are consistent.

[Installing-Tools](installing-tools/SKILL.md): basic verification of unknown third-party tools.

## Harness-dependent activation examples

Choose mechanisms supported by the target harness; these are examples, not required infrastructure:
- Explicit invocation: ask for a scope check before starting another phase of a long task.
- Workflow checkpoint: after investigation, before implementation, compare the proposed work with the agreed goal; repeat when an unexpected dependency would expand the work.
- Supported hooks or supervisors: invoke an appropriate safeguard before a commit or final response. A scope check needs the agreed goal, current plan, and a compact account of the work, not just the latest message.

For a scope checkpoint, identify the original goal, what remains, and whether the next action serves that goal. If it is an unrelated improvement, put it in the backlog; if necessary work has grown substantially, report the scope change. A skill's presence alone does not establish when it runs.
