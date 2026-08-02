---
type: project
project: Hibachi
status: active
created: 2026-08-01
updated: 2026-08-02
sources:
  - kofiarhin/hibachi
  - kofiarhin/ideahub/projects/hibachi.md
tags:
  - project/hibachi
  - status/active
---

# Hibachi

Search tags: #project/hibachi #status/active #local-first #voice #engineering-assistant

## Outcome

Build a local-first, voice-driven engineering and operations assistant for one owner on native Windows. Hibachi uses a browser UI, a localhost Node.js companion service, MongoDB operational history, Obsidian durable knowledge, Claude Code reasoning, and typed governed tools.

## Current state

- Repository: https://github.com/kofiarhin/hibachi
- The repository contains the React/Vite/Tailwind client, Node.js/Express companion service, shared schemas, MongoDB models, Obsidian tools, controlled execution tools, startup scripts, policy files, and test suites.
- The browser interface has been changed from the initial dashboard into an immersive full-screen visualizer and command interface.
- Claude Code subprocess readiness and failure diagnostics have been hardened so unavailable, unauthenticated, incompatible, and runtime failure states are distinguishable.
- The current implementation supports deterministic Vault Index retrieval, targeted Markdown search, note reading, safe creation and append, and governed higher-risk note operations with backups.
- A redistributable wake-word model is not bundled; push-to-talk remains the reliable input path.
- Full local verification was not rerun as part of this vault population and must be treated as pending for the current repository revision.

## Current focus

- Configure the local machine dependencies and environment.
- Point `OBSIDIAN_VAULT_PATH` at this vault and verify `Vault Index.md` retrieval.
- Run the complete verification suite against the current repository revision.
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
- Claude Code reasoning with Hibachi-controlled tool execution.
- Grill, execution contracts, explicit approval, and protected-change confirmation.
- Registered project workspaces, Git safety, verification, draft pull requests, and Vercel preview deployments.
- Read-only public web research through isolated Crawlee and Playwright.

## Durable decisions

- Windows, Edge, and Chrome are the first supported platform and browsers.
- Use one root `package.json` with npm workspaces for `client`, `server`, and `packages/shared`.
- Use MongoDB for operational history and Obsidian for user-owned durable knowledge.
- Read `Vault Index.md` first, then use targeted folder, filename, tag, link, and text search.
- Do not use embeddings or a vector database in the MVP.
- Claude Code proposes; Hibachi applies validated actions through typed allowlisted tools.
- Direct `main` changes, merges, production deployments, arbitrary shell execution, and administrator operations remain blocked.
- Code-changing work requires a clean repository, task branch, Git checkpoint, verification, and approved scope.

## Known limitations

- Wake-word activation is unavailable until a compatible local model is added.
- The MVP is single-owner and Windows-first.
- Gmail, Calendar, Telegram, proactive scheduling, production deployment, and PR merge are outside the MVP.

## Evidence

- Application repository README and source on `kofiarhin/hibachi`.
- Recent repository commits through `5c03c7e8f55a51398ad0cb6c2e34cef4b0f3703c` observed on 2026-08-02.
- Durable product decisions curated from `kofiarhin/ideahub/projects/hibachi.md`.
