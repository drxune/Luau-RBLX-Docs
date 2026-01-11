# ParticleEmitter | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ParticleEmitter
Scraped: 2026-01-11T02:36:03.884272Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- ParticleEmitter
- BasePart
- Attachment
- Enabled
- Rate
- Emit
- Speed
- ShapeInOut
- Orientation
- Lifetime
- Color
- Size
- Drag
- Acceleration
- LockedToPart
- VelocityInheritance
- EmissionDirection
- ParticleEmitter.LightInfluence
- Texture
- Transparency
- LightEmission
- SpreadAngle
- Attachment.Orientation
- Clear()
- Emit()
- FlipbookSizeX
- FlipbookSizeY
- FlipbookFramerate
- FlipbookLayout
- LightInfluence
- PointLight
- RotSpeed
- Rotation
- ShapeStyle
- ShapePartial
- Shape
- Velocity
- Workspace.GlobalWind
- GuiObject.ZIndex
- ParticleEmitter:Emit()
- ParticleEmitter:Clear()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ParticleEmitter](/docs/reference/engine/classes/ParticleEmitter)

English

Feedback

Engine Class

![ParticleEmitter](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/ParticleEmitter-Dark.webp)ParticleEmitter

A special object that emits customizable 2D particles into the world.

---

Summary

Properties

