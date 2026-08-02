---
type: project
project: Nexus
status: active
source: kofiarhin/ideahub/projects/nexus.md
source_updated: 2026-07-30
captured: 2026-08-02
tags:
  - project/nexus
  - status/active
  - source/ideas-hub
---

# Nexus

This note contains a small, non-sensitive snapshot copied from the canonical Ideas Hub project record.
It reflects the source as last updated on 2026-07-30 and is not an automatic live status feed.

## Summary

Nexus is an AI-native productivity and knowledge operating system using a React/Vite client,
an Express MVC API, a GitHub-backed Markdown Vault, and NVIDIA-only reasoning.

## Repositories

- Application: https://github.com/kofiarhin/nexus
- Vault: https://github.com/kofiarhin/nexus-vault
- Live URL: not deployed in the source record

## Recorded state

- The application foundation exists on branch `agent/foundation-mvp` in draft pull request #1.
- The application includes a React/Vite client shell, Express MVC API, environment validation,
  request IDs, standard errors, health endpoints, deterministic project listing, read-only Vault access,
  initial tests, Heroku configuration, a PRD, and a technical specification.
- Application dependency installation, tests, linting, and the client build were recorded as unverified
  because the available npm mirror returned package 404 responses.
- The Vault foundation exists on branch `agent/vault-foundation` in draft pull request #1.
- The Vault includes an operating charter, identity and working-style records, project context,
  deterministic registries, planning, tasks, roadmap, changelog, system rules, and reusable contracts.
- Both pull requests were recorded as open drafts, unmerged, undeployed, and not fully verified.

## Key decisions

- Frontend: React and Vite.
- Backend: Node.js, Express, and MVC separation.
- Client hosting target: Vercel.
- API hosting target: Heroku.
- Durable knowledge storage: GitHub repositories and portable Markdown.
- AI provider: NVIDIA only for reasoning workflows.
- Deterministic retrieval does not use AI.
- Authentication is excluded from the MVP.
- Retrieval begins with `NEXUS.md`, then identity, registry, project index, project instructions,
  relevant Markdown, and AI only when needed.
- Agents must not load the entire Vault by default.

## Recorded next actions

- Review both draft pull requests.
- Restore working npm dependency access.
- Generate and commit `package-lock.json`.
- Run application tests, linting, and the client build against the exact PR revision.
- Verify the application parser against the Vault `registry/PROJECTS.md` contract.

## Source

- Ideas Hub record: `projects/nexus.md`
- Source last updated: 2026-07-30
