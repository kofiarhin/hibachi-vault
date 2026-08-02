---
type: vault-index
version: 1
updated: 2026-08-02
tags:
  - hibachi
  - vault-index
---

# Vault Index

This is the primary routing index for Hibachi.

Hibachi should read this file first and use the folder descriptions,
filenames, tags, wikilinks, and Markdown links to decide which notes to load.

## Folder priority

1. `00 Inbox/`
2. `10 Daily/`
3. `20 Projects/`
4. `30 Areas/`
5. `40 Resources/`
6. `50 Research/`
7. `60 Decisions/`
8. `99 Archive/`

## Inbox

Path: `00 Inbox/`

Contains quick captures, unprocessed ideas, temporary notes, voice-command
captures, and information that has not yet been organised.

Primary note:

- [[00 Inbox/Quick Capture]]

Useful tags:

- `#inbox`
- `#capture`
- `#idea`

## Daily notes

Path: `10 Daily/`

Filename format:

`YYYY-MM-DD.md`

Contains daily priorities, tasks, progress, blockers, decisions, and review
notes.

Useful tags:

- `#daily`
- `#task`

## Task sources

Hibachi should search these locations when producing an on-demand daily brief:

- `10 Daily/`
- `20 Projects/*/Tasks.md`

Task format:

- [ ] Open task
- [x] Completed task

Priority tags:

- `#priority/high`
- `#priority/medium`
- `#priority/low`

## Projects

Path: `20 Projects/`

Each project should normally contain:

- `Project.md`
- `Tasks.md`
- `Decisions/`
- `Research/`
- `Meetings/`
- `Logs/`

`Project.md` is the canonical project overview.

`Tasks.md` is the canonical project task list.

### Hibachi

Path: `20 Projects/Hibachi/`

Project overview:

- [[20 Projects/Hibachi/Project]]

Ideas Hub source snapshot:

- [[20 Projects/Hibachi/Ideas Hub Snapshot]]

Project tasks:

- [[20 Projects/Hibachi/Tasks]]

Useful tags:

- `#project/hibachi`
- `#status/active`
- `#source/ideas-hub`

### Nexus

Path: `20 Projects/Nexus/`

Project overview and Ideas Hub source snapshot:

- [[20 Projects/Nexus/Project]]

Useful tags:

- `#project/nexus`
- `#status/active`
- `#source/ideas-hub`

## Areas

Path: `30 Areas/`

Contains long-running responsibilities without a fixed completion date.

Current areas:

- Software Development
- Content Creation
- Photography
- Business

## Resources

Path: `40 Resources/`

Contains reusable references, documentation, code snippets, guides, and
learning material.

## Research

Path: `50 Research/`

Contains general research notes, findings, source links, and investigations
that are not owned by one project.

Useful tags:

- `#research`
- `#source`
- `#reference`

## Decisions

Path: `60 Decisions/`

Contains important technical, product, business, and creative decisions that
apply across projects.

Useful tags:

- `#decision`
- `#architecture`
- `#product`

## Templates

Path: `90 Templates/`

Contains reusable templates for daily notes, projects, research, and
decisions.

Templates:

- [[90 Templates/Daily Note]]
- [[90 Templates/Project]]
- [[90 Templates/Decision]]
- [[90 Templates/Research]]

## Backups

Path: `98 Backups/`

Reserved for timestamped backups created before approved overwrite, move,
bulk-edit, or delete operations.

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
3. Search only the targeted locations.
4. Load only relevant Markdown notes.
5. Return the source note paths when useful.
6. Do not treat the archive as a primary source unless explicitly requested.

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

Higher-risk operations should identify affected notes and create a timestamped
backup before modification.
