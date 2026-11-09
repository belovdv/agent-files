# Agent files

Personal source of truth for synchronizing coding-agent setups across machines and harnesses. This repository uses my conventions; each agent adapts them to its own environment.

## Usage

Four semiautomatic workflows. Run each workflow from this workspace and provide a target path if applicable. Each will:
- compare existing setup with the current agent-files revision,
- ask clarifying questions if user decision is needed,
- suggest improvements for upstream (implementing them is a manual task),
- prepare a proposal for review.
  - User-level in `./tmp/<session>/`.
  - Workspace-level will save a backup and modify in place.

| Prompt | Notes |
| --- | --- |
| [user-setup](prompt-user-setup.md) | New `./.agent-files/<agent>.md` |
| [user-update](prompt-user-update.md) | Expects `./.agent-files/<agent>.md` |
| [workspace-setup](prompt-workspace-setup.md) `<target-path>` | Expects `./.agent-files/<agent>.md`, creates `<target-path>/agents/.agent-files.md` |
| [workspace-update](prompt-workspace-update.md) `<target-path>` | Expects `./.agent-files/<agent>.md` and `<target-path>/agents/.agent-files.md` |

## Layout

| Directory | Details |
| --- | --- |
| [instructions-mandatory](instructions-mandatory/README.md) | Fundamental rules `~/SYSTEM.md` |
| [instructions-preferences](instructions-preferences/README.md) | General defaults `~/AGENTS.md` |
| [skills-workflow](skills-workflow/README.md) | Prompts for user-agent interaction |
| [skills-knowledge](skills-knowledge/README.md) | Specialized task knowledge |
| [skills-watching](skills-watching/README.md) | Safeguards |
| [workspace-local-layout](workspace-local-layout/README.md) | Layout for git-ignored agent files |
| [workspace-instruction-examples](workspace-instruction-examples/README.md) | Cookbook for `./AGENTS.md` |
| `prompt-*.md` | Instructions for sync workflows |
| `.agent-files/` | Git-ignored local configurations |

Template folders follow this structure:
- `README.md`: what the templates in this folder cover
- `agents[.name].md`: templates
- `<skill-name>/`: templates
