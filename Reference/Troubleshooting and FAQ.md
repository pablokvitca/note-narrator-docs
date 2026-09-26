---
title: Troubleshooting and FAQ
description: Answers to common problems and questions about Note Narrator.
tags:
  - note-narrator
  - reference
  - faq
publish: true
permalink: reference/troubleshooting
plugin-version: 0.16.1
updated: 2026-09-26
---

# Troubleshooting and FAQ

## Nothing happens when I click the icon

The icons only open the panel. Click **Read** in the panel, or run **Read note aloud**. See [[Reading a Note]].

## "Set an ElevenLabs API key in the Note Narrator settings."

You have not chosen an API key secret yet. See [[Setting Up ElevenLabs]].

## The voice dropdown is empty

Set an API key, then press the refresh button next to **Voice**. If you set a shortlist, only those voices show in the panel. See [[Panel Voices Settings]].

## "ElevenLabs rate limit hit"

You are making requests faster than your plan allows. Note Narrator retries and switches to one chunk at a time. To avoid it, lower **Max parallel chunk generation** and **Max parallel background chunk generation**. See [[Performance Settings]].

## Highlighting does not show

Highlighting needs the note open in **Editing view**, and **Highlight while reading** turned on. It does not work in Reading view or for selection reads. See [[Highlighting and Scrolling]].

## It says "Saved audio is outdated" but I only changed a little

Any change to the note, anywhere, marks audio outdated. Exclude noisy properties with **Extra properties to exclude from staleness hashing**. See [[Saving Audio]].

## Previous and Next part do not work during Play Saved

Either the note is outdated, or a chunk-affecting setting changed since the audio was made, so the file plays as one piece. Regenerate. See [[Known Limitations]].

## "Cleaned up stale Note Narrator audio file metadata properties"

A note linked to an audio file that no longer exists, so the leftover properties were removed. Turn this off with **Auto-clean up properties when saved file is missing**.

## It reads symbols like `<!--`

HTML comments are read as text. See [[Known Limitations]].

## FAQ

**Does it work offline?** Not yet. It needs ElevenLabs. Local voices are planned. See [[Roadmap]].

**Does it work on mobile?** Yes. It has been tested on iPhone, iPad, iPad mini and visionOS.

**How much does it cost?** The plugin is free. ElevenLabs charges credits for generated audio. Saved audio replays for free.

**Can I use other voice providers?** Not yet. The provider layer is designed for it. See [[Roadmap]].

**Can I rename the audio properties?** Yes, in [[Save Audio Settings]].
