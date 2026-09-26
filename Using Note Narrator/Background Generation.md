---
title: Background Generation
description: Keep generating a note's audio in the background while you read or work on something else.
tags:
  - note-narrator
  - usage
  - background
publish: true
permalink: using/background-generation
plugin-version: 0.17.0
updated: 2026-09-26
---

# Background Generation

If you want a note to finish generating without listening to it now, send it to the background.

## How it works

1. Start a read (or have one generating).
2. Click **Background** in the panel.
3. The note keeps generating on its own, separate from what you play.
4. It appears in the panel's **background jobs** list as queued, generating or done. You get a notice when one finishes.
5. Click a job to play it. Use its small button to discard it (or remove it when done).

![[background-jobs-list.png]]

## Separate concurrency

Background work has its own parallelism, **Max parallel background chunk generation** (default 1), set on the provider the note's narrator uses. It is low on purpose so it does not compete with a read you are actively listening to. See [[Providers Settings]].

## Display style

**Background job display** (in [[Appearance Settings]]) chooses how jobs look:

| Style | Look |
| --- | --- |
| **Minimal card** (default) | A small card with icon buttons |
| **Compact row** | A slim row with icon buttons |
| **Full callout** | A callout with text buttons per note |

All three play the note when you click anywhere on them except the buttons.

> [!info] Planned improvements
> Generating directly in the background without starting a read first, and automatically moving the current read to the background when you start another, are on the [[Roadmap]].
