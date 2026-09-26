---
title: Settings Overview
description: Every Note Narrator setting, grouped as they appear in the settings tab, with defaults.
tags:
  - note-narrator
  - settings
publish: true
permalink: settings/overview
plugin-version: 0.16.1
updated: 2026-09-26
---

# Settings Overview

Open **Settings, Note Narrator**. Settings are organised in six groups, each with its own page here. Some settings only appear when a related setting is on, and the page for each group says so.

> [!todo] Screenshot needed: `settings-tab-overview.png`
> The whole settings tab scrolled to the top, showing group headings.

| Group | Page | About |
| --- | --- | --- |
| ElevenLabs | [[ElevenLabs Settings]] | API key, voice, model, voice tuning |
| Panel voices | [[Panel Voices Settings]] | Shortlist of voices for the panel |
| Reading | [[Reading Settings]] | What text is read, comments, chunking |
| Highlighting | [[Highlighting Settings]] | Follow-along highlight and scroll button |
| Performance | [[Performance Settings]] | Speed, generation, panel controls, time display |
| Save audio | [[Save Audio Settings]] | Saving, linking, staleness, cleanup |

## All defaults at a glance

| Setting | Default |
| --- | --- |
| API key secret name | `elevenlabs-api-key` |
| Voice | Rachel (`21m00Tcm4TlvDq8ikWAM`) |
| Model | Eleven Multilingual v2 |
| Stability / Similarity boost | 0.5 / 0.75 |
| Panel voices | None (show all) |
| Read note title / properties | On / Off |
| Skip Markdown comments | On |
| Text chunker / Max heading depth | Markdown-aware / 2 |
| Highlight while reading | Off |
| Highlight granularity / style | Chunk / Margin marker |
| Scroll-to-current button | On |
| Start playback immediately / Quick start | On / On |
| Quick start size | 150 words (750 characters) |
| Generate in parallel / Max parallel | On / 2 |
| Max parallel in background | 1 |
| Background job display | Minimal card |
| Read selection instead of whole note | On |
| Default playback speed | 1x |
| Rewind / Skip forward | 15s / 15s |
| Compact buttons | Off |
| Show volume / speed slider | On / On |
| Time display | Current part |
| Save audio / Link in note | Off / Off |
| Save location | Same folder as the note |
| Custom folder path | `Note Narrator Audio` |
| On regenerate | Replace existing file |
| Auto-generate on open | Off |
| Show clear files button | On |
| Auto-clean missing files | On |

> [!note] Settings are per vault
> Settings live in the vault's plugin `data.json`. Your API key does not: it is in Obsidian's secret storage. See [[Setting Up ElevenLabs]].
