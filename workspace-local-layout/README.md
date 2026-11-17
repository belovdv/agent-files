# Workspace layout

See the [layout and structural expansion rules](../skills-workflow/workspace-maintenance/SKILL.md#layout). Migrations from older or nonconforming layouts use the [agent-files workspace setup](../prompt-workspace-setup.md) or [workspace update](../prompt-workspace-update.md) workflow.

## Migration

Migration from older or nonconforming layouts belongs to agent-files workspace setup/update. Analyze the existing layout starting with `<target>/agents/index.md`. Map existing material to the current specification, preserve active guidance and useful history, identify conflicts, and update references to moved files. Follow the selected workflow's approval and backup steps before applying changes.

A workspace can use a subset of the layout; absent collections with no content do not require migration or empty directories. Preserve documented extensions that have clear ownership and discovery routes. Resolve conflicting conventions during setup/update rather than leaving competing destinations.

If the workspace used `agents/tmp/`, map disposable files to root `tmp/` and material worth retaining to its session or persistent home. Check for collisions and verify moved contents before retiring the old scratch directory.

Establish separate Layout and Topics sections in `agents/index.md` using the specification's catalog format. Wire startup reading of the catalog, user notes, agent observations, and active-session list into the generated workspace instructions. Verify links and preserve user-authored guidance separately from agent-written additions.
