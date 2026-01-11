# SortOrder | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/SortOrder
Scraped: 2026-01-11T02:43:12.104613Z

## Inherits
- UIGridStyleLayout.SortOrder
- Instance.Name
- GuiObject.LayoutOrder
1. [Enums](/docs/reference/engine/enums)
2. /
3. [SortOrder](/docs/reference/engine/enums/SortOrder)

English

Feedback

Engine Enum

SortOrder

---

Used by [UIGridStyleLayout.SortOrder](/docs/reference/engine/classes/UIGridStyleLayout#SortOrder) to order the elements in the
layout.

![](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/UIListLayout/SortOrder.png)

Items

| Name | Value | Summary |
| --- | --- | --- |
| Name | 0 | Elements are ordered by their [Instance.Name](/docs/reference/engine/classes/Instance#Name) in alphanumeric order. |
| Custom | 1 | Deprecated |
| LayoutOrder | 2 | Elements are ordered by [GuiObject.LayoutOrder](/docs/reference/engine/classes/GuiObject#LayoutOrder) in ascending order; for example 0 will be placed before 1. |