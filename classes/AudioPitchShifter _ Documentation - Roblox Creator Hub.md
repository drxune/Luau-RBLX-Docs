# AudioPitchShifter | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AudioPitchShifter
Scraped: 2026-01-11T02:27:52.695859Z

## Inherits
- Instance
- AudioPitchShifter
- Wire
- Object
- Wires
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AudioPitchShifter](/docs/reference/engine/classes/AudioPitchShifter)

English

Feedback

Engine Class

![AudioPitchShifter](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AudioPitchShifter-Dark.webp)AudioPitchShifter

Adjusts the perceived pitch of audio streams.

---

Summary

Properties

|  |
| --- |
| [Bypass](#Bypass):[boolean](/docs/luau/booleans) |
| [Pitch](#Pitch):[number](/docs/luau/numbers) |
| [WindowSize](#WindowSize):[Enum.AudioWindowSize](/docs/reference/engine/enums/AudioWindowSize) |

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

[AudioPitchShifter](/docs/reference/engine/classes/AudioPitchShifter) adjusts the perceived pitch of audio streams. It
provides one Input pin and one Output pin which can be connected
to/from by [Wires](/docs/reference/engine/classes/Wire). [AudioPitchShifter](/docs/reference/engine/classes/AudioPitchShifter) performs its
modifications in the frequency domain and may introduce artifacts with extreme
pitch changes.

---

API Reference

Properties

Bypass

Read Parallel

Whether audio streams are passed-through unaffected by this effect.

AudioPitchShifter.Bypass:[boolean](/docs/luau/booleans)

If true, audio streams are passed-through unaffected by this effect.

Provide feedback

---

Pitch

Read Parallel

Pitch modification to be multiplied by the pitch of the input stream.

AudioPitchShifter.Pitch:[number](/docs/luau/numbers)

Pitch modification to be multiplied by the pitch of the input stream.
Ranges from 0.5 to 2.

Provide feedback

---

WindowSize

Read Parallel

AudioPitchShifter.WindowSize:[Enum.AudioWindowSize](/docs/reference/engine/enums/AudioWindowSize)

Provide feedback

---

Methods

GetConnectedWires

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin.

AudioPitchShifter:GetConnectedWires(pin:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| pin:[string](/docs/luau/strings) |

Returns

Instances

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin. [AudioPitchShifter](/docs/reference/engine/classes/AudioPitchShifter) has one "Input" pin and one "Output" pin.

Provide feedback

---

GetInputPins

AudioPitchShifter:GetInputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetOutputPins

AudioPitchShifter:GetOutputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

Events

WiringChanged

Fires when another instance is connected to or disconnected from the
[AudioPitchShifter](/docs/reference/engine/classes/AudioPitchShifter) via a [Wire](/docs/reference/engine/classes/Wire).

AudioPitchShifter.WiringChanged(

connected:[boolean](/docs/luau/booleans), pin:[string](/docs/luau/strings), wire:[Wire](/docs/reference/engine/classes/Wire), instance:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| connected:[boolean](/docs/luau/booleans)  Whether the instance got connected or disconnected. |
| pin:[string](/docs/luau/strings)  The pin on the [AudioPitchShifter](/docs/reference/engine/classes/AudioPitchShifter) that the [Wire](/docs/reference/engine/classes/Wire) targets. |
| wire:[Wire](/docs/reference/engine/classes/Wire)  The [Wire](/docs/reference/engine/classes/Wire) between the [AudioPitchShifter](/docs/reference/engine/classes/AudioPitchShifter) and the other instance. |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The other instance that is or was connected through the [Wire](/docs/reference/engine/classes/Wire). |

Event that fires after a [Wire](/docs/reference/engine/classes/Wire) becomes connected or disconnected,
and that [Wire](/docs/reference/engine/classes/Wire) is now or was previously connected to a pin on the
[AudioPitchShifter](/docs/reference/engine/classes/AudioPitchShifter) and to some other wirable instance.

Provide feedback

---