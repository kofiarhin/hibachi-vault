---
type: project
project: Hibachi
status: active
created: 2026-08-01
updated: 2026-08-02
sources:
  - kofiarhin/hibachi
  - kofiarhin/hibachi-vault
  - kofiarhin/ideahub/projects/hibachi.md
tags:
  - project/hibachi
  - status/active
---

# Hibachi

Search tags: #project/hibachi #status/active #local-first #voice #engineering-assistant

## Outcome

Build a local-first, voice-driven engineering and operations assistant for one owner on native Windows. Hibachi uses a browser UI, a localhost Node.js companion service, MongoDB operational history, Obsidian durable knowledge, governed coding-agent reasoning, and typed controlled tools.

## Current state

- Application repository: https://github.com/kofiarhin/hibachi
- Vault repository: https://github.com/kofiarhin/hibachi-vault
- The vault repository was renamed from the mistaken `kofiarhin/hibachi-bault` slug on 2026-08-02; `kofiarhin/hibachi-vault` is canonical.
- The application repository contains the React/Vite/Tailwind client, Node.js/Express companion service, shared schemas, MongoDB models, Obsidian tools, controlled execution tools, startup scripts, policy files, and test suites.
- The browser interface has been changed from the initial dashboard into an immersive full-screen visualizer and command interface.
- Claude Code and Codex subprocess readiness, isolation, diagnostics, and failure handling have been implemented and hardened through repository changes.
- The current implementation supports deterministic Vault Index retrieval, targeted Markdown search, note reading, safe creation and append, and governed higher-risk note operations with backups.
- Windows vault-path configuration handling was improved at application commit `d3ec4783c7415b62a322511575722a469275bcd4`.
- This vault’s curated operating context was merged to `main` at commit `6c5d2a383374266edc013a7b0c4f6b9fb2fa113f`.
- A redistributable wake-word model is not bundled; push-to-talk remains the reliable input path.
- Full local verification was not rerun as part of the repository rename and must be treated as pending for the current application revision.

## Current focus

- Update local Git remotes or configuration that still use `hibachi-bault`.
- Configure the local machine dependencies and environment.
- Point `OBSIDIAN_VAULT_PATH` at the local clone of `kofiarhin/hibachi-vault` and verify `Vault Index.md` retrieval.
- Run the complete verification suite against the current application repository revision.
- Validate the end-to-end local startup, command, Obsidian retrieval, and governed execution flows on Windows.

## Canonical links

- Tasks: [[20 Projects/Hibachi/Tasks]]
- Portfolio: [[20 Projects/Projects Index]]
- Vault routing: [[Vault Index]]
- Working profile: [[40 Resources/Operating Context/Working Profile]]
- Engineering defaults: [[60 Decisions/Engineering Defaults]]

## Product scope

- Local React browser application served by the companion service.
- Local Node.js companion service bound to `127.0.0.1`.
- Typed text commands and push-to-talk voice input.
- Optional session-armed local wake-word activation.
- Local `whisper.cpp` transcription and browser speech synthesis.
- MongoDB conversation and workflow history.
- Obsidian long-term knowledge retrieval and note capture.
- Governed coding-agent reasoning with Hibachi-controlled tool execution.
- Grill, execution contracts, explicit approval, and protected-change confirmation.
- Registered project workspaces, Git safety, verification, draft pull requests, and Vercel preview deployments.
- Read-only public web research through isolated Crawlee and Playwright.

## Durable decisions

- Windows, Edge, and Chrome are the first supported platform and browsers.
- Use one root `package.json` with npm workspaces for `client`, `server`, and `packages/shared`.
- Use MongoDB for operational history and Obsidian for user-owned durable knowledge.
- Use `kofiarhin/hibachi-vault` as the canonical GitHub repository for this curated vault.
- Read `Vault Index.md` first, then use targeted folder, filename, tag, link, and text search.
- Do not use embeddings or a vector database in the MVP.
- Coding agents propose; Hibachi applies validated actions through typed allowlisted tools.
- Direct `main` changes, merges, production deployments, arbitrary shell execution, and administrator operations remain blocked inside Hibachi’s own governed execution model.
- Code-changing work requires a clean repository, task branch, Git checkpoint, verification, and approved scope.

## Known limitations

- Wake-word activation is unavailable until a compatible local model is added.
- The MVP is single-owner and Windows-first.
- Gmail, Calendar, Telegram, proactive scheduling, production deployment, and PR merge are outside the MVP.
- Complete local verification for the exact current application revision is not yet recorded in this note.

## Evidence

- Application repository README, source, and commits in `kofiarhin/hibachi`.
- Latest observed application commit: `d3ec4783c7415b62a322511575722a469275bcd4` on 2026-08-02.
- Canonical vault repository: `kofiarhin/hibachi-vault`.
- Curated vault population merge commit: `6c5d2a383374266edc013a7b0c4f6b9fb2fa113f`.
- Durable product decisions curated from `kofiarhin/ideahub/projects/hibachi.md`.
