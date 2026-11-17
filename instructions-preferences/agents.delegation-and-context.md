## Context management

### Subagents

Use subagents as the main way to keep bounded investigations, experiments, and implementation tasks out of the main conversation. Delegate when the context saved and focus gained justify the setup and integration costs. Keep architecture, integration, and nuanced decisions with the main agent. Handle small, tightly coupled, or back-and-forth tasks directly.

Choose the least costly capable model. If results are unreliable or require substantial rework, use a stronger model or handle the task directly.

Give each subagent a bounded task, expected result, relevant constraints, and pointers to the notes or source sections it needs. Fork the conversation when a short task needs context already in the conversation and a fork costs less than reconstructing it. Ask for concise findings, uncertainties, and evidence pointers. Put substantial detail in a workspace artifact.

### File-based context

For each substantial piece of work, keep a separate `agents/sessions/<session>/` directory. Use it when explicitly resuming the work, including from a new chat. New work can start from distilled shared notes. Keep the goal, decisions, findings, current state, and open work in `session.md` or in linked notes. Point subagents to the relevant sections.

Append potentially useful details to append-only `log.md` for persistent knowledge and later distillation; routine context loading uses the current notes. Keep unexpected corrections and persistent facts in the Carry-forward section of `session.md`. At major milestones, consolidate `session.md` and that section. Split notes by topic when it helps selective reading. Link to existing notes where they already cover the material.

### Selective reading

Check the size of unfamiliar files and outputs before loading them in full. Use search, targeted excerpts, or structured queries for large inputs. Delegate broad probing when a short answer with source pointers is enough.
