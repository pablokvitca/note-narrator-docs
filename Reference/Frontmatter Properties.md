---
title: Frontmatter Properties
description: The frontmatter properties Note Narrator writes to notes with saved audio and what each is for.
tags:
  - note-narrator
  - reference
  - saved-audio
publish: true
permalink: reference/frontmatter-properties
plugin-version: 0.16.1
updated: 2026-09-26
---

# Frontmatter Properties

When **Link saved audio in the note** is on, Note Narrator writes six properties to the note. All names are configurable in [[Save Audio Settings]]. These are the defaults.

| Property | Contains |
| --- | --- |
| `note_narrator_audio` | A wikilink to the saved `.mp3`, so Obsidian shows and tracks it |
| `note_narrator_audio_hash` | Hash of the note's content when the audio was made, used for [[Saving Audio#Linking and staleness\|staleness]] |
| `note_narrator_audio_path` | Raw vault path of the file, used internally |
| `note_narrator_audio_timestamp` | When the audio was generated |
| `note_narrator_audio_voice` | ElevenLabs voice ID used |
| `note_narrator_audio_chunk_durations` | A list of `[duration in seconds, byte length]` pairs, one per chunk |

## Example

```yaml
---
note_narrator_audio: "[[My Note (Rachel).mp3]]"
note_narrator_audio_hash: 4ac88baf
note_narrator_audio_path: Notes/My Note (Rachel).mp3
note_narrator_audio_timestamp: 2026-09-12T16:24:48.902-04:00
note_narrator_audio_voice: 21m00Tcm4TlvDq8ikWAM
note_narrator_audio_chunk_durations:
  - - 33.11
    - 530852
  - - 9.06
    - 145911
---
```

> [!note] They are excluded from the hash
> Note Narrator's own six properties never count as an edit, so writing them does not make the audio look outdated.

> [!info] Editing by hand
> Do not edit these by hand. Removing them detaches the note from its audio. Use **Clear Note Narrator files** to do it properly.

> [!tip] Hiding them
> The properties show in Obsidian's Properties view. A setting to hide them is on the [[Roadmap]].
