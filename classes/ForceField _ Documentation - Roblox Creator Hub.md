# ForceField | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ForceField
Scraped: 2026-01-11T02:39:54.257597Z

## Inherits
- Object
- Instance
- ForceField
- Humanoid
- Humanoid:TakeDamage()
- BaseParts
- Explosion
- SpawnLocation
- SpawnLocation.Duration
- Model
- BasePart
- Humanoids
- Humanoid.Health
- ForceField.Visible
- Humanoid.RigType
- BasePart.Position
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ForceField](/docs/reference/engine/classes/ForceField)

English

Feedback

Engine Class

![ForceField](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/ForceField-Dark.webp)ForceField

Protects a [Humanoid](/docs/reference/engine/classes/Humanoid) from taking damage dealt through the
[Humanoid:TakeDamage()](/docs/reference/engine/classes/Humanoid#TakeDamage) method and protects [BaseParts](/docs/reference/engine/classes/BasePart)
from having their joints broken due to an [Explosion](/docs/reference/engine/classes/Explosion).

---

Summary

Properties

|  |
| --- |
| [Visible](#Visible):[boolean](/docs/luau/booleans) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A ForceField protects a [Humanoid](/docs/reference/engine/classes/Humanoid) from taking damage dealt through
the [Humanoid:TakeDamage()](/docs/reference/engine/classes/Humanoid#TakeDamage) method and protects
[BaseParts](/docs/reference/engine/classes/BasePart) from having their joints broken due to an
[Explosion](/docs/reference/engine/classes/Explosion). A new ForceField is created when a character spawns on
a [SpawnLocation](/docs/reference/engine/classes/SpawnLocation) and the [SpawnLocation.Duration](/docs/reference/engine/classes/SpawnLocation#Duration) property is
greater than zero.

#### Damage and Joints

A ForceField influences the instance it's parented to. When parented to a
[Model](/docs/reference/engine/classes/Model), it protects all of the [BaseParts](/docs/reference/engine/classes/BasePart) descending
from that model. If parented to a [BasePart](/docs/reference/engine/classes/BasePart), the part's joints will
only be protected if both the part and the part it's connected to also contain
a ForceField.

ForceField only protects [Humanoids](/docs/reference/engine/classes/Humanoid) from damage dealt by
the [Humanoid:TakeDamage()](/docs/reference/engine/classes/Humanoid#TakeDamage) method. Humanoids can still be damaged by
setting [Humanoid.Health](/docs/reference/engine/classes/Humanoid#Health) directly. For this reason, it's advised that
you use [Humanoid:TakeDamage()](/docs/reference/engine/classes/Humanoid#TakeDamage) to assign damage while accounting for
force field protection.

#### Visualization

When [ForceField.Visible](/docs/reference/engine/classes/ForceField#Visible) is set to true, a particle effect is created.
A number of rules determine where this effect will be emitted from:

* When parented to a [Model](/docs/reference/engine/classes/Model), if the model includes a [Humanoid](/docs/reference/engine/classes/Humanoid)
  named Humanoid with [Humanoid.RigType](/docs/reference/engine/classes/Humanoid#RigType) set to R15, the effect will
  be emitted from the part named UpperTorso. Otherwise, the effect will be
  emitted from the part named Torso.
* When parented to a [BasePart](/docs/reference/engine/classes/BasePart) the effect will be emitted from the
  part's [BasePart.Position](/docs/reference/engine/classes/BasePart#Position).

Code Samples

ForceField Instantiation

This code sample includes a function that will give a Player a ForceField for
a specific duration.

```
local Players = game:GetService("Players")



local FORCE_FIELD_DURATION = 15



local function giveForcefield(player, duration)



local character = player.Character



if character then



local forceField = Instance.new("ForceField")



forceField.Visible = true



forceField.Parent = character



if duration then



task.delay(duration, function()



if forceField then



forceField:Destroy()



end



end)



end



end



end



local function onPlayerAdded(player)



player.CharacterAdded:Connect(function(_character)



giveForcefield(player, FORCE_FIELD_DURATION)



end)



end



Players.PlayerAdded(onPlayerAdded)
```

---

API Reference

Properties

Visible

Read Parallel

Determines whether or not the [ForceField](/docs/reference/engine/classes/ForceField) particle effect is
visible.

ForceField.Visible:[boolean](/docs/luau/booleans)

Determines whether or not the [ForceField](/docs/reference/engine/classes/ForceField) particle effect is
visible. Setting this to false lets you replace the default particle
effect with a custom effect as demonstrated in the following code sample.

Code Samples

Custom ForceField Effect

This sample includes a function that will replace the default ForceField
particle effect with an effect using ParticleEmitters that can be modified by
the developer.

```
local Players = game:GetService("Players")



local FORCE_FIELD_DURATION = 15



local function createCustomForcefield(player, duration)



local character = player.Character



if character then



local humanoid = character:FindFirstChild("Humanoid")



if humanoid then



-- find the torso



local torsoName = humanoid.RigType == Enum.HumanoidRigType.R15 and "UpperTorso" or "Torso"



local torso = character:FindFirstChild(torsoName)



if torso then



-- create a forcefield



local forceField = Instance.new("ForceField")



forceField.Visible = false -- not visible



-- create a particle effect



local particleEmitter = Instance.new("ParticleEmitter")



particleEmitter.Enabled = true



particleEmitter.Parent = torso



-- listen for the forcefield being removed



forceField.AncestryChanged:Connect(function(_child, parent)



if not parent then



if particleEmitter and particleEmitter.Parent then



particleEmitter:Destroy()



end



end



end)



-- parent the forcefield and set it to expire



forceField.Parent = character



if duration then



task.delay(duration, function()



if forceField then



forceField:Destroy()



end



end)



end



end



end



end



end



local function onPlayerAdded(player)



player.CharacterAdded:Connect(function(_character)



createCustomForcefield(player, FORCE_FIELD_DURATION)



end)



end



Players.PlayerAdded(onPlayerAdded)
```

Provide feedback

---