---
type: vault-index
version: 2
updated: 2026-08-02
tags:
  - hibachi
  - vault-index
---

# Vault Index

This is the primary routing index for Hibachi.

Hibachi should read this file first and use its folder descriptions, filenames, tags, wikilinks, and Markdown links to decide which notes to load.

## Folder priority

1. `00 Inbox/`
2. `10 Daily/`
3. `20 Projects/`
4. `30 Areas/`
5. `40 Resources/`
6. `50 Research/`
7. `60 Decisions/`
8. `99 Archive/`

## Machine routing

- `00 Inbox/` — quick captures and unprocessed ideas
- `10 Daily/` — daily priorities, progress, blockers, and reviews
- `20 Projects/` — current project context, canonical task lists, decisions, research, meetings, and logs
- `30 Areas/` — ongoing responsibilities and working standards
- `40 Resources/` — reusable operating context, documentation, guides, and references
- `50 Research/` — active investigations and evidence that are not owned by one project
- `60 Decisions/` — accepted cross-project technical, product, business, and creative decisions
- `99 Archive/` — completed, abandoned, deprecated, or inactive material with the lowest retrieval priority

## Primary context

Read these notes when broad user or portfolio context is required:

- [[40 Resources/Operating Context/Working Profile]]
- [[20 Projects/Projects Index]]
- [[60 Decisions/Engineering Defaults]]

Useful tags:

- #context/working-profile
- #project/index
- #decision
- #engineering

## Inbox

Path: `00 Inbox/`

Contains quick captures, unprocessed ideas, temporary notes, voice-command captures, and information that has not yet been organised.

Primary note:

- [[00 Inbox/Quick Capture]]

Useful tags:

- #inbox
- #capture
- #idea

## Daily notes

Path: `10 Daily/`

Filename format: `YYYY-MM-DD.md`

Contains daily priorities, tasks, progress, blockers, decisions, and review notes.

Useful tags:

- #daily
- #task

## Task sources

Hibachi should prefer these locations when producing an on-demand daily brief:

- `10 Daily/`
- `20 Projects/*/Tasks.md`

Canonical task format:

- [ ] Open task
- [x] Completed task

Priority tags:

- #priority/high
- #priority/medium
- #priority/low

Unchecked checkboxes should appear only in canonical task lists or intentional daily notes. Reference notes, specifications, examples, and historical records should not use unchecked task syntax.

## Projects

Path: `20 Projects/`

Portfolio resolver:

- [[20 Projects/Projects Index]]

Each sufficiently active project should normally contain:

- `Project.md`
- `Tasks.md`
- `Decisions/`
- `Research/`
- `Meetings/`
- `Logs/`

`Project.md` is the canonical project overview.

`Tasks.md` is the canonical current project task list.

### Hibachi

Path: `20 Projects/Hibachi/`

- Project overview: [[20 Projects/Hibachi/Project]]
- Project tasks: [[20 Projects/Hibachi/Tasks]]

Useful tags:

- #project/hibachi
- #status/active

### Nexus

Path: `20 Projects/Nexus/`

- Project overview: [[20 Projects/Nexus/Project]]
- Project tasks: [[20 Projects/Nexus/Tasks]]

Useful tags:

- #project/nexus
- #status/active

## Areas

Path: `30 Areas/`

Contains long-running responsibilities without a fixed completion date.

Current areas:

- [[30 Areas/Software Development/Overview]]
- [[30 Areas/Content Creation/Overview]]
- [[30 Areas/Photography/Overview]]
- [[30 Areas/Business/Overview]]

Useful tags:

- #area/development
- #area/content
- #area/photography
- #area/business

## Resources

Path: `40 Resources/`

Contains reusable operating context, documentation, code snippets, guides, and learning material.

Primary operating context:

- [[40 Resources/Operating Context/Working Profile]]

## Research

Path: `50 Research/`

Contains general research notes, findings, source links, and investigations that are not owned by one project.

Useful tags:

- #research
- #source
- #reference

## Decisions

Path: `60 Decisions/`

Contains important accepted technical, product, business, and creative decisions that apply across projects.

Primary decision:

- [[60 Decisions/Engineering Defaults]]

Useful tags:

- #decision
- #architecture
- #product
- #engineering

## Templates

Path: `90 Templates/`

Contains reusable templates for daily notes, projects, research, and decisions.

Templates:

- [[90 Templates/Daily Note]]
- [[90 Templates/Project]]
- [[90 Templates/Decision]]
- [[90 Templates/Research]]

## Backups

Path: `98 Backups/`

Reserved for timestamped backups created before approved overwrite, move, bulk-edit, or delete operations.

## Archive

Path: `99 Archive/`

Contains completed, abandoned, deprecated, or inactive material.

Archive content should have the lowest retrieval priority.

## Attachments

Path: `Attachments/`

Contains images, documents, recordings, and other note attachments.

## Retrieval rules

When retrieving information:

1. Read this index first.
2. Identify the most relevant folder, filename, tag, or linked note.
3. Search only targeted locations.
4. Prefer canonical project, task, area, context, and decision notes.
5. Load only relevant Markdown notes.
6. Return source note paths when useful.
7. Do not treat snapshots, archive content, or unprocessed inbox material as current fact without checking the canonical note.
8. Do not load the entire vault by default.

## Write rules

Safe direct operations:

- Create a new note in an approved folder.
- Append to an explicitly identified note.

Higher-risk operations:

- Overwrite a note.
- Move notes.
- Bulk edit notes.
- Delete notes.
- Materially restructure this index.

Higher-risk operations should identify affected notes and create a timestamped backup before modification.
