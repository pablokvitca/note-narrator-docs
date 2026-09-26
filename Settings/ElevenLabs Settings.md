---
title: ElevenLabs Settings
description: API key, voice, model, stability and similarity boost settings.
tags:
  - note-narrator
  - settings
  - elevenlabs
publish: true
permalink: settings/elevenlabs
plugin-version: 0.16.1
updated: 2026-09-26
---

# ElevenLabs Settings

> [!todo] Screenshot needed: `settings-elevenlabs.png`
> The ElevenLabs group with a voice selected and both sliders visible.

## API key

Stored in Obsidian's secret storage, not in the plugin's settings file. The setting remembers only the secret's name. See [[Setting Up ElevenLabs]].

## Voice

The default voice for new reads. Populated from your ElevenLabs account (first 100 voices). Use the refresh button after adding a key or creating voices. The panel's Voice dropdown can override it per read.

## Model

| Option | Character limit |
| --- | --- |
| Eleven v3 (research preview) | 5,000 |
| Eleven Multilingual v2 (default) | 10,000 |
| Eleven Flash v2.5 | 40,000 |

## Stability

Slider, 0 to 1, step 0.05, default **0.5**. Lower values sound more expressive and varied. Higher values sound steadier. On Eleven v3 it maps to ElevenLabs' Creative (low), Natural (middle) and Robust (high) presets.

## Similarity boost

Slider, 0 to 1, step 0.05, default **0.75**. How closely the output should match the original voice.

> [!tip] Tuning
> If a voice sounds inconsistent between chunks of a long note, try raising Stability. If it sounds flat, lower it a little.
