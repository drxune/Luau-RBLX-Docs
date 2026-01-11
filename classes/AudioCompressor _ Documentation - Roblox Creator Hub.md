# AudioCompressor | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AudioCompressor
Scraped: 2026-01-11T02:31:37.495609Z

## Tags
- Not Replicated

## Inherits
- Instance
- AudioCompressor
- Wire
- Object
- Wire.TargetName
- Wire.SourceName
- Threshold
- Attack
- Release
- Wires
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AudioCompressor](/docs/reference/engine/classes/AudioCompressor)

English

Feedback

Engine Class

![AudioCompressor](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AudioCompressor-Dark.webp)AudioCompressor

Adjusts the dynamic range of input streams.

---

Summary

Properties

|  |
| --- |
| [Attack](#Attack):[number](/docs/luau/numbers) |
| [Bypass](#Bypass):[boolean](/docs/luau/booleans) |
| [Editor](#Editor):[boolean](/docs/luau/booleans) |
| [MakeupGain](#MakeupGain):[number](/docs/luau/numbers) |
| [Ratio](#Ratio):[number](/docs/luau/numbers) |
| [Release](#Release):[number](/docs/luau/numbers) |
| [Threshold](#Threshold):[number](/docs/luau/numbers) |

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

[AudioCompressor](/docs/reference/engine/classes/AudioCompressor) adjusts the dynamic range of audio streams. Any
momentary bursts of loudness will be clamped down according to the
compressor's properties.

[AudioCompressor](/docs/reference/engine/classes/AudioCompressor) provides Input and Sidechain pins that can be
targeted by [Wire.TargetName](/docs/reference/engine/classes/Wire#TargetName), and an Output pin that can be used by
[Wire.SourceName](/docs/reference/engine/classes/Wire#SourceName).

Code Samples

Sidechain Compression

By using Sidechain compression, the background ambience can be ducked around an explosion

```
local deviceOutput: AudioDeviceOutput = Instance.new("AudioDeviceOutput")



deviceOutput.Parent = workspace



local explosionPlayer: AudioPlayer = Instance.new("AudioPlayer")



explosionPlayer.Parent = workspace



explosionPlayer.AssetId = "rbxassetid://1835333184"



local ambiencePlayer = Instance.new("AudioPlayer")



ambiencePlayer.AssetId = "rbxassetid://9112854440"



local compressor = Instance.new("AudioCompressor")



local wireToCompressor = Instance.new("Wire")



local wireToSidechain = Instance.new("Wire")



local wireToOutput = Instance.new("Wire")



ambiencePlayer.Parent = workspace



compressor.Parent = workspace



wireToCompressor.Parent = workspace



wireToSidechain.Parent = workspace



wireToOutput.Parent = workspace



wireToCompressor.SourceInstance = ambiencePlayer



wireToCompressor.TargetInstance = compressor



wireToSidechain.SourceInstance = explosionPlayer



wireToSidechain.TargetInstance = compressor



wireToSidechain.TargetName = "Sidechain"



wireToOutput.SourceInstance = compressor



wireToOutput.TargetInstance = deviceOutput



ambiencePlayer:Play()
```

---

API Reference

Properties

Attack

Read Parallel

Controls how quickly the compressor will clamp down on volume after it
surpasses [Threshold](/docs/reference/engine/classes/AudioCompressor#Threshold).

AudioCompressor.Attack:[number](/docs/luau/numbers)

Time, in seconds, denoting how quickly the compressor will clamp down on
volume after it surpasses [Threshold](/docs/reference/engine/classes/AudioCompressor#Threshold).
Ranges from 0.001 to 0.5.

Provide feedback

---

Bypass

Read Parallel

Whether audio streams are passed-through unaffected by this effect.

AudioCompressor.Bypass:[boolean](/docs/luau/booleans)

If true, audio streams are passed-through unaffected by this effect.

Provide feedback

---

Editor

Not Replicated

Roblox Script Security

Read Parallel

AudioCompressor.Editor:[boolean](/docs/luau/booleans)

Provide feedback

---

MakeupGain

Read Parallel

A gain value to be applied after compression.

AudioCompressor.MakeupGain:[number](/docs/luau/numbers)

Gain value to be applied after compression, in decibels. After limiting
the dynamic range, the resulting stream may be very quiet and this
property can be used to compensate. Ranges from -30 to 30.

Provide feedback

---

Ratio

Read Parallel

Ratio of input volume to output volume, to be applied when surpassing
[Threshold](/docs/reference/engine/classes/AudioCompressor#Threshold).

AudioCompressor.Ratio:[number](/docs/luau/numbers)

Ratio of input volume to output volume, to be applied when surpassing
[Threshold](/docs/reference/engine/classes/AudioCompressor#Threshold). For example, a value of 2
will cut the amount by which the input stream exceeds the threshold in
half whenever the input stream does so. Ranges from 1 to 50.

Provide feedback

---

Release

Read Parallel

Controls how quickly the compressor will unclamp after the stream volume
dips back below [Threshold](/docs/reference/engine/classes/AudioCompressor#Threshold).

AudioCompressor.Release:[number](/docs/luau/numbers)

Time, in seconds, denoting how quickly the compressor will unclamp after
its stream volume dips back below
[Threshold](/docs/reference/engine/classes/AudioCompressor#Threshold). Ranges from 0.01 to 0.5.

Provide feedback

---

Threshold

Read Parallel

Gain value at which the compressor will start to modify the input stream.

AudioCompressor.Threshold:[number](/docs/luau/numbers)

Gain value at which the compressor will start to modify the input stream,
in decibels, with a range of -60 to 0. When the input stream's volume
surpasses [Threshold](/docs/reference/engine/classes/AudioCompressor#Threshold), the compressor will
take [Attack](/docs/reference/engine/classes/AudioCompressor#Attack) seconds to kick in. When the
input stream's volume recedes below
[Threshold](/docs/reference/engine/classes/AudioCompressor#Threshold), the compressor will take
[Release](/docs/reference/engine/classes/AudioCompressor#Release) seconds to stop acting.

If any [Wires](/docs/reference/engine/classes/Wire) are connected to the Sidechain pin of the
compressor, this threshold analyzes those streams instead of the Input
streams; this can be used to duck the volume of one stream in response to
another.

Provide feedback

---

Methods

GetConnectedWires

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin.

AudioCompressor:GetConnectedWires(pin:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| pin:[string](/docs/luau/strings) |

Returns

Instances

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin. [AudioCompressor](/docs/reference/engine/classes/AudioCompressor) has one "Input" pin, one "Sidechain" pin, and
one "Output" pin.

Provide feedback

---

GetInputPins

AudioCompressor:GetInputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetOutputPins

AudioCompressor:GetOutputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

Events

WiringChanged

Fires when another instance is connected to or disconnected from the
[AudioCompressor](/docs/reference/engine/classes/AudioCompressor) via a [Wire](/docs/reference/engine/classes/Wire).

AudioCompressor.WiringChanged(

connected:[boolean](/docs/luau/booleans), pin:[string](/docs/luau/strings), wire:[Wire](/docs/reference/engine/classes/Wire), instance:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| connected:[boolean](/docs/luau/booleans)  Whether the instance got connected or disconnected. |
| pin:[string](/docs/luau/strings)  The pin on the [AudioCompressor](/docs/reference/engine/classes/AudioCompressor) that the [Wire](/docs/reference/engine/classes/Wire) targets. |
| wire:[Wire](/docs/reference/engine/classes/Wire)  The [Wire](/docs/reference/engine/classes/Wire) between the [AudioCompressor](/docs/reference/engine/classes/AudioCompressor) and the other instance. |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The other instance that is or was connected through the [Wire](/docs/reference/engine/classes/Wire). |

Event that fires after a [Wire](/docs/reference/engine/classes/Wire) becomes connected or disconnected,
and that [Wire](/docs/reference/engine/classes/Wire) is now or was previously connected to a pin on the
[AudioCompressor](/docs/reference/engine/classes/AudioCompressor) and to some other wirable instance.

Provide feedback

---