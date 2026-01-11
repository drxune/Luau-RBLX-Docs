# EqualizerSoundEffect | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/EqualizerSoundEffect
Scraped: 2026-01-11T02:27:26.589599Z

## Inherits
- SoundEffect
- EqualizerSoundEffect
- Instance
- Object
- Sound
- SoundGroup
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [SoundEffect](/docs/reference/engine/classes/SoundEffect)
6. /
7. [EqualizerSoundEffect](/docs/reference/engine/classes/EqualizerSoundEffect)

English

Feedback

Engine Class

![EqualizerSoundEffect](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/EqualizerSoundEffect-Dark.webp)EqualizerSoundEffect

Controls the volume of incoming audio across three frequency ranges.

---

Summary

Properties

|  |
| --- |
| [HighGain](#HighGain):[number](/docs/luau/numbers) |
| [LowGain](#LowGain):[number](/docs/luau/numbers) |
| [MidGain](#MidGain):[number](/docs/luau/numbers) |

Inherited Members

2 inherited from [SoundEffect](/docs/reference/engine/classes/SoundEffect)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An equalizer allows for control of the volume of various frequency ranges for
the [Sound](/docs/reference/engine/classes/Sound) or [SoundGroup](/docs/reference/engine/classes/SoundGroup) the effect is parented to. This can be
used to highlight particular elements of audio or minimize or outright
eliminate others. The [EqualizerSoundEffect](/docs/reference/engine/classes/EqualizerSoundEffect) gives control over three
ranges of frequency: Low, Mid, and High. Their specific frequencies are as
follows:

* Low: 0 - 400 Hz
* Mid: 400 - 4000 Hz
* High: 4000+ Hz

---

API Reference

Properties

HighGain

Read Parallel

The output volume of frequencies greater than 4000 Hz.

EqualizerSoundEffect.HighGain:[number](/docs/luau/numbers)

Range: -80 to 10 (default 0) The output volume of frequencies greater than
4000 Hz. Measured in dB.

Provide feedback

---

LowGain

Read Parallel

The output volume of frequencies lower than 400 Hz.

EqualizerSoundEffect.LowGain:[number](/docs/luau/numbers)

Range: -80 to 10 (default 0) The output volume of frequencies lower than
400 Hz. Measured in dB.

Provide feedback

---

MidGain

Read Parallel

The output volume of frequencies between 400 and 4000 Hz.

EqualizerSoundEffect.MidGain:[number](/docs/luau/numbers)

Range: -80 to 10 (default 0) The output volume of frequencies between 400
and 4000 Hz. Measured in dB.

Provide feedback

---