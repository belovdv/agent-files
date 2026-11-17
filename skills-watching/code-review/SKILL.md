---
name: code-review
description: For the agent conducting a code review. Inspect the assigned change, verify behavior, and deliver an independent verdict.
---

## Scope and inputs

Use `git diff --cached` unless the review request specifies another comparison. Leave the reviewed files untouched and reach your own verdict from the requirements and evidence.

Use the provided design and any agreed amendments as the requirements. For a small, simple change, the request itself can supply the requirements. Check commit message as well if present. Report any essential input that is missing.

## Acceptance checks

Follow the workspace instructions and read `agents/review.md` when it exists for project-specific contracts, invariants, and required checks.

- Check that the change satisfies the requirements through its normal entry points, preserves existing behavior outside scope, and handles relevant failure paths and edge cases. Trace consequential behavior into callers, tests, or adjacent code as needed.
- Check for missing work and unrelated changes. When reviewing a correction, look for other affected locations, including new files, metadata, and docs. Check changed docs against their audience and purpose.
- Check that additions and abstractions serve a concrete need. Look for avoidable duplication, complexity, and meaningful performance or scaling costs in new and changed code. Check whether such costs reflect a deliberate tradeoff and explain their impact.
- Rerun relevant tests, builds, lint, and formatting checks on the reviewed snapshot. Where practical, observe that the changed behavior works through a test or reproduction. Reuse prior evidence when workspace guidance permits it and it applies to the snapshot. If unrelated working-tree changes can affect verification, run checks in an isolated copy of the reviewed snapshot or report the verification gap.
- Check for private information and leftover debug code, temporary guards, or scratch artifacts. Check a proposed commit message for private information when it is supplied. Treat confirmed private-info leakage as blocking regardless of how easy it is to remove. Identify its location without repeating the sensitive content.

## Verdict

- **Pass** when the required checks for the review scope are complete and there are no blockers. Include a few minor corrections or suggestions when useful.
- **Changes requested** when there are blockers. List each blocker with its location, the requirement or check it violates, and its consequence. If a required check could not be completed, withhold a pass and report what's missing.
- **Changes requested, review budget reached** when the agreed review budget runs out before the blockers can all be examined or reported. Save the detailed findings in `agents/reviews/<review-id>.md`, using a unique ID for the review. Summarize the main blockers and state where the next pass should resume.
