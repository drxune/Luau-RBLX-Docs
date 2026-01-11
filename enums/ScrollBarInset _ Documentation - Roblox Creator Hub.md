# ScrollBarInset | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/ScrollBarInset
Scraped: 2026-01-11T02:44:35.127649Z

## Inherits
- ScrollingFrame.HorizontalScrollBarInset
- ScrollingFrame.VerticalScrollBarInset
- ScrollBarThickness
1. [Enums](/docs/reference/engine/enums)
2. /
3. [ScrollBarInset](/docs/reference/engine/enums/ScrollBarInset)

English

Feedback

Engine Enum

ScrollBarInset

---

This enum is used with [ScrollingFrame.HorizontalScrollBarInset](/docs/reference/engine/classes/ScrollingFrame#HorizontalScrollBarInset) and
[ScrollingFrame.VerticalScrollBarInset](/docs/reference/engine/classes/ScrollingFrame#VerticalScrollBarInset) to indicate whether the canvas
should be inset by
[ScrollBarThickness](/docs/reference/engine/classes/ScrollingFrame#ScrollBarThickness) for the
respective scroll bar.

Items

| Name | Value | Summary |
| --- | --- | --- |
| None | 0 | The canvas will never be inset for the respective scroll bar. |
| ScrollBar | 1 | The canvas will only be inset if the respective scroll bar is showing. |
| Always | 2 | The canvas will always be inset for the respective scroll bar, regardless of whether that scroll bar is showing. |