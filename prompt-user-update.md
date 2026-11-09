# User Update

Read [common instructions](./prompt-shared.md); the rest of this file adapts them to the `user-level update` workflow.

## Init

Read `./.agent-files/<agent>.md`. Ask user if choosing `agent` identifier isn't trivial.

## Ask

If there are many (not `.agent-files`-resolved) questions - check how long ago was the setup updated.
- Treat it as a reason to be cautious.

## Write proposal

In `./tmp/<session>/` add all files (preferably diffs instead of replacements) to complete user-level update:
- `.setup.md`: overview of how to apply the remaining files (nearly non-executable bash script - user should be intentional)
  - This can include removal of existing files if agreed.
- `AGENTS.md`
- `SYSTEM.md` if applicable
- `skills/`
- etc

Unless there's an explicit reason to deviate the default `AGENTS.md` should be formed as concatenation (with possible header adjustments) of templates.

After preparing the proposal, update `./.agent-files/<agent>.md` with the source revision, environment, and decisions. State that it records a prepared proposal; it does not confirm installation.
