# CompressorSoundEffect | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/CompressorSoundEffect
Scraped: 2026-01-11T02:38:53.764548Z

## Inherits
- SoundEffect
- CompressorSoundEffect
- Instance
- Object
- Sound
- SoundGroup
- Threshold
- Attack
- Release
- GainMakeup
- SideChain
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [SoundEffect](/docs/reference/engine/classes/SoundEffect)
6. /
7. [CompressorSoundEffect](/docs/reference/engine/classes/CompressorSoundEffect)

English

Feedback

Engine Class

![CompressorSoundEffect](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/CompressorSoundEffect-Dark.webp)CompressorSoundEffect

Adjusts the dynamic range of audio.

---

Summary

Properties

|  |
| --- |
| [Attack](#Attack):[number](/docs/luau/numbers) |
| [GainMakeup](#GainMakeup):[number](/docs/luau/numbers) |
| [Ratio](#Ratio):[number](/docs/luau/numbers) |
| [Release](#Release):[number](/docs/luau/numbers) |
| [SideChain](#SideChain):[Instance](/docs/reference/engine/datatypes/Instance) |
| [Threshold](#Threshold):[number](/docs/luau/numbers) |

Inherited Members

2 inherited from [SoundEffect](/docs/reference/engine/classes/SoundEffect)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A [CompressorSoundEffect](/docs/reference/engine/classes/CompressorSoundEffect) is used to reduce the dynamic range of audio
by moving the highs and lows of a signal closer together. It does this by
lowering the volume of the highest parts of a source while at the same time
raising the overall volume. This type of effect is useful when you have many
sounds playing and you want to make sure the quieter ones are still audible.
This effect can be applied to either an individual [Sound](/docs/reference/engine/classes/Sound) or
[SoundGroup](/docs/reference/engine/classes/SoundGroup) by parenting it to the desired instance.

A compressor has several properties which determine how it works. The
[Threshold](/docs/reference/engine/classes/CompressorSoundEffect#Threshold) is the audio level where the
compressor will start to lower the volume. As soon as the source goes below
the threshold, the compressor will stop lowering the volume.

The [Attack](/docs/reference/engine/classes/CompressorSoundEffect#Attack) determines how long it takes
for the compressed effect to fully apply. After the threshold has been crossed
the compressor will lower the volume over time until the desired ratio has
been reached. It will take the time specified by
[Attack](/docs/reference/engine/classes/CompressorSoundEffect#Attack) to reach this ratio.

The [Release](/docs/reference/engine/classes/CompressorSoundEffect#Release) determines how long it takes
for the compressor to remove its effect. After the volume of the source is
under the threshold, the compressor will restore the volume back to the
original over the time specified by
[Release](/docs/reference/engine/classes/CompressorSoundEffect#Release).

Along with lowering the volume when the sound has passed the threshold, a
compressor will also amplify the entire sound (after any threshold lowering
has taken effect). This allows quieter sounds to be amplified while louder
sounds can stay about the same. The
[GainMakeup](/docs/reference/engine/classes/CompressorSoundEffect#GainMakeup) determines how much the
effect amplifies the sound.

---

API Reference

Properties

Attack

Read Parallel

The time the effect takes to become active after its
[Threshold](/docs/reference/engine/classes/CompressorSoundEffect#Threshold) has been reached.

CompressorSoundEffect.Attack:[number](/docs/luau/numbers)

The time the effect takes to become active after its
[Threshold](/docs/reference/engine/classes/CompressorSoundEffect#Threshold) has been reached. Range
is 0.1 to 1 (default 0.1), measured in seconds.

Provide feedback

---

GainMakeup

Read Parallel

The overall amplification applied to the effect's [Sound](/docs/reference/engine/classes/Sound) or
[SoundGroup](/docs/reference/engine/classes/SoundGroup) after attenuation of sounds above the threshold.

CompressorSoundEffect.GainMakeup:[number](/docs/luau/numbers)

The overall amplification applied to the effect's [Sound](/docs/reference/engine/classes/Sound) or
[SoundGroup](/docs/reference/engine/classes/SoundGroup) after attenuation of sounds above the threshold. Keep
in mind this amplification will occur as long as the effect is active,
regardless of whether the
[Threshold](/docs/reference/engine/classes/CompressorSoundEffect#Threshold) has been reached or not.
Range is 0 to 30 (default 0), measured in dB.

Provide feedback

---

Ratio

Read Parallel

The ratio between the [SideChain](/docs/reference/engine/classes/CompressorSoundEffect#SideChain)
sound effect, and this sound effect.

CompressorSoundEffect.Ratio:[number](/docs/luau/numbers)

The ratio between the [SideChain](/docs/reference/engine/classes/CompressorSoundEffect#SideChain)
sound effect, and this sound effect.

Provide feedback

---

Release

Read Parallel

The time the effect takes to become inactive after its sound is below the
[Threshold](/docs/reference/engine/classes/CompressorSoundEffect#Threshold).

CompressorSoundEffect.Release:[number](/docs/luau/numbers)

The time the effect takes to become inactive after its sound is below the
[Threshold](/docs/reference/engine/classes/CompressorSoundEffect#Threshold). Range is 0 to 5
(default 0.1), measured in seconds.

Provide feedback

---

SideChain

Read Parallel

Applies a ducking effect to the compressor sound effect. The behavior of
the sidechain depends on the [Sound](/docs/reference/engine/classes/Sound) or [SoundGroup](/docs/reference/engine/classes/SoundGroup) linked to
it.

CompressorSoundEffect.SideChain:[Instance](/docs/reference/engine/datatypes/Instance)

Applies a ducking effect to the compressor sound effect. The behavior of
the sidechain depends on the [Sound](/docs/reference/engine/classes/Sound) or [SoundGroup](/docs/reference/engine/classes/SoundGroup) linked to
it.

Provide feedback

---

Threshold

Read Parallel

Volume level at which point the compressor applies its effect.

CompressorSoundEffect.Threshold:[number](/docs/luau/numbers)

Volume level at which point the compressor applies its effect. If the
effect's [Sound](/docs/reference/engine/classes/Sound) or [SoundGroup](/docs/reference/engine/classes/SoundGroup) is below the effect will not
attenuate the sound, although the
[GainMakeup](/docs/reference/engine/classes/CompressorSoundEffect#GainMakeup) will still be applied.
Range is -80 to 0 (default 0), measured in dB.

Provide feedback

---