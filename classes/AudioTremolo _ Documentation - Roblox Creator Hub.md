# AudioTremolo | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AudioTremolo
Scraped: 2026-01-11T02:34:25.187516Z

## Inherits
- Object
- Instance
- AudioTremolo
- Wire
- Wires
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AudioTremolo](/docs/reference/engine/classes/AudioTremolo)

English

Feedback

Engine Class

![AudioTremolo](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AudioTremolo-Dark.webp)AudioTremolo

Creates a trembling effect on a sound by varying the volume of the sound up
and down.

---

Summary

Properties

|  |
| --- |
| [Bypass](#Bypass):[boolean](/docs/luau/booleans) |
| [Depth](#Depth):[number](/docs/luau/numbers) |
| [Duty](#Duty):[number](/docs/luau/numbers) |
| [Frequency](#Frequency):[number](/docs/luau/numbers) |
| [Shape](#Shape):[number](/docs/luau/numbers) |
| [Skew](#Skew):[number](/docs/luau/numbers) |
| [Square](#Square):[number](/docs/luau/numbers) |

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

[AudioTremolo](/docs/reference/engine/classes/AudioTremolo) creates a trembling effect on a sound by varying the
volume of the sound up and down. It provides one Input pin and one
Output pin which can be connected to/from by [Wires](/docs/reference/engine/classes/Wire).

---

API Reference

Properties

Bypass

Read Parallel

AudioTremolo.Bypass:[boolean](/docs/luau/booleans)

Provide feedback

---

Depth

Read Parallel

Controls how much the volume will raise and lower.

AudioTremolo.Depth:[number](/docs/luau/numbers)

Controls how much the volume will raise and lower, ranging between 0 and
1 with a default of 1. If set to 0, the volume will not oscillate at
all.

Provide feedback

---

Duty

Read Parallel

Controls how long the effect will be active during one volume oscillation.

AudioTremolo.Duty:[number](/docs/luau/numbers)

Controls how long the effect will be active during one volume oscillation
in the range of 0 (0%) to 1 (100%). Default is 0.5.

Provide feedback

---

Frequency

Read Parallel

Sets how often the effect will oscillate the volume.

AudioTremolo.Frequency:[number](/docs/luau/numbers)

Sets how often the effect will oscillate the volume, measured in Hz, in
the range of 0.1 to 20. Default is 5.

Provide feedback

---

Shape

Read Parallel

Controls the shape of the low frequency oscillations.

AudioTremolo.Shape:[number](/docs/luau/numbers)

Morphs the LFO (low frequency oscillation) shape in a range of 0 to 1
where 0 is triangle and 1 is sine. Default is 0.

Provide feedback

---

Skew

Read Parallel

Time-skews the low frequency oscillations cycle.

AudioTremolo.Skew:[number](/docs/luau/numbers)

Controls the time-skewing of the LFO (low frequency oscillation) cycle in
the range of -1 to 1. No skewing occurs at 0, with more extremal
forwards and backwards skewing towards +1/-1. Default is 0.

Provide feedback

---

Square

Read Parallel

Flatness of the low frequency oscillations shape.

AudioTremolo.Square:[number](/docs/luau/numbers)

Determines the squareness of the oscillations in the range of 0 to 1.
The original shape is retained when 0 and the shape flattens more as the
value increases. Default is 0.

Provide feedback

---

Methods

GetConnectedWires

AudioTremolo:GetConnectedWires(pin:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| pin:[string](/docs/luau/strings) |

Returns

Instances

Provide feedback

---

GetInputPins

AudioTremolo:GetInputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetOutputPins

AudioTremolo:GetOutputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

Events

WiringChanged

AudioTremolo.WiringChanged(

connected:[boolean](/docs/luau/booleans), pin:[string](/docs/luau/strings), wire:[Wire](/docs/reference/engine/classes/Wire), instance:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| connected:[boolean](/docs/luau/booleans) |
| pin:[string](/docs/luau/strings) |
| wire:[Wire](/docs/reference/engine/classes/Wire) |
| instance:[Instance](/docs/reference/engine/datatypes/Instance) |

Provide feedback

---