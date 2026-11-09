# User Setup

Read [common instructions](./prompt-shared.md); the rest of this file adapts them to the `user-level setup` workflow.

## Init

Choose `<agent>` for `./.agent-files/<agent>.md`. Ask the user if the identifier isn't clear. If the record already exists, suggest user to use `user-level update` instead.

## Write proposal

In `./tmp/<session>/` create all files (or diffs, or in both forms) to complete user setup according to Q&A results:
- `.setup.md`: overview of what to copy where (nearly non-executable bash script - user should be intentional)
  - This can include removal of existing files if agreed.
- `AGENTS.md`
- `SYSTEM.md` if applicable
- `skills/`
- etc

Unless there's an explicit reason to deviate the default `AGENTS.md` should be formed as concatenation (with possible header adjustments) of templates.

After preparing the proposal, write `./.agent-files/<agent>.md` with the source revision, environment, and decisions. State that it records a prepared proposal; it does not confirm installation.
