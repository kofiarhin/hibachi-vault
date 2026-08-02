---
type: task-list
project: Hibachi
status: active
updated: 2026-08-02
tags:
  - project/hibachi
  - task
---

# Hibachi Tasks

Search tags: #project/hibachi #task #status/active

Only current actionable work uses unchecked checkboxes in this note.

## High priority

- [ ] Configure `OBSIDIAN_VAULT_PATH` to this vault and verify `Vault Index.md` retrieval #priority/high
- [ ] Verify targeted search returns the Working Profile, Projects Index, Hibachi project note, and Engineering Defaults #priority/high
- [ ] Run `npm run lint`, `npm run typecheck`, `npm test`, `npm run build`, `npm run test:e2e`, and `npm run verify:policies` against the current repository revision #priority/high
- [ ] Validate `npm run hibachi` end-to-end on native Windows with MongoDB, Claude Code, Git, GitHub CLI, Vercel CLI, `whisper.cpp`, Edge or Chrome, and the configured vault #priority/high

## Medium priority

- [ ] Verify safe Obsidian note creation and append against a disposable test note #priority/medium
- [ ] Verify governed overwrite, move, and delete operations create recoverable backups and enforce approval #priority/medium
- [ ] Decide whether to bundle a compatible redistributable wake-word model or retain push-to-talk only #priority/medium
- [ ] Review the daily brief against real project task notes and remove any noisy task sources #priority/medium

## Completed

- [x] Create the local-first Hibachi application repository and implementation foundation
- [x] Implement the React client, companion service, shared schemas, policies, MongoDB models, and test structure
- [x] Implement deterministic `Vault Index.md` retrieval and targeted Markdown note search
- [x] Implement safe note creation, append, and governed high-risk vault operations with backups
- [x] Implement pairing, session, CSRF, origin, WebSocket, redaction, and policy-integrity controls
- [x] Improve Claude Code readiness detection and subprocess failure diagnostics
- [x] Replace the initial dashboard with the immersive visualizer and command interface
- [x] Populate the vault with curated operating context and project routing

## Related notes

- [[20 Projects/Hibachi/Project]]
- [[Vault Index]]
