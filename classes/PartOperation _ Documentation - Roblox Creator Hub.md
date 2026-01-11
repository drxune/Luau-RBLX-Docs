# PartOperation | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/PartOperation
Scraped: 2026-01-11T02:32:56.871372Z

## Tags
- Not Replicated

## Inherits
- TriangleMeshPart
- PartOperation
- BasePart
- PVInstance
- Instance
- Object
- IntersectOperation
- NegateOperation
- UnionOperation
- SmoothingAngle
- BasePart.Color
- BasePart.BrickColor
- Color
- BrickColor
- UnionAsync()
- SubtractAsync()
- IntersectAsync()
- Attachments
- Constraints
- ParticleEmitters
- CalculateConstraintsToPreserve()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [TriangleMeshPart](/docs/reference/engine/classes/TriangleMeshPart)
6. /
7. [PartOperation](/docs/reference/engine/classes/PartOperation)

English

Feedback

Engine Class

PartOperation

An abstract class that all parts based on solid modeling inherit from.

---

Summary

Properties

|  |
| --- |
| [RenderFidelity](#RenderFidelity):[Enum.RenderFidelity](/docs/reference/engine/enums/RenderFidelity) |
| [SmoothingAngle](#SmoothingAngle):[number](/docs/luau/numbers) |
| [TriangleCount](#TriangleCount):[number](/docs/luau/numbers) |
| [UsePartColor](#UsePartColor):[boolean](/docs/luau/booleans) |

Methods

|  |
| --- |
| [SubstituteGeometry](#SubstituteGeometry)(source: [Instance](/docs/reference/engine/datatypes/Instance)):() |

Inherited Members

3 inherited from [TriangleMeshPart](/docs/reference/engine/classes/TriangleMeshPart)

105 inherited from [BasePart](/docs/reference/engine/classes/BasePart)

4 inherited from [PVInstance](/docs/reference/engine/classes/PVInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[IntersectOperation](/docs/reference/engine/classes/IntersectOperation), [NegateOperation](/docs/reference/engine/classes/NegateOperation), [UnionOperation](/docs/reference/engine/classes/UnionOperation)

An abstract class that all parts based on
[solid modeling](/docs/parts/solid-modeling) inherit from.

---

API Reference

Properties

RenderFidelity

Plugin Security

Read Parallel

The level of detail used to render the solid modeled part.

PartOperation.RenderFidelity:[Enum.RenderFidelity](/docs/reference/engine/enums/RenderFidelity)

This property determines the level of detail that the solid modeled part
will be shown in. It can be set to the possible values of the
[Enum.RenderFidelity](/docs/reference/engine/enums/RenderFidelity) enum.

The default value is [Automatic](/docs/reference/engine/enums/RenderFidelity#Automatic), meaning
the part's detail is based on its distance from the camera as outlined in
the following table.

| Distance From Camera | Render Fidelity |
| --- | --- |
| Less than 250 studs | Highest |
| 250-500 studs | Medium |
| 500 or more studs | Lowest |

Provide feedback

---

SmoothingAngle

Plugin Security

Read Parallel

An angle in degrees which affects the smooth shading of a solid modeled
part.

PartOperation.SmoothingAngle:[number](/docs/luau/numbers)

This property represents an angle in degrees for a threshold value between
face normals on a [solid modeled](/docs/parts/solid-modeling) part.
If the normal difference is less than the value, normals will be adjusted
to smooth the difference. While a value between 30 and 70 degrees usually
produces a good result, values between 90 and 180 are not recommended as
they may cause a "shadowing" effect on unions with sharp edges.

Note that smoothing does not affect the normals between different
materials or different colors.

![Solid modeled part with SmoothingAngle of 0](https://prod.docsiteassets.roblox.com/assets/modeling/solid-modeling/CSG-SmoothingAngle-0.jpg)


[SmoothingAngle](/docs/reference/engine/classes/PartOperation#SmoothingAngle)
= 0


![Solid modeled part with SmoothingAngle of 50](https://prod.docsiteassets.roblox.com/assets/modeling/solid-modeling/CSG-SmoothingAngle-50.jpg)


[SmoothingAngle](/docs/reference/engine/classes/PartOperation#SmoothingAngle)
= 50

Provide feedback

---

TriangleCount

Read Only

Not Replicated

Read Parallel

The number of polygons in this solid model.

PartOperation.TriangleCount:[number](/docs/luau/numbers)

The number of polygons in this solid model.

Provide feedback

---

UsePartColor

Read Parallel

Sets whether the [PartOperation](/docs/reference/engine/classes/PartOperation) can be recolored using inherited
color properties.

PartOperation.UsePartColor:[boolean](/docs/luau/booleans)

Sets whether the [PartOperation](/docs/reference/engine/classes/PartOperation) can be recolored using the
[BasePart.Color](/docs/reference/engine/classes/BasePart#Color) or [BasePart.BrickColor](/docs/reference/engine/classes/BasePart#BrickColor) properties. When
true, the entire union will be colored as per [Color](/docs/reference/engine/classes/BasePart#Color)
or [BrickColor](/docs/reference/engine/classes/BasePart#BrickColor). When false, the parts in the
union will maintain their original colors from before the onion operation
was performed.

Provide feedback

---

Methods

SubstituteGeometry

Substitutes the geometry of this [PartOperation](/docs/reference/engine/classes/PartOperation) with the geometry
of another [PartOperation](/docs/reference/engine/classes/PartOperation).

PartOperation:SubstituteGeometry(source:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| source:[Instance](/docs/reference/engine/datatypes/Instance)  The [PartOperation](/docs/reference/engine/classes/PartOperation) whose geometry will substitute the geometry of this [PartOperation](/docs/reference/engine/classes/PartOperation). |

Returns

()

Substitutes the geometry of this [PartOperation](/docs/reference/engine/classes/PartOperation) with the geometry
of another [PartOperation](/docs/reference/engine/classes/PartOperation). This makes it easier to utilize the
geometry of a solid modeling operation like
[UnionAsync()](/docs/reference/engine/classes/GeometryService#UnionAsync),
[SubtractAsync()](/docs/reference/engine/classes/GeometryService#SubtractAsync), or
[IntersectAsync()](/docs/reference/engine/classes/GeometryService#IntersectAsync) but maintain
properties, attributes, tags, and children of the main part such as
[Attachments](/docs/reference/engine/classes/Attachment), [Constraints](/docs/reference/engine/classes/Constraint),
[ParticleEmitters](/docs/reference/engine/classes/ParticleEmitter), light objects, decals, and more.
This approach also circumvents the potential "flicker" of completely
replacing the original [PartOperation](/docs/reference/engine/classes/PartOperation) with another.

Note that if you're calling this method on a [PartOperation](/docs/reference/engine/classes/PartOperation) with
child [Attachments](/docs/reference/engine/classes/Attachment) or [Constraints](/docs/reference/engine/classes/Constraint),
you should calculate the affected instances with
[CalculateConstraintsToPreserve()](/docs/reference/engine/classes/GeometryService#CalculateConstraintsToPreserve),
then drop those whose recommended parent is nil.

Code Samples

Substitute Geometry and Drop Constraints

The following example substitutes the geometry of one [PartOperation](/docs/reference/engine/classes/PartOperation)
with the geometry of another [PartOperation](/docs/reference/engine/classes/PartOperation), then drops
constraints/attachments that should not be preserved after
substitution.

```
local GeometryService = game:GetService("GeometryService")



local mainPart = workspace.PurpleBlock



local otherParts = { workspace.BlueBlock }



local options = {



CollisionFidelity = Enum.CollisionFidelity.Default,



RenderFidelity = Enum.RenderFidelity.Automatic,



SplitApart = false,



}



local constraintOptions = {



tolerance = 0.1,



weldConstraintPreserve = Enum.WeldConstraintPreserve.All,



}



-- Perform union operation in pcall() since it's asyncronous



local success, newParts = pcall(function()



return GeometryService:UnionAsync(mainPart, otherParts, options)



end)



if success and #newParts > 0 and mainPart:IsA("PartOperation") then



-- Set first part in resulting operation as part to use for substitution



-- First part is simply an option; this can be any PartOperation



local substitutePart = newParts[1]



-- Reposition part to the position of main part



substitutePart.CFrame = mainPart.CFrame



-- Calculate constraints/attachments to either preserve or drop



local recommendedTable = GeometryService:CalculateConstraintsToPreserve(mainPart, newParts, constraintOptions)



-- Substitute main part's geometry with substitution geometry



mainPart:SubstituteGeometry(substitutePart)



-- Drop constraints/attachments that are not automatically preserved with substitution



for _, item in pairs(recommendedTable) do



if item.Attachment then



if item.ConstraintParent == nil then



item.Constraint.Parent = nil



end



if item.AttachmentParent == nil then



item.Attachment.Parent = nil



end



elseif item.WeldConstraint then



if item.Parent == nil then



item.WeldConstraint.Parent = nil



end



end



end



-- Destroy other parts



for _, otherPart in pairs(otherParts) do



otherPart.Parent = nil



otherPart:Destroy()



end



end
```

Provide feedback

---