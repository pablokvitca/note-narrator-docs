---
title: Performance Settings
description: Settings for how quickly playback starts, including quick start.
tags:
  - note-narrator
  - settings
  - performance
publish: true
permalink: note-narrator/settings/performance
plugin-version: 0.17.0
updated: 2026-09-26
---

# Performance Settings

The **Performance** tab controls how quickly playback starts.

> [!info] Parallel generation moved
> How many chunks generate at once is now set **per provider**, because rate limits belong to the account. See [[Providers Settings#Generation|the provider's Generation group]].

![[settings-performance.png]]

| Setting | Default | Greyed out when | What it does |
| --- | --- | --- | --- |
| **Start playback immediately** | Enabled | never | Plays as soon as the first chunk is ready, instead of waiting for the whole note |
| **Quick start** | Enabled | Start immediately is off | Makes the first chunk artificially short (including the title and properties preamble) so playback starts sooner |
| **Quick start unit** | Words | Start immediately or Quick start is off | Size the first chunk in **Words** or **Characters** |
| **Quick start word count** | 150 | Unit is not Words, or the settings above are off | Target size in words. Recommended 50 to 300. Has a reset button |
| **Quick start character count** | 750 | Unit is not Characters, or the settings above are off | Slider 100 to 2000, step 50 |

> [!tip] Long notes
> Quick start matters most on long notes: the first sentence or two are generated alone, and the rest generates while you listen. See [[Long Notes and Chunking]].
