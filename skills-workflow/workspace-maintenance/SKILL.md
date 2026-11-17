---
name: workspace-maintenance
description: Expand a workspace initialized with agent-files conventions by adding a structural location or changing how workspace files are organized and discovered.
---

# Workspace structure

Use this skill when expanding the layout or changing navigation. Read and update content at established paths using the workspace's regular instructions. Use the agent-files workspace setup/update workflow when an existing workspace needs migration to the current layout.

## Layout

Private means local-only and git-excluded. Create directories as their contents are needed. Root exclusions belong in `.git/info/exclude`.

- `agents/` is the private workspace collection.
  - `AGENTS.md` holds local additions and overrides to the root instructions. Read the root instructions first.
  - `index.md` is the discovery entry point, with separate **Layout** and **Topics** sections as described below.
  - `.agent-files.md` and `.agent-files.user.md` hold setup metadata and user overrides.
  - `user-notes.md` holds user-authored durable guidance, covering long- and short-term project goals, current status, scope, priorities, and corrections to common misconceptions or recurring failures. Suggest additions for the user to review; preserve user ownership.
  - `observations.md` holds compact agent-written additions on the same subjects, drawn from user corrections and persistent facts. Distinguish explicit user statements from agent interpretations, retain dates and source pointers, and resolve superseded entries when consolidating. Interpretations do not acquire the authority of user instructions.
  - `review.md` holds project-specific instructions for reviewers.
  - `reviews/<review-id>.md` holds detailed review findings retained for follow-up or reflection.
  - `knowledge/` holds deep dives into topics, including implementation understanding and supporting evidence.
  - `procedures/` holds workspace-specific guidance for recurring tasks.
  - `sessions/index.md` links to active and paused work. Describe each objective and the affected project or projects.
  - `sessions/<session>/` holds one substantial piece of work. Choose a unique, readable session name. Explicitly resumed work uses its existing directory; new work can start from distilled shared information.
    - `session.md` holds the current goal, decisions, state, and next steps. Its **Carry-forward** section keeps unexpected user corrections and explicit persistent facts salient until they are distilled into shared notes.
    - `log.md` is append-only capture for user inspection and later distillation. Preserve decisions, corrections, rejected approaches, findings, deferred work, and changes of direction, including context subsequently incorporated into other files. Append corrections rather than rewriting earlier entries. Agents append during work; routine context loading uses `session.md` and relevant notes. Read the log during session archiving-distillation to check for omissions; successful distillation archives the session directory. Milestone snapshots of `session.md` are unnecessary.
    - Keep session-local designs, measurements, scripts, and supporting evidence here when needed to resume, review, or reproduce the work. Link to shared knowledge and larger artifacts where they live.
  - `backlog.md` holds actionable deferred work across the workspace, with links to its originating session or evidence. Each entry records its added date and last substantive revision date. Keep a short entry-format note in the file; reading or reformatting does not refresh dates.
  - `reflections/` holds dated reflection records. Use `reflections/index.md` to find them when needed.
  - `reference/` holds concise mirrors of analyzed external references.
  - `roadmap.md` is an optional project roadmap.
  - `scripts/` holds reusable tools. Add shared operational collections only when an ongoing use justifies moving evidence out of sessions.
  - `archive/` holds historical evidence and material retained for recovery.
    - `sessions/index.md` links to archived sessions by name, date, and objective.
    - `sessions/<session>/` holds the final `session.md`, `log.md`, and remaining session-local files after handoff distillation and archiving.
- Root `reference/` holds external implementations, papers, and other source material directly under descriptive source names, such as `reference/<paper-name>.pdf` or `reference/<implementation>/`. Avoid media-type buckets such as `reference/papers/`; expand by a concrete topic or project only when needed.
- Root `tmp/` holds disposable workspace artifacts such as scratch scripts, routine build output, and intermediate results.

## Ownership and discovery

Create new work material in the current session first and distill reusable material at handoff. Exceptions include global backlog entries, user-authored notes, established review records, and small updates to an existing shared fact. Keep one owning copy and link to it. Cross-link review records with their session, requirements, and reviewed snapshot.

Workspace instructions require reading `index.md`, `user-notes.md`, `observations.md`, and `sessions/index.md` at startup when present. Keep routinely loaded guidance compact. Load the chosen session state when resuming work.

In `index.md`, **Layout** explains where categories of files live through short navigational descriptions and links. **Topics** is a skill-like discovery catalog spanning knowledge, procedures, references, and other useful material. Each entry gives a name, a concrete description of when to consult it, and a link to its entry document. For example:

- **Extraction decisions** — Consult when changing extraction algorithms or assessing determinism and performance tradeoffs. Covers settled choices and rejected alternatives. → `knowledge/extraction.md`

Read the compact catalog at startup, load entries relevant to the task, and revisit it when the task changes. Entry documents can link to deeper material for selective reading. Introduce a collection-level catalog only when size warrants it; its parent description must expose the subjects and task triggers underneath it. Keep instructions, findings, and decisions in their owning files. Project-specific subdivisions can be added as the workspace grows.

## Partial layouts and extensions

This layout is a starting structure that can grow. A subset is valid when omitted collections have no content. Add a location when material has a distinct owner or retrieval need that existing locations cannot serve clearly; document its purpose and discovery route. Avoid parallel destinations for the same material.

During ordinary work, follow the workspace's established instructions and paths. If they conflict with this specification, identify the mismatch and route migration to agent-files setup/update; do not silently migrate or create a competing structure. Resolve a missing path needed for the current task using a focused clarification. Structural expansion of a conforming workspace uses the procedure below.

## Expand the structure

1. Choose the owning location according to the kind of material. Put rules in instructions, reusable decisions and procedures in topic notes, work status in summaries, and actionable deferred work in the backlog.
2. Add the smallest navigation change that makes the new material discoverable. Indexes contain links and short descriptions of what each target covers and when to read it. Route to topics or collections. Keep status, decisions, instructions, and findings in their owning files.
3. Use topic catalogs for progressive discovery. A catalog entry gives the topic, when it is useful, and where to read it. A topic note can link to deeper evidence or procedures. Workspace instructions point to the catalog.
4. When splitting or reorganizing files in the current layout, preserve current decisions, unique evidence, and required backups. Update affected links, then verify the new paths from the workspace entry point. Follow the workspace's permissions for entry-point changes and deletion.
