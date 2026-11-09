Once agreement is reached, the planning session ends.

Implementation should proceed in a fresh session unless the goal turns out to be simple enough.
- Motivation: context clarity.

What remains is to save the agreed plan as a design document, then run final checks:
- Run a fresh (low-cost) subagent to summarize what's written. The goal - make sure nothing in the session's context is left undocumented. It can read a few files, but not much - if lots of search is needed to understand the document - it's not good enough, improve it.
  - Ask user whether to run this check.
- After automatic check (or user's refusal) ask user to review the final state.
  - Usually they should agree, but if needed - there might be several adjustments.
  - If it turns into many rounds - agreement wasn't achieved - planning session should resume.
