# Model | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Model
Scraped: 2026-01-11T02:32:58.645632Z

## Tags
- Not Replicated

## Inherits
- PVInstance
- Model
- BaseParts
- BasePart
- Player
- Instance
- Object
- Actor
- BackpackItem
- Status
- WorldRoot
- Scripts
- Folder
- PrimaryPart
- Humanoid
- Part
- Workspace.FallenPartsDestroyHeight
- Workspace.StreamingEnabled
- ModelStreamingMode
- LevelOfDetail
- LocalScript
- WaitForChild()
- Models
- LocalScripts
- Model.PrimaryPart
- WeldConstraints
- Motor6Ds
- Anchored
- Model:ScaleTo()
- Script
- Model:GetScale()
- WorldPivot
- Model.WorldPivot
- PVInstance:PivotTo()
- Model:MoveTo()
- Terrain:FillBlock()
- LocalPlayer
- ScaleTo(x)
- ScaleTo(1)
- Animations
- AnimationController
- Model:PivotTo()
- MoveTo()
- Terrain
- TranslateBy()
- RopeConstraint
- HingeConstraint
- Sound.RollOffMinDistance
- Model:TranslateBy()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [PVInstance](/docs/reference/engine/classes/PVInstance)
6. /
7. [Model](/docs/reference/engine/classes/Model)

English

Feedback

Engine Class

![Model](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Model-Dark.webp)Model

Models are container objects, meaning they group objects together. They are
best used to hold collections of [BaseParts](/docs/reference/engine/classes/BasePart) and have a number
of functions that extend their functionality.

---

Summary

Properties

