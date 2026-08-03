---
type: project
project: Hibachi
status: active
created: 2026-08-01
updated: 2026-08-03
sources:
  - kofiarhin/hibachi
  - kofiarhin/hibachi-vault
  - kofiarhin/ideahub/projects/hibachi.md
tags:
  - project/hibachi
  - status/active
---

# Hibachi

Search tags: #project/hibachi #status/active #local-first #voice #engineering-assistant #elevenlabs

## Outcome

Build a local-first, voice-driven engineering and operations assistant for one owner on native Windows. Hibachi uses a browser UI, a localhost Node.js companion service, MongoDB operational history, Obsidian durable knowledge, governed coding-agent reasoning, typed controlled tools, local speech input, and ElevenLabs speech output.

## Current state

- Application repository: https://github.com/kofiarhin/hibachi
- Vault repository: https://github.com/kofiarhin/hibachi-vault
- The application repository contains the React/Vite/Tailwind client, Node.js/Express companion service, shared schemas, MongoDB models, Obsidian tools, controlled execution tools, startup scripts, policy files, and test suites.
- The browser interface uses an immersive full-screen visualizer, command input, push-to-talk controls, conversation history, speech status, and stop controls.
- ElevenLabs TTS was implemented on application `main` at commit `0b29390690a731383293cfeecf0f677953d8f826`.
- Branch `fix/elevenlabs-sole-tts-provider` removes browser `SpeechSynthesis` and automatic browser fallback so ElevenLabs is the sole spoken-output provider.
- Duplicate ElevenLabs playback was traced to the same logical assistant response arriving through both WebSocket delivery and the post-command conversation refresh with different message IDs.
- The branch now applies bounded logical-response deduplication during Redux ingestion and speech playback. Identical responses inside five seconds are suppressed, while legitimate repeated responses later remain allowed.
- The latest GitHub-recorded fix branch head observed during implementation was `a13d528477297a597fbbb12078902e50fc123479`. A final local test-only TypeScript correction was applied after that observed head and still requires push evidence.
- Local Windows verification shown on 2026-08-03 passed:
  - client tests: 12 files, 131 tests;
  - server tests: 13 suites, 398 tests;
  - root typecheck;
  - lint;
  - production build.
- End-to-end tests, policy verification, exact runtime network-count confirmation, branch merge, and deployment remain unrecorded.
- Obsidian support includes deterministic `Vault Index.md` retrieval, targeted Markdown search, note reading, safe creation and append, and governed higher-risk operations with backups.
- Google Chrome is the default local browser. Microsoft Edge remains the supported browser fallback.
- The application is not publicly deployed.

## Current focus

- Commit and push the final local test correction on `fix/elevenlabs-sole-tts-provider`.
- Run `npm run test:e2e` and `npm run verify:policies` on the exact final branch revision.
- Confirm one logical assistant response creates exactly one `POST /api/v1/voice/speech` request and one ElevenLabs playback.
- Confirm a new response cancels existing playback, reload does not replay old responses, and offline behavior remains text-only.
- Review and merge the fix branch only after exact final verification evidence is recorded.
- Keep `OBSIDIAN_VAULT_PATH` pointed at the local clone of this repository and verify project retrieval and daily briefs.

## Canonical links

- Tasks: [[20 Projects/Hibachi/Tasks]]
- Latest log: [[20 Projects/Hibachi/Logs/2026-08-03 ElevenLabs TTS]]
- Portfolio: [[20 Projects/Projects Index]]
- Vault routing: [[Vault Index]]
- Working profile: [[40 Resources/Operating Context/Working Profile]]
- Engineering defaults: [[60 Decisions/Engineering Defaults]]

## Product scope

- Local React browser application served by the companion service.
- Local Node.js companion service bound to `127.0.0.1`.
- Typed text commands and push-to-talk voice input.
- Optional session-armed local wake-word activation.
- Local `whisper.cpp` transcription.
- ElevenLabs-only spoken output with server-side credentials and ephemeral streamed audio.
- MongoDB conversation and workflow history.
- Obsidian long-term knowledge retrieval and note capture.
- Governed coding-agent reasoning with Hibachi-controlled tool execution.
- Grill, execution contracts, explicit approval, and protected-change confirmation.
- Registered project workspaces, Git safety, verification, draft pull requests, and Vercel preview deployments.
- Read-only public web research through isolated Crawlee and Playwright.

## Durable decisions

- Windows, Chrome, and Edge are the first supported platform and browsers.
- Use one root `package.json` with npm workspaces for `client`, `server`, and `packages/shared`.
- Use MongoDB for operational history and Obsidian for user-owned durable knowledge.
- Use `kofiarhin/hibachi-vault` as the canonical GitHub repository for this curated vault.
- Read `Vault Index.md` first, then use targeted folder, filename, tag, link, and text search.
- Do not use embeddings or a vector database in the MVP.
- Use ElevenLabs as the sole TTS provider; do not invoke browser `SpeechSynthesis` as a fallback.
- Store the ElevenLabs API key only in server-side local environment configuration.
- Do not persist generated TTS audio.
- If ElevenLabs is unavailable, keep the application text-only.
- Use one live speech adapter and bounded logical-response deduplication across WebSocket and HTTP refresh paths.
- Coding agents propose; Hibachi applies validated actions through typed allowlisted tools.
- Direct `main` changes, merges, production deployments, arbitrary shell execution, and administrator operations remain blocked inside Hibachi’s own governed execution model.
- Code-changing work requires a clean repository, task branch, Git checkpoint, verification, and approved scope.

## Known limitations

- Wake-word activation is unavailable until a compatible local model is added.
- The MVP is single-owner and Windows-first.
- ElevenLabs speech requires internet access and available account quota.
- Gmail, Calendar, Telegram, proactive scheduling, production deployment, and PR merge are outside the MVP.
- E2E, policy, and exact runtime request-count evidence are still pending for the final fix revision.

## Evidence

- Application repository README, source, and commits in `kofiarhin/hibachi`.
- ElevenLabs implementation commit on application `main`: `0b29390690a731383293cfeecf0f677953d8f826`.
- Latest observed remote fix branch head: `a13d528477297a597fbbb12078902e50fc123479`.
- User-provided local verification screenshots on 2026-08-03 showing client tests, server tests, typecheck, lint, and build passing.
- Canonical Ideas Hub record: `kofiarhin/ideahub/projects/hibachi.md`.
- Canonical vault repository: `kofiarhin/hibachi-vault`.
