---
name: reflect-conversation
description: Reflect on selected conversation history to identify durable preferences, recurring workflow lessons, and useful new or revised skills when explicitly requested.
---

# Reflect and improve instructions

Use the current conversation or the history selected by the user. Ask which conversation if the target is ambiguous; do not scan all chats or private files by default. Distinguish explicit user corrections and decisions from agent suggestions, temporary experiments, and your own inferences.

Identify recurring pain points and procedures that would change future behavior. Compare candidates with the existing rules, preferences, skills, and suitable built-in capabilities. Do not turn a one-off task constraint into a global rule or create a skill that only repeats generic model behavior.

Report a compact list: evidence from the conversation, intended scope and audience, proposed owning file, whether it changes existing policy, and any unresolved interpretation. Separate public project facts from private context. Group related corrections instead of preserving a transcript.

If the user requested reflection only, propose changes without applying them. If instruction or skill creation is also authorized, update the appropriate source within that scope. For a reusable procedure, create or refine a focused skill with a concise name, trigger description, and task-relevant instructions; keep detailed conditional material out of the permanent prompt. Follow an available skill-authoring procedure and validate the result. Check for existing equivalents before adding anything.

Do not silently change fundamental rules, install the result in other setups, or modify protected instruction files. Surface candidate local improvements for the user to port manually. Link the resulting files and report remaining decisions.

Pay special attention to sessions that didn't end with an explicit result: they might have been abandoned because something went really wrong.
