# UIFlexMode | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/UIFlexMode
Scraped: 2026-01-11T02:44:44.853279Z

## Inherits
- UIFlexItem.FlexMode
- GuiObject
- GrowRatio
- ShrinkRatio
- UIFlexItem
1. [Enums](/docs/reference/engine/enums)
2. /
3. [UIFlexMode](/docs/reference/engine/enums/UIFlexMode)

English

Feedback

Engine Enum

UIFlexMode

---

Used with [UIFlexItem.FlexMode](/docs/reference/engine/classes/UIFlexItem#FlexMode) to define how the parent
[GuiObject](/docs/reference/engine/classes/GuiObject) grows or shrinks with available space in the container.

Items

| Name | Value | Summary |
| --- | --- | --- |
| None | 0 | The parent [GuiObject](/docs/reference/engine/classes/GuiObject) is unaffected and neither shrinks nor grows. |
| Grow | 1 | Sets an effective 1:0 grow‑shrink ratio on the parent [GuiObject](/docs/reference/engine/classes/GuiObject). Objects set to Grow never shrink below their basis size, so overflow may occur if the container becomes smaller than the flex line's combined basis size. |
| Shrink | 2 | Sets an effective 0:1 grow‑shrink ratio on the parent [GuiObject](/docs/reference/engine/classes/GuiObject). Objects set to Shrink never grow above their basis size, so underflow may occur if the container becomes larger than the flex line's combined basis size. |
| Fill | 3 | Sets an effective 1:1 grow‑shrink ratio on the parent [GuiObject](/docs/reference/engine/classes/GuiObject). This setting ensures the flex line always fills the container, even if the container size changes. |
| Custom | 4 | Enables the [GrowRatio](/docs/reference/engine/classes/UIFlexItem#GrowRatio) and [ShrinkRatio](/docs/reference/engine/classes/UIFlexItem#ShrinkRatio) properties for the [UIFlexItem](/docs/reference/engine/classes/UIFlexItem), allowing for relative growth or shrinking of the parent [GuiObject](/docs/reference/engine/classes/GuiObject) in a ratio compared to other flex objects also under control of a [UIFlexItem](/docs/reference/engine/classes/UIFlexItem). |