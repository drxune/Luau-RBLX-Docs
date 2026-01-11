# UICorner | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/UICorner
Scraped: 2026-01-11T02:31:14.129441Z

## Inherits
- UIComponent
- UICorner
- GuiObject
- Instance
- Object
- CornerRadius
- ScrollingFrame
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [UIComponent](/docs/reference/engine/classes/UIComponent)
6. /
7. [UICorner](/docs/reference/engine/classes/UICorner)

English

Feedback

Engine Class

![UICorner](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/UICorner-Dark.webp)UICorner

UI modifier which applies deformation to corners of its parent
[GuiObject](/docs/reference/engine/classes/GuiObject).

---

Summary

Properties

|  |
| --- |
| [CornerRadius](#CornerRadius):[UDim](/docs/reference/engine/datatypes/UDim) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[UICorner](/docs/reference/engine/classes/UICorner) is a modifier which applies deformation to corners of its
parent [GuiObject](/docs/reference/engine/classes/GuiObject). Input, but not descendants, will be clipped to the
round corner area. See [here](/docs/ui/appearance-modifiers#corners) for
examples.

In order to keep the circular shape of round corners with the
[CornerRadius](/docs/reference/engine/classes/UICorner#CornerRadius) value ([UDim](/docs/reference/engine/datatypes/UDim)), the radius
is internally calculated as follows:

* The radius of the X axis is always the same as the radius of Y axis.
* [Scale](/docs/reference/engine/datatypes/UDim#Scale) rounding will always apply to the minimum
  width or height.
* Rounded rectangles will always be in a "pill" shape if
  [CornerRadius](/docs/reference/engine/classes/UICorner#CornerRadius) is set to a value that leads to a
  calculated result greater than half of the rectangle's minimum width or
  height.

Alternatively, rounded corners can be accomplished using slices which are
suitable for decorative borders that are not simply rounded. See
[9‑Slice Design](/docs/ui/9-slice) for details.

Note that [UICorner](/docs/reference/engine/classes/UICorner) can not be applied to a [ScrollingFrame](/docs/reference/engine/classes/ScrollingFrame).

---

API Reference

Properties

CornerRadius

Read Parallel

Determines the radius of the component.

UICorner.CornerRadius:[UDim](/docs/reference/engine/datatypes/UDim)

A [UDim](/docs/reference/engine/datatypes/UDim) property that determines the radius of the
[UICorner](/docs/reference/engine/classes/UICorner) component, internally calculated as follows:

* The radius of the X axis is always the same as the radius of Y
  axis.
* [Scale](/docs/reference/engine/datatypes/UDim#Scale) rounding will always apply to the
  minimum width or height.
* Rounded rectangles will always be in a "pill" shape if
  [CornerRadius](/docs/reference/engine/classes/UICorner#CornerRadius) is set to a value that leads
  to a calculated result greater than half of the rectangle's minimum
  width or height.

Provide feedback

---