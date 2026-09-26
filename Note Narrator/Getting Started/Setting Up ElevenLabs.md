---
title: Setting Up ElevenLabs
description: Create an ElevenLabs API key, store it safely in Obsidian, and choose a voice and model in a narrator profile.
tags:
  - note-narrator
  - getting-started
  - elevenlabs
publish: true
permalink: note-narrator/getting-started/setting-up-elevenlabs
plugin-version: 0.17.0
updated: 2026-09-26
---

# Setting Up ElevenLabs

Note Narrator generates speech with ElevenLabs, so you need an account with an API key.

## API key

1. Sign in at [elevenlabs.io](https://elevenlabs.io) and create an API key in your account settings.
2. In Obsidian, open **Settings, Note Narrator, Providers** and open (or add) an ElevenLabs provider.
3. Under **API key**, pick an existing secret or create a new one and paste the key.

Adding a provider with **+** also creates a narrator profile called **Default (provider name)** for it, so you can pick a voice and read straight away.

> [!tip] Two accounts?
> Add a second ElevenLabs provider with its own key (for example personal and work), then point different narrator profiles at each. See [[Providers Settings]].

> [!info] Where the key lives
> The key is stored with Obsidian's built-in [secret storage](https://docs.obsidian.md/plugins/guides/secret-storage), not in the plugin's `data.json`. The plugin only remembers the **name** of the secret to look up (`elevenlabs-api-key` by default), so the key never appears in your vault files or your synced settings, and other plugins can share the same secret.

> [!info] Your plan's terms apply
> Free ElevenLabs accounts may use the service for non-commercial purposes only. See [[Privacy and Network Use]] for the terms that apply to you.

## Voices

A narrator profile's **Voice** dropdown lists voices from its provider's account, **the first 100**. Use the refresh button after adding a key or creating a voice. To keep the panel tidy, turn off **Show in panel dropdown** for profiles you rarely use. See [[Profiles Settings]].

## Models

| Model | Character limit per request | Notes |
| --- | --- | --- |
| **Eleven Multilingual v2** (default) | 10,000 | Balanced quality and cost, many languages |
| **Eleven Flash v2.5** | 40,000 | Fastest and cheapest, fewer characters per request |
| **Eleven v3** (research preview) | 5,000 | Most expressive, but ElevenLabs labels it a research preview |

> [!caution] Eleven v3 is a research preview
> ElevenLabs notes v3 can be more prone to mispronunciations or invented words than Multilingual v2, and Professional Voice Clones are not fully optimized for it yet.

The character limit is the size of one request. Longer notes are split into several chunks automatically. See [[Long Notes and Chunking]].

## Voice tuning

**Stability** and **Similarity boost** are set per narrator profile and shape how the voice sounds. See [[Profiles Settings]] for what each does.

## Rate limits

If ElevenLabs answers with a rate limit (HTTP 429), Note Narrator retries automatically with exponential backoff (up to 8 retries, with the wait capped at 30 seconds) and switches to one chunk at a time for the rest of that read. Parallelism is set per provider. See [[Providers Settings]].
