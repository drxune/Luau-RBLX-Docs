# TremoloSoundEffect | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TremoloSoundEffect
Scraped: 2026-01-11T02:36:27.004341Z

## Inherits
- SoundEffect
- TremoloSoundEffect
- Instance
- Object
- SoundEffects
- Sound
- SoundGroup
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [SoundEffect](/docs/reference/engine/classes/SoundEffect)
6. /
7. [TremoloSoundEffect](/docs/reference/engine/classes/TremoloSoundEffect)

English

Feedback

Engine Class

![TremoloSoundEffect](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/TremoloSoundEffect-Dark.webp)TremoloSoundEffect

Creates a trembling effect on a sound by varying the volume of the sound up
and down.

---

Summary

Properties

|  |
| --- |
| [Depth](#Depth):[number](/docs/luau/numbers) |
| [Duty](#Duty):[number](/docs/luau/numbers) |
| [Frequency](#Frequency):[number](/docs/luau/numbers) |

Inherited Members

2 inherited from [SoundEffect](/docs/reference/engine/classes/SoundEffect)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The TremoloSoundEffect creates a trembling effect on a sound by varying the
volume of the sound up and down.

Like all other [SoundEffects](/docs/reference/engine/classes/SoundEffect), a TremoloSoundEffect can be
applied either to a [Sound](/docs/reference/engine/classes/Sound) or [SoundGroup](/docs/reference/engine/classes/SoundGroup) by being parented to
either.

---

API Reference

Properties

Depth

Read Parallel

Controls how much the volume will raise and lower.

TremoloSoundEffect.Depth:[number](/docs/luau/numbers)

Range: 0 to 1 (default 1) Controls how much the volume will raise and
lower. This value ranges between 0 (minimum volume) and 1 (maximum
volume). If set to its minimum, the volume will not oscillate at all.

Provide feedback

---

Duty

Read Parallel

Controls how long during one volume oscillation the effect will be active.

TremoloSoundEffect.Duty:[number](/docs/luau/numbers)

Range: 0 to 1 (default 0.5) Controls how long during one volume
oscillation the effect will be active, specifically what percentage
between 0 (0%) and 1 (100%).

Provide feedback

---

Frequency

Read Parallel

Sets how often the effect will oscillate the volume.

TremoloSoundEffect.Frequency:[number](/docs/luau/numbers)

Range: 0.1 to 20 (default 5) Sets how often the effect will oscillate the
volume. Measured in Hz.

Provide feedback

---