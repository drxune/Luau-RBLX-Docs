# Fire | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Fire
Scraped: 2026-01-11T02:38:33.684374Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- Fire
- Smoke
- Sparkles
- BasePart
- Attachment
- Enabled
- ParticleEmitter
- Heat
- Attachment.CFrame
- Size
- Color
- SecondaryColor
- Parent
- ParticleEmitter:Clear()
- PointLight
- Workspace
- ParticleEmitter.Enabled
- ParticleEmitter.Acceleration
- ParticleEmitter.LightEmission
- ParticleEmitter.Size
- Brightness
- Range
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Fire](/docs/reference/engine/classes/Fire)

English

Feedback

Engine Class

![Fire](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Fire-Dark.webp)Fire

A preconfigured particle emitter with the visual aesthetic of fire.

---

Summary

Properties

|  |
| --- |
| [Color](#Color):[Color3](/docs/reference/engine/datatypes/Color3) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [Heat](#Heat):[number](/docs/luau/numbers) |
| [LocalTransparencyModifier](#LocalTransparencyModifier):[number](/docs/luau/numbers) |
| [SecondaryColor](#SecondaryColor):[Color3](/docs/reference/engine/datatypes/Color3) |
| [Size](#Size):[number](/docs/luau/numbers) |
| [size](#size):[number](/docs/luau/numbers)  Deprecated |
| [TimeScale](#TimeScale):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[Fire](/docs/reference/engine/classes/Fire) is one of several preconfigured particle-emitting classes,
alongside [Smoke](/docs/reference/engine/classes/Smoke), [Sparkles](/docs/reference/engine/classes/Sparkles), and others. Like the others, it
emits particles when parented to a [BasePart](/docs/reference/engine/classes/BasePart) or an [Attachment](/docs/reference/engine/classes/Attachment)
while [Enabled](/docs/reference/engine/classes/Fire#Enabled). This object is useful to create a quick
visual effect for fire, but for more detailed work it's recommended that you
use a [ParticleEmitter](/docs/reference/engine/classes/ParticleEmitter) instead.

Particles emit from the center of the parent in an upward (+Y) direction,
but a negative [Heat](/docs/reference/engine/classes/Fire#Heat) value may be used to emit particles
downward (-Y). Using an [Attachment](/docs/reference/engine/classes/Attachment) as the parent instead of a
[BasePart](/docs/reference/engine/classes/BasePart) allows for the emission position/direction to be modified by
changing the [Attachment.CFrame](/docs/reference/engine/classes/Attachment#CFrame) or related properties.

[Fire](/docs/reference/engine/classes/Fire) objects consist of two emitters, each affected in various ways by
the [Size](/docs/reference/engine/classes/Fire#Size), [Heat](/docs/reference/engine/classes/Fire#Heat), [Color](/docs/reference/engine/classes/Fire#Color),
and [SecondaryColor](/docs/reference/engine/classes/Fire#SecondaryColor) properties. Particles which
emit from the smaller, secondary emitter have a significantly longer lifetime
(and rise farther) than those emitted by the primary emitter.

When [Enabled](/docs/reference/engine/classes/Fire#Enabled) is off, existing particles continue to
render until they expire. However, if the [Fire](/docs/reference/engine/classes/Fire) object's
[Parent](/docs/reference/engine/classes/Instance#Parent) is set to nil, all existing particles
immediately disappear, similar to the behavior of
[ParticleEmitter:Clear()](/docs/reference/engine/classes/ParticleEmitter#Clear).

[Fire](/docs/reference/engine/classes/Fire) objects emit no light on their own. To help create a cohesive
environment around a burning object, try adding a [PointLight](/docs/reference/engine/classes/PointLight) with an
orange [Color](/docs/reference/engine/classes/Light#Color).

Code Samples

Lighting Torches

This code sample adds [Fire](/docs/reference/engine/classes/Fire) to all [BasePart](/docs/reference/engine/classes/BasePart) instances in the [Workspace](/docs/reference/engine/classes/Workspace) named
Torch.

```
local Workspace = game:GetService("Workspace")



for _, descendant in Workspace:GetDescendants() do



if descendant.Name == "Torch" and descendant:IsA("BasePart") then



local fire = Instance.new("Fire")



fire.Heat = 10



fire.SecondaryColor = Color3.new(1, 1, 1)



fire.Size = math.max(descendant.Size.X, descendant.Size.Z) -- Pick the larger of the two dimensions



fire.Parent = descendant



end



end
```

---

API Reference

Properties

Color

Read Parallel

Determines the color of the primary (outer) flame particles.

Fire.Color:[Color3](/docs/reference/engine/datatypes/Color3)

This property determines the color of the larger particles emitted by a
[Fire](/docs/reference/engine/classes/Fire) object. It is essentially the color of the outer portion of
the flame.

In general, the cooler flames are on the outside of a fire. Therefore,
fire looks more realistic if the outer portions are red or orange-yellow.
A fire that is bright all throughout doesn't look very realistic, so avoid
setting this property to yellow or white.

Provide feedback

---

Enabled

Read Parallel

Determines whether flame particles are emit.

Fire.Enabled:[boolean](/docs/luau/booleans)

This property, much like [ParticleEmitter.Enabled](/docs/reference/engine/classes/ParticleEmitter#Enabled), determines
whether flame particles are emitted. Any particles already emitted will
continue to render until their lifetime expires.

Since all fire particles are destroyed when the [Fire](/docs/reference/engine/classes/Fire) object's
[Parent](/docs/reference/engine/classes/Instance#Parent) is set to nil, this property is useful in
allowing existing particles the opportunity to expire before destroying
the [Fire](/docs/reference/engine/classes/Fire) object altogether (see the code example below).

```
local Debris = game:GetService("Debris")



local function douseFlames(fire)



fire.Enabled = false -- No more new particles



Debris:AddItem(fire, 2) -- Remove the object after existing particles have expired



end



douseFlames(part.Fire)
```

Provide feedback

---

Heat

Not Replicated

Read Parallel

Determines the velocity at which particles are emit.

Fire.Heat:[number](/docs/luau/numbers)

This property determines how fast particles are emitted from the
[Fire](/docs/reference/engine/classes/Fire) object. It is limited to the range of -25 to 25
inclusive. Positive values are in the top (+Y) direction of the parent
[BasePart](/docs/reference/engine/classes/BasePart) or [Attachment](/docs/reference/engine/classes/Attachment), while negative values are in the
downward (-Y) direction. It also affects the
[ParticleEmitter.Acceleration](/docs/reference/engine/classes/ParticleEmitter#Acceleration) of the inner particles.

Provide feedback

---

LocalTransparencyModifier

Hidden

Not Replicated

Read Parallel

A multiplier for the [Fire](/docs/reference/engine/classes/Fire) object's transparency that is only
visible to the local client.

Fire.LocalTransparencyModifier:[number](/docs/luau/numbers)

This property is a multiplier for the [Fire](/docs/reference/engine/classes/Fire) object's transparency
that is only visible to the local client. It does not replicate from
client to server and is useful for when the object should appear
differently for a specific client.

Provide feedback

---

SecondaryColor

Read Parallel

Determines the color of the of the secondary (inner) flame particles.

Fire.SecondaryColor:[Color3](/docs/reference/engine/datatypes/Color3)

This property determines the color of the smaller particles emitted by a
[Fire](/docs/reference/engine/classes/Fire) object. It is essentially the color of the inner portion of
the flame.

Note that the inner particles use a [ParticleEmitter.LightEmission](/docs/reference/engine/classes/ParticleEmitter#LightEmission)
of 1, so darker colors will instead cause the particles to appear
transparent, and black will stop rendering inner particles altogether.

Provide feedback

---

Size

Not Replicated

Read Parallel

Determines the size of the flame particles.

Fire.Size:[number](/docs/luau/numbers)

This property determines the size of the flame particles. It must be in
the range of 2 to 30. Unlike [ParticleEmitter.Size](/docs/reference/engine/classes/ParticleEmitter#Size), the actual
size of the flames will not match 1:1 with the equivalent size in studs;
it is somewhat smaller.

If you add a [PointLight](/docs/reference/engine/classes/PointLight) as a sibling to the [Fire](/docs/reference/engine/classes/Fire) object to
generate light, try setting the light's
[Brightness](/docs/reference/engine/classes/PointLight#Brightness) and
[Range](/docs/reference/engine/classes/PointLight#Range) proportional to this property so that
larger flames produce more light.

Provide feedback

---

size

Deprecated

Show details

---

TimeScale

Read Parallel

Controls the speed of the particle effect.

Fire.TimeScale:[number](/docs/luau/numbers)

A value between 0 and 1 than controls the speed of the particle
effect. 1 runs at normal speed, 0.5 runs at half speed, and 0
freezes time.

Provide feedback

---