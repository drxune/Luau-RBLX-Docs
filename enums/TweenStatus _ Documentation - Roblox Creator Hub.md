# TweenStatus | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/TweenStatus
Scraped: 2026-01-11T02:43:03.307436Z

## Inherits
- GuiObject
- GuiObject:TweenPosition()
- GuiObject:TweenSize()
- GuiObject:TweenSizeAndPosition()
- TweenService
1. [Enums](/docs/reference/engine/enums)
2. /
3. [TweenStatus](/docs/reference/engine/enums/TweenStatus)

English

Feedback

Engine Enum

TweenStatus

---

Describes the completion status of a [GuiObject](/docs/reference/engine/classes/GuiObject) tween function.

Passed as an argument to the callback function provided to
[GuiObject:TweenPosition()](/docs/reference/engine/classes/GuiObject#TweenPosition), [GuiObject:TweenSize()](/docs/reference/engine/classes/GuiObject#TweenSize), and
[GuiObject:TweenSizeAndPosition()](/docs/reference/engine/classes/GuiObject#TweenSizeAndPosition).

Not to be confused for [Enum.PlaybackState](/docs/reference/engine/enums/PlaybackState) which is used with
[TweenService](/docs/reference/engine/classes/TweenService).

Items

| Name | Value | Summary |
| --- | --- | --- |
| Canceled | 0 | The tween was cancelled before completion. |
| Completed | 1 | The Tween has successfully completed. |