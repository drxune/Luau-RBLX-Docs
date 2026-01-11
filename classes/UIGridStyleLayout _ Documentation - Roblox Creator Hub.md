# UIGridStyleLayout | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/UIGridStyleLayout
Scraped: 2026-01-11T02:29:08.340705Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- UILayout
- UIGridStyleLayout
- Instance
- Object
- UIGridLayout
- UIListLayout
- UIPageLayout
- UITableLayout
- Frames
- Object.Changed
- GuiObject.LayoutOrder
- UIGridStyleLayout.SortOrder
- TextLabel.TextXAlignment
- TextLabel.Text
- LayoutOrder
- Instance.Name
- TextLabel.TextYAlignment
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [UILayout](/docs/reference/engine/classes/UILayout)
6. /
7. [UIGridStyleLayout](/docs/reference/engine/classes/UIGridStyleLayout)

English

Feedback

Engine Class

UIGridStyleLayout

The base class for grid style UI layouts.

Not Creatable

Not Browsable

---

Summary

Properties

|  |
| --- |
| [AbsoluteContentSize](#AbsoluteContentSize):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [FillDirection](#FillDirection):[Enum.FillDirection](/docs/reference/engine/enums/FillDirection) |
| [HorizontalAlignment](#HorizontalAlignment):[Enum.HorizontalAlignment](/docs/reference/engine/enums/HorizontalAlignment) |
| [SortOrder](#SortOrder):[Enum.SortOrder](/docs/reference/engine/enums/SortOrder) |
| [VerticalAlignment](#VerticalAlignment):[Enum.VerticalAlignment](/docs/reference/engine/enums/VerticalAlignment) |

Methods

|  |
| --- |
| [ApplyLayout](#ApplyLayout)():()  Deprecated |
| [SetCustomSortFunction](#SetCustomSortFunction)(function: [function](/docs/luau/functions)):()  Deprecated |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[UIGridLayout](/docs/reference/engine/classes/UIGridLayout), [UIListLayout](/docs/reference/engine/classes/UIListLayout), [UIPageLayout](/docs/reference/engine/classes/UIPageLayout), [UITableLayout](/docs/reference/engine/classes/UITableLayout)

The base class for grid style UI layouts.

---

API Reference

Properties

AbsoluteContentSize

Read Only

Not Replicated

The absolute size of space being taken up by the grid layout.

UIGridStyleLayout.AbsoluteContentSize:[Vector2](/docs/reference/engine/datatypes/Vector2)

The AbsoluteContentSize property of a [UIGridStyleLayout](/docs/reference/engine/classes/UIGridStyleLayout)
reveals how much space the elements of the grid are taking up, including
any padding created by the grid. This property is particularly useful to
size containers of grids such as [Frames](/docs/reference/engine/classes/Frame) to make sure they
aren't any larger than the grid itself.

This property updates as soon as it's read. It will not fire a
[Object.Changed](/docs/reference/engine/classes/Object#Changed) event immediately after the UI has changed, but if
the value is read, it will become current and a [Object.Changed](/docs/reference/engine/classes/Object#Changed)
event will fire on the next render step.

Provide feedback

---

FillDirection

Read Parallel

Determines the axis in which UI objects are laid out.

UIGridStyleLayout.FillDirection:[Enum.FillDirection](/docs/reference/engine/enums/FillDirection)

The FillDirection property determines the axis in which UI elements
are laid out. [Enum.FillDirection.Horizontal](/docs/reference/engine/enums/FillDirection#Horizontal) arranges objects from left
to right, while [Enum.FillDirection.Vertical](/docs/reference/engine/enums/FillDirection#Vertical) arranges objects from top to
bottom. To reverse elements, such as to arrange right to left, you'll need
to reverse the sorting; for example by negating the child UI objects'
[GuiObject.LayoutOrder](/docs/reference/engine/classes/GuiObject#LayoutOrder) values when
[UIGridStyleLayout.SortOrder](/docs/reference/engine/classes/UIGridStyleLayout#SortOrder) is set to
[Enum.SortOrder.LayoutOrder](/docs/reference/engine/enums/SortOrder#LayoutOrder).

![](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/UIListLayout/FillDirection.png)

Provide feedback

---

HorizontalAlignment

Read Parallel

Determines the horizontal alignment of UI elements within the parent
element.

UIGridStyleLayout.HorizontalAlignment:[Enum.HorizontalAlignment](/docs/reference/engine/enums/HorizontalAlignment)

The HorizontalAlignment property determines the X axis alignment
of the grid of UI elements, much like [TextLabel.TextXAlignment](/docs/reference/engine/classes/TextLabel#TextXAlignment)
does with [TextLabel.Text](/docs/reference/engine/classes/TextLabel#Text).

Provide feedback

---

SortOrder

Read Parallel

Determines the order in which child UI objects are placed in a layout.

UIGridStyleLayout.SortOrder:[Enum.SortOrder](/docs/reference/engine/enums/SortOrder)

The SortOrder property determines the order in which child UI objects
are placed in a layout.

For [Enum.SortOrder.LayoutOrder](/docs/reference/engine/enums/SortOrder#LayoutOrder), an ascending sort is used on the
[LayoutOrder](/docs/reference/engine/classes/GuiObject#LayoutOrder) property of child UI objects. If
two children share the same [LayoutOrder](/docs/reference/engine/classes/GuiObject#LayoutOrder),
whichever was added sooner to the parent object takes precedence.

For [Enum.SortOrder.Name](/docs/reference/engine/enums/SortOrder#Name), an alphanumeric sort is used on the
[Instance.Name](/docs/reference/engine/classes/Instance#Name) of the child UI objects.

![](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/UIListLayout/SortOrder.png)

Provide feedback

---

VerticalAlignment

Read Parallel

Determines the vertical alignment of UI elements within the parent
element.

UIGridStyleLayout.VerticalAlignment:[Enum.VerticalAlignment](/docs/reference/engine/enums/VerticalAlignment)

The VerticalAlignment property determines the Y axis alignment of
the grid of UI elements, much like [TextLabel.TextYAlignment](/docs/reference/engine/classes/TextLabel#TextYAlignment) does
with [TextLabel.Text](/docs/reference/engine/classes/TextLabel#Text).

Provide feedback

---

Methods

ApplyLayout

Deprecated

Show details

---

SetCustomSortFunction

Deprecated

Show details

---