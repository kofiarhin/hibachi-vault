---
type: project-source
project: Hibachi
status: snapshot
source: kofiarhin/ideahub/projects/hibachi.md
source_updated: 2026-08-01
captured: 2026-08-02
tags:
  - project/hibachi
  - source/ideas-hub
  - snapshot
---

# Hibachi — Ideas Hub Snapshot

This note contains a small, non-sensitive snapshot copied from the canonical Ideas Hub project record.
It reflects the source as last updated on 2026-08-01 and is not an automatic live status feed.

## Purpose

Hibachi is a local-first, voice-driven engineering and operations assistant using a browser UI,
a local Node.js companion service, Obsidian, MongoDB, and governed tools.

## Repository

- Application repository: https://github.com/kofiarhin/hibachi
- Intended platform: native Windows
- Initial browsers: Microsoft Edge and Google Chrome
- Distribution: developer-run source project

## Core product decisions

- React, Vite, TypeScript, and Tailwind for the browser UI.
- One root `package.json` with npm workspaces for `client`, `server`, and `packages/shared`.
- Typed commands, push-to-talk, optional local wake-word activation, local `whisper.cpp`, and browser speech synthesis.
- MongoDB for operational history and Obsidian for durable user-owned knowledge.
- Obsidian retrieval begins with `Vault Index.md`, then uses targeted folder, filename, tag, and text search.
- No embeddings or vector database in the MVP.

## Governance decisions

- Clear, reversible, low-risk requests may use a direct path.
- Material work enters the Grill, one material question at a time.
- Execution starts only after an approved execution contract.
- Approval is invalidated when scope, files, dependencies, risks, targets, or verification materially change.
- Only Hibachi executes typed, allowlisted tools.
- One tool-executing workflow may run at a time.

## Delivery and safety decisions

- Work occurs on non-`main` task branches with a clean repository and Git safety checkpoint.
- Tests, linting, type checks, builds, and browser verification gate publication actions.
- Approved commits, branch pushes, and draft pull requests are supported; merge is excluded from the MVP.
- The local service binds to `127.0.0.1` and uses pairing, session, CSRF, origin, WebSocket, redaction, and policy-integrity controls.
- Administrator-level Windows operations are blocked.

## Source

- Ideas Hub record: `projects/hibachi.md`
- Source last updated: 2026-08-01
