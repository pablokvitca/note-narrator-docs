---
title: Background Generation
description: Keep generating a note's audio in the background while you read or work on something else.
tags:
  - note-narrator
  - usage
  - background
publish: true
permalink: note-narrator/using/background-generation
plugin-version: 1.0.0
updated: 2026-09-27
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

## Starting another note while one is still generating

With **Keep generating when starting another note** on (Performance tab, enabled by default), pressing **Read** or **Play saved** on a *different* note while one is still generating automatically moves the note that was generating to the background first -- the same as clicking **Background** yourself -- instead of discarding its progress. It then starts the new note as usual.

This only applies when the note you're switching to is genuinely different. Reading the same note again (or one that already has a background job) adopts that job instead, as it always did.

Turn the setting off in [[Performance Settings]] to go back to the old behaviour, where starting another note discards whatever was generating.

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
> Generating directly in the background without starting a read first is on the [[Roadmap]].
