---
name: run-code-review
description: For the review requester. Prepare and run a code review before committing, finishing implementation, or reporting a requested review.
---

## Prepare the assignment

Reviewer will use `git diff --cached` by default. Make sure all unrelated changes (e.g. to be committed separately) are saved elsewhere.
- If that's not possible (e.g. untracked files) explicitly tell what to review.
- List any extra paths the reviewer should inspect, such as artifacts.
- Before requesting review, confirm that the comparison includes the intended work. For unstaged or already-committed work, specify the appropriate comparison and any untracked files explicitly.

For a small, simple change, give the reviewer the request. For any other change, provide a local design document that records the agreed requirements and relevant decisions. Create it before review if it does not yet exist, clarify any unsettled requirements, and retain it with the session records for distillation and archiving at handoff. A short design is enough if it records the goal, scope, requirements, and how to verify them.

## Run the review

Prefer delegation - reviewer should have fresh eyes. Ask reviewer to use `code-review`. Include relevant workspace guidance pointers and the proposed commit message when in scope.
