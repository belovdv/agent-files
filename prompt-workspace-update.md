# Workspace update

Read [common instructions](./prompt-shared.md); the rest of this file adapts them to the `workspace update` workflow.

Read `./.agent-files/<agent>.md`. Ask user if choosing `agent` identifier isn't trivial.

Before changing the target, check that the user-level setup is current, including the actual installed setup as described in the shared instructions. If the record is missing or the setup needs updating, stop and ask the user to run user setup/update first.

Read `<target>/agents/.agent-files.md`

## Inspect current setup

Analyze current layout, start with `<target>/agents/index.md`.

Use `<target>/agents/.agent-files.md` to get revision it was created on - check what was proposed back then.

## Inspect agent-files

Focus on `./workspace-*`.

## Compare

List the differences in the layout.

List the deviations of `<target>/AGENTS.md`.

## Ask

Depending on the user's specific prompt they might want to update `<target>/AGENTS.md` only - ask if unsure.

If migration is trivial - nothing to ask. Otherwise write a high-level proposal first, ask for approval.

## Apply changes

Follow the shared backup, apply, verify, and metadata-update sequence. The artifact is the modified `<target>/` itself; report the backup location and restoration instructions.
