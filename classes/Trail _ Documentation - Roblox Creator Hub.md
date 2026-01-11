# Trail | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Trail
Scraped: 2026-01-11T02:28:50.529424Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- Trail
- Attachment
- Trails
- BasePart
- Attachments
- Attachment0
- Attachment1
- TweenService
- Enabled
- Color
- Texture
- LightInfluence
- Lifetime
- Clear()
- CurrentCamera
- Transparency
- LightEmission
- MinLength
- MaxLength
- TextureMode
- TextureLength
- WidthScale
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Trail](/docs/reference/engine/classes/Trail)

English

Feedback

Engine Class

![Trail](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Trail-Dark.webp)Trail

Used to create a trail effect between two attachments.

---

Summary

Properties

|  |
| --- |
| [Attachment0](#Attachment0):[Attachment](/docs/reference/engine/classes/Attachment) |
| [Attachment1](#Attachment1):[Attachment](/docs/reference/engine/classes/Attachment) |
| [Brightness](#Brightness):[number](/docs/luau/numbers) |
| [Color](#Color):[ColorSequence](/docs/reference/engine/datatypes/ColorSequence) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [FaceCamera](#FaceCamera):[boolean](/docs/luau/booleans) |
| [Lifetime](#Lifetime):[number](/docs/luau/numbers) |
| [LightEmission](#LightEmission):[number](/docs/luau/numbers) |
| [LightInfluence](#LightInfluence):[number](/docs/luau/numbers) |
| [LocalTransparencyModifier](#LocalTransparencyModifier):[number](/docs/luau/numbers) |
| [MaxLength](#MaxLength):[number](/docs/luau/numbers) |
| [MinLength](#MinLength):[number](/docs/luau/numbers) |
| [Texture](#Texture):ContentId |
| [TextureLength](#TextureLength):[number](/docs/luau/numbers) |
| [TextureMode](#TextureMode):[Enum.TextureMode](/docs/reference/engine/enums/TextureMode) |
| [Transparency](#Transparency):[NumberSequence](/docs/reference/engine/datatypes/NumberSequence) |
| [WidthScale](#WidthScale):[NumberSequence](/docs/reference/engine/datatypes/NumberSequence) |

Methods

|  |
| --- |
| [Clear](#Clear)():() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The Trail object is used to create a trail effect between two attachments.
As the attachments move through space, a texture is drawn on their defined
plane. This is commonly used to create effects that visualize movements like
tracer trails behind projectiles, footprints, tire tracks, and similar
effects.

See [Trails](/docs/effects/trails) for more information.

Code Samples

Creating a Part with a Basic Trail

This example demos the functionality of [Trails](/docs/reference/engine/classes/Trail) by creating a
[BasePart](/docs/reference/engine/classes/BasePart) to be the parent of the trail. Two
[Attachments](/docs/reference/engine/classes/Attachment) are then parented to the part. The positions of
these two attachments (more importantly the distance between them) determines
where the trail is drawn as the part moves.

For these attachments to create a trail as described, a new [Trail](/docs/reference/engine/classes/Trail) is
parented to the part and its [Attachment0](/docs/reference/engine/classes/Trail#Attachment0) and
[Attachment1](/docs/reference/engine/classes/Trail#Attachment1) are parented to attachment0 and
attachment1 respectively. Finally, [TweenService](/docs/reference/engine/classes/TweenService) is used to move the
part back and forth, showing how the trail is drawn as the part (and its
attachments) move.

```
local TweenService = game:GetService("TweenService")



-- Create a parent part



local part = Instance.new("Part")



part.Material = Enum.Material.SmoothPlastic



part.Size = Vector3.new(4, 1, 2)



part.Position = Vector3.new(0, 5, 0)



part.Anchored = true



part.Parent = workspace



-- Create attachments on part



local attachment0 = Instance.new("Attachment")



attachment0.Name = "Attachment0"



attachment0.Position = Vector3.new(-2, 0, 0)



attachment0.Parent = part



local attachment1 = Instance.new("Attachment")



attachment1.Name = "Attachment1"



attachment1.Position = Vector3.new(2, 0, 0)



attachment1.Parent = part



-- Create a new trail



local trail = Instance.new("Trail")



trail.Attachment0 = attachment0



trail.Attachment1 = attachment1



trail.Parent = part



-- Tween part to display trail



local dir = 15



while true do



dir *= -1



local goal = { Position = part.Position + Vector3.new(0, 0, dir) }



local tweenInfo = TweenInfo.new(3)



local tween = TweenService:Create(part, tweenInfo, goal)



tween:Play()



task.wait(4)



end
```

---

API Reference

Properties

Attachment0

Read Parallel

Along with [Attachment1](/docs/reference/engine/classes/Trail#Attachment1), determines where the
trail will start drawing its segments.

Trail.Attachment0:[Attachment](/docs/reference/engine/classes/Attachment)

A [Trail](/docs/reference/engine/classes/Trail) starts drawing its segments at the positions of its
Attachment0 and [Attachment1](/docs/reference/engine/classes/Trail#Attachment1). When the trail
is [Enabled](/docs/reference/engine/classes/Trail#Enabled), it records the positions of its
attachments every frame and connects these positions to the attachments'
positions on the previous frame, creating a polygon that is then filled in
by the trail's [Color](/docs/reference/engine/classes/Trail#Color) and
[Texture](/docs/reference/engine/classes/Trail#Texture).

Changing the attachments of a trail while a trail is drawing will remove
all of the segments the trail has already drawn.

Provide feedback

---

Attachment1

Read Parallel

Along with [Attachment0](/docs/reference/engine/classes/Trail#Attachment0), determines where the
trail will start drawing its segments.

Trail.Attachment1:[Attachment](/docs/reference/engine/classes/Attachment)

A [Trail](/docs/reference/engine/classes/Trail) starts drawing its segments at the positions of its
[Attachment0](/docs/reference/engine/classes/Trail#Attachment0) and Attachment1. When the trail
is [Enabled](/docs/reference/engine/classes/Trail#Enabled), it records the positions of its
attachments every frame and connects these positions to the attachments'
positions on the previous frame, creating a polygon that is then filled in
by the trail's [Color](/docs/reference/engine/classes/Trail#Color) and
[Texture](/docs/reference/engine/classes/Trail#Texture).

Changing the attachments of a trail while a trail is drawing will remove
all of the segments the trail has already drawn.

Provide feedback

---

Brightness

Read Parallel

Scales the light emitted from the trail when
[LightInfluence](/docs/reference/engine/classes/Trail#LightInfluence) is less than 1.

Trail.Brightness:[number](/docs/luau/numbers)

Scales the light emitted from the trail when
[LightInfluence](/docs/reference/engine/classes/Trail#LightInfluence) is less than 1. This property
is 1 by default and can set to any number within the range of 0 to 10000.
Increasing the value of [LightInfluence](/docs/reference/engine/classes/Trail#LightInfluence)
decreases the effect of this property's value.

Provide feedback

---

Color

Read Parallel

The color of the trail throughout its lifetime.

Trail.Color:[ColorSequence](/docs/reference/engine/datatypes/ColorSequence)

Determines the color of the trail throughout its lifetime. If
[Texture](/docs/reference/engine/classes/Trail#Texture) is set, this color will tint the texture.

This property is a [ColorSequence](/docs/reference/engine/datatypes/ColorSequence), allowing the color to be
configured to vary across the length of the trail. If the color changes
after some of the trail segments have been drawn, all of the old segments
will be updated to match the new colors.

Code Samples

Creating a Trail with a Color Gradient

This example creates a [Trail](/docs/reference/engine/classes/Trail) with a gradient color, meaning that the
color at one end of the trail is different than the color at the opposite end,
and both colors blend together as they get closer to the middle of the trail.

```
local TweenService = game:GetService("TweenService")



-- Create a parent part



local part = Instance.new("Part")



part.Material = Enum.Material.SmoothPlastic



part.Size = Vector3.new(4, 1, 2)



part.Position = Vector3.new(0, 5, 0)



part.Anchored = true



part.Parent = workspace



-- Create attachments on part



local attachment0 = Instance.new("Attachment")



attachment0.Name = "Attachment0"



attachment0.Position = Vector3.new(-2, 0, 0)



attachment0.Parent = part



local attachment1 = Instance.new("Attachment")



attachment1.Name = "Attachment1"



attachment1.Position = Vector3.new(2, 0, 0)



attachment1.Parent = part



-- Create a new trail with color gradient



local trail = Instance.new("Trail")



trail.Attachment0 = attachment0



trail.Attachment1 = attachment1



local color1 = Color3.fromRGB(255, 0, 0)



local color2 = Color3.fromRGB(0, 0, 255)



trail.Color = ColorSequence.new(color1, color2)



trail.Parent = part



-- Tween part to display trail



local dir = 15



while true do



dir *= -1



local goal = { Position = part.Position + Vector3.new(0, 0, dir) }



local tweenInfo = TweenInfo.new(3)



local tween = TweenService:Create(part, tweenInfo, goal)



tween:Play()



task.wait(4)



end
```

Provide feedback

---

Enabled

Read Parallel

Determines whether the trail will be drawn or not.

Trail.Enabled:[boolean](/docs/luau/booleans)

This property determines whether the trail will be drawn or not.

If set to false while a trail is drawing, no new segments will be drawn,
but any existing segments will be cleaned up naturally when they reach the
end of their [Lifetime](/docs/reference/engine/classes/Trail#Lifetime). To forcibly clean up
existing segments, call the [Clear()](/docs/reference/engine/classes/Trail#Clear) method at the
same time.

Provide feedback

---

FaceCamera

Read Parallel

Determines whether the trail will always face the camera, regardless of
its orientation.

Trail.FaceCamera:[boolean](/docs/luau/booleans)

A [Trail](/docs/reference/engine/classes/Trail) is a 2D projection existing in 3D space, meaning that it
may not be visible from every angle. The FaceCamera property, when set
to true, ensures that the trail always faces the
[CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera), regardless of its
orientation.

Changing this property immediately affects all existing and future trail
segments.

Provide feedback

---

Lifetime

Read Parallel

Determines how long each segment in a trail will last, in seconds.

Trail.Lifetime:[number](/docs/luau/numbers)

The Lifetime property determines how long each segment in a trail will
last, in seconds, before it disappears. Defaults to 2 seconds but can be
set anywhere between 0.01 and 20.

The lifetime of a trail is also used by that effect's
[Color](/docs/reference/engine/classes/Trail#Color) and [Transparency](/docs/reference/engine/classes/Trail#Transparency)
properties to determine how each segment is drawn. Both of these
properties are sequences, meaning that they define their values at certain
keypoints in the segment's lifetime and then interpolate between the
values as the segment ages.

If a trail's lifetime changes, existing segments will immediately behave
as if they always had the new lifetime, meaning that if they've existed
for longer than the new lifetime, they will be removed immediately.

Provide feedback

---

LightEmission

Read Parallel

Determines to what degree the colors of the trail are blended with the
colors behind it.

Trail.LightEmission:[number](/docs/luau/numbers)

Determines to what degree the colors of the trail are blended with the
colors behind it. It should be set in the range of 0 to 1. A value of 0
uses normal blending modes and a value of 1 uses additive blending.

This property should not be confused with
[LightInfluence](/docs/reference/engine/classes/Trail#LightInfluence) which determines how the trail
is affected by environmental light.

Changing this property immediately affects all existing and future
segments of the trail.

This property does not cause the trail to light the environment.

Provide feedback

---

LightInfluence

Read Parallel

Determines the degree to which the trail is influenced by the
environment's lighting.

Trail.LightInfluence:[number](/docs/luau/numbers)

Determines the degree to which the trail is influenced by the
environment's lighting, clamped between 0 and 1. When 0, the trail will be
unaffected by the environment's lighting. When 1, it will be fully
affected by lighting as a [BasePart](/docs/reference/engine/classes/BasePart) would be.

Changing this property immediately affects all existing and future
segments of the trail.

See also [LightEmission](/docs/reference/engine/classes/Trail#LightEmission) which specifies to what
degree the colors of the trail are blended with the colors behind it.

Provide feedback

---

LocalTransparencyModifier

Hidden

Not Replicated

Read Parallel

Trail.LocalTransparencyModifier:[number](/docs/luau/numbers)

Provide feedback

---

MaxLength

Read Parallel

Sets the maximum length of the trail.

Trail.MaxLength:[number](/docs/luau/numbers)

This property determines the maximum length of the trail, in studs. Its
value defaults to 0, meaning that the trail will not have a maximum length
and trail segments will expire in their [Lifetime](/docs/reference/engine/classes/Trail#Lifetime).

This property can be used alongside the [MinLength](/docs/reference/engine/classes/Trail#MinLength)
property which determines the minimum length a trail must be before it's
drawn.

Provide feedback

---

MinLength

Read Parallel

Sets the minimum length of the trail.

Trail.MinLength:[number](/docs/luau/numbers)

This property determines the minimum length of the trail, in studs. If
neither of the trail's attachments have moved at least this value, no new
segments will be created and the endpoints of the current segment will be
moved to the current position of the attachments.

Note that changing this property will only affect new segments that
are drawn; any old segments that have already been drawn will maintain
their current length.

This property can be used alongside the [MaxLength](/docs/reference/engine/classes/Trail#MaxLength)
property which determines the maximum trail length before its oldest
segments are erased.

Provide feedback

---

Texture

Read Parallel

The content ID of the texture to be displayed on the trail.

Trail.Texture:ContentId

The content ID of the texture to be displayed on the trail. If this
property is not set, the trail will be displayed as a solid plane; this
also occurs when the texture is set to an invalid content ID or the image
associated with the texture has not yet loaded.

The appearance of the texture can be further modified by other trail
properties including [Color](/docs/reference/engine/classes/Trail#Color) and
[Transparency](/docs/reference/engine/classes/Trail#Transparency).

Scaling of the texture is determined by the distance between
[Attachment0](/docs/reference/engine/classes/Trail#Attachment0) and
[Attachment1](/docs/reference/engine/classes/Trail#Attachment1), as well as the
[TextureMode](/docs/reference/engine/classes/Trail#TextureMode),
[TextureLength](/docs/reference/engine/classes/Trail#TextureLength), and
[WidthScale](/docs/reference/engine/classes/Trail#WidthScale) properties.

Code Samples

Creating a Trail with a Paw Print Texture

This example adds a [paw
prints](https://create.roblox.com/store/asset/16178262259/PawPrintTexture)
texture to a trail object. In order for the paw prints to remain "stamped" in
place after rendering, [TextureMode](/docs/reference/engine/classes/Trail#TextureMode) is set to
[Enum.TextureMode.Static](/docs/reference/engine/enums/TextureMode#Static).

```
local TweenService = game:GetService("TweenService")



-- Create a parent part



local part = Instance.new("Part")



part.Material = Enum.Material.SmoothPlastic



part.Size = Vector3.new(2, 1, 2)



part.Position = Vector3.new(0, 5, 0)



part.Anchored = true



part.Parent = workspace



-- Create attachments on part



local attachment0 = Instance.new("Attachment")



attachment0.Name = "Attachment0"



attachment0.Position = Vector3.new(-1, 0, 0)



attachment0.Parent = part



local attachment1 = Instance.new("Attachment")



attachment1.Name = "Attachment1"



attachment1.Position = Vector3.new(1, 0, 0)



attachment1.Parent = part



-- Create a new trail with color gradient



local trail = Instance.new("Trail")



trail.Attachment0 = attachment0



trail.Attachment1 = attachment1



trail.Texture = "rbxassetid://16178262222"



trail.TextureMode = Enum.TextureMode.Static



trail.TextureLength = 2



trail.Parent = part



-- Tween part to display trail



local dir = 15



while true do



dir *= -1



local goal = { Position = part.Position + Vector3.new(0, 0, dir) }



local tweenInfo = TweenInfo.new(3)



local tween = TweenService:Create(part, tweenInfo, goal)



tween:Play()



task.wait(4)



end
```

Provide feedback

---

TextureLength

Read Parallel

Sets the length of the trail's texture, dependent on
[TextureMode](/docs/reference/engine/classes/Trail#TextureMode).

Trail.TextureLength:[number](/docs/luau/numbers)

Sets the length of the trail's texture, dependent on
[TextureMode](/docs/reference/engine/classes/Trail#TextureMode). Changing this property immediately
affects all existing and future trail segments.

Provide feedback

---

TextureMode

Read Parallel

Determines the manner in which the [Texture](/docs/reference/engine/classes/Trail#Texture) scales,
repeats, and moves along with the trail's attachments.

Trail.TextureMode:[Enum.TextureMode](/docs/reference/engine/enums/TextureMode)

This property, alongside [TextureLength](/docs/reference/engine/classes/Trail#TextureLength),
determines how a trail's [Texture](/docs/reference/engine/classes/Trail#Texture) scales, repeats,
and moves along with the trail's attachments. Changing this property
immediately affects all existing and future trail segments.

#### Scale and Repetition

When TextureMode is set to [Enum.TextureMode.Wrap](/docs/reference/engine/enums/TextureMode#Wrap) or
[Enum.TextureMode.Static](/docs/reference/engine/enums/TextureMode#Static), the [TextureLength](/docs/reference/engine/classes/Trail#TextureLength)
property sets the length of the texture as it repeats across the trail's
length.

![TextureMode diagram with Wrap mode](https://prod.docsiteassets.roblox.com/assets/engine-api/enums/TextureMode/Wrap-Static.png)

When TextureMode is set to [Enum.TextureMode.Stretch](/docs/reference/engine/enums/TextureMode#Stretch), the texture
will repeat [TextureLength](/docs/reference/engine/classes/Trail#TextureLength) times across the
trail's overall length.

![TextureMode diagram with Stretch mode](https://prod.docsiteassets.roblox.com/assets/engine-api/enums/TextureMode/Stretch.png)

#### Movement

The TextureMode property also affects the movement of the trail's
texture as follows:

* If set to [Enum.TextureMode.Stretch](/docs/reference/engine/enums/TextureMode#Stretch), the texture will stretch out based
  on the lifetime of the trail, and shrink inwards if the trail's
  attachments stop moving.
* If set to [Enum.TextureMode.Wrap](/docs/reference/engine/enums/TextureMode#Wrap), the texture will be tiled as the
  length of the trail changes, but the textures will remain stationary
  relative to their attachments.
* If set to [Enum.TextureMode.Static](/docs/reference/engine/enums/TextureMode#Static), the texture will be rolled out as
  the attachments move, and they will remain in place until their lifetime
  is met. This setting is ideal for trail textures that should appear
  "stamped" where rendered, such as paw prints or tire tracks.

Provide feedback

---

Transparency

Read Parallel

Sets the transparency of the trail's segments over its
[Lifetime](/docs/reference/engine/classes/Trail#Lifetime).

Trail.Transparency:[NumberSequence](/docs/reference/engine/datatypes/NumberSequence)

Sets the transparency of the trail's segments over its
[Lifetime](/docs/reference/engine/classes/Trail#Lifetime). This value is a
[NumberSequence](/docs/reference/engine/datatypes/NumberSequence), meaning it can be a static value or can change
throughout the lifetime of the trail segments.

Provide feedback

---

WidthScale

Read Parallel

Scales the width of the trail over the course of its lifetime.

Trail.WidthScale:[NumberSequence](/docs/reference/engine/datatypes/NumberSequence)

This property is a [NumberSequence](/docs/reference/engine/datatypes/NumberSequence) that scales the width of the
trail over the course of its lifetime. Values can range between 0 and 1,
acting as a multiplier on the distance between the trail's attachments.
For example, if the trail's attachments are 2 stud's apart and the value
of this property is 0.5, the trail's width will be 1 stud and the trail
will be centered between the two attachments.

Provide feedback

---

Methods

Clear

Clears the segments of the trail.

Trail:Clear():()

Returns

()

This method immediately clears all segments of the trail and is useful for
cleaning up trails with longer lifetimes or for cases where the trail
should be removed because of a specific action.

Calling this method only affects existing segments. To clear existing
trail segments and temporarily prevent new segments from being drawn,
toggle the trail's [Enabled](/docs/reference/engine/classes/Trail#Enabled) property to false at
the same time.

Provide feedback

---