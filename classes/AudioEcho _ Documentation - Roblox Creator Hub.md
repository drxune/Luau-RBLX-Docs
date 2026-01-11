# AudioEcho | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AudioEcho
Scraped: 2026-01-11T02:31:18.634067Z

## Inherits
- Object
- Instance
- AudioEcho
- Wire
- Wires
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AudioEcho](/docs/reference/engine/classes/AudioEcho)

English

Feedback

Engine Class

![AudioEcho](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AudioEcho-Dark.webp)AudioEcho

Overlays delayed copies of audio streams.

---

Summary

Properties

|  |
| --- |
| [Bypass](#Bypass):[boolean](/docs/luau/booleans) |
| [DelayTime](#DelayTime):[number](/docs/luau/numbers) |
| [DryLevel](#DryLevel):[number](/docs/luau/numbers) |
| [Feedback](#Feedback):[number](/docs/luau/numbers) |
| [RampTime](#RampTime):[number](/docs/luau/numbers) |
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

[AudioEcho](/docs/reference/engine/classes/AudioEcho) overlays delayed copies of audio streams. It provides one
Input pin and one Output pin which can be connected to/from by
[Wires](/docs/reference/engine/classes/Wire).

---

API Reference

Properties

Bypass

Read Parallel

Whether audio streams are passed-through unaffected by this effect.

AudioEcho.Bypass:[boolean](/docs/luau/booleans)

If true, audio streams are passed-through unaffected by this effect.

Provide feedback

---

DelayTime

Read Parallel

The amount of time between echoes.

AudioEcho.DelayTime:[number](/docs/luau/numbers)

The amount of time between echoes, in seconds. Ranges from 0.001 to 5.

Provide feedback

---

DryLevel

Read Parallel

Gain level determining how loud the original, unaltered audio stream will
be.

AudioEcho.DryLevel:[number](/docs/luau/numbers)

Gain level, in decibels, determining how loud the original, unaltered
audio stream will be. Ranges from -80 to 10.

Provide feedback

---

Feedback

Read Parallel

How slowly echoes fade away.

AudioEcho.Feedback:[number](/docs/luau/numbers)

Determines how slowly echoes fade away, with a range of 0 to 1. A value of
0 means that only a single echo is heard, whereas a value of 1 means that
old echoes never fully disappear.

Provide feedback

---

RampTime

Read Parallel

AudioEcho.RampTime:[number](/docs/luau/numbers)

Provide feedback

---

WetLevel

Read Parallel

Gain level determining how loud the echoed stream will be.

AudioEcho.WetLevel:[number](/docs/luau/numbers)

Gain level, in decibels, determining how loud the echoed stream will be.
Ranges from -80 to 10.

Provide feedback

---

Methods

GetConnectedWires

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin.

AudioEcho:GetConnectedWires(pin:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| pin:[string](/docs/luau/strings) |

Returns

Instances

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin. [AudioEcho](/docs/reference/engine/classes/AudioEcho) has one "Input" pin and one "Output" pin.

Provide feedback

---

GetInputPins

AudioEcho:GetInputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetOutputPins

AudioEcho:GetOutputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

Events

WiringChanged

Fires when another instance is connected to or disconnected from the
[AudioEcho](/docs/reference/engine/classes/AudioEcho) via a [Wire](/docs/reference/engine/classes/Wire).

AudioEcho.WiringChanged(

connected:[boolean](/docs/luau/booleans), pin:[string](/docs/luau/strings), wire:[Wire](/docs/reference/engine/classes/Wire), instance:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| connected:[boolean](/docs/luau/booleans)  Whether the instance got connected or disconnected. |
| pin:[string](/docs/luau/strings)  The pin on the [AudioEcho](/docs/reference/engine/classes/AudioEcho) that the [Wire](/docs/reference/engine/classes/Wire) targets. |
| wire:[Wire](/docs/reference/engine/classes/Wire)  The [Wire](/docs/reference/engine/classes/Wire) between the [AudioEcho](/docs/reference/engine/classes/AudioEcho) and the other instance. |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The other instance that is or was connected through the [Wire](/docs/reference/engine/classes/Wire). |

Event that fires after a [Wire](/docs/reference/engine/classes/Wire) becomes connected or disconnected,
and that [Wire](/docs/reference/engine/classes/Wire) is now or was previously connected to a pin on the
[AudioEcho](/docs/reference/engine/classes/AudioEcho) and to some other wirable instance.

Provide feedback

---