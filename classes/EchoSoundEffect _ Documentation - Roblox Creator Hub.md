# EchoSoundEffect | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/EchoSoundEffect
Scraped: 2026-01-11T02:35:26.534137Z

## Inherits
- SoundEffect
- EchoSoundEffect
- Instance
- Object
- Sound
- SoundGroup
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [SoundEffect](/docs/reference/engine/classes/SoundEffect)
6. /
7. [EchoSoundEffect](/docs/reference/engine/classes/EchoSoundEffect)

English

Feedback

Engine Class

![EchoSoundEffect](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/EchoSoundEffect-Dark.webp)EchoSoundEffect

Adds delayed repetitions of a sound with diminishing volume.

---

Summary

Properties

|  |
| --- |
| [Delay](#Delay):[number](/docs/luau/numbers) |
| [DryLevel](#DryLevel):[number](/docs/luau/numbers) |
| [Feedback](#Feedback):[number](/docs/luau/numbers) |
| [WetLevel](#WetLevel):[number](/docs/luau/numbers) |

Inherited Members

2 inherited from [SoundEffect](/docs/reference/engine/classes/SoundEffect)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An echo effect causes a sound to repeat on a delay with diminishing volume,
simulating the real effect of an echo. This effect can be applied to either an
individual sound or to a sound group by parenting it to the desired instance.

The effect is controlled by several properties. First, the Delay is how long
the effect will wait to play the echoed sound. Feedback determines how much
the original signal is diminished to play as the echoed sound. Note that this
echoed sound also goes through the echo effect which will wait another delay
and play another echo. This process will repeat until the volume of the echoed
sound is negligible.

You can also adjust the wet/dry mix of the effect. The dry component of the
sound is the original sound that the effect is being applied to. You can
adjust the volume of the dry sound by adjusting the DryLevel. The wet sound is
the echoed effect itself, and its volume can be adjusted with WetLevel.

It is recommended to only use the EchoSoundEffect with sound groups. If an
echo effect is applied to a regular Sound, once that sound stops playing the
echo effect will also be cut off. When applied to a SoundGroup, the echo
effect will continue playing even if the original source sound has
stopped.Like all other [SoundEffect](/docs/reference/engine/classes/SoundEffect), a EchoSoundEffect can be applied
either to a [Sound](/docs/reference/engine/classes/Sound) or [SoundGroup](/docs/reference/engine/classes/SoundGroup) by being parented to either.

---

API Reference

Properties

Delay

Read Parallel

The amount of time between echoes.

EchoSoundEffect.Delay:[number](/docs/luau/numbers)

Range: 0.01 to 5 (default 1) The amount of time between echoes. Measured
in seconds.

If a EchoSoundEffect is applied to a singular sound instead of a sound
group, if the sound stops playing before the delay causes an echo, the
echo will not play. Because of this, it is recommended to apply echo
effects to SoundGroups and not Sounds.

Provide feedback

---

DryLevel

Read Parallel

The output volume of the original sound.

EchoSoundEffect.DryLevel:[number](/docs/luau/numbers)

Range: -80 to 10 (default 0) The output volume of the original sound.

Provide feedback

---

Feedback

Read Parallel

The echo decay every time the echo plays.

EchoSoundEffect.Feedback:[number](/docs/luau/numbers)

Range: 0 to 1 (default 0.5) The echo decay every time the echo plays.
Setting this at it's minimum (0) will cause no feedback, meaning the echo
won't be audible at all. Setting this at the maximum (1) will have no
decay, meaning the echoed sound will play at the level of the original and
will not diminish over time.

Provide feedback

---

WetLevel

Read Parallel

The output volume of the echoed effect.

EchoSoundEffect.WetLevel:[number](/docs/luau/numbers)

Range: -80 to 10 (default 0) The output volume of the echoed effect.

Provide feedback

---