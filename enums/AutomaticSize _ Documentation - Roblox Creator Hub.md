# AutomaticSize | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/AutomaticSize
Scraped: 2026-01-11T02:45:12.501976Z

## Inherits
- AutomaticSize
- Size
- GuiObject.AutomaticSize
- ScrollingFrame.AutomaticCanvasSize
1. [Enums](/docs/reference/engine/enums)
2. /
3. [AutomaticSize](/docs/reference/engine/enums/AutomaticSize)

English

Feedback

Engine Enum

AutomaticSize

---

UI objects with [AutomaticSize](/docs/reference/engine/classes/GuiObject#AutomaticSize) enabled will
increase in size up to maximum size allowed by the parent (if there is one)
and no smaller than the [Size](/docs/reference/engine/classes/GuiObject#Size) property bounds. To enable
[Enum.AutomaticSize](/docs/reference/engine/enums/AutomaticSize), set the value to an enum value other than None.

This enum is used by [GuiObject.AutomaticSize](/docs/reference/engine/classes/GuiObject#AutomaticSize) and
[ScrollingFrame.AutomaticCanvasSize](/docs/reference/engine/classes/ScrollingFrame#AutomaticCanvasSize) to determine whether and how
resizing occurs based on child content.

For more information, see
[Automatic Sizing](/docs/ui/size-modifiers#automatic-sizing).

Items

| Name | Value | Summary |
| --- | --- | --- |
| None | 0 | Default sizing behavior. |
| X | 1 | Automatically resize element along X-axis to fit child contents. |
| Y | 2 | Automatically resize element along Y-axis to fit child contents. Text Objects will only resize along the Y-axis if TextWrapped is enabled. |
| XY | 3 | Automatically resize element along X and Y axes to fit child contents. |