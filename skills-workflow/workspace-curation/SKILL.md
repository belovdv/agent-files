---
name: workspace-curation
description: Check workspace notes, active sessions, backlog, goals, and navigation for stale or conflicting information. Use on request to assess or curate an existing workspace collection.
---

# Workspace curation

Use the workspace instructions and indexes to identify the collection and the scope requested by the user. Start with the relevant indexes, goals, and backlog. Open linked records as needed. Apply changes when the request authorizes curation. Report findings when the user asks for a check.

## Currency and consistency

- Check active and paused entries against their session files and archived records. Fix entries that point to work already archived. Flag uncertain session disposition for confirmation. Use age to prioritize inspection and evidence to establish disposition.
- Check whether current notes agree with the owning decisions and relevant files. Distinguish outdated claims from unresolved conflicts and historical records that still describe their original context.

## Backlog

Check `agents/backlog.md` for completed, duplicate, superseded, or underspecified work. Use added and last substantive revision dates to identify old entries; preserve the added date and update the revision date only for substantive changes. Verify completion against the relevant artifacts or decisions. Flag old, simple items that are still actionable so the user can decide whether to do or drop them. Group duplicates and preserve the context needed to resume actionable items.

## Goals and scope

Check whether the recorded goals and scope still make sense given the project's current state, constraints, and user decisions. Flag goals that have been met, overtaken by a later decision, or depend on assumptions that no longer hold. Check each project's goals separately in a multi-project workspace. Bring proposed changes to goals or scope to the user with the evidence behind them.

## Navigation

Check for broken links, missing routes to useful notes, and index entries whose descriptions no longer match their targets. Check affected links from the workspace entry point after any edits. Use `workspace-maintenance` if a repair changes the layout or discovery structure.

## Compaction and archiving

Merge overlapping material into the owning note and retain decisions, rationale, sources, and unresolved questions. Split long notes where readers benefit from loading topics separately. Archive superseded material when its history, evidence, or recovery value warrants retention. Use `session-handoff` for requested session handoff or archiving so distillation precedes moving the session; identify candidates during a general curation check. Verify affected links and archive entries. Follow existing permissions for user-owned files, moves, and deletion.

## Scratchpad cleanup

Revisit root `tmp/`. Move material worth retaining to persistent locations and verify copies and affected links before cleaning scratch files. Preserve proposals awaiting review, required backups, and evidence needed for recovery or reproducibility. If there's anything added by someone else, ask the user whether the full cleanup is needed. This directory is disposable and should be cleaned frequently.

Summarize what was checked, what changed, and which findings still need a decision. Link substantial findings or updated notes.
