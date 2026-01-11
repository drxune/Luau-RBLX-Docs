# UIGridLayout | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/UIGridLayout
Scraped: 2026-01-11T02:29:12.613537Z

## Tags
- Not Replicated

## Inherits
- UIGridStyleLayout
- UIGridLayout
- Instance
- Object
- GuiObject.Size
- GuiObject.Position
- UIListLayout.SortOrder
- GuiObject.LayoutOrder
- Instance.Name
- UIGridStyleLayout:ApplyLayout()
- UISizeConstraint
- UIAspectRatioConstraint
- MinSize
- CellSize
- UIGridLayout.FillDirectionMaxCells
- UITableLayout
- UIScale
- UIConstraint
- UIGridStyleLayout.FillDirection
- UIListLayout
- UIGridLayout.FIllDirectionMaxCells
- ImageLabel
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [UIGridStyleLayout](/docs/reference/engine/classes/UIGridStyleLayout)
6. /
7. [UIGridLayout](/docs/reference/engine/classes/UIGridLayout)

English

Feedback

Engine Class

![UIGridLayout](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/UIGridLayout-Dark.webp)UIGridLayout

Positions sibling UI elements by filling rows using the space of the parent UI
element.

---

Summary

Properties

|  |
| --- |
| [AbsoluteCellCount](#AbsoluteCellCount):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [AbsoluteCellSize](#AbsoluteCellSize):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [CellPadding](#CellPadding):[UDim2](/docs/reference/engine/datatypes/UDim2) |
| [CellSize](#CellSize):[UDim2](/docs/reference/engine/datatypes/UDim2) |
| [FillDirectionMaxCells](#FillDirectionMaxCells):[number](/docs/luau/numbers) |
| [StartCorner](#StartCorner):[Enum.StartCorner](/docs/reference/engine/enums/StartCorner) |

Inherited Members

7 inherited from [UIGridStyleLayout](/docs/reference/engine/classes/UIGridStyleLayout)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A UIGridLayout (not to be confused with the abstract [UIGridStyleLayout](/docs/reference/engine/classes/UIGridStyleLayout)
from which this class inherits) lays out sibling UI elements in multiple rows
within the parent UI element, adding elements to a row one-by-one until the
next element would not fit. It then continues adding elements in the next row.
A UIGridLayout will take UI elements' [GuiObject.Size](/docs/reference/engine/classes/GuiObject#Size) and
[GuiObject.Position](/docs/reference/engine/classes/GuiObject#Position) under control. While under control, these UI
elements' properties will not be editable in the Properties window.

By default, it lays out elements in ascending order where lower values
take more priority over higher values, but this can be changed to use
elements' names by changing [UIListLayout.SortOrder](/docs/reference/engine/classes/UIListLayout#SortOrder) to Name. A
UIListLayout will automatically re-layout elements when elements are
added/removed, or if a relevant property changes:
[GuiObject.LayoutOrder](/docs/reference/engine/classes/GuiObject#LayoutOrder) or [Instance.Name](/docs/reference/engine/classes/Instance#Name). This can be triggered
manually by calling [UIGridStyleLayout:ApplyLayout()](/docs/reference/engine/classes/UIGridStyleLayout#ApplyLayout), though this is
typically not necessary.

The actual cell sizes are the same for all cells. A UIGridLayout will respect
UI constraints placed with it, such as [UISizeConstraint](/docs/reference/engine/classes/UISizeConstraint) and
[UIAspectRatioConstraint](/docs/reference/engine/classes/UIAspectRatioConstraint). Elements in the layout can span multiple
cells if they have a [UISizeConstraint](/docs/reference/engine/classes/UISizeConstraint) with a
[MinSize](/docs/reference/engine/classes/UISizeConstraint#MinSize) set higher than the
[CellSize](/docs/reference/engine/classes/UIGridLayout#CellSize). It is possible to limit the number of
elements per row using [UIGridLayout.FillDirectionMaxCells](/docs/reference/engine/classes/UIGridLayout#FillDirectionMaxCells). If set to
1, it is possible to create a single row of elements (as each element would be
positioned in its own row).

This layout is appropriate when line breaks are OK after arbitrary cells. For
example, a set of inventory spaces is a good use of this layout. If building a
table of values in which a line break is not appropriate in the middle of
tabular data, it might be a better idea to use a [UITableLayout](/docs/reference/engine/classes/UITableLayout)
instead.

---

API Reference

Properties

AbsoluteCellCount

Read Only

Not Replicated

The number of elements in the grid.

UIGridLayout.AbsoluteCellCount:[Vector2](/docs/reference/engine/datatypes/Vector2)

Measures the maximum number of elements in each direction. Read-only.

Provide feedback

---

AbsoluteCellSize

Read Only

Not Replicated

The absolute size of each element in the grid.

UIGridLayout.AbsoluteCellSize:[Vector2](/docs/reference/engine/datatypes/Vector2)

Provides the size of each element of the grid in offsets. Read-only. Not
affected by any [UIScale](/docs/reference/engine/classes/UIScale), [UISizeConstraint](/docs/reference/engine/classes/UISizeConstraint) or
[UIAspectRatioConstraint](/docs/reference/engine/classes/UIAspectRatioConstraint) applied to any individual element in the
grid.

Provide feedback

---

CellPadding

Read Parallel

Determines how much space there is between elements in the grid.

UIGridLayout.CellPadding:[UDim2](/docs/reference/engine/datatypes/UDim2)

(default {0, 5},{0, 5}) Determines how much space there is between
elements in the grid. As with all UDim2s, this space can be both in a
percentage of the parent container's size and raw pixel offset.

Provide feedback

---

CellSize

Read Parallel

Determines the size of each element in the grid.

UIGridLayout.CellSize:[UDim2](/docs/reference/engine/datatypes/UDim2)

(default {0, 100},{0, 100}) Determines the size of each element in the
grid. As with all UDim2s, this size can be both in a percentage of the
parent container's size and raw pixel offset. If the element being size
has a [UIConstraint](/docs/reference/engine/classes/UIConstraint) then the size will be determined by the
constraint, not the grid.

Provide feedback

---

FillDirectionMaxCells

Read Parallel

Determines the maximum number of cells that may be used in a row or column
before the next one is started.

UIGridLayout.FillDirectionMaxCells:[number](/docs/luau/numbers)

FillDirectionMaxCells determines the number of cells in the grid that can
be used before continuing on the next row/column (whether this is a row or
column is dependent on [UIGridStyleLayout.FillDirection](/docs/reference/engine/classes/UIGridStyleLayout#FillDirection)). This
value must be non-negative.

* If set to zero, there is no maximum number of cells that may appear in
  one row/column except for how many can fit within the parent UI element.
* If set to one, this creates a list similar to those created by
  [UIListLayout](/docs/reference/engine/classes/UIListLayout).

Provide feedback

---

StartCorner

Read Parallel

Determines from which corner the grid starts laying out UI elements.

UIGridLayout.StartCorner:[Enum.StartCorner](/docs/reference/engine/enums/StartCorner)

StartCorner ([Enum.StartCorner](/docs/reference/engine/enums/StartCorner)) determines from which corner the grid
starts laying out UI elements. The grid continues in the
[UIGridStyleLayout.FillDirection](/docs/reference/engine/classes/UIGridStyleLayout#FillDirection), filling elements one by one until
[UIGridLayout.FIllDirectionMaxCells](/docs/reference/engine/classes/UIGridLayout#FIllDirectionMaxCells) cells have been laid out in
that row/column or if all the parent UI element's space has been occupied
by previous cells.

Above, the potion is the first [ImageLabel](/docs/reference/engine/classes/ImageLabel), followed by the gem and
the sword. The UIGridLayout is using a [Enum.StartCorner](/docs/reference/engine/enums/StartCorner) of BottomRight.
The [UIGridStyleLayout.FillDirection](/docs/reference/engine/classes/UIGridStyleLayout#FillDirection) is Horizontal.

Provide feedback

---