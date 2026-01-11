# ReverbSoundEffect | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ReverbSoundEffect
Scraped: 2026-01-11T02:32:47.051136Z

## Inherits
- SoundEffect
- ReverbSoundEffect
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
7. [ReverbSoundEffect](/docs/reference/engine/classes/ReverbSoundEffect)

English

Feedback

Engine Class

![ReverbSoundEffect](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/ReverbSoundEffect-Dark.webp)ReverbSoundEffect

Reverberates audio, simulating the effect of bouncing off walls in a room.

---

Summary

Properties

|  |
| --- |
| [DecayTime](#DecayTime):[number](/docs/luau/numbers) |
| [Density](#Density):[number](/docs/luau/numbers) |
| [Diffusion](#Diffusion):[number](/docs/luau/numbers) |
| [DryLevel](#DryLevel):[number](/docs/luau/numbers) |
| [WetLevel](#WetLevel):[number](/docs/luau/numbers) |

Inherited Members

2 inherited from [SoundEffect](/docs/reference/engine/classes/SoundEffect)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The ReverbSoundEffect simulates the effect of sounds bouncing off of
several surfaces (such as walls in a room), which causes several overlapping
echoes that arrive at the listener at slightly offset times.

Like all other [SoundEffects](/docs/reference/engine/classes/SoundEffect), a [ReverbSoundEffect](/docs/reference/engine/classes/ReverbSoundEffect)
can be applied either to a [Sound](/docs/reference/engine/classes/Sound) or [SoundGroup](/docs/reference/engine/classes/SoundGroup) by being
parented to either.

---

API Reference

Properties

DecayTime

Read Parallel

Sets how long it takes for the reverberating echoes to fade out
completely.

ReverbSoundEffect.DecayTime:[number](/docs/luau/numbers)

Range: 0.1 to 20 (default 1.5) Sets how long it takes for the
reverberating echoes to fade out completely. Larger decay times simulate
larger (empty) spaces

Provide feedback

---

Density

Read Parallel

Controls how many reflections are generated.

ReverbSoundEffect.Density:[number](/docs/luau/numbers)

Range: 0 to 1 (default 1) Controls how many reflections are generated.

Provide feedback

---

Diffusion

Read Parallel

Controls how smooth and reflective the simulated surfaces are.

ReverbSoundEffect.Diffusion:[number](/docs/luau/numbers)

Range: 0 to 1 (default 1) Controls how smooth and reflective the simulated
surfaces are. The lower this value, the more discrete the echoes are. At
higher levels the echos will blend more.

Provide feedback

---

DryLevel

Read Parallel

The output volume of the original sound.

ReverbSoundEffect.DryLevel:[number](/docs/luau/numbers)

Range: -80 to 10 (default -6) The output volume of the original sound.

Provide feedback

---

WetLevel

Read Parallel

The output volume of the echoed effect.

ReverbSoundEffect.WetLevel:[number](/docs/luau/numbers)

Range: -80 to 10 (default 0) The output volume of the echoed effect.

Provide feedback

---