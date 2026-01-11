# DragDetectorDragStyle | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/DragDetectorDragStyle
Scraped: 2026-01-11T02:46:55.916372Z

## Inherits
- DragDetector
- Axis
- TrackballRadialPullFactor
- TrackballRollFactor
- SetDragStyleFunction()
1. [Enums](/docs/reference/engine/enums)
2. /
3. [DragDetectorDragStyle](/docs/reference/engine/enums/DragDetectorDragStyle)

English

Feedback

Engine Enum

DragDetectorDragStyle

---

Used with [DragDetector](/docs/reference/engine/classes/DragDetector) as the paradigm to generate proposed motion,
given a stream of cursor rays.

Items

| Name | Value | Summary |
| --- | --- | --- |
| TranslateLine | 0 | 1D motion along the detector's [Axis](/docs/reference/engine/classes/DragDetector#Axis), by default the world Y axis. |
| TranslatePlane | 1 | 2D motion in the plane perpendicular to the detector's [Axis](/docs/reference/engine/classes/DragDetector#Axis), by default the world XZ plane. |
| TranslatePlaneOrLine | 2 | 2D motion in the plane perpendicular to the detector's [Axis](/docs/reference/engine/classes/DragDetector#Axis) and, when the modifier is active, 1D motion along the detector's [Axis](/docs/reference/engine/classes/DragDetector#Axis). |
| TranslateLineOrPlane | 3 | 1D motion along the detector's [Axis](/docs/reference/engine/classes/DragDetector#Axis) and, when the modifier is active, 2D motion in the plane perpendicular to the detector's [Axis](/docs/reference/engine/classes/DragDetector#Axis). |
| TranslateViewPlane | 4 | 2D motion in the plane perpendicular to the camera's view. In this mode, the plane is constantly updated, even while dragging, and will always face the camera's current view. |
| RotateAxis | 5 | Rotation about the detector's [Axis](/docs/reference/engine/classes/DragDetector#Axis), by default the world Y axis. |
| RotateTrackball | 6 | Trackball rotation, further customized through the [TrackballRadialPullFactor](/docs/reference/engine/classes/DragDetector#TrackballRadialPullFactor) and [TrackballRollFactor](/docs/reference/engine/classes/DragDetector#TrackballRollFactor) properties. |
| Scriptable | 7 | Calculates desired motion via a custom function provided through [SetDragStyleFunction()](/docs/reference/engine/classes/DragDetector#SetDragStyleFunction). |
| BestForDevice | 8 | TranslatePlaneOrLine for mouse and gamepad; TranslatePlane for touch; 6DOF for VR. |