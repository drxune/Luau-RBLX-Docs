# AudioChannelLayout | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/AudioChannelLayout
Scraped: 2026-01-11T02:43:48.799360Z
1. [Enums](/docs/reference/engine/enums)
2. /
3. [AudioChannelLayout](/docs/reference/engine/enums/AudioChannelLayout)

English

Feedback

Engine Enum

AudioChannelLayout

---

The AudioChannelLayout enum describes the channel layout of an audio stream.
Audio streams contain one or more channels that are intended to be rendered
simultaneously with a particular arrangement of speakers. In general, more
channels impact performance but provide higher spatial quality.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Mono | 0 | Monaural audio streams contain only one Center channel. Diagram showing position of channels for Mono layout. |
| Stereo | 1 | Stereophonic audio streams consist of two channels: Left and Right. Diagram showing position of channels for Stereo layout. |
| Quad | 2 | Quadrophonic audio streams consist of four channels: Left, Right, BackLeft, and BackRight. Quadrophonic streams can encode forward/backward spatial information that stereo streams might struggle with. Diagram showing position of channels for Quad layout. |
| Surround\_5 | 3 | Surround sound audio streams consist of five channels: Left, Right, Center, BackLeft, and BackRight. Surround sound streams encode spatial information with better resolution front and center. Diagram showing position of channels for Surround 5 layout. |
| Surround\_5\_1 | 4 | 5.1 surround sound consists of six channels: Left, Right, Center, BackLeft, BackRight, and a Sub (subsonic) low‑frequency channel. 5.1 surround sound benefits from low frequencies being less directional in order to encode higher resolution spatial information versus simple 5‑channel surround sound. Diagram showing position of channels for Surround 5.1 layout. |
| Surround\_7\_1 | 5 | 7.1 surround sound consists of eight channels: Left, Right, Center, SurroundLeft, SurroundRight, BackLeft, BackRight, and a Sub (subsonic) low‑frequency channel. 7.1 surround sound is an improvement over 5.1 surround sound, offering better spatial resolution directly to the left and right as well. Diagram showing position of channels for Surround 7.1 layout. |
| Surround\_7\_1\_4 | 6 | 7.1.4 surround sound consists of twelve channels: Left, Right, Center, SurroundLeft, SurroundRight, BackLeft, BackRight, Sub, TopLeft, TopRight, TopBackLeft, and TopBackRight. 7.1.4 is the only currently supported channel layout that encodes height information. Diagram showing position of channels for Surround 7.1.4 layout. |