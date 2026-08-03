---
type: task-list
project: Hibachi
status: active
updated: 2026-08-03
tags:
  - project/hibachi
  - task
---

# Hibachi Tasks

Search tags: #project/hibachi #task #status/active #elevenlabs

Only current actionable work uses unchecked checkboxes in this note.

## High priority

- [ ] Commit and push the final local test-only TypeScript correction on `fix/elevenlabs-sole-tts-provider` #priority/high
- [ ] Run `npm run test:e2e` against the exact final fix branch revision #priority/high
- [ ] Run `npm run verify:policies` against the exact final fix branch revision #priority/high
- [ ] Verify one logical assistant response creates exactly one `POST /api/v1/voice/speech` request and one ElevenLabs playback #priority/high
- [ ] Verify a new response cancels the previous playback and only the latest response continues #priority/high
- [ ] Verify reload does not replay old responses and offline mode remains text-only #priority/high
- [ ] Review and merge `fix/elevenlabs-sole-tts-provider` only after final verification evidence is retained #priority/high
- [ ] Configure `OBSIDIAN_VAULT_PATH` to this vault and verify `Vault Index.md` retrieval #priority/high

## Medium priority

- [ ] Verify targeted search returns the Working Profile, Projects Index, Hibachi project note, and Engineering Defaults #priority/medium
- [ ] Validate `npm run hibachi` end-to-end on native Windows with MongoDB, coding CLIs, Git, GitHub CLI, Vercel CLI, `whisper.cpp`, Chrome or Edge, ElevenLabs, and the configured vault #priority/medium
- [ ] Verify safe Obsidian note creation and append against a disposable test note #priority/medium
- [ ] Verify governed overwrite, move, and delete operations create recoverable backups and enforce approval #priority/medium
- [ ] Decide whether to bundle a compatible redistributable wake-word model or retain push-to-talk only #priority/medium
- [ ] Review the daily brief against real project task notes and remove noisy task sources #priority/medium

## Completed

- [x] Create the local-first Hibachi application repository and implementation foundation
- [x] Implement the React client, companion service, shared schemas, policies, MongoDB models, and test structure
- [x] Implement deterministic `Vault Index.md` retrieval and targeted Markdown note search
- [x] Implement safe note creation, append, and governed high-risk vault operations with backups
- [x] Implement pairing, session, CSRF, origin, WebSocket, redaction, and policy-integrity controls
- [x] Improve coding-agent readiness detection and subprocess failure diagnostics
- [x] Replace the initial dashboard with the immersive visualizer and command interface
- [x] Populate the vault with curated operating context and project routing
- [x] Implement ElevenLabs TTS with server-side credential isolation and streamed audio
- [x] Remove browser `SpeechSynthesis` and browser TTS fallback on the fix branch
- [x] Add bounded logical-response deduplication for WebSocket and HTTP refresh paths
- [x] Pass local client tests: 12 files and 131 tests
- [x] Pass local server tests: 13 suites and 398 tests
- [x] Pass root typecheck after the final test correction
- [x] Pass lint
- [x] Pass production build

## Related notes

- [[20 Projects/Hibachi/Project]]
- [[20 Projects/Hibachi/Logs/2026-08-03 ElevenLabs TTS]]
- [[Vault Index]]
