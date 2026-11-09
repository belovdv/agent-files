---
name: commit-gate
description: Checklist before git-commit
---

## Agent-review

Review first; do not fix issues encountered during this checklist.

Use (low-cost) subagents: both to preserve your context and to get a fresh-eyes opinion.

- Use the most recent successful applicable build, lint, formatting, and test checks from this session. Make sure everything needed was successfully run.
- Confirm the changes form one logical diff. Do not mix unrelated fixes or refactors with a feature. If splitting is needed - suggest; if a split was already suggested, check atomicity.
- Review the whole diff, including new files, for debug prints, commented-out code, temporary test guards, and other stale artifacts. (subagents)
- Check content and the eventual message for private info leakage (see the **## Rules**). (subagents)
- Check workspace-specific instructions if any. (subagent)
- Make sure parent commit is not `wip: ...`.

If an issue is found, report it and stop before committing.

## User-review

Make sure user reviewed the code. Exception: user explicitly told to skip this step. In that case there must be an agent usage (authorship) disclosure in the code (ideally already present) or in the commit message.

## Message and approval

Code, written mostly by agent, should be explained in detail in the commit's body - what and why - unless the diff is tiny/cosmetic.

Unless overridden by workspace: format: `<significance> [<scope1>,<scope2>,…] <optional logical group: > <header>`

Significance: `1` major, `2` intermediate, `3` minor, `4` styling, formatting, comments, and similar changes. Scopes are paths containing most of the change. Use a logical group when the scope spans much of the repository.

Examples:

- `1 [awesome-tool/tui] introduce tui for awesome-tool`
- `2 [crates/server,crates/client] api: switch to json`
- `4 [package/cli.py] clarify comments for xxx feature`

Propose the message; leave the body empty for trivial changes. Ask: "Approve, or should I adjust anything?" Revise if requested and ask again. Do not run `git commit` until the user explicitly approves the proposed commit.

After approval, make a final disclosure check, commit, and report explicitly that it was made with a concise summary. Update relevant agent session notes.

## Notes

Commit approval never implies push approval.

## Local WIP exception

If explicitly told by user to use `wip: ...` checkpoint(s): it's allowed to skip user's review (both diff and message) and most pre-commit checks.
