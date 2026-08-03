---
type: project-log
project: Hibachi
date: 2026-08-03
status: recorded
sources:
  - kofiarhin/hibachi
  - kofiarhin/ideahub
  - kofiarhin/hibachi-vault
tags:
  - project/hibachi
  - progress
  - accomplishment
  - elevenlabs
  - voice
---

# Hibachi ElevenLabs TTS — 2026-08-03

## Summary

Hibachi now has an ElevenLabs text-to-speech implementation with server-side credential isolation, ephemeral streamed audio, playback status, cancellation, visualizer integration, and dedicated tests. The follow-up fix branch removes the old browser speech provider and adds logical-response deduplication to prevent duplicate ElevenLabs playback.

## Implemented

- Added ElevenLabs TTS to the application repository on `main` at commit `0b29390690a731383293cfeecf0f677953d8f826`.
- Kept the ElevenLabs API key inside the local companion service environment.
- Added authenticated localhost speech generation, request validation, error normalization, timeouts, cancellation, no-store responses, and streamed MP3 playback.
- Added real playback analyser levels for the Hibachi visualizer.
- Added voice configuration status, Test voice, Stop, and safe provider error presentation.
- Added server and client test coverage for the provider, local speech route, player, state, cancellation, and redaction boundaries.

## Sole-provider correction

- Branch: `fix/elevenlabs-sole-tts-provider`.
- Removed browser `SpeechSynthesis` and the browser fallback adapter.
- Removed browser provider and fallback settings.
- ElevenLabs is the only spoken-output provider on the fix branch.
- When ElevenLabs is unavailable, Hibachi remains usable in text-only mode.

## Duplicate-playback root cause

The same logical assistant response could arrive through two client data paths:

1. the live WebSocket `conversation.message` event;
2. the post-command conversation refresh used to support socket-less sessions.

Those copies could carry different message IDs. Exact-ID deduplication therefore allowed both copies to enter playback.

## Duplicate-playback fix

- Added normalized logical-response identity using conversation, workflow, action, and speech-ready text.
- Added a five-second bounded deduplication window.
- Applied deduplication during Redux message ingestion and before automatic speech begins.
- Kept exact message-ID tracking.
- Preserved legitimate repeated responses outside the bounded window.
- Preserved the single live speech adapter and operation-token cancellation safeguards.

## Verification recorded

Local Windows verification shown on 2026-08-03 passed:

- Client tests: 12 files, 131 tests.
- Server tests: 13 suites, 398 tests.
- Root typecheck.
- Lint.
- Production build.

The final TypeScript correction was limited to the speech-deduplication test input shape; logical deduplication intentionally ignores message IDs.

## Evidence boundaries

- Latest observed remote fix branch head during implementation: `a13d528477297a597fbbb12078902e50fc123479`.
- A final local test-only correction was applied after that observed head; its pushed commit SHA is not yet recorded here.
- `npm run test:e2e` is not yet recorded as passing on the final revision.
- `npm run verify:policies` is not yet recorded as passing on the final revision.
- Runtime browser evidence for exactly one `POST /api/v1/voice/speech` request per logical response is not yet recorded.
- The fix branch is not recorded as merged into application `main`.
- No deployment is recorded.

## Next actions

- Commit and push the final local test correction.
- Run E2E and policy verification against that exact commit.
- Confirm one network speech request and one playback per logical assistant response.
- Confirm new responses cancel existing playback, reload does not replay history, and offline behavior is text-only.
- Review and merge only after exact final evidence is retained.

## Related notes

- [[20 Projects/Hibachi/Project]]
- [[20 Projects/Hibachi/Tasks]]
- [[Vault Index]]
