# UIGradient | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/UIGradient
Scraped: 2026-01-11T02:27:25.577905Z

## Inherits
- UIComponent
- UIGradient
- GuiObject
- Instance
- Object
- Color
- Transparency
- Offset
- Rotation
- GuiObjects
- Frame
- TextLabel
- TextButton
- ImageLabel
- ImageButton
- ViewportFrame
- ScrollingFrame
- TextBox
- TextStrokeColor3
- BackgroundColor3
- ImageColor3
- TextColor3
- Beam.Color
- Trail.Color
- AbsoluteSize
- Beam.Transparency
- Trail.Transparency
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [UIComponent](/docs/reference/engine/classes/UIComponent)
6. /
7. [UIGradient](/docs/reference/engine/classes/UIGradient)

English

Feedback

Engine Class

![UIGradient](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/UIGradient-Dark.webp)UIGradient

Applies a color and transparency gradient to the UI elements rendered by the
parent [GuiObject](/docs/reference/engine/classes/GuiObject).

---

Summary

Properties

|  |
| --- |
| [Color](#Color):[ColorSequence](/docs/reference/engine/datatypes/ColorSequence) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [Offset](#Offset):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [Rotation](#Rotation):[number](/docs/luau/numbers) |
| [Transparency](#Transparency):[NumberSequence](/docs/reference/engine/datatypes/NumberSequence) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

UIGradient applies a color and transparency gradient to the UI elements
rendered by the parent [GuiObject](/docs/reference/engine/classes/GuiObject). The appearance of the gradient is
configurable through its [Color](/docs/reference/engine/classes/UIGradient#Color)
([ColorSequence](/docs/reference/engine/datatypes/ColorSequence)), [Transparency](/docs/reference/engine/classes/UIGradient#Transparency)
([NumberSequence](/docs/reference/engine/datatypes/NumberSequence)), [Offset](/docs/reference/engine/classes/UIGradient#Offset)
([Vector2](/docs/reference/engine/datatypes/Vector2)), and [Rotation](/docs/reference/engine/classes/UIGradient#Rotation) (number).

A [UIGradient](/docs/reference/engine/classes/UIGradient) will not apply to child or descendant
[GuiObjects](/docs/reference/engine/classes/GuiObject). In order to apply the same gradient to multiple
objects, you will need multiple gradient instances.

See also [Appearance Modifiers](/docs/ui/appearance-modifiers) for more
information on [UIGradient](/docs/reference/engine/classes/UIGradient) objects and how they work.

#### Supported Objects

You can apply gradients to [Frame](/docs/reference/engine/classes/Frame), [TextLabel](/docs/reference/engine/classes/TextLabel),
[TextButton](/docs/reference/engine/classes/TextButton), [ImageLabel](/docs/reference/engine/classes/ImageLabel), [ImageButton](/docs/reference/engine/classes/ImageButton), and
[ViewportFrame](/docs/reference/engine/classes/ViewportFrame). However, [ScrollingFrame](/docs/reference/engine/classes/ScrollingFrame) and [TextBox](/docs/reference/engine/classes/TextBox) are
not currently supported.

#### Performance Considerations

In order to efficiently use a [UIGradient](/docs/reference/engine/classes/UIGradient), follow these principles:

* Avoid using more than 6 color stops on the [Color](/docs/reference/engine/classes/UIGradient#Color)
  sequence.
* Avoid using a [UIGradient](/docs/reference/engine/classes/UIGradient) on any object that applies a text stroke
  ([TextStrokeColor3](/docs/reference/engine/classes/TextLabel#TextStrokeColor3)), as the gradient will
  try to blend with strokes and borders, and may cause performance issues.
* Avoid setting [Color](/docs/reference/engine/classes/UIGradient#Color) and
  [Transparency](/docs/reference/engine/classes/UIGradient#Transparency) frequently: this causes the
  sequence of colors to rebuild often, which is expensive. If possible, set
  these properties only once and try to animate the
  [Offset](/docs/reference/engine/classes/UIGradient#Offset) or [Rotation](/docs/reference/engine/classes/UIGradient#Rotation)
  properties to achieve a similar effect. Alternatively, you can change the
  color of the parent [GuiObject](/docs/reference/engine/classes/GuiObject) using such properties as
  [BackgroundColor3](/docs/reference/engine/classes/GuiObject#BackgroundColor3),
  [ImageColor3](/docs/reference/engine/classes/ImageLabel#ImageColor3), or
  [TextColor3](/docs/reference/engine/classes/TextLabel#TextColor3).
* When applying an unchanging gradient on a UI element whose state changes a
  lot, there is a tradeoff between using a [UIGradient](/docs/reference/engine/classes/UIGradient) (processing
  time) and a static gradient image (memory).

---

API Reference

Properties

Color

Read Parallel

Determines the color blended with the parent GuiObject along the length of
the gradient.

UIGradient.Color:[ColorSequence](/docs/reference/engine/datatypes/ColorSequence)

This property describes the color to blend with the parent UI element
along the provided [ColorSequence](/docs/reference/engine/datatypes/ColorSequence). This property works in a
similar manner to [Beam.Color](/docs/reference/engine/classes/Beam#Color) or [Trail.Color](/docs/reference/engine/classes/Trail#Color), except that
it applies over an on-screen distance determined by the
[Offset](/docs/reference/engine/classes/UIGradient#Offset) and [Rotation](/docs/reference/engine/classes/UIGradient#Rotation).

Provide feedback

---

Enabled

Read Parallel

Whether the gradient is enabled or not.

UIGradient.Enabled:[boolean](/docs/luau/booleans)

Whether the gradient is enabled or not.

Provide feedback

---

Offset

Read Parallel

Determines the scalar translation of the gradient from the center of the
parent GuiObject.

UIGradient.Offset:[Vector2](/docs/reference/engine/datatypes/Vector2)

This property determines the scalar translation of the gradient from the
center of the parent [GuiObject](/docs/reference/engine/classes/GuiObject). It is a scalar translation,
meaning that the actual pixel offset is determined by the
[AbsoluteSize](/docs/reference/engine/classes/GuiBase2d#AbsoluteSize) of the parent
[GuiObject](/docs/reference/engine/classes/GuiObject). So, a value of (1, 0) would shift the gradient
horizontally to the right by a distance equal to the parent object's
on‑screen size. Depending on the [Rotation](/docs/reference/engine/classes/UIGradient#Rotation),
this may cause the gradient to be partially visible or not visible at all.

Also see [Rotation](/docs/reference/engine/classes/UIGradient#Rotation) which also affects the
geometry of the applied gradient.

Provide feedback

---

Rotation

Read Parallel

Determines the clockwise rotation in degrees of the gradient starting from
left to right.

UIGradient.Rotation:[number](/docs/luau/numbers)

This property determines the clockwise rotation in degrees of the
[UIGradient](/docs/reference/engine/classes/UIGradient) starting from left to right. The beginning and end
control points snap to the edges of the parent [GuiObject](/docs/reference/engine/classes/GuiObject), but
maintain the provided rotation.

Also see [Offset](/docs/reference/engine/classes/UIGradient#Offset) which also affects the geometry
of the applied gradient.

Provide feedback

---

Transparency

Read Parallel

Determines how much the parent GuiObject can be seen through along the
length of the gradient.

UIGradient.Transparency:[NumberSequence](/docs/reference/engine/datatypes/NumberSequence)

This property describes how opaque the parent UI element will be along the
provided [NumberSequence](/docs/reference/engine/datatypes/NumberSequence). This property works in a similar
manner to [Beam.Transparency](/docs/reference/engine/classes/Beam#Transparency) or [Trail.Transparency](/docs/reference/engine/classes/Trail#Transparency), except
that it applies over an on‑screen distance determined by the
[Offset](/docs/reference/engine/classes/UIGradient#Offset) and [Rotation](/docs/reference/engine/classes/UIGradient#Rotation).

Note that the envelope values of the
[NumberSequenceKeypoints](/docs/reference/engine/datatypes/NumberSequenceKeypoint) are ignored.

Provide feedback

---