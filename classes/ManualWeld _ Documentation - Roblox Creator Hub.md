# ManualWeld | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ManualWeld
Scraped: 2026-01-11T02:33:52.013784Z

## Inherits
- ManualSurfaceJointInstance
- ManualWeld
- Weld
- JointInstance
- Instance
- Object
- WeldConstraint
- C0
- C1
- BasePart:GetRootPart()
- Part0
- Part1
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [ManualSurfaceJointInstance](/docs/reference/engine/classes/ManualSurfaceJointInstance)
6. /
7. [ManualWeld](/docs/reference/engine/classes/ManualWeld)

English

Feedback

Engine Class

ManualWeld

Deprecated

Holds two parts together and functions identically to [Weld](/docs/reference/engine/classes/Weld).

---

Summary

Inherited Members

7 inherited from [JointInstance](/docs/reference/engine/classes/JointInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An object that holds two parts together. It is commonly created when the *Join
Always* setting in Studio is turned on.

Functions identically to [Weld](/docs/reference/engine/classes/Weld).

See also [WeldConstraint](/docs/reference/engine/classes/WeldConstraint) for a newer alternative using the
[constraints](/docs/physics/mechanical-constraints) system that does not
require [C0](/docs/reference/engine/classes/JointInstance#C0) or [C1](/docs/reference/engine/classes/JointInstance#C1) properties
to be manually set.

Root part
---------

Every Assembly has a root part, see [BasePart:GetRootPart()](/docs/reference/engine/classes/BasePart#GetRootPart). When a
ManualWeld's [C0](/docs/reference/engine/classes/JointInstance#C0)/[C1](/docs/reference/engine/classes/JointInstance#C1) is
modified the root part will stay where it was.

Directionality
--------------

ManualWelds do not have any directionality. [Part0](/docs/reference/engine/classes/JointInstance#Part0)
or [Part1](/docs/reference/engine/classes/JointInstance#Part1), doesn't matter. You can imagine rigid
joints forming a tree branching down from the root part. All the parts down
the tree from root will move, and their welded "children" in this tree will
move with them.