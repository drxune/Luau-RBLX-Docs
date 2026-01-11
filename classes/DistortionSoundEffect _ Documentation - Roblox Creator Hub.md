# DistortionSoundEffect | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/DistortionSoundEffect
Scraped: 2026-01-11T02:31:13.217476Z

## Inherits
- SoundEffect
- DistortionSoundEffect
- Instance
- Object
- Sound
- SoundGroup
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [SoundEffect](/docs/reference/engine/classes/SoundEffect)
6. /
7. [DistortionSoundEffect](/docs/reference/engine/classes/DistortionSoundEffect)

English

Feedback

Engine Class

![DistortionSoundEffect](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/DistortionSoundEffect-Dark.webp)DistortionSoundEffect

Distorts audio, making it sound fuzzier and overdriven.

---

Summary

Properties

|  |
| --- |
| [Level](#Level):[number](/docs/luau/numbers) |

Inherited Members

2 inherited from [SoundEffect](/docs/reference/engine/classes/SoundEffect)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A distortion effect is used to simulate the effect that would occur when
overdriving older style audio equipment (such as vacuum tubes). This effect
causes clipping in the sound and adds a general "fuzziness".

Like all other [SoundEffect](/docs/reference/engine/classes/SoundEffect), a DistortionSoundEffect can be applied
either to a [Sound](/docs/reference/engine/classes/Sound) or [SoundGroup](/docs/reference/engine/classes/SoundGroup) by being parented to either.

---

API Reference

Properties

Level

Read Parallel

The intensity of the effect.

DistortionSoundEffect.Level:[number](/docs/luau/numbers)

Range: 0 to 1 (default 0.5) The intensity of the effect. Setting this
property to its minimum (0) will cause no distortion at all.

Provide feedback

---