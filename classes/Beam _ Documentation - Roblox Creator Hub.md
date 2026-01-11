# Beam | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Beam
Scraped: 2026-01-11T02:32:53.464753Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- Beam
- Attachments
- Attachment
- Workspace
- Attachment0
- Attachment1
- CurveSize0
- CurveSize1
- LightInfluence
- Segments
- Texture
- CurrentCamera
- BasePart
- LightEmission
- Color
- Transparency
- TextureMode
- TextureLength
- Width0
- Width1
- Beams
- Beam.ZOffset
- TextureSpeed
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Beam](/docs/reference/engine/classes/Beam)

English

Feedback

Engine Class

![Beam](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Beam-Dark.webp)Beam

Connects two [Attachments](/docs/reference/engine/classes/Attachment) by drawing a texture between them.

---

Summary

Properties

|  |
| --- |
| [Attachment0](#Attachment0):[Attachment](/docs/reference/engine/classes/Attachment) |
| [Attachment1](#Attachment1):[Attachment](/docs/reference/engine/classes/Attachment) |
| [Brightness](#Brightness):[number](/docs/luau/numbers) |
| [Color](#Color):[ColorSequence](/docs/reference/engine/datatypes/ColorSequence) |
| [CurveSize0](#CurveSize0):[number](/docs/luau/numbers) |
| [CurveSize1](#CurveSize1):[number](/docs/luau/numbers) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [FaceCamera](#FaceCamera):[boolean](/docs/luau/booleans) |
| [LightEmission](#LightEmission):[number](/docs/luau/numbers) |
| [LightInfluence](#LightInfluence):[number](/docs/luau/numbers) |
| [LocalTransparencyModifier](#LocalTransparencyModifier):[number](/docs/luau/numbers) |
| [Segments](#Segments):[number](/docs/luau/numbers) |
| [Texture](#Texture):ContentId |
| [TextureLength](#TextureLength):[number](/docs/luau/numbers) |
| [TextureMode](#TextureMode):[Enum.TextureMode](/docs/reference/engine/enums/TextureMode) |
| [TextureSpeed](#TextureSpeed):[number](/docs/luau/numbers) |
| [Transparency](#Transparency):[NumberSequence](/docs/reference/engine/datatypes/NumberSequence) |
| [Width0](#Width0):[number](/docs/luau/numbers) |
| [Width1](#Width1):[number](/docs/luau/numbers) |
| [ZOffset](#ZOffset):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [SetTextureOffset](#SetTextureOffset)(offset: [number](/docs/luau/numbers)):() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A Beam object connects two [Attachments](/docs/reference/engine/classes/Attachment) by drawing a
texture between them.

To display, a beam must be a descendant of the [Workspace](/docs/reference/engine/classes/Workspace) with its
[Attachment0](/docs/reference/engine/classes/Beam#Attachment0) and [Attachment1](/docs/reference/engine/classes/Beam#Attachment1)
properties set to [Attachments](/docs/reference/engine/classes/Attachment) also descending from the
[Workspace](/docs/reference/engine/classes/Workspace).

The beam's appearance can be customized using the range of properties outlined
below. Also see the [Beams](/docs/effects/beams) guide for visual
examples.

#### Beam Curvature

Beams are configured to use a cubic Bézier curve formed by four control
points. This means they are not constrained to straight lines and the curve of
the beam can be modified by changing [CurveSize0](/docs/reference/engine/classes/Beam#CurveSize0),
[CurveSize1](/docs/reference/engine/classes/Beam#CurveSize1), and the orientation of the beam's
[Attachments](/docs/reference/engine/classes/Attachment).

* P0 — The start of the beam; position of
  [Attachment0](/docs/reference/engine/classes/Beam#Attachment0).
* P1 — [CurveSize0](/docs/reference/engine/classes/Beam#CurveSize0) studs away from
  [Attachment0](/docs/reference/engine/classes/Beam#Attachment0), in the positive X direction of
  [Attachment0](/docs/reference/engine/classes/Beam#Attachment0).
* P2 — [CurveSize1](/docs/reference/engine/classes/Beam#CurveSize1) studs away from
  [Attachment1](/docs/reference/engine/classes/Beam#Attachment1), in the negative X direction of
  [Attachment1](/docs/reference/engine/classes/Beam#Attachment1).
* P3 — The end of the beam; position of
  [Attachment1](/docs/reference/engine/classes/Beam#Attachment1)

![Beam curvature diagram](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/Beam/Curvature-Diagram.png)

Code Samples

Creating a Beam From Scratch

This code sample demonstrates how a Beam effect can be created from scratch
by creating a Beam, setting all of its properties and configuring it's
Attachments.

```
-- create attachments



local att0 = Instance.new("Attachment")



local att1 = Instance.new("Attachment")



-- parent to terrain (can be part instead)



att0.Parent = workspace.Terrain



att1.Parent = workspace.Terrain



-- position attachments



att0.Position = Vector3.new(0, 10, 0)



att1.Position = Vector3.new(0, 10, 10)



-- create beam



local beam = Instance.new("Beam")



beam.Attachment0 = att0



beam.Attachment1 = att1



-- appearance properties



beam.Color = ColorSequence.new({ -- a color sequence shifting from white to blue



ColorSequenceKeypoint.new(0, Color3.fromRGB(255, 255, 255)),



ColorSequenceKeypoint.new(1, Color3.fromRGB(0, 255, 255)),



})



beam.LightEmission = 1 -- use additive blending



beam.LightInfluence = 0 -- beam not influenced by light



beam.Texture = "rbxasset://textures/particles/sparkles_main.dds" -- a built in sparkle texture



beam.TextureMode = Enum.TextureMode.Wrap -- wrap so length can be set by TextureLength



beam.TextureLength = 1 -- repeating texture is 1 stud long



beam.TextureSpeed = 1 -- slow texture speed



beam.Transparency = NumberSequence.new({ -- beam fades out at the end



NumberSequenceKeypoint.new(0, 0),



NumberSequenceKeypoint.new(0.8, 0),



NumberSequenceKeypoint.new(1, 1),



})



beam.ZOffset = 0 -- render at the position of the beam without offset



-- shape properties



beam.CurveSize0 = 2 -- create a curved beam



beam.CurveSize1 = -2 -- create a curved beam



beam.FaceCamera = true -- beam is visible from every angle



beam.Segments = 10 -- default curve resolution



beam.Width0 = 0.2 -- starts small



beam.Width1 = 2 -- ends big



-- parent beam



beam.Enabled = true



beam.Parent = att0
```

---

API Reference

Properties

Attachment0

Read Parallel

The [Attachment](/docs/reference/engine/classes/Attachment) the beam originates from.

Beam.Attachment0:[Attachment](/docs/reference/engine/classes/Attachment)

The [Attachment](/docs/reference/engine/classes/Attachment) the beam originates from. This attachment is the
first control point on the beam's cubic Bézier curve; its orientation,
alongside the [CurveSize0](/docs/reference/engine/classes/Beam#CurveSize0) property, determines the
position of the second control point. See
[Beams](/docs/effects/beams#curve) for more details.

For the [Attachment](/docs/reference/engine/classes/Attachment) where the beam ends, see
[Attachment1](/docs/reference/engine/classes/Beam#Attachment1).

Provide feedback

---

Attachment1

Read Parallel

The [Attachment](/docs/reference/engine/classes/Attachment) the beam ends at.

Beam.Attachment1:[Attachment](/docs/reference/engine/classes/Attachment)

The [Attachment](/docs/reference/engine/classes/Attachment) the beam ends at. This attachment is the fourth and
final control point on the beam's cubic Bézier curve; its orientation,
alongside the [CurveSize1](/docs/reference/engine/classes/Beam#CurveSize1) property, determines the
position of the third control point. See
[Beams](/docs/effects/beams#curve) for more details.

For the [Attachment](/docs/reference/engine/classes/Attachment) where the beam originates from, see
[Attachment0](/docs/reference/engine/classes/Beam#Attachment0).

Provide feedback

---

Brightness

Read Parallel

Scales the light emitted from the beam when
[LightInfluence](/docs/reference/engine/classes/Beam#LightInfluence) is less than 1.

Beam.Brightness:[number](/docs/luau/numbers)

Scales the light emitted from the beam when
[LightInfluence](/docs/reference/engine/classes/Beam#LightInfluence) is less than 1. This property
is 1 by default and can set to any number within the range of 0 to 10000.
Increasing the value of [LightInfluence](/docs/reference/engine/classes/Beam#LightInfluence)
decreases the effect of this property's value.

Provide feedback

---

Color

Read Parallel

Determines the color of the beam across its
[Segments](/docs/reference/engine/classes/Beam#Segments).

Beam.Color:[ColorSequence](/docs/reference/engine/datatypes/ColorSequence)

Determines the color of the beam across its
[Segments](/docs/reference/engine/classes/Beam#Segments). If [Texture](/docs/reference/engine/classes/Beam#Texture) is set,
this color will be applied to the beam's texture. If no
[Texture](/docs/reference/engine/classes/Beam#Texture) is set, the [Beam](/docs/reference/engine/classes/Beam) will appear as a
solid line colored in accordance with this property.

This property is a [ColorSequence](/docs/reference/engine/datatypes/ColorSequence), allowing the color to be
configured to vary across the length of the beam. Consider the following
[ColorSequence](/docs/reference/engine/datatypes/ColorSequence) which, when applied to a beam, would yield the
pictured result.

```
local colorSequence = ColorSequence.new({



ColorSequenceKeypoint.new(0, Color3.fromRGB(255, 0, 0)), -- Red



ColorSequenceKeypoint.new(0.5, Color3.fromRGB(0, 188, 203)), -- Cyan



ColorSequenceKeypoint.new(1, Color3.fromRGB(196, 0, 255)), -- Purple



}



)
```

![](https://prod.docsiteassets.roblox.com/assets/lighting-and-effects/beam/ColorSequence-Applied.png)

Note the beam's coloration also depends on the number of
[Segments](/docs/reference/engine/classes/Beam#Segments) the [Beam](/docs/reference/engine/classes/Beam) has. Each segment of the
beam can only show a transition between two colors. Therefore a
[Beam](/docs/reference/engine/classes/Beam) will need to have at least n-1 segments in order for the
color to display correctly, where n is the number of
[ColorSequenceKeypoints](/docs/reference/engine/datatypes/ColorSequenceKeypoint) in the
[ColorSequence](/docs/reference/engine/datatypes/ColorSequence).

Provide feedback

---

CurveSize0

Read Parallel

Determines, along with [Attachment0](/docs/reference/engine/classes/Beam#Attachment0), the position
of the second control point in the beam's Bézier curve.

Beam.CurveSize0:[number](/docs/luau/numbers)

Determines, along with [Attachment0](/docs/reference/engine/classes/Beam#Attachment0), the position
of the second control point in the beam's Bézier curve. See
[Beams](/docs/effects/beams#curve) for more details.

The position of this point can be determined by the following equation:

```
local controlPoint2 = Beam.Attachment0.WorldPosition + (Beam.Attachment0.CFrame.RightVector * Beam.CurveSize0)
```

Provide feedback

---

CurveSize1

Read Parallel

Determines, along with [Attachment1](/docs/reference/engine/classes/Beam#Attachment1), the position
of the third control point in the beam's Bézier curve.

Beam.CurveSize1:[number](/docs/luau/numbers)

Determines, along with [Attachment1](/docs/reference/engine/classes/Beam#Attachment1), the position
of the third control point in the beam's Bézier curve. See
[Beams](/docs/effects/beams#curve) for more details.

The position of this point can be determined by the following equation:

```
local controlPoint3 = Beam.Attachment1.WorldPosition - (Beam.Attachment1.CFrame.RightVector * Beam.CurveSize1)
```

Provide feedback

---

Enabled

Read Parallel

Determines whether the beam is visible or not.

Beam.Enabled:[boolean](/docs/luau/booleans)

Determines whether the beam is visible or not.

When this property is set to false, the beam's
[Segments](/docs/reference/engine/classes/Beam#Segments) will not be displayed.

Provide feedback

---

FaceCamera

Read Parallel

Determines whether the [Segments](/docs/reference/engine/classes/Beam#Segments) of the beam will
always face the camera, regardless of its orientation.

Beam.FaceCamera:[boolean](/docs/luau/booleans)

A [Beam](/docs/reference/engine/classes/Beam) is a 2D projection existing in 3D space, meaning that it
may not be visible from every angle. The FaceCamera property, when set
to true, ensures that the beam always faces the
[CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera), regardless of its
orientation.

Provide feedback

---

LightEmission

Read Parallel

Determines to what degree the colors of the beam are blended with the
colors behind it.

Beam.LightEmission:[number](/docs/luau/numbers)

Determines to what degree the colors of the beam are blended with the
colors behind it. It should be set in the range of 0 to 1. A value of 0
uses normal blending modes and a value of 1 uses additive blending.

This property should not be confused with
[LightInfluence](/docs/reference/engine/classes/Beam#LightInfluence) which determines how the beam
is affected by environmental light.

This property does not cause the beam to light the environment.

Provide feedback

---

LightInfluence

Read Parallel

Determines the degree to which the beam is influenced by the environment's
lighting.

Beam.LightInfluence:[number](/docs/luau/numbers)

Determines the degree to which the beam is influenced by the environment's
lighting, clamped between 0 and 1. When 0, the beam will be unaffected by
the environment's lighting. When 1, it will be fully affected by lighting
as a [BasePart](/docs/reference/engine/classes/BasePart) would be.

See also [LightEmission](/docs/reference/engine/classes/Beam#LightEmission) which specifies to what
degree the colors of the beam are blended with the colors behind it.

Provide feedback

---

LocalTransparencyModifier

Hidden

Not Replicated

Read Parallel

Beam.LocalTransparencyModifier:[number](/docs/luau/numbers)

Provide feedback

---

Segments

Read Parallel

Sets how many straight segments the beam is made up of.

Beam.Segments:[number](/docs/luau/numbers)

Rather than being a perfect curve, a beam is made up of straight segments.
The more segments, the higher the resolution of the curve. The
Segments property sets how many straight segments the beam is made up
of, with a default value of 10.

Note that the [Color](/docs/reference/engine/classes/Beam#Color) and
[Transparency](/docs/reference/engine/classes/Beam#Transparency) properties require a certain number
of segments to display correctly. This is because each segment can only
show a transition between two colors or transparencies. Therefore a
[Beam](/docs/reference/engine/classes/Beam) requires at least n-1 segments to display correctly, where
n is the number of keypoint associated with the beam's
[Color](/docs/reference/engine/classes/Beam#Color) and [Transparency](/docs/reference/engine/classes/Beam#Transparency).

Provide feedback

---

Texture

Read Parallel

The content ID of the texture to be displayed on the beam.

Beam.Texture:ContentId

The content ID of the texture to be displayed on the beam. If this
property is not set, the beam will be displayed as a solid line; this also
occurs when the texture is set to an invalid content ID or the image
associated with the texture has not yet loaded.

The appearance of the texture can be further modified by other beam
properties including [Color](/docs/reference/engine/classes/Beam#Color) and
[Transparency](/docs/reference/engine/classes/Beam#Transparency).

Scaling of the texture is determined by the
[TextureMode](/docs/reference/engine/classes/Beam#TextureMode),
[TextureLength](/docs/reference/engine/classes/Beam#TextureLength), [Width0](/docs/reference/engine/classes/Beam#Width0), and
[Width1](/docs/reference/engine/classes/Beam#Width1) properties.

Provide feedback

---

TextureLength

Read Parallel

Sets the length of the beam's texture, dependent on
[TextureMode](/docs/reference/engine/classes/Beam#TextureMode).

Beam.TextureLength:[number](/docs/luau/numbers)

Sets the length of the beam's texture, dependent on
[TextureMode](/docs/reference/engine/classes/Beam#TextureMode).

Provide feedback

---

TextureMode

Read Parallel

Determines the manner in which the [Texture](/docs/reference/engine/classes/Beam#Texture) scales and
repeats.

Beam.TextureMode:[Enum.TextureMode](/docs/reference/engine/enums/TextureMode)

This property, alongside [TextureLength](/docs/reference/engine/classes/Beam#TextureLength),
determines how a beam's [Texture](/docs/reference/engine/classes/Beam#Texture) repeats.

When set to [Enum.TextureMode.Wrap](/docs/reference/engine/enums/TextureMode#Wrap) or [Enum.TextureMode.Static](/docs/reference/engine/enums/TextureMode#Static), the
texture repetitions will equal the beam's overall length (in studs)
divided by its [TextureLength](/docs/reference/engine/classes/Beam#TextureLength).

![TextureMode diagram with Wrap mode](https://prod.docsiteassets.roblox.com/assets/engine-api/enums/TextureMode/Wrap-Static.png)

When set to [Enum.TextureMode.Stretch](/docs/reference/engine/enums/TextureMode#Stretch), the texture will repeat
[TextureLength](/docs/reference/engine/classes/Beam#TextureLength) times across the beam's overall
length.

![TextureMode diagram with Stretch mode](https://prod.docsiteassets.roblox.com/assets/engine-api/enums/TextureMode/Stretch.png)

Provide feedback

---

TextureSpeed

Read Parallel

Determines the speed at which the [Texture](/docs/reference/engine/classes/Beam#Texture) image moves
along the beam.

Beam.TextureSpeed:[number](/docs/luau/numbers)

Determines the speed at which the [Texture](/docs/reference/engine/classes/Beam#Texture) image moves
along the beam. When this property is a positive value, the beam's texture
will move from [Attachment0](/docs/reference/engine/classes/Beam#Attachment0) to
[Attachment1](/docs/reference/engine/classes/Beam#Attachment1). This direction can be inverted by
setting this property to a negative number.

Provide feedback

---

Transparency

Read Parallel

Determines the transparency of the beam across its segments.

Beam.Transparency:[NumberSequence](/docs/reference/engine/datatypes/NumberSequence)

Determines the transparency of the beam across its segments. This property
is a [NumberSequence](/docs/reference/engine/datatypes/NumberSequence), allowing the transparency to be configured
to vary across the length of the beam.

Consider the following [NumberSequence](/docs/reference/engine/datatypes/NumberSequence) which, when applied to a
beam, would yield the pictured result.

```
local numberSequence = NumberSequence.new({



NumberSequenceKeypoint.new(0, 0), -- Opaque



NumberSequenceKeypoint.new(0.5, 1), -- Transparent



NumberSequenceKeypoint.new(1, 0), -- Opaque



}



)
```

![](https://prod.docsiteassets.roblox.com/assets/lighting-and-effects/beam/Transparency-Applied.png)

Note that the beam's transparency also depends on the number of
[Segments](/docs/reference/engine/classes/Beam#Segments). Each segment of the beam can only show a
transition between two transparencies. Therefore a beam will need to have
at least n-1 segments in order to display correctly, where n is the
number of [NumberSequenceKeypoints](/docs/reference/engine/datatypes/NumberSequenceKeypoint) in the
[NumberSequence](/docs/reference/engine/datatypes/NumberSequence).

Provide feedback

---

Width0

Read Parallel

The width of the beam at its origin
([Attachment0](/docs/reference/engine/classes/Beam#Attachment0)), in studs.

Beam.Width0:[number](/docs/luau/numbers)

The width of the beam at its origin
([Attachment0](/docs/reference/engine/classes/Beam#Attachment0)), in studs. The beam's width will
change linearly to [Width1](/docs/reference/engine/classes/Beam#Width1) studs at its end
([Attachment1](/docs/reference/engine/classes/Beam#Attachment1)).

Provide feedback

---

Width1

Read Parallel

The width of the beam at its end ([Attachment1](/docs/reference/engine/classes/Beam#Attachment1)),
in studs.

Beam.Width1:[number](/docs/luau/numbers)

The width of the beam at its end ([Attachment1](/docs/reference/engine/classes/Beam#Attachment1)),
in studs. The beam's width will change linearly from
[Width0](/docs/reference/engine/classes/Beam#Width0) studs at its origin
([Attachment0](/docs/reference/engine/classes/Beam#Attachment0)).

Provide feedback

---

ZOffset

Read Parallel

The distance, in studs, the beam display is offset relative to the
[CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera).

Beam.ZOffset:[number](/docs/luau/numbers)

The distance, in studs, the beam display is offset relative to the
[CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera). When 0, the beam will be
displayed in its standard position between
[Attachment0](/docs/reference/engine/classes/Beam#Attachment0) and
[Attachment1](/docs/reference/engine/classes/Beam#Attachment1). ZOffset can be either positive
or negative.

This property is particularly useful to avoid "Z‑fighting" when using
multiple [Beams](/docs/reference/engine/classes/Beam) between the same
[Attachments](/docs/reference/engine/classes/Attachment).

Code Samples

Layering Beams

This code sample uses the [Beam.ZOffset](/docs/reference/engine/classes/Beam#ZOffset) property to layer multiple
beams between the same attachments.

```
-- Create beams



local beam1 = Instance.new("Beam")



beam1.Color = ColorSequence.new(Color3.new(1, 0, 0))



beam1.FaceCamera = true



beam1.Width0 = 3



beam1.Width1 = 3



local beam2 = Instance.new("Beam")



beam2.Color = ColorSequence.new(Color3.new(0, 1, 0))



beam2.FaceCamera = true



beam2.Width0 = 2



beam2.Width1 = 2



local beam3 = Instance.new("Beam")



beam3.Color = ColorSequence.new(Color3.new(0, 0, 1))



beam3.FaceCamera = true



beam3.Width0 = 1



beam3.Width1 = 1



-- Layer beams



beam1.ZOffset = 0



beam2.ZOffset = 0.01



beam3.ZOffset = 0.02



-- Create attachments



local attachment0 = Instance.new("Attachment")



attachment0.Position = Vector3.new(0, -10, 0)



attachment0.Parent = workspace.Terrain



local attachment1 = Instance.new("Attachment")



attachment1.Position = Vector3.new(0, 10, 0)



attachment1.Parent = workspace.Terrain



-- Connect beams



beam1.Attachment0 = attachment0



beam1.Attachment1 = attachment1



beam2.Attachment0 = attachment0



beam2.Attachment1 = attachment1



beam3.Attachment0 = attachment0



beam3.Attachment1 = attachment1



-- Parent beams



beam1.Parent = workspace



beam2.Parent = workspace



beam3.Parent = workspace
```

Provide feedback

---

Methods

SetTextureOffset

Sets the current offset of the beam's texture cycle.

Beam:SetTextureOffset(offset:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| offset:[number](/docs/luau/numbers) Default Value: 0 The desired offset of the texture cycle. |

Returns

()

The offset of a beam's texture cycle represents the progress of its
texture animation. This method sets the current offset of the beam's
texture cycle; hence, it can be used to reset the cycle by passing 0 as
the offset parameter.

#### Notes

* The given offset parameter is expected to be a value between 0 and 1,
  but greater values can be used.
* The texture cycle wraps at 0 and 1, meaning the texture is in the same
  position when the offset is at 0 or 1.
* If the [Texture](/docs/reference/engine/classes/Beam#Texture) property is not set, this method
  does nothing.
* Increasing the offset will act in the inverse direction to the
  [TextureSpeed](/docs/reference/engine/classes/Beam#TextureSpeed) property, meaning it will move
  the texture in the opposite direction to the direction the texture
  animates when [TextureSpeed](/docs/reference/engine/classes/Beam#TextureSpeed) is greater than 0.

Provide feedback

---