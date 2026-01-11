# UIDragSpeedAxisMapping | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/UIDragSpeedAxisMapping
Scraped: 2026-01-11T02:44:50.979319Z

## Inherits
- UIDragDetector.UIDragSpeedAxisMapping
- SelectionModeDragSpeed
- UIDragSpeedAxisMapping
1. [Enums](/docs/reference/engine/enums)
2. /
3. [UIDragSpeedAxisMapping](/docs/reference/engine/enums/UIDragSpeedAxisMapping)

English

Feedback

Engine Enum

UIDragSpeedAxisMapping

---

Used with [UIDragDetector.UIDragSpeedAxisMapping](/docs/reference/engine/classes/UIDragDetector#UIDragSpeedAxisMapping) to determine the
X/Y dimension dragging speeds, based on the detector's
[SelectionModeDragSpeed](/docs/reference/engine/classes/UIDragDetector#SelectionModeDragSpeed).

Items

| Name | Value | Summary |
| --- | --- | --- |
| XY | 0 | Default setting for a detector's [UIDragSpeedAxisMapping](/docs/reference/engine/classes/UIDragDetector#UIDragSpeedAxisMapping) where the X and Y axis speeds are based off the X and Y [Scale](/docs/reference/engine/datatypes/UDim#Scale)/[Offset](/docs/reference/engine/datatypes/UDim#Offset) values respectively. |
| XX | 1 | Both the X and Y axis speeds are based off the X axis for [Scale](/docs/reference/engine/datatypes/UDim#Scale), while the [Offset](/docs/reference/engine/datatypes/UDim#Offset) values still apply to their respective axis. |
| YY | 2 | Both the X and Y axis speeds are based off the Y axis for [Scale](/docs/reference/engine/datatypes/UDim#Scale), while the [Offset](/docs/reference/engine/datatypes/UDim#Offset) values still apply to their respective axis. |