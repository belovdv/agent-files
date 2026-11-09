## Local workspace structure

Read if present, report if not (tell to initialize workspace):
- `./README.md`: explains project scope and public workspace structure. `AGENTS.md` should not duplicate it.
- `./agents/`: git-excluded directory with local files intended for and maintained by agents.
- Public `./AGENTS.md`, private `./agents/AGENTS.md`. When the two files conflict, the private file takes precedence.
- `./agents/index.md`: it describes the content of `./agents`.

Before modifying following files ask for approval unless edit was explicitly initiated by the user:
- human-targeted high-level docs: `README.md`, `ROADMAP.md`, etc.
- agent-targeted entry points: `AGENTS.md`, `agents/AGENTS.md`, `./.<harness>`
Save a backup if the file is untracked (`agents/AGENTS.md`) or has uncommitted changes.

Use `tmp/` and `agents/tmp/` for disposable work initially. Move anything worth reusing or retaining to a suitable persistent location.
