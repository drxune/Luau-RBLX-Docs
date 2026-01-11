# AudioChorus | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AudioChorus
Scraped: 2026-01-11T02:32:10.208623Z

## Inherits
- Object
- Instance
- AudioChorus
- Wire
- Wires
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AudioChorus](/docs/reference/engine/classes/AudioChorus)

English

Feedback

Engine Class

![AudioChorus](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AudioChorus-Dark.webp)AudioChorus

Makes an audio stream sound more voluminous. If applied to a single voice, it
may sound like multiple voices.

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

[AudioChorus](/docs/reference/engine/classes/AudioChorus) makes an audio stream sound more voluminous. It provides
one Input pin and one Output pin which can be connected to/from by
[Wires](/docs/reference/engine/classes/Wire).

[AudioChorus](/docs/reference/engine/classes/AudioChorus) is implemented by duplicating the input stream and
modulating the pitch of several delayed copies so that the overall result
sounds like a cloud of streams. If applied to a single voice, it may sound
like multiple voices.

---

API Reference

Properties

Bypass

Read Parallel

Whether audio streams are passed-through unaffected by this effect.

AudioChorus.Bypass:[boolean](/docs/luau/booleans)

If true, audio streams are passed-through unaffected by this effect.

Provide feedback

---

Depth

Read Parallel

Controls the maximum delay time of the copied streams in the chorus
effect.

AudioChorus.Depth:[number](/docs/luau/numbers)

Controls how strong the chorus effect is by changing the maximum delay
time of the copy streams. Ranges from 0 to 1 which corresponds to 0 to 100
milliseconds of maximum delay.

Provide feedback

---

Mix

Read Parallel

Controls the balance of plain input stream to modified output stream.

AudioChorus.Mix:[number](/docs/luau/numbers)

Controls the balance of plain input stream to modified output stream.
Ranges from 0 to 1.

Provide feedback

---

Rate

Read Parallel

Controls the rate of pitch modulations.

AudioChorus.Rate:[number](/docs/luau/numbers)

Frequency controlling the rate of pitch modulations, in hertz. Ranges from
0 to 20.

Provide feedback

---

Methods

GetConnectedWires

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin.

AudioChorus:GetConnectedWires(pin:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| pin:[string](/docs/luau/strings) |

Returns

Instances

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin. [AudioChorus](/docs/reference/engine/classes/AudioChorus) has one "Input" pin and one "Output" pin.

Provide feedback

---

GetInputPins

AudioChorus:GetInputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetOutputPins

AudioChorus:GetOutputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

Events

WiringChanged

Fires when another instance is connected to or disconnected from the
[AudioChorus](/docs/reference/engine/classes/AudioChorus) via a [Wire](/docs/reference/engine/classes/Wire).

AudioChorus.WiringChanged(

connected:[boolean](/docs/luau/booleans), pin:[string](/docs/luau/strings), wire:[Wire](/docs/reference/engine/classes/Wire), instance:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| connected:[boolean](/docs/luau/booleans)  Whether the instance got connected or disconnected. |
| pin:[string](/docs/luau/strings)  The pin on the [AudioChorus](/docs/reference/engine/classes/AudioChorus) that the [Wire](/docs/reference/engine/classes/Wire) targets. |
| wire:[Wire](/docs/reference/engine/classes/Wire)  The [Wire](/docs/reference/engine/classes/Wire) between the [AudioChorus](/docs/reference/engine/classes/AudioChorus) and the other instance. |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The other instance that is or was connected through the [Wire](/docs/reference/engine/classes/Wire). |

Event that fires after a [Wire](/docs/reference/engine/classes/Wire) becomes connected or disconnected,
and that [Wire](/docs/reference/engine/classes/Wire) is now or was previously connected to a pin on the
[AudioChorus](/docs/reference/engine/classes/AudioChorus) and to some other wirable instance.

Provide feedback

---