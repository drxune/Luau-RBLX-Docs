# NumberValue | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/NumberValue
Scraped: 2026-01-11T02:30:57.254064Z

## Inherits
- ValueBase
- NumberValue
- Instance
- Object
- Value
- NumberValue.Value
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [ValueBase](/docs/reference/engine/classes/ValueBase)
6. /
7. [NumberValue](/docs/reference/engine/classes/NumberValue)

English

Feedback

Engine Class

NumberValue

A container object for a single double-precision floating point number.

---

Summary

Properties

|  |
| --- |
| [Value](#Value):[number](/docs/luau/numbers) |

Events

|  |
| --- |
| [Changed](#Changed)(value: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [changed](#changed)(value: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Store a single [Luau number](https://luau.org/syntax#number-literals), defined
to be
[double-precision floating point number](https://en.wikipedia.org/wiki/Double-precision_floating-point_format),
or more commonly known as a double. This stores a number in 64 bits (8
bytes) using the IEEE 754 representation (1 sign bit, 11 exponent bits and 52
fractional bits). Maximum and minimum values are
±1.7976931348623157e+308, with a range of ±2^53 for exact
integer representations.

Like all [ValueBase](/docs/reference/engine/classes/ValueBase) objects, this single value is stored in the
[Value](/docs/reference/engine/classes/NumberValue#Value) property. The Changed event fires with the
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

Used to hold a double value.

NumberValue.Value:[number](/docs/luau/numbers)

Used to hold a double value.

Provide feedback

---

Events

Changed

Fires whenever the [NumberValue.Value](/docs/reference/engine/classes/NumberValue#Value) is changed.

NumberValue.Changed(value:[number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| value:[number](/docs/luau/numbers)  The new value after the change. |

Fires whenever the [NumberValue.Value](/docs/reference/engine/classes/NumberValue#Value) changes. It runs with the new
value being stored in the argument object, instead of a string
representing the property being changed.

Listening for the Changed signal can be useful in games that use
NumberValues to track values like leaderboard statistics or item prices.

Code Samples

NumberValue Changed

This example prints the new value of the NumberValue each time it changes. Here it prints 20.

```
local numberValue = script.Parent.NumberValue



local function printValue(value)



print(value)



end



numberValue.Changed:Connect(printValue)



numberValue.Value = 20
```

Provide feedback

---

changed

Deprecated

Show details

---