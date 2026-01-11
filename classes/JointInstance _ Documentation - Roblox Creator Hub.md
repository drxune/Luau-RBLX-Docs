# JointInstance | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/JointInstance
Scraped: 2026-01-11T02:31:44.452628Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- Instance
- JointInstance
- BasePart
- DynamicRotate
- Glue
- ManualSurfaceJointInstance
- Motor
- Rotate
- Welds
- Motors
- Weld
- WeldConstraint
- Motor6D
- BasePart:GetRootPart()
- C0
- C1
- Workspace
- JointsService
- Snap
- JointInstance.Part0
- JointInstance.Part1
- JointInstance.C0
- Snaps
- JointInstance.Active
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [JointInstance](/docs/reference/engine/classes/JointInstance)

English

Feedback

Engine Class

JointInstance

The base class for joints.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [Active](#Active):[boolean](/docs/luau/booleans) |
| [C0](#C0):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [C1](#C1):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [Part0](#Part0):[BasePart](/docs/reference/engine/classes/BasePart) |
| [Part1](#Part1):[BasePart](/docs/reference/engine/classes/BasePart) |
| [part1](#part1):[BasePart](/docs/reference/engine/classes/BasePart)  Deprecated |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[DynamicRotate](/docs/reference/engine/classes/DynamicRotate), [Glue](/docs/reference/engine/classes/Glue), [ManualSurfaceJointInstance](/docs/reference/engine/classes/ManualSurfaceJointInstance), [Motor](/docs/reference/engine/classes/Motor), [Rotate](/docs/reference/engine/classes/Rotate), Show more...

JointInstance is the base class for joints such as [Welds](/docs/reference/engine/classes/Weld) and
[Motors](/docs/reference/engine/classes/Motor).

[Weld](/docs/reference/engine/classes/Weld), [WeldConstraint](/docs/reference/engine/classes/WeldConstraint), [Motor](/docs/reference/engine/classes/Motor), and [Motor6D](/docs/reference/engine/classes/Motor6D) all
combine multiple parts into the same
[assembly](/docs/physics/assemblies). Every assembly has a root part
([BasePart:GetRootPart()](/docs/reference/engine/classes/BasePart#GetRootPart)) and when
[C0](/docs/reference/engine/classes/JointInstance#C0)/[C1](/docs/reference/engine/classes/JointInstance#C1) of a
[JointInstance](/docs/reference/engine/classes/JointInstance) is modified, the root part will stay where it was.

Welds do not have any directionality. You can imagine rigid joints forming a
tree branching down from the root part. All the parts down the tree from root
will move, and their welded "children" in this tree will move with them.

---

API Reference

Properties

Active

Read Only

Not Replicated

Read Parallel

Determines if the joint is currently active in the world.

JointInstance.Active:[boolean](/docs/luau/booleans)

This property determines if the joint is currently active in the world. If
true, the joint is active.

If the [JointInstance](/docs/reference/engine/classes/JointInstance) is not in [Workspace](/docs/reference/engine/classes/Workspace) or
[JointsService](/docs/reference/engine/classes/JointsService), or one of its parts is not in Workspace the joint
will be inactive.

Rigid joints like [Weld](/docs/reference/engine/classes/Weld), [Snap](/docs/reference/engine/classes/Snap), [WeldConstraint](/docs/reference/engine/classes/WeldConstraint),
[Motor](/docs/reference/engine/classes/Motor), or [Motor6D](/docs/reference/engine/classes/Motor6D) may also be disabled due to conflicts
with other rigid joints, such as joints between the same two parts or
indirect cycles in the weld graph. Joints disabled this way may be
re-enabled later when another joint or part is added or removed.

Provide feedback

---

C0

Read Parallel

Determines how the offset point is attached to
[JointInstance.Part0](/docs/reference/engine/classes/JointInstance#Part0).

JointInstance.C0:[CFrame](/docs/reference/engine/datatypes/CFrame)

C0 is the position aspect of the orientation between two parts in a weld.
[JointInstance.Part0](/docs/reference/engine/classes/JointInstance#Part0) and [JointInstance.Part1](/docs/reference/engine/classes/JointInstance#Part1) move
accordingly to this value, which denotes their respective positions.

Provide feedback

---

C1

Read Parallel

Is subtracted from the [JointInstance.C0](/docs/reference/engine/classes/JointInstance#C0) property to create an
offset point for [JointInstance.Part1](/docs/reference/engine/classes/JointInstance#Part1).

JointInstance.C1:[CFrame](/docs/reference/engine/datatypes/CFrame)

Is subtracted from the [JointInstance.C0](/docs/reference/engine/classes/JointInstance#C0) property to create an
offset point for [JointInstance.Part1](/docs/reference/engine/classes/JointInstance#Part1).

Provide feedback

---

Enabled

Read Parallel

Sets whether the joint is active or not.

JointInstance.Enabled:[boolean](/docs/luau/booleans)

This property sets whether the joint is active or not.

When this property is set to true, if the joints's
[JointInstance.Part0](/docs/reference/engine/classes/JointInstance#Part0) and [JointInstance.Part1](/docs/reference/engine/classes/JointInstance#Part1) properties are
set, then the joint will ensure that its two parts will be connected and
behave according to joint type (e.g. [Welds](/docs/reference/engine/classes/Weld), and
[Snaps](/docs/reference/engine/classes/Snap)).

See also:

* [JointInstance.Active](/docs/reference/engine/classes/JointInstance#Active), determines if the joint is currently
  active in the world

Provide feedback

---

Part0

Read Parallel

The first [BasePart](/docs/reference/engine/classes/BasePart) that the joint connects.

JointInstance.Part0:[BasePart](/docs/reference/engine/classes/BasePart)

The first [BasePart](/docs/reference/engine/classes/BasePart) that the joint connects.

Provide feedback

---

Part1

Read Parallel

The second [BasePart](/docs/reference/engine/classes/BasePart) that the joint connects.

JointInstance.Part1:[BasePart](/docs/reference/engine/classes/BasePart)

The second [BasePart](/docs/reference/engine/classes/BasePart) that the joint connects.

Provide feedback

---

part1

Deprecated

Show details

---