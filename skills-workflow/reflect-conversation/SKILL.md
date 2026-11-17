---
name: reflect-conversation
description: Reflect on selected conversation history to identify durable preferences, recurring workflow lessons, and useful changes to user practices, workspace knowledge, or agent guidance when explicitly requested.
---

# Reflect and improve working practices

Use the current conversation or the history selected by the user. Ask which conversation if the target is ambiguous; do not scan all chats or private files by default. Establish the reviewed range and chronological order, including the latest user objective. Distinguish history fetched from content actually inspected; record truncation or unavailable turns.

Read ordinary user replies as well as explicit complaints and feedback blocks. Look for repeated clarification, softened corrections, narrowed scope, and unanswered requests; distinguish failures from new requirements and normal design development. Local search hints may help locate examples but do not replace reading surrounding exchanges.

Pay particular attention to sessions without an explicit ending. Check whether the last response addressed the latest objective and whether requested actions were verified. Silence, an assistant final message, or an earlier completed task does not establish the disposition of later work. Report the ending as unknown when evidence is insufficient.

For delegated analysis, supply bounded session ranges and request ordered turn references with short supporting excerpts, including relevant counterexamples. Verify consequential interpretations against the original turns before consolidating them. Separate direct evidence, user-reported experience, and inferred causes; a sample from one harness or model cannot establish a cross-model cause, but it does not invalidate the user's reported experience elsewhere.

Identify remedies in agent behavior, workspace organization, and the user's workflow. Prefer the least burdensome effective change. A short intent marker or brief mismatch/stop reason may help when it saves repeated clarification; finding existing knowledge and detecting repeated investigation remain agent responsibilities. Do not make the user responsible for enumerating every instance of a correction.

Distinguish user corrections and approved decisions from agent suggestions and temporary experiments; do not promote the latter into user preferences without supporting evidence.

Compare candidates with existing rules, preferences, skills, and suitable built-in capabilities. Do not turn a one-off task constraint into a global rule or create a skill that only repeats generic model behavior. Group related corrections rather than preserving a transcript in the findings.

Put substantial findings in the workspace's designated notes when writing is authorized; give a concise chat summary with links. For each proposal record evidence, intended scope and audience, owning file, whether it changes existing policy, and unresolved interpretations. Separate public project facts from private context. In the dated reflection record, include the sessions and ranges actually reviewed, evidence limits, pending changes, and any observed results of earlier adopted changes. Link the record from the workspace's reflection index when one exists. Use recorded coverage to guide future reviews.

If the user requested reflection only, propose changes without applying them. If instruction or skill creation is also authorized, update the appropriate source within that scope. For a reusable procedure, create or refine a focused skill with a concise name, trigger description, and task-relevant instructions; keep detailed conditional material out of the permanent prompt. Follow an available skill-authoring procedure and validate the result. Check for existing equivalents before adding anything.

Do not silently change fundamental rules, install the result in other setups, or modify protected instruction files. Surface candidate local improvements for the user to port manually. Link the resulting files and report remaining decisions.
