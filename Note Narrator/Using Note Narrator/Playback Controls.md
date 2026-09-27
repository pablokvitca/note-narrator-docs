---
title: Playback Controls
description: The transport controls, speed and volume sliders, and progress display in the Note Narrator panel.
tags:
  - note-narrator
  - usage
  - playback
publish: true
permalink: note-narrator/using/playback-controls
plugin-version: 0.17.1
updated: 2026-09-27
---

# Playback Controls

![[playback-controls-row.png]]

## Transport row

Left to right:

| Control | Action |
| --- | --- |
| **Previous part** | Jumps straight to the previous chunk |
| **Rewind** | Back by the configured seconds |
| **Pause / Resume** | Toggles playback |
| **Skip forward** | Ahead by the configured seconds |
| **Next part** | Jumps straight to the next chunk |
| **Stop** | Ends the read |
| **Scroll to current section** | Scrolls the note to the section playing now. Set apart from the others because it moves the editor, not the audio |

Previous and Next part move immediately without waiting for the current chunk to finish. They also work during **Play saved**, moving between the saved file's own parts (see [[Saving Audio]]).

The rewind and skip amounts are separate dropdowns (5 to 60 seconds). The icons show the chosen number. See [[Appearance Settings]].

> [!note] No scrubbing
> There is no scrub bar for jumping to an arbitrary time. Use parts and the relative rewind and skip.

## Speed and volume

- **Playback speed** slider from 0.5x to 3x. It changes the current and next reads live without changing your default (set that under [[General Settings]]).
- **Volume** slider with a mute button. Live and per session, not saved.

Either row can be hidden in [[Appearance Settings]] if you do not use it. On narrow panels each collapses to a small pill that opens a popover slider.

![[slider-compact-popover.png]]

## Progress

- Elapsed, total and remaining time. Remaining is divided by playback speed.
- "Part X of Y, Z% complete".
- The [[The Panel#The generation bar|generation bar]].

Total and remaining can undercount while later parts are still generating. With **Time display** set to a full mode, unfinished parts appear as "(+N parts)" instead of being silently left out.
