---
title: Privacy and Network Use
description: What data Note Narrator sends over the network, to whom, and what it stores.
tags:
  - note-narrator
  - reference
  - privacy
publish: true
permalink: reference/privacy
plugin-version: 0.17.0
updated: 2026-09-26
---

# Privacy and Network Use

Note Narrator does not collect telemetry or analytics, and it never runs remote code.

## What is sent, and when

> [!important] One external service
> Note Narrator talks only to **ElevenLabs** (`api.elevenlabs.io`), and only when you trigger a read, regenerate, or (if enabled) auto-generate on open, or when you load your voice list.

| Request | Data sent |
| --- | --- |
| Generate speech | The text being read (after Markdown cleanup), the narrator profile's voice, model and voice settings, and the provider's API key |
| List voices | The provider's API key, to fetch that account's voices (when you open a profile's page or press refresh) |

The text of a note leaves your device when you read it. If a note is sensitive, do not read it with this plugin. ElevenLabs' own terms and privacy policy apply to what they receive.

## What is stored

- **API keys:** in Obsidian's secret storage, not in the vault or plugin settings. Only the name of each provider's secret is saved.
- **Settings:** in the plugin's `data.json`.
- **Audio and tracking data:** `.mp3` files in your vault and frontmatter properties on notes. See [[Frontmatter Properties]].

Nothing is sent to the plugin author.

> [!tip] Keep audio out of sync targets
> If your vault syncs, saved `.mp3` files sync with it and can be large. Choose a folder you can exclude from sync under **Save location**. Saving outside the vault is planned. See [[Roadmap]].

## ElevenLabs terms that apply to you

Note Narrator only sends requests to ElevenLabs on your behalf. Your ElevenLabs account and the audio it produces are covered by ElevenLabs' own terms:

- **Who can use it:** ElevenLabs' [Terms of Service](https://elevenlabs.io/terms-of-use) say you must be 18 or over (or of legal age where you live) to use its services.
- **What you may do with the audio:** the terms allow free accounts to use the service for non-commercial purposes only, and paid plans for commercial purposes. Check your plan before using saved audio commercially.
- **What you may read:** you need the rights to any text you send, and your use must follow ElevenLabs' [Prohibited Use Policy](https://elevenlabs.io/use-policy).
- **AI-generated audio:** if you share it, consider saying it is AI-generated.
- **Your API key:** it is yours alone. Do not share it or use it to resell access.

> [!note] Not legal advice
> These are summaries, and ElevenLabs can change its terms. The terms on their site are the ones that count.

