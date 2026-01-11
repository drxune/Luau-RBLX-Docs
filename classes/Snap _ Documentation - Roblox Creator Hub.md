# Snap | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Snap
Scraped: 2026-01-11T02:36:09.441463Z

## Inherits
- JointInstance
- Snap
- Weld
- Instance
- Object
- BasePart:MakeJoints()
- WeldConstraint
- C0
- C1
- BasePart:GetRootPart()
- Part0
- Part1
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [JointInstance](/docs/reference/engine/classes/JointInstance)
6. /
7. [Snap](/docs/reference/engine/classes/Snap)

English

Feedback

Engine Class

![Snap](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Snap-Dark.webp)Snap

Deprecated

Holds two parts together and functions identically to [Weld](/docs/reference/engine/classes/Weld).

---

Summary

Inherited Members

7 inherited from [JointInstance](/docs/reference/engine/classes/JointInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An object that holds two objects rigidly together. Most commonly created when
[BasePart:MakeJoints()](/docs/reference/engine/classes/BasePart#MakeJoints) is called on parts where Inlet and Stud
[Enum.SurfaceType](/docs/reference/engine/enums/SurfaceType) are touching.

Functionally identical to [Weld](/docs/reference/engine/classes/Weld).

See also [WeldConstraint](/docs/reference/engine/classes/WeldConstraint) for a newer alternative using the
[constraints](/docs/physics/mechanical-constraints) system that does not
require [C0](/docs/reference/engine/classes/JointInstance#C0) or [C1](/docs/reference/engine/classes/JointInstance#C1) properties
to be manually set.

Root part
---------

Every Assembly has a root part, see [BasePart:GetRootPart()](/docs/reference/engine/classes/BasePart#GetRootPart). When a
Snap's [C0](/docs/reference/engine/classes/JointInstance#C0)/[C1](/docs/reference/engine/classes/JointInstance#C1) is modified the
root part will stay where it was.

Directionality
--------------

Snaps do not have any directionality. [Part0](/docs/reference/engine/classes/JointInstance#Part0) or
[Part1](/docs/reference/engine/classes/JointInstance#Part1), doesn't matter. You can imagine rigid
joints forming a tree branching down from the root part. All the parts down
the tree from root will move, and their welded "children" in this tree will
move with them.