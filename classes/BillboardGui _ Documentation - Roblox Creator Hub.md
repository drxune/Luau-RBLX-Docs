# BillboardGui | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BillboardGui
Scraped: 2026-01-11T02:30:47.167828Z

## Tags
- Not Replicated

## Inherits
- LayerCollector
- BillboardGui
- GuiObjects
- GuiBase2d
- Instance
- Object
- BasePart
- Attachment
- Adornee
- BaseParts
- Position
- Attachments
- WorldPosition
- Size
- GuiObject.Size
- TextLabel
- TextScaled
- ImageButtons
- TextButtons
- PlayerGui
- StarterGui
- GuiButton
- Active
- ScreenGui
- LightInfluence
- Brightness
- AlwaysOnTop
- DistanceStep
- CurrentDistance
- Camera
- StudsOffset
- ExtentsOffsetWorldSpace
- ExtentsOffset
- BillboardGuis
- MaxDistance
- Enabled
- LocalPlayer
- Workspace
- GuiObject.AnchorPoint
- StudsOffsetWorldSpace
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [LayerCollector](/docs/reference/engine/classes/LayerCollector)
6. /
7. [BillboardGui](/docs/reference/engine/classes/BillboardGui)

English

Feedback

Engine Class

![BillboardGui](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/BillboardGui-Dark.webp)BillboardGui

A container for [GuiObjects](/docs/reference/engine/classes/GuiObject) that renders in 3D space facing
the camera.

---

Summary

Properties

