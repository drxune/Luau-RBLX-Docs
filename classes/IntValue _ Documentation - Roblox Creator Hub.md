# IntValue | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/IntValue
Scraped: 2026-01-11T02:37:32.505076Z

## Inherits
- ValueBase
- IntValue
- Instance
- Object
- NumberValue
- Value
- IntValue.Value
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [ValueBase](/docs/reference/engine/classes/ValueBase)
6. /
7. [IntValue](/docs/reference/engine/classes/IntValue)

English

Feedback

Engine Class

IntValue

A container object for a single integer.

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

Stores a single signed [64-bit integer](/docs/luau/numbers#int64). The
highest allowed value is 2^63-1 or around 9.2 quintillion (9.2^18). Attempting
to store larger numbers causes an
[integer overflow](https://en.wikipedia.org/wiki/Integer_overflow). The lowest
allowed value is -2^63. Practically, however, working with integers larger
than 2^53 (9^15) causes loss of precision since Luau uses double-precision
floating-point to store numbers.

It's possible to store values between 2^53 and 2^63-1 using the
[Properties](/docs/studio/properties) window since it uses strings to
pass data to the engine, but manipulating large values via Luau scripts
results in loss of precision and rounding as mentioned above.

The main advantage of using IntValue lies in its rounding of values to the
nearest integer, with halfway cases rounded away from 0. For values outside of
this range, use [NumberValue](/docs/reference/engine/classes/NumberValue) instead.

Like all [ValueBase](/docs/reference/engine/classes/ValueBase) objects, this single value is stored in the
[Value](/docs/reference/engine/classes/IntValue#Value) property. The Changed event fires with the new
value being stored in the object, instead of a string representing the
property being changed.

---

API Reference

Properties

Value

Read Parallel

Used to hold an integer.

IntValue.Value:[number](/docs/luau/numbers)

Used to hold an integer.

Provide feedback

---

Events

Changed

Fires whenever the [IntValue.Value](/docs/reference/engine/classes/IntValue#Value) is changed.

IntValue.Changed(value:[number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| value:[number](/docs/luau/numbers)  The new value after the change. |

Fires whenever the [IntValue.Value](/docs/reference/engine/classes/IntValue#Value) changes. It runs with the new
value being stored in the argument object, instead of a string
representing the property being changed.

Listening for the Changed signal can be useful in games that use
IntValues to track values like leaderboard statistics or item prices.

Code Samples

How to Use IntValue.Changed

The below example, assuming all referenced objects existed, would print the
IntValue's new value each time it changed. In the example below it would
print 20.

```
local value = Instance.new("IntValue")



value.Parent = workspace



local function onValueChanged(newValue)



print(newValue)



end



value.Changed:Connect(onValueChanged)



value.Value = 20
```

Provide feedback

---

changed

Deprecated

Show details

---