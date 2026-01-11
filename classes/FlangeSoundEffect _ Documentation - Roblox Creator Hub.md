# FlangeSoundEffect | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/FlangeSoundEffect
Scraped: 2026-01-11T02:30:25.729545Z

## Inherits
- SoundEffect
- FlangeSoundEffect
- Instance
- Object
- Sound
- SoundGroup
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [SoundEffect](/docs/reference/engine/classes/SoundEffect)
6. /
7. [FlangeSoundEffect](/docs/reference/engine/classes/FlangeSoundEffect)

English

Feedback

Engine Class

![FlangeSoundEffect](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/FlangeSoundEffect-Dark.webp)FlangeSoundEffect

Creates a sweeping or swooshing effect on a sound.

---

Summary

Properties

|  |
| --- |
| [Depth](#Depth):[number](/docs/luau/numbers) |
| [Mix](#Mix):[number](/docs/luau/numbers) |
| [Rate](#Rate):[number](/docs/luau/numbers) |

Inherited Members

2 inherited from [SoundEffect](/docs/reference/engine/classes/SoundEffect)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The FlangeSoundEffect creates a sweeping or swooshing effect on the Sound or
SoundGroup it is applied to. It does this by copying the original audio signal
and playing on top of the original but slightly offset and modulated.

Like all other [SoundEffect](/docs/reference/engine/classes/SoundEffect), a FlangeSoundEffect can be applied either
to a [Sound](/docs/reference/engine/classes/Sound) or [SoundGroup](/docs/reference/engine/classes/SoundGroup) by being parented to either.

---

API Reference

Properties

Depth

Read Parallel

The intensity of the effect.

FlangeSoundEffect.Depth:[number](/docs/luau/numbers)

Range: 0.01 to 1 (default 0.45) The intensity of the effect. This value
determines how offset the duplicated signal will be from the original.
This value is the percentage of the max offset (40ms).

Provide feedback

---

Mix

Read Parallel

Percentage of the original sound that will be applied to the filter.

FlangeSoundEffect.Mix:[number](/docs/luau/numbers)

Range: 0 to 1 (default 0.85) Percentage of the original sound that will be
applied to the filter. Raising this value will make the effect sound
louder and be more apparent.

Provide feedback

---

Rate

Read Parallel

The frequency that the effect oscillates at.

FlangeSoundEffect.Rate:[number](/docs/luau/numbers)

Range: 0 to 20 (default 5) The frequency that the effect oscillates at.
Measured in Hz.

Provide feedback

---