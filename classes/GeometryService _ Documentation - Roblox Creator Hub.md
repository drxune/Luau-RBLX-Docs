# GeometryService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/GeometryService
Scraped: 2026-01-11T02:37:11.033603Z

## Tags
- Not Creatable
- Service

## Inherits
- Instance
- GeometryService
- Object
- Constraints
- Attachments
- UnionAsync()
- Attachment
- Parent
- WeldConstraints
- NoCollisionConstraints
- Constraint
- HingeConstraint
- BasePart
- WeldConstraint
- NoCollisionConstraint
- CalculateConstraintsToPreserve()
- PartOperations
- Part
- PartOperation
- CollisionFidelity
- RenderFidelity
- FluidFidelity
- Parts
- Terrain
- MeshParts
- Clone()
- Color
- Material
- MaterialVariant
- Reflectance
- Transparency
- CanCollide
- Anchored
- Density
- Elasticity
- ElasticityWeight
- Friction
- FrictionWeight
- IntersectAsync()
- BasePart:IntersectAsync()
- Destroy()
- UsePartColor
- SubstituteGeometry()
- ParticleEmitters
- SubtractAsync()
- BasePart:SubtractAsync()
- BasePart:UnionAsync()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [GeometryService](/docs/reference/engine/classes/GeometryService)

English

Feedback

Engine Class

GeometryService

Service containing geometric operations.

Not Creatable

Service

---

Summary

Methods

