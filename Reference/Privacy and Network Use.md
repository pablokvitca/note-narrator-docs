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
