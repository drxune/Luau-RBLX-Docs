# UIStroke | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/UIStroke
Scraped: 2026-01-11T02:41:21.257768Z

## Inherits
- UIComponent
- UIStroke
- Instance
- Object
- Color
- Thickness
- Transparency
- LineJoinMode
- BorderStrokePosition
- BorderOffset
- UIGradient
- StrokeSizingMode
- BackgroundTransparency
- TextTransparency
- TextLabel.TextTransparency
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [UIComponent](/docs/reference/engine/classes/UIComponent)
6. /
7. [UIStroke](/docs/reference/engine/classes/UIStroke)

English

Feedback

Engine Class

![UIStroke](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/UIStroke-Dark.webp)UIStroke

Applies an outline to text or a UI border.

---

Summary

Properties

|  |
| --- |
| [ApplyStrokeMode](#ApplyStrokeMode):[Enum.ApplyStrokeMode](/docs/reference/engine/enums/ApplyStrokeMode) |
| [BorderOffset](#BorderOffset):[UDim](/docs/reference/engine/datatypes/UDim) |
| [BorderStrokePosition](#BorderStrokePosition):[Enum.BorderStrokePosition](/docs/reference/engine/enums/BorderStrokePosition) |
| [Color](#Color):[Color3](/docs/reference/engine/datatypes/Color3) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [LineJoinMode](#LineJoinMode):[Enum.LineJoinMode](/docs/reference/engine/enums/LineJoinMode) |
| [StrokeSizingMode](#StrokeSizingMode):[Enum.StrokeSizingMode](/docs/reference/engine/enums/StrokeSizingMode) |
| [Thickness](#Thickness):[number](/docs/luau/numbers) |
| [Transparency](#Transparency):[number](/docs/luau/numbers) |
| [ZIndex](#ZIndex):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[UIStroke](/docs/reference/engine/classes/UIStroke) applies an outline to text or a UI border. Some properties
may require enabling the
[Improved UIStrokes beta](https://devforum.roblox.com/t/studio-beta-uistroke-improvements-scaling-offsets-and-more/3958036).

Key features include:

* Adjust the [Color](/docs/reference/engine/classes/UIStroke#Color) and
  [Thickness](/docs/reference/engine/classes/UIStroke#Thickness) of the stroke outline.
* Change the stroke [Transparency](/docs/reference/engine/classes/UIStroke#Transparency) independently
  from the text or UI object.
* Choose the [LineJoinMode](/docs/reference/engine/classes/UIStroke#LineJoinMode) of the stroke (round,
  bevel, or miter).
* Specify the [BorderStrokePosition](/docs/reference/engine/classes/UIStroke#BorderStrokePosition) on
  its parent's border and/or an additional
  [BorderOffset](/docs/reference/engine/classes/UIStroke#BorderOffset) to the stroke's position.
* Add a gradient to the stroke via the [UIGradient](/docs/reference/engine/classes/UIGradient) instance.
* Use [rich text](/docs/ui/rich-text) tags to add stroke to inline text
  segments.

For more details on the [UIStroke](/docs/reference/engine/classes/UIStroke) object, see
[Appearance Modifiers](/docs/ui/appearance-modifiers).

---

API Reference

Properties

ApplyStrokeMode

Read Parallel

Determines whether to apply the stroke to the object's border instead of
the text itself.

UIStroke.ApplyStrokeMode:[Enum.ApplyStrokeMode](/docs/reference/engine/enums/ApplyStrokeMode)

When a [UIStroke](/docs/reference/engine/classes/UIStroke) instance is applied to a text object, this
property determines whether to apply the stroke to the object's border
instead of the text itself.

![](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/UIStroke-As-Text-Outline.png)


ApplyStrokeMode = [Contextual](/docs/reference/engine/enums/ApplyStrokeMode#Contextual)


![](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/UIStroke-Stroke-Mode-Border.png)


ApplyStrokeMode = [Border](/docs/reference/engine/enums/ApplyStrokeMode#Border)

Provide feedback

---

BorderOffset

Read Parallel

Specifies an additional offset to the stroke's position, relative to the
parent's minimum height or width.

UIStroke.BorderOffset:[UDim](/docs/reference/engine/datatypes/UDim)

This property specifies an additional offset ([UDim](/docs/reference/engine/datatypes/UDim)) to the
stroke's position, relative to the parent's minimum height or width.

![](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/UIStroke-BorderOffset-Out.png)


BorderOffset = (0.15, 0)


![](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/UIStroke-BorderOffset-In.png)


BorderOffset = (0, -16)

Provide feedback

---

BorderStrokePosition

Read Parallel

Determines the stroke's position on its parent's border.

UIStroke.BorderStrokePosition:[Enum.BorderStrokePosition](/docs/reference/engine/enums/BorderStrokePosition)

This property determines the stroke's position on its parent's border as
an [Enum.BorderStrokePosition](/docs/reference/engine/enums/BorderStrokePosition) value.

![](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/UIStroke-BorderStrokePosition-Center.png)


BorderStrokePosition = [Center](/docs/reference/engine/enums/BorderStrokePosition#Center)


![](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/UIStroke-BorderStrokePosition-Inner.png)


BorderStrokePosition = [Inner](/docs/reference/engine/enums/BorderStrokePosition#Inner)


![](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/UIStroke-BorderStrokePosition-Outer.png)


BorderStrokePosition = [Outer](/docs/reference/engine/enums/BorderStrokePosition#Outer)

Provide feedback

---

Color

Read Parallel

Determines the stroke color.

UIStroke.Color:[Color3](/docs/reference/engine/datatypes/Color3)

Determines the [UIStroke](/docs/reference/engine/classes/UIStroke) color. You can also insert a
[UIGradient](/docs/reference/engine/classes/UIGradient) instance as a child to create gradient strokes.

![](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/UIStroke-Color-Solid.png)


Color = (0, 95, 225)


![](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/UIStroke-Color-Gradient.png)


UIStroke with [UIGradient](/docs/reference/engine/classes/UIGradient) child

Provide feedback

---

Enabled

Read Parallel

Determines whether the stroke in visible.

UIStroke.Enabled:[boolean](/docs/luau/booleans)

This property determines whether the [UIStroke](/docs/reference/engine/classes/UIStroke) is visible. When set
to false, the stroke will not be rendered. Defaults to true.

Provide feedback

---

LineJoinMode

Read Parallel

Determines how corners are interpreted.

UIStroke.LineJoinMode:[Enum.LineJoinMode](/docs/reference/engine/enums/LineJoinMode)

This property determines how corners are interpreted. It accepts an
[Enum.LineJoinMode](/docs/reference/engine/enums/LineJoinMode) value of either [Round](/docs/reference/engine/enums/LineJoinMode#Round)
(default), [Bevel](/docs/reference/engine/enums/LineJoinMode#Bevel), or
[Miter](/docs/reference/engine/enums/LineJoinMode#Miter).

![](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/UIStroke-LineJoinMode-Round.png)


LineJoinMode = [Round](/docs/reference/engine/enums/LineJoinMode#Round)


![](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/UIStroke-LineJoinMode-Bevel.png)


LineJoinMode = [Bevel](/docs/reference/engine/enums/LineJoinMode#Bevel)


![](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/UIStroke-LineJoinMode-Miter.png)


LineJoinMode = [Miter](/docs/reference/engine/enums/LineJoinMode#Miter)

Provide feedback

---

StrokeSizingMode

Read Parallel

Determines whether the stroke's [Thickness](/docs/reference/engine/classes/UIStroke#Thickness) will
be measured in pixels or be relative to the parent.

UIStroke.StrokeSizingMode:[Enum.StrokeSizingMode](/docs/reference/engine/enums/StrokeSizingMode)

This property determines whether the stroke's
[Thickness](/docs/reference/engine/classes/UIStroke#Thickness) will be measured in pixels or be
scaled relative to the parent. See [Enum.StrokeSizingMode](/docs/reference/engine/enums/StrokeSizingMode) for further
details.

Provide feedback

---

Thickness

Read Parallel

Determines the stroke's thickness.

UIStroke.Thickness:[number](/docs/luau/numbers)

This property determines the stroke's thickness, measured in pixels
(default) or scaled relative to the parent, depending on
[StrokeSizingMode](/docs/reference/engine/classes/UIStroke#StrokeSizingMode).

![](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/UIStroke-Thickness-4.png)


Thickness = 4


![](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/UIStroke-Thickness-12.png)


Thickness = 12

Be mindful of [tweening](/docs/ui/animation) this [UIStroke](/docs/reference/engine/classes/UIStroke)
property when applied to text objects. This renders and stores many glyph
sizes each frame, potentially causing performance issues or text
flickering.

Provide feedback

---

Transparency

Read Parallel

Sets the stroke opacity independently of the parent object's
[BackgroundTransparency](/docs/reference/engine/classes/GuiObject#BackgroundTransparency) or
[TextTransparency](/docs/reference/engine/classes/TextLabel#TextTransparency).

UIStroke.Transparency:[number](/docs/luau/numbers)

This property sets the stroke opacity independently of the parent object's
[BackgroundTransparency](/docs/reference/engine/classes/GuiObject#BackgroundTransparency) or
[TextTransparency](/docs/reference/engine/classes/TextLabel#TextTransparency). This allows you to
render text and borders that are "hollow" (consisting of only an outline).

![](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/UIStroke-Transparency-A.png)


Transparency = 0.5  ·  [TextLabel.TextTransparency](/docs/reference/engine/classes/TextLabel#TextTransparency) = 0


![](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/UIStroke-Transparency-B.png)


Transparency = 0  ·  [TextLabel.TextTransparency](/docs/reference/engine/classes/TextLabel#TextTransparency) = 1

Provide feedback

---

ZIndex

Read Parallel

Determines the order in which the stroke renders relative to sibling
[UIStroke](/docs/reference/engine/classes/UIStroke) instances.

UIStroke.ZIndex:[number](/docs/luau/numbers)

This property determines the order in which the stroke renders relative to
sibling [UIStroke](/docs/reference/engine/classes/UIStroke) instances. Those with a lower ZIndex render
under (behind) those with a higher ZIndex.

Note that the rendering order for [UIStroke](/docs/reference/engine/classes/UIStroke) instances with the same
ZIndex is undefined. Do not apply multiple [UIStroke](/docs/reference/engine/classes/UIStroke) instances
with the same ZIndex if their rendering order matters.

Provide feedback

---