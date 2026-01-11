# UIDragDetectorBoundingBehavior | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/UIDragDetectorBoundingBehavior
Scraped: 2026-01-11T02:44:10.337710Z

## Inherits
- UIDragDetector
- UIDragDetector.BoundingUI
- BoundingUI
1. [Enums](/docs/reference/engine/enums)
2. /
3. [UIDragDetectorBoundingBehavior](/docs/reference/engine/enums/UIDragDetectorBoundingBehavior)

English

Feedback

Engine Enum

UIDragDetectorBoundingBehavior

---

Used with [UIDragDetector](/docs/reference/engine/classes/UIDragDetector) to determine bounding behavior of the dragged
UI object when [UIDragDetector.BoundingUI](/docs/reference/engine/classes/UIDragDetector#BoundingUI) is set.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Automatic | 0 | Mimics EntireObject behavior for a UI object that's entirely contained by the [BoundingUI](/docs/reference/engine/classes/UIDragDetector#BoundingUI), or else HitPoint for a UI object that's partially outside the [BoundingUI](/docs/reference/engine/classes/UIDragDetector#BoundingUI). |
| EntireObject | 1 | Bounds the entire dragged UI object within the [BoundingUI](/docs/reference/engine/classes/UIDragDetector#BoundingUI). |
| HitPoint | 2 | Bounds the dragged UI only by the exact hit/grab point and its respective position after translation/rotation. |