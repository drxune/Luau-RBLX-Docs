# ScrollingFrame | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ScrollingFrame
Scraped: 2026-01-11T02:36:53.717259Z

## Tags
- Not Replicated

## Inherits
- GuiObject
- ScrollingFrame
- Frame
- GuiBase2d
- Instance
- Object
- CanvasSize
- AutomaticCanvasSize
- ScrollingFrame.CanvasSize
- AbsoluteCanvasSize
- ScrollBarThickness
- TopImage
- BottomImage
- TopImageContent
- BottomImageContent
- MidImage
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [GuiObject](/docs/reference/engine/classes/GuiObject)
6. /
7. [ScrollingFrame](/docs/reference/engine/classes/ScrollingFrame)

English

Feedback

Engine Class

![ScrollingFrame](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/ScrollingFrame-Dark.webp)ScrollingFrame

ScrollingFrame is a special [Frame](/docs/reference/engine/classes/Frame) type with built-in scrolling
interactivity and different ways to customize how the scrolling works.

---

Summary

Properties

|  |
| --- |
| [AbsoluteCanvasSize](#AbsoluteCanvasSize):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [AbsoluteWindowSize](#AbsoluteWindowSize):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [AutomaticCanvasSize](#AutomaticCanvasSize):[Enum.AutomaticSize](/docs/reference/engine/enums/AutomaticSize) |
| [BottomImage](#BottomImage):ContentId |
| [BottomImageContent](#BottomImageContent):[Content](/docs/reference/engine/datatypes/Content) |
| [CanvasPosition](#CanvasPosition):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [CanvasSize](#CanvasSize):[UDim2](/docs/reference/engine/datatypes/UDim2) |
| [ElasticBehavior](#ElasticBehavior):[Enum.ElasticBehavior](/docs/reference/engine/enums/ElasticBehavior) |
| [HorizontalScrollBarInset](#HorizontalScrollBarInset):[Enum.ScrollBarInset](/docs/reference/engine/enums/ScrollBarInset) |
| [MidImage](#MidImage):ContentId |
| [MidImageContent](#MidImageContent):[Content](/docs/reference/engine/datatypes/Content) |
| [ScrollBarImageColor3](#ScrollBarImageColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [ScrollBarImageTransparency](#ScrollBarImageTransparency):[number](/docs/luau/numbers) |
| [ScrollBarThickness](#ScrollBarThickness):[number](/docs/luau/numbers) |
| [ScrollingDirection](#ScrollingDirection):[Enum.ScrollingDirection](/docs/reference/engine/enums/ScrollingDirection) |
| [ScrollingEnabled](#ScrollingEnabled):[boolean](/docs/luau/booleans) |
| [TopImage](#TopImage):ContentId |
| [TopImageContent](#TopImageContent):[Content](/docs/reference/engine/datatypes/Content) |
| [VerticalScrollBarInset](#VerticalScrollBarInset):[Enum.ScrollBarInset](/docs/reference/engine/enums/ScrollBarInset) |
| [VerticalScrollBarPosition](#VerticalScrollBarPosition):[Enum.VerticalScrollBarPosition](/docs/reference/engine/enums/VerticalScrollBarPosition) |

Inherited Members

50 inherited from [GuiObject](/docs/reference/engine/classes/GuiObject)

12 inherited from [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

ScrollingFrame is a special [Frame](/docs/reference/engine/classes/Frame) type with built-in scrolling
interactivity and different ways to customize how the scrolling works.

![Example ScrollingFrame on the screen containing a tabbed category bar and a list of magical items for the player to consider purchasing.](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/ScrollingFrame-Example.jpg)

---

API Reference

Properties

AbsoluteCanvasSize

Read Only

Not Replicated

The size of the area that is scrollable, in offsets.

ScrollingFrame.AbsoluteCanvasSize:[Vector2](/docs/reference/engine/datatypes/Vector2)

The size of the area that is scrollable, in offsets. This property is set
to the maximum of the [CanvasSize](/docs/reference/engine/classes/ScrollingFrame#CanvasSize)
property and the size of the children if
[AutomaticCanvasSize](/docs/reference/engine/classes/ScrollingFrame#AutomaticCanvasSize) is set to
something other than [Enum.AutomaticSize.None](/docs/reference/engine/enums/AutomaticSize#None).

Provide feedback

---

AbsoluteWindowSize

Read Only

Not Replicated

The size of the frame, in offsets, without the scroll bars.

ScrollingFrame.AbsoluteWindowSize:[Vector2](/docs/reference/engine/datatypes/Vector2)

The size of the frame, in offsets, without the scroll bars.

Provide feedback

---

AutomaticCanvasSize

Read Parallel

Determines whether [ScrollingFrame.CanvasSize](/docs/reference/engine/classes/ScrollingFrame#CanvasSize) is resized based on
child content.

ScrollingFrame.AutomaticCanvasSize:[Enum.AutomaticSize](/docs/reference/engine/enums/AutomaticSize)

This property is used to automatically size parent UI objects based on the
size of its descendants. You can use this property to dynamically add text
and other content to a ScrollingFrame at edit or run time and the size
will adjust to fit that content.

When this property is set to an [Enum.AutomaticSize](/docs/reference/engine/enums/AutomaticSize) value other than
[None](/docs/reference/engine/enums/AutomaticSize),
[AbsoluteCanvasSize](/docs/reference/engine/classes/ScrollingFrame#AbsoluteCanvasSize) may resize
depending on its child content.

Provide feedback

---

BottomImage

Read Parallel

Image that displays on the bottom of a vertical scroll bar, or the right
of a horizontal scroll bar (rotated 90° counterclockwise for a
horizontal scroll bar).

ScrollingFrame.BottomImage:ContentId

Image that displays on the bottom of a vertical scroll bar, or the right
of a horizontal scroll bar (rotated 90° counterclockwise for a
horizontal scroll bar).

![Diagram showing the three image asset elements which construct a scrolling frame's scroll bar.](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/ScrollingFrame-Scroll-Bar-Elements.png)

Provide feedback

---

BottomImageContent

Read Parallel

Image that displays on the bottom of a vertical scroll bar, or the right
of a horizontal scroll bar (rotated 90° counterclockwise for a
horizontal scroll bar). Only supports asset URIs as textures.

ScrollingFrame.BottomImageContent:[Content](/docs/reference/engine/datatypes/Content)

Image that displays on the bottom of a vertical scroll bar, or the right
of a horizontal scroll bar (rotated 90° counterclockwise for a
horizontal scroll bar).

![Diagram showing the three image asset elements which construct a scrolling frame's scroll bar.](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/ScrollingFrame-Scroll-Bar-Elements.png)

Provide feedback

---

CanvasPosition

Read Parallel

Reflects the current positional offset of the canvas within the frame,
in pixels, and sets the position of scroll bars accordingly.

ScrollingFrame.CanvasPosition:[Vector2](/docs/reference/engine/datatypes/Vector2)

Reflects the current positional offset of the canvas within the frame,
in pixels, and sets the position of scroll bars accordingly. Note that
this property doesn't do anything if scroll bars aren't visible.

Provide feedback

---

CanvasSize

Read Parallel

Determines the size of the scrollable area.

ScrollingFrame.CanvasSize:[UDim2](/docs/reference/engine/datatypes/UDim2)

Determines the size of the scrollable area. For an adaptive alternative
based on the overall size of children within the ScrollingFrame,
consider using
[AutomaticCanvasSize](/docs/reference/engine/classes/ScrollingFrame#AutomaticCanvasSize).

Provide feedback

---

ElasticBehavior

Read Parallel

Determines if and when elastic scrolling is allowed on touch‑enabled
devices.

ScrollingFrame.ElasticBehavior:[Enum.ElasticBehavior](/docs/reference/engine/enums/ElasticBehavior)

This property determines if and when elastic scrolling is allowed on
touch‑enabled devices. Defaults to [WhenScrollable](/docs/reference/engine/enums/ElasticBehavior).

Provide feedback

---

HorizontalScrollBarInset

Read Parallel

Indicates whether [CanvasSize](/docs/reference/engine/classes/ScrollingFrame#CanvasSize) is inset by
[ScrollBarThickness](/docs/reference/engine/classes/ScrollingFrame#ScrollBarThickness) on the
horizontal axis.

ScrollingFrame.HorizontalScrollBarInset:[Enum.ScrollBarInset](/docs/reference/engine/enums/ScrollBarInset)

Indicates whether [CanvasSize](/docs/reference/engine/classes/ScrollingFrame#CanvasSize) is inset by
[ScrollBarThickness](/docs/reference/engine/classes/ScrollingFrame#ScrollBarThickness) on the
horizontal axis.

Provide feedback

---

MidImage

Read Parallel

Image which spans the area between
[TopImage](/docs/reference/engine/classes/ScrollingFrame#TopImage) and
[BottomImage](/docs/reference/engine/classes/ScrollingFrame#BottomImage) (rotated 90°
counterclockwise for a horizontal scroll bar).

ScrollingFrame.MidImage:ContentId

Image which spans the area between
[TopImage](/docs/reference/engine/classes/ScrollingFrame#TopImage) and
[BottomImage](/docs/reference/engine/classes/ScrollingFrame#BottomImage) (rotated 90°
counterclockwise for a horizontal scroll bar). This image automatically
scales to fill the space between the cap segments.

![Diagram showing the three image asset elements which construct a scrolling frame's scroll bar.](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/ScrollingFrame-Scroll-Bar-Elements.png)

Provide feedback

---

MidImageContent

Read Parallel

Image which spans the area between
[TopImageContent](/docs/reference/engine/classes/ScrollingFrame#TopImageContent) and
[BottomImageContent](/docs/reference/engine/classes/ScrollingFrame#BottomImageContent) (rotated
90° counterclockwise for a horizontal scroll bar). Only supports asset
URIs as textures.

ScrollingFrame.MidImageContent:[Content](/docs/reference/engine/datatypes/Content)

Image which spans the area between
[TopImage](/docs/reference/engine/classes/ScrollingFrame#TopImage) and
[BottomImage](/docs/reference/engine/classes/ScrollingFrame#BottomImage) (rotated 90°
counterclockwise for a horizontal scroll bar). This image automatically
scales to fill the space between the cap segments.

![Diagram showing the three image asset elements which construct a scrolling frame's scroll bar.](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/ScrollingFrame-Scroll-Bar-Elements.png)

Provide feedback

---

ScrollBarImageColor3

Read Parallel

Determines how the rendered scroll bar images are colorized.

ScrollingFrame.ScrollBarImageColor3:[Color3](/docs/reference/engine/datatypes/Color3)

Determines how the scroll bar images
([TopImage](/docs/reference/engine/classes/ScrollingFrame#TopImage),
[MidImage](/docs/reference/engine/classes/ScrollingFrame#MidImage),
[BottomImage](/docs/reference/engine/classes/ScrollingFrame#BottomImage)) are colorized. When set to
white, no colorization occurs. This property is useful for reusing image
assets; if the source images are completely white with transparency, you
can set the color of the entire scroll bar at once.

Provide feedback

---

ScrollBarImageTransparency

Read Parallel

Determines the opacity of the scroll bar images.

ScrollingFrame.ScrollBarImageTransparency:[number](/docs/luau/numbers)

Determines the opacity of the scroll bar images
([TopImage](/docs/reference/engine/classes/ScrollingFrame#TopImage),
[MidImage](/docs/reference/engine/classes/ScrollingFrame#MidImage),
[BottomImage](/docs/reference/engine/classes/ScrollingFrame#BottomImage)). A value of 0 is
completely opaque and a value of 1 is completely transparent
(invisible).

Provide feedback

---

ScrollBarThickness

Read Parallel

Thickness of the scroll bar in pixels; applies to both horizontal and
vertical scroll bars.

ScrollingFrame.ScrollBarThickness:[number](/docs/luau/numbers)

Thickness of the scroll bar in pixels; applies to both horizontal and
vertical scroll bars. If set to 0, no scroll bars are rendered.

Provide feedback

---

ScrollingDirection

Read Parallel

Determines the direction(s) in which scrolling is allowed.

ScrollingFrame.ScrollingDirection:[Enum.ScrollingDirection](/docs/reference/engine/enums/ScrollingDirection)

This property determines the direction(s) in which scrolling is allowed.
If scrolling is disallowed in a direction, the associated scroll bar will
not appear. Defaults to [Enum.ScrollingDirection.XY](/docs/reference/engine/enums/ScrollingDirection#XY).

Provide feedback

---

ScrollingEnabled

Read Parallel

Determines whether scrolling is allowed on the frame.

ScrollingFrame.ScrollingEnabled:[boolean](/docs/luau/booleans)

Determines whether scrolling is allowed on the frame. If false, no
scroll bars will be rendered.

Provide feedback

---

TopImage

Read Parallel

Image which displays on the top of a vertical scroll bar, or the left of a
horizontal scroll bar (rotated 90° counterclockwise for a horizontal
scroll bar).

ScrollingFrame.TopImage:ContentId

Image which displays on the top of a vertical scroll bar, or the left of a
horizontal scroll bar (rotated 90° counterclockwise for a horizontal
scroll bar).

![Diagram showing the three image asset elements which construct a scrolling frame's scroll bar.](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/ScrollingFrame-Scroll-Bar-Elements.png)

Provide feedback

---

TopImageContent

Read Parallel

ScrollingFrame.TopImageContent:[Content](/docs/reference/engine/datatypes/Content)

Provide feedback

---

VerticalScrollBarInset

Read Parallel

Indicates whether [CanvasSize](/docs/reference/engine/classes/ScrollingFrame#CanvasSize) is inset by
[ScrollBarThickness](/docs/reference/engine/classes/ScrollingFrame#ScrollBarThickness) on the
vertical axis.

ScrollingFrame.VerticalScrollBarInset:[Enum.ScrollBarInset](/docs/reference/engine/enums/ScrollBarInset)

Indicates whether [CanvasSize](/docs/reference/engine/classes/ScrollingFrame#CanvasSize) is inset by
[ScrollBarThickness](/docs/reference/engine/classes/ScrollingFrame#ScrollBarThickness) on the
vertical axis.

Provide feedback

---

VerticalScrollBarPosition

Read Parallel

Indicates whether the vertical scroll bar is positioned to the left or
right of the canvas.

ScrollingFrame.VerticalScrollBarPosition:[Enum.VerticalScrollBarPosition](/docs/reference/engine/enums/VerticalScrollBarPosition)

Indicates whether the vertical scroll bar is positioned to the left or
right of the canvas. Defaults to [Enum.VerticalScrollBarPosition.Right](/docs/reference/engine/enums/VerticalScrollBarPosition#Right).

Provide feedback

---