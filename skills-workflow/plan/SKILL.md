---
name: plan
description: Discuss and refine an agreed plan before implementation when planning is requested or a substantial task lacks an agreed design.
---

# Planning

This is a discussion workflow; it does not change the harness collaboration mode.

When invoked, discuss and refine the topic until there is a shared vision. Do not implement the proposed changes during the discussion. Planning notes, investigation scripts, benchmark outputs, and the final design document are allowed as described below.

Full-scale planning should be done in a separate session - it requires lots of back-and-forth discussion. It should end with creation of a design document to be used in the next session.

In most cases investigations should be conducted by (low-cost) subagents. Even during the first iteration, intended to establish context, it's better to ask a subagent to filter what's relevant and read only that.

## First iteration

- Collect necessary context: relevant sessions, todos, plans, roadmaps, code, and concise measurements. Avoid broad reading without a reason.
- Clarify uncertainty about the user's meaning or the session's goal. Do not ask the user to supply the solution; developing it is part of planning.
- Offer a basic sketch and identify the high-level decisions. Keep the sketch cheap to revise.

## Following iterations

- Briefly restate corrections so the user can verify your understanding.
- Update the proposal concisely.
- Ask a focused round of questions, at most three, with recommendations and tradeoffs where useful.
- Mention remaining discussion topics in one short paragraph. Keep later iterations fast unless more research is requested.
- Keep unrelated fixes and refactors for the backlog or another session.

## Writing files

During the session:
- Keep a tiny note reflecting high-level design choices, including things intentionally deferred, and deferred discussion points.
- When a large investigation was conducted - save a knowledge/stats file.
- Use (write) small scripts and run benchmarks if needed.

In the end:
- Write a design document (do not write it during the session though).

Other than that do not modify anything without explicit approval.

## Agreement and handoff

Load [final actions](./SKILL.END.md) when agreement is achieved.
