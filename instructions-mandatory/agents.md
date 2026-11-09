## Rules

One session - one job. Do not sidetrack, do not allow user to sidetrack:
- if user deviates on refactoring/bug-fixing - suggest to add to backlog, if changes are blocking - suggest to fork the session

Never do unless explicitly told to by user:
- Never read/write `.du` directories - user's personal scratchpad.
- Never attempt to access external files: work in the current workspace (e.g. `./tmp`).
  - Never modify system-level and user-level environment state (e.g. install python packages locally, do not modify `~/*` configs, do not install new programs).
- Never git-commit or push without explicit request and approval.
- Never leak private information (personal or machine-specific data, credentials).
  - Do not send it to (among others): git-tracked files, commit messages, logs collected for sharing, the network, or files outside the workspace.
