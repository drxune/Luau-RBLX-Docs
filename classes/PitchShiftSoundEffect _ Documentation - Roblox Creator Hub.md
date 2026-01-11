# PitchShiftSoundEffect | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/PitchShiftSoundEffect
Scraped: 2026-01-11T02:27:16.247986Z

## Inherits
- SoundEffect
- PitchShiftSoundEffect
- Instance
- Object
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [SoundEffect](/docs/reference/engine/classes/SoundEffect)
6. /
7. [PitchShiftSoundEffect](/docs/reference/engine/classes/PitchShiftSoundEffect)

English

Feedback

Engine Class

![PitchShiftSoundEffect](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/PitchShiftSoundEffect-Dark.webp)PitchShiftSoundEffect

Adjusts the pitch of a sound without changing its playback speed.

---

Summary

Properties

|  |
| --- |
| [Octave](#Octave):[number](/docs/luau/numbers) |

Inherited Members

2 inherited from [SoundEffect](/docs/reference/engine/classes/SoundEffect)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The PitchShiftSoundEffect raises or lowers the pitch of the associated Sound
or SoundGroup without changing the playback speed of the audio. This effect
can be computationally expensive.

---

API Reference

Properties

Octave

Read Parallel

The percentage to shift the original pitch.

PitchShiftSoundEffect.Octave:[number](/docs/luau/numbers)

Range: 0.5 to 2 (default 1.25) The percentage to shift the original pitch.
Setting this to its minimum (0.5) lowers the octave by 1, setting this to
its maximum (2) increases the octave by 1.

Provide feedback

---