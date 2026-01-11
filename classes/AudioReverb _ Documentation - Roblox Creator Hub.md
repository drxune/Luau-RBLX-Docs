# AudioReverb | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AudioReverb
Scraped: 2026-01-11T02:39:43.740147Z

## Inherits
- Object
- Instance
- AudioReverb
- Wire
- Wires
- ReferenceFrequency
- LowShelfGain
- DecayRatio
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AudioReverb](/docs/reference/engine/classes/AudioReverb)

English

Feedback

Engine Class

![AudioReverb](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AudioReverb-Dark.webp)AudioReverb

Reverberates audio streams.

---

Summary

Properties

|  |
| --- |
| [Bypass](#Bypass):[boolean](/docs/luau/booleans) |
| [DecayRatio](#DecayRatio):[number](/docs/luau/numbers) |
| [DecayTime](#DecayTime):[number](/docs/luau/numbers) |
| [Density](#Density):[number](/docs/luau/numbers) |
| [Diffusion](#Diffusion):[number](/docs/luau/numbers) |
| [DryLevel](#DryLevel):[number](/docs/luau/numbers) |
| [EarlyDelayTime](#EarlyDelayTime):[number](/docs/luau/numbers) |
| [HighCutFrequency](#HighCutFrequency):[number](/docs/luau/numbers) |
| [LateDelayTime](#LateDelayTime):[number](/docs/luau/numbers) |
| [LowShelfFrequency](#LowShelfFrequency):[number](/docs/luau/numbers) |
| [LowShelfGain](#LowShelfGain):[number](/docs/luau/numbers) |
| [ReferenceFrequency](#ReferenceFrequency):[number](/docs/luau/numbers) |
| [WetLevel](#WetLevel):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [GetConnectedWires](#GetConnectedWires)(pin: [string](/docs/luau/strings)):Instances |
| [GetInputPins](#GetInputPins)():[Array](/docs/luau/tables#arrays) |
| [GetOutputPins](#GetOutputPins)():[Array](/docs/luau/tables#arrays) |

Events

|  |
| --- |
| [WiringChanged](#WiringChanged)(connected: [boolean](/docs/luau/booleans),pin: [string](/docs/luau/strings),wire: [Wire](/docs/reference/engine/classes/Wire),instance: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[AudioReverb](/docs/reference/engine/classes/AudioReverb) reverberates audio streams, modeling the natural echoes of
a room or enclosed space. It provides one Input pin and one Output pin
which can be connected to/from by [Wires](/docs/reference/engine/classes/Wire).

---

API Reference

Properties

Bypass

Read Parallel

Whether audio streams are passed-through unaffected by this effect.

AudioReverb.Bypass:[boolean](/docs/luau/booleans)

If true, audio streams are passed-through unaffected by this effect.

Provide feedback

---

DecayRatio

Read Parallel

Controls how quickly high frequency sound decays compared to the overall
reverb.

AudioReverb.DecayRatio:[number](/docs/luau/numbers)

A ratio of high frequency decay time to total decay time, where high
frequencies are determined to be anything above
[ReferenceFrequency](/docs/reference/engine/classes/AudioReverb#ReferenceFrequency), in hertz.
Ranges from 0.1 to 1.

Provide feedback

---

DecayTime

Read Parallel

Controls how long it takes for the reverb to dissipate.

AudioReverb.DecayTime:[number](/docs/luau/numbers)

Time, in seconds, that it will take for the reverb to fully decay. Ranges
from 0.1 to 20.

Provide feedback

---

Density

Read Parallel

Controls how many reflections are generated.

AudioReverb.Density:[number](/docs/luau/numbers)

A number controlling how many reflections are generated. Ranges from 0
to 1.

Provide feedback

---

Diffusion

Read Parallel

Controls how smooth and reflective the simulated surfaces are.

AudioReverb.Diffusion:[number](/docs/luau/numbers)

A number controlling how smooth and reflective the reverb's simulated
surfaces are. Ranges from 0 to 1.

Provide feedback

---

DryLevel

Read Parallel

Gain level determining how loud the original, unaltered audio stream will
be.

AudioReverb.DryLevel:[number](/docs/luau/numbers)

Gain level, in decibels, determining how loud the original, unaltered
audio stream will be. Ranges from -80 to 20.

Provide feedback

---

EarlyDelayTime

Read Parallel

Controls the amount of time before reverberation begins .

AudioReverb.EarlyDelayTime:[number](/docs/luau/numbers)

Time, in seconds, before any reverberation begins. Ranges from 0 to 0.3.

Provide feedback

---

HighCutFrequency

Read Parallel

Frequency above which sound is filtered out of the reverb.

AudioReverb.HighCutFrequency:[number](/docs/luau/numbers)

Frequency, in hertz, which acts as a cutoff for a low-pass filter. Any
audio that has a higher frequency than this is excluded from the reverb.
Ranges from 20 to 20,000.

Provide feedback

---

LateDelayTime

Read Parallel

Time, following early delays, before diffuse reverberations begin.

AudioReverb.LateDelayTime:[number](/docs/luau/numbers)

Time in seconds, following early delays, before diffuse reverberations
begin. Ranges from 0 to 0.1.

Provide feedback

---

LowShelfFrequency

Read Parallel

Frequency below which audio can be boosted or reduced in the reverb.

AudioReverb.LowShelfFrequency:[number](/docs/luau/numbers)

Frequency, in hertz, below which audio can be boosted or reduced in the
reverb via [LowShelfGain](/docs/reference/engine/classes/AudioReverb#LowShelfGain). Ranges from 20
to 20,000.

Provide feedback

---

LowShelfGain

Read Parallel

Controls the presence of low frequency content in the reverb.

AudioReverb.LowShelfGain:[number](/docs/luau/numbers)

Gain level, in decibels, that controls the presence of low frequency
content in the reverb. Ranges from -36 to 12.

Provide feedback

---

ReferenceFrequency

Read Parallel

Frequency that separates low frequency decay speeds from high frequency
decay speeds.

AudioReverb.ReferenceFrequency:[number](/docs/luau/numbers)

Frequency, in hertz, that separates low frequency decay speeds from high
frequency decay speeds. This is used by
[DecayRatio](/docs/reference/engine/classes/AudioReverb#DecayRatio) to determine whether low or high
frequencies decay faster. Ranges from 20 to 20,000.

Provide feedback

---

WetLevel

Read Parallel

Gain level determining how loud the reverberated stream will be.

AudioReverb.WetLevel:[number](/docs/luau/numbers)

Gain level, in decibels, determining how loud the reverberated stream will
be. Ranges from -80 to 20.

Provide feedback

---

Methods

GetConnectedWires

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin.

AudioReverb:GetConnectedWires(pin:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| pin:[string](/docs/luau/strings) |

Returns

Instances

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin. [AudioReverb](/docs/reference/engine/classes/AudioReverb) has one "Input" pin and one "Output" pin.

Provide feedback

---

GetInputPins

AudioReverb:GetInputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetOutputPins

AudioReverb:GetOutputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

Events

WiringChanged

Fires when another instance is connected to or disconnected from the
[AudioReverb](/docs/reference/engine/classes/AudioReverb) via a [Wire](/docs/reference/engine/classes/Wire).

AudioReverb.WiringChanged(

connected:[boolean](/docs/luau/booleans), pin:[string](/docs/luau/strings), wire:[Wire](/docs/reference/engine/classes/Wire), instance:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| connected:[boolean](/docs/luau/booleans)  Whether the instance got connected or disconnected. |
| pin:[string](/docs/luau/strings)  The pin on the [AudioReverb](/docs/reference/engine/classes/AudioReverb) that the [Wire](/docs/reference/engine/classes/Wire) targets. |
| wire:[Wire](/docs/reference/engine/classes/Wire)  The [Wire](/docs/reference/engine/classes/Wire) between the [AudioReverb](/docs/reference/engine/classes/AudioReverb) and the other instance. |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The other instance that is or was connected through the [Wire](/docs/reference/engine/classes/Wire). |

Event that fires after a [Wire](/docs/reference/engine/classes/Wire) becomes connected or disconnected,
and that [Wire](/docs/reference/engine/classes/Wire) is now or was previously connected to a pin on the
[AudioReverb](/docs/reference/engine/classes/AudioReverb) and to some other wirable instance.

Provide feedback

---