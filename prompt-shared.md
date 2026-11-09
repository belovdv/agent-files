# Using agent-files

Use the record for the selected workflow: `./.agent-files/<agent>.md` for user setup/update, or `<target>/agents/.agent-files.md` for workspace setup/update. The user record is also a prerequisite for workspace workflows, not a substitute for the target record.

Treat the recorded revision as a comparison baseline, not proof that synchronization is complete. Check local edits, user overrides, and environment changes even at the same revision. A user-level record describes the prepared setup; verify the installed files or ask whether the proposal was applied before relying on it as the current environment. Report no changes needed only after comparing the relevant inputs and actual setup.

Process overview:
- Inspect current setup.
- Compare with `agent-files`.
- Ask user if needed.
- Suggest improvements for upstream.
- Write proposal (if user-level) or backup and modify (if workspace-level).
- Report.

Remind the user it's a good idea to run reflection from time to time.

Set `<session>` to `<date>-<topic>` and create `./tmp/<session>/` for intermediate results.

## Agent Files Config

Use this template for both user and workspace records:
```md
# Agent Files Config

Last modified: `<date>`

Revision: `<git-revision>`

## Environment (if user-level - local to this workspace)

Harness (including web/desktop/tui), models, basic system info, etc.
General assessment of them (e.g. frontier-general-thinker/frontier-coder/local-small-llm).
Multiple entries are allowed.

## Workspace (if workspace-level)

Workspace-specific notices if any.

## Decisions

Decisions made (e.g. use/not specific skill/optional-instruction-part), motivation behind them (user told to is not a good motivation - ask them to clarify if possible). Including general ones (that can affect multiple choices - e.g. skip all `skills-workflow`)
```

User overrides live in `./.agent-files/<agent>.user.md` for a user record, or `<target>/agents/.agent-files.user.md` for a workspace record. Read them alongside the corresponding record; explicit overrides take precedence over recorded decisions. Do not rewrite the override file or the record timestamp merely because an override was read.

## Inspect current setup

Note: most harnesses provide a skill describing their capabilities. Ask if unavailable.

Check the current environment capabilities:
- **Subagents**: required, strongly recommend that the user make them available if they aren't available.
- **Different-cost models**: if unavailable - some prompts/skills should be modified to omit those mentions.
  - The exact list of available (planned to be used if too many) models (ask user if needed).
- **Extendability**:
  - Skills: required
  - Prompts
  - Extensions
- Available environment-specific but disabled (not present in the context) things (skills, tools)
- **Instruction loading and scope**: where user and workspace instructions are loaded, how public and private instructions are included, and how their precedence is expressed. Ensure the private workspace instructions are read after the public ones and override them without duplicating them.
- **Skill activation and safeguards**: explicit invocation, automatic selection, hooks, or supervisor support. Adapt to the harness; see the [safeguard examples](skills-watching/README.md).
- **Persistence and context compression**: what survives a new session or compaction, and where durable decisions should be stored.
- **Permissions**: accessible paths, allowed writes, network/tool restrictions, and approval mechanisms.
- **Model selection**: which models can actually be selected for the main agent and subagents, rather than merely listed by the provider.

Check the current context:
- **Instructions**
  - system if that doesn't violate safety policies
  - user-level: predefined
  - user-level: available to user, e.g. `~/<harness>/AGENTS.md`
- **Skills**
  - environment-specific
  - gates/watching, workflow, knowledge
- **Tools**

Write discovery results to `./tmp/<session>/current-setup.md`

## Inspect agent-files

Read these compact templates directly; do not create or commit a separate summary of them. Keep discovery in the session directory and durable environment details and decisions in the ignored setup record.

Follow the links from the root [README](README.md) to read what `agent-files` proposes. Adapt it to the current environment specifics (e.g. remove lowest-cost model suggestion if there's only a single one available).

## Compare

Focus on functionality:
- Which is present locally and is generic enough to suggest adding to upstream `agent-files`.
- Which is present in `agent-files`, but not in the local setup.
  - Check if it is relevant.
- Which is present in both but different.
  - Evaluate which version should be chosen.
- Which is present in both and nearly identical.
- Which exists at the harness-specific layer.
  - Usually it's better to keep it, but analyze whether `agent-files` introduces something worth adding even with duplication.

## Ask

If the selected setup record is present, reuse its decisions along with the user overrides.

If one version (`agent-files` vs `current-setup`) is strictly better - choose it.
Otherwise ask user what to choose. Provide the context needed to make an informed decision.

If something looks deprecated/not-useful-enough-to-justify-context-cost - ask.

Actively identify useful adaptations, ambiguities, conflicts, and opportunities to improve the setup. Present substantive options with a recommendation and tradeoffs, even when faithful copying is possible. Ask before incorporating any semantic deviation into the generated instructions or skills. Until decided, preserve the source semantics. Phrasing changes may proceed only when they preserve scope, triggers, permissions, and exceptions.

Batch related decisions into a concise comparison: source behavior, proposed alternative, reason, and recommendation. Do not silently adopt an alternative because it appears better. Record approved deviations and summarize them in the final report.

## Suggest upstream improvements

For things from `current-setup` that are strictly better and generic enough (ask if in doubt) - list them and suggest that the user add them upstream.

## Prepare or apply changes

User-level workflows write proposals in `./tmp/<session>/`; they do not change the installed setup.
Final proposal will suggest to modify some files and folders (likely including `~/<>/AGENTS.md` and `~/.agents/skills`) - make a backup for them.

Workspace-level workflows modify the target in place:
- Finish prerequisite checks, comparison, and any required migration approval before changing target files.
- Before the first target change, save the existing contents of every file to be overwritten or removed in `./tmp/<session>/backup/`, preserving paths relative to the target. Include existing setup metadata. Record newly created paths separately so rollback can remove them.
- Write restoration instructions alongside the backup. Check that the backup covers the planned changes before proceeding; stop if it cannot be created.
- Apply the changes and verify the resulting files and layout.
- Only after verification, create or update `<target>/agents/.agent-files.md` with the source revision and decisions. If the work fails or remains incomplete, report that state and the restoration path without recording a successful update.

Proposals and backups in `tmp/` follow the scratchpad cleanup policy. Report their location so the user can review or restore them before cleanup, or preserve them explicitly if needed.

## Report

Final report should:
- Summarize comparison (e.g. nearly identical or mention specific differences).
- Suggestions for upstream
- What was written (including temporary scratch files)
- The proposal:
  - Files to copy to user-level setup.
  - What was created or modified in the target workspace, where the backup is.
- Free-form opinion if there's anything to tell.