|  |
| --- |
| [CalculateConstraintsToPreserve](#CalculateConstraintsToPreserve)(source: [Instance](/docs/reference/engine/datatypes/Instance),destination: [Array](/docs/luau/tables#arrays),options: [Dictionary](/docs/luau/tables#dictionaries)):[Array](/docs/luau/tables#arrays) |
| [IntersectAsync](#IntersectAsync)(part: [Instance](/docs/reference/engine/datatypes/Instance),parts: [Array](/docs/luau/tables#arrays),options: [Dictionary](/docs/luau/tables#dictionaries)):[Array](/docs/luau/tables#arrays) |
| [SubtractAsync](#SubtractAsync)(part: [Instance](/docs/reference/engine/datatypes/Instance),parts: [Array](/docs/luau/tables#arrays),options: [Dictionary](/docs/luau/tables#dictionaries)):[Array](/docs/luau/tables#arrays) |
| [UnionAsync](#UnionAsync)(part: [Instance](/docs/reference/engine/datatypes/Instance),parts: [Array](/docs/luau/tables#arrays),options: [Dictionary](/docs/luau/tables#dictionaries)):[Array](/docs/luau/tables#arrays) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Service containing geometric operations not directly related to specific
objects.

---

API Reference

Methods

CalculateConstraintsToPreserve

Returns a table of [Constraints](/docs/reference/engine/classes/Constraint) and
[Attachments](/docs/reference/engine/classes/Attachment) which you may choose to preserve, along
with their respective parents.

GeometryService:CalculateConstraintsToPreserve(

source:[Instance](/docs/reference/engine/datatypes/Instance), destination:[Array](/docs/luau/tables#arrays), options:[Dictionary](/docs/luau/tables#dictionaries)

):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| source:[Instance](/docs/reference/engine/datatypes/Instance)  An original object that the solid modeling operation was performed on, for example part in [UnionAsync()](/docs/reference/engine/classes/GeometryService#UnionAsync). |
| destination:[Array](/docs/luau/tables#arrays) |
| options:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" Options dictionary for the method:   * tolerance — The distance tolerance, in regards to   [Attachment](/docs/reference/engine/classes/Attachment) preservation, between the attachment and the   closest point on the original part's surface versus the closest   point on the resulting part's surface. If the resulting distance   following the solid modeling operation is greater than this value,   the [Parent](/docs/reference/engine/classes/Instance#Parent) of attachments and their   associated constraints will be nil in the returned recommendation   table. * weldConstraintPreserve — A [Enum.WeldConstraintPreserve](/docs/reference/engine/enums/WeldConstraintPreserve) enum   value describing how [WeldConstraints](/docs/reference/engine/classes/WeldConstraint) are   preserved in the resulting recommendation table. * dropAttachmentsWithoutConstraints — Boolean with default of   true. If set to false, [Attachments](/docs/reference/engine/classes/Attachment) that have   no [Constraints](/docs/reference/engine/classes/Constraint) will be preserved. |

Returns

[Array](/docs/luau/tables#arrays)

Table containing information for general case
[Constraints](/docs/reference/engine/classes/Constraint),
[NoCollisionConstraints](/docs/reference/engine/classes/NoCollisionConstraint), and
[WeldConstraints](/docs/reference/engine/classes/WeldConstraint). In cases where an
[Attachment](/docs/reference/engine/classes/Attachment) or [Constraint](/docs/reference/engine/classes/Constraint) should be dropped, its
respective parent will be nil.

For general case [Constraints](/docs/reference/engine/classes/Constraint) such as
[HingeConstraint](/docs/reference/engine/classes/HingeConstraint):

| Key | Type |
| --- | --- |
| Attachment | [Attachment](/docs/reference/engine/classes/Attachment) |
| Constraint | [Constraint](/docs/reference/engine/classes/Constraint) or nil |
| AttachmentParent | [BasePart](/docs/reference/engine/classes/BasePart) or nil |
| ConstraintParent | [BasePart](/docs/reference/engine/classes/BasePart) or nil |

For [WeldConstraints](/docs/reference/engine/classes/WeldConstraint):

| Key | Type |
| --- | --- |
| WeldConstraint | [WeldConstraint](/docs/reference/engine/classes/WeldConstraint) |
| WeldConstraintParent | [BasePart](/docs/reference/engine/classes/BasePart) or nil |
| WeldConstraintPart0 | [BasePart](/docs/reference/engine/classes/BasePart) |
| WeldConstraintPart1 | [BasePart](/docs/reference/engine/classes/BasePart) |

For [NoCollisionConstraints](/docs/reference/engine/classes/NoCollisionConstraint):

| Key | Type |
| --- | --- |
| NoCollisionConstraint | [NoCollisionConstraint](/docs/reference/engine/classes/NoCollisionConstraint) |
| NoCollisionConstraintParent | [BasePart](/docs/reference/engine/classes/BasePart) or nil |
| NoCollisionConstraintPart0 | [BasePart](/docs/reference/engine/classes/BasePart) |
| NoCollisionConstraintPart1 | [BasePart](/docs/reference/engine/classes/BasePart) |

Returns a table of [Constraints](/docs/reference/engine/classes/Constraint) and
[Attachments](/docs/reference/engine/classes/Attachment) which you may choose to preserve, along
with their respective parents. Iterating over this table lets you decide
whether to reparent recommended constraints and attachments to their
respective parents.

Code Samples

Preserve Constraints

The following example shows how to preserve [Attachments](/docs/reference/engine/classes/Attachment) and
[Constraints](/docs/reference/engine/classes/Constraint) based on a recommended table produced by
[CalculateConstraintsToPreserve()](/docs/reference/engine/classes/GeometryService#CalculateConstraintsToPreserve).

```
local GeometryService = game:GetService("GeometryService")



local mainPart = workspace.PurpleBlock



local otherParts = { workspace.BlueBlock }



local options = {



CollisionFidelity = Enum.CollisionFidelity.Default,



RenderFidelity = Enum.RenderFidelity.Automatic,



SplitApart = true,



}



local constraintOptions = {



tolerance = 0.1,



weldConstraintPreserve = Enum.WeldConstraintPreserve.All,



dropAttachmentsWithoutConstraints = false,



}



-- Perform subtract operation in pcall() since it's asyncronous



local success, newParts = pcall(function()



return GeometryService:SubtractAsync(mainPart, otherParts, options)



end)



if success and newParts then



-- Loop through resulting parts to reparent/reposition



for _, newPart in pairs(newParts) do



newPart.Parent = mainPart.Parent



newPart.CFrame = mainPart.CFrame



newPart.Anchored = mainPart.Anchored



end



-- Calculate constraints/attachments to either preserve or drop



local recommendedTable = GeometryService:CalculateConstraintsToPreserve(mainPart, newParts, constraintOptions)



-- Preserve constraints/attachments based on recommended table



for _, item in pairs(recommendedTable) do



if item.Attachment then



item.Attachment.Parent = item.AttachmentParent



if item.Constraint then



item.Constraint.Parent = item.ConstraintParent



end



elseif item.NoCollisionConstraint then



local newNoCollision = Instance.new("NoCollisionConstraint")



newNoCollision.Part0 = item.NoCollisionPart0



newNoCollision.Part1 = item.NoCollisionPart1



newNoCollision.Parent = item.NoCollisionParent



elseif item.WeldConstraint then



local newWeldConstraint = Instance.new("WeldConstraint")



newWeldConstraint.Part0 = item.WeldConstraintPart0



newWeldConstraint.Part1 = item.WeldConstraintPart1



newWeldConstraint.Parent = item.WeldConstraintParent



end



end



-- Destroy original parts



mainPart.Parent = nil



mainPart:Destroy()



for _, otherPart in pairs(otherParts) do



otherPart.Parent = nil



otherPart:Destroy()



end



end
```

Provide feedback

---

IntersectAsync

Yields

Creates one or more [PartOperations](/docs/reference/engine/classes/PartOperation) from the
intersecting geometry of one part and other parts.

GeometryService:IntersectAsync(

part:[Instance](/docs/reference/engine/datatypes/Instance), parts:[Array](/docs/luau/tables#arrays), options:[Dictionary](/docs/luau/tables#dictionaries)

):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| part:[Instance](/docs/reference/engine/datatypes/Instance)  Main [Part](/docs/reference/engine/classes/Part) or [PartOperation](/docs/reference/engine/classes/PartOperation) to operate on. |
| parts:[Array](/docs/luau/tables#arrays)  Array of parts to intersect with the main part. |
| options:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" Options table containing all the controls for the method:   * CollisionFidelity — The value of   [CollisionFidelity](/docs/reference/engine/classes/PartOperation#CollisionFidelity) in the   resulting parts. * RenderFidelity — The value of   [RenderFidelity](/docs/reference/engine/classes/PartOperation#RenderFidelity) in the resulting   parts. * FluidFidelity — The value of   [FluidFidelity](/docs/reference/engine/classes/PartOperation#FluidFidelity) in the resulting   parts. * SplitApart — Boolean controlling whether the objects should all be   kept together or properly split apart. Default is true (split). |

Returns

[Array](/docs/luau/tables#arrays)

One or more [PartOperations](/docs/reference/engine/classes/PartOperation) from the intersecting
geometry of the main part (part) and the other parts.

Creates one or more [PartOperations](/docs/reference/engine/classes/PartOperation) from the
intersecting geometry of the main part and other parts in the given array.
Only primitive [Parts](/docs/reference/engine/classes/Part) and [PartOperations](/docs/reference/engine/classes/PartOperation)
are supported, not [Terrain](/docs/reference/engine/classes/Terrain) or [MeshParts](/docs/reference/engine/classes/MeshPart). Similar
to [Clone()](/docs/reference/engine/classes/Instance#Clone), the returned parts have no set
[Parent](/docs/reference/engine/classes/Instance#Parent).

The following properties from the main part (part) are applied to the
resulting [PartOperations](/docs/reference/engine/classes/PartOperation):

* [Color](/docs/reference/engine/classes/BasePart#Color), [Material](/docs/reference/engine/classes/BasePart#Material),
  [MaterialVariant](/docs/reference/engine/classes/BasePart#MaterialVariant),
  [Reflectance](/docs/reference/engine/classes/BasePart#Reflectance),
  [Transparency](/docs/reference/engine/classes/BasePart#Transparency)
* [CanCollide](/docs/reference/engine/classes/BasePart#CanCollide)
* [Anchored](/docs/reference/engine/classes/BasePart#Anchored), [Density](/docs/reference/engine/classes/BasePart#Density),
  [Elasticity](/docs/reference/engine/classes/BasePart#Elasticity),
  [ElasticityWeight](/docs/reference/engine/classes/BasePart#ElasticityWeight),
  [Friction](/docs/reference/engine/classes/BasePart#Friction),
  [FrictionWeight](/docs/reference/engine/classes/BasePart#FrictionWeight)

In the following image comparison,
[IntersectAsync()](/docs/reference/engine/classes/GeometryService#IntersectAsync) is called using
the purple block and an array containing the blue block. The resulting
[PartOperation](/docs/reference/engine/classes/PartOperation) resolves into a shape of the intersecting geometry
of both parts.

![Two block parts overlapping](https://prod.docsiteassets.roblox.com/assets/modeling/solid-modeling/Separate-Parts-To-Intersect.jpg)


Separate parts


![Parts intersected into a new solid model](https://prod.docsiteassets.roblox.com/assets/modeling/solid-modeling/Intersect-Result.jpg)


Resulting [PartOperation](/docs/reference/engine/classes/PartOperation)

#### Notes

* Compared to [BasePart:IntersectAsync()](/docs/reference/engine/classes/BasePart#IntersectAsync), this method differs as
  follows:

  + The input parts do not need to be parented to the scene, allowing for
    background operations.
  + When the SplitApart option is set to true (default), each distinct
    body will be returned in its own [PartOperation](/docs/reference/engine/classes/PartOperation).
  + Each of the returned parts are in the coordinate space of the main
    part. This means that the (0, 0, 0) of any returned part is not
    necessarily at the center of its body.
  + It's possible to call this method on the client, but with some
    limitations. First, it currently must be done with objects created
    on the client. Secondly, there is no replication available from client
    to the server.
* The original parts remain intact following a successful operation. In
  most cases, you should parent the returned
  [PartOperations](/docs/reference/engine/classes/PartOperation) to the same place as the main part,
  then [Destroy()](/docs/reference/engine/classes/Instance#Destroy) all of the original parts.
* By default, the face colors of the resulting
  [PartOperations](/docs/reference/engine/classes/PartOperation) are borrowed from the
  [Color](/docs/reference/engine/classes/BasePart#Color) property of the original parts, although
  you can enable their [UsePartColor](/docs/reference/engine/classes/PartOperation#UsePartColor)
  property to change them to a specific color.
* If an intersect operation would result in any
  [PartOperations](/docs/reference/engine/classes/PartOperation) with more than 20,000 triangles,
  they will be simplified to 20,000. This will result in an error with
  code -14.
* If the main part is moving during the calculation of the operation, you
  can set the resulting parts to the updated [CFrame](/docs/reference/engine/datatypes/CFrame) of the main
  part, since the returned parts are in the same coordinate space as the
  main part.
* If using this method with a [PartOperation](/docs/reference/engine/classes/PartOperation) as the main part, you
  can substitute the geometry of another [PartOperation](/docs/reference/engine/classes/PartOperation) via
  [SubstituteGeometry()](/docs/reference/engine/classes/PartOperation#SubstituteGeometry), making
  it easier to utilize the geometry of the operation but maintain
  properties, attributes, tags, and children of the main part such as
  [Attachments](/docs/reference/engine/classes/Attachment), [Constraints](/docs/reference/engine/classes/Constraint),
  [ParticleEmitters](/docs/reference/engine/classes/ParticleEmitter), light objects, and decals.
  This approach also circumvents the potential "flicker" of completely
  replacing the original [PartOperation](/docs/reference/engine/classes/PartOperation) with another.

Code Samples

GeometryService:IntersectAsync()

This example intersects the geometry of mainPart and the parts in the otherParts array, splitting them into distinct [PartOperations](/docs/reference/engine/classes/PartOperation). Then it destroys the original parts involved in the operation.

```
local GeometryService = game:GetService("GeometryService")



local mainPart = workspace.PurpleBlock



local otherParts = { workspace.BlueBlock }



local options = {



CollisionFidelity = Enum.CollisionFidelity.Default,



RenderFidelity = Enum.RenderFidelity.Automatic,



SplitApart = true,



}



-- Perform intersect operation in pcall() since it's asyncronous



local success, newParts = pcall(function()



return GeometryService:IntersectAsync(mainPart, otherParts, options)



end)



if success and newParts then



-- Loop through resulting parts to reparent/reposition



for _, newPart in pairs(newParts) do



newPart.Parent = mainPart.Parent



newPart.CFrame = mainPart.CFrame



newPart.Anchored = mainPart.Anchored



end



-- Destroy original parts



mainPart.Parent = nil



mainPart:Destroy()



for _, otherPart in pairs(otherParts) do



otherPart.Parent = nil



otherPart:Destroy()



end



end
```

Provide feedback

---

SubtractAsync

Yields

Creates one or more [PartOperations](/docs/reference/engine/classes/PartOperation) from one part
minus the geometry occupied by other parts.

GeometryService:SubtractAsync(

part:[Instance](/docs/reference/engine/datatypes/Instance), parts:[Array](/docs/luau/tables#arrays), options:[Dictionary](/docs/luau/tables#dictionaries)

):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| part:[Instance](/docs/reference/engine/datatypes/Instance)  Main [Part](/docs/reference/engine/classes/Part) or [PartOperation](/docs/reference/engine/classes/PartOperation) to operate on. |
| parts:[Array](/docs/luau/tables#arrays)  Array of parts to subtract from the main part. |
| options:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" Options table containing all the controls for the method:   * CollisionFidelity — The value of   [CollisionFidelity](/docs/reference/engine/classes/PartOperation#CollisionFidelity) in the   resulting parts. * RenderFidelity — The value of   [RenderFidelity](/docs/reference/engine/classes/PartOperation#RenderFidelity) in the resulting   parts. * FluidFidelity — The value of   [FluidFidelity](/docs/reference/engine/classes/PartOperation#FluidFidelity) in the resulting   parts. * SplitApart — Boolean controlling whether the objects should all be   kept together or properly split apart. Default is true (split). |

Returns

[Array](/docs/luau/tables#arrays)

One or more [PartOperations](/docs/reference/engine/classes/PartOperation) from the geometry of
the main part (part) minus the geometry occupied by the other parts.

Creates one or more [PartOperations](/docs/reference/engine/classes/PartOperation) from the main
part minus the geometry occupied by other parts in the given array. Only
primitive [Parts](/docs/reference/engine/classes/Part) and [PartOperations](/docs/reference/engine/classes/PartOperation) are
supported, not [Terrain](/docs/reference/engine/classes/Terrain) or [MeshParts](/docs/reference/engine/classes/MeshPart). Similar to
[Clone()](/docs/reference/engine/classes/Instance#Clone), the returned parts have no set
[Parent](/docs/reference/engine/classes/Instance#Parent).

The following properties from the main part (part) are applied to the
resulting [PartOperations](/docs/reference/engine/classes/PartOperation):

* [Color](/docs/reference/engine/classes/BasePart#Color), [Material](/docs/reference/engine/classes/BasePart#Material),
  [MaterialVariant](/docs/reference/engine/classes/BasePart#MaterialVariant),
  [Reflectance](/docs/reference/engine/classes/BasePart#Reflectance),
  [Transparency](/docs/reference/engine/classes/BasePart#Transparency)
* [CanCollide](/docs/reference/engine/classes/BasePart#CanCollide)
* [Anchored](/docs/reference/engine/classes/BasePart#Anchored), [Density](/docs/reference/engine/classes/BasePart#Density),
  [Elasticity](/docs/reference/engine/classes/BasePart#Elasticity),
  [ElasticityWeight](/docs/reference/engine/classes/BasePart#ElasticityWeight),
  [Friction](/docs/reference/engine/classes/BasePart#Friction),
  [FrictionWeight](/docs/reference/engine/classes/BasePart#FrictionWeight)

In the following image comparison,
[SubtractAsync()](/docs/reference/engine/classes/BasePart#SubtractAsync) is called using the blue
cylinder and an array containing the purple block. The resulting
[PartOperation](/docs/reference/engine/classes/PartOperation) resolves into a shape that omits the block's
geometry from that of the cylinder.

![Longer block overlapping a cylinder](https://prod.docsiteassets.roblox.com/assets/modeling/solid-modeling/Separate-Parts-To-Subtract.jpg)


Separate parts


![Block part subtracted from cylinder](https://prod.docsiteassets.roblox.com/assets/modeling/solid-modeling/Negate-Result.jpg)


Resulting [PartOperation](/docs/reference/engine/classes/PartOperation)

#### Notes

* Compared to [BasePart:SubtractAsync()](/docs/reference/engine/classes/BasePart#SubtractAsync), this method differs as
  follows:

  + The input parts do not need to be parented to the scene, allowing for
    background operations.
  + When the SplitApart option is set to true (default), each distinct
    body will be returned in its own [PartOperation](/docs/reference/engine/classes/PartOperation).
  + Each of the returned parts are in the coordinate space of the main
    part. This means that the (0, 0, 0) of any returned part is not
    necessarily at the center of its body.
  + It's possible to call this method on the client, but with some
    limitations. First, it currently must be done with objects created
    on the client. Secondly, there is no replication available from client
    to the server.
* The original parts remain intact following a successful operation. In
  most cases, you should parent the returned
  [PartOperations](/docs/reference/engine/classes/PartOperation) to the same place as the main part,
  then [Destroy()](/docs/reference/engine/classes/Instance#Destroy) all of the original parts.
* By default, the face colors of the resulting
  [PartOperations](/docs/reference/engine/classes/PartOperation) are borrowed from the
  [Color](/docs/reference/engine/classes/BasePart#Color) property of the original parts, although
  you can enable their [UsePartColor](/docs/reference/engine/classes/PartOperation#UsePartColor)
  property to change them to a specific color.
* If a subtract operation would result in any
  [PartOperations](/docs/reference/engine/classes/PartOperation) with more than 20,000 triangles,
  they will be simplified to 20,000. This will result in an error with
  code -14.
* If the main part is moving during the calculation of the operation, you
  can set the resulting parts to the updated [CFrame](/docs/reference/engine/datatypes/CFrame) of the main
  part, since the returned parts are in the same coordinate space as the
  main part.
* If using this method with a [PartOperation](/docs/reference/engine/classes/PartOperation) as the main part, you
  can substitute the geometry of another [PartOperation](/docs/reference/engine/classes/PartOperation) via
  [SubstituteGeometry()](/docs/reference/engine/classes/PartOperation#SubstituteGeometry), making
  it easier to utilize the geometry of the operation but maintain
  properties, attributes, tags, and children of the main part such as
  [Attachments](/docs/reference/engine/classes/Attachment), [Constraints](/docs/reference/engine/classes/Constraint),
  [ParticleEmitters](/docs/reference/engine/classes/ParticleEmitter), light objects, and decals.
  This approach also circumvents the potential "flicker" of completely
  replacing the original [PartOperation](/docs/reference/engine/classes/PartOperation) with another.

Code Samples

GeometryService:SubtractAsync()

This example subtracts the geometry of the parts in the otherParts array from mainPart, splitting the results into distinct [PartOperations](/docs/reference/engine/classes/PartOperation). Then it destroys the original parts involved in the operation.

```
local GeometryService = game:GetService("GeometryService")



local mainPart = workspace.BlueCylinder



local otherParts = { workspace.PurpleBlock }



local options = {



CollisionFidelity = Enum.CollisionFidelity.Default,



RenderFidelity = Enum.RenderFidelity.Automatic,



SplitApart = true,



}



-- Perform subtract operation in pcall() since it's asyncronous



local success, newParts = pcall(function()



return GeometryService:SubtractAsync(mainPart, otherParts, options)



end)



if success and newParts then



-- Loop through resulting parts to reparent/reposition



for _, newPart in pairs(newParts) do



newPart.Parent = mainPart.Parent



newPart.CFrame = mainPart.CFrame



newPart.Anchored = mainPart.Anchored



end



-- Destroy original parts



mainPart.Parent = nil



mainPart:Destroy()



for _, otherPart in pairs(otherParts) do



otherPart.Parent = nil



otherPart:Destroy()



end



end
```

Provide feedback

---

UnionAsync

Yields

Creates one or more [PartOperations](/docs/reference/engine/classes/PartOperation) from one part
plus the geometry occupied by other parts.

GeometryService:UnionAsync(

part:[Instance](/docs/reference/engine/datatypes/Instance), parts:[Array](/docs/luau/tables#arrays), options:[Dictionary](/docs/luau/tables#dictionaries)

):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| part:[Instance](/docs/reference/engine/datatypes/Instance)  Main [Part](/docs/reference/engine/classes/Part) or [PartOperation](/docs/reference/engine/classes/PartOperation) to operate on. |
| parts:[Array](/docs/luau/tables#arrays)  Array of parts to union with the main part. |
| options:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" Options table containing all the controls for the method:   * CollisionFidelity — The value of   [CollisionFidelity](/docs/reference/engine/classes/PartOperation#CollisionFidelity) in the   resulting parts. * RenderFidelity — The value of   [RenderFidelity](/docs/reference/engine/classes/PartOperation#RenderFidelity) in the resulting   parts. * FluidFidelity — The value of   [FluidFidelity](/docs/reference/engine/classes/PartOperation#FluidFidelity) in the resulting   parts. * SplitApart — Boolean controlling whether the objects should all be   kept together or properly split apart. Default is true (split). |

Returns

[Array](/docs/luau/tables#arrays)

One or more [PartOperations](/docs/reference/engine/classes/PartOperation) from the geometry of
the main part (part) plus the geometry occupied by the other parts.

Creates one or more [PartOperations](/docs/reference/engine/classes/PartOperation) from the main
part plus the geometry occupied by other parts in the given array. Only
primitive [Parts](/docs/reference/engine/classes/Part) and [PartOperations](/docs/reference/engine/classes/PartOperation) are
supported, not [Terrain](/docs/reference/engine/classes/Terrain) or [MeshParts](/docs/reference/engine/classes/MeshPart). Similar to
[Clone()](/docs/reference/engine/classes/Instance#Clone), the returned parts have no set
[Parent](/docs/reference/engine/classes/Instance#Parent).

The following properties from the main part (part) are applied to the
resulting [PartOperations](/docs/reference/engine/classes/PartOperation):

* [Color](/docs/reference/engine/classes/BasePart#Color), [Material](/docs/reference/engine/classes/BasePart#Material),
  [MaterialVariant](/docs/reference/engine/classes/BasePart#MaterialVariant),
  [Reflectance](/docs/reference/engine/classes/BasePart#Reflectance),
  [Transparency](/docs/reference/engine/classes/BasePart#Transparency)
* [CanCollide](/docs/reference/engine/classes/BasePart#CanCollide)
* [Anchored](/docs/reference/engine/classes/BasePart#Anchored), [Density](/docs/reference/engine/classes/BasePart#Density),
  [Elasticity](/docs/reference/engine/classes/BasePart#Elasticity),
  [ElasticityWeight](/docs/reference/engine/classes/BasePart#ElasticityWeight),
  [Friction](/docs/reference/engine/classes/BasePart#Friction),
  [FrictionWeight](/docs/reference/engine/classes/BasePart#FrictionWeight)

In the following image comparison,
[UnionAsync()](/docs/reference/engine/classes/GeometryService#UnionAsync) is called using the blue
block and an array containing the purple cylinder. The resulting
[PartOperation](/docs/reference/engine/classes/PartOperation) resolves into a shape of the combined geometry of
both parts.

![Block and cylinder parts overlapping](https://prod.docsiteassets.roblox.com/assets/modeling/solid-modeling/Separate-Parts-To-Union.jpg)


Separate parts


![Parts joined together into a single solid union](https://prod.docsiteassets.roblox.com/assets/modeling/solid-modeling/Union-Result.jpg)


Resulting [PartOperation](/docs/reference/engine/classes/PartOperation)

#### Notes

* Compared to [BasePart:UnionAsync()](/docs/reference/engine/classes/BasePart#UnionAsync), this method differs as
  follows:

  + The input parts do not need to be parented to the scene, allowing for
    background operations.
  + When the SplitApart option is set to true (default), each distinct
    body will be returned in its own [PartOperation](/docs/reference/engine/classes/PartOperation).
  + Each of the returned parts are in the coordinate space of the main
    part. This means that the (0, 0, 0) of any returned part is not
    necessarily at the center of its body.
  + It's possible to call this method on the client, but with some
    limitations. First, it currently must be done with objects created
    on the client. Secondly, there is no replication available from client
    to the server.
* The original parts remain intact following a successful operation. In
  most cases, you should parent the returned
  [PartOperations](/docs/reference/engine/classes/PartOperation) to the same place as the main part,
  then [Destroy()](/docs/reference/engine/classes/Instance#Destroy) all of the original parts.
* By default, the colors of the resulting
  [PartOperations](/docs/reference/engine/classes/PartOperation) are borrowed from the
  [Color](/docs/reference/engine/classes/BasePart#Color) property of the original parts, although
  you can enable their [UsePartColor](/docs/reference/engine/classes/PartOperation#UsePartColor)
  property to change them to a specific color.
* If a union operation would result in any
  [PartOperations](/docs/reference/engine/classes/PartOperation) with more than 20,000 triangles,
  they will be simplified to 20,000. This will result in an error with
  code -14.
* If the main part is moving during the calculation of the operation, you
  can set the resulting parts to the updated [CFrame](/docs/reference/engine/datatypes/CFrame) of the main
  part, since the returned parts are in the same coordinate space as the
  main part.
* If using this method with a [PartOperation](/docs/reference/engine/classes/PartOperation) as the main part, you
  can substitute the geometry of another [PartOperation](/docs/reference/engine/classes/PartOperation) via
  [SubstituteGeometry()](/docs/reference/engine/classes/PartOperation#SubstituteGeometry), making
  it easier to utilize the geometry of the operation but maintain
  properties, attributes, tags, and children of the main part such as
  [Attachments](/docs/reference/engine/classes/Attachment), [Constraints](/docs/reference/engine/classes/Constraint),
  [ParticleEmitters](/docs/reference/engine/classes/ParticleEmitter), light objects, and decals.
  This approach also circumvents the potential "flicker" of completely
  replacing the original [PartOperation](/docs/reference/engine/classes/PartOperation) with another.

Code Samples

GeometryService:UnionAsync()

This example combines the geometry of mainPart and the parts in the otherParts array, then it destroys the original parts involved in the operation.

```
local GeometryService = game:GetService("GeometryService")



local mainPart = workspace.BlueBlock



local otherParts = { workspace.PurpleCylinder }



local options = {



CollisionFidelity = Enum.CollisionFidelity.Default,



RenderFidelity = Enum.RenderFidelity.Automatic,



SplitApart = false,



}



-- Perform union operation in pcall() since it's asyncronous



local success, newParts = pcall(function()



return GeometryService:UnionAsync(mainPart, otherParts, options)



end)



if success and newParts then



-- Loop through resulting parts to reparent/reposition



for _, newPart in pairs(newParts) do



newPart.Parent = mainPart.Parent



newPart.CFrame = mainPart.CFrame



newPart.Anchored = mainPart.Anchored



end



-- Destroy original parts



mainPart.Parent = nil



mainPart:Destroy()



for _, otherPart in pairs(otherParts) do



otherPart.Parent = nil



otherPart:Destroy()



end



end
```

Provide feedback

---