---
title: Roadmap
description: What Note Narrator has shipped recently, what is in progress, and what is planned or under consideration.
tags:
  - note-narrator
  - roadmap
publish: true
permalink: roadmap
plugin-version: 0.16.1
updated: 2026-09-26
---

# Roadmap

> [!warning] Not a promise
> This is direction, not a schedule. Ideas move between milestones, get reshaped, or get dropped. Version numbers show intended order, not dates.

## Recently shipped

- Background generation with a job list, click to play, and a separate concurrency limit
- Volume slider and mute, plus optional speed and volume rows
- Full-audio time display modes with "+N parts" for ungenerated chunks
- Highlight while reading (chunk and section granularity, three styles) and a scroll to current section button
- Skip sections by heading regex, and separate Markdown comment toggles
- Saved audio: up to date tracking, per-chunk parts for Previous/Next during Play Saved, auto-generate on open
- Mobile support: tested on iPhone, iPad, iPad mini and visionOS, with touch-sized controls
- Configurable rewind and skip amounts, compact buttons, and a panel voice shortlist

## In progress: 0.17

> [!info] In the beta
> **Saved state on the toolbar icon.** The note's toolbar icon switches to a waveform with a check badge when it has up-to-date saved audio, so you no longer need to open the panel to check. Available in the 0.17 beta through BRAT.

## Toward 1.0

The goal for 1.0 is a polished first public release.

| Item | Why |
| --- | --- |
| **Community plugin directory listing** | Install without BRAT |
| **Documentation and screenshots** | This site |
| **Reorganize settings panels** | The settings grew one feature at a time. Regroup and reorder them for someone seeing them fresh |
| **ElevenLabs credit usage and cost estimates** | Show remaining credits and an estimate before you read a long note |
| **Other TTS providers** | The provider layer is already an interface. Add more than ElevenLabs |
| **Local or offline voices** | OS text to speech or a local model. No key, no network, lower expressiveness |
| **Auto-caption images** | Use a vision model to give images a short spoken description instead of skipping them |

## After 1.0

### 1.1

| Item | Notes |
| --- | --- |
| **HTML comment skipping fix** | `<!-- -->` comments are currently read aloud. A previous attempt did not hold up |
| **"Do not read aloud" delimiters** | A start and end marker, for example `---(start do not read aloud)---`, to exclude any region regardless of chunker |
| **Hide Note Narrator properties** | A toggle to hide its frontmatter from the rendered Properties view (feasibility is being investigated) |
| **Read out backlinks** | An option to speak the notes that link to this one. Off by default |
| **Better per-chunk saving** | Proper MP3 re-muxing, or saving chunks separately with a manifest |

### 2.0

| Item | Notes |
| --- | --- |
| **Save audio outside the vault** | For example a folder synced by iCloud, Google Drive or OneDrive, so audio does not bloat vault sync |
| **Cloud storage** | Save to and stream from remote storage such as S3 |

## Under consideration

Not scheduled yet.

- **Move tracking data onto the audio file.** Today six properties live on every note. Storing the metadata with the audio file would keep notes clean.
- **Generate directly in the background.** Skip the "start a read, then move to background" step.
- **Auto-move the current read to the background** when you start another, instead of discarding it.
- **More content filters.** Toggles to skip code blocks, inline code, blockquotes, tags, tables, image embeds, emojis and other syntax.
- **Per-section and chapter bookmarks.**
- **Sentence and word level highlighting.** Needs word timing from the provider to stay in sync.

> [!question] Have an idea?
> Open an issue on the [GitHub repository](https://github.com/pablokvitca/note-narrator). See also [[Known Limitations]] for the gaps these items address.
