## Local workspace structure

Read these workspace entry points when present. If the task needs local conventions and they are missing, flag the gap for workspace setup.
- `./README.md`: explains project scope and public workspace structure. `AGENTS.md` should not duplicate it.
- Public `./AGENTS.md` first, then private `./agents/AGENTS.md`. When the two files conflict, the private file takes precedence.
- `./agents/index.md`: read its Layout and Topics sections, then load topic entries relevant to the task. Revisit the catalog when the task changes.
- `./agents/user-notes.md` and `./agents/observations.md`: user-authored guidance and agent-written additions about long- and short-term project goals, current status, scope, priorities, and corrections to common misconceptions or recurring failures. Preserve their separate ownership and distinguish explicit user statements from interpretations.
- `./agents/sessions/index.md`: read when starting work to find relevant active or paused sessions. Requests such as `resume <session>: <task>` select existing work; `new session <topic>` starts a separate record, using shared information where relevant. These are examples, not required syntax. If either choice is plausible and it matters which record you use, ask the user.

Before modifying the following files, ask for approval unless the user explicitly requested the edit:
- human-targeted high-level docs: `README.md`, `ROADMAP.md`, etc.
- agent-targeted entry points: `AGENTS.md`, `agents/AGENTS.md`, `./.<harness>`
Save a backup if the file is untracked (`agents/AGENTS.md`) or has uncommitted changes.

Consult `workspace-maintenance` before expanding the local file structure or changing how its contents are organized or discovered.

Keep new work material in the session first; distill reusable material at handoff. Global backlog entries and small updates to established shared facts can go directly to their owners. A handoff or `archive session` request invokes `session-handoff` to distill and archive the session.

Use root `tmp/` for disposable work. Keep persistent local notes in the workspace's git-excluded `agents/` collection.
