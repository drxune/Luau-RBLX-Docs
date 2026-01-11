# BinaryStringValue | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BinaryStringValue
Scraped: 2026-01-11T02:29:38.219248Z

## Inherits
- ValueBase
- BinaryStringValue
- StringValue
- Instance
- Object
- BinaryStringValue.Value
- NumberValue
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [ValueBase](/docs/reference/engine/classes/ValueBase)
6. /
7. [BinaryStringValue](/docs/reference/engine/classes/BinaryStringValue)

English

Feedback

Engine Class

BinaryStringValue

An internal type of [StringValue](/docs/reference/engine/classes/StringValue) object, that stores a BinaryString
value.

---

Summary

Events

|  |
| --- |
| [Changed](#Changed)(value: BinaryString):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An internal type of [StringValue](/docs/reference/engine/classes/StringValue) object, that stores a BinaryString
value.

---

API Reference

Events

Changed

Fires if the BinaryStringValue's value is changed.

BinaryStringValue.Changed(value:BinaryString):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| value:BinaryString  The new value after the change. |

Fires if the [BinaryStringValue.Value](/docs/reference/engine/classes/BinaryStringValue#Value) of the
[BinaryStringValue](/docs/reference/engine/classes/BinaryStringValue) is changed by the engine.

In practice, this object is stored out of reach from normal scripts, so
this event cannot be connected to. If a BinaryStringValue is created by a
script, the engine will not do anything with it, so the event will never
fire.

Equivalent changed events exist for similar objects, such as
[NumberValue](/docs/reference/engine/classes/NumberValue) and [StringValue](/docs/reference/engine/classes/StringValue), depending on what object type
best suits the need.

Provide feedback

---