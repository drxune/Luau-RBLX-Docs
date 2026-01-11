# Vector3Value | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Vector3Value
Scraped: 2026-01-11T02:28:23.692719Z

## Inherits
- ValueBase
- Vector3Value
- Instance
- Object
- Vector3Value.Value
- NumberValue
- StringValue
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [ValueBase](/docs/reference/engine/classes/ValueBase)
6. /
7. [Vector3Value](/docs/reference/engine/classes/Vector3Value)

English

Feedback

Engine Class

Vector3Value

A container object for a single Vector3 value.

---

Summary

Properties

|  |
| --- |
| [Value](#Value):[Vector3](/docs/reference/engine/datatypes/Vector3) |

Events

|  |
| --- |
| [Changed](#Changed)(value: [Vector3](/docs/reference/engine/datatypes/Vector3)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [changed](#changed)(value: [Vector3](/docs/reference/engine/datatypes/Vector3)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A Vector3Value simply holds a Vector3 as a value. This value can be used for
scripts to communicate, for objects to move to a preset location, etc.

Code Samples

Teleporter Part

This code sample causes a Part to teleport any players that touch it to a
specific position defined by a "TeleportPosition" Vector3Value.

```
-- Paste me in a Script inside a Part



local part = script.Parent



local teleportPosition = part.TeleportPosition



local function onTouch(otherPart)



-- First, find the HumanoidRootPart. If we can't find it, exit.



local hrp = otherPart.Parent:FindFirstChild("HumanoidRootPart")



if not hrp then



return



end



-- Now teleport by setting the CFrame to one created from



-- the stored TeleportPosition



hrp.CFrame = CFrame.new(teleportPosition.Value)



end



part.Touched:Connect(onTouch)
```

Storing Vector2 inside Vector3Value

This code sample demonstrates how it is possible to store a Vector2 within a
Vector3Value by converting a Vector2 into a Vector3 with a dummy Z value.
Similarly, you can load it by reconstructing the Vector2 from the X and Y
axes.

```
local vector3Value = Instance.new("Vector3Value")



-- Store a Vector2 in a Vector3



local vector2 = Vector2.new(42, 70)



vector3Value.Value = Vector3.new(vector2.X, vector2.Y, 0) -- The Z value is ignored



-- Load a Vector2 from a Vector3



vector2 = Vector2.new(vector3Value.Value.X, vector3Value.Value.Y)



print(vector2)
```

---

API Reference

Properties

Value

Read Parallel

The stored [Vector3](/docs/reference/engine/datatypes/Vector3).

Vector3Value.Value:[Vector3](/docs/reference/engine/datatypes/Vector3)

The stored [Vector3](/docs/reference/engine/datatypes/Vector3).

Provide feedback

---

Events

Changed

Fired whenever [Vector3Value.Value](/docs/reference/engine/classes/Vector3Value#Value) is changed.

Vector3Value.Changed(value:[Vector3](/docs/reference/engine/datatypes/Vector3)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| value:[Vector3](/docs/reference/engine/datatypes/Vector3)  The new value after the change. |

Fired whenever the [Vector3Value.Value](/docs/reference/engine/classes/Vector3Value#Value) of the [Vector3Value](/docs/reference/engine/classes/Vector3Value)
is changed. It will run with the new value being stored in the argument
object, instead of a string representing the property being changed.

This event, like other changed events, can be used to track when an
Vector3Value changes and to track the different values that it may change
to.

For instance, this may be useful in games that rely on Vector3Values to
track positions in the game world.

Equivalent changed events exist for similar objects, such as
[NumberValue](/docs/reference/engine/classes/NumberValue) and [StringValue](/docs/reference/engine/classes/StringValue), depending on what object type
best suits the need.

Code Samples

How to Use Vector3Value.Changed

The below example, assuming all referenced objects existed, would print the
Vector3Value's new value each time it changed. In the example below it would
print *"10,10,10"*.

```
local value = Instance.new("Vector3Value")



value.Parent = workspace



value.Changed:Connect(function(NewValue)



print(NewValue)



end)



value.Value = Vector3.new(10, 10, 10)
```

Provide feedback

---

changed

Deprecated

Show details

---