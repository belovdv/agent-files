---
name: scope-creep
description: Check whether a long or complex session is still focused on its original goal.
---

Recall what was the stated goal of the session.

Check if we're still doing what's necessary for that - we did not sidetrack:
- Small deviations:
  - Fix this adjacent piece.
  - Add unrelated comments.
  - Format nearby code.
- Complete redirection: we didn't shift to something entirely different.
- Unexpected complexity: we're still doing what's needed to achieve what we need, but it turns out we have to do way more than we should in a single session.

If any of these occur, trace how it happened (why we got sidetracked) and report it to the user.
- During autonomous work, correct small accidental deviations yourself; report material expansion of the agreed objective before undertaking it.
