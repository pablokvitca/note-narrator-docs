---
title: Note Narrator
description: Note Narrator reads your Obsidian notes aloud with ElevenLabs text to speech. Documentation, setup, settings reference and roadmap.
tags:
  - note-narrator
  - docs
aliases:
  - Home
  - Note Narrator docs
publish: true
permalink: /
plugin-version: 0.16.1
updated: 2026-09-26
---

# Note Narrator

Note Narrator is an Obsidian plugin that **reads your notes aloud** using text to speech. It ships with [ElevenLabs](https://elevenlabs.io) as its voice provider, plays audio while it is still being generated, and can save the result as an `.mp3` linked from the note.

> [!tip] New here?
> Start with [[Installation]], then follow the [[Quick Start]]. You will be listening to a note in a few minutes.

> [!todo] Screenshot needed: `hero-panel-and-note.png`
> A note open in Editing view with the Note Narrator panel in the right sidebar, mid-playback, with the highlight margin marker visible.

## What it does

- Reads the whole note, or just your selection, with a voice from your ElevenLabs account.
- Starts playing after the first short chunk is ready, and keeps generating the rest while you listen. See [[Long Notes and Chunking]].
- Saves audio to your vault and tracks whether it is still up to date. See [[Saving Audio]].
- Highlights what is being read and scrolls the note to it. See [[Highlighting and Scrolling]].
- Keeps generating other notes in the background. See [[Background Generation]].

## Documentation map

### Getting started
- [[Installation]]: BRAT, manual install, requirements
- [[Quick Start]]: from install to your first read
- [[Setting Up ElevenLabs]]: API key, voices and models

### Using Note Narrator
- [[The Panel]]: every part of the sidebar panel
- [[Reading a Note]]: what gets read and how to start
- [[Playback Controls]]
- [[Long Notes and Chunking]]
- [[Saving Audio]]
- [[Highlighting and Scrolling]]
- [[Background Generation]]
- [[Commands]]

### Settings
- [[Settings Overview]] links to one page per settings group:
  [[ElevenLabs Settings]], [[Panel Voices Settings]], [[Reading Settings]], [[Highlighting Settings]], [[Performance Settings]], [[Save Audio Settings]]

### Reference
- [[Frontmatter Properties]]
- [[Known Limitations]]
- [[Privacy and Network Use]]
- [[Troubleshooting and FAQ]]

### Roadmap
- [[Roadmap]]: what is next and what is being considered

> [!info] About this documentation
> These docs describe version **0.16.1** (stable). Features that only exist in a beta are marked with a callout. Something wrong or missing? Open an issue on the [GitHub repository](https://github.com/pablokvitca/note-narrator).
