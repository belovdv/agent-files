# Workspace layout

Yet-to-be-stabilized layout for workspace files (mostly git excluded). Agent caches, persistent logs, and related files.

## Layout

Private directories should be eagerly initialized.
- Motivation: avoid putting their full specification in the permanent prompt.

The word *private* will be used for local-only (git excluded) files. Usually (unless the specific file is created to be shared) they can contain private info.

Root folders should be added to `.git/info/exclude`.

`./`
- `agents/`: entry to private agent-used agent-maintained files world.
  - `.agent-files.md`, `.agent-files.user.md`: used by `agent-files` workflows.
  - `AGENTS.md`: private workspace instructions. Read the public root `AGENTS.md` first; keep only additions and overrides here, without duplicating public instructions. The private file always takes precedence when these two files conflict.
  - `index.md`: compact navigation.
    - The starting point for navigating local agent files.
    - Should not mention every single file - should be small enough to load it every single time. Logs, deeply nested directories, etc. should use their own indexes (if needed - usually not).
  - `todo.md`: workspace-level list to keep postponed actions.
  - `roadmap.md` (optional): high-level project roadmap
  - `sessions/`: active session files and backlog
    - Note: overriding harness's default session file path might require explicit user action.
    - `sessions/backlog/`
  - `knowledge`: deep-dive, investigation results.
  - `reference/`: mirror for `./reference`, keeps concise overview for already-analyzed references: its importance and links to documentation and relevant modules.
  - `scripts/`: reusable agent-written scripts (e.g. log scraping)
  - `logs/`: general persistent log files
  - `stats/`: log files that contain relevant statistics. Used to analyze long-term progress.
  - `tmp/`: disposable agent scratchpad, subject to the cleanup policy below.
    - `logs/`, `stats/`, `scripts/`: temporary artifacts; move anything worth keeping into the corresponding persistent directory.
- `reference/`: keeps project-external files that can be used as a reference if needed: existing implementations, relevant papers, etc.
  - `<project>/`: usually git clone
  - `<paper>.pdf`: usually downloaded public paper
- `tmp/`: disposable workspace scratchpad; use it instead of `/tmp/`.

## Migration from previous revision

(will describe nontrivial migration rules)
