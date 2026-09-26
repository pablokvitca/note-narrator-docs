---
title: Reading Settings
description: Settings that control what text is read: titles, properties, comments, the chunker and section skipping.
tags:
  - note-narrator
  - settings
  - reading
publish: true
permalink: settings/reading
plugin-version: 0.16.1
updated: 2026-09-26
---

# Reading Settings

> [!todo] Screenshot needed: `settings-reading.png`
> The Reading group. Take a second one with **Skip Markdown comments** off to show the extra comment toggles.

| Setting | Default | What it does |
| --- | --- | --- |
| **Read note title** | On | Speaks the note's title before its content |
| **Read note properties** | Off | Speaks "properties", each key and value, then "content", before the body. Not used when reading a selection |
| **Skip Markdown comments** | On | Strips Obsidian comments (`%% like this %%`) before reading |
| **Don't read comment delimiter symbols** | On | Shown only when comment skipping is **off**. Never reads the raw `%%` markup aloud, only the text between |
| **Announce comments as "Comment: ..."** | On | Shown only when comment skipping is **off**. Prefixes the comment text with "Comment:" so a listener knows what it was |
| **Text chunker** | Markdown-aware | How the note is split into requests: Markdown-aware or Sentence-only |
| **Max heading depth for sections** | 2 | Markdown-aware only. Slider 1 to 6. Headings at or shallower than this start a new section |
| **Skip sections by heading** | empty | Markdown-aware only. One regex per line. Sections whose heading matches are skipped entirely |

> [!example] Skip patterns
> ```
> Changelog
> Notes to self
> ^Draft
> ```
> Any section headed "Changelog", "Notes to self", or starting with "Draft" is never read.

> [!bug] HTML comments
> `<!-- HTML comments -->` are not handled by any of these settings and are read as literal text. See [[Known Limitations]].

Read more in [[Reading a Note]] and [[Long Notes and Chunking]].
