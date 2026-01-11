# ItemLineAlignment | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/ItemLineAlignment
Scraped: 2026-01-11T02:45:33.883830Z

## Inherits
- ItemLineAlignment
- UIListLayout
- UIFlexItem
- GuiObject
- HorizontalAlignment
- VerticalAlignment
- FillDirection
- HorizontalFlex
- VerticalFlex
1. [Enums](/docs/reference/engine/enums)
2. /
3. [ItemLineAlignment](/docs/reference/engine/enums/ItemLineAlignment)

English

Feedback

Engine Enum

ItemLineAlignment

---

In a [flex layout](/docs/ui/list-flex-layouts#flex-layouts), this enum
is used for the [ItemLineAlignment](/docs/reference/engine/classes/UIListLayout#ItemLineAlignment)
property of the [UIListLayout](/docs/reference/engine/classes/UIListLayout) to define the cross-directional
alignment of siblings within a line. It is also used for the
[ItemLineAlignment](/docs/reference/engine/classes/UIFlexItem#ItemLineAlignment) property of a specific
[UIFlexItem](/docs/reference/engine/classes/UIFlexItem) to define the cross-directional alignment of the parent
[GuiObject](/docs/reference/engine/classes/GuiObject) within the line.

![Examples of options for ItemLineAlignment in a horizontal
fill direction.](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/UIListLayout/ItemLineAlignment.png)

Items

| Name | Value | Summary |
| --- | --- | --- |
| Automatic | 0 | Aligns the siblings of the [UIListLayout](/docs/reference/engine/classes/UIListLayout) or the specific [UIFlexItem](/docs/reference/engine/classes/UIFlexItem) parent to the layout's [HorizontalAlignment](/docs/reference/engine/classes/UIListLayout#HorizontalAlignment) or [VerticalAlignment](/docs/reference/engine/classes/UIListLayout#VerticalAlignment), depending on its [FillDirection](/docs/reference/engine/classes/UIListLayout#FillDirection). If [HorizontalFlex](/docs/reference/engine/classes/UIListLayout#HorizontalFlex) or [VerticalFlex](/docs/reference/engine/classes/UIListLayout#VerticalFlex) is enabled for the [UIListLayout](/docs/reference/engine/classes/UIListLayout) cross‑direction, Stretch will be used for that direction. |
| Start | 1 | Aligns the siblings of the [UIListLayout](/docs/reference/engine/classes/UIListLayout) or the specific [UIFlexItem](/docs/reference/engine/classes/UIFlexItem) parent to the line's top in a horizontal fill or the line's left in a vertical fill. |
| Center | 2 | Aligns the siblings of the [UIListLayout](/docs/reference/engine/classes/UIListLayout) or the specific [UIFlexItem](/docs/reference/engine/classes/UIFlexItem) parent to the line's center in either a horizontal or vertical fill. |
| End | 3 | Aligns the siblings of the [UIListLayout](/docs/reference/engine/classes/UIListLayout) or the specific [UIFlexItem](/docs/reference/engine/classes/UIFlexItem) parent to the line's bottom in a horizontal fill or the line's right in a vertical fill. |
| Stretch | 4 | Stretches the siblings of the [UIListLayout](/docs/reference/engine/classes/UIListLayout) or the specific [UIFlexItem](/docs/reference/engine/classes/UIFlexItem) parent to fill the entire cross‑direction of the line in either a horizontal or vertical fill. |