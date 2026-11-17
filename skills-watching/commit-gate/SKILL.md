---
name: commit-gate
description: Checklist before git-commit
---

## Commit scope

Stage the intended files and hunks, including any new files that belong in the commit. Preserve unrelated working-tree changes. Check that the staged snapshot forms one logical change. If the snapshot needs splitting, explain the split before proceeding.

## Review gate

Use `run-code-review` to review the staged snapshot with a fresh, low-cost subagent. Check workspace commit rules and confirm the parent is not a `wip: ...` commit unless using the local WIP exception below.

- If there are significant findings or required checks are incomplete, report them and wait for the user to decide what to do.
- If the only findings are typo-level and the fixes leave behavior and prior verification intact, fix them and verify the affected lines and staged diff. Tell the user what the review found and what you fixed. Stop and ask whether to review again before proceeding with the updated commit.

## User review and approval

Make sure the user reviewed the code and follow any workspace-specific understanding checklist. If the user explicitly skips their review, make sure there's an agent usage disclosure in the code or the proposed commit message.

### Commit message

Use the commit body to explain what changed and why when that context is useful. Keep detailed design rationale and review evidence in the local archive.

Unless overridden by workspace: format: `<significance> [<scope1>,<scope2>,…] <optional logical group: > <header>`

Significance: `1` major, `2` intermediate, `3` minor, `4` styling, formatting, comments, and similar changes. Scopes are paths containing most of the change. Use a logical group when the scope spans much of the repository.

Examples:

- `1 [awesome-tool/tui] introduce tui for awesome-tool`
- `2 [crates/server,crates/client] api: switch to json`
- `4 [package/cli.py] clarify comments for xxx feature`

Propose the message and leave the body empty for trivial changes. Include the proposed message in the review for private information. If that version has yet to be checked, request a focused check through `run-code-review`. Obtain explicit approval for the proposed commit before running `git commit`.

## Commit

Confirm the staged snapshot and message match what was approved and covered by review or the typo-level verification above. Commit them and update relevant work notes.

## Notes

Commit approval never implies push approval.

## Local WIP exception

If explicitly told by user to use `wip: ...` checkpoint(s): it's allowed to skip user's review (both diff and message) and most pre-commit checks.
