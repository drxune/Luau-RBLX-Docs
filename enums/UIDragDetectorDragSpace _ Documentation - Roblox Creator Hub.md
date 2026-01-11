# UIDragDetectorDragSpace | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/UIDragDetectorDragSpace
Scraped: 2026-01-11T02:43:07.627032Z

## Inherits
- DragDetector
- SetDragStyleFunction()
- AddConstraintFunction()
- GuiObject
- LayerCollector
- ReferenceUIInstance
- DragRelativity
- DragUDim2
1. [Enums](/docs/reference/engine/enums)
2. /
3. [UIDragDetectorDragSpace](/docs/reference/engine/enums/UIDragDetectorDragSpace)

English

Feedback

Engine Enum

UIDragDetectorDragSpace

---

Used with [DragDetector](/docs/reference/engine/classes/DragDetector) to set the paradigm which defines the space of
inputs/outputs from a custom drag function registered through
[SetDragStyleFunction()](/docs/reference/engine/classes/UIDragDetector#SetDragStyleFunction) or
[AddConstraintFunction()](/docs/reference/engine/classes/UIDragDetector#AddConstraintFunction).

Items

| Name | Value | Summary |
| --- | --- | --- |
| Parent | 0 | Designates the input and return values' space as the local space of the detector's parent [GuiObject](/docs/reference/engine/classes/GuiObject). |
| LayerCollector | 1 | Designates the input and return values' space as that of the [LayerCollector](/docs/reference/engine/classes/LayerCollector). |
| Reference | 2 | Designates the input and return values' space as that of the [ReferenceUIInstance](/docs/reference/engine/classes/UIDragDetector#ReferenceUIInstance). For [DragRelativity](/docs/reference/engine/classes/UIDragDetector#DragRelativity) and [DragUDim2](/docs/reference/engine/classes/UIDragDetector#DragUDim2) purposes, the (0, 0) origin is the absolute center position of the [ReferenceUIInstance](/docs/reference/engine/classes/UIDragDetector#ReferenceUIInstance).  If [ReferenceUIInstance](/docs/reference/engine/classes/UIDragDetector#ReferenceUIInstance) is not nil, this will behave the same as Parent. |