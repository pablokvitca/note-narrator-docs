---
title: General Settings
description: The General tab holds the default reading settings that narrator profiles can override, plus the default playback speed.
tags:
  - note-narrator
  - settings
  - reading
publish: true
permalink: note-narrator/settings/general
plugin-version: 0.17.0
updated: 2026-09-26
---

# General Settings

The **General** tab has the default configuration. Everything under **Reading** here can be overridden per narrator profile. See [[Profiles Settings#Reading overrides|reading overrides]].

![[settings-general.png]]

![[settings-general-comments-off.png]]

With **Skip Markdown comments** off, the two comment options below it are greyed out.

## Reading

| Setting | Default | Greyed out when | What it does |
| --- | --- | --- | --- |
| **Read selection instead of whole note** | On | never | With a text selection active, reads only the selection |
| **Read note title** | On | never | Speaks the note's title before its content |
| **Read note properties** | Off | never | Speaks "properties", each key and value, then "content", before the body. Not used for a selection |
| **Skip Markdown comments** | On | never | Strips Obsidian comments (`%% like this %%`) before reading |
| **Don't read comment delimiter symbols** | On | Skip Markdown comments is on | Never reads the raw `%%` markup aloud, only the text between |
| **Announce comments as "Comment: ..."** | On | Skip Markdown comments is on | Prefixes a comment's text with "Comment:" |
| **Text chunker** | Markdown-aware | never | Markdown-aware or Sentence-only |
| **Max heading depth for sections** | 2 | Chunker is not Markdown-aware | Slider 1 to 6. Headings at or shallower than this start a new section |
| **Skip sections by heading** | empty | Chunker is not Markdown-aware | One regex per line. Matching sections are skipped entirely |

> [!example] Skip patterns
> ```
> Changelog
> Notes to self
> ^Draft
> ```
> Any section headed "Changelog", "Notes to self", or starting with "Draft" is never read.

> [!bug] HTML comments
> `<!-- HTML comments -->` are not handled by any of these settings and are read as literal text. See [[Known Limitations]].

## Playback

| Setting | Default | What it does |
| --- | --- | --- |
| **Default playback speed** | 1x | Starting speed for each read. Slider 0.5x to 3x, step 0.05. The panel slider adjusts live without changing it |

Read more in [[Reading a Note]] and [[Long Notes and Chunking]].
