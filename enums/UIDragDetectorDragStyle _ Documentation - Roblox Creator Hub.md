# UIDragDetectorDragStyle | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/UIDragDetectorDragStyle
Scraped: 2026-01-11T02:43:56.630591Z

## Inherits
- UIDragDetector
- LayerCollector
- DragAxis
- GuiObject
- ReferenceUIInstance
- SetDragStyleFunction()
1. [Enums](/docs/reference/engine/enums)
2. /
3. [UIDragDetectorDragStyle](/docs/reference/engine/enums/UIDragDetectorDragStyle)

English

Feedback

Engine Enum

UIDragDetectorDragStyle

---

Used with [UIDragDetector](/docs/reference/engine/classes/UIDragDetector) as the paradigm to generate proposed motion,
given a stream of input position vectors.

Items

| Name | Value | Summary |
| --- | --- | --- |
| TranslatePlane | 0 | 2D motion in the plane of the [LayerCollector](/docs/reference/engine/classes/LayerCollector). |
| TranslateLine | 1 | 1D motion along the detector's [DragAxis](/docs/reference/engine/classes/UIDragDetector#DragAxis). |
| Rotate | 2 | By default, rotation about the absolute center position of the detector's parent [GuiObject](/docs/reference/engine/classes/GuiObject). If [ReferenceUIInstance](/docs/reference/engine/classes/UIDragDetector#ReferenceUIInstance) is set, rotation happens about that instance's absolute center position. |
| Scriptable | 3 | Calculates desired motion via a custom function provided through [SetDragStyleFunction()](/docs/reference/engine/classes/UIDragDetector#SetDragStyleFunction). |