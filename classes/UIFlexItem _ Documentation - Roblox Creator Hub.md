# UIFlexItem | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/UIFlexItem
Scraped: 2026-01-11T02:29:36.910756Z

## Inherits
- UIComponent
- UIFlexItem
- GuiObject
- UIListLayout
- Instance
- Object
- GrowRatio
- ShrinkRatio
- FlexMode
- UIListLayout.ItemLineAlignment
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [UIComponent](/docs/reference/engine/classes/UIComponent)
6. /
7. [UIFlexItem](/docs/reference/engine/classes/UIFlexItem)

English

Feedback

Engine Class

![UIFlexItem](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/UIFlexItem-Dark.webp)UIFlexItem

Defines flex behavior for a [GuiObject](/docs/reference/engine/classes/GuiObject) within a [UIListLayout](/docs/reference/engine/classes/UIListLayout).

---

Summary

Properties

|  |
| --- |
| [FlexMode](#FlexMode):[Enum.UIFlexMode](/docs/reference/engine/enums/UIFlexMode) |
| [GrowRatio](#GrowRatio):[number](/docs/luau/numbers) |
| [ItemLineAlignment](#ItemLineAlignment):[Enum.ItemLineAlignment](/docs/reference/engine/enums/ItemLineAlignment) |
| [ShrinkRatio](#ShrinkRatio):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The [UIFlexItem](/docs/reference/engine/classes/UIFlexItem) object defines flex behavior for its parent
[GuiObject](/docs/reference/engine/classes/GuiObject) under the control of a [UIListLayout](/docs/reference/engine/classes/UIListLayout). The defined
flex behavior overrides that of the controlling [UIListLayout](/docs/reference/engine/classes/UIListLayout), letting
you configure flex behavior on a per‑object basis where necessary.

![Example of UIFlexItem applied to a specific GuiObject under control of a UIListLayout.](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/UIFlexItem-Example.png)
![Example hierarchy of a UIFlexItem parented to a GuiObject under control of a UIListLayout.](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/UIFlexItem-Hierarchy.png)

---

API Reference

Properties

FlexMode

Read Parallel

How the parent [GuiObject](/docs/reference/engine/classes/GuiObject) grows or shrinks with available space in
the flex layout container.

UIFlexItem.FlexMode:[Enum.UIFlexMode](/docs/reference/engine/enums/UIFlexMode)

[Enum.UIFlexMode](/docs/reference/engine/enums/UIFlexMode) value which defines how the parent [GuiObject](/docs/reference/engine/classes/GuiObject)
grows or shrinks with available space in the
[flex layout](/docs/ui/list-flex-layouts#flex-layouts) container.

When the container's size is larger than the flex line's combined
basis size, a value of [Enum.UIFlexMode.Grow](/docs/reference/engine/enums/UIFlexMode#Grow) sets an effective 1:0
grow‑shrink ratio on the parent [GuiObject](/docs/reference/engine/classes/GuiObject). Objects set to
[Enum.UIFlexMode.Grow](/docs/reference/engine/enums/UIFlexMode#Grow) never shrink below their basis size, so overflow
may occur if the container becomes smaller than the line's combined basis
size.

![Diagram showing two items in a line with FlexMode set to Grow.](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/UIListLayout/FlexMode-Grow.png)

When the container's size is smaller than the flex line's combined
basis size and the controlling [UIListLayout](/docs/reference/engine/classes/UIListLayout) is not set to wrap
(resulting in overflow), a value of [Enum.UIFlexMode.Shrink](/docs/reference/engine/enums/UIFlexMode#Shrink) sets an
effective 0:1 grow‑shrink ratio on the parent [GuiObject](/docs/reference/engine/classes/GuiObject). Objects
set to [Enum.UIFlexMode.Shrink](/docs/reference/engine/enums/UIFlexMode#Shrink) never grow above their basis size, so
underflow may occur if the container becomes larger than the line's
combined basis size.

![Diagram showing two items in a line with FlexMode set to Shrink.](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/UIListLayout/FlexMode-Shrink.png)

When the container's size is either larger or smaller than the flex line's
combined basis size, a value of [Enum.UIFlexMode.Fill](/docs/reference/engine/enums/UIFlexMode#Fill) sets an effective
1:1 grow‑shrink ratio on the parent [GuiObject](/docs/reference/engine/classes/GuiObject). This setting
ensures the flex line always fills the container, even if the container
size changes.

![Diagram showing two items in a line with FlexMode set to Fill.](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/UIListLayout/FlexMode-Fill.png)

For fine-tuned layouts, a value of [Enum.UIFlexMode.Custom](/docs/reference/engine/enums/UIFlexMode#Custom) enables the
[GrowRatio](/docs/reference/engine/classes/UIFlexItem#GrowRatio) and
[ShrinkRatio](/docs/reference/engine/classes/UIFlexItem#ShrinkRatio) properties, allowing for
relative growth or shrinking of the object in a ratio compared to other
flex objects also under control of a [UIFlexItem](/docs/reference/engine/classes/UIFlexItem).

Provide feedback

---

GrowRatio

Read Parallel

Determines the amount the parent [GuiObject](/docs/reference/engine/classes/GuiObject) grows relative to other
items in the line. Applies only if [FlexMode](/docs/reference/engine/classes/UIFlexItem#FlexMode) is
set to [Enum.UIFlexMode.Custom](/docs/reference/engine/enums/UIFlexMode#Custom).

UIFlexItem.GrowRatio:[number](/docs/luau/numbers)

If there is free space in the flex line, this property determines the
amount the parent [GuiObject](/docs/reference/engine/classes/GuiObject) grows relative to other flex items in
the line. Applies only if [FlexMode](/docs/reference/engine/classes/UIFlexItem#FlexMode) is set to
[Enum.UIFlexMode.Custom](/docs/reference/engine/enums/UIFlexMode#Custom).

Provide feedback

---

ItemLineAlignment

Read Parallel

Cross-axis alignment of the specific parent [GuiObject](/docs/reference/engine/classes/GuiObject) within the
flex line.

UIFlexItem.ItemLineAlignment:[Enum.ItemLineAlignment](/docs/reference/engine/enums/ItemLineAlignment)

Cross-axis alignment of the specific parent [GuiObject](/docs/reference/engine/classes/GuiObject) within the
flex line. See [UIListLayout.ItemLineAlignment](/docs/reference/engine/classes/UIListLayout#ItemLineAlignment) for details.

Provide feedback

---

ShrinkRatio

Read Parallel

Determines the amount the parent [GuiObject](/docs/reference/engine/classes/GuiObject) shrinks relative to
other items in the line. Applies only if
[FlexMode](/docs/reference/engine/classes/UIFlexItem#FlexMode) is set to [Enum.UIFlexMode.Custom](/docs/reference/engine/enums/UIFlexMode#Custom).

UIFlexItem.ShrinkRatio:[number](/docs/luau/numbers)

If there is overflow in the flex line, this property determines the amount
the parent [GuiObject](/docs/reference/engine/classes/GuiObject) shrinks relative to other flex items in the
line. Applies only if [FlexMode](/docs/reference/engine/classes/UIFlexItem#FlexMode) is set to
[Enum.UIFlexMode.Custom](/docs/reference/engine/enums/UIFlexMode#Custom).

Provide feedback

---