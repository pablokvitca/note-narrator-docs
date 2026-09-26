---
title: Supported Platforms
description: Which Obsidian platforms Note Narrator supports, and how well each one has been tested.
tags:
  - note-narrator
  - reference
  - platforms
publish: true
permalink: reference/supported-platforms
plugin-version: 0.17.0
updated: 2026-09-26
---

# Supported Platforms

Note Narrator is not desktop-only, so Obsidian will load it on every platform. That does not mean every platform has been tried. This page says which have.

## Support levels

| Level | Meaning |
| --- | --- |
| ✅ **Tested** | Used on a real device and works as expected |
| ❔ **Not tested** | Should work, since the plugin uses only Obsidian's cross-platform APIs, but nobody has tried it. Reports welcome |
| ⛔ **Unsupported** | Known not to work, or not meant to work |

## Platforms

| Platform | Support | Notes |
| --- | --- | --- |
| macOS | ✅ Tested | Where the plugin is developed |
| Windows | ❔ Not tested | |
| Linux | ❔ Not tested | |
| iPhone (iOS) | ✅ Tested | Touch-sized controls. See the iOS note below |
| iPad and iPad mini (iPadOS) | ✅ Tested | |
| Apple Vision Pro (visionOS) | ✅ Tested | Runs the iPad version of Obsidian |
| Android phone and tablet | ❔ Not tested | |
| Obsidian on the web or other platforms | ⛔ Unsupported | There is no Obsidian web app; anything else is untested |

> [!info] iOS below 16.4
> Regular expression lookbehind is not available on iOS and iPadOS before 16.4. Note Narrator itself does not use lookbehind, but a lookbehind pattern you type in **Skip sections by heading** may be ignored there. See [[General Settings]].

## Obsidian versions

| Obsidian version | Support |
| --- | --- |
| 1.13.1 and newer | ✅ Tested |
| 1.13.0 and older | ⛔ Unsupported. The settings screen needs APIs added in 1.13.1 |

> [!tip] Help fill in the gaps
> If you use Note Narrator on a platform marked **Not tested**, tell us whether it works by opening an issue on the [GitHub repository](https://github.com/pablokvitca/note-narrator). Include your platform and Obsidian version.

See also [[Installation]], [[Known Limitations]] and [[Troubleshooting and FAQ]].
