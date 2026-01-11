# BoolValue | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BoolValue
Scraped: 2026-01-11T02:39:10.865678Z

## Inherits
- ValueBase
- BoolValue
- Instance
- Object
- Value
- BoolValue.Value
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [ValueBase](/docs/reference/engine/classes/ValueBase)
6. /
7. [BoolValue](/docs/reference/engine/classes/BoolValue)

English

Feedback

Engine Class

![BoolValue](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/BoolValue-Dark.webp)BoolValue

A container object for a single boolean value.

---

Summary

Properties

|  |
| --- |
| [Value](#Value):[boolean](/docs/luau/booleans) |

Events

|  |
| --- |
| [Changed](#Changed)(value: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [changed](#changed)(value: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Stores a single boolean value. The value can be used for many things,
including to communicate between scripts.

Like all [ValueBase](/docs/reference/engine/classes/ValueBase) objects, this single value is stored in the
[Value](/docs/reference/engine/classes/BoolValue#Value) property. The Changed event fires with the new
value being stored in the object, instead of a string representing the
property being changed.

---

API Reference

Properties

Value

Read Parallel

Used to hold a boolean value.

BoolValue.Value:[boolean](/docs/luau/booleans)

Used to hold a boolean value.

Provide feedback

---

Events

Changed

Fires whenever the [BoolValue.Value](/docs/reference/engine/classes/BoolValue#Value) is changed.

BoolValue.Changed(value:[boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| value:[boolean](/docs/luau/booleans)  The new value after the change. |

Fires whenever the [BoolValue.Value](/docs/reference/engine/classes/BoolValue#Value) changes. It runs with the new
value being stored in the argument object, instead of a string
representing the property being changed.

Listening for the Changed signal can be useful in games that use
BoolValues to track switch or enabled states.

Code Samples

BoolValue.Changed

This example prints the BoolValue's new value each time it changes.

```
local boolValue = script.Parent.BoolValue



local function printValue(value)



print(value)



end



boolValue.Changed:Connect(printValue)



boolValue.Value = true
```

Provide feedback

---

changed

Deprecated

Show details

---