# RigidConstraint | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/RigidConstraint
Scraped: 2026-01-11T02:38:15.367500Z

## Inherits
- Constraint
- RigidConstraint
- Attachments
- Bones
- Instance
- Object
- WeldConstraint
- BaseParts
- BasePart
- Attachment
- RigidConstraint.Attachment0
- RigidConstraint.Attachment1
- Bone
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Constraint](/docs/reference/engine/classes/Constraint)
6. /
7. [RigidConstraint](/docs/reference/engine/classes/RigidConstraint)

English

Feedback

Engine Class

![RigidConstraint](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/RigidConstraint-Dark.webp)RigidConstraint

Creates a rigid connection between two [Attachments](/docs/reference/engine/classes/Attachment) or
[Bones](/docs/reference/engine/classes/Bone).

---

Summary

Inherited Members

8 inherited from [Constraint](/docs/reference/engine/classes/Constraint)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

RigidConstraint connects two [Attachments](/docs/reference/engine/classes/Attachment) or
[Bones](/docs/reference/engine/classes/Bone) and ensures they stay in the same relative
position/orientation to each other. This flexibility gives it additional
functionality beyond [WeldConstraint](/docs/reference/engine/classes/WeldConstraint), such as attaching accessories to
[Attachments](/docs/reference/engine/classes/Attachment) on a character rig.

The fastest way to create this constraint is by selecting
Rigid Constraint through Studio's Create menu in the toolbar's
Model tab.

Note that this tool behaves differently depending on whether you click on
existing [BaseParts](/docs/reference/engine/classes/BasePart), [Attachments](/docs/reference/engine/classes/Attachment), or
[Bones](/docs/reference/engine/classes/Bone) after the tool is activated:

* Clicking on an existing [BasePart](/docs/reference/engine/classes/BasePart) creates a new [Attachment](/docs/reference/engine/classes/Attachment)
  upon it as the intended [RigidConstraint.Attachment0](/docs/reference/engine/classes/RigidConstraint#Attachment0) or
  [RigidConstraint.Attachment1](/docs/reference/engine/classes/RigidConstraint#Attachment1).
* Clicking on an existing [Attachment](/docs/reference/engine/classes/Attachment) or [Bone](/docs/reference/engine/classes/Bone) uses that
  instance as the intended [RigidConstraint.Attachment0](/docs/reference/engine/classes/RigidConstraint#Attachment0) or
  [RigidConstraint.Attachment1](/docs/reference/engine/classes/RigidConstraint#Attachment1).

Following the second valid click, a new [RigidConstraint](/docs/reference/engine/classes/RigidConstraint) is created to
connect the two new attachments. If either the first or second click is
not made on a [BasePart](/docs/reference/engine/classes/BasePart), [Attachment](/docs/reference/engine/classes/Attachment), or [Bone](/docs/reference/engine/classes/Bone), the
workflow is canceled and no constraint is created.