|  |
| --- |
| [Acceleration](#Acceleration):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Brightness](#Brightness):[number](/docs/luau/numbers) |
| [Color](#Color):[ColorSequence](/docs/reference/engine/datatypes/ColorSequence) |
| [Drag](#Drag):[number](/docs/luau/numbers) |
| [EmissionDirection](#EmissionDirection):[Enum.NormalId](/docs/reference/engine/enums/NormalId) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [FlipbookFramerate](#FlipbookFramerate):[NumberRange](/docs/reference/engine/datatypes/NumberRange) |
| [FlipbookIncompatible](#FlipbookIncompatible):[string](/docs/luau/strings) |
| [FlipbookLayout](#FlipbookLayout):[Enum.ParticleFlipbookLayout](/docs/reference/engine/enums/ParticleFlipbookLayout) |
| [FlipbookMode](#FlipbookMode):[Enum.ParticleFlipbookMode](/docs/reference/engine/enums/ParticleFlipbookMode) |
| [FlipbookSizeX](#FlipbookSizeX):[number](/docs/luau/numbers) |
| [FlipbookSizeY](#FlipbookSizeY):[number](/docs/luau/numbers) |
| [FlipbookStartRandom](#FlipbookStartRandom):[boolean](/docs/luau/booleans) |
| [Lifetime](#Lifetime):[NumberRange](/docs/reference/engine/datatypes/NumberRange) |
| [LightEmission](#LightEmission):[number](/docs/luau/numbers) |
| [LightInfluence](#LightInfluence):[number](/docs/luau/numbers) |
| [LocalTransparencyModifier](#LocalTransparencyModifier):[number](/docs/luau/numbers) |
| [LockedToPart](#LockedToPart):[boolean](/docs/luau/booleans) |
| [Orientation](#Orientation):[Enum.ParticleOrientation](/docs/reference/engine/enums/ParticleOrientation) |
| [Rate](#Rate):[number](/docs/luau/numbers) |
| [Rotation](#Rotation):[NumberRange](/docs/reference/engine/datatypes/NumberRange) |
| [RotSpeed](#RotSpeed):[NumberRange](/docs/reference/engine/datatypes/NumberRange) |
| [Shape](#Shape):[Enum.ParticleEmitterShape](/docs/reference/engine/enums/ParticleEmitterShape) |
| [ShapeInOut](#ShapeInOut):[Enum.ParticleEmitterShapeInOut](/docs/reference/engine/enums/ParticleEmitterShapeInOut) |
| [ShapePartial](#ShapePartial):[number](/docs/luau/numbers) |
| [ShapeStyle](#ShapeStyle):[Enum.ParticleEmitterShapeStyle](/docs/reference/engine/enums/ParticleEmitterShapeStyle) |
| [Size](#Size):[NumberSequence](/docs/reference/engine/datatypes/NumberSequence) |
| [Speed](#Speed):[NumberRange](/docs/reference/engine/datatypes/NumberRange) |
| [SpreadAngle](#SpreadAngle):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [Squash](#Squash):[NumberSequence](/docs/reference/engine/datatypes/NumberSequence) |
| [Texture](#Texture):ContentId |
| [TimeScale](#TimeScale):[number](/docs/luau/numbers) |
| [Transparency](#Transparency):[NumberSequence](/docs/reference/engine/datatypes/NumberSequence) |
| [VelocityInheritance](#VelocityInheritance):[number](/docs/luau/numbers) |
| [VelocitySpread](#VelocitySpread):[number](/docs/luau/numbers)  Deprecated |
| [WindAffectsDrag](#WindAffectsDrag):[boolean](/docs/luau/booleans) |
| [ZOffset](#ZOffset):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [Clear](#Clear)():() |
| [Emit](#Emit)(particleCount: [number](/docs/luau/numbers)):() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A ParticleEmitter is a special object that emits customizable 2D particles
into the world. To emit and render particles, it must be parented to a
[BasePart](/docs/reference/engine/classes/BasePart) or an [Attachment](/docs/reference/engine/classes/Attachment) within such a part. When parented to
a [BasePart](/docs/reference/engine/classes/BasePart), particles spawn randomly within the part's bounding box or
[shape](/docs/effects/particle-emitters#shape); when parented to an
[Attachment](/docs/reference/engine/classes/Attachment), particles spawn from the attachment's position.

Particles emit automatically when the emitter is
[Enabled](/docs/reference/engine/classes/ParticleEmitter#Enabled) with a non-zero
[Rate](/docs/reference/engine/classes/ParticleEmitter#Rate), or manually when the
[Emit](/docs/reference/engine/classes/ParticleEmitter#Emit) method is called. With a non-zero
[Speed](/docs/reference/engine/classes/ParticleEmitter#Speed), particles are set in motion outwards
and/or inwards, depending on the [ShapeInOut](/docs/reference/engine/classes/ParticleEmitter#ShapeInOut)
property.

By default, particles face the camera, but the
[Orientation](/docs/reference/engine/classes/ParticleEmitter#Orientation) can be modified to respect the
particle velocity instead.

During the [Lifetime](/docs/reference/engine/classes/ParticleEmitter#Lifetime) of the particles, they
can change appearance according to the [Color](/docs/reference/engine/classes/ParticleEmitter#Color) and
[Size](/docs/reference/engine/classes/ParticleEmitter#Size). Their motion can change over time according
to the [Drag](/docs/reference/engine/classes/ParticleEmitter#Drag) and
[Acceleration](/docs/reference/engine/classes/ParticleEmitter#Acceleration) properties, and they can
also move as their parent moves when they are
[LockedToPart](/docs/reference/engine/classes/ParticleEmitter#LockedToPart) or have a non-zero
[VelocityInheritance](/docs/reference/engine/classes/ParticleEmitter#VelocityInheritance).

To learn more about creating and customizing particle emitters, see
[Particle Emitters](/docs/effects/particle-emitters).

Code Samples

Creating a Particle Emitter from Scratch

This rather lengthy code sample shows how every property of a
ParticleEmitter can be set, including [NumberRange](/docs/reference/engine/datatypes/NumberRange),
[NumberSequence](/docs/reference/engine/datatypes/NumberSequence) and [ColorSequence](/docs/reference/engine/datatypes/ColorSequence) properties. Below is
how the ParticleEmitter should look after every property is set. Try playing
around with the different properties to customize how the effect looks!

```
local emitter = Instance.new("ParticleEmitter")



-- Number of particles = Rate * Lifetime



emitter.Rate = 5 -- Particles per second



emitter.Lifetime = NumberRange.new(1, 1) -- How long the particles should be alive (min, max)



emitter.Enabled = true



-- Visual properties



emitter.Texture = "rbxassetid://1266170131" -- A transparent image of a white ring



-- For Color, build a ColorSequence using ColorSequenceKeypoint



local colorKeypoints = {



-- API: ColorSequenceKeypoint.new(time, color)



ColorSequenceKeypoint.new(0, Color3.new(1, 1, 1)), -- At t=0, White



ColorSequenceKeypoint.new(0.5, Color3.new(1, 0.5, 0)), -- At t=.5, Orange



ColorSequenceKeypoint.new(1, Color3.new(1, 0, 0)), -- At t=1, Red



}



emitter.Color = ColorSequence.new(colorKeypoints)



local numberKeypoints = {



-- API: NumberSequenceKeypoint.new(time, size, envelop)



NumberSequenceKeypoint.new(0, 1), -- At t=0, fully transparent



NumberSequenceKeypoint.new(0.1, 0), -- At t=.1, fully opaque



NumberSequenceKeypoint.new(0.5, 0.25), -- At t=.5, mostly opaque



NumberSequenceKeypoint.new(1, 1), -- At t=1, fully transparent



}



emitter.Transparency = NumberSequence.new(numberKeypoints)



emitter.LightEmission = 1 -- When particles overlap, multiply their color to be brighter



emitter.LightInfluence = 0 -- Don't be affected by world lighting



-- Speed properties



emitter.EmissionDirection = Enum.NormalId.Front -- Emit forwards



emitter.Speed = NumberRange.new(0, 0) -- Speed of zero



emitter.Drag = 0 -- Apply no drag to particle motion



emitter.VelocitySpread = NumberRange.new(0, 0)



emitter.VelocityInheritance = 0 -- Don't inherit parent velocity



emitter.Acceleration = Vector3.new(0, 0, 0)



emitter.LockedToPart = false -- Don't lock the particles to the parent



emitter.SpreadAngle = Vector2.new(0, 0) -- No spread angle on either axis



-- Simulation properties



local numberKeypoints2 = {



NumberSequenceKeypoint.new(0, 0), -- At t=0, size of 0



NumberSequenceKeypoint.new(1, 10), -- At t=1, size of 10



}



emitter.Size = NumberSequence.new(numberKeypoints2)



emitter.ZOffset = -1 -- Render slightly behind the actual position



emitter.Rotation = NumberRange.new(0, 360) -- Start at random rotation



emitter.RotSpeed = NumberRange.new(0) -- Do not rotate during simulation



-- Create an attachment so particles emit from the exact same spot (concentric rings)



local attachment = Instance.new("Attachment")



attachment.Position = Vector3.new(0, 5, 0) -- Move the attachment upwards a little



attachment.Parent = script.Parent



emitter.Parent = attachment
```

---

API Reference

Properties

Acceleration

Read Parallel

Determines the global-axis acceleration of all active particles, measured
in studs per second squared.

ParticleEmitter.Acceleration:[Vector3](/docs/reference/engine/datatypes/Vector3)

The Acceleration property determines how the
[Speed](/docs/reference/engine/classes/ParticleEmitter#Speed) of particles changes over their
lifetime. It is defined using a [Vector3](/docs/reference/engine/datatypes/Vector3) to determine the
acceleration on the global X/Y/Z axes and is measured in studs
per second squared. When changed, this property affects all particles
emitted by the emitter, both current and future.

Acceleration will slow particles down if the vector points in the opposite
[EmissionDirection](/docs/reference/engine/classes/ParticleEmitter#EmissionDirection) in which they
are emitted. Otherwise, it will speed them up.

Provide feedback

---

Brightness

Read Parallel

Scales the light emitted from the emitter when
[ParticleEmitter.LightInfluence](/docs/reference/engine/classes/ParticleEmitter#LightInfluence) is 0.

ParticleEmitter.Brightness:[number](/docs/luau/numbers)

Scales the light emitted from the emitter when
[ParticleEmitter.LightInfluence](/docs/reference/engine/classes/ParticleEmitter#LightInfluence) is 0.

Provide feedback

---

Color

Read Parallel

Determines the color of all active particles over their individual
lifetimes.

ParticleEmitter.Color:[ColorSequence](/docs/reference/engine/datatypes/ColorSequence)

The Color property determines the color of all active particles over
their individual lifetimes. The color applies to the
[Texture](/docs/reference/engine/classes/ParticleEmitter#Texture) when rendering and it uses the
texture alpha along with the emitter's
[Transparency](/docs/reference/engine/classes/ParticleEmitter#Transparency). If an emitter has a
[LightEmission](/docs/reference/engine/classes/ParticleEmitter#LightEmission) value that's greater
than 0, darker colors make particles appear more transparent.

Changing this property affects all particles emitted by the emitter, both
current and future.

When this property uses a gradient [ColorSequence](/docs/reference/engine/datatypes/ColorSequence), a particle's
present color is determined by linearly interpolating on the sequence
using the particle's age and its total lifetime. For example, if a
particle spawned 2 seconds ago and has a 4 second lifetime, the color will
be whatever is 50% of the way through the [ColorSequence](/docs/reference/engine/datatypes/ColorSequence).

Provide feedback

---

Drag

Read Parallel

Determines the rate at which particles will lose half their speed through
exponential decay.

ParticleEmitter.Drag:[number](/docs/luau/numbers)

The Drag property determines the rate in seconds at which individual
particles will lose half their speed via exponential decay. Drag is
applied by scaling the expected velocity from
[Speed](/docs/reference/engine/classes/ParticleEmitter#Speed) and any velocity inherited from the
parent from
[VelocityInheritance](/docs/reference/engine/classes/ParticleEmitter#VelocityInheritance). Setting
this property to a negative value will cause particles' velocities to grow
exponentially.

Provide feedback

---

EmissionDirection

Read Parallel

Determines the face of the object that particles emit from.

ParticleEmitter.EmissionDirection:[Enum.NormalId](/docs/reference/engine/enums/NormalId)

The EmissionDirection property determines the face ([Enum.NormalId](/docs/reference/engine/enums/NormalId))
of the parent object that particles emit from. A negative
[Speed](/docs/reference/engine/classes/ParticleEmitter#Speed) means particles emit in the opposite
direction. [SpreadAngle](/docs/reference/engine/classes/ParticleEmitter#SpreadAngle) further varies
the emission direction.

If you add a [ParticleEmitter](/docs/reference/engine/classes/ParticleEmitter) to an [Attachment](/docs/reference/engine/classes/Attachment), which has a
direction, you can rotate the attachment itself
([Attachment.Orientation](/docs/reference/engine/classes/Attachment#Orientation)) instead of using this property.

Provide feedback

---

Enabled

Read Parallel

Determines if particles emit from the emitter.

ParticleEmitter.Enabled:[boolean](/docs/luau/booleans)

The Enabled property determines if particles emit from the emitter.
Setting this to false stops further particles from spawning, but any
existing particles remain active until they expire. This property is
useful when you have a pre-made particle effect that you want to remain
disabled until you need it to emit particles.

If you want to clear all particles from a disabled emitter, call
[Clear()](/docs/reference/engine/classes/ParticleEmitter#Clear). Then, if desired, call
[Emit()](/docs/reference/engine/classes/ParticleEmitter#Emit) on the emitter to emit and render
particles.

Provide feedback

---

FlipbookFramerate

Read Parallel

Determines how fast the flipbook texture animates in frames per second.

ParticleEmitter.FlipbookFramerate:[NumberRange](/docs/reference/engine/datatypes/NumberRange)

The FlipbookFramerate property determines how fast the flipbook
texture animates in frames per second. Like
[Lifetime](/docs/reference/engine/classes/ParticleEmitter#Lifetime), you can set a minimum and
maximum range to randomize the framerate of the flipbook, with a maximum
of 30 frames per second.

Provide feedback

---

FlipbookIncompatible

Read Parallel

The error message to display if the
[Texture](/docs/reference/engine/classes/ParticleEmitter#Texture) is incompatible for a flipbook.

ParticleEmitter.FlipbookIncompatible:[string](/docs/luau/strings)

The error message to display if the
[Texture](/docs/reference/engine/classes/ParticleEmitter#Texture) is incompatible for a flipbook.
The flipbook texture size must be an exact multiple of the flipbook layout
size.

Provide feedback

---

FlipbookLayout

Read Parallel

Determines the layout of the flipbook texture. Must be None, Grid2x2,
Grid4x4, Grid8x8 or Custom.

ParticleEmitter.FlipbookLayout:[Enum.ParticleFlipbookLayout](/docs/reference/engine/enums/ParticleFlipbookLayout)

The FlipbookLayout property determines the layout of the texture. It
can be any value of the [Enum.ParticleFlipbookLayout](/docs/reference/engine/enums/ParticleFlipbookLayout) enum:

* None – Disable flipbook features and use the texture as a
  single static texture over the particle's lifetime.
* Grid2x2 – 2×2 frames for a 4-frame animation.
* Grid4x4 – 4×4 frames for a 16-frame animation.
* Grid8x8 – 8×8 frames for a 64-frame animation.
* Custom – A custom grid size defined by
  [FlipbookSizeX](/docs/reference/engine/classes/ParticleEmitter#FlipbookSizeX) and
  [FlipbookSizeY](/docs/reference/engine/classes/ParticleEmitter#FlipbookSizeY).

Provide feedback

---

FlipbookMode

Read Parallel

Determines the type of the flipbook animation. Must be Loop, OneShot,
PingPong, or Random.

ParticleEmitter.FlipbookMode:[Enum.ParticleFlipbookMode](/docs/reference/engine/enums/ParticleFlipbookMode)

The FlipbookMode property determines the type of the flipbook
animation. It can be any value of the [Enum.ParticleFlipbookMode](/docs/reference/engine/enums/ParticleFlipbookMode) enum:

* Loop – Continuously play through all frames, starting back at
  the first frame after playing the last.
* OneShot – Play through the animation only once across the
  particle's lifetime. With this setting, the
  [FlipbookFramerate](/docs/reference/engine/classes/ParticleEmitter#FlipbookFramerate) property
  doesn't apply; instead, the framerate is determined by the particle's
  [Lifetime](/docs/reference/engine/classes/ParticleEmitter#Lifetime) divided evenly by the number
  of frames in the animation. OneShot animations are useful for clear
  non-repeating animations, such as an explosion that creates a puff of
  smoke and then fades out.
* PingPong – Play from the first to the last frame, then in
  reverse from the last to the first, repeating throughout the
  [Lifetime](/docs/reference/engine/classes/ParticleEmitter#Lifetime) of the particle.
* Random – Play the frames in a random order,
  blending/crossfading from one frame to the next. This can be useful for
  organic particle textures at low framerates, such as stars slowly
  twinkling between subtly different shapes.

Provide feedback

---

FlipbookSizeX

Read Parallel

Defines the number of horizontal frames in a custom flipbook layout.

ParticleEmitter.FlipbookSizeX:[number](/docs/luau/numbers)

The FlipbookSizeX property defines the number of horizontal frames
(columns) in a custom flipbook layout. This property only applies when
[FlipbookLayout](/docs/reference/engine/classes/ParticleEmitter#FlipbookLayout) is set to
[Custom](/docs/reference/engine/enums/ParticleFlipbookLayout#Custom).

Provide feedback

---

FlipbookSizeY

Read Parallel

Defines the number of vertical frames in a custom flipbook layout.

ParticleEmitter.FlipbookSizeY:[number](/docs/luau/numbers)

The FlipbookSizeY property defines the number of vertical frames
(rows) in a custom flipbook layout. This property only applies when
[FlipbookLayout](/docs/reference/engine/classes/ParticleEmitter#FlipbookLayout) is set to
[Custom](/docs/reference/engine/enums/ParticleFlipbookLayout#Custom).

Provide feedback

---

FlipbookStartRandom

Read Parallel

Determines whether the animation starts at a random frame chosen per
particle instead of always starting at frame zero.

ParticleEmitter.FlipbookStartRandom:[boolean](/docs/luau/booleans)

The FlipbookStartRandom property determines whether each particle
begins at a random frame of the animation instead of always starting at
the first frame. One use case is to enable this property and also set
[FlipbookFramerate](/docs/reference/engine/classes/ParticleEmitter#FlipbookFramerate) to zero,
causing each emitted particle to be a static frame chosen randomly from
the flipbook texture.

Provide feedback

---

Lifetime

Read Parallel

Defines a random range of ages for newly emitted particles.

ParticleEmitter.Lifetime:[NumberRange](/docs/reference/engine/datatypes/NumberRange)

The Lifetime property defines the maximum and minimum ages for newly
emitted particles. Lifetimes are stored on a per-particle basis, so if
this value is changed, existing particles will stay active until their
randomly chosen lifetime ends. A lifetime of 0 will prevent particles from
emitting at all.

Provide feedback

---

LightEmission

Read Parallel

Determines how much particles' colors are blended with the colors behind
them.

ParticleEmitter.LightEmission:[number](/docs/luau/numbers)

The LightEmission property determines the blending of the
[Texture](/docs/reference/engine/classes/ParticleEmitter#Texture) colors with the colors behind
them. A value of 0 uses normal blending mode while a value of 1 uses
additive blending. When changed, this property instantly affects all
particles owned by the emitter, both current and future.

This property should not be confused with
[LightInfluence](/docs/reference/engine/classes/ParticleEmitter#LightInfluence) which determines how
particles are affected by environmental light.

This property does not cause particles to light the environment around
them. To accomplish that, consider using a [PointLight](/docs/reference/engine/classes/PointLight).

Provide feedback

---

LightInfluence

Read Parallel

Determines how much particles are influenced by the environmental light.

ParticleEmitter.LightInfluence:[number](/docs/luau/numbers)

The LightInfluence property determines how much environmental light
affects the color of individual particles when they render. It must be in
the range of 0–1; behavior of values outside of this range are not
defined. At 0, particles are not influenced by light at all (they retain
full brightness); at 1, particles are fully influenced by light (in
complete darkness, particles will be black).

By default, this value is 1 if inserted with Studio tools. If inserted
using [Instance.new()](/docs/reference/engine/datatypes/Instance#new), it is 0.

Provide feedback

---

LocalTransparencyModifier

Hidden

Not Replicated

Read Parallel

ParticleEmitter.LocalTransparencyModifier:[number](/docs/luau/numbers)

Provide feedback

---

LockedToPart

Read Parallel

Determines whether the particles rigidly move with the part they're being
emitted from.

ParticleEmitter.LockedToPart:[boolean](/docs/luau/booleans)

The LockedToPart property determines if particles "stick" to the
emission source (the [Attachment](/docs/reference/engine/classes/Attachment) or [BasePart](/docs/reference/engine/classes/BasePart) to which the
[ParticleEmitter](/docs/reference/engine/classes/ParticleEmitter) is parented). If true, active particles will
move in lock step if the parent object moves.

Alternatively, consider using the
[VelocityInheritance](/docs/reference/engine/classes/ParticleEmitter#VelocityInheritance) property
with a value of 1 which may be more appropriate for some effects.

Provide feedback

---

Orientation

Read Parallel

Specifies how to orient particles.

ParticleEmitter.Orientation:[Enum.ParticleOrientation](/docs/reference/engine/enums/ParticleOrientation)

The Orientation property determines which orientation mode to use for
an emitter's particle geometry.

| Orientation | Particle Behavior |
| --- | --- |
| **FacingCamera** | Standard camera-facing billboard quad; default behavior. |
| **FacingCameraWorldUp** | Facing the camera, but rotating only on the vertical upward world **Y** axis. |
| **VelocityParallel** | Aligned parallel to their direction of movement. |
| **VelocityPerpendicular** | Aligned perpendicular to their direction movement. |

Provide feedback

---

Rate

Read Parallel

Determines the number of particles emitted per second.

ParticleEmitter.Rate:[number](/docs/luau/numbers)

The Rate property determines how many particles are emitted per second
while the emitter is [Enabled](/docs/reference/engine/classes/ParticleEmitter#Enabled). It is the
inverse of frequency, meaning that a rate of 5 emits a particle every 0.2
seconds. When changed, this property has no affect on any active
particles.

Provide feedback

---

Rotation

Read Parallel

Determines the range of rotations in degrees for newly emitted particles.

ParticleEmitter.Rotation:[NumberRange](/docs/reference/engine/datatypes/NumberRange)

The Rotation property determines the range of rotations in degrees for
newly emitted particles, measured in degrees. Positive values are in the
clockwise direction. This property is commonly set to [0, 360] to
provide a completely random rotation to new particles.
[RotSpeed](/docs/reference/engine/classes/ParticleEmitter#RotSpeed) also influences the rotation of
a particle over its lifetime.

Changes to this value only affect new particles; existing particles
maintain the rotation at which they were originally emitted.

Provide feedback

---

RotSpeed

Read Parallel

Determines the range of angular speeds of emitted particles, measured in
degrees per second.

ParticleEmitter.RotSpeed:[NumberRange](/docs/reference/engine/datatypes/NumberRange)

The RotSpeed property determines a random range of angular speeds for
newly emitted particles, measured in degrees per second. A random angular
speed is chosen upon emission, so changing this property doesn't affect
active particles. This property, along with
[Rotation](/docs/reference/engine/classes/ParticleEmitter#Rotation), affects the angle of the
rendered particle image.

Particles with very high angular speeds can appear to rotate slower or not
at all, since the angle of rotation is synchronized with the software
render speed. For example, if particles rotate at exactly 360 degrees
every frame, there will be no apparent change in rotation.

Provide feedback

---

Shape

Read Parallel

Sets the shape of the emitter to either a box, sphere, cylinder, or disc.

ParticleEmitter.Shape:[Enum.ParticleEmitterShape](/docs/reference/engine/enums/ParticleEmitterShape)

The Shape property sets the shape of the emitter to either a box,
sphere, cylinder, or disc. After you make a selection, you can adjust the
[ShapeStyle](/docs/reference/engine/classes/ParticleEmitter#ShapeStyle),
[ShapeInOut](/docs/reference/engine/classes/ParticleEmitter#ShapeInOut), and
[ShapePartial](/docs/reference/engine/classes/ParticleEmitter#ShapePartial) properties to further
customize particle emission. For visual examples, see
[here](/docs/effects/particle-emitters#shape).

Provide feedback

---

ShapeInOut

Read Parallel

Sets whether particles emit outward only, inward only, or in both
directions.

ParticleEmitter.ShapeInOut:[Enum.ParticleEmitterShapeInOut](/docs/reference/engine/enums/ParticleEmitterShapeInOut)

Sets whether particles emit outward only, inward only, or in both
directions. For visual examples, see
[here](/docs/effects/particle-emitters#shape).

Provide feedback

---

ShapePartial

Read Parallel

Influences particle emission from cylinder, disc, sphere, and box shapes.

ParticleEmitter.ShapePartial:[number](/docs/luau/numbers)

Depending on the [Shape](/docs/reference/engine/classes/ParticleEmitter#Shape) value, this property
performs a different action:

* For cylinders, it specifies the top radius proportion. A value of 0
  means the top of the cylinder has zero radius, making it a cone. A value
  of 1 means the cylinder has no deformation.
* For discs, it specifies the inner radius proportion. A value of 0 means
  the disc is fully closed (circle/ellipse), while a value of 1 means
  emission only occurs on the outermost rim of the disc. Values between 0
  and 1 emit from an annulus with a certain thickness.
* For spheres, it specifies the hemispherical angle over which particles
  emit. A value of 1 means particles emit from the entire sphere; a value
  of 0.5 means particles emit from a half-dome; a value of 0 means
  particles only emit from a single point at the north pole.

For visual examples, see
[here](/docs/effects/particle-emitters#shape).

Provide feedback

---

ShapeStyle

Read Parallel

Sets particle emission to either volumetric or surface-only emission.

ParticleEmitter.ShapeStyle:[Enum.ParticleEmitterShapeStyle](/docs/reference/engine/enums/ParticleEmitterShapeStyle)

Sets particle emission to either volumetric or surface-only emission. For
visual examples, see [here](/docs/effects/particle-emitters#shape).

Provide feedback

---

Size

Read Parallel

Determines the world size over individual particles' lifetimes.

ParticleEmitter.Size:[NumberSequence](/docs/reference/engine/datatypes/NumberSequence)

The Size property determines the world size of all active particles
over their individual lifetimes. This property represents the dimensions
of the square [Texture](/docs/reference/engine/classes/ParticleEmitter#Texture) for each particle.
It is a [NumberSequence](/docs/reference/engine/datatypes/NumberSequence) that works similarly to
[Transparency](/docs/reference/engine/classes/ParticleEmitter#Transparency).

A particle's present size is determined by linearly interpolating on this
sequence using the particle's age and its total lifetime. For example, if
a particle spawned 2 seconds ago and has a 4 second lifetime, the size
will be whatever is 50% of the way through the [NumberSequence](/docs/reference/engine/datatypes/NumberSequence).
For any [NumberSequenceKeypoint](/docs/reference/engine/datatypes/NumberSequenceKeypoint) with a non-zero envelope value,
a random value in the envelope range is chosen for each keypoint for each
particle when it emits.

Provide feedback

---

Speed

Read Parallel

Determines a random range of velocities (minimum to maximum) at which new
particles will emit, measured in studs per second.

ParticleEmitter.Speed:[NumberRange](/docs/reference/engine/datatypes/NumberRange)

The Speed property determines a random range of velocities (minimum to
maximum) at which new particles will emit, measured in studs per second.
Each particle's velocity is chosen upon emission and it applies in the
[EmissionDirection](/docs/reference/engine/classes/ParticleEmitter#EmissionDirection). Negative
values cause particles to travel in reverse.

Note that changing [Speed](/docs/reference/engine/classes/ParticleEmitter#Speed) does not affect
active particles and they retain whatever speed they already have.
However, [Acceleration](/docs/reference/engine/classes/ParticleEmitter#Acceleration),
[Drag](/docs/reference/engine/classes/ParticleEmitter#Drag), and
[VelocityInheritance](/docs/reference/engine/classes/ParticleEmitter#VelocityInheritance) can be
used to affect the speed of active particles over their lifetime.

Provide feedback

---

SpreadAngle

Read Parallel

Determines the angles at which particles may be randomly emit, measured in
degrees.

ParticleEmitter.SpreadAngle:[Vector2](/docs/reference/engine/datatypes/Vector2)

The SpreadAngle property determines the random angles at which a
particle may be emitted. For example, if the
[EmissionDirection](/docs/reference/engine/classes/ParticleEmitter#EmissionDirection) is Top
(+Y), this [Vector2](/docs/reference/engine/datatypes/Vector2) describes the size of the random angle
spread on the X/Z axes, in degrees.

Setting one axis to 360 will cause particles to emit in all direction in a
circle. Setting both to 360 will cause particles to emit in all
directions in a sphere.

Provide feedback

---

Squash

Read Parallel

Allows for non-uniform scaling of particles, curve-controlled over their
lifetime.

ParticleEmitter.Squash:[NumberSequence](/docs/reference/engine/datatypes/NumberSequence)

Allows for non-uniform scaling of particles, curve-controlled over their
lifetime. Values greater than 0 cause particles to both shrink
horizontally and grow vertically, while values less than 0 cause particles
to both grow horizontally and shrink vertically.

Provide feedback

---

Texture

Read Parallel

Determines the image rendered on particles.

ParticleEmitter.Texture:ContentId

The Texture property determines the image rendered on particles. This
image is influenced by [Color](/docs/reference/engine/classes/ParticleEmitter#Color),
[Transparency](/docs/reference/engine/classes/ParticleEmitter#Transparency),
[LightInfluence](/docs/reference/engine/classes/ParticleEmitter#LightInfluence), and
[LightEmission](/docs/reference/engine/classes/ParticleEmitter#LightEmission). Textures with
transparent backgrounds work best for particles.

Provide feedback

---

TimeScale

Read Parallel

Value between 0 and 1 that controls the speed of the particle effect.

ParticleEmitter.TimeScale:[number](/docs/luau/numbers)

A value between 0 and 1 that controls the speed of the particle effect. At
1, it runs at normal speed; at 0.5 it runs at half speed; at 0 it freezes
in time.

Provide feedback

---

Transparency

Read Parallel

Determines the transparency of particles over their individual lifetimes.

ParticleEmitter.Transparency:[NumberSequence](/docs/reference/engine/datatypes/NumberSequence)

The Transparency property determines the transparency of all active
particles over their individual lifetimes. It works similar to
[Size](/docs/reference/engine/classes/ParticleEmitter#Size) in how it affects particles over time.
In terms of rendering, a value of 0 is completely visible (opaque) and a
value of 1 is completely invisible (not rendered at all).

A particle's present transparency is determined by linearly interpolating
on this sequence using the particle's age and its total lifetime. For
example, if a particle spawned 2 seconds ago and has a 4 second lifetime,
the transparency will be whatever is 50% of the way through the
[NumberSequence](/docs/reference/engine/datatypes/NumberSequence). For any [NumberSequenceKeypoint](/docs/reference/engine/datatypes/NumberSequenceKeypoint) with
a non-zero envelope value, a random value in the envelope range is chosen
for each keypoint for each particle when it emits.

Provide feedback

---

VelocityInheritance

Read Parallel

Determines how much of the parent's velocity is inherited by particles
when emitted.

ParticleEmitter.VelocityInheritance:[number](/docs/luau/numbers)

The VelocityInheritance property determines how much of the parent
part's [Velocity](/docs/reference/engine/classes/BasePart#Velocity) is inherited by particles when
they are emitted. A value of 0 means that no velocity is inherited, while
a value of 1 means the particle will have the exact same speed as the
parent [BasePart](/docs/reference/engine/classes/BasePart).

When used in conjunction with [Drag](/docs/reference/engine/classes/ParticleEmitter#Drag), a
particle emitter can appear to "shed" particles from a moving part.

Provide feedback

---

VelocitySpread

Deprecated

Show details

---

WindAffectsDrag

Read Parallel

Whether emitted particles follow the [Workspace.GlobalWind](/docs/reference/engine/classes/Workspace#GlobalWind) vector.

ParticleEmitter.WindAffectsDrag:[boolean](/docs/luau/booleans)

If true, emitted particles follow the [Workspace.GlobalWind](/docs/reference/engine/classes/Workspace#GlobalWind) vector.
Only applies if the [Drag](/docs/reference/engine/classes/ParticleEmitter#Drag) property is greater
than 0.

Provide feedback

---

ZOffset

Read Parallel

Determines the forward-backward render position of particles; used to
control what particles render on top/bottom.

ParticleEmitter.ZOffset:[number](/docs/luau/numbers)

The ZOffset property determines the forward-backward render position
of particles, in studs, without changing their size on the screen. When
changed, this property affects both current and future particles. Note
that this property accepts fractional values; it is not like
[GuiObject.ZIndex](/docs/reference/engine/classes/GuiObject#ZIndex) (an integer).

Positive values move particles closer to the camera and negative values
move particles away. Sufficiently negative values can cause particles to
render inside or behind the parent part.

Provide feedback

---

Methods

Clear

Clears all particles that have been emitted.

ParticleEmitter:Clear():()

Returns

()

The Clear method instantly clears all existing particles that have
been emitted by the [ParticleEmitter](/docs/reference/engine/classes/ParticleEmitter) through its natural emission
(non-zero [Rate](/docs/reference/engine/classes/ParticleEmitter#Rate) on an
[Enabled](/docs/reference/engine/classes/ParticleEmitter#Enabled) emitter) or via
[Emit()](/docs/reference/engine/classes/ParticleEmitter#Emit).

Code Samples

ParticleEmitter Burst

This code sample causes a ParticleEmitter to [ParticleEmitter:Emit()](/docs/reference/engine/classes/ParticleEmitter#Emit)
particles in bursts of 10 every 2 seconds. It [ParticleEmitter:Clear()](/docs/reference/engine/classes/ParticleEmitter#Clear)s
any existing particles before doing so.

```
local emitter = script.Parent



while true do



emitter:Clear()



emitter:Emit(10)



task.wait(2)



end
```

Provide feedback

---

Emit

Emits a given number of particles.

ParticleEmitter:Emit(particleCount:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| particleCount:[number](/docs/luau/numbers) Default Value: 16 The number of particles to emit. |

Returns

()

The Emit method will cause the [ParticleEmitter](/docs/reference/engine/classes/ParticleEmitter) to instantly
emit the given number of particles.

Code Samples

Emit Particles Over Distance

This code sample causes a parent ParticleEmitter to
[ParticleEmitter:Emit()](/docs/reference/engine/classes/ParticleEmitter#Emit) particles based on how far the parent
BasePart moves.

```
local RunService = game:GetService("RunService")



local emitter = script.Parent



local part = emitter.Parent



local PARTICLES_PER_STUD = 3



local lastPosition = part.Position



local distance = 0



local function onStep()



local displacement = part.Position - lastPosition



distance = distance + displacement.magnitude



local n = math.floor(distance * PARTICLES_PER_STUD)



emitter:Emit(n)



distance = distance - n / PARTICLES_PER_STUD



lastPosition = part.Position



end



RunService.Stepped:Connect(onStep)



emitter.Enabled = false
```

ParticleEmitter Burst

This code sample causes a ParticleEmitter to [ParticleEmitter:Emit()](/docs/reference/engine/classes/ParticleEmitter#Emit)
particles in bursts of 10 every 2 seconds. It [ParticleEmitter:Clear()](/docs/reference/engine/classes/ParticleEmitter#Clear)s
any existing particles before doing so.

```
local emitter = script.Parent



while true do



emitter:Clear()



emitter:Emit(10)



task.wait(2)



end
```

Provide feedback

---