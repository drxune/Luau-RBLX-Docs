# UISizeConstraint | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/UISizeConstraint
Scraped: 2026-01-11T02:40:11.290067Z

## Inherits
- UIConstraint
- UISizeConstraint
- GuiObject
- Instance
- Object
- MaxSize
- MinSize
- UILayout
- UIGridLayout
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [UIConstraint](/docs/reference/engine/classes/UIConstraint)
6. /
7. [UISizeConstraint](/docs/reference/engine/classes/UISizeConstraint)

English

Feedback

Engine Class

![UISizeConstraint](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/UISizeConstraint-Dark.webp)UISizeConstraint

Ensures a [GuiObject](/docs/reference/engine/classes/GuiObject) does not become larger or smaller than the
constraint's maximum size or minimum size.

---

Summary

Properties

|  |
| --- |
| [MaxSize](#MaxSize):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [MinSize](#MinSize):[Vector2](/docs/reference/engine/datatypes/Vector2) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The [UISizeConstraint](/docs/reference/engine/classes/UISizeConstraint) ensures a [GuiObject](/docs/reference/engine/classes/GuiObject) does not become
larger or smaller than the [MaxSize](/docs/reference/engine/classes/UISizeConstraint#MaxSize) and
[MinSize](/docs/reference/engine/classes/UISizeConstraint#MinSize). For example, if
[MaxSize](/docs/reference/engine/classes/UISizeConstraint#MaxSize) is set to
(200, 200) and
[MinSize](/docs/reference/engine/classes/UISizeConstraint#MinSize) to (100, 100), the constrained object cannot scale to be
larger than 200×200 pixels or smaller than 100×100 pixels.

Note that if the object with this constraint is also under the control of a
[UILayout](/docs/reference/engine/classes/UILayout) such as [UIGridLayout](/docs/reference/engine/classes/UIGridLayout), the constraint determines
the object's minimum/maximum size and overwrites any size the layout would
apply.

---

API Reference

Properties

MaxSize

Read Parallel

The largest size, in pixels, the parent object is allowed to be.

UISizeConstraint.MaxSize:[Vector2](/docs/reference/engine/datatypes/Vector2)

The largest size, in pixels, the parent object is allowed to be. The X
and Y of this value must be greater than or equal to the corresponding
components of [MinSize](/docs/reference/engine/classes/UISizeConstraint#MinSize).

Provide feedback

---

MinSize

Read Parallel

The smallest size, in pixels, the object is allowed to be.

UISizeConstraint.MinSize:[Vector2](/docs/reference/engine/datatypes/Vector2)

The smallest size, in pixels, the object is allowed to be. The X and
Y of this value must be less than or equal to the corresponding
components of [MaxSize](/docs/reference/engine/classes/UISizeConstraint#MaxSize).

Provide feedback

---