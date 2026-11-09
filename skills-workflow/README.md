# Workflow skills

Prompts to initiate personal workflow styles:
- session kind description (plan)
- workspace organization (new-reference)

[Plan](plan/SKILL.md): initiate a planning session.
- Note: has [end](plan/SKILL.END.md). If possible it should be another context injection which triggers only at the end of planning session. Fallback - add "look at the file at the end"-like line to the main file. Fallback - append to the same skill.

[New-Reference](new-reference/SKILL.md): analyze a reference.
- Note: it's important to sync paths mentioned here with [this](../workspace-local-layout/).
- Note: it's probably better to make this work not only on the first access, but on consecutive ones as well (or use a separate skill): it has a lot of specific agent optimizations.

[Reflect-Conversation](reflect-conversation/SKILL.md): a workflow for extracting durable lessons from conversations.
- Note: most high-level harnesses should have built-in version for this - prefer it.
