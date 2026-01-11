# NoCollisionConstraint | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/NoCollisionConstraint
Scraped: 2026-01-11T02:30:49.077866Z

## Inherits
- Instance
- NoCollisionConstraint
- BasePart
- Object
- Attachments
- BaseParts
- Part0
- Part1
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [NoCollisionConstraint](/docs/reference/engine/classes/NoCollisionConstraint)

English

Feedback

Engine Class

![NoCollisionConstraint](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/NoCollisionConstraint-Dark.webp)NoCollisionConstraint

An instance used to prevent collisions between two specific parts.

---

Summary

Properties

|  |
| --- |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [Part0](#Part0):[BasePart](/docs/reference/engine/classes/BasePart) |
| [Part1](#Part1):[BasePart](/docs/reference/engine/classes/BasePart) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The NoCollisionConstraint prevents collisions between two specific parts,
but those parts may still register collisions with the rest of the world.
Compared to
[collision groups](/docs/workspace/collisions#collision-filtering), it
provides a direct way to disable specific collisions, such as the wheel of a
car scraping against the car's body.

The most common way to create this constraint is by selecting
No Collision through Studio's Create menu in the toolbar's
Model tab.

Unlike most constraints, [NoCollisionConstraint](/docs/reference/engine/classes/NoCollisionConstraint) does not utilize any
[Attachments](/docs/reference/engine/classes/Attachment). Note that the tool acts differently based on
how many parts are selected when the tool is activated:

| Option | Tool Behavior |
| --- | --- |
| No parts selected | The next two parts that are clicked will be linked together. If the same part is clicked twice, no link will be created. |
| One part selected | The next part that is clicked will be linked to the selected part. |
| Two parts selected | Both selected parts will be linked together. |

---

API Reference

Properties

Enabled

Read Parallel

Determines whether the two linked [BaseParts](/docs/reference/engine/classes/BasePart) will collide
with each other.

NoCollisionConstraint.Enabled:[boolean](/docs/luau/booleans)

This property determines whether the two linked parts,
[Part0](/docs/reference/engine/classes/NoCollisionConstraint#Part0) and
[Part1](/docs/reference/engine/classes/NoCollisionConstraint#Part1), will collide with each other.

Provide feedback

---

Part0

Read Parallel

The second [BasePart](/docs/reference/engine/classes/BasePart) that the constraint connects.

NoCollisionConstraint.Part0:[BasePart](/docs/reference/engine/classes/BasePart)

The second [BasePart](/docs/reference/engine/classes/BasePart) that the constraint connects.

Provide feedback

---

Part1

Read Parallel

The first [BasePart](/docs/reference/engine/classes/BasePart) that the constraint connects.

NoCollisionConstraint.Part1:[BasePart](/docs/reference/engine/classes/BasePart)

The first [BasePart](/docs/reference/engine/classes/BasePart) that the constraint connects.

Provide feedback

---