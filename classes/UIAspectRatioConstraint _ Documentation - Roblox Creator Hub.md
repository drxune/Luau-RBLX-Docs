# UIAspectRatioConstraint | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/UIAspectRatioConstraint
Scraped: 2026-01-11T02:27:20.270410Z

## Inherits
- UIConstraint
- UIAspectRatioConstraint
- Instance
- Object
- GuiObject
- Frame
- AspectRatio
- ImageLabel
- UIListLayout
- AbsoluteSize
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [UIConstraint](/docs/reference/engine/classes/UIConstraint)
6. /
7. [UIAspectRatioConstraint](/docs/reference/engine/classes/UIAspectRatioConstraint)

English

Feedback

Engine Class

![UIAspectRatioConstraint](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/UIAspectRatioConstraint-Dark.webp)UIAspectRatioConstraint

Ensures the parent UI element maintains a particular aspect ratio.

---

Summary

Properties

|  |
| --- |
| [AspectRatio](#AspectRatio):[number](/docs/luau/numbers) |
| [AspectType](#AspectType):[Enum.AspectType](/docs/reference/engine/enums/AspectType) |
| [DominantAxis](#DominantAxis):[Enum.DominantAxis](/docs/reference/engine/enums/DominantAxis) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The [UIAspectRatioConstraint](/docs/reference/engine/classes/UIAspectRatioConstraint) enforces a width‑to‑height aspect
ratio on a [GuiObject](/docs/reference/engine/classes/GuiObject) regardless of its core size, even if that size is
set as a percentage of its parent. For example, inserting this constraint as a
child of a [Frame](/docs/reference/engine/classes/Frame) and setting the constraint's
[AspectRatio](/docs/reference/engine/classes/UIAspectRatioConstraint#AspectRatio) property to 2
(2:1) keeps the frame's width at twice that of its height. Similarly,
setting this constraint's
[AspectRatio](/docs/reference/engine/classes/UIAspectRatioConstraint#AspectRatio) property to 0.5
(0.5:1) keeps the frame's width at half that of its height.

Setting this constraint's
[AspectRatio](/docs/reference/engine/classes/UIAspectRatioConstraint#AspectRatio) to the default of 1
(1:1) is a convenient way to prevent non‑proportional scaling/stretching of
an [ImageLabel](/docs/reference/engine/classes/ImageLabel) with a square image asset.

Note that when a UI object is under control of both a layout structure such as
[UIListLayout](/docs/reference/engine/classes/UIListLayout) and a [UIAspectRatioConstraint](/docs/reference/engine/classes/UIAspectRatioConstraint), the constraint
will override the layout and control the object's size.

---

API Reference

Properties

AspectRatio

Read Parallel

Determines the width-to-height ratio to maintain.

UIAspectRatioConstraint.AspectRatio:[number](/docs/luau/numbers)

This property determines the width‑to‑height ratio to maintain. To flip
the ratio to height‑to‑width, take the inverse (divide 1 by the number
or raise to the -1st power). This value must be greater than 0.

Provide feedback

---

AspectType

Read Parallel

Determines how the maximum size of the object is limited.

UIAspectRatioConstraint.AspectType:[Enum.AspectType](/docs/reference/engine/enums/AspectType)

This property determines how the maximum size of the object is limited.

* When set to [FitWithinMaxSize](/docs/reference/engine/enums/AspectType#FitWithinMaxSize), the
  object will be the maximum size possible within its own
  [AbsoluteSize](/docs/reference/engine/classes/GuiBase2d#AbsoluteSize).
* When set to [ScaleWithParentSize](/docs/reference/engine/enums/AspectType#ScaleWithParentSize),
  the object's maximum size will be the size of the parent while still
  maintaining the aspect ratio.

Provide feedback

---

DominantAxis

Read Parallel

Determines the axis to use when setting the new size of the object.

UIAspectRatioConstraint.DominantAxis:[Enum.DominantAxis](/docs/reference/engine/enums/DominantAxis)

This property determines which axis to use when setting the new size of
the object, assuming it would otherwise exceed the size of the parent.

Provide feedback

---