# AudioLimiter | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AudioLimiter
Scraped: 2026-01-11T02:29:45.967816Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- AudioLimiter
- Wire
- MaxLevel
- Wires
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AudioLimiter](/docs/reference/engine/classes/AudioLimiter)

English

Feedback

Engine Class

![AudioLimiter](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AudioLimiter-Dark.webp)AudioLimiter

Limits how loud audio streams are allowed to be.

---

Summary

Properties

|  |
| --- |
| [Bypass](#Bypass):[boolean](/docs/luau/booleans) |
| [Editor](#Editor):[boolean](/docs/luau/booleans) |
| [MaxLevel](#MaxLevel):[number](/docs/luau/numbers) |
| [Release](#Release):[number](/docs/luau/numbers) |

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

AudioLimiter limits how loud audio streams are allowed to be. Whenever its
input stream exceeds a specified maximum level, the stream's volume is reduced
for a moment. AudioLimiter provides a single Input pin, and a single
Output pin that can be connected to/from by Class.Wires.

---

API Reference

Properties

Bypass

Read Parallel

Whether audio streams are passed-through unaffected by this effect.

AudioLimiter.Bypass:[boolean](/docs/luau/booleans)

If true, audio streams are passed-through unaffected by this effect.

Provide feedback

---

Editor

Not Replicated

Roblox Script Security

Read Parallel

AudioLimiter.Editor:[boolean](/docs/luau/booleans)

Provide feedback

---

MaxLevel

Read Parallel

The maximum volume tolerated.

AudioLimiter.MaxLevel:[number](/docs/luau/numbers)

The maximum volume, in decibels, that the limiter will allow to pass
through without reduction. Whenever the input stream exceeds
[MaxLevel](/docs/reference/engine/classes/AudioLimiter#MaxLevel), the output stream's volume will be
reduced to compensate. This value ranges from -12 to 0.

Provide feedback

---

Release

Read Parallel

The amount of time it takes for previously limited streams to return to
their normal volume.

AudioLimiter.Release:[number](/docs/luau/numbers)

The amount of time, in seconds, that it takes for any previously (but not
currently) limited streams to return to their normal volume. This value
ranges from 0.001 to 1.

Provide feedback

---

Methods

GetConnectedWires

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin.

AudioLimiter:GetConnectedWires(pin:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| pin:[string](/docs/luau/strings) |

Returns

Instances

Returns an array of [Wires](/docs/reference/engine/classes/Wire) that are connected to the specified
pin. [AudioLimiter](/docs/reference/engine/classes/AudioLimiter) has one Input pin and one Output pin.

Provide feedback

---

GetInputPins

AudioLimiter:GetInputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetOutputPins

AudioLimiter:GetOutputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

Events

WiringChanged

Fires when another instance is connected to or disconnected from the
[AudioLimiter](/docs/reference/engine/classes/AudioLimiter) via a [Wire](/docs/reference/engine/classes/Wire).

AudioLimiter.WiringChanged(

connected:[boolean](/docs/luau/booleans), pin:[string](/docs/luau/strings), wire:[Wire](/docs/reference/engine/classes/Wire), instance:[Instance](/docs/reference/engine/datatypes/Instance)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| connected:[boolean](/docs/luau/booleans)  Whether the instance got connected or disconnected. |
| pin:[string](/docs/luau/strings)  The pin on the [AudioLimiter](/docs/reference/engine/classes/AudioLimiter) that the [Wire](/docs/reference/engine/classes/Wire) targets. |
| wire:[Wire](/docs/reference/engine/classes/Wire)  The [Wire](/docs/reference/engine/classes/Wire) between the [AudioLimiter](/docs/reference/engine/classes/AudioLimiter) and the other instance. |
| instance:[Instance](/docs/reference/engine/datatypes/Instance)  The other instance that is or was connected through the [Wire](/docs/reference/engine/classes/Wire). |

Event that fires after a [Wire](/docs/reference/engine/classes/Wire) becomes connected or disconnected,
and that [Wire](/docs/reference/engine/classes/Wire) is now or was previously connected to a pin on the
[AudioLimiter](/docs/reference/engine/classes/AudioLimiter) and to some other wirable instance.

Provide feedback

---