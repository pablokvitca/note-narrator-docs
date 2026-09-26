---
title: Save Audio Settings
description: Settings for saving audio files, linking them in note frontmatter, staleness tracking, regeneration and cleanup.
tags:
  - note-narrator
  - settings
  - saved-audio
publish: true
permalink: settings/save-audio
plugin-version: 0.16.1
updated: 2026-09-26
---

# Save Audio Settings

Most of these appear only after you turn on the settings above them. Concepts are explained in [[Saving Audio]].

> [!todo] Screenshot needed: `settings-save-audio.png`
> The Save audio group fully expanded (saving and linking both on).

| Setting | Default | Shown when | What it does |
| --- | --- | --- | --- |
| **Save generated audio to a file** | Off | Always | Saves each read as an `.mp3` in the vault |
| **Save location** | Same folder as the note | Saving on | Same folder as the note, or a custom folder |
| **Custom folder path** | `Note Narrator Audio` | Custom folder | Vault-relative folder, created if missing. Empty falls back to the default |
| **Link saved audio in the note** | Off | Saving on | Writes the link and tracking data to frontmatter and enables up to date / outdated tracking |
| **Link property** | `note_narrator_audio` | Linking on | Property holding the link to the audio |
| **Hash property** | `note_narrator_audio_hash` | Linking on | Content hash used to detect staleness |
| **Path property** | `note_narrator_audio_path` | Linking on | Raw vault path, used internally to find the file |
| **Timestamp property** | `note_narrator_audio_timestamp` | Linking on | When the audio was generated |
| **Voice property** | `note_narrator_audio_voice` | Linking on | Voice ID used. Detects a voice change |
| **Chunk durations property** | `note_narrator_audio_chunk_durations` | Linking on | Each chunk's `[duration, byte length]`, used to slice the file into parts |
| **Extra properties to exclude from staleness hashing** | empty | Linking on | One property key per line. Ignored when checking whether the note changed |
| **On regenerate** | Replace existing file | Linking on | **Replace existing file** or **Keep old versions** |
| **Auto-generate on open** | Off | Linking on | Silently regenerates missing or outdated audio when a note opens |
| **Show "clear Note Narrator files" menu item and delete button** | On | Linking on | Enables the panel menu item and the status-line delete button |
| **Auto-clean up properties when saved file is missing** | On | Linking on | Removes stale properties if the linked file no longer exists |

> [!tip] Change the property names if you like
> Every property name is editable, so you can match an existing vault convention. An empty entry falls back to the default. Existing notes keep their old property names until regenerated, so change these before you build up saved audio.

> [!danger] Auto-generate on open spends credits
> It makes ElevenLabs requests every time you open a note that is missing audio or outdated. Leave it off for notes you edit constantly.

> [!warning] Deleting is permanent for properties
> Clearing moves the file to trash per your vault setting, but the properties are removed with no undo.
