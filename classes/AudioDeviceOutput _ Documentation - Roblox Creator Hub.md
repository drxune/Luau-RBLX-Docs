# AudioDeviceOutput | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AudioDeviceOutput
Scraped: 2026-01-11T02:33:25.761844Z

## Inherits
- Instance
- AudioDeviceOutput
- Player
- Wire
- Object
- Wires
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AudioDeviceOutput](/docs/reference/engine/classes/AudioDeviceOutput)

English

Feedback

Engine Class

![AudioDeviceOutput](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AudioDeviceOutput-Dark.webp)AudioDeviceOutput

Accepts audio streams to be rendered out to physical hardware devices such as
speakers or headphones.

---

Summary

Properties

|  |
| --- |
| [Player](#Player):[Player](/docs/reference/engine/classes/Player) |

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

[AudioDeviceOutput](/docs/reference/engine/classes/AudioDeviceOutput) accepts audio streams to be rendered out to physical
hardware devices such as speakers or headphones. It provides a single
Input pin that can be targeted by [Wires](/docs/reference/engine/classes/Wire). Any audio streams
wired to an [AudioDeviceOutput](/docs/reference/engine/classes/AudioDeviceOutput) are heard.

Code Samples

Outputting Audio to Device

```
local audioPlayer: AudioPlayer = Instance.new("AudioPlayer")



audioPlayer.Parent = workspace



audioPlayer.AssetId = "rbxassetid://9112854440"



local deviceOutput = Instance.new("AudioDeviceOutput")



deviceOutput.Parent = workspace



local wire = Instance.new("Wire")



wire.Parent = workspace



wire.SourceInstance = audioPlayer



wire.TargetInstance = deviceOutput



audioPlayer:Play()
```

---

API Reference

Properties

Player

Read Parallel

A [Player](/docs/reference/engine/classes/Player) who is intended to hear the connected audio streams.

AudioDeviceOutput.Player:[Player](/docs/reference/engine/classes/Player)

An optional [Player](/docs/reference/engine/classes/Player) who is intended to hear the connected audio
streams. If left unspecified, the streams wired to this
[AudioDeviceOutput](/docs/reference/engine/classes/AudioDeviceOutput) are heard by everyone.

Provide feedback

---

Methods

GetConnectedWires

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin.

AudioDeviceOutput:GetConnectedWires(pin:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| pin:[string](/docs/luau/strings) |

Returns

Instances

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin. [AudioDeviceOutput](/docs/reference/engine/classes/AudioDeviceOutput) has one "Input" pin.

Provide feedback

---

GetInputPins

AudioDeviceOutput:GetInputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetOutputPins

AudioDeviceOutput:GetOutputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

Events

WiringChanged

Fires when another instance is connected to or disconnected from the
[AudioDeviceOutput](/docs/reference/engine/classes/AudioDeviceOutput) via a [Wire](/docs/reference/engine/classes/Wire).

AudioDeviceOutput.WiringChanged(

connected:[boolean](/docs/luau/booleans), pin:[string](/docs/luau/strings), wire:[Wire](/docs/reference/engine/classes/Wire), instance:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| connected:[boolean](/docs/luau/booleans)  Whether the instance got connected or disconnected. |
| pin:[string](/docs/luau/strings)  The pin on the [AudioDeviceOutput](/docs/reference/engine/classes/AudioDeviceOutput) that the [Wire](/docs/reference/engine/classes/Wire) targets. |
| wire:[Wire](/docs/reference/engine/classes/Wire)  The [Wire](/docs/reference/engine/classes/Wire) between the [AudioDeviceOutput](/docs/reference/engine/classes/AudioDeviceOutput) and the other instance. |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The other instance that is or was connected through the [Wire](/docs/reference/engine/classes/Wire). |

Event that fires after a [Wire](/docs/reference/engine/classes/Wire) becomes connected or disconnected,
and that [Wire](/docs/reference/engine/classes/Wire) is now or was previously connected to a pin on the
[AudioDeviceOutput](/docs/reference/engine/classes/AudioDeviceOutput) and to some other wirable instance.

Provide feedback

---