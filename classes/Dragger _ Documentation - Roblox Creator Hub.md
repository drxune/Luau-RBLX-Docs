# Dragger | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Dragger
Scraped: 2026-01-11T02:39:37.155170Z

## Inherits
- Object
- Instance
- Dragger
- FilteringEnabled
- Mouse
- Dragger:MouseDown()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Dragger](/docs/reference/engine/classes/Dragger)

English

Feedback

Engine Class

Dragger

Deprecated

A helper object used to create tools that can drag parts.

This class has been deprecated, as it does not work well with
[FilteringEnabled](/docs/reference/engine/classes/Workspace#FilteringEnabled), and should not be used in
new work.

---

Summary

Methods

|  |
| --- |
| [AxisRotate](#AxisRotate)(axis: [Enum.Axis](/docs/reference/engine/enums/Axis)):() |
| [MouseDown](#MouseDown)(mousePart: [Instance](/docs/reference/engine/datatypes/Instance),pointOnMousePart: [Vector3](/docs/reference/engine/datatypes/Vector3),parts: Instances):() |
| [MouseMove](#MouseMove)(mouseRay: [Ray](/docs/reference/engine/datatypes/Ray)):() |
| [MouseUp](#MouseUp)():() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The Dragger object is a helper object used to create tools that can drag
parts. It is expected (but not required) to be used with [Mouse](/docs/reference/engine/classes/Mouse) events.

Its implementation is primarily used in the RbxStamper library.

---

API Reference

Methods

AxisRotate

Rotates the currently dragged part(s) by 90 degrees on the given axis.

Dragger:AxisRotate(axis:[Enum.Axis](/docs/reference/engine/enums/Axis)):()

Parameters

|  |
| --- |
| axis:[Enum.Axis](/docs/reference/engine/enums/Axis) Default Value: "X" |

Returns

()

Rotates the currently dragged part(s) by 90 degrees on the given axis.

Provide feedback

---

MouseDown

Initializes a dragging action, specifying which parts to use when
dragging.

Dragger:MouseDown(

mousePart:[Instance](/docs/reference/engine/datatypes/Instance), pointOnMousePart:[Vector3](/docs/reference/engine/datatypes/Vector3), parts:Instances

):()

Parameters

|  |
| --- |
| mousePart:[Instance](/docs/reference/engine/datatypes/Instance) |
| pointOnMousePart:[Vector3](/docs/reference/engine/datatypes/Vector3) |
| parts:Instances |

Returns

()

Initializes a dragging action, specifying which parts to use when
dragging.

Provide feedback

---

MouseMove

Tries to move the currently dragged part to the point where MouseRay hits
another part.

Dragger:MouseMove(mouseRay:[Ray](/docs/reference/engine/datatypes/Ray)):()

Parameters

|  |
| --- |
| mouseRay:[Ray](/docs/reference/engine/datatypes/Ray) |

Returns

()

Tries to move the currently dragged part to the point where MouseRay hits
another part.

Provide feedback

---

MouseUp

Stops the current dragging action (made by [Dragger:MouseDown()](/docs/reference/engine/classes/Dragger#MouseDown)).

Dragger:MouseUp():()

Returns

()

Stops the current dragging action (made by [Dragger:MouseDown()](/docs/reference/engine/classes/Dragger#MouseDown))

Provide feedback

---