|  |
| --- |
| [Active](#Active):[boolean](/docs/luau/booleans) |
| [Adornee](#Adornee):[Instance](/docs/reference/engine/datatypes/Instance) |
| [AlwaysOnTop](#AlwaysOnTop):[boolean](/docs/luau/booleans) |
| [Brightness](#Brightness):[number](/docs/luau/numbers) |
| [ClipsDescendants](#ClipsDescendants):[boolean](/docs/luau/booleans) |
| [CurrentDistance](#CurrentDistance):[number](/docs/luau/numbers) |
| [DistanceLowerLimit](#DistanceLowerLimit):[number](/docs/luau/numbers)  Deprecated |
| [DistanceStep](#DistanceStep):[number](/docs/luau/numbers) |
| [DistanceUpperLimit](#DistanceUpperLimit):[number](/docs/luau/numbers)  Deprecated |
| [ExtentsOffset](#ExtentsOffset):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [ExtentsOffsetWorldSpace](#ExtentsOffsetWorldSpace):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [LightInfluence](#LightInfluence):[number](/docs/luau/numbers) |
| [MaxDistance](#MaxDistance):[number](/docs/luau/numbers) |
| [PlayerToHideFrom](#PlayerToHideFrom):[Instance](/docs/reference/engine/datatypes/Instance) |
| [Size](#Size):[UDim2](/docs/reference/engine/datatypes/UDim2) |
| [SizeOffset](#SizeOffset):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [StudsOffset](#StudsOffset):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [StudsOffsetWorldSpace](#StudsOffsetWorldSpace):[Vector3](/docs/reference/engine/datatypes/Vector3) |

Inherited Members

4 inherited from [LayerCollector](/docs/reference/engine/classes/LayerCollector)

12 inherited from [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[BillboardGui](/docs/reference/engine/classes/BillboardGui) is a container for UI objects to appear in the 3D space
but always face the camera. The container's position is relative to the parent
[BasePart](/docs/reference/engine/classes/BasePart) or [Attachment](/docs/reference/engine/classes/Attachment) (or the
[Adornee](/docs/reference/engine/classes/BillboardGui#Adornee)). For [BaseParts](/docs/reference/engine/classes/BasePart), the
[Position](/docs/reference/engine/classes/BasePart#Position) property is used, while for
[Attachments](/docs/reference/engine/classes/Attachment), the
[WorldPosition](/docs/reference/engine/classes/Attachment#WorldPosition) property is used.

![BillboardGui with a TextLabel describing the screen console it floats above.](https://prod.docsiteassets.roblox.com/assets/ui/in-experience/BillboardGui-Diagram.jpg)

A billboard's [Size](/docs/reference/engine/classes/BillboardGui#Size) property works slightly
differently than [GuiObject.Size](/docs/reference/engine/classes/GuiObject#Size). While the offset components work
the same, the scale components are used as stud sizes in 3D space.

When creating a size-scaled [BillboardGui](/docs/reference/engine/classes/BillboardGui) that contains a
[TextLabel](/docs/reference/engine/classes/TextLabel), it's useful to enable the label's
[TextScaled](/docs/reference/engine/classes/TextLabel#TextScaled) property so that its text scales along
with the billboard canvas as the camera distance changes.

Note that interactive UI elements like [ImageButtons](/docs/reference/engine/classes/ImageButton) and
[TextButtons](/docs/reference/engine/classes/TextButton) inside a [BillboardGui](/docs/reference/engine/classes/BillboardGui) will only receive
user input if they are parented to the [PlayerGui](/docs/reference/engine/classes/PlayerGui), typically via
placing the [BillboardGui](/docs/reference/engine/classes/BillboardGui) inside [StarterGui](/docs/reference/engine/classes/StarterGui). The
[Adornee](/docs/reference/engine/classes/BillboardGui#Adornee) property can be used to target a part or
attachment in the 3D world while the [BillboardGui](/docs/reference/engine/classes/BillboardGui) itself remains in
the [PlayerGui](/docs/reference/engine/classes/PlayerGui).

See [In-Experience UI](/docs/ui/in-experience-containers#billboard-ui)
for a guide on working with [BillboardGui](/docs/reference/engine/classes/BillboardGui) containers.

##### Caching Behavior

To help improve performance, the appearance of a [BillboardGui](/docs/reference/engine/classes/BillboardGui) is
cached until one of the following occurs, after which its appearance will be
recomputed on the next rendering frame.

* A descendant is added to or removed from the [BillboardGui](/docs/reference/engine/classes/BillboardGui).
* A property of a descendant of the [BillboardGui](/docs/reference/engine/classes/BillboardGui) changes.
* A property of the [BillboardGui](/docs/reference/engine/classes/BillboardGui) itself changes.

---

API Reference

Properties

Active

Read Parallel

Controls whether the descendants will receive input events.

BillboardGui.Active:[boolean](/docs/luau/booleans)

Controls whether the descendants will receive input events. If the
[BillboardGui](/docs/reference/engine/classes/BillboardGui) contains a [GuiButton](/docs/reference/engine/classes/GuiButton), that button will become
clickable only if [Active](/docs/reference/engine/classes/BillboardGui#Active) is set to true on
both the [BillboardGui](/docs/reference/engine/classes/BillboardGui) and the button.

Note that interactive UI elements like [ImageButtons](/docs/reference/engine/classes/ImageButton)
and [TextButtons](/docs/reference/engine/classes/TextButton) inside a [BillboardGui](/docs/reference/engine/classes/BillboardGui) will only
receive user input if they are parented to the [PlayerGui](/docs/reference/engine/classes/PlayerGui),
typically via placing the [BillboardGui](/docs/reference/engine/classes/BillboardGui) inside [StarterGui](/docs/reference/engine/classes/StarterGui).
The [Adornee](/docs/reference/engine/classes/BillboardGui#Adornee) property can be used to target a
part or attachment in the 3D world while the [BillboardGui](/docs/reference/engine/classes/BillboardGui) itself
remains in the [PlayerGui](/docs/reference/engine/classes/PlayerGui).

Provide feedback

---

Adornee

Read Parallel

Sets the target part or attachment that the [BillboardGui](/docs/reference/engine/classes/BillboardGui) is
positioned relative to.

BillboardGui.Adornee:[Instance](/docs/reference/engine/datatypes/Instance)

Sets the target [BasePart](/docs/reference/engine/classes/BasePart) or [Attachment](/docs/reference/engine/classes/Attachment) that the
[BillboardGui](/docs/reference/engine/classes/BillboardGui) is positioned relative to, overriding the parent part
or attachment.

Provide feedback

---

AlwaysOnTop

Read Parallel

Determines whether the [BillboardGui](/docs/reference/engine/classes/BillboardGui) will always be rendered on top
of other 3D objects.

BillboardGui.AlwaysOnTop:[boolean](/docs/luau/booleans)

This property determines whether the [BillboardGui](/docs/reference/engine/classes/BillboardGui) will always
render on top of other 3D objects.

When set to false (default), the [BillboardGui](/docs/reference/engine/classes/BillboardGui) renders like other
3D content and is occluded by other 3D objects. When set to true, the
[BillboardGui](/docs/reference/engine/classes/BillboardGui) always renders on top of 3D content and the
appearance changes significantly:

* Colors match how they appear inside a [ScreenGui](/docs/reference/engine/classes/ScreenGui).
* Text may appear sharper on high DPI devices.
* [LightInfluence](/docs/reference/engine/classes/BillboardGui#LightInfluence) is treated as though
  it's 0.
* [Brightness](/docs/reference/engine/classes/BillboardGui#Brightness) has no effect.

Provide feedback

---

Brightness

Read Parallel

Determines the factor by which the [BillboardGui](/docs/reference/engine/classes/BillboardGui) container's light
is scaled when [LightInfluence](/docs/reference/engine/classes/BillboardGui#LightInfluence) is 0.

BillboardGui.Brightness:[number](/docs/luau/numbers)

This property determines the factor by which the [BillboardGui](/docs/reference/engine/classes/BillboardGui)
container's light is scaled when
[LightInfluence](/docs/reference/engine/classes/BillboardGui#LightInfluence) is 0. By default,
this property is 1 and can be set to any number between 0 and 1000.
By modifying this property, the apparent brightness of a
[BillboardGui](/docs/reference/engine/classes/BillboardGui) can be better matched to its environment. For
instance, a video billboard can be brightened inside a dark room by
increasing [Brightness](/docs/reference/engine/classes/BillboardGui#Brightness) to 10.

Note that [Brightness](/docs/reference/engine/classes/BillboardGui#Brightness) is inaccessible in
Studio and has no effect when either
[LightInfluence](/docs/reference/engine/classes/BillboardGui#LightInfluence) is 1 or
[AlwaysOnTop](/docs/reference/engine/classes/BillboardGui#AlwaysOnTop) is true.

Provide feedback

---

ClipsDescendants

Read Parallel

Whether portions of [GuiObjects](/docs/reference/engine/classes/GuiObject) that fall outside of the
[BillboardGui](/docs/reference/engine/classes/BillboardGui) canvas borders will be drawn.

BillboardGui.ClipsDescendants:[boolean](/docs/luau/booleans)

When set to true (default), portions of [GuiObjects](/docs/reference/engine/classes/GuiObject)
that fall outside of the [BillboardGui](/docs/reference/engine/classes/BillboardGui) canvas borders will not be
drawn.

Even when this property is false, [GuiObjects](/docs/reference/engine/classes/GuiObject) that are
completely outside of the canvas will not render.

Provide feedback

---

CurrentDistance

Read Only

Not Replicated

Read Parallel

The current distance in studs that the [BillboardGui](/docs/reference/engine/classes/BillboardGui) is from the
player's camera.

BillboardGui.CurrentDistance:[number](/docs/luau/numbers)

The current distance in studs that the [BillboardGui](/docs/reference/engine/classes/BillboardGui) is from the
player's camera. A changed event does not fire for this property unless
[DistanceStep](/docs/reference/engine/classes/BillboardGui#DistanceStep) is more than 0.

Provide feedback

---

DistanceLowerLimit

Deprecated

Show details

---

DistanceStep

Not Replicated

Read Parallel

Determines the size [CurrentDistance](/docs/reference/engine/classes/BillboardGui#CurrentDistance)
increments and decrements in studs as the player's camera moves closer and
further from the [BillboardGui](/docs/reference/engine/classes/BillboardGui).

BillboardGui.DistanceStep:[number](/docs/luau/numbers)

Determines the size [CurrentDistance](/docs/reference/engine/classes/BillboardGui#CurrentDistance)
increments and decrements in studs as the player's camera moves closer and
further from the [BillboardGui](/docs/reference/engine/classes/BillboardGui). The property defaults to 0.

Provide feedback

---

DistanceUpperLimit

Deprecated

Show details

---

ExtentsOffset

Read Parallel

Determines how the [BillboardGui](/docs/reference/engine/classes/BillboardGui) is offset from its
[Adornee](/docs/reference/engine/classes/BillboardGui#Adornee), relative to the [Camera](/docs/reference/engine/classes/Camera)
orientation, in units half the dimensions of the model's
[Camera](/docs/reference/engine/classes/Camera)-aligned bounding box.

BillboardGui.ExtentsOffset:[Vector3](/docs/reference/engine/datatypes/Vector3)

This property determines how the [BillboardGui](/docs/reference/engine/classes/BillboardGui) is offset from its
[Adornee](/docs/reference/engine/classes/BillboardGui#Adornee), relative to the [Camera](/docs/reference/engine/classes/Camera)
orientation, in units half the dimensions of the model's
[Camera](/docs/reference/engine/classes/Camera)-aligned bounding box.

See also [StudsOffset](/docs/reference/engine/classes/BillboardGui#StudsOffset) which works
similarly but uses stud units, or
[ExtentsOffsetWorldSpace](/docs/reference/engine/classes/BillboardGui#ExtentsOffsetWorldSpace) which
works similarly except the offset orientation is relative to the global
axes.

Provide feedback

---

ExtentsOffsetWorldSpace

Read Parallel

Determines how the [BillboardGui](/docs/reference/engine/classes/BillboardGui) is offset from its
[Adornee](/docs/reference/engine/classes/BillboardGui#Adornee), relative to the global axes, in
units half the dimensions of the model's axis-aligned bounding box.

BillboardGui.ExtentsOffsetWorldSpace:[Vector3](/docs/reference/engine/datatypes/Vector3)

This property determines how the [BillboardGui](/docs/reference/engine/classes/BillboardGui) is offset from its
[Adornee](/docs/reference/engine/classes/BillboardGui#Adornee), relative to the global axes, in
units half the dimensions of the model's axis-aligned bounding box.

See also [StudsOffset](/docs/reference/engine/classes/BillboardGui#StudsOffset) which works
similarly but uses stud units, or
[ExtentsOffset](/docs/reference/engine/classes/BillboardGui#ExtentsOffset) which works similarly
except the offset orientation is relative to the [Camera](/docs/reference/engine/classes/Camera).

Provide feedback

---

LightInfluence

Read Parallel

Controls how much the [BillboardGui](/docs/reference/engine/classes/BillboardGui) is influenced by environmental
lighting.

BillboardGui.LightInfluence:[number](/docs/luau/numbers)

Controls how much the [BillboardGui](/docs/reference/engine/classes/BillboardGui) is influenced by environmental
lighting, in a range from 0 to 1. Setting this to 1 means that
surrounding lighting has complete control over the appearance, while
setting it to 0 means that the lighting has no effect.

Provide feedback

---

MaxDistance

Read Parallel

Controls how far away the [BillboardGui](/docs/reference/engine/classes/BillboardGui) can be displayed before it
stops rendering.

BillboardGui.MaxDistance:[number](/docs/luau/numbers)

This property controls how far from the camera the [BillboardGui](/docs/reference/engine/classes/BillboardGui)
will be displayed before it stops rendering. A value of 0 or inf
(default) means there is no limit and it will render infinitely far away.

For [BillboardGuis](/docs/reference/engine/classes/BillboardGui) that appear outdoors, it's
recommended that [MaxDistance](/docs/reference/engine/classes/BillboardGui#MaxDistance) is high
enough to ensure that the container's UI is sufficiently small on the
screen when it appears or disappears, minimizing the sudden pop‑in/out
effect.

Provide feedback

---

PlayerToHideFrom

Read Parallel

Used by scripts to hide the [BillboardGui](/docs/reference/engine/classes/BillboardGui) from a specific player.

BillboardGui.PlayerToHideFrom:[Instance](/docs/reference/engine/datatypes/Instance)

Used by scripts to hide the [BillboardGui](/docs/reference/engine/classes/BillboardGui) from a specific player.

To hide a [BillboardGui](/docs/reference/engine/classes/BillboardGui) from more than one player, place it into
[StarterGui](/docs/reference/engine/classes/StarterGui) and use a script to set the
[Enabled](/docs/reference/engine/classes/BillboardGui#Enabled) property according to whether the
[LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) should be able to see it. The
[Adornee](/docs/reference/engine/classes/BillboardGui#Adornee) property can be used to attach the
[BillboardGui](/docs/reference/engine/classes/BillboardGui) to a [BasePart](/docs/reference/engine/classes/BasePart) or [Attachment](/docs/reference/engine/classes/Attachment) in the
[Workspace](/docs/reference/engine/classes/Workspace), instead of parenting it.

Provide feedback

---

Size

Read Parallel

Controls the size that the [BillboardGui](/docs/reference/engine/classes/BillboardGui) will have on screen.

BillboardGui.Size:[UDim2](/docs/reference/engine/datatypes/UDim2)

Controls the size that the [BillboardGui](/docs/reference/engine/classes/BillboardGui) will have on screen.
Unlike [GuiObject.Size](/docs/reference/engine/classes/GuiObject#Size), the
[scale](/docs/ui/position-and-size#size) components of this property
set the billboard's stud size in 3D space.

Provide feedback

---

SizeOffset

Read Parallel

A 2D offset in size-relative units that acts like an anchor point.

BillboardGui.SizeOffset:[Vector2](/docs/reference/engine/datatypes/Vector2)

A 2D offset in size-relative units that acts like an anchor point. This
can be used similarly to the [GuiObject.AnchorPoint](/docs/reference/engine/classes/GuiObject#AnchorPoint) property, but
the values are different.

| Size Offset | Explanation |
| --- | --- |
| 0, 0 | The default in which UI will be anchored at its center. |
| 0.5, 0.5 | UI will anchor at the bottom left. |
| 0.5, -0.5 | UI will anchor at the top left. |
| -0.5, 0.5 | UI will anchor at the top right. |
| -0.5, -0.5 | UI will anchor at the bottom right. |

See also [StudsOffset](/docs/reference/engine/classes/BillboardGui#StudsOffset),
[StudsOffsetWorldSpace](/docs/reference/engine/classes/BillboardGui#StudsOffsetWorldSpace),
[ExtentsOffset](/docs/reference/engine/classes/BillboardGui#ExtentsOffset), and
[ExtentsOffsetWorldSpace](/docs/reference/engine/classes/BillboardGui#ExtentsOffsetWorldSpace) which
are offset properties that work in 3D space instead.

Provide feedback

---

StudsOffset

Read Parallel

Determines how the [BillboardGui](/docs/reference/engine/classes/BillboardGui) is offset from its
[Adornee](/docs/reference/engine/classes/BillboardGui#Adornee) in studs, relative to the
[Camera](/docs/reference/engine/classes/Camera) orientation.

BillboardGui.StudsOffset:[Vector3](/docs/reference/engine/datatypes/Vector3)

This property determines how the [BillboardGui](/docs/reference/engine/classes/BillboardGui) is offset from its
[Adornee](/docs/reference/engine/classes/BillboardGui#Adornee) in studs, relative to the
[Camera](/docs/reference/engine/classes/Camera) orientation.

See also [StudsOffsetWorldSpace](/docs/reference/engine/classes/BillboardGui#StudsOffsetWorldSpace)
which works similarly except the offset orientation is relative to the
global axes.

Provide feedback

---

StudsOffsetWorldSpace

Read Parallel

Determines how the [BillboardGui](/docs/reference/engine/classes/BillboardGui) is offset from its
[Adornee](/docs/reference/engine/classes/BillboardGui#Adornee) in studs, relative to the global
axes.

BillboardGui.StudsOffsetWorldSpace:[Vector3](/docs/reference/engine/datatypes/Vector3)

This property determines how the [BillboardGui](/docs/reference/engine/classes/BillboardGui) is offset from its
[Adornee](/docs/reference/engine/classes/BillboardGui#Adornee) in studs, relative to the global
axes.

See also [StudsOffset](/docs/reference/engine/classes/BillboardGui#StudsOffset) which works
similarly except the offset orientation is relative to the [Camera](/docs/reference/engine/classes/Camera).

Provide feedback

---