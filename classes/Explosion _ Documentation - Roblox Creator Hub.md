# Explosion | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Explosion
Scraped: 2026-01-11T02:41:39.762533Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- Explosion
- BaseParts
- Explosion.BlastRadius
- JointInstances
- WeldConstraints
- Humanoid
- ForceField
- BasePart
- BlastRadius
- Constraints
- Instance:Destroy()
- Workspace
- Humanoids
- Model
- DestroyJointRadiusPercent
- Hit
- Terrain
- ExplosionType
- Explosion.Position
- Explosion.DestroyJointRadiusPercent
- Explosion.ExplosionType
- Explosion.Hit
- Explosion.BlastPressure
- Explosions
- ParticleEmitter
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Explosion](/docs/reference/engine/classes/Explosion)

English

Feedback

Engine Class

![Explosion](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Explosion-Dark.webp)Explosion

Applies force to [BaseParts](/docs/reference/engine/classes/BasePart) within the explosion's
[Explosion.BlastRadius](/docs/reference/engine/classes/Explosion#BlastRadius). Breaks [JointInstances](/docs/reference/engine/classes/JointInstance) and
[WeldConstraints](/docs/reference/engine/classes/WeldConstraint) between parts and kills
[Humanoid](/docs/reference/engine/classes/Humanoid) characters not protected by a [ForceField](/docs/reference/engine/classes/ForceField).

---

Summary

Properties

|  |
| --- |
| [BlastPressure](#BlastPressure):[number](/docs/luau/numbers) |
| [BlastRadius](#BlastRadius):[number](/docs/luau/numbers) |
| [DestroyJointRadiusPercent](#DestroyJointRadiusPercent):[number](/docs/luau/numbers) |
| [ExplosionType](#ExplosionType):[Enum.ExplosionType](/docs/reference/engine/enums/ExplosionType) |
| [LocalTransparencyModifier](#LocalTransparencyModifier):[number](/docs/luau/numbers) |
| [Position](#Position):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [TimeScale](#TimeScale):[number](/docs/luau/numbers) |
| [Visible](#Visible):[boolean](/docs/luau/booleans) |

Events

|  |
| --- |
| [Hit](#Hit)(part: [BasePart](/docs/reference/engine/classes/BasePart),distance: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An Explosion applies force to [BaseParts](/docs/reference/engine/classes/BasePart) within the
explosion's [BlastRadius](/docs/reference/engine/classes/Explosion#BlastRadius). This force breaks
[JointInstances](/docs/reference/engine/classes/JointInstance) and
[WeldConstraints](/docs/reference/engine/classes/WeldConstraint) between parts and kills
[Humanoid](/docs/reference/engine/classes/Humanoid) characters not protected by a [ForceField](/docs/reference/engine/classes/ForceField).
[Constraints](/docs/reference/engine/classes/Constraint) will not be broken by an explosion.

If an [Explosion](/docs/reference/engine/classes/Explosion) is parented anywhere in the data model while the
experience is running, it immediately sets off and, within a few seconds, it
becomes unparented. It is not destroyed with [Instance:Destroy()](/docs/reference/engine/classes/Instance#Destroy) in
this case, so connections do not get disconnected and the parent is not
locked. As with all instances, keeping a strong reference an [Explosion](/docs/reference/engine/classes/Explosion)
will prevent it from being garbage collected.

Note that an [Explosion](/docs/reference/engine/classes/Explosion) must be a descendant of [Workspace](/docs/reference/engine/classes/Workspace) for
the explosion visuals to play and the physical/damaging effects to have an
impact.

#### Explosion Effects

[Humanoids](/docs/reference/engine/classes/Humanoid) are killed by explosions, as the explosion breaks
the character [Model](/docs/reference/engine/classes/Model) neck joint. Parenting a [ForceField](/docs/reference/engine/classes/ForceField) to a
model will protect all of its children from the explosion kill effect.

If you do not want joints between [BaseParts](/docs/reference/engine/classes/BasePart) to be broken, or
you want to implement your own formula for damaging
[Humanoids](/docs/reference/engine/classes/Humanoid), it's recommended that you set
[DestroyJointRadiusPercent](/docs/reference/engine/classes/Explosion#DestroyJointRadiusPercent) to 0 and
use the [Hit](/docs/reference/engine/classes/Explosion#Hit) event to handle the result of the explosion.

Explosions can also be configured to damage [Terrain](/docs/reference/engine/classes/Terrain), creating craters,
as configured through the [ExplosionType](/docs/reference/engine/classes/Explosion#ExplosionType)
property.

Note that the effect of an explosion is not disrupted by obstacles,
meaning that parts/terrain shielded behind other parts/terrain will still be
affected.

Code Samples

Explosion Instantiation

This code sample includes a brief snippet that creates a large explosion in
the game at 0, 10, 0.

```
local explosion = Instance.new("Explosion")



explosion.BlastRadius = 60



explosion.ExplosionType = Enum.ExplosionType.Craters -- damages terrain



explosion.Position = Vector3.new(0, 10, 0)



explosion.Parent = workspace
```

---

API Reference

Properties

BlastPressure

Read Parallel

Used to determine the amount of force applied to
[BaseParts](/docs/reference/engine/classes/BasePart) caught in the [Explosion.BlastRadius](/docs/reference/engine/classes/Explosion#BlastRadius).

Explosion.BlastPressure:[number](/docs/luau/numbers)

Used to determine the amount of force applied to
[BaseParts](/docs/reference/engine/classes/BasePart) caught in the [Explosion.BlastRadius](/docs/reference/engine/classes/Explosion#BlastRadius).

Currently this level of force applied does not vary based on distance from
[Explosion.Position](/docs/reference/engine/classes/Explosion#Position). Unanchored BaseParts will accelerate equally
away from the origin regardless of distance provided they are within the
blast radius.

The blast pressure determines the acceleration of parts due to an
explosion. It does not determine the degree to which joints are broken.
When [Explosion.DestroyJointRadiusPercent](/docs/reference/engine/classes/Explosion#DestroyJointRadiusPercent) is equal to 1 all joints
between parts in the [Explosion.BlastRadius](/docs/reference/engine/classes/Explosion#BlastRadius) will be destroyed
provided BlastPressure is greater than 0.

The BlastPressure also does not determine the amount of damage given to
[Terrain](/docs/reference/engine/classes/Terrain). Provided BlastPressure is greater than 0 and
[Explosion.ExplosionType](/docs/reference/engine/classes/Explosion#ExplosionType) isn't set to Enum.ExplosionType.NoCraters
the size of the crater created is determined exclusively by the
[Explosion.BlastRadius](/docs/reference/engine/classes/Explosion#BlastRadius).

Setting BlastPressure to 0 eliminates the effect of the explosion and is
useful when developers want to program their own custom behavior for
explosions using the [Explosion.Hit](/docs/reference/engine/classes/Explosion#Hit) event.

Code Samples

Custom Explosion

This sample contains a simple function that creates a custom explosion. The
custom explosion will not break joints as Explosion.DestroyJointRadiusPercent
is equal to 0. This means Humanoids will not be instantly killed as their neck
joints are broken. In this example explosion.BlastPressure is equal to zero so
as not to apply force or damage terrain but this can be changed.

The Explosion.Hit event is used to listen for contact. Once contact has been
made the code will look for the parent model of the BasePart hit by the
explosion. If that model exists, hasn't already been damaged and has a
Humanoid in it damage will be applied based on distance from the explosion's
origin.

```
local function customExplosion(position, radius, maxDamage)



local explosion = Instance.new("Explosion")



explosion.BlastPressure = 0 -- this could be set higher to still apply velocity to parts



explosion.DestroyJointRadiusPercent = 0 -- joints are safe



explosion.BlastRadius = radius



explosion.Position = position



-- set up a table to track the models hit



local modelsHit = {}



-- listen for contact



explosion.Hit:Connect(function(part, distance)



local parentModel = part.Parent



if parentModel then



-- check to see if this model has already been hit



if modelsHit[parentModel] then



return



end



-- log this model as hit



modelsHit[parentModel] = true



-- look for a humanoid



local humanoid = parentModel:FindFirstChild("Humanoid")



if humanoid then



local distanceFactor = distance / explosion.BlastRadius -- get the distance as a value between 0 and 1



distanceFactor = 1 - distanceFactor -- flip the amount, so that lower == closer == more damage



humanoid:TakeDamage(maxDamage * distanceFactor) -- TakeDamage to respect ForceFields



end



end



end)



explosion.Parent = game.Workspace



-- Roblox removes explosions after a few seconds, but does not destroy them.



-- To ensure our .Hit connection gets disconnected, destroy the explosion once it's removed.



explosion.AncestryChanged:Connect(function()



if not explosion.Parent then



explosion:Destroy()



end



end)



end



customExplosion(Vector3.new(0, 10, 0), 12, 50)
```

Provide feedback

---

BlastRadius

Read Parallel

This property determines the radius of the [Explosion](/docs/reference/engine/classes/Explosion), in studs.
This radius determines the area of effect of the explosion, not the size
of the explosion's visuals.

Explosion.BlastRadius:[number](/docs/luau/numbers)

This property determines the radius of the [Explosion](/docs/reference/engine/classes/Explosion), in studs.
This property accepts any value between 0 and 100.

This radius determines the area of effect of the Explosion, not the size
of the Explosion's visuals. The size of the Explosion's visual effect is
the same regardless of BlastRadius (even if BlastRadius is 0).

[BaseParts](/docs/reference/engine/classes/BasePart) within the BlastRadius will be affected by the
explosion. Meaning, if [Explosion.BlastPressure](/docs/reference/engine/classes/Explosion#BlastPressure) is greater than 0,
force will be applied to parts. The degree to which joints are broken
within the BlastRadius depends on
[Explosion.DestroyJointRadiusPercent](/docs/reference/engine/classes/Explosion#DestroyJointRadiusPercent). [Explosion.Hit](/docs/reference/engine/classes/Explosion#Hit) will
fire for any every [BasePart](/docs/reference/engine/classes/BasePart) within the radius.

[BaseParts](/docs/reference/engine/classes/BasePart) are considered within
[Explosion.BlastRadius](/docs/reference/engine/classes/Explosion#BlastRadius) even if they are only partially in range.

Code Samples

Explosion Instantiation

This code sample includes a brief snippet that creates a large explosion in
the game at 0, 10, 0.

```
local explosion = Instance.new("Explosion")



explosion.BlastRadius = 60



explosion.ExplosionType = Enum.ExplosionType.Craters -- damages terrain



explosion.Position = Vector3.new(0, 10, 0)



explosion.Parent = workspace
```

Provide feedback

---

DestroyJointRadiusPercent

Read Parallel

Used to set the proportion of the [Explosion.BlastRadius](/docs/reference/engine/classes/Explosion#BlastRadius), between 0
and 1, within which all joints will be destroyed. Anything outside of this
range will only have the [Explosion](/docs/reference/engine/classes/Explosion) force applied to it.

Explosion.DestroyJointRadiusPercent:[number](/docs/luau/numbers)

Used to set the proportion of the [Explosion.BlastRadius](/docs/reference/engine/classes/Explosion#BlastRadius), between 0
and 1, within which all joints will be destroyed. Anything outside of this
range will only have the [Explosion](/docs/reference/engine/classes/Explosion) force applied to it.

For example, if [Explosion.BlastRadius](/docs/reference/engine/classes/Explosion#BlastRadius) is set to 100 and
DestroyJointRadiusPercent is set to 0.5, any joints within a radius of 50
studs would be broken. Any joints between the ranges of 50 and 100 studs
wouldn't be destroyed, but the [Explosion](/docs/reference/engine/classes/Explosion) force would still be
applied to the [BaseParts](/docs/reference/engine/classes/BasePart).

This property allows developers to make [Explosions](/docs/reference/engine/classes/Explosion)
'non-lethal' to [Humanoids](/docs/reference/engine/classes/Humanoid) by setting
DestroyJointRadiusPercent to 0. This means the neck joint will not be
broken when characters come into contact with the [Explosion](/docs/reference/engine/classes/Explosion).

Code Samples

Non lethal explosions

This sample includes an example of how Explosions can be made non lethal to
player characters.

```
local function onDescendantAdded(instance)



if instance:IsA("Explosion") then



local explosion = instance



explosion.DestroyJointRadiusPercent = 0



local destroyJointRadiusPercent = 1



explosion.Hit:Connect(function(part, distance)



-- check the part is in range to break joints



if distance <= destroyJointRadiusPercent * explosion.BlastRadius then



-- make sure the part does not belong to a character



if not game.Players:GetPlayerFromCharacter(part.Parent) then



part:BreakJoints()



end



end



end)



end



end



workspace.DescendantAdded:Connect(onDescendantAdded)
```

Custom Explosion

This sample contains a simple function that creates a custom explosion. The
custom explosion will not break joints as Explosion.DestroyJointRadiusPercent
is equal to 0. This means Humanoids will not be instantly killed as their neck
joints are broken. In this example explosion.BlastPressure is equal to zero so
as not to apply force or damage terrain but this can be changed.

The Explosion.Hit event is used to listen for contact. Once contact has been
made the code will look for the parent model of the BasePart hit by the
explosion. If that model exists, hasn't already been damaged and has a
Humanoid in it damage will be applied based on distance from the explosion's
origin.

```
local function customExplosion(position, radius, maxDamage)



local explosion = Instance.new("Explosion")



explosion.BlastPressure = 0 -- this could be set higher to still apply velocity to parts



explosion.DestroyJointRadiusPercent = 0 -- joints are safe



explosion.BlastRadius = radius



explosion.Position = position



-- set up a table to track the models hit



local modelsHit = {}



-- listen for contact



explosion.Hit:Connect(function(part, distance)



local parentModel = part.Parent



if parentModel then



-- check to see if this model has already been hit



if modelsHit[parentModel] then



return



end



-- log this model as hit



modelsHit[parentModel] = true



-- look for a humanoid



local humanoid = parentModel:FindFirstChild("Humanoid")



if humanoid then



local distanceFactor = distance / explosion.BlastRadius -- get the distance as a value between 0 and 1



distanceFactor = 1 - distanceFactor -- flip the amount, so that lower == closer == more damage



humanoid:TakeDamage(maxDamage * distanceFactor) -- TakeDamage to respect ForceFields



end



end



end)



explosion.Parent = game.Workspace



-- Roblox removes explosions after a few seconds, but does not destroy them.



-- To ensure our .Hit connection gets disconnected, destroy the explosion once it's removed.



explosion.AncestryChanged:Connect(function()



if not explosion.Parent then



explosion:Destroy()



end



end)



end



customExplosion(Vector3.new(0, 10, 0), 12, 50)
```

Provide feedback

---

ExplosionType

Read Parallel

This property determines how the [Explosion](/docs/reference/engine/classes/Explosion) will interact with
[Terrain](/docs/reference/engine/classes/Terrain). Used to set if explosions will cause damage to the
terrain or not.

Explosion.ExplosionType:[Enum.ExplosionType](/docs/reference/engine/enums/ExplosionType)

This property determines how the [Explosion](/docs/reference/engine/classes/Explosion) will interact with
[Terrain](/docs/reference/engine/classes/Terrain). It is an Enum.ExplosionType value and can be set to one
of three options.

* NoCraters - Explosions will not damage Terrain
* Craters - Explosions will create craters in Terrain
* CratersAndDebris - Redundant, behaves the same as Craters

If ExplosionType is set to create craters in [Terrain](/docs/reference/engine/classes/Terrain), the radius
of the crater will be roughly equal to the [Explosion.BlastRadius](/docs/reference/engine/classes/Explosion#BlastRadius).
Craters are created in all [Terrain](/docs/reference/engine/classes/Terrain) materials other than water. The
size of the crater is not influenced by the material, although some
materials create rougher edges than others.

Code Samples

Stop Explosions from Damaging Terrain

This code sample includes an example of how the Explosion.ExplosionType
property can be used to stop Explosions from damaging terrain. It is
recommended to set the ExplosionType to NoCraters at the point of Explosion
instantiation, but if that is not practical the code below will work.

```
local function onDescendantAdded(instance)



if instance:IsA("Explosion") then



instance.ExplosionType = Enum.ExplosionType.NoCraters



instance:GetPropertyChangedSignal("ExplosionType"):Connect(function()



instance.ExplosionType = Enum.ExplosionType.NoCraters



end)



end



end



workspace.DescendantAdded:Connect(onDescendantAdded)
```

Provide feedback

---

LocalTransparencyModifier

Hidden

Not Replicated

Read Parallel

Explosion.LocalTransparencyModifier:[number](/docs/luau/numbers)

Provide feedback

---

Position

Read Parallel

This property is the position of the center of the [Explosion](/docs/reference/engine/classes/Explosion). It
is defined in world-space and not influenced by the [Explosion](/docs/reference/engine/classes/Explosion)
parent.

Explosion.Position:[Vector3](/docs/reference/engine/datatypes/Vector3)

This property is the position of the center of the [Explosion](/docs/reference/engine/classes/Explosion). It
is defined in world-space and not influenced by the [Explosion](/docs/reference/engine/classes/Explosion)
parent.

[BaseParts](/docs/reference/engine/classes/BasePart) will be influenced by the [Explosion](/docs/reference/engine/classes/Explosion) if
they are within [Explosion.BlastRadius](/docs/reference/engine/classes/Explosion#BlastRadius) studs of the explosion's
position.

The effect of an explosion is instantaneous. This means that although the
position of an explosion can be changed after it has been set it cannot
affect two different areas. Once an explosion has been 'detonated',
shortly after parenting it to a descendant of the [Workspace](/docs/reference/engine/classes/Workspace), it
will not do so again. In some cases the visual effect of the explosion
will move but it will have no effect.

For this reason a new Explosion should be created if the developer wants
an explosion to appear at a different position.

Code Samples

Explosion Instantiation

This code sample includes a brief snippet that creates a large explosion in
the game at 0, 10, 0.

```
local explosion = Instance.new("Explosion")



explosion.BlastRadius = 60



explosion.ExplosionType = Enum.ExplosionType.Craters -- damages terrain



explosion.Position = Vector3.new(0, 10, 0)



explosion.Parent = workspace
```

Provide feedback

---

TimeScale

Read Parallel

Value between 0 and 1 that controls the speed of the particle effect.

Explosion.TimeScale:[number](/docs/luau/numbers)

A value between 0 and 1 that controls the speed of the particle effect. At
1 it runs at normal speed, at 0.5 it runs at half speed, and at 0 it
freezes time.

Provide feedback

---

Visible

Read Parallel

This property determines whether or not the visual effect of an
[Explosion](/docs/reference/engine/classes/Explosion) is shown or not.

Explosion.Visible:[boolean](/docs/luau/booleans)

This property determines whether or not the visual effect of an
[Explosion](/docs/reference/engine/classes/Explosion) is shown or not.

When Visible is set to false, the explosion will still affect
[BaseParts](/docs/reference/engine/classes/BasePart) in its [Explosion.BlastRadius](/docs/reference/engine/classes/Explosion#BlastRadius), the only
difference is it will not be seen.

One use for this property would be for a developer to make their own
custom explosion effects using a [ParticleEmitter](/docs/reference/engine/classes/ParticleEmitter), while retaining
the default [Explosion](/docs/reference/engine/classes/Explosion) functionality.

Code Samples

Explosion Custom Visuals

This sample includes a function that will create an Explosion but replace the
default Explosion visuals but those of a ParticleEmitter.

```
local function customExplosion(position)



local explosion = Instance.new("Explosion")



explosion.Position = position



explosion.Visible = false



local attachment = Instance.new("Attachment")



attachment.Position = position



attachment.Parent = workspace.Terrain



local particleEmitter = Instance.new("ParticleEmitter")



particleEmitter.Enabled = false



particleEmitter.Parent = attachment



particleEmitter.Speed = NumberRange.new(5, 30)



particleEmitter.SpreadAngle = Vector2.new(-90, 90)



explosion.Parent = workspace



particleEmitter:Emit(20)



task.delay(5, function()



if attachment then



attachment:Destroy()



end



end)



end



customExplosion(Vector3.new(0, 10, 0))
```

Provide feedback

---

Events

Hit

Fires when the [Explosion](/docs/reference/engine/classes/Explosion) hits a [BasePart](/docs/reference/engine/classes/BasePart) within its
[Explosion.BlastRadius](/docs/reference/engine/classes/Explosion#BlastRadius). Returns the part hit along with the
distance of the part from [Explosion.Position](/docs/reference/engine/classes/Explosion#Position).

Explosion.Hit(

part:[BasePart](/docs/reference/engine/classes/BasePart), distance:[number](/docs/luau/numbers)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| part:[BasePart](/docs/reference/engine/classes/BasePart)  The [BasePart](/docs/reference/engine/classes/BasePart) hit by the [Explosion](/docs/reference/engine/classes/Explosion). |
| distance:[number](/docs/luau/numbers)  The distance of the hit from [Explosion.Position](/docs/reference/engine/classes/Explosion#Position). |

Fires when the [Explosion](/docs/reference/engine/classes/Explosion) hits a [BasePart](/docs/reference/engine/classes/BasePart) within its
[Explosion.BlastRadius](/docs/reference/engine/classes/Explosion#BlastRadius). Returns the part hit along with the
distance of the part from [Explosion.Position](/docs/reference/engine/classes/Explosion#Position).

Note that the effect of an [Explosion](/docs/reference/engine/classes/Explosion) is not disrupted by
obstacles, this means parts shielded behind other parts will still be hit,
even if the [BasePart](/docs/reference/engine/classes/BasePart) they are shielded behind is anchored.

This event will also fire when [Explosion.BlastPressure](/docs/reference/engine/classes/Explosion#BlastPressure) is equal to
zero. This means developers can program their own custom behavior for
explosions by eliminating the explosion's influence on
[BaseParts](/docs/reference/engine/classes/BasePart) and [Terrain](/docs/reference/engine/classes/Terrain).

Note that this event will fire for every [BasePart](/docs/reference/engine/classes/BasePart) hit. This means
it can fire multiple times for the same player character (as the character
[Model](/docs/reference/engine/classes/Model) is made up of multiple parts). For this reason when dealing
custom damage using the [Explosion.Hit](/docs/reference/engine/classes/Explosion#Hit) event it's recommended to
implement a check to see if the character has already been hit by the
[Explosion](/docs/reference/engine/classes/Explosion).

Code Samples

Custom Explosion

This sample contains a simple function that creates a custom explosion. The
custom explosion will not break joints as Explosion.DestroyJointRadiusPercent
is equal to 0. This means Humanoids will not be instantly killed as their neck
joints are broken. In this example explosion.BlastPressure is equal to zero so
as not to apply force or damage terrain but this can be changed.

The Explosion.Hit event is used to listen for contact. Once contact has been
made the code will look for the parent model of the BasePart hit by the
explosion. If that model exists, hasn't already been damaged and has a
Humanoid in it damage will be applied based on distance from the explosion's
origin.

```
local function customExplosion(position, radius, maxDamage)



local explosion = Instance.new("Explosion")



explosion.BlastPressure = 0 -- this could be set higher to still apply velocity to parts



explosion.DestroyJointRadiusPercent = 0 -- joints are safe



explosion.BlastRadius = radius



explosion.Position = position



-- set up a table to track the models hit



local modelsHit = {}



-- listen for contact



explosion.Hit:Connect(function(part, distance)



local parentModel = part.Parent



if parentModel then



-- check to see if this model has already been hit



if modelsHit[parentModel] then



return



end



-- log this model as hit



modelsHit[parentModel] = true



-- look for a humanoid



local humanoid = parentModel:FindFirstChild("Humanoid")



if humanoid then



local distanceFactor = distance / explosion.BlastRadius -- get the distance as a value between 0 and 1



distanceFactor = 1 - distanceFactor -- flip the amount, so that lower == closer == more damage



humanoid:TakeDamage(maxDamage * distanceFactor) -- TakeDamage to respect ForceFields



end



end



end)



explosion.Parent = game.Workspace



-- Roblox removes explosions after a few seconds, but does not destroy them.



-- To ensure our .Hit connection gets disconnected, destroy the explosion once it's removed.



explosion.AncestryChanged:Connect(function()



if not explosion.Parent then



explosion:Destroy()



end



end)



end



customExplosion(Vector3.new(0, 10, 0), 12, 50)
```

Provide feedback

---