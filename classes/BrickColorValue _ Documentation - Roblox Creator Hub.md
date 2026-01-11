# BrickColorValue | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BrickColorValue
Scraped: 2026-01-11T02:28:42.081688Z

## Inherits
- ValueBase
- BrickColorValue
- Instance
- Object
- BrickColorValue.Value
- NumberValue
- StringValue
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [ValueBase](/docs/reference/engine/classes/ValueBase)
6. /
7. [BrickColorValue](/docs/reference/engine/classes/BrickColorValue)

English

Feedback

Engine Class

![BrickColorValue](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/BrickColorValue-Dark.webp)BrickColorValue

A container object for a single BrickColor value.

---

Summary

Properties

|  |
| --- |
| [Value](#Value):[BrickColor](/docs/reference/engine/datatypes/BrickColor) |

Events

|  |
| --- |
| [Changed](#Changed)(value: [BrickColor](/docs/reference/engine/datatypes/BrickColor)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [changed](#changed)(value: [BrickColor](/docs/reference/engine/datatypes/BrickColor)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An instance which is used to store a BrickColor value.

---

API Reference

Properties

Value

Read Parallel

Used to hold a [BrickColor](/docs/reference/engine/datatypes/BrickColor) value.

BrickColorValue.Value:[BrickColor](/docs/reference/engine/datatypes/BrickColor)

Used to hold a [BrickColor](/docs/reference/engine/datatypes/BrickColor) value.

Provide feedback

---

Events

Changed

Fired whenever the [BrickColorValue.Value](/docs/reference/engine/classes/BrickColorValue#Value) of the BrickColorValue is
changed.

BrickColorValue.Changed(value:[BrickColor](/docs/reference/engine/datatypes/BrickColor)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| value:[BrickColor](/docs/reference/engine/datatypes/BrickColor)  The new value after the change. |

Fired whenever the [BrickColorValue.Value](/docs/reference/engine/classes/BrickColorValue#Value) of the
[BrickColorValue](/docs/reference/engine/classes/BrickColorValue) is changed. It will run with the new value being
stored in the argument object, instead of a string representing the
property being changed.

This event, like other changed events, can be used to track when an
BrickColorValue changes and to track the different values that it may
change to.

Equivalent changed events exist for similar objects, such as
[NumberValue](/docs/reference/engine/classes/NumberValue) and [StringValue](/docs/reference/engine/classes/StringValue), depending on what object type
best suits the need.

Code Samples

BrickColorValue.Changed

This example prints the BrickColorValue's new value each time it changes.

```
local brickColorValue = script.Parent.BrickColorValue



brickColorValue.Changed:Connect(print)



brickColorValue.Value = BrickColor.new("Bright red")
```

Provide feedback

---

changed

Deprecated

Show details

---