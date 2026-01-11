# UIListLayout | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/UIListLayout
Scraped: 2026-01-11T02:41:38.382291Z

## Inherits
- UIGridStyleLayout
- UIListLayout
- Instance
- Object
- FillDirection
- Position
- Rotation
- GuiObject
- Size
- SortOrder
- LayoutOrder
- Name
- Padding
- Wraps
- HorizontalAlignment
- VerticalAlignment
- UIFlexItem
- HorizontalFlex
- VerticalFlex
- ItemLineAlignment
- GuiObject.AutomaticSize
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [UIGridStyleLayout](/docs/reference/engine/classes/UIGridStyleLayout)
6. /
7. [UIListLayout](/docs/reference/engine/classes/UIListLayout)

English

Feedback

Engine Class

![UIListLayout](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/UIListLayout-Dark.webp)UIListLayout

Positions sibling UI elements in rows or columns within the parent UI
container.

---

Summary

Properties

|  |
| --- |
| [HorizontalFlex](#HorizontalFlex):[Enum.UIFlexAlignment](/docs/reference/engine/enums/UIFlexAlignment) |
| [ItemLineAlignment](#ItemLineAlignment):[Enum.ItemLineAlignment](/docs/reference/engine/enums/ItemLineAlignment) |
| [Padding](#Padding):[UDim](/docs/reference/engine/datatypes/UDim) |
| [VerticalFlex](#VerticalFlex):[Enum.UIFlexAlignment](/docs/reference/engine/enums/UIFlexAlignment) |
| [Wraps](#Wraps):[boolean](/docs/luau/booleans) |

Inherited Members

7 inherited from [UIGridStyleLayout](/docs/reference/engine/classes/UIGridStyleLayout)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A [UIListLayout](/docs/reference/engine/classes/UIListLayout) positions sibling UI elements in rows or columns within
the parent UI container, based on the
[FillDirection](/docs/reference/engine/classes/UIListLayout#FillDirection). The
[Position](/docs/reference/engine/classes/GuiObject#Position) and [Rotation](/docs/reference/engine/classes/GuiObject#Rotation)
properties of each sibling [GuiObject](/docs/reference/engine/classes/GuiObject) are either ignored or overridden
by the list layout, while each sibling retains its defined
[Size](/docs/reference/engine/classes/GuiObject#Size) unless the layout is configured to utilize a flex
layout. See [List and Flex Layouts](/docs/ui/list-flex-layouts) for
further information.

![UIListLayouts illustrating FillDirection of either horizontal
or vertical.](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/UIListLayout/FillDirection.png)

To control the layout order of siblings, set
[SortOrder](/docs/reference/engine/classes/UIListLayout#SortOrder) to either [Enum.SortOrder.Name](/docs/reference/engine/enums/SortOrder#Name) or
[Enum.SortOrder.LayoutOrder](/docs/reference/engine/enums/SortOrder#LayoutOrder), then rename siblings in alphanumerical order or
set their [LayoutOrder](/docs/reference/engine/classes/GuiObject#LayoutOrder) value, respectively.
[UIListLayout](/docs/reference/engine/classes/UIListLayout) will automatically re‑layout elements when elements are
added/removed, or if a sibling's [Name](/docs/reference/engine/classes/Instance#Name) or
[LayoutOrder](/docs/reference/engine/classes/GuiObject#LayoutOrder) changes.

![List layout examples illustrating numerical LayoutOrder
sorting or alphanumerical Name sorting.](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/UIListLayout/SortOrder.png)

Padding between siblings is controlled through the
[Padding](/docs/reference/engine/classes/UIListLayout#Padding) property, and wrapping within the parent
container's bounds through the [Wraps](/docs/reference/engine/classes/UIListLayout#Wraps) boolean.
Alignment of siblings within the parent container is controlled through
[HorizontalAlignment](/docs/reference/engine/classes/UIListLayout#HorizontalAlignment) and
[VerticalAlignment](/docs/reference/engine/classes/UIListLayout#VerticalAlignment) unless the layout is
configured to utilize a
[flex layout](/docs/ui/list-flex-layouts#flex-layouts).

Note that there are performance implications of using a
[flex‑enabled](/docs/ui/list-flex-layouts#flex-layouts) list layout,
since extra calculations are needed to calculate flex basis sizes, flexed
sizes, and line wrapping. Flex is enabled on a [UIListLayout](/docs/reference/engine/classes/UIListLayout) when the
following properties are set, or if any [GuiObject](/docs/reference/engine/classes/GuiObject) sibling has a
[UIFlexItem](/docs/reference/engine/classes/UIFlexItem) parented to it:

* [HorizontalFlex](/docs/reference/engine/classes/UIListLayout#HorizontalFlex) and/or
  [VerticalFlex](/docs/reference/engine/classes/UIListLayout#VerticalFlex) are not set to
  [Enum.UIFlexAlignment.None](/docs/reference/engine/enums/UIFlexAlignment#None).
* [ItemLineAlignment](/docs/reference/engine/classes/UIListLayout#ItemLineAlignment) is not set to
  [Enum.ItemLineAlignment.Automatic](/docs/reference/engine/enums/ItemLineAlignment#Automatic).
* [Wraps](/docs/reference/engine/classes/UIListLayout#Wraps) is true.

---

API Reference

Properties

HorizontalFlex

Read Parallel

Controls how to distribute extra horizontal space.

UIListLayout.HorizontalFlex:[Enum.UIFlexAlignment](/docs/reference/engine/enums/UIFlexAlignment)

When the list layout's [FillDirection](/docs/reference/engine/classes/UIListLayout#FillDirection) is
set to [Enum.FillDirection.Horizontal](/docs/reference/engine/enums/FillDirection#Horizontal), the
[HorizontalFlex](/docs/reference/engine/classes/UIListLayout#HorizontalFlex) property specifies how
to distribute extra horizontal space in the parent container.

| Setting | Sibling Behavior |
| --- | --- |
| [None](/docs/reference/engine/enums/UIFlexAlignment#None) | No flex behavior; siblings maintain their defined width. |
| [Fill](/docs/reference/engine/enums/UIFlexAlignment#Fill) | Siblings resize horizontally to fill the entire parent container, overriding their defined width. The number of siblings in a row remain unchanged; for example, if three siblings fit horizontally within the container's width under the [None](/docs/reference/engine/enums/UIFlexAlignment#None) setting, those three siblings will resize to fill the entire width. |
| [SpaceAround](/docs/reference/engine/enums/UIFlexAlignment#SpaceAround) | Siblings maintain their defined width. Equal spacing is added on both sides of each sibling. |
| [SpaceBetween](/docs/reference/engine/enums/UIFlexAlignment#SpaceBetween) | Siblings maintain their defined width. Equal spacing is added **between** siblings, but no additional space is added **around** siblings. |
| [SpaceEvenly](/docs/reference/engine/enums/UIFlexAlignment#SpaceEvenly) | Siblings maintain their defined width. Equal spacing is added both **between** and **around** siblings. |

![UIListLayout examples showing how each HorizontalFlex option affects the size and spacing of sibling UI objects.](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/UIListLayout/HorizontalFlex-Options.png)

##### Cross-Direction Behavior

In vertical list layouts
([FillDirection](/docs/reference/engine/classes/UIListLayout#FillDirection) set to
[Enum.FillDirection.Vertical](/docs/reference/engine/enums/FillDirection#Vertical)), the
[HorizontalFlex](/docs/reference/engine/classes/UIListLayout#HorizontalFlex) property specifies how
to distribute the siblings across the horizontal cross‑direction. In
such layouts, a setting of [Enum.UIFlexAlignment.Fill](/docs/reference/engine/enums/UIFlexAlignment#Fill) makes the siblings
fill the entire horizontal space while vertical spacing adheres to
[VerticalFlex](/docs/reference/engine/classes/UIListLayout#VerticalFlex).

![Diagram showing how HorizontalFlex affects the horizontal size of sibling UI objects when the UIListLayout fill direction is set to vertical.](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/UIListLayout/HorizontalFlex-Cross-Direction.png)

##### AutomaticSize Interaction

If [GuiObject.AutomaticSize](/docs/reference/engine/classes/GuiObject#AutomaticSize) is enabled for a child of the
[UIListLayout](/docs/reference/engine/classes/UIListLayout) in the
[FillDirection](/docs/reference/engine/classes/UIListLayout#FillDirection), it is interpreted as
"automatic flex basis" and it defines the size of the [GuiObject](/docs/reference/engine/classes/GuiObject)
from which it can grow or shrink.

If [GuiObject.AutomaticSize](/docs/reference/engine/classes/GuiObject#AutomaticSize) is enabled for a child of the
[UIListLayout](/docs/reference/engine/classes/UIListLayout) in the cross‑direction, it is interpreted as
"automatic cross size" and it defines the minimum size needed to contain
all the child's content in the cross‑direction.

Provide feedback

---

ItemLineAlignment

Read Parallel

In a flex layout, defines the cross-directional alignment of siblings
within a line.

UIListLayout.ItemLineAlignment:[Enum.ItemLineAlignment](/docs/reference/engine/enums/ItemLineAlignment)

In a [flex layout](/docs/ui/list-flex-layouts#flex-layouts), defines
the cross-directional alignment of siblings within a line. See
[Enum.ItemLineAlignment](/docs/reference/engine/enums/ItemLineAlignment) for visual examples.

| Setting | Sibling Behavior |
| --- | --- |
| [Automatic](/docs/reference/engine/enums/ItemLineAlignment#Automatic) | Aligns the layout's siblings or the specific [UIFlexItem](/docs/reference/engine/classes/UIFlexItem) parent to the layout's [HorizontalAlignment](/docs/reference/engine/classes/UIListLayout#HorizontalAlignment) or [VerticalAlignment](/docs/reference/engine/classes/UIListLayout#VerticalAlignment), depending on its [FillDirection](/docs/reference/engine/classes/UIListLayout#FillDirection). |
| [Start](/docs/reference/engine/enums/ItemLineAlignment#Start) | Aligns the layout's siblings or the specific [UIFlexItem](/docs/reference/engine/classes/UIFlexItem) parent to the line's **top** in a horizontal fill or the line's **left** in a vertical fill. |
| [Center](/docs/reference/engine/enums/ItemLineAlignment#Center) | Aligns the layout's siblings or the specific [UIFlexItem](/docs/reference/engine/classes/UIFlexItem) parent to the line's **center** in either a horizontal or vertical fill. |
| [End](/docs/reference/engine/enums/ItemLineAlignment#End) | Aligns the layout's siblings or the specific [UIFlexItem](/docs/reference/engine/classes/UIFlexItem) parent to the line's **bottom** in a horizontal fill or the line's **right** in a vertical fill. |
| [Stretch](/docs/reference/engine/enums/ItemLineAlignment#Stretch) | Stretches the layout's siblings or the specific [UIFlexItem](/docs/reference/engine/classes/UIFlexItem) parent to fill the entire cross‑direction of the line in either a horizontal or vertical fill. |

![Examples of options for ItemLineAlignment in a horizontal fill direction.](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/UIListLayout/ItemLineAlignment.png)

Provide feedback

---

Padding

Read Parallel

Amount of free space between each element.

UIListLayout.Padding:[UDim](/docs/reference/engine/datatypes/UDim)

Determines the amount of free space between each element, set to either a
scale (percentage of the parent's size in the current direction) or an
offset (static spacing value similar to pixel size).

Provide feedback

---

VerticalFlex

Read Parallel

Controls how to distribute extra vertical space.

UIListLayout.VerticalFlex:[Enum.UIFlexAlignment](/docs/reference/engine/enums/UIFlexAlignment)

When the list layout's [FillDirection](/docs/reference/engine/classes/UIListLayout#FillDirection) is
set to [Enum.FillDirection.Vertical](/docs/reference/engine/enums/FillDirection#Vertical), the
[VerticalFlex](/docs/reference/engine/classes/UIListLayout#VerticalFlex) property specifies how to
distribute extra vertical space in the parent container.

| Setting | Sibling Behavior |
| --- | --- |
| [None](/docs/reference/engine/enums/UIFlexAlignment#None) | No flex behavior; siblings maintain their defined height. |
| [Fill](/docs/reference/engine/enums/UIFlexAlignment#Fill) | Siblings resize vertically to fill the entire parent container, overriding their defined height. The number of siblings in a column remain unchanged; for example, if three siblings fit vertically within the container's height under the [None](/docs/reference/engine/enums/UIFlexAlignment#None) setting, those three siblings will resize to fill the entire height. |
| [SpaceAround](/docs/reference/engine/enums/UIFlexAlignment#SpaceAround) | Siblings maintain their defined height. Equal spacing is added on both sides of each sibling. |
| [SpaceBetween](/docs/reference/engine/enums/UIFlexAlignment#SpaceBetween) | Siblings maintain their defined height. Equal spacing is added **between** siblings, but no additional space is added **around** siblings. |
| [SpaceEvenly](/docs/reference/engine/enums/UIFlexAlignment#SpaceEvenly) | Siblings maintain their defined height. Equal spacing is added both **between** and **around** siblings. |

![UIListLayout examples showing how each VerticalFlex option affects the size and spacing of sibling UI objects.](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/UIListLayout/VerticalFlex-Options.png)

##### Cross-Direction Behavior

In horizontal list layouts
([FillDirection](/docs/reference/engine/classes/UIListLayout#FillDirection) set to
[Enum.FillDirection.Horizontal](/docs/reference/engine/enums/FillDirection#Horizontal)), the
[VerticalFlex](/docs/reference/engine/classes/UIListLayout#VerticalFlex) property specifies how to
distribute the siblings across the vertical cross direction. In such
layouts, a setting of [Enum.UIFlexAlignment.Fill](/docs/reference/engine/enums/UIFlexAlignment#Fill) makes the siblings fill
the entire vertical space while horizontal spacing adheres to
[HorizontalFlex](/docs/reference/engine/classes/UIListLayout#HorizontalFlex).

![Diagram showing how VerticalFlex affects the vertical size of sibling UI objects when the UIListLayout fill direction is set to horizontal.](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/UIListLayout/VerticalFlex-Cross-Direction.png)

##### AutomaticSize Interaction

If [GuiObject.AutomaticSize](/docs/reference/engine/classes/GuiObject#AutomaticSize) is enabled for a child of the
[UIListLayout](/docs/reference/engine/classes/UIListLayout) in the
[FillDirection](/docs/reference/engine/classes/UIListLayout#FillDirection), it is interpreted as
"automatic flex basis" and it defines the size of the [GuiObject](/docs/reference/engine/classes/GuiObject)
from which it can grow or shrink.

If [GuiObject.AutomaticSize](/docs/reference/engine/classes/GuiObject#AutomaticSize) is enabled for a child of the
[UIListLayout](/docs/reference/engine/classes/UIListLayout) in the cross‑direction, it is interpreted as
"automatic cross size" and it defines the minimum size needed to contain
all the child's content in the cross‑direction.

Provide feedback

---

Wraps

Read Parallel

Controls whether siblings within the parent container wrap.

UIListLayout.Wraps:[boolean](/docs/luau/booleans)

Controls whether siblings within the parent container wrap to another line
when their default size exceeds the width/height of the container's
bounds.

![Diagram showing how Wraps affects how siblings are distributed within the parent container's bounds.](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/UIListLayout/Wraps.png)

Provide feedback

---