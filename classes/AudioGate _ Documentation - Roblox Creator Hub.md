# AudioGate | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AudioGate
Scraped: 2026-01-11T02:27:35.443354Z

## Inherits
- Object
- Instance
- AudioGate
- Wire
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AudioGate](/docs/reference/engine/classes/AudioGate)

English

Feedback

Engine Class

AudioGate

---

Summary

Properties

|  |
| --- |
| [Attack](#Attack):[number](/docs/luau/numbers) |
| [Bypass](#Bypass):[boolean](/docs/luau/booleans) |
| [Release](#Release):[number](/docs/luau/numbers) |
| [Threshold](#Threshold):[NumberRange](/docs/reference/engine/datatypes/NumberRange) |

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

---

API Reference

Properties

Attack

Read Parallel

AudioGate.Attack:[number](/docs/luau/numbers)

Provide feedback

---

Bypass

Read Parallel

AudioGate.Bypass:[boolean](/docs/luau/booleans)

Provide feedback

---

Release

Read Parallel

AudioGate.Release:[number](/docs/luau/numbers)

Provide feedback

---

Threshold

Read Parallel

AudioGate.Threshold:[NumberRange](/docs/reference/engine/datatypes/NumberRange)

Provide feedback

---

Methods

GetConnectedWires

AudioGate:GetConnectedWires(pin:[string](/docs/luau/strings)):Instances

Parameters

|  |
| --- |
| pin:[string](/docs/luau/strings) |

Returns

Instances

Provide feedback

---

GetInputPins

AudioGate:GetInputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

GetOutputPins

AudioGate:GetOutputPins():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

Provide feedback

---

Events

WiringChanged

AudioGate.WiringChanged(

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