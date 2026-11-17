---
name: investigate
description: Research, investigate, or evaluate through evidence and reversible experiments. Use for research, investigation, and evaluation requests, including their intent markers; exclude quick replies and implementation tasks.
---

# Research, investigation, and evaluation

Use the initialized workspace's already-loaded private instructions and index for artifact locations and knowledge routing. If a needed convention is missing from context, resolve that specific gap before writing.

## Establish the question

Identify the question to answer, the target that must remain unchanged, and the evidence needed. Research usually starts externally; evaluation locally. Use either source as the question requires.

If the requested conclusion cannot be established within the constraints, say so. Explain the missing evidence or capability and the smallest useful change to the constraints. Provide supported partial findings without inventing certainty or silently broadening the task.

## Select relevant guidance

Read only the supporting files needed for the task; several may apply. Do not run every procedure for every investigation.

| Question | Guidance |
|---|---|
| What does an existing implementation actually do? | [Implementation understanding](references/implementation.md) |
| What approaches exist, and which fit this use case? | [Literature and alternatives](references/landscape-and-comparison.md) |
| Is this proposal sound or ready to implement? | [Design and readiness](references/design-and-readiness.md) |
| How well does it work, or why does it behave this way? | [Experiments and diagnosis](references/experiments.md) |
| Is this feasible within resource or cost constraints? | [Estimation](references/estimation.md) |
| What does accumulated history establish? | [History and workflow audits](references/history.md) |

## Shared evidence and notes

- Start with relevant existing knowledge and evidence. Recheck assumptions that may have changed rather than repeating settled investigations. Record source revisions, configurations, dates, and applicability where they affect the result.
- Support consequential claims with source locations, measurements, or concrete examples. Separate observed behavior, source claims, inference, and proposals. Seek counterexamples to important conclusions; state the limits of inspected paths and tested cases.
- Give bounded subagents the question, constraints, relevant note pointers, and expected evidence. Incorporate useful findings into the owning notes; do not leave them only in subagent messages. Verify consequential interpretations before adopting them.
- Capture useful discoveries and unresolved work as investigation proceeds, using existing session-record conventions. At meaningful milestones, consolidate readable session-local findings. Distill reusable material into shared topic notes at handoff.
- The main deliverable is persistent notes in `agents/sessions/<session>/`. Keep current state and carry-forward corrections in `session.md`; append detailed capture to `log.md`. Distill deep dives into `agents/knowledge/`, procedures into `agents/procedures/`, and reference mirrors into `agents/reference/` at handoff. Put actionable deferred work in `agents/backlog.md`. Follow explicit workspace path overrides; small updates to an existing shared fact can go to its owning note. Link evidence and supporting artifacts instead of duplicating them. Make notes discoverable through the established index. Respect explicit no-write requests and report when persistence is prevented.
- For implementation investigations, preserve a durable session-local analysis note and distill it into shared knowledge/reference mirrors at handoff. Follow the workspace's mirror convention and the implementation guidance; do not defer preservation until someone asks for a summary.

## Investigate

- Read, measure, and run tests as needed for the question and within its execution constraints.
- Keep scripts, reports, and experiment outputs needed for review or reproduction in `agents/sessions/<session>/`; use root `tmp/` for disposable artifacts. Store retained external sources directly under descriptive names in root `reference/`, following the workspace layout. These may remain after the investigation; they are not changes to the assessed target.
- Before temporarily changing the target, preserve enough of its initial state to undo only your changes. Include existing edits and relevant untracked files; Git HEAD alone is not a baseline for a dirty working tree. Use an isolated copy or experiment when reliable in-place restoration is impractical.
- Temporary instrumentation and experimental implementations are allowed. Do not retain fixes, comments, formatting changes, or other target modifications. A clean Git state makes comparison easier; it does not authorize permanent changes or blanket cleanup.
- Keep experiments proportional to the question. Distinguish observations from explanations, and tested cases from broader claims. A benchmark on a fixture does not establish production performance or complete semantic equivalence.

## Finish

- Restore temporary target changes and verify against the initial state, preserving pre-existing work. Check for accidental changes and misplaced artifacts. Do not use broad reset/clean operations that could discard unrelated work.
- If restoration fails or evidence is insufficient, report exactly what remains unresolved. Do not claim the investigation completed cleanly.
- Verify the persistent notes contain the main findings, supporting evidence, uncertainty, and proposed next work. Distinguish proposals from approved decisions. Recommend implementation separately; investigation does not authorize applying the recommendation.
- In chat, provide a concise summary sufficient to understand the high-level result, important limitations, and recommended next steps, with links to the notes. Do not repeat the full report.
