---
title: Publishing Guide
description: How this vault is written, synced with git, and published with Obsidian Publish.
tags:
  - meta
  - docs
publish: false
updated: 2026-09-26
---

# Publishing Guide

These docs are an Obsidian vault kept in git and published with **Obsidian Publish**.

## Conventions

- Every page has frontmatter: `title`, `description`, `tags`, `publish`, `permalink`, `plugin-version`, `updated`.
- `plugin-version` is the plugin version the page describes. Bump it when you review a page against a new release.
- `updated` is the date of the last content change.
- Callouts carry meaning: `[!tip]` advice, `[!note]` detail, `[!info]` context, `[!warning]` and `[!caution]` things that can bite, `[!danger]` credit spend or data loss, `[!bug]` known bugs, `[!todo]` screenshot placeholders, `[!example]` samples.
- Link with wikilinks, and use `[[Page|label]]` for custom text.

## Obsidian Publish setup

1. Open **Publish changes** and select the notes to publish. Everything with `publish: true` should be selected. Notes with `publish: false` (this folder) must stay unpublished.
2. `index.md` is the home page (`permalink: /`). Confirm it under Site options.
3. Each page has a `permalink` for a stable, readable URL. Keep them when renaming files so links do not break.
4. Use only features Publish supports: standard Markdown, wikilinks, callouts, tables, embeds of published files. Do not use Dataview or other community plugin syntax.

> [!warning] Placeholders and embeds
> A `![[missing.png]]` embed renders as a broken link on the published site. That is why unfinished screenshots are `[!todo]` callouts instead. Only add an embed once the image file exists in `Screenshots/`. Also select the image when publishing.

> [!caution] Before publishing
> Search the vault for `Screenshot needed`. Placeholders are visible to readers. Decide whether to ship them or hide the page until images are ready.

## Git sync

- Commit the vault as it is. `.obsidian/workspace.json` and other per-device state are git-ignored.
- The optional [Obsidian Git](https://github.com/Vinzent03/obsidian-git) plugin can auto-commit and push.
- The plugin's own code lives in a separate repository, `pablokvitca/note-narrator`.

## Keeping docs accurate

When a setting or behaviour changes in the plugin:

1. Update the matching [[Settings Overview]] page and the group page.
2. Update [[Known Limitations]] and the [[Roadmap]] if something shipped or was fixed.
3. Bump `plugin-version` and `updated` on touched pages.