|  |
| --- |
| [LevelOfDetail](#LevelOfDetail):[Enum.ModelLevelOfDetail](/docs/reference/engine/enums/ModelLevelOfDetail) |
| [ModelStreamingMode](#ModelStreamingMode):[Enum.ModelStreamingMode](/docs/reference/engine/enums/ModelStreamingMode) |
| [PrimaryPart](#PrimaryPart):[BasePart](/docs/reference/engine/classes/BasePart) |
| [Scale](#Scale):[number](/docs/luau/numbers) |
| [WorldPivot](#WorldPivot):[CFrame](/docs/reference/engine/datatypes/CFrame) |

Methods

|  |
| --- |
| [AddPersistentPlayer](#AddPersistentPlayer)(playerInstance: [Player](/docs/reference/engine/classes/Player)):() |
| [BreakJoints](#BreakJoints)():()  Deprecated |
| [breakJoints](#breakJoints)():()  Deprecated |
| [GetBoundingBox](#GetBoundingBox)():[Tuple](/docs/luau/tuples) |
| [GetExtentsSize](#GetExtentsSize)():[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [GetModelCFrame](#GetModelCFrame)():[CFrame](/docs/reference/engine/datatypes/CFrame)  Deprecated |
| [GetModelSize](#GetModelSize)():[Vector3](/docs/reference/engine/datatypes/Vector3)  Deprecated |
| [GetPersistentPlayers](#GetPersistentPlayers)():Instances |
| [GetPrimaryPartCFrame](#GetPrimaryPartCFrame)():[CFrame](/docs/reference/engine/datatypes/CFrame)  Deprecated |
| [GetScale](#GetScale)():[number](/docs/luau/numbers) |
| [MakeJoints](#MakeJoints)():()  Deprecated |
| [makeJoints](#makeJoints)():()  Deprecated |
| [move](#move)(location: [Vector3](/docs/reference/engine/datatypes/Vector3)):()  Deprecated |
| [MoveTo](#MoveTo)(position: [Vector3](/docs/reference/engine/datatypes/Vector3)):() |
| [moveTo](#moveTo)(location: [Vector3](/docs/reference/engine/datatypes/Vector3)):()  Deprecated |
| [RemovePersistentPlayer](#RemovePersistentPlayer)(playerInstance: [Player](/docs/reference/engine/classes/Player)):() |
| [ResetOrientationToIdentity](#ResetOrientationToIdentity)():()  Deprecated |
| [ScaleTo](#ScaleTo)(newScaleFactor: [number](/docs/luau/numbers)):() |
| [SetIdentityOrientation](#SetIdentityOrientation)():()  Deprecated |
| [SetPrimaryPartCFrame](#SetPrimaryPartCFrame)(cframe: [CFrame](/docs/reference/engine/datatypes/CFrame)):()  Deprecated |
| [TranslateBy](#TranslateBy)(delta: [Vector3](/docs/reference/engine/datatypes/Vector3)):() |

Inherited Members

4 inherited from [PVInstance](/docs/reference/engine/classes/PVInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[Actor](/docs/reference/engine/classes/Actor), [BackpackItem](/docs/reference/engine/classes/BackpackItem), [Status](/docs/reference/engine/classes/Status), [WorldRoot](/docs/reference/engine/classes/WorldRoot)

Models are container objects, meaning they group objects together. They are
best used to hold collections of [BaseParts](/docs/reference/engine/classes/BasePart) and have a number
of functions that extend their functionality.

Models are intended to represent geometric groupings. If your grouping has
no geometric interpretation, for instance a collection of
[Scripts](/docs/reference/engine/classes/Script), use a [Folder](/docs/reference/engine/classes/Folder) instead.

Models whose constituent parts are joined together with joints (so that they
can move around or be destroyed via physics simulation) usually have a
[PrimaryPart](/docs/reference/engine/classes/Model#PrimaryPart) set, as it specifies which part within
the model the pivot and bounding box will "follow" as the model moves. Static
models which stay in one place do not benefit from having a primary part set.

Models have a wide range of applications, including Roblox player characters.
They also have a number of unique behaviors that are important to keep in
mind:

* When a [Humanoid](/docs/reference/engine/classes/Humanoid) and a [Part](/docs/reference/engine/classes/Part) named Head are parented under
  a model, a name/health GUI will appear over the model; see
  [Character Name/Health Display](/docs/characters/name-health-display)
  for details.
* If a part's position on the Y axis hits the
  [Workspace.FallenPartsDestroyHeight](/docs/reference/engine/classes/Workspace#FallenPartsDestroyHeight) value, and it was the last object
  inside of a [Model](/docs/reference/engine/classes/Model), the model will be destroyed as well.
* When used in a place with [Workspace.StreamingEnabled](/docs/reference/engine/classes/Workspace#StreamingEnabled) set to true,
  the value of [ModelStreamingMode](/docs/reference/engine/classes/Model#ModelStreamingMode) controls
  various behaviors around how the model and any descendants are replicated
  and/or removed from clients. In addition, the value of
  [LevelOfDetail](/docs/reference/engine/classes/Model#LevelOfDetail) impacts rendering of the model.

As with all [Instance](/docs/reference/engine/classes/Instance) types, the fact that a parent [Model](/docs/reference/engine/classes/Model) is
replicated to a client does not guarantee that all its children are
replicated. This is particularly important if these instances are being
accessed by code running on the client, such as in a [LocalScript](/docs/reference/engine/classes/LocalScript).
Using [ModelStreamingMode](/docs/reference/engine/classes/Model#ModelStreamingMode) with values such as
[Atomic](/docs/reference/engine/enums/ModelStreamingMode) can ensure that the entire model and all of
its descendants are present if the parent model exists on the client, or you
can use [WaitForChild()](/docs/reference/engine/classes/Instance#WaitForChild) when atomicity is not
desired.

Code Samples

Basic Model Instantiation

The following sample includes a basic function that takes a table of objects
and parents them into a new Model, returning that Model.

```
local function groupObjects(objectTable)



local model = Instance.new("Model")



for _, object in pairs(objectTable) do



object.Parent = model



end



return model



end



local objects = {



Instance.new("Part"),



Instance.new("Part"),



}



groupObjects(objects)
```

---

API Reference

Properties

LevelOfDetail

Plugin Security

Read Parallel

Sets the level of detail on the model for experiences with instance
streaming enabled.

Model.LevelOfDetail:[Enum.ModelLevelOfDetail](/docs/reference/engine/enums/ModelLevelOfDetail)

Sets the level of detail on the model for experiences with instance
[streaming](/docs/workspace/streaming) enabled.

When set to [StreamingMesh](/docs/reference/engine/enums/ModelLevelOfDetail), a lower resolution
"imposter" mesh (colored, coarse mesh that wraps around all child parts of
the model) renders outside the streaming radius.

When set to [SLIM](/docs/reference/engine/enums/ModelLevelOfDetail), a Scalable Lightweight
Interactive Model, or SLIM, model (a composite of all child parts of the
model) renders at progressively lower resolutions at distances based on
the streaming radius. This greatly improves visual quality over
[StreamingMesh](/docs/reference/engine/enums/ModelLevelOfDetail).

When set to [Disabled](/docs/reference/engine/enums/ModelLevelOfDetail) or
[Automatic](/docs/reference/engine/enums/ModelLevelOfDetail), lower resolution meshes will not be
displayed.

Provide feedback

---

ModelStreamingMode

Read Parallel

Controls the model streaming behavior on [Models](/docs/reference/engine/classes/Model) when
instance streaming is enabled.

Model.ModelStreamingMode:[Enum.ModelStreamingMode](/docs/reference/engine/enums/ModelStreamingMode)

Controls how [Models](/docs/reference/engine/classes/Model) are streamed in and out when instance
[streaming](/docs/workspace/streaming) is enabled. Behavior depends
on the selected enum. Has no effect when streaming is not enabled.

This property should only be changed in Studio via the
[Properties](/docs/studio/properties) window when streaming is
enabled, or in [Scripts](/docs/reference/engine/classes/Script), but never in
[LocalScripts](/docs/reference/engine/classes/LocalScript) (doing so can result in undefined
behavior).

Provide feedback

---

PrimaryPart

Read Parallel

The primary part of the [Model](/docs/reference/engine/classes/Model), or nil if not explicitly set.

Model.PrimaryPart:[BasePart](/docs/reference/engine/classes/BasePart)

Points to the primary part of the [Model](/docs/reference/engine/classes/Model). The primary part is the
[BasePart](/docs/reference/engine/classes/BasePart) that acts as the physical reference for the pivot of the
model. That is, when parts within the model are moved due to physical
simulation or other means, the pivot will move in sync with the primary
part.

Note that [Models](/docs/reference/engine/classes/Model) do not have PrimaryPart set by default.
If you are creating a model that needs to be acted upon by physics, you
should manually set this property in Studio or within a script. If the
primary part is not set, the pivot will remain at the same location in
world space, even if parts within the model are moved.

Also note that when setting this property, it must be a [BasePart](/docs/reference/engine/classes/BasePart)
that is a descendant of the model. If you try to set
[Model.PrimaryPart](/docs/reference/engine/classes/Model#PrimaryPart) to a [BasePart](/docs/reference/engine/classes/BasePart) that is not a
descendant of the model, it will be set to that part but reset to nil
during the next simulation step — this is legacy behavior to support
scripts which assume they can temporarily set the primary part to a
[BasePart](/docs/reference/engine/classes/BasePart) which isn't a descendant of the model.

The general rule for models is that:

* Models whose parts are joined together via physical joints such as
  [WeldConstraints](/docs/reference/engine/classes/WeldConstraint) or [Motor6Ds](/docs/reference/engine/classes/Motor6D)
  should have a primary part assigned. For example, Roblox character
  models have their [Model.PrimaryPart](/docs/reference/engine/classes/Model#PrimaryPart) set to the
  HumanoidRootPart by default.
* Static (usually [Anchored](/docs/reference/engine/classes/BasePart#Anchored)) models which stay in
  one place unless a script explicitly moves them don't require a
  [Model.PrimaryPart](/docs/reference/engine/classes/Model#PrimaryPart) and tend not to benefit from having one set.

Code Samples

Throwing Dice

This code sample creates and throws a dice model, then outputs whether it
landed with the blue side facing up. If [Model.PrimaryPart](/docs/reference/engine/classes/Model#PrimaryPart) was not set,
the pivot / bounding box of the dice would rotate, as the parts inside of it
are physically simulated during the roll.

```
-- Create a dice model with two halves and attach them together



local diceModel = Instance.new("Model")



diceModel.Name = "ChanceCube"



local diceTop = Instance.new("Part")



diceTop.Size = Vector3.new(4, 2, 4)



diceTop.Position = Vector3.new(0, 1, 0)



diceTop.Color = Color3.new(0, 0, 1)



diceTop.Parent = diceModel



local diceBottom = diceTop:Clone()



diceBottom.Position = Vector3.new(0, -1, 0)



diceBottom.Color = Color3.new(1, 0, 0)



diceBottom.Parent = diceModel



local weld = Instance.new("WeldConstraint")



weld.Part0 = diceTop



weld.Part1 = diceBottom



weld.Parent = diceModel



-- Put the dice up in the air above the workspace origin (does not require a primary part)



diceModel.Parent = workspace



diceModel:PivotTo(CFrame.new(0, 10, 0))



-- Assign the primary part before physical simulation



-- Without this line, the script will always output the same thing and the bounding box of the model will not change orientation



diceModel.PrimaryPart = diceTop



-- Wait a bit before rolling the dice (let it settle onto the floor)



for i = 5, 1, -1 do



print("Rolling dice in...", i)



task.wait(1)



end



diceTop:ApplyAngularImpulse(Vector3.new(15000, 1000, 5000))



diceTop:ApplyImpulse(Vector3.new(0, 3000, 0))



task.wait(1)



-- Wait for the roll to complete



while diceTop.AssemblyLinearVelocity.Magnitude > 0.1 or diceTop.AssemblyAngularVelocity.Magnitude > 0.1 do



task.wait()



end



-- Get the dice orientation, impacted by the primary part



local orientation = diceModel:GetBoundingBox()



if orientation.YVector.Y > 0.5 then



print("It's the boy!")



else



print("It's his mother!")



end
```

Provide feedback

---

Scale

Not Replicated

Not Scriptable

Read Parallel

Editor-only property used to scale the model around its pivot. Setting
this property will move the scale as though [Model:ScaleTo()](/docs/reference/engine/classes/Model#ScaleTo) was
called on it.

Model.Scale:[number](/docs/luau/numbers)

Setting this property in the Properties window will scale the model as
though [Model:ScaleTo()](/docs/reference/engine/classes/Model#ScaleTo) was called on it, scaling all descendant
Instances in the model, such as materials, images, and the 3D geometry of
parts, so that the model has the specified scale factor relative to its
original size.

This property is only available in Studio and will throw an error if used
in a [Script](/docs/reference/engine/classes/Script) or [LocalScript](/docs/reference/engine/classes/LocalScript). [Model:ScaleTo()](/docs/reference/engine/classes/Model#ScaleTo) and
[Model:GetScale()](/docs/reference/engine/classes/Model#GetScale) should be used from scripts.

Provide feedback

---

WorldPivot

Not Replicated

Read Parallel

Determines where the pivot of a [Model](/docs/reference/engine/classes/Model) which does not have a
set [Model.PrimaryPart](/docs/reference/engine/classes/Model#PrimaryPart) is located.

Model.WorldPivot:[CFrame](/docs/reference/engine/datatypes/CFrame)

This property determines where the pivot of a [Model](/docs/reference/engine/classes/Model) which does
not have a set [Model.PrimaryPart](/docs/reference/engine/classes/Model#PrimaryPart) is located. If the
[Model](/docs/reference/engine/classes/Model) does have a [PrimaryPart](/docs/reference/engine/classes/Model#PrimaryPart), the
pivot of the [Model](/docs/reference/engine/classes/Model) is equal to the pivot of that primary part
instead, and this [WorldPivot](/docs/reference/engine/classes/Model#WorldPivot) property is ignored.

For a newly created [Model](/docs/reference/engine/classes/Model), its pivot will be treated as the center
of the bounding box of its contents until the first time its
[Model.WorldPivot](/docs/reference/engine/classes/Model#WorldPivot) property is set. Once the world pivot is set for
the first time, it is impossible to restore this initial behavior.

Most commonly, moving the model with the Studio tools, or with model
movement functions such as [PVInstance:PivotTo()](/docs/reference/engine/classes/PVInstance#PivotTo) and
[Model:MoveTo()](/docs/reference/engine/classes/Model#MoveTo), will set the world pivot and thus end this new
model behavior.

The purpose of this behavior is to allow Luau code to get a sensible pivot
simply by creating a new model and parenting objects to it, avoiding the
need to explicitly set [Model.WorldPivot](/docs/reference/engine/classes/Model#WorldPivot) every time you create a
model in code.

```
local Workspace = game:GetService("Workspace")



local model = Instance.new("Model")



Workspace.BluePart.Parent = model



Workspace.RedPart.Parent = model



model.Parent = Workspace



print(model:GetPivot())  -- Currently equal to the center of the bounding box containing "BluePart" and "RedPart"



model:PivotTo(CFrame.new(0, 10, 0))  -- This works without needing to explicitly set "model.WorldPivot"
```

Code Samples

Reset Pivot

This code sample shows a custom function for resetting the pivot of a model
back to the center of that model's bounding box.

```
local function resetPivot(model)



local boundsCFrame = model:GetBoundingBox()



if model.PrimaryPart then



model.PrimaryPart.PivotOffset = model.PrimaryPart.CFrame:ToObjectSpace(boundsCFrame)



else



model.WorldPivot = boundsCFrame



end



end



resetPivot(script.Parent)
```

Provide feedback

---

Methods

AddPersistentPlayer

Sets this model to be persistent for the specified player.
[ModelStreamingMode](/docs/reference/engine/classes/Model#ModelStreamingMode) must be set to
[PersistentPerPlayer](/docs/reference/engine/enums/ModelStreamingMode) for behavior to be changed
as a result of addition.

Model:AddPersistentPlayer(playerInstance:[Player](/docs/reference/engine/classes/Player)):()

Parameters

|  |
| --- |
| playerInstance:[Player](/docs/reference/engine/classes/Player) Default Value: "nil" The [Player](/docs/reference/engine/classes/Player) to make this model persistent for. |

Returns

()

Sets this model to be persistent for the specified player. Persistent
models stay present for the player regardless of streaming settings or
conditions.

[ModelStreamingMode](/docs/reference/engine/classes/Model#ModelStreamingMode) must be set to
[PersistentPerPlayer](/docs/reference/engine/enums/ModelStreamingMode) for behavior to be changed
as a result of addition.

Provide feedback

---

BreakJoints

Deprecated

Show details

---

breakJoints

Deprecated

Show details

---

GetBoundingBox

Returns a description of a volume that contains all parts of a Model.

Model:GetBoundingBox():[Tuple](/docs/luau/tuples)

Returns

[Tuple](/docs/luau/tuples)

A [CFrame](/docs/reference/engine/datatypes/CFrame) representing the orientation of the volume
followed by a [Vector3](/docs/reference/engine/datatypes/Vector3) representing the size of the volume.

This function returns a description of a volume that contains all
[BasePart](/docs/reference/engine/classes/BasePart) children within a [Model](/docs/reference/engine/classes/Model). The volume's orientation
is based on the orientation of the [PrimaryPart](/docs/reference/engine/classes/Model#PrimaryPart),
and matches the selection box rendered in Studio when the model is
selected. Mirroring the behavior of [Terrain:FillBlock()](/docs/reference/engine/classes/Terrain#FillBlock), it
returns a [CFrame](/docs/reference/engine/datatypes/CFrame) representing the center of that bounding box
and a [Vector3](/docs/reference/engine/datatypes/Vector3) representing its size. The size may be inaccurate
at runtime if physics constraints are acting upon the parts within the
[Model](/docs/reference/engine/classes/Model).

If there is no [PrimaryPart](/docs/reference/engine/classes/Model#PrimaryPart) for the model, the
bounding box will be aligned to the world axes.

```
local Workspace = game:GetService("Workspace")



local model = Workspace.Model



local part = Workspace.Part



local orientation, size = model:GetBoundingBox()



-- Resize and position part equal to bounding box of model



part.Size = size



part.CFrame = orientation
```

Provide feedback

---

GetExtentsSize

Returns the size of the smallest bounding box that contains all of the
[BaseParts](/docs/reference/engine/classes/BasePart) in the [Model](/docs/reference/engine/classes/Model), aligned with the
[Model.PrimaryPart](/docs/reference/engine/classes/Model#PrimaryPart) if it is set.

Model:GetExtentsSize():[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

The [Vector3](/docs/reference/engine/datatypes/Vector3) extents size of the [Model](/docs/reference/engine/classes/Model).

Returns the size of the smallest bounding box that contains all of the
[BaseParts](/docs/reference/engine/classes/BasePart) in the [Model](/docs/reference/engine/classes/Model). If
[Model.PrimaryPart](/docs/reference/engine/classes/Model#PrimaryPart) exists then the bounding box will be aligned to
that part. If a primary part has not been set then the function will chose
a part in the model to align the bounding box to. As the selection of this
part is not deterministic it is recommended to set a
[Model.PrimaryPart](/docs/reference/engine/classes/Model#PrimaryPart) to get consistent results with this function.

Note this function only returns the size of the smallest bounding box, and
the developer must employ their own method to obtain the position of the
bounding box.

Code Samples

Model GetExtentsSize

The code sample below demonstrates how Model.GetExtentsSize can be used to get
the size of the bounding box containing the parts.

```
local model = Instance.new("Model")



model.Parent = workspace



local RNG = Random.new()



for _ = 1, 5 do



local part = Instance.new("Part")



part.Anchored = true



part.Size = Vector3.new(RNG:NextNumber(0.05, 5), RNG:NextNumber(0.05, 5), RNG:NextNumber(0.05, 5))



part.Parent = model



end



print(model:GetExtentsSize())
```

Provide feedback

---

GetModelCFrame

Deprecated

Show details

---

GetModelSize

Deprecated

Show details

---

GetPersistentPlayers

Returns all the [Player](/docs/reference/engine/classes/Player) objects that this model object is
persistent for. Behavior varies based on whether this method is called
from a [Script](/docs/reference/engine/classes/Script) or a [LocalScript](/docs/reference/engine/classes/LocalScript).

Model:GetPersistentPlayers():Instances

Returns

Instances

A table with all the [Player](/docs/reference/engine/classes/Player) objects that this model object is
persistent for.

When this method is called from a [Script](/docs/reference/engine/classes/Script), it returns all the
[Player](/docs/reference/engine/classes/Player) objects that this model is persistent for. When called from
a [LocalScript](/docs/reference/engine/classes/LocalScript), this method only checks if this model is persistent
for the [LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer).

Provide feedback

---

GetPrimaryPartCFrame

Deprecated

Show details

---

GetScale

Returns the canonical scale of the model, which defaults to 1 for newly
created models and will change as it is scaled via
[Model:ScaleTo()](/docs/reference/engine/classes/Model#ScaleTo).

Model:GetScale():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

The current canonical scale factor of the model.

Models contain a persistent canonical scale factor, which starts out at 1
for newly created models and changes as the model is scaled by calling
[Model:ScaleTo()](/docs/reference/engine/classes/Model#ScaleTo). This function returns the current canonical scale
factor of the model.

The current scale factor does not *directly* impact the size of Instances
under the model. It is used for content authoring and scripting purposes
to remember how the model has been scaled relative to its original size.

Within a given session, the model will cache the precise original size
information of the descendant Instances after the first
[Model:ScaleTo()](/docs/reference/engine/classes/Model#ScaleTo) call. This means that calling
[ScaleTo(x)](/docs/reference/engine/classes/Model#ScaleTo) followed by
[ScaleTo(1)](/docs/reference/engine/classes/Model#ScaleTo) will get you back *exactly* the
original configuration of the model with no floating point drift. Avoiding
floating point drift is the motivation for having a ScaleTo function
instead of a ScaleBy function.

The scale factor does impact engine behavior in one way: The scale factor
of a model will be applied to joint offsets of
[Animations](/docs/reference/engine/classes/Animation) played on an [AnimationController](/docs/reference/engine/classes/AnimationController)
under that model, so that animated rigs will correctly play back
animations even when scaled.

Code Samples

Substituting in a replacement model using PivotTo and ScaleTo

This code sample demonstrates substituting in a replacement for all the copies of a tree model using [Model:PivotTo()](/docs/reference/engine/classes/Model#PivotTo) and [Model:ScaleTo()](/docs/reference/engine/classes/Model#ScaleTo). The pivot and scale of the models are used as a reference ensuring that the relative sizes and locations of the replacement models match those of the originals.

```
local CollectionService = game:GetService("CollectionService")



local ReplicatedStorage = game:GetService("ReplicatedStorage")



-- Find all the models with the tag we want to replace



local items = CollectionService:GetTagged("Tree")



local newModel = ReplicatedStorage.FancyTreeReplacementModel



for _, item in items do



-- Make the new item and scale / position it where the old one was



local newItem = newModel:Clone()



newItem:ScaleTo(item:GetScale())



newItem:PivotTo(item:GetPivot())



-- Add the same tag to the replacement



CollectionService:AddTag(newItem, "Tree")



-- Delete the old item and parent the new one



newItem.Parent = item.Parent



item:Destroy()



end
```

Provide feedback

---

MakeJoints

Deprecated

Show details

---

makeJoints

Deprecated

Show details

---

move

Deprecated

Show details

---

MoveTo

Moves the [PrimaryPart](/docs/reference/engine/classes/Model#PrimaryPart) to the given position. If
a primary part has not been specified, the root part of the model will be
used.

Model:MoveTo(position:[Vector3](/docs/reference/engine/datatypes/Vector3)):()

Parameters

|  |
| --- |
| position:[Vector3](/docs/reference/engine/datatypes/Vector3)  The [Vector3](/docs/reference/engine/datatypes/Vector3) the [Model](/docs/reference/engine/classes/Model) is moved to. |

Returns

()

Moves the [PrimaryPart](/docs/reference/engine/classes/Model#PrimaryPart) to the given position. If
a primary part has not been specified, the root part of the model will be
used, but the root part is not deterministic and it is recommended that
you always set a primary part when using [MoveTo()](/docs/reference/engine/classes/Model#MoveTo).

If there are any obstructions where the model is to be moved, such as
[Terrain](/docs/reference/engine/classes/Terrain) or other [BaseParts](/docs/reference/engine/classes/BasePart), the model will be
moved vertically upward until there is nothing in the way. If this
behavior is not desired, [PVInstance:PivotTo()](/docs/reference/engine/classes/PVInstance#PivotTo) should be used
instead.

Note that rotation is not preserved when moving a model with
[MoveTo()](/docs/reference/engine/classes/Model#MoveTo). It is recommended to use either
[TranslateBy()](/docs/reference/engine/classes/Model#TranslateBy) or [PVInstance:PivotTo()](/docs/reference/engine/classes/PVInstance#PivotTo)
if the current rotation of the model needs to be preserved.

Code Samples

Model MoveTo

This sample demonstrates how [Model:MoveTo()](/docs/reference/engine/classes/Model#MoveTo) avoids collisions.

A simple two part [Model](/docs/reference/engine/classes/Model) is created, and its [Model.PrimaryPart](/docs/reference/engine/classes/Model#PrimaryPart) is set. An large
obstruction part is placed next to it.

After 5 seconds [Model:MoveTo()](/docs/reference/engine/classes/Model#MoveTo) is used to direct the model to move inside the
obstruction part. However, as MoveTo will not move a model inside of an
obstruction the [Model](/docs/reference/engine/classes/Model) is moved up on the Y axis and placed above the
obstruction.

```
local START_POSITION = Vector3.new(-20, 10, 0)



local END_POSITION = Vector3.new(0, 10, 0)



local model = Instance.new("Model")



model.Parent = workspace



local part1 = Instance.new("Part")



part1.Size = Vector3.new(4, 4, 4)



part1.Position = START_POSITION



part1.Anchored = true



part1.BrickColor = BrickColor.new("Bright yellow")



part1.Parent = model



local part2 = Instance.new("Part")



part2.Size = Vector3.new(2, 2, 2)



part2.Position = START_POSITION + Vector3.new(0, 3, 0)



part2.Anchored = true



part2.BrickColor = BrickColor.new("Bright blue")



part2.Parent = model



model.PrimaryPart = part1



model.Parent = workspace



local obstruction = Instance.new("Part")



obstruction.Name = "Obstruction"



obstruction.Size = Vector3.new(10, 10, 10)



obstruction.Position = Vector3.new(0, 10, 0)



obstruction.Anchored = true



obstruction.BrickColor = BrickColor.new("Bright green")



obstruction.Parent = workspace



task.wait(3)



model:MoveTo(END_POSITION)
```

Provide feedback

---

moveTo

Deprecated

Show details

---

RemovePersistentPlayer

Makes this model no longer persistent for the specified player.
[ModelStreamingMode](/docs/reference/engine/classes/Model#ModelStreamingMode) must be set to
[PersistentPerPlayer](/docs/reference/engine/enums/ModelStreamingMode) for behavior to be changed
as a result of removal.

Model:RemovePersistentPlayer(playerInstance:[Player](/docs/reference/engine/classes/Player)):()

Parameters

|  |
| --- |
| playerInstance:[Player](/docs/reference/engine/classes/Player) Default Value: "nil" The [Player](/docs/reference/engine/classes/Player) to make this model no longer persistent for. |

Returns

()

Makes this model no longer persistent for the specified player. This does
not guarantee the model will immediately be removed for the player; after
calling this method, the model will be treated as
[Atomic](/docs/reference/engine/enums/ModelStreamingMode) for that player and will remain present
as long as it is within the target streaming radius.

[ModelStreamingMode](/docs/reference/engine/classes/Model#ModelStreamingMode) must be set to
[PersistentPerPlayer](/docs/reference/engine/enums/ModelStreamingMode) for behavior to be changed
as a result of removal.

Provide feedback

---

ResetOrientationToIdentity

Deprecated

Show details

---

ScaleTo

Sets the scale factor of the model, adjusting the sizing and location of
all descendant Instances such that they have that scale factor relative to
their initial sizes and locations when scale factor was 1.

Model:ScaleTo(newScaleFactor:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| newScaleFactor:[number](/docs/luau/numbers) |

Returns

()

Models contain a persistent canonical scale factor, which starts out at 1
for newly created models. This function scales the model, around the pivot
location, relative to how it would look at a scale factor of 1. To
accomplish this it does two things:

* Sets the current scale factor of the model to the specified value
* Resizes and repositions all descendant Instances accordingly

The scaling of locations is done around the pivot location.

All "geometric" properties of descendant Instances will be scaled. That
obviously includes the sizes of parts, but here are some other examples of
properties which are scaled:

* The length of joints like [WeldConstraints](/docs/reference/engine/classes/WeldConstraint), and
  [RopeConstraint](/docs/reference/engine/classes/RopeConstraint)
* Physical velocities and forces like [HingeConstraint](/docs/reference/engine/classes/HingeConstraint)
* Visual properties like sizes of particle emitters
* Other length properties like [Sound.RollOffMinDistance](/docs/reference/engine/classes/Sound#RollOffMinDistance)

Provide feedback

---

SetIdentityOrientation

Deprecated

Show details

---

SetPrimaryPartCFrame

Deprecated

Show details

---

TranslateBy

Shifts a [Model](/docs/reference/engine/classes/Model) by the given [Vector3](/docs/reference/engine/datatypes/Vector3) offset, preserving
the model's orientation. If another [BasePart](/docs/reference/engine/classes/BasePart) or [Terrain](/docs/reference/engine/classes/Terrain)
already exists at the new position then the [Model](/docs/reference/engine/classes/Model) will overlap
said object.

Model:TranslateBy(delta:[Vector3](/docs/reference/engine/datatypes/Vector3)):()

Parameters

|  |
| --- |
| delta:[Vector3](/docs/reference/engine/datatypes/Vector3)  The [Vector3](/docs/reference/engine/datatypes/Vector3) to translate the [Model](/docs/reference/engine/classes/Model) by. |

Returns

()

Shifts a [Model](/docs/reference/engine/classes/Model) by the given [Vector3](/docs/reference/engine/datatypes/Vector3) offset, preserving
the model's orientation. If another [BasePart](/docs/reference/engine/classes/BasePart) or [Terrain](/docs/reference/engine/classes/Terrain)
already exists at the new position then the [Model](/docs/reference/engine/classes/Model) will overlap
said object.

The translation is applied in world space rather than object space,
meaning even if the model's parts are orientated differently it will still
move along the standard axis.

Code Samples

Model TranslateBy

This sample demonstrates how [Model:TranslateBy()](/docs/reference/engine/classes/Model#TranslateBy) ignores collisions and respects
the orientation of the model.

A simple two part [Model](/docs/reference/engine/classes/Model) is created, rotated 45 degrees on the Y axis, and its
[Model.PrimaryPart](/docs/reference/engine/classes/Model#PrimaryPart) is set. An large obstruction part is placed next to it.

After 5 seconds [Model:TranslateBy()](/docs/reference/engine/classes/Model#TranslateBy) is used to direct the model to move inside
the obstruction part. The model will move inside of the obstruction and
maintain it's current orientation.

```
local START_POSITION = Vector3.new(-20, 10, 0)



local END_POSITION = Vector3.new(0, 10, 0)



local model = Instance.new("Model")



local part1 = Instance.new("Part")



part1.Size = Vector3.new(4, 4, 4)



part1.CFrame = CFrame.new(START_POSITION) * CFrame.Angles(0, math.rad(45), 0)



part1.Anchored = true



part1.BrickColor = BrickColor.new("Bright yellow")



part1.Parent = model



local part2 = Instance.new("Part")



part2.Size = Vector3.new(2, 2, 2)



part2.CFrame = part1.CFrame * CFrame.new(0, 3, 0)



part2.Anchored = true



part2.BrickColor = BrickColor.new("Bright blue")



part2.Parent = model



model.PrimaryPart = part1



model.Parent = workspace



local obstruction = Instance.new("Part")



obstruction.Name = "Obstruction"



obstruction.Size = Vector3.new(10, 10, 10)



obstruction.Position = Vector3.new(0, 10, 0)



obstruction.Transparency = 0.5



obstruction.Anchored = true



obstruction.BrickColor = BrickColor.new("Bright green")



obstruction.Parent = workspace



task.wait(3)



-- use TranslateBy to shift the model into the obstruction



model:TranslateBy(END_POSITION - START_POSITION)
```

Provide feedback

---