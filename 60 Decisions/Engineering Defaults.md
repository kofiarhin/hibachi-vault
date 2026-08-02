---
type: decision
status: accepted
date: 2026-08-02
scope: cross-project
source: kofiarhin/ideahub/CONTEXT.md
tags:
  - decision
  - architecture
  - engineering
---

# Engineering Defaults

Search tags: #decision #architecture #engineering #mern

## Context

Kofi works primarily on full-stack JavaScript and TypeScript systems. Shared defaults reduce repeated setup decisions while allowing project-specific requirements to override them explicitly.

## Decision

Use the following defaults unless a project records a different decision:

- React with the latest Vite for frontend applications.
- Node.js and Express for backend APIs and companion services.
- MongoDB with Mongoose for durable application data.
- Tailwind CSS for styling.
- TanStack Query for server state.
- Redux Toolkit only for global client state shared across UI regions.
- Vitest and React Testing Library for frontend tests.
- Jest and Supertest for backend tests.
- Environment variables for secrets and environment-specific configuration.
- One root `package.json` by default, including workspace-based projects.
- Keep API and data-access logic outside UI components.
- Use non-main branches and evidence-backed verification for code-changing work.

## Consequences

- New projects begin from a consistent, testable baseline.
- Deviations should be recorded in the relevant project note or decision note.
- Package versions remain project-specific and should be selected from current compatible releases.

## Related notes

- [[40 Resources/Operating Context/Working Profile]]
- [[30 Areas/Software Development/Overview]]
- [[20 Projects/Projects Index]]
