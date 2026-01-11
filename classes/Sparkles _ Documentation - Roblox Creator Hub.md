# Sparkles | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Sparkles
Scraped: 2026-01-11T02:32:10.654834Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- Sparkles
- BasePart
- Part
- Attachment
- ParticleEmitter
- ParticleEmitter.Lifetime
- ParticleEmitter:Emit()
- Sparkles.Enabled
- Instance.Parent
- Instance:Destroy()
- Debris
- ParticleEmitter:Clear()
- ParticleEmitter.Enabled
- Sparkles.Color
- ParticleEmitter.Color
- ParticleEmitter.LightEmission
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Sparkles](/docs/reference/engine/classes/Sparkles)

English

Feedback

Engine Class

![Sparkles](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Sparkles-Dark.webp)Sparkles

A particle emitter with the visual aesthetic of sparkles.

---

Summary

Properties

|  |
| --- |
| [Color](#Color):[Color3](/docs/reference/engine/datatypes/Color3)  Deprecated |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [LocalTransparencyModifier](#LocalTransparencyModifier):[number](/docs/luau/numbers) |
| [SparkleColor](#SparkleColor):[Color3](/docs/reference/engine/datatypes/Color3) |
| [TimeScale](#TimeScale):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Sparkles is one of several particle-emitting classes. Like other particle
emitters of its kind, Sparkles objects emit particles when parented to a
[BasePart](/docs/reference/engine/classes/BasePart) (such as a [Part](/docs/reference/engine/classes/Part)) or an [Attachment](/docs/reference/engine/classes/Attachment) within such
a [BasePart](/docs/reference/engine/classes/BasePart). Compared to the [ParticleEmitter](/docs/reference/engine/classes/ParticleEmitter) class, Sparkles
lacks many different customization properties and special methods, such as
[ParticleEmitter.Lifetime](/docs/reference/engine/classes/ParticleEmitter#Lifetime) or [ParticleEmitter:Emit()](/docs/reference/engine/classes/ParticleEmitter#Emit). It is
useful to create a quick special effect in a pinch; for more detailed work it
is preferable to use a [ParticleEmitter](/docs/reference/engine/classes/ParticleEmitter) instead.

When [Sparkles.Enabled](/docs/reference/engine/classes/Sparkles#Enabled) is toggled off, particles emit by this object
will continue to render until their lifetime expires. When a Sparkles object's
[Instance.Parent](/docs/reference/engine/classes/Instance#Parent) is set to nil (and/or [Instance:Destroy()](/docs/reference/engine/classes/Instance#Destroy)ed),
all particles will instantly disappear. If this effect is not desired, try
hiding the parent object at a far away position, then removing the Sparkles
after a few seconds using [Debris](/docs/reference/engine/classes/Debris) to give the last particles a chance
to expire. This object does not have a [ParticleEmitter:Clear()](/docs/reference/engine/classes/ParticleEmitter#Clear) method,
but it is possible to set the [Instance.Parent](/docs/reference/engine/classes/Instance#Parent) to nil and back to the
exact same object for the same effect.

Sparkles particles are only emitted from the center of [BasePart](/docs/reference/engine/classes/BasePart) to
which they are parented. Parenting a Sparkles object to an [Attachment](/docs/reference/engine/classes/Attachment)
instead allows customization of the particles' start position.

Code Samples

Give Sparkles

The code sample below gives any new players sparkles that are colored the same
as their torso color.

```
local Players = game:GetService("Players")



local function onCharacterSpawned(character)



local hrp = character:WaitForChild("HumanoidRootPart")



-- Add sparkles that are colored to the player's torso color



local sparkles = Instance.new("Sparkles")



sparkles.Parent = hrp



sparkles.SparkleColor = character:WaitForChild("Body Colors").TorsoColor.Color



sparkles.Enabled = true



end



local function onPlayerAdded(player)



player.CharacterAdded:Connect(onCharacterSpawned)



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

---

API Reference

Properties

Color

Deprecated

Show details

---

Enabled

Read Parallel

Determines whether sparkles are emit.

Sparkles.Enabled:[boolean](/docs/luau/booleans)

The Enabled property, much like [ParticleEmitter.Enabled](/docs/reference/engine/classes/ParticleEmitter#Enabled),
determines whether sparkle particles are emit. Any particles already emit
will continue to render until their lifetime expires. This property is
useful for keeping pre-made sparkle effects off until they are needed
later. Since sparkle particles are destroyed when the Sparkle object's
[Instance.Parent](/docs/reference/engine/classes/Instance#Parent) is set to nil, this property is useful in
allowing existing particles the opportunity to expire before destroying
the Fire object altogether. See the function below.

```
local Debris = game:GetService("Debris")



local part = script.Parent



function stopSparkling(sparkles)



sparkles.Enabled = false -- No more new particles



Debris:AddItem(sparkles, 4) -- Remove the object after a delay (after existing particles have expired)



end



stopSparkling(part.Sparkles)
```

Code Samples

Give Sparkles

The code sample below gives any new players sparkles that are colored the same
as their torso color.

```
local Players = game:GetService("Players")



local function onCharacterSpawned(character)



local hrp = character:WaitForChild("HumanoidRootPart")



-- Add sparkles that are colored to the player's torso color



local sparkles = Instance.new("Sparkles")



sparkles.Parent = hrp



sparkles.SparkleColor = character:WaitForChild("Body Colors").TorsoColor.Color



sparkles.Enabled = true



end



local function onPlayerAdded(player)



player.CharacterAdded:Connect(onCharacterSpawned)



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Provide feedback

---

LocalTransparencyModifier

Hidden

Not Replicated

Read Parallel

Sparkles.LocalTransparencyModifier:[number](/docs/luau/numbers)

Provide feedback

---

SparkleColor

Read Parallel

Determines the color of the sparkle particles.

Sparkles.SparkleColor:[Color3](/docs/reference/engine/datatypes/Color3)

This property functions identically to [Sparkles.Color](/docs/reference/engine/classes/Sparkles#Color).

The SparkleColor property determines the color of all the particles emit
by a [Sparkles](/docs/reference/engine/classes/Sparkles) object (both existing and future particles). It
behaves similarly to [ParticleEmitter.Color](/docs/reference/engine/classes/ParticleEmitter#Color), except that it is only
one color and not a [ColorSequence](/docs/reference/engine/datatypes/ColorSequence). Sparkles have a natural
color sequence applied which is most apparent when this property is set to
white; sparkles very faintly animate between a subtle green and red.

It should be noted that sparkles have a partial
[ParticleEmitter.LightEmission](/docs/reference/engine/classes/ParticleEmitter#LightEmission) effect, so dark colors tend to
render more transparent and white colors look very bright.

Code Samples

Give Sparkles

The code sample below gives any new players sparkles that are colored the same
as their torso color.

```
local Players = game:GetService("Players")



local function onCharacterSpawned(character)



local hrp = character:WaitForChild("HumanoidRootPart")



-- Add sparkles that are colored to the player's torso color



local sparkles = Instance.new("Sparkles")



sparkles.Parent = hrp



sparkles.SparkleColor = character:WaitForChild("Body Colors").TorsoColor.Color



sparkles.Enabled = true



end



local function onPlayerAdded(player)



player.CharacterAdded:Connect(onCharacterSpawned)



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Provide feedback

---

TimeScale

Read Parallel

Sparkles.TimeScale:[number](/docs/luau/numbers)

Provide feedback

---