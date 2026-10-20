# Voice interface integration reference

Canonical fork: https://github.com/deqodegroup/voiceorbs
Agent entry: ../AGENTS.md

## Selected consumers
- TOP Lite / STORM: src/registry/orbe/particles-orb; ocean-blue and soft white, calm motion. Existing standalone project only. Main TOP is protected.
- DEQODE Studio: src/registry/orbe/glass-orb; monochrome styling.
- Other products: choose independently; keep data, knowledge and permissions separate.

## Agent workflow
1. Read the consuming project's AGENTS.md and run its current ICM preflight.
2. Reuse an existing checkout under C:\dev when present; inventory before cloning to prevent duplicates. This session has not accessed or modified C:\dev.
3. Read this fork's AGENTS.md and the selected component plus its imports. Copy only required source/hooks/styles, retain MIT notice, and record the source commit in the consumer. The upstream package is private; do not assume npm installation or a Git dependency is a supported component package.
4. Map the existing session to idle, connecting, listening, thinking, speaking, error and disabled. Drive speaking from actual playback events and amplitude, not a timer or microphone signal. Do not start a second microphone capture when the voice provider already owns one.
5. Keep the UI dependent on a provider-neutral state/audio adapter. Browser UI must not call unrestricted agent tools or contain provider secrets. Hermes/runtime access must use authenticated, authorised service boundaries.
6. Show visible status, mute/end/retry controls and text fallback. Preserve reduced-motion behaviour. Handle denied microphone permission, disconnection, interruption and playback completion.
7. Check React compatibility, imports, licence/provenance and consumer build before delivery. Test listening, actual output reactivity, interruption, error recovery, mobile and reduced motion. Validate Niuean pronunciation separately.

## Validation and deployment
Fork source-change checks: pnpm install --frozen-lockfile, pnpm lint, pnpm test, pnpm build. Review upstream CONTRIBUTING.md first. Documentation-only bootstrap requires reference/content review; it does not certify source tests or live voice functionality. Do not deploy the gallery or change consumer deployment settings merely to adopt a component.
