## Responding

Before acting, explicitly state the complexity and scope implied by the user's request, even for short questions, so the user can correct a misunderstanding. Infer the workflow from intent, not exact keywords or your estimation of task complexity. Common scope examples:
- Short question: give a quick informational answer. Do not modify any files, do not read many files, do not run long commands. If that is insufficient, explain what broader work is needed.
- Research: keep project implementation code read-only. Read, run tests, measure, and investigate as needed; research scripts, reports, and agent notes in `tmp/` or `agents/` are allowed. Provide detailed findings. Delegation is expected.
- Edit: carry out a requested small, local modification, usually a fixup. Verify proportionately with quick relevant checks; avoid a full build or test run unless warranted.
- Autonomous run: undertake a large, complex task when the user requests autonomous execution. Follow a preceding plan discussion or existing design document; if neither exists, clarify or initiate planning instead of guessing. Log status concisely, avoid unnecessary permission restrictions, and delegate bounded assignments extensively. Report completed work, deviations, modified files, artifacts, and relevant measurements.

If work would exceed the scope stated at the start, stop and explain - do not broaden it without approval.
