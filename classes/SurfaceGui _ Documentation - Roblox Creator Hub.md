# SurfaceGui | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/SurfaceGui
Scraped: 2026-01-11T02:35:34.927716Z

## Inherits
- SurfaceGuiBase
- SurfaceGui
- LayerCollector
- GuiBase2d
- Instance
- Object
- Decals
- Textures
- TextLabels
- ImageLabels
- Face
- ImageButtons
- TextButtons
- PlayerGui
- StarterGui
- Adornee
- CanQuery
- ScreenGui
- LightInfluence
- Brightness
- AlwaysOnTop
- SurfaceGuis
- ScreenGuis
- GuiObjects
- MaxDistance
- UIScale
- GuiObject.Size
- TextLabel.TextSize
- PixelsPerStud
- CanvasSize
- Tool
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [SurfaceGuiBase](/docs/reference/engine/classes/SurfaceGuiBase)
6. /
7. [SurfaceGui](/docs/reference/engine/classes/SurfaceGui)

English

Feedback

Engine Class

![SurfaceGui](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/SurfaceGui-Dark.webp)SurfaceGui

Container for GuiObjects that are rendered on the surface of a part.

---

Summary

Properties

|  |
| --- |
| [AlwaysOnTop](#AlwaysOnTop):[boolean](/docs/luau/booleans) |
| [Brightness](#Brightness):[number](/docs/luau/numbers) |
| [CanvasSize](#CanvasSize):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [ClipsDescendants](#ClipsDescendants):[boolean](/docs/luau/booleans) |
| [LightInfluence](#LightInfluence):[number](/docs/luau/numbers) |
| [MaxDistance](#MaxDistance):[number](/docs/luau/numbers) |
| [PixelsPerStud](#PixelsPerStud):[number](/docs/luau/numbers) |
| [SizingMode](#SizingMode):[Enum.SurfaceGuiSizingMode](/docs/reference/engine/enums/SurfaceGuiSizingMode) |
| [ToolPunchThroughDistance](#ToolPunchThroughDistance):[number](/docs/luau/numbers) |
| [ZOffset](#ZOffset):[number](/docs/luau/numbers) |

Inherited Members

3 inherited from [SurfaceGuiBase](/docs/reference/engine/classes/SurfaceGuiBase)

4 inherited from [LayerCollector](/docs/reference/engine/classes/LayerCollector)

12 inherited from [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[SurfaceGui](/docs/reference/engine/classes/SurfaceGui) allows for the rendering of UI objects onto a part's
surface in the 3D world while also allowing for basic user interaction to
occur. Similar to [Decals](/docs/reference/engine/classes/Decal) and [Textures](/docs/reference/engine/classes/Texture), UI
objects such as [TextLabels](/docs/reference/engine/classes/TextLabel) and
[ImageLabels](/docs/reference/engine/classes/ImageLabel) parented to a [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) face the same
direction as the surface they're on, editable through the
[Face](/docs/reference/engine/classes/SurfaceGui#Face) property.

![SurfaceGui on a 3D part in the place with an ImageLabel child to depict a screen console.](https://prod.docsiteassets.roblox.com/assets/ui/in-experience/SurfaceGui-Diagram.jpg)

Note that interactive UI elements like [ImageButtons](/docs/reference/engine/classes/ImageButton) and
[TextButtons](/docs/reference/engine/classes/TextButton) inside a [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) will only receive
user input if they are parented to the [PlayerGui](/docs/reference/engine/classes/PlayerGui), typically via
placing the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) inside [StarterGui](/docs/reference/engine/classes/StarterGui) (the
[Adornee](/docs/reference/engine/classes/SurfaceGui#Adornee) property can be used to target a part in
the 3D world while the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) itself remains in the
[PlayerGui](/docs/reference/engine/classes/PlayerGui)). Additionally, the part's
[CanQuery](/docs/reference/engine/classes/BasePart#CanQuery) property must be true for the interactive
UI element to receive input.

See [In-Experience UI](/docs/ui/in-experience-containers#surface-ui) for
a guide on working with [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) containers.

##### Caching Behavior

To help improve performance, the appearance of a [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) is cached
until one of the following occurs, after which its appearance will be
recomputed on the next rendering frame.

* A descendant is added to or removed from the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui).
* A property of a descendant of the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) changes.
* A property of the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) itself changes.

---

API Reference

Properties

AlwaysOnTop

Read Parallel

Determines whether the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) will always be rendered on top
of other 3D objects.

SurfaceGui.AlwaysOnTop:[boolean](/docs/luau/booleans)

This property determines whether the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) will always render
on top of other 3D objects.

When set to false (default), the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) renders like other
3D content and is occluded by other 3D objects. When set to true, the
[SurfaceGui](/docs/reference/engine/classes/SurfaceGui) always renders on top of 3D content and the appearance
changes significantly:

* Colors match how they appear inside a [ScreenGui](/docs/reference/engine/classes/ScreenGui).
* Text may appear sharper on high DPI devices.
* [LightInfluence](/docs/reference/engine/classes/SurfaceGui#LightInfluence) is treated as though
  it's 0.
* [Brightness](/docs/reference/engine/classes/SurfaceGui#Brightness) has no effect.

Provide feedback

---

Brightness

Read Parallel

Determines the factor by which the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) container's light is
scaled when [LightInfluence](/docs/reference/engine/classes/SurfaceGui#LightInfluence) is 0.

SurfaceGui.Brightness:[number](/docs/luau/numbers)

This property determines the factor by which the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui)
container's light is scaled when
[LightInfluence](/docs/reference/engine/classes/SurfaceGui#LightInfluence) is 0. By default, this
property is 1 and can be set to any number between 0 and 1000. By
modifying this property, the apparent brightness of a [SurfaceGui](/docs/reference/engine/classes/SurfaceGui)
can be better matched to its environment. For instance, a video billboard
can be brightened inside a dark room by increasing
[Brightness](/docs/reference/engine/classes/SurfaceGui#Brightness) to 10.

Note that [Brightness](/docs/reference/engine/classes/SurfaceGui#Brightness) is inaccessible in
Studio and has no effect when either
[LightInfluence](/docs/reference/engine/classes/SurfaceGui#LightInfluence) is 1 or
[AlwaysOnTop](/docs/reference/engine/classes/SurfaceGui#AlwaysOnTop) is true.

Provide feedback

---

CanvasSize

Read Parallel

The size of a "virtual screen" in "virtual pixels" which makes
[SurfaceGuis](/docs/reference/engine/classes/SurfaceGui) pixel-to-pixel compatible with
[ScreenGuis](/docs/reference/engine/classes/ScreenGui).

SurfaceGui.CanvasSize:[Vector2](/docs/reference/engine/datatypes/Vector2)

The size of a "virtual screen" in "virtual pixels" which makes
[SurfaceGuis](/docs/reference/engine/classes/SurfaceGui) pixel-to-pixel compatible with
[ScreenGuis](/docs/reference/engine/classes/ScreenGui).

Provide feedback

---

ClipsDescendants

Read Parallel

Whether portions of [GuiObjects](/docs/reference/engine/classes/GuiObject) that fall outside of the
[SurfaceGui](/docs/reference/engine/classes/SurfaceGui) canvas borders will be drawn.

SurfaceGui.ClipsDescendants:[boolean](/docs/luau/booleans)

When set to true (default), portions of [GuiObjects](/docs/reference/engine/classes/GuiObject)
that fall outside of the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) canvas borders will not be
drawn.

Even when this property is false, [GuiObjects](/docs/reference/engine/classes/GuiObject) that are
completely outside of the canvas will not render.

Provide feedback

---

LightInfluence

Read Parallel

Controls how much the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) is influenced by environmental
lighting.

SurfaceGui.LightInfluence:[number](/docs/luau/numbers)

Controls how much the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) is influenced by environmental
lighting, in a range from 0 to 1. Setting this to 1 means that
surrounding lighting has complete control over the appearance, while
setting it to 0 means that the lighting has no effect.

Provide feedback

---

MaxDistance

Read Parallel

Controls how far away the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) can be displayed before it
stops rendering.

SurfaceGui.MaxDistance:[number](/docs/luau/numbers)

This property controls how far from the camera the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) will
be displayed before it stops rendering. A value of 0 means there is no
limit and it will render infinitely far away. The default value of 1000
works fine for most cases.

For [SurfaceGuis](/docs/reference/engine/classes/SurfaceGui) that appear outdoors, it's recommended
that [MaxDistance](/docs/reference/engine/classes/SurfaceGui#MaxDistance) is high enough to ensure
that the container's UI is sufficiently small on the screen when it
appears or disappears, minimizing the sudden pop‑in/out effect.

Provide feedback

---

PixelsPerStud

Read Parallel

Determines the density of pixels used for each world-space stud to render
the contents of the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui).

SurfaceGui.PixelsPerStud:[number](/docs/luau/numbers)

This property determines the density of pixels used for each world-space
stud to render the contents of the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui). Higher values will
cause the various [GuiObjects](/docs/reference/engine/classes/GuiObject) within to appear smaller if
they are kept the same size. Conversely, lower values will cause objects
to appear larger. However, if the [GuiObjects](/docs/reference/engine/classes/GuiObject) are scaled
proportionally through use of [UIScale](/docs/reference/engine/classes/UIScale), [GuiObject.Size](/docs/reference/engine/classes/GuiObject#Size),
[TextLabel.TextSize](/docs/reference/engine/classes/TextLabel#TextSize), or similar, this property allows for higher
definition to be used.

It's important to select a value based on how far away you expect a player
to view the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui). Also be mindful that a large pixel density
could negatively affect performance if the face of the adorned part is
large enough.

Provide feedback

---

SizingMode

Read Parallel

Determines whether the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) will render at a fixed size or
scale with its size in studs.

SurfaceGui.SizingMode:[Enum.SurfaceGuiSizingMode](/docs/reference/engine/enums/SurfaceGuiSizingMode)

When set to [Enum.SurfaceGuiSizingMode.PixelsPerStud](/docs/reference/engine/enums/SurfaceGuiSizingMode#PixelsPerStud) (default), the
[SurfaceGui](/docs/reference/engine/classes/SurfaceGui) renders with a variable size based on
[PixelsPerStud](/docs/reference/engine/classes/SurfaceGui#PixelsPerStud) and the surface's size in
studs.

When set to [Enum.SurfaceGuiSizingMode.FixedSize](/docs/reference/engine/enums/SurfaceGuiSizingMode#FixedSize), the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui)
renders with a fixed size set through
[CanvasSize](/docs/reference/engine/classes/SurfaceGui#CanvasSize).

Provide feedback

---

ToolPunchThroughDistance

Read Parallel

Sets the distance in which left clicking starts acting on the
[SurfaceGui](/docs/reference/engine/classes/SurfaceGui) instead of for the held [Tool](/docs/reference/engine/classes/Tool).

SurfaceGui.ToolPunchThroughDistance:[number](/docs/luau/numbers)

Sets the distance in which left clicking starts acting on the
[SurfaceGui](/docs/reference/engine/classes/SurfaceGui) instead of for the held [Tool](/docs/reference/engine/classes/Tool). If a character is
within this distance of the [SurfaceGui](/docs/reference/engine/classes/SurfaceGui), the [Tool](/docs/reference/engine/classes/Tool) will not
activate on click.

Provide feedback

---

ZOffset

Read Parallel

Layers this [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) in relation to other
[SurfaceGuis](/docs/reference/engine/classes/SurfaceGui) on the same face.

SurfaceGui.ZOffset:[number](/docs/luau/numbers)

Layers this [SurfaceGui](/docs/reference/engine/classes/SurfaceGui) in relation to others on the same face
(changing this does not visually "lift" or "sink" a [SurfaceGui](/docs/reference/engine/classes/SurfaceGui)
from the surface).

Provide feedback

---