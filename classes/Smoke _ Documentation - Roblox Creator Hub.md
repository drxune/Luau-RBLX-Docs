# Smoke | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Smoke
Scraped: 2026-01-11T02:38:00.011095Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- Smoke
- BasePart
- Part
- Attachment
- ParticleEmitter
- ParticleEmitter.Lifetime
- ParticleEmitter:Emit()
- Smoke.Enabled
- Instance.Parent
- Instance:Destroy()
- Debris
- ParticleEmitter:Clear()
- ParticleEmitter.Color
- Smoke.Opacity
- Fire
- ParticleEmitter.Enabled
- BasePart.Transparency
- ParticleEmitter.Transparency
- ParticleEmitter.Speed
- Fire.Heat
- Smoke.Color
- ParticleEmitter.Size
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Smoke](/docs/reference/engine/classes/Smoke)

English

Feedback

Engine Class

![Smoke](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Smoke-Dark.webp)Smoke

A particle emitter with the visual aesthetic of smoke.

---

Summary

Properties

|  |
| --- |
| [Color](#Color):[Color3](/docs/reference/engine/datatypes/Color3) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [LocalTransparencyModifier](#LocalTransparencyModifier):[number](/docs/luau/numbers) |
| [Opacity](#Opacity):[number](/docs/luau/numbers) |
| [RiseVelocity](#RiseVelocity):[number](/docs/luau/numbers) |
| [Size](#Size):[number](/docs/luau/numbers) |
| [TimeScale](#TimeScale):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Smoke is one of several particle-emitting classes. Like other particle
emitters of its kind, Smoke objects emit particles when parented to a
[BasePart](/docs/reference/engine/classes/BasePart) (such as a [Part](/docs/reference/engine/classes/Part)) or an [Attachment](/docs/reference/engine/classes/Attachment) within such
a [BasePart](/docs/reference/engine/classes/BasePart). Compared to the [ParticleEmitter](/docs/reference/engine/classes/ParticleEmitter) class, Smoke lacks
many different customization properties and special methods, such as
[ParticleEmitter.Lifetime](/docs/reference/engine/classes/ParticleEmitter#Lifetime) or [ParticleEmitter:Emit()](/docs/reference/engine/classes/ParticleEmitter#Emit). It is
useful to create a quick special effect in a pinch; for more detailed work it
is preferable to use a [ParticleEmitter](/docs/reference/engine/classes/ParticleEmitter) instead.

When [Smoke.Enabled](/docs/reference/engine/classes/Smoke#Enabled) is toggled off, particles emit by this object will
continue to render until their lifetime expires. When a Smoke object's
[Instance.Parent](/docs/reference/engine/classes/Instance#Parent) is set to nil (and/or [Instance:Destroy()](/docs/reference/engine/classes/Instance#Destroy)ed),
all particles will instantly disappear. If this effect is not desired, try
hiding the parent object at a far away position, then removing the Smoke after
a few seconds using [Debris](/docs/reference/engine/classes/Debris) to give the last particles a chance to
expire. This object does not have a [ParticleEmitter:Clear()](/docs/reference/engine/classes/ParticleEmitter#Clear) method,
but it is possible to set the [Instance.Parent](/docs/reference/engine/classes/Instance#Parent) to nil and back to the
exact same object for the same effect.

Smoke particles are only emitted from the center of [BasePart](/docs/reference/engine/classes/BasePart) to which
they are parented. Parenting a Smoke object to an [Attachment](/docs/reference/engine/classes/Attachment) instead
allows customization of the particles' start position.

Code Samples

Add Smoke to All Fire

This code sample adds a Smoke object to every Fire object in the
Workspace. It does this by using a recursive search.

```
local function recurseForFire(object)



-- Check if we found a Fire object that has no Smoke



if object:IsA("Fire") and not object.Parent:FindFirstChildOfClass("Smoke") then



-- Create a smoke effect for this fire



local smoke = Instance.new("Smoke")



smoke.Color = Color3.new(0, 0, 0)



smoke.Opacity = 0.15



smoke.RiseVelocity = 4



smoke.Size = object.Size / 4



smoke.Parent = object.Parent



end



-- Continue search for Fire objects



for _, child in pairs(object:GetChildren()) do



recurseForFire(child)



end



end



recurseForFire(workspace)
```

---

API Reference

Properties

Color

Read Parallel

Determines the color of the smoke particles.

Smoke.Color:[Color3](/docs/reference/engine/datatypes/Color3)

The Color property determines the color of all the particles emit by a
[Smoke](/docs/reference/engine/classes/Smoke) object (both existing and future particles). It behaves
similarly to [ParticleEmitter.Color](/docs/reference/engine/classes/ParticleEmitter#Color), except that it is only one
color and not a [ColorSequence](/docs/reference/engine/datatypes/ColorSequence). A color of white with some
[Smoke.Opacity](/docs/reference/engine/classes/Smoke#Opacity) makes for a nice fog effect, and a very opaque black
color can compliment a [Fire](/docs/reference/engine/classes/Fire) object nicely.

Code Samples

Add Smoke to All Fire

This code sample adds a Smoke object to every Fire object in the
Workspace. It does this by using a recursive search.

```
local function recurseForFire(object)



-- Check if we found a Fire object that has no Smoke



if object:IsA("Fire") and not object.Parent:FindFirstChildOfClass("Smoke") then



-- Create a smoke effect for this fire



local smoke = Instance.new("Smoke")



smoke.Color = Color3.new(0, 0, 0)



smoke.Opacity = 0.15



smoke.RiseVelocity = 4



smoke.Size = object.Size / 4



smoke.Parent = object.Parent



end



-- Continue search for Fire objects



for _, child in pairs(object:GetChildren()) do



recurseForFire(child)



end



end



recurseForFire(workspace)
```

Provide feedback

---

Enabled

Read Parallel

Determines whether smoke particles emit.

Smoke.Enabled:[boolean](/docs/luau/booleans)

The Enabled property, much like [ParticleEmitter.Enabled](/docs/reference/engine/classes/ParticleEmitter#Enabled),
determines whether smoke particles are emitted. Any particles already emit
will continue to render until their lifetime expires. This property is
useful for keeping pre-made smoke effects off until they are needed later.
Since smoke particles are destroyed when the [Smoke](/docs/reference/engine/classes/Smoke) object's
[Instance.Parent](/docs/reference/engine/classes/Instance#Parent) is set to nil, this property is useful in
allowing existing particles the opportunity to expire before destroying
the Fire object altogether. See the function below.

```
local Debris = game:GetService("Debris")



local part = script.Parent



function stopSmoke(smoke)



smoke.Enabled = false -- No more new particles



Debris:AddItem(smoke, 10) -- Remove the object after a delay (after existing particles have expired)



end



stopSmoke(part.Smoke)
```

Code Samples

Add Smoke to All Fire

This code sample adds a Smoke object to every Fire object in the
Workspace. It does this by using a recursive search.

```
local function recurseForFire(object)



-- Check if we found a Fire object that has no Smoke



if object:IsA("Fire") and not object.Parent:FindFirstChildOfClass("Smoke") then



-- Create a smoke effect for this fire



local smoke = Instance.new("Smoke")



smoke.Color = Color3.new(0, 0, 0)



smoke.Opacity = 0.15



smoke.RiseVelocity = 4



smoke.Size = object.Size / 4



smoke.Parent = object.Parent



end



-- Continue search for Fire objects



for _, child in pairs(object:GetChildren()) do



recurseForFire(child)



end



end



recurseForFire(workspace)
```

Provide feedback

---

LocalTransparencyModifier

Hidden

Not Replicated

Read Parallel

Smoke.LocalTransparencyModifier:[number](/docs/luau/numbers)

Provide feedback

---

Opacity

Not Replicated

Read Parallel

Determines how opaque smoke particles render.

Smoke.Opacity:[number](/docs/luau/numbers)

Opacity determines the opaqueness of the smoke particles. It must be in
the range [0, 1]. This property works inversely in comparison to a
part's [BasePart.Transparency](/docs/reference/engine/classes/BasePart#Transparency) or ParticleEmitter's
[ParticleEmitter.Transparency](/docs/reference/engine/classes/ParticleEmitter#Transparency): a value of 0 is completely
invisible, 1 is completely visible.

The texture that Roblox uses for [Smoke](/docs/reference/engine/classes/Smoke) particles is partially
transparent, so setting this property to 1 still yields transparency in
rendered smoke.

Code Samples

Add Smoke to All Fire

This code sample adds a Smoke object to every Fire object in the
Workspace. It does this by using a recursive search.

```
local function recurseForFire(object)



-- Check if we found a Fire object that has no Smoke



if object:IsA("Fire") and not object.Parent:FindFirstChildOfClass("Smoke") then



-- Create a smoke effect for this fire



local smoke = Instance.new("Smoke")



smoke.Color = Color3.new(0, 0, 0)



smoke.Opacity = 0.15



smoke.RiseVelocity = 4



smoke.Size = object.Size / 4



smoke.Parent = object.Parent



end



-- Continue search for Fire objects



for _, child in pairs(object:GetChildren()) do



recurseForFire(child)



end



end



recurseForFire(workspace)
```

Provide feedback

---

RiseVelocity

Not Replicated

Read Parallel

Determines the velocity of the smoke particles.

Smoke.RiseVelocity:[number](/docs/luau/numbers)

RiseVelocity behaves similarly to [ParticleEmitter.Speed](/docs/reference/engine/classes/ParticleEmitter#Speed) and
[Fire.Heat](/docs/reference/engine/classes/Fire#Heat): it determines how fast the smoke particles move during
their lifetime. It must be in the range [-25, 25]. Negative values will
cause particles to emit in the bottom (-Y) direction of the parent
[BasePart](/docs/reference/engine/classes/BasePart).

When using a [Smoke](/docs/reference/engine/classes/Smoke) effect to create fog, set this property to 0.
For large smoke effects, make the rise subtle (2 to 8). For chimneys and
smokestacks, higher values are appropriate.

Code Samples

Add Smoke to All Fire

This code sample adds a Smoke object to every Fire object in the
Workspace. It does this by using a recursive search.

```
local function recurseForFire(object)



-- Check if we found a Fire object that has no Smoke



if object:IsA("Fire") and not object.Parent:FindFirstChildOfClass("Smoke") then



-- Create a smoke effect for this fire



local smoke = Instance.new("Smoke")



smoke.Color = Color3.new(0, 0, 0)



smoke.Opacity = 0.15



smoke.RiseVelocity = 4



smoke.Size = object.Size / 4



smoke.Parent = object.Parent



end



-- Continue search for Fire objects



for _, child in pairs(object:GetChildren()) do



recurseForFire(child)



end



end



recurseForFire(workspace)
```

Provide feedback

---

Size

Not Replicated

Read Parallel

Determines the size of newly emit smoke particles.

Smoke.Size:[number](/docs/luau/numbers)

The Size property of [Smoke](/docs/reference/engine/classes/Smoke) determines the size of the newly emit
smoke particles. Unlike [Smoke.Color](/docs/reference/engine/classes/Smoke#Color), this property will not change
the size of existing particles. It must be in the range [0.1, 100]. Unlike
[ParticleEmitter.Size](/docs/reference/engine/classes/ParticleEmitter#Size), this property is only a number (not a
[NumberSequence](/docs/reference/engine/datatypes/NumberSequence)). Also note also that the size of the particles
is not 1-to-1 with studs; in fact, the size of the smoke particle is more
than twice as large. At the largest size, smoke particles can render
larger than 200 studs wide!

Code Samples

Add Smoke to All Fire

This code sample adds a Smoke object to every Fire object in the
Workspace. It does this by using a recursive search.

```
local function recurseForFire(object)



-- Check if we found a Fire object that has no Smoke



if object:IsA("Fire") and not object.Parent:FindFirstChildOfClass("Smoke") then



-- Create a smoke effect for this fire



local smoke = Instance.new("Smoke")



smoke.Color = Color3.new(0, 0, 0)



smoke.Opacity = 0.15



smoke.RiseVelocity = 4



smoke.Size = object.Size / 4



smoke.Parent = object.Parent



end



-- Continue search for Fire objects



for _, child in pairs(object:GetChildren()) do



recurseForFire(child)



end



end



recurseForFire(workspace)
```

Provide feedback

---

TimeScale

Read Parallel

Value between 0-1 that controls the speed of the particle effect.

Smoke.TimeScale:[number](/docs/luau/numbers)

A value between 0-1 than controls the speed of the particle effect. At 1
it runs at normal speed, at 0.5 it runs at half speed, and at 0 it freezes
time.

Provide feedback

---