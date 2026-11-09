---
name: code-present
description: Checklist before finishing a large autonomous coding session.
---

After a long autonomous coding session, before reporting to the user, review the code.

Use (low-cost) subagents: both to preserve your context and to get a fresh-eyes opinion.

Check the following:
- Code does what was planned: there's no unplanned functionality with made-up/no motivation.
- Code does what was planned: nothing was forgotten.
- Code is correct (to the project's standard): there was an observable effect that looks correct.
- Code is good: there's no:
  - unnecessary abstractions,
  - functionality duplication,
  - undocumented poor asymptotic behavior:
    - worse than expected from the functionality;
    - e.g. quadratic where linear is possible because on real data simple is faster or it was decided to postpone complex implementation.
- Formatters/Linters/etc

Exception: the deviation was a conscious decision with explicit reason and it will be reported to the user.

This should be done regardless of presence of user-approved design document.

If an issue is found, fix it, and return to this check.

If everything is good, give a concise final report covering:
- What changed and why.
- Validation evidence and any remaining limitations.
- Deviations from the plan and their reasons.
- Follow-up work worth considering.

Write detailed durable notes only when useful for future work, and link them from the final report instead of repeating them. Do not require a separate report file or a per-file diff narration.
