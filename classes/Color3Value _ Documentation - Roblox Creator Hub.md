# Color3Value | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Color3Value
Scraped: 2026-01-11T02:39:34.412734Z

## Inherits
- ValueBase
- Color3Value
- Instance
- Object
- Color3Value.Value
- NumberValue
- StringValue
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [ValueBase](/docs/reference/engine/classes/ValueBase)
6. /
7. [Color3Value](/docs/reference/engine/classes/Color3Value)

English

Feedback

Engine Class

Color3Value

A container object for a single Color3 value.

---

Summary

Properties

|  |
| --- |
| [Value](#Value):[Color3](/docs/reference/engine/datatypes/Color3) |

Events

|  |
| --- |
| [Changed](#Changed)(value: [Color3](/docs/reference/engine/datatypes/Color3)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [changed](#changed)(value: [Color3](/docs/reference/engine/datatypes/Color3)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A container object for a single [Color3](/docs/reference/engine/datatypes/Color3) value.

Code Samples

Set Color3Value

This code sample sets the Value property of a Color3Value to Red.

```
local myColor3Value = script.Parent



myColor3Value.Value = Color3.new(1, 0, 0) -- Red



-- You can also store the color of a BrickColor value by accessing BrickColor's Color property, which is a Color3:



local someBrickColor = BrickColor.new("Really red")



myColor3Value.Value = someBrickColor.Color
```

---

API Reference

Properties

Value

Read Parallel

The stored [Color3](/docs/reference/engine/datatypes/Color3).

Color3Value.Value:[Color3](/docs/reference/engine/datatypes/Color3)

The stored [Color3](/docs/reference/engine/datatypes/Color3).

Provide feedback

---

Events

Changed

Fired whenever the [Color3Value.Value](/docs/reference/engine/classes/Color3Value#Value) is changed.

Color3Value.Changed(value:[Color3](/docs/reference/engine/datatypes/Color3)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| value:[Color3](/docs/reference/engine/datatypes/Color3)  The new value after the change. |

Fired whenever the [Color3Value.Value](/docs/reference/engine/classes/Color3Value#Value) of the [Color3Value](/docs/reference/engine/classes/Color3Value) is
changed. It will run with the new value being stored in the argument
object, instead of a string representing the property being changed.

This event, like other changed events, can be used to track when an
Color3Value changes and to track the different values that it may change
to.

For instance, this may be useful in games that rely on Color3Values to
track values such as colors for games using customizable outfits or items.

Equivalent changed events exist for similar objects, such as
[NumberValue](/docs/reference/engine/classes/NumberValue) and [StringValue](/docs/reference/engine/classes/StringValue), depending on what object type
best suits the need.

Code Samples

How to Use Color3Value.Changed

The below example, assuming all referenced objects existed, would print the
Color3Value's new value each time it changed. In the example below it would
print *"0.196078, 0.196078, 0.196078"*.

```
local value = Instance.new("Color3Value")



value.Parent = workspace



value.Changed:Connect(function(NewValue)



print(NewValue)



end)



value.Value = Color3.fromRGB(50, 50, 50)
```

Provide feedback

---

changed

Deprecated

Show details

---