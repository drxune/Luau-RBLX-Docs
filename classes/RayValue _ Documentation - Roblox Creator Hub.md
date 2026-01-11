# RayValue | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/RayValue
Scraped: 2026-01-11T02:31:30.485589Z

## Inherits
- ValueBase
- RayValue
- Instance
- Object
- Workspace
- RayValue.Value
- NumberValue
- StringValue
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [ValueBase](/docs/reference/engine/classes/ValueBase)
6. /
7. [RayValue](/docs/reference/engine/classes/RayValue)

English

Feedback

Engine Class

RayValue

A container object for a single Ray.

---

Summary

Properties

|  |
| --- |
| [Value](#Value):[Ray](/docs/reference/engine/datatypes/Ray) |

Events

|  |
| --- |
| [Changed](#Changed)(value: [Ray](/docs/reference/engine/datatypes/Ray)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [changed](#changed)(value: [Ray](/docs/reference/engine/datatypes/Ray)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A RayValue is an object whose purpose is to store a single Ray. Similar to
CFrameValue, a RayValue's stored ray cannot be viewed or edited within the
Properties window within studio. Instead, use the Command bar to get and set
the value of these objects. For example, you can use a line like the one below
to create a new RayValue named "Value" within the [Workspace](/docs/reference/engine/classes/Workspace). It
creates a ray at (0, 50, 0) and it faces in the positive-X direction.

Instance.new("RayValue").Value = Ray.new(Vector3.new(0, 50, 0), Vector3.new(10, 0, 0))

Since there is no trivial way to edit rays within Studio, sometimes it is
better to use a CFrameValue instead (which can be changed through a part or
the camera). You can reconstruct a ray from a CFrame using
Ray.new(cf.p, cf.lookVector \* dist), where cf is a given CFrame and dist
is the length of the Ray you want to construct.

Like all "-Value" objects, this single value is stored in the Value property.
The Changed event for this (and other objects like it) will fire with the new
value being stored in the object, instead of a string representing the
property being changed.

Code Samples

Rays, RayValue and Raycasting

This code sample demonstrates constructing a Ray, storing the Ray within a
RayValue and Raycasting to find other parts between two parts named "PartA"
and "PartB".

```
local partA = workspace.PartA



local partB = workspace.PartB



local origin = partA.Position



local direction = partB.Position - partA.Position



local ray = Ray.new(origin, direction)



local rayValue = Instance.new("RayValue")



rayValue.Value = ray



rayValue.Name = "PartA-to-PartB Ray"



rayValue.Parent = workspace



-- Raycast to find any parts in between PartA and PartB



local part = workspace:FindPartOnRay(ray)



if part then



print("Hit part: " .. part:GetFullName())



else



-- This ought to never happen, as our ray starts at PartA



-- and points towards PartB, so we should always hit PartB



-- or some other part.



print("No part hit!")



end
```

---

API Reference

Properties

Value

Read Parallel

The stored Ray.

RayValue.Value:[Ray](/docs/reference/engine/datatypes/Ray)

The stored Ray.

Provide feedback

---

Events

Changed

Fired when [RayValue.Value](/docs/reference/engine/classes/RayValue#Value) is changed.

RayValue.Changed(value:[Ray](/docs/reference/engine/datatypes/Ray)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| value:[Ray](/docs/reference/engine/datatypes/Ray)  The value after the change. |

This event fires whenever the [RayValue.Value](/docs/reference/engine/classes/RayValue#Value) property is changed.
It will run with the new value being stored in the argument object,
instead of a string representing the property being changed.

This event, like other changed events, can be used to track when an
RayValue changes and to track the different values that it may change to.

Equivalent changed events exist for similar objects, such as
[NumberValue](/docs/reference/engine/classes/NumberValue) and [StringValue](/docs/reference/engine/classes/StringValue), depending on what object type
best suits the need.

Code Samples

How to Use RayValue.Changed

The below example, assuming all referenced objects existed, would print the
RayValue's new value each time it changed. In the example below it would print
*"{0, 0, 0}, {0.577350199, 0.577350199, 0.577350199}"*.

```
local value = Instance.new("RayValue")



value.Parent = workspace



value.Changed:Connect(function(NewValue)



print(NewValue)



end)



local start = Vector3.new(0, 0, 0)



local lookAt = Vector3.new(10, 10, 10)



local ray = Ray.new(start, (lookAt - start).Unit)



value.Value = ray
```

Provide feedback

---

changed

Deprecated

Show details

---