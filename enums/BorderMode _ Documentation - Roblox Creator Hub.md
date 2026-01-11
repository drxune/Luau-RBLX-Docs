# BorderMode | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/BorderMode
Scraped: 2026-01-11T02:44:30.560415Z

## Inherits
- GuiObject
- GuiObject.BorderMode
- GuiObject.BorderSizePixel
1. [Enums](/docs/reference/engine/enums)
2. /
3. [BorderMode](/docs/reference/engine/enums/BorderMode)

English

Feedback

Engine Enum

BorderMode

---

Determines in what matter the border of a [GuiObject](/docs/reference/engine/classes/GuiObject) is laid out
relative to its actual dimensions. It is used by the property of the same
name, [GuiObject.BorderMode](/docs/reference/engine/classes/GuiObject#BorderMode).

Items

| Name | Value | Summary |
| --- | --- | --- |
| Outline | 0 | As [GuiObject.BorderSizePixel](/docs/reference/engine/classes/GuiObject#BorderSizePixel) increases, the border grows outward. The dimensions of the GuiObject's contents do not change. |
| Middle | 1 | As [GuiObject.BorderSizePixel](/docs/reference/engine/classes/GuiObject#BorderSizePixel) increases, the border grows evenly inward and outward. The dimensions of the GuiObject's contents are reduced at a 1:1 ratio. |
| Inset | 2 | As [GuiObject.BorderSizePixel](/docs/reference/engine/classes/GuiObject#BorderSizePixel) increases, the border grows evenly inward only. The dimensions of the GuiObject's contents are reduced at a 1:2 ratio. |