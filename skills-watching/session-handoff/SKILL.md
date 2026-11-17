---
name: session-handoff
description: Distill and archive a session when the user requests handoff or archiving. Propose handoff when most session-local context is no longer needed.
---

A handoff or archive request authorizes distillation followed by archiving. Propose handoff when most current session-local context is no longer needed for the next work. Apply this workflow to an active session directory; archived sessions are historical evidence.

At handoff:
- Reconcile this session's decisions, results, unresolved work, changed artifacts, and verification against available history and retained evidence. Read `agents/sessions/<session>/log.md` for omissions during distillation. Report gaps in the available evidence.
- Consolidate current state in `agents/sessions/<session>/session.md`. Distill reusable decisions, measurements, and procedures into the appropriate workspace notes. Propagate durable cross-task user guidance and corrections from its Carry-forward section to `agents/observations.md`; route topic-specific facts to their knowledge notes, preserving dates, sources, and the distinction between user statements and interpretations. Suggest changes to `agents/user-notes.md` for user review. Put actionable deferred work in `agents/backlog.md`, retaining added dates and updating substantive revision dates. Move files with lasting workspace value to their owning locations. Verify that the notes were saved and update affected links.
- Record the status of the work and what remains. Use verified outcomes or explicit user direction to establish whether work is complete, paused, or stopped. Record a reason if the user supplied one. Respect a stop request.
- Report obvious reflection points without launching a separate retrospective.
- After distillation, move `session.md`, `log.md`, and the other remaining session files to `agents/archive/sessions/<session>/`. Move the navigation entry from `agents/sessions/index.md` to `agents/archive/sessions/index.md`. Update and verify both internal and incoming links. Subsequent work may start a new session using the distilled shared information. Verify the archived contents before removing the original active directory; if distillation or archiving is incomplete, retain the active record and report what remains.

Report concisely what was saved, where, what was checked, and what remains uncertain or unfinished. State only the synchronization and preservation actually verified.
