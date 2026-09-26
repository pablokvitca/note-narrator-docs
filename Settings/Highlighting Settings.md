---
title: Highlighting Settings
description: Settings for the follow-along highlight and the scroll to current section button.
tags:
  - note-narrator
  - settings
  - highlighting
publish: true
permalink: settings/highlighting
plugin-version: 0.16.1
updated: 2026-09-26
---

# Highlighting Settings

> [!todo] Screenshot needed: `settings-highlighting.png`
> The Highlighting group with **Highlight while reading** on so all dependent settings show.

| Setting | Default | Shown when | What it does |
| --- | --- | --- | --- |
| **Highlight while reading** | Off | Always | Marks the playing text in the editor. Needs Editing view |
| **Highlight granularity** | Chunk | Highlighting on | **Chunk** moves per audio request. **Section** moves least often (Markdown-aware chunker) |
| **Only highlight the section heading** | Off | Highlighting on and Section granularity | Highlights just the heading line |
| **Highlight style** | Margin marker | Highlighting on | **Margin marker**, **Background wash**, or **Underline** |
| **Scroll-to-current button** | On | Always | Adds the **Scroll to current section** button to the playback controls. Works with highlighting off |

See [[Highlighting and Scrolling]] for how it looks and its limits.

> [!info] Sentence and word granularity
> Not offered yet. See [[Roadmap]].
