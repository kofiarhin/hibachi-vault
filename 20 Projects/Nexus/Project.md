---
type: project
project: Nexus
status: active
updated: 2026-08-02
source: kofiarhin/ideahub/projects/nexus.md
source_updated: 2026-07-30
tags:
  - project/nexus
  - status/active
  - source/ideas-hub
---

# Nexus

Search tags: #project/nexus #status/active #knowledge-system #nvidia

## Outcome

Build an AI-native productivity and knowledge operating system using a React/Vite client, an Express MVC API, a GitHub-backed Markdown Vault, and NVIDIA-only reasoning.

## Current state

- Application: https://github.com/kofiarhin/nexus
- Vault: https://github.com/kofiarhin/nexus-vault
- The application foundation was recorded on branch `agent/foundation-mvp` in draft pull request #1.
- The application includes a React/Vite client shell, Express MVC API, environment validation, request IDs, standard errors, health endpoints, deterministic project listing, read-only Vault access, initial tests, Heroku configuration, a PRD, and a technical specification.
- The Vault foundation was recorded on branch `agent/vault-foundation` in draft pull request #1.
- The Vault includes an operating charter, identity and working-style records, deterministic registries, project records, planning, tasks, roadmap, changelog, system rules, and reusable contracts.
- Dependency installation, lockfile generation, application tests, linting, build, parser compatibility, review, merge, and deployment were not verified in the Ideas Hub source record.

## Current focus

- Review the application and Vault draft pull requests.
- Restore reliable npm dependency access.
- Generate and commit the lockfile.
- Run application tests, linting, and the client build against the exact revision.
- Verify the application parser against the Vault `registry/PROJECTS.md` contract.

## Canonical links

- Tasks: [[20 Projects/Nexus/Tasks]]
- Portfolio: [[20 Projects/Projects Index]]
- Vault routing: [[Vault Index]]

## Durable decisions

- Frontend: React and Vite.
- Backend: Node.js and Express with MVC separation.
- Client hosting target: Vercel.
- API hosting target: Heroku.
- Durable knowledge storage: GitHub repositories and portable Markdown.
- AI reasoning provider: NVIDIA only.
- Deterministic retrieval does not use AI.
- Authentication is excluded from the MVP.
- Retrieval begins with `NEXUS.md`, then identity, registry, project index, project instructions, relevant Markdown, and AI only when needed.
- Agents must not load the entire Vault by default.

## Source

Curated from `kofiarhin/ideahub/projects/nexus.md`, last recorded as updated on 2026-07-30. This note does not infer later merge, deployment, or verification state.
