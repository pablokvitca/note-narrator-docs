---
title: Performance Settings
description: Settings for playback start, parallel generation, background jobs, speed, skip amounts and panel controls.
tags:
  - note-narrator
  - settings
  - performance
publish: true
permalink: settings/performance
plugin-version: 0.16.1
updated: 2026-09-26
---

# Performance Settings

Despite the name, this group holds most playback and panel behaviour.

> [!todo] Screenshot needed: `settings-performance.png`
> The Performance group, possibly two shots because it is long.

## Starting and generating

| Setting | Default | Shown when | What it does |
| --- | --- | --- | --- |
| **Start playback immediately** | On | Always | Plays as soon as the first chunk is ready, instead of waiting for the whole note |
| **Quick start** | On | Start immediately on | Makes the first chunk artificially short (including the title and properties preamble) so playback starts sooner |
| **Quick start unit** | Words | Quick start on | Size the first chunk in **Words** or **Characters** |
| **Quick start word count** | 150 | Unit is Words | Target size in words. Recommended 50 to 300. Has a reset button |
| **Quick start character count** | 750 | Unit is Characters | Slider 100 to 2000, step 50 |
| **Generate chunks in parallel** | On | Always | Generate more than one chunk ahead of playback |
| **Max parallel chunk generation** | 2 | Parallel on | Chunks generating at once (minimum 2). Recommended 2 to 5. Higher is faster but hits rate limits sooner |
| **Max parallel background chunk generation** | 1 | Always | Same, for notes in the background. Kept low so it does not compete with what you are hearing. Recommended 1 to 3 |
| **Background job display** | Minimal card | Always | **Minimal card**, **Compact row** or **Full callout**. See [[Background Generation]] |

## Reading and playback

| Setting | Default | What it does |
| --- | --- | --- |
| **Read selection instead of whole note** | On | With a text selection active, reads only the selection |
| **Default playback speed** | 1x | Starting speed for each read. Slider 0.5x to 3x, step 0.05. The panel slider adjusts live without changing it |
| **Rewind seconds** | 15s | Dropdown: 5, 10, 15, 20, 25, 30, 45 or 60 |
| **Skip forward seconds** | 15s | Same options, set independently |

## Panel appearance

| Setting | Default | What it does |
| --- | --- | --- |
| **Compact buttons** | Off | Play Saved, Read, Cancel and Background become icon-only with tooltips, at every panel size |
| **Show volume slider in panel** | On | Shows the volume slider and mute button |
| **Show playback speed slider in panel** | On | Shows the speed slider |
| **Time display** | Show current part times | What the time readout means, see below |

### Time display

| Option | Shows |
| --- | --- |
| **Show full times** | Totals across the whole read. Ungenerated parts appear as "+N parts" |
| **Show current part times** | Only the playing chunk's times |
| **Show full times + current part times** | Full totals with the current part's times in parentheses |

> [!warning] Rate limits and parallelism
> If you raise **Max parallel chunk generation** and see rate limit notices, lower it again. The read falls back to one chunk at a time after a 429 anyway. See [[Long Notes and Chunking]].
