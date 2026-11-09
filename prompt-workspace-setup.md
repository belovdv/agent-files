# Workspace setup

Read [common instructions](./prompt-shared.md); the rest of this file adapts them to the `workspace setup` workflow.

Read `./.agent-files/<agent>.md`. Ask user if choosing `agent` identifier isn't trivial.

Before changing the target, check that the user-level setup is current, including the actual installed setup as described in the shared instructions. If the record is missing or the setup needs updating, stop and ask the user to run user setup/update first.

## Init

Check if the target workspace is present. Try to access it in a way that triggers only a few permission prompts, allowing the user to enable read access to the whole workspace and write access to files/folders that need to be modified.

Read [workspace-layout](workspace-local-layout/README.md)

If workspace has complex `./agents/` structure or another agent-targeted scratchpad - read [workspace-update-instructions](./prompt-workspace-update.md) - while it isn't `agent-files`-compatible workspace - migration will likely be needed. Do not throw away existing info. Ask user whether they want that migration.

## Inspect current setup

Run simplified checks. The results might be needed for existing `<target>/AGENTS.md` adjustments.

## Inspect agent-files

Focus on `./workspace-*`.

## Compare

If there is no existing information - nothing to compare. If there was... prepare for thorough migration.

## Ask

If there's existing `AGENTS.md` - ask user what to do with that. One local-only option is to use `<target>/agents/AGENTS.md` only.

If it's going to be rewritten a lot - make sure it doesn't duplicate info present in the context unless user wants to because of "not everyone has it".

## Apply changes

Follow the shared backup, apply, verify, and metadata-update sequence. The artifact is the modified `<target>/` itself; report the backup location and restoration instructions.
