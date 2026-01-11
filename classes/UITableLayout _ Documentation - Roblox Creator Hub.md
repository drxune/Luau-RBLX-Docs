# UITableLayout | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/UITableLayout
Scraped: 2026-01-11T02:42:23.943978Z

## Inherits
- UIGridStyleLayout
- UITableLayout
- Instance
- Object
- UIGridStyleLayout.FillDirection
- GuiObject.Size
- GuiObject.Position
- UITableLayout.FillEmptySpaceColumns
- UITableLayout.FillEmptySpaceRows
- UISizeConstraint
- UISizeConstraint.MinSize
- UISizeConstraints
- UISizeConstraint.MaxSize
- GuiBase2d.AbsoluteSize
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [UIGridStyleLayout](/docs/reference/engine/classes/UIGridStyleLayout)
6. /
7. [UITableLayout](/docs/reference/engine/classes/UITableLayout)

English

Feedback

Engine Class

![UITableLayout](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/UITableLayout-Dark.webp)UITableLayout

Lays out sibling UI elements and their child UI elements as rows/columns and
cells in a table.

---

Summary

Properties

|  |
| --- |
| [FillEmptySpaceColumns](#FillEmptySpaceColumns):[boolean](/docs/luau/booleans) |
| [FillEmptySpaceRows](#FillEmptySpaceRows):[boolean](/docs/luau/booleans) |
| [MajorAxis](#MajorAxis):[Enum.TableMajorAxis](/docs/reference/engine/enums/TableMajorAxis) |
| [Padding](#Padding):[UDim2](/docs/reference/engine/datatypes/UDim2) |

Inherited Members

7 inherited from [UIGridStyleLayout](/docs/reference/engine/classes/UIGridStyleLayout)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A UITableLayout lays out sibling UI elements as rows in a table. Child UI
elements (the table cells) of these rows are then arranged in columns (within
rows). Each cell within a row has the same height, and each cell within a
column has the same width.

By changing the [UIGridStyleLayout.FillDirection](/docs/reference/engine/classes/UIGridStyleLayout#FillDirection), sibling UI elements
can act as columns instead.

When applied, a UITableLayout will take control of sibling and cell elements'
[GuiObject.Size](/docs/reference/engine/classes/GuiObject#Size) and [GuiObject.Position](/docs/reference/engine/classes/GuiObject#Position). Changing these in the
Properties window is still possible will not produce any effect.

Dimensions of the cells in the resulting table are controlled by the parent UI
element's dimensions. Unless [UITableLayout.FillEmptySpaceColumns](/docs/reference/engine/classes/UITableLayout#FillEmptySpaceColumns) or
[UITableLayout.FillEmptySpaceRows](/docs/reference/engine/classes/UITableLayout#FillEmptySpaceRows) is enabled, the cell dimensions will
be that of the parent UI element (and thus tables with more than one cell
extend outside of their parent).

Cells will continue to respect [UISizeConstraint](/docs/reference/engine/classes/UISizeConstraint) objects within them.
In other words, setting [UISizeConstraint.MinSize](/docs/reference/engine/classes/UISizeConstraint#MinSize) on
[UISizeConstraints](/docs/reference/engine/classes/UISizeConstraint) within the header cells can
determine the size of the rest of the cells. If
[UISizeConstraint.MaxSize](/docs/reference/engine/classes/UISizeConstraint#MaxSize) restricts a cell's size from filling the
allotted space (i.e. another row/column is wider than it), it will align to
the top-left.

Code Samples

Build UI Table

This code sample builds a table of 4 rows, the first having headers. It does
this using some for-loops and a UITableLayout. The widths of each column are
set using UISizeConstraints.

```
local frame = script.Parent



-- Table data



local headerWidth = { 200, 80, 80 }



local headers = {



"Name",



"Job",



"Cash",



}



local data = {



{ "Bob", "Waiter", 100 },



{ "Lisa", "Police", 200 },



{ "George", "-", 50 },



}



-- First, build the table layout



local uiTableLayout = Instance.new("UITableLayout")



uiTableLayout.FillDirection = Enum.FillDirection.Vertical



uiTableLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center



uiTableLayout.VerticalAlignment = Enum.VerticalAlignment.Center



uiTableLayout.FillEmptySpaceColumns = false



uiTableLayout.FillEmptySpaceRows = false



uiTableLayout.Padding = UDim2.new(0, 5, 0, 5)



uiTableLayout.SortOrder = Enum.SortOrder.LayoutOrder



frame.Size = UDim2.new(0, 0, 0, 40) -- The Size of the parent frame is the cell size



uiTableLayout.Parent = frame



-- Next, create column headers



local headerFrame = Instance.new("Frame")



headerFrame.Name = "Headers"



headerFrame.Parent = frame



for i = 1, #headers do



local headerText = headers[i]



local headerCell = Instance.new("TextLabel")



headerCell.Text = headerText



headerCell.Name = headerText



headerCell.LayoutOrder = i



headerCell.Size = UDim2.new(0, 0, 0, 24)



headerCell.Parent = headerFrame



local headerSize = Instance.new("UISizeConstraint")



headerSize.MinSize = Vector2.new(headerWidth[i], 0)



headerSize.Parent = headerCell



end



-- Finally, add data rows by iterating over each row and the columns in that row



for index, value in ipairs(data) do



local rowData = value



local rowFrame = Instance.new("Frame")



rowFrame.Name = "Row" .. index



rowFrame.Parent = frame



for col = 1, #value do



local cellData = rowData[col]



local cell = Instance.new("TextLabel")



cell.Text = cellData



cell.Name = headers[col]



cell.TextXAlignment = Enum.TextXAlignment.Left



if tonumber(cellData) then -- If this cell is a number, right-align it instead



cell.TextXAlignment = Enum.TextXAlignment.Right



end



cell.ClipsDescendants = true



cell.Size = UDim2.new(0, 0, 0, 24)



cell.Parent = rowFrame



end



end
```

---

API Reference

Properties

FillEmptySpaceColumns

Read Parallel

Determines whether cells are sized such that they occupy the horizontal
space of the parent UI element.

UITableLayout.FillEmptySpaceColumns:[boolean](/docs/luau/booleans)

FillEmptySpaceColumns determines whether cells' X size are set such that
the entire horizontal space of the parent UI element is used. Enabling
this is useful for making sure your table takes up a more easily
predictable amount of horizontal space (the X-axis size of the parent UI
element). It is still possible that a [UISizeConstraint](/docs/reference/engine/classes/UISizeConstraint) applied to
cells will cause underflow/overflow.

When enabling this property, the column widths will be approximately equal
to the parent's [GuiBase2d.AbsoluteSize](/docs/reference/engine/classes/GuiBase2d#AbsoluteSize).X component divided by the
number of columns (not accounting for padding or other factors).

Code Samples

Build UI Table

This code sample builds a table of 4 rows, the first having headers. It does
this using some for-loops and a UITableLayout. The widths of each column are
set using UISizeConstraints.

```
local frame = script.Parent



-- Table data



local headerWidth = { 200, 80, 80 }



local headers = {



"Name",



"Job",



"Cash",



}



local data = {



{ "Bob", "Waiter", 100 },



{ "Lisa", "Police", 200 },



{ "George", "-", 50 },



}



-- First, build the table layout



local uiTableLayout = Instance.new("UITableLayout")



uiTableLayout.FillDirection = Enum.FillDirection.Vertical



uiTableLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center



uiTableLayout.VerticalAlignment = Enum.VerticalAlignment.Center



uiTableLayout.FillEmptySpaceColumns = false



uiTableLayout.FillEmptySpaceRows = false



uiTableLayout.Padding = UDim2.new(0, 5, 0, 5)



uiTableLayout.SortOrder = Enum.SortOrder.LayoutOrder



frame.Size = UDim2.new(0, 0, 0, 40) -- The Size of the parent frame is the cell size



uiTableLayout.Parent = frame



-- Next, create column headers



local headerFrame = Instance.new("Frame")



headerFrame.Name = "Headers"



headerFrame.Parent = frame



for i = 1, #headers do



local headerText = headers[i]



local headerCell = Instance.new("TextLabel")



headerCell.Text = headerText



headerCell.Name = headerText



headerCell.LayoutOrder = i



headerCell.Size = UDim2.new(0, 0, 0, 24)



headerCell.Parent = headerFrame



local headerSize = Instance.new("UISizeConstraint")



headerSize.MinSize = Vector2.new(headerWidth[i], 0)



headerSize.Parent = headerCell



end



-- Finally, add data rows by iterating over each row and the columns in that row



for index, value in ipairs(data) do



local rowData = value



local rowFrame = Instance.new("Frame")



rowFrame.Name = "Row" .. index



rowFrame.Parent = frame



for col = 1, #value do



local cellData = rowData[col]



local cell = Instance.new("TextLabel")



cell.Text = cellData



cell.Name = headers[col]



cell.TextXAlignment = Enum.TextXAlignment.Left



if tonumber(cellData) then -- If this cell is a number, right-align it instead



cell.TextXAlignment = Enum.TextXAlignment.Right



end



cell.ClipsDescendants = true



cell.Size = UDim2.new(0, 0, 0, 24)



cell.Parent = rowFrame



end



end
```

Provide feedback

---

FillEmptySpaceRows

Read Parallel

Determines whether cells are sized such that they occupy the vertical
space of the parent UI element.

UITableLayout.FillEmptySpaceRows:[boolean](/docs/luau/booleans)

FillEmptySpaceRows determines whether cells' Y size are set such that the
entire vertical space of the parent UI element is used. Enabling this is
useful for making sure your table takes up a more easily predictable
amount of vertical space (the Y-axis size of the parent UI element). It is
still possible that a [UISizeConstraint](/docs/reference/engine/classes/UISizeConstraint) applied to cells will cause
underflow/overflow.

When enabling this property, the row heights will be approximately equal
to the parent's [GuiBase2d.AbsoluteSize](/docs/reference/engine/classes/GuiBase2d#AbsoluteSize).Y component divided by the
number of rows (not accounting for padding or other factors).

Code Samples

Build UI Table

This code sample builds a table of 4 rows, the first having headers. It does
this using some for-loops and a UITableLayout. The widths of each column are
set using UISizeConstraints.

```
local frame = script.Parent



-- Table data



local headerWidth = { 200, 80, 80 }



local headers = {



"Name",



"Job",



"Cash",



}



local data = {



{ "Bob", "Waiter", 100 },



{ "Lisa", "Police", 200 },



{ "George", "-", 50 },



}



-- First, build the table layout



local uiTableLayout = Instance.new("UITableLayout")



uiTableLayout.FillDirection = Enum.FillDirection.Vertical



uiTableLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center



uiTableLayout.VerticalAlignment = Enum.VerticalAlignment.Center



uiTableLayout.FillEmptySpaceColumns = false



uiTableLayout.FillEmptySpaceRows = false



uiTableLayout.Padding = UDim2.new(0, 5, 0, 5)



uiTableLayout.SortOrder = Enum.SortOrder.LayoutOrder



frame.Size = UDim2.new(0, 0, 0, 40) -- The Size of the parent frame is the cell size



uiTableLayout.Parent = frame



-- Next, create column headers



local headerFrame = Instance.new("Frame")



headerFrame.Name = "Headers"



headerFrame.Parent = frame



for i = 1, #headers do



local headerText = headers[i]



local headerCell = Instance.new("TextLabel")



headerCell.Text = headerText



headerCell.Name = headerText



headerCell.LayoutOrder = i



headerCell.Size = UDim2.new(0, 0, 0, 24)



headerCell.Parent = headerFrame



local headerSize = Instance.new("UISizeConstraint")



headerSize.MinSize = Vector2.new(headerWidth[i], 0)



headerSize.Parent = headerCell



end



-- Finally, add data rows by iterating over each row and the columns in that row



for index, value in ipairs(data) do



local rowData = value



local rowFrame = Instance.new("Frame")



rowFrame.Name = "Row" .. index



rowFrame.Parent = frame



for col = 1, #value do



local cellData = rowData[col]



local cell = Instance.new("TextLabel")



cell.Text = cellData



cell.Name = headers[col]



cell.TextXAlignment = Enum.TextXAlignment.Left



if tonumber(cellData) then -- If this cell is a number, right-align it instead



cell.TextXAlignment = Enum.TextXAlignment.Right



end



cell.ClipsDescendants = true



cell.Size = UDim2.new(0, 0, 0, 24)



cell.Parent = rowFrame



end



end
```

Provide feedback

---

MajorAxis

Read Parallel

Determines whether sibling UI elements are treated as rows or columns.

UITableLayout.MajorAxis:[Enum.TableMajorAxis](/docs/reference/engine/enums/TableMajorAxis)

MajorAxis determines whether sibling UI elements are treated as rows or
columns.

Code Samples

Build UI Table

This code sample builds a table of 4 rows, the first having headers. It does
this using some for-loops and a UITableLayout. The widths of each column are
set using UISizeConstraints.

```
local frame = script.Parent



-- Table data



local headerWidth = { 200, 80, 80 }



local headers = {



"Name",



"Job",



"Cash",



}



local data = {



{ "Bob", "Waiter", 100 },



{ "Lisa", "Police", 200 },



{ "George", "-", 50 },



}



-- First, build the table layout



local uiTableLayout = Instance.new("UITableLayout")



uiTableLayout.FillDirection = Enum.FillDirection.Vertical



uiTableLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center



uiTableLayout.VerticalAlignment = Enum.VerticalAlignment.Center



uiTableLayout.FillEmptySpaceColumns = false



uiTableLayout.FillEmptySpaceRows = false



uiTableLayout.Padding = UDim2.new(0, 5, 0, 5)



uiTableLayout.SortOrder = Enum.SortOrder.LayoutOrder



frame.Size = UDim2.new(0, 0, 0, 40) -- The Size of the parent frame is the cell size



uiTableLayout.Parent = frame



-- Next, create column headers



local headerFrame = Instance.new("Frame")



headerFrame.Name = "Headers"



headerFrame.Parent = frame



for i = 1, #headers do



local headerText = headers[i]



local headerCell = Instance.new("TextLabel")



headerCell.Text = headerText



headerCell.Name = headerText



headerCell.LayoutOrder = i



headerCell.Size = UDim2.new(0, 0, 0, 24)



headerCell.Parent = headerFrame



local headerSize = Instance.new("UISizeConstraint")



headerSize.MinSize = Vector2.new(headerWidth[i], 0)



headerSize.Parent = headerCell



end



-- Finally, add data rows by iterating over each row and the columns in that row



for index, value in ipairs(data) do



local rowData = value



local rowFrame = Instance.new("Frame")



rowFrame.Name = "Row" .. index



rowFrame.Parent = frame



for col = 1, #value do



local cellData = rowData[col]



local cell = Instance.new("TextLabel")



cell.Text = cellData



cell.Name = headers[col]



cell.TextXAlignment = Enum.TextXAlignment.Left



if tonumber(cellData) then -- If this cell is a number, right-align it instead



cell.TextXAlignment = Enum.TextXAlignment.Right



end



cell.ClipsDescendants = true



cell.Size = UDim2.new(0, 0, 0, 24)



cell.Parent = rowFrame



end



end
```

Provide feedback

---

Padding

Read Parallel

Determines the empty space between cells.

UITableLayout.Padding:[UDim2](/docs/reference/engine/datatypes/UDim2)

Padding will position elements with extra space between them. This can be
done using Scale or Offset components of UDim2. Negative values can bring
elements closer together. When non-zero, the sibling UI elements may be
visible between the cells contained within them.

Code Samples

Build UI Table

This code sample builds a table of 4 rows, the first having headers. It does
this using some for-loops and a UITableLayout. The widths of each column are
set using UISizeConstraints.

```
local frame = script.Parent



-- Table data



local headerWidth = { 200, 80, 80 }



local headers = {



"Name",



"Job",



"Cash",



}



local data = {



{ "Bob", "Waiter", 100 },



{ "Lisa", "Police", 200 },



{ "George", "-", 50 },



}



-- First, build the table layout



local uiTableLayout = Instance.new("UITableLayout")



uiTableLayout.FillDirection = Enum.FillDirection.Vertical



uiTableLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center



uiTableLayout.VerticalAlignment = Enum.VerticalAlignment.Center



uiTableLayout.FillEmptySpaceColumns = false



uiTableLayout.FillEmptySpaceRows = false



uiTableLayout.Padding = UDim2.new(0, 5, 0, 5)



uiTableLayout.SortOrder = Enum.SortOrder.LayoutOrder



frame.Size = UDim2.new(0, 0, 0, 40) -- The Size of the parent frame is the cell size



uiTableLayout.Parent = frame



-- Next, create column headers



local headerFrame = Instance.new("Frame")



headerFrame.Name = "Headers"



headerFrame.Parent = frame



for i = 1, #headers do



local headerText = headers[i]



local headerCell = Instance.new("TextLabel")



headerCell.Text = headerText



headerCell.Name = headerText



headerCell.LayoutOrder = i



headerCell.Size = UDim2.new(0, 0, 0, 24)



headerCell.Parent = headerFrame



local headerSize = Instance.new("UISizeConstraint")



headerSize.MinSize = Vector2.new(headerWidth[i], 0)



headerSize.Parent = headerCell



end



-- Finally, add data rows by iterating over each row and the columns in that row



for index, value in ipairs(data) do



local rowData = value



local rowFrame = Instance.new("Frame")



rowFrame.Name = "Row" .. index



rowFrame.Parent = frame



for col = 1, #value do



local cellData = rowData[col]



local cell = Instance.new("TextLabel")



cell.Text = cellData



cell.Name = headers[col]



cell.TextXAlignment = Enum.TextXAlignment.Left



if tonumber(cellData) then -- If this cell is a number, right-align it instead



cell.TextXAlignment = Enum.TextXAlignment.Right



end



cell.ClipsDescendants = true



cell.Size = UDim2.new(0, 0, 0, 24)



cell.Parent = rowFrame



end



end
```

Provide feedback

---