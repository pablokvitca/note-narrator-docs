---
title: Supported Platforms
description: Which Obsidian platforms Note Narrator supports, and how well each one has been tested.
tags:
  - note-narrator
  - reference
  - platforms
publish: true
permalink: note-narrator/reference/supported-platforms
plugin-version: 0.17.0
updated: 2026-09-26
---

# Supported Platforms

Note Narrator is not desktop-only, so Obsidian will load it on every platform. That does not mean every platform has been tried. This page says which have.

## Support levels

Two things vary by platform: whether Note Narrator has been tried there, and which text to speech provider you can use with it.

| Testing level | Meaning |
| --- | --- |
| ✅ **Tested** | Used on a real device and works as expected |
| ❔ **Not tested** | Should work, since the plugin uses only Obsidian's cross-platform APIs, but nobody has tried it. Reports welcome |
| ⛔ **Unsupported** | Known not to work, or not meant to work |

| Provider level | Meaning |
| --- | --- |
| ✅ **Supported** | Available in the current version |
| 🔜 **Upcoming** | Planned, not available yet. See the [[Roadmap]] |
| ➖ **Not applicable** | The provider cannot exist on that platform |

## Platforms

| Platform | Testing | ElevenLabs | Google Gemini | Apple OS (Local) |
| --- | --- | --- | --- | --- |
| macOS | ✅ Tested | ✅ Supported | 🔜 Upcoming | 🔜 Upcoming |
| iPhone (iOS) | ✅ Tested | ✅ Supported | 🔜 Upcoming | 🔜 Upcoming |
| iPad (iPadOS) | ✅ Tested | ✅ Supported | 🔜 Upcoming | 🔜 Upcoming |
| iPad mini (iPadOS) | ✅ Tested | ✅ Supported | 🔜 Upcoming | 🔜 Upcoming |
| Apple Vision Pro (visionOS) | ✅ Tested | ✅ Supported | 🔜 Upcoming | 🔜 Upcoming |
| Windows | ❔ Not tested | ✅ Supported | 🔜 Upcoming | ➖ Not applicable |
| Linux | ❔ Not tested | ✅ Supported | 🔜 Upcoming | ➖ Not applicable |
| Android phone and tablet | ❔ Not tested | ✅ Supported | 🔜 Upcoming | ➖ Not applicable |

- **ElevenLabs** is the only provider in the current version. It needs an internet connection and an ElevenLabs account. See [[Setting Up ElevenLabs]].
- **Google Gemini** will be a second cloud provider.
- **Apple OS (Local)** will use the text to speech built into Apple's operating systems, with no network or account, so it only applies to Apple platforms.
- VisionOS runs the iPad version of Obsidian. There is no Obsidian web app, so a browser is not a supported platform.

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
