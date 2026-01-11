# FrameStyle | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/FrameStyle
Scraped: 2026-01-11T02:43:26.178077Z

## Inherits
- Frame
- GuiObject.BackgroundColor3
- GuiObject.BorderColor3
- GuiObject.BackgroundTransparency
- Dialog
- Tone
1. [Enums](/docs/reference/engine/enums)
2. /
3. [FrameStyle](/docs/reference/engine/enums/FrameStyle)

English

Feedback

Engine Enum

FrameStyle

---

The FrameStyle enum is used to set the style of a [Frame](/docs/reference/engine/classes/Frame).

Items

| Name | Value | Summary |
| --- | --- | --- |
| Custom | 0 | Uses the frame's [GuiObject.BackgroundColor3](/docs/reference/engine/classes/GuiObject#BackgroundColor3), [GuiObject.BorderColor3](/docs/reference/engine/classes/GuiObject#BorderColor3), and [GuiObject.BackgroundTransparency](/docs/reference/engine/classes/GuiObject#BackgroundTransparency) properties to determine the frame's appearance. It has no padding; elements with the position [UDim2.new(0, 0, 0, 0)](/docs/reference/engine/datatypes/UDim2#new) will appear at the frame's top-left corner. |
| ChatBlue | 1 | Causes the frame to appear similar to a [Dialog](/docs/reference/engine/classes/Dialog) with its [Tone](/docs/reference/engine/classes/Dialog#Tone) property set to [Enum.DialogTone.Neutral](/docs/reference/engine/enums/DialogTone#Neutral). Like ChatGreen and ChatRed, this has a padding of fifteen pixels on all sides. |
| RobloxSquare | 2 | Causes the frame to appear as a translucent dark gray rectangle with a padding of five pixels on all sides. |
| RobloxRound | 3 | Causes the frame to appear as a translucent dark gray rectangle with rounded edges. Like RobloxSquare, this has a padding of five pixels on all sides. |
| ChatGreen | 4 | Causes the frame to appear similar to a [Dialog](/docs/reference/engine/classes/Dialog) with its [Tone](/docs/reference/engine/classes/Dialog#Tone) property set to [Enum.DialogTone.Friendly](/docs/reference/engine/enums/DialogTone#Friendly). Like ChatBlue and ChatRed, this has a padding of fifteen pixels on all sides. |
| ChatRed | 5 | Causes the frame to appear similar to a [Dialog](/docs/reference/engine/classes/Dialog) with its [Tone](/docs/reference/engine/classes/Dialog#Tone) property set to [Enum.DialogTone.Enemy](/docs/reference/engine/enums/DialogTone#Enemy). Like ChatBlue and ChatGreen, this has a padding of fifteen pixels on all sides. |
| DropShadow | 6 | Causes the frame to appear as a translucent gray rectangle with blurred sides. The blur is more apparent on the bottom edge. It has a padding of eight pixels on all sides. |