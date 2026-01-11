# ChorusSoundEffect | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ChorusSoundEffect
Scraped: 2026-01-11T02:31:47.422471Z

## Inherits
- SoundEffect
- ChorusSoundEffect
- Instance
- Object
- Sound
- SoundGroup
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [SoundEffect](/docs/reference/engine/classes/SoundEffect)
6. /
7. [ChorusSoundEffect](/docs/reference/engine/classes/ChorusSoundEffect)

English

Feedback

Engine Class

![ChorusSoundEffect](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/ChorusSoundEffect-Dark.webp)ChorusSoundEffect

Makes audio more voluminous by simulating multiple voices playing the same
part.

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

A ChorusSoundEffect simulates the effect of multiple vocals or instruments
playing the same part. It does this by taking the original sound and
overlaying copies of that sound. These copies are not exact matches to the
original but instead vary in pitch slightly. This simulates a real chorus, as
different singers or instruments will have slight variations. This effect can
be applied to either an individual sound or to a sound group by parenting it
to the desired instance.

Like all other [SoundEffect](/docs/reference/engine/classes/SoundEffect), a ChorusSoundEffect can be applied either
to a [Sound](/docs/reference/engine/classes/Sound) or [SoundGroup](/docs/reference/engine/classes/SoundGroup) by being parented to either.

---

API Reference

Properties

Depth

Read Parallel

Controls how intense the effect is.

ChorusSoundEffect.Depth:[number](/docs/luau/numbers)

Range: 0 to 1 (default 0.15) Controls how intense the effect is.

Provide feedback

---

Mix

Read Parallel

Percentage of the original sound that will be applied to the filter.

ChorusSoundEffect.Mix:[number](/docs/luau/numbers)

Range: 0 to 1 (default 0.5) Percentage of the original sound that will be
applied to the filter. Raising this value will make the effect sound
louder and be more apparent.

Provide feedback

---

Rate

Read Parallel

How frequently the pitch variation changes.

ChorusSoundEffect.Rate:[number](/docs/luau/numbers)

Range: 0 to 20 (default 0.5) How frequently the pitch variation changes.
Measured in Hz.

Provide feedback

---