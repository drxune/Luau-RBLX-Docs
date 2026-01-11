# SoundEffect | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/SoundEffect
Scraped: 2026-01-11T02:30:24.494899Z

## Tags
- Not Creatable

## Inherits
- Object
- Instance
- SoundEffect
- Sound
- SoundGroup
- ChorusSoundEffect
- CompressorSoundEffect
- DistortionSoundEffect
- EchoSoundEffect
- EqualizerSoundEffect
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [SoundEffect](/docs/reference/engine/classes/SoundEffect)

English

Feedback

Engine Class

![SoundEffect](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/SoundEffect-Dark.webp)SoundEffect

SoundEffect is the base class that all other sound effects derive from. A
SoundEffect can be applied to either a [Sound](/docs/reference/engine/classes/Sound) or [SoundGroup](/docs/reference/engine/classes/SoundGroup) by
being parented to either.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [Priority](#Priority):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[ChorusSoundEffect](/docs/reference/engine/classes/ChorusSoundEffect), [CompressorSoundEffect](/docs/reference/engine/classes/CompressorSoundEffect), [DistortionSoundEffect](/docs/reference/engine/classes/DistortionSoundEffect), [EchoSoundEffect](/docs/reference/engine/classes/EchoSoundEffect), [EqualizerSoundEffect](/docs/reference/engine/classes/EqualizerSoundEffect), Show more...

SoundEffect is the base class that all other sound effects derive from. A
SoundEffect can be applied to either a [Sound](/docs/reference/engine/classes/Sound) or [SoundGroup](/docs/reference/engine/classes/SoundGroup) by
being parented to either. Multiple effects can be applied to the same Sound or
SoundGroup. The order the effects will be applied in is determined by that
effect's Priority.

---

API Reference

Properties

Enabled

Read Parallel

Toggles the effect on and off.

SoundEffect.Enabled:[boolean](/docs/luau/booleans)

Toggles the effect on and off. True by default.

Provide feedback

---

Priority

Read Parallel

Determines the order the effect will be applied in relation to other
effects.

SoundEffect.Priority:[number](/docs/luau/numbers)

Determines the order the effect will be applied in relation to other
effects. Higher priority effects will be applied earlier. The exception is
when Priority equals 0 (which is the default). In this case, the base
priority for the effect will be used. If the priority of two effects are
equal, then the order is undetermined.

Provide feedback

---