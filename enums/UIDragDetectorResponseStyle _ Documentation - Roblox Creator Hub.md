# UIDragDetectorResponseStyle | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/UIDragDetectorResponseStyle
Scraped: 2026-01-11T02:44:18.417743Z

## Inherits
- GuiObject
- GuiObject.Position
- DragUDim2
1. [Enums](/docs/reference/engine/enums)
2. /
3. [UIDragDetectorResponseStyle](/docs/reference/engine/enums/UIDragDetectorResponseStyle)

English

Feedback

Engine Enum

UIDragDetectorResponseStyle

---

Describes how the clicked [GuiObject](/docs/reference/engine/classes/GuiObject) will be treated once the desired
motion has been calculated.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Offset | 0 | Move by the [Offset](/docs/reference/engine/datatypes/UDim#Offset) values of the detector's parent's [GuiObject.Position](/docs/reference/engine/classes/GuiObject#Position) value. |
| Scale | 1 | Move by the [Scale](/docs/reference/engine/datatypes/UDim#Scale) values of the detector's parent's [GuiObject.Position](/docs/reference/engine/classes/GuiObject#Position) value. |
| CustomOffset | 2 | The UI element will not move at all, but the [Offset](/docs/reference/engine/datatypes/UDim#Offset) values of the detector's [DragUDim2](/docs/reference/engine/classes/UIDragDetector#DragUDim2) will still be updated and the detector's events will still fire, allowing you to respond to drag manipulation however you'd like. |
| CustomScale | 3 | The UI element will not move at all, but the [Scale](/docs/reference/engine/datatypes/UDim#Scale) values of the detector's [DragUDim2](/docs/reference/engine/classes/UIDragDetector#DragUDim2) will still be updated and the detector's events will still fire, allowing you to respond to drag manipulation however you'd like. |