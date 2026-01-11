# AudioFlanger | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AudioFlanger
Scraped: 2026-01-11T02:31:55.711075Z

## Inherits
- Object
- Instance
- AudioFlanger
- Wire
- Wires
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AudioFlanger](/docs/reference/engine/classes/AudioFlanger)

English

Feedback

Engine Class

![AudioFlanger](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AudioFlanger-Dark.webp)AudioFlanger

Imparts a whooshing or sweeping sound on audio streams.

---

Summary

Properties

|  |
| --- |
| [Bypass](#Bypass):[boolean](/docs/luau/booleans) |
| [Depth](#Depth):[number](/docs/luau/numbers) |
| [Mix](#Mix):[number](/docs/luau/numbers) |
| [Rate](#Rate):[number](/docs/luau/numbers) |

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

[AudioFlanger](/docs/reference/engine/classes/AudioFlanger) imparts a whooshing or sweeping sound on audio streams by
overlaying a delayed copy of the input stream and modulating the pitch of the
copy. It provides one Input pin and one Output pin which can be
connected to/from by [Wires](/docs/reference/engine/classes/Wire).

---

API Reference

Properties

Bypass

Read Parallel

Whether audio streams are passed-through unaffected by this effect.

AudioFlanger.Bypass:[boolean](/docs/luau/booleans)

If true, audio streams are passed-through unaffected by this effect.

Provide feedback

---

Depth

Read Parallel

Controls how strong the pitch modulation of the flanger is.

AudioFlanger.Depth:[number](/docs/luau/numbers)

Controls how strong the pitch modulation of the flanger is. Ranges from 0
to 1 which determines the maximum delay time of the modulated signal. A
value of 1 corresponds to 10 milliseconds of maximum delay; beyond this,
the modulated signal would begin to sound more like an echo than a flange.

Provide feedback

---

Mix

Read Parallel

Controls the balance of plain input stream to modified output stream.

AudioFlanger.Mix:[number](/docs/luau/numbers)

Controls the balance of plain input stream to modified output stream.
Ranges from 0 to 1.

Provide feedback

---

Rate

Read Parallel

Controls the rate of pitch modulations.

AudioFlanger.Rate:[number](/docs/luau/numbers)

Frequency controlling the rate of pitch modulations, in hertz. Ranges from
0 to 20.

Provide feedback

---

Methods

GetConnectedWires

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin.

AudioFlanger:GetConnectedWires(pin:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| pin:[string](/docs/luau/strings) |

Returns

Instances

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin. [AudioFlanger](/docs/reference/engine/classes/AudioFlanger) has one "Input" pin and one "Output" pin.

Provide feedback

---

GetInputPins

AudioFlanger:GetInputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetOutputPins

AudioFlanger:GetOutputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

Events

WiringChanged

Fires when another instance is connected to or disconnected from the
[AudioFlanger](/docs/reference/engine/classes/AudioFlanger) via a [Wire](/docs/reference/engine/classes/Wire).

AudioFlanger.WiringChanged(

connected:[boolean](/docs/luau/booleans), pin:[string](/docs/luau/strings), wire:[Wire](/docs/reference/engine/classes/Wire), instance:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| connected:[boolean](/docs/luau/booleans)  Whether the instance got connected or disconnected. |
| pin:[string](/docs/luau/strings)  The pin on the [AudioFlanger](/docs/reference/engine/classes/AudioFlanger) that the [Wire](/docs/reference/engine/classes/Wire) targets. |
| wire:[Wire](/docs/reference/engine/classes/Wire)  The [Wire](/docs/reference/engine/classes/Wire) between the [AudioFlanger](/docs/reference/engine/classes/AudioFlanger) and the other instance. |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The other instance that is or was connected through the [Wire](/docs/reference/engine/classes/Wire). |

Event that fires after a [Wire](/docs/reference/engine/classes/Wire) becomes connected or disconnected,
and that [Wire](/docs/reference/engine/classes/Wire) is now or was previously connected to a pin on the
[AudioFlanger](/docs/reference/engine/classes/AudioFlanger) and to some other wirable instance.

Provide feedback

---