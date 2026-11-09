---
name: session-handoff
description: Actions at the end of the session - design document after planning is written, implementation is finished, commit is made, etc.
---

When the end of the session is in sight (or user explicitly told so):
- Make sure all agent-maintained files are in sync - there are no stale links, no-longer-correct info, etc.
- Make sure all important info is saved: in the next session user will assume all decisions from this session will be available in future sessions.
- If there are obvious reflection points to address - report to the user.
  - Do not scan whole session - it'll be done in special sessions.
- Revisit all of `tmp/` and `agents/tmp/`: move anything worth retaining to persistent locations, then clean the scratchpads. If there's anything added by someone else - ask user whether the full cleanup is needed. These directories are disposable and should be cleaned frequently.

Explicitly tell user: workspace's agent files are in sync, session info is saved.
