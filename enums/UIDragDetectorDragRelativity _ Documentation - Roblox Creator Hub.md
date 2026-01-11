# UIDragDetectorDragRelativity | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/UIDragDetectorDragRelativity
Scraped: 2026-01-11T02:46:33.107352Z

## Inherits
- DragDetector
- SetDragStyleFunction()
- AddConstraintFunction()
- DragSpace
1. [Enums](/docs/reference/engine/enums)
2. /
3. [UIDragDetectorDragRelativity](/docs/reference/engine/enums/UIDragDetectorDragRelativity)

English

Feedback

Engine Enum

UIDragDetectorDragRelativity

---

Used with [DragDetector](/docs/reference/engine/classes/DragDetector) to set the paradigm which defines the
relativity of inputs/outputs from a custom drag function registered through
[SetDragStyleFunction()](/docs/reference/engine/classes/UIDragDetector#SetDragStyleFunction) or
[AddConstraintFunction()](/docs/reference/engine/classes/UIDragDetector#AddConstraintFunction).

Items

| Name | Value | Summary |
| --- | --- | --- |
| Absolute | 0 | Designates the input and return values as the absolute target position/rotation in the space defined by [DragSpace](/docs/reference/engine/classes/UIDragDetector#DragSpace). |
| Relative | 1 | Designates the input and return values as the change from the current position/rotation in the space defined by [DragSpace](/docs/reference/engine/classes/UIDragDetector#DragSpace). |