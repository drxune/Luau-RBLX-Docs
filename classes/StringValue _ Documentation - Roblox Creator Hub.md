# StringValue | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/StringValue
Scraped: 2026-01-11T02:38:34.490699Z

## Inherits
- ValueBase
- StringValue
- Instance
- Object
- Value
- StringValue.Value
- IntValue.Value
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [ValueBase](/docs/reference/engine/classes/ValueBase)
6. /
7. [StringValue](/docs/reference/engine/classes/StringValue)

English

Feedback

Engine Class

StringValue

A container object for a single string.

---

Summary

Properties

|  |
| --- |
| [Value](#Value):[string](/docs/luau/strings) |

Events

|  |
| --- |
| [Changed](#Changed)(value: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [changed](#changed)(value: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Stores a single [Luau string](https://luau.org/syntax#string-literals). The
length of the string can't be more than 200,000 characters; anything longer
causes a String too long error.

If the string is too long to be displayed in the Value field within the
Properties window, it shows partial string contents and an ellipsis (...).

Like all [ValueBase](/docs/reference/engine/classes/ValueBase) objects, this single value is stored in the
[Value](/docs/reference/engine/classes/StringValue#Value) property. The Changed event fires with the
new value being stored in the object, instead of a string representing the
property being changed.

Code Samples

Changed Event

This sample demonstrates the subtleties of the Changed event on normal objects
and Value objects.

```
-- Demonstrate the Changed event by creating a Part



local part = Instance.new("Part")



part.Changed:Connect(print)



-- This fires Changed with "Transparency"



part.Transparency = 0.5



-- Similarly, this fires Changed with "Number"



part.Name = "SomePart"



-- Since changing BrickColor will also change other



-- properties at the same time, this line fires Changed



-- with "BrickColor", "Color3" and "Color3uint16".



part.BrickColor = BrickColor.Red()



-- A NumberValue holds a double-precision floating-point number



local vNumber = Instance.new("NumberValue")



vNumber.Changed:Connect(print)



-- This fires Changed with 123.456 (not "Value")



vNumber.Value = 123.456



-- This does not fire Changed



vNumber.Name = "SomeNumber"



-- A StringValue stores one string



local vString = Instance.new("StringValue")



vString.Changed:Connect(print)



-- This fires Changed with "Hello" (not "Value")



vString.Value = "Hello"
```

---

API Reference

Properties

Value

Read Parallel

The stored string.

StringValue.Value:[string](/docs/luau/strings)

The stored [string](/docs/luau/strings).

Provide feedback

---

Events

Changed

Fires whenever [StringValue.Value](/docs/reference/engine/classes/StringValue#Value) is changed.

StringValue.Changed(value:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| value:[string](/docs/luau/strings)  The new value after the change. |

Fires whenever the [IntValue.Value](/docs/reference/engine/classes/IntValue#Value) changes. It runs with the new
value being stored in the argument object, instead of a string
representing the property being changed.

Listening for the Changed signal can be useful in games that use
StringValues to track values like NPC names or item descriptions.

Code Samples

How to Use StringValue.Changed

The below example, assuming all referenced objects existed, would print the
StringValue's new value each time it changed. In the example below it would
print *"Hello world!"*.

```
local value = Instance.new("StringValue")



value.Parent = workspace



value.Changed:Connect(function(NewValue)



print(NewValue)



end)



value.Value = "Hello world!"
```

Provide feedback

---

changed

Deprecated

Show details

---