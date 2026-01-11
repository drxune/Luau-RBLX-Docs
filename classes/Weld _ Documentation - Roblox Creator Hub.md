# Weld | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Weld
Scraped: 2026-01-11T02:35:29.517271Z

## Inherits
- JointInstance
- Weld
- Instance
- Object
- BasePart
- Part1
- C0
- C1
- RigidConstraint
- Attachments
- Constraint.Attachment0
- Constraint.Attachment1
- Active
- BasePart:GetRootPart()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [JointInstance](/docs/reference/engine/classes/JointInstance)
6. /
7. [Weld](/docs/reference/engine/classes/Weld)

English

Feedback

Engine Class

![Weld](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Weld-Dark.webp)Weld

---

Summary

Inherited Members

7 inherited from [JointInstance](/docs/reference/engine/classes/JointInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An object used to hold two objects together in a relative position, regardless
of whether they're touching. This object is placed inside of a
[BasePart](/docs/reference/engine/classes/BasePart) and the [Part1](/docs/reference/engine/classes/JointInstance#Part1) property determines
which other part should be welded to the original part. Two
[CFrames](/docs/reference/engine/datatypes/CFrame), [C0](/docs/reference/engine/classes/JointInstance#C0) and
[C1](/docs/reference/engine/classes/JointInstance#C1), then determine how the parts should be placed.

See also [RigidConstraint](/docs/reference/engine/classes/RigidConstraint) for a newer alternative using the constraints
system that does not require [C0](/docs/reference/engine/classes/JointInstance#C0) or
[C1](/docs/reference/engine/classes/JointInstance#C1), but instead uses [Attachments](/docs/reference/engine/classes/Attachment)
to control offsets through [Constraint.Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) and
[Constraint.Attachment1](/docs/reference/engine/classes/Constraint#Attachment1).

While the weld is [Active](/docs/reference/engine/classes/JointInstance#Active), it maintains the part
positions such that:

part1.CFrame \* C1 == Part0.CFrame \* C0

#### Root Part

Every assembly has a root part (see [BasePart:GetRootPart()](/docs/reference/engine/classes/BasePart#GetRootPart)). When a
weld's [C0](/docs/reference/engine/classes/JointInstance#C0)/[C1](/docs/reference/engine/classes/JointInstance#C1) is modified,
the root part will stay where it was.

#### Directionality

Welds do not have any directionality. Imagine rigid joints forming a tree,
branching up from the root part such that all the parts up the tree from the
root will move and their welded "children" will move with them.