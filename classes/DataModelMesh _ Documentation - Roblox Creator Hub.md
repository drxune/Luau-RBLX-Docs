# DataModelMesh | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/DataModelMesh
Scraped: 2026-01-11T02:40:37.792616Z

## Tags
- Not Creatable

## Inherits
- Instance
- DataModelMesh
- Object
- BevelMesh
- FileMesh
- BaseParts
- MeshParts
- MeshPart
- CharacterMesh
- BasePart.Position
- BasePart
- SelectionBox
- DataModelMesh.Scale
- TweenService
- DataModelMesh.Offset
- SpecialMesh
- SpecialMesh.FileType
- BlockMesh
- BasePart.Size
- CylinderMesh
- FileMesh.TextureId
- Texture
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [DataModelMesh](/docs/reference/engine/classes/DataModelMesh)

English

Feedback

Engine Class

DataModelMesh

The DataModelMesh is an abstract class from which mesh classes descend.

Not Creatable

Not Browsable

---

Summary

Properties

|  |
| --- |
| [Offset](#Offset):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Scale](#Scale):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [VertexColor](#VertexColor):[Vector3](/docs/reference/engine/datatypes/Vector3) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[BevelMesh](/docs/reference/engine/classes/BevelMesh), [FileMesh](/docs/reference/engine/classes/FileMesh)

The DataModelMesh is an abstract class from which mesh classes descend.

Mesh classes are objects that, when parented to [BaseParts](/docs/reference/engine/classes/BasePart)
alter the appearance of the part to that of a predefined mesh. Note, they only
alter the appearance of the part and not the physics/collision boundaries of
the part. Developers looking to apply a mesh to a part that alters the part's
collision should use [MeshParts](/docs/reference/engine/classes/MeshPart).

Note the [MeshPart](/docs/reference/engine/classes/MeshPart) and [CharacterMesh](/docs/reference/engine/classes/CharacterMesh) classes do not descend
from DataModelMesh.

---

API Reference

Properties

Offset

Read Parallel

The Offset of a mesh determines the relative position from the
[BasePart.Position](/docs/reference/engine/classes/BasePart#Position) of a [BasePart](/docs/reference/engine/classes/BasePart) that the mesh will be
displayed at.

DataModelMesh.Offset:[Vector3](/docs/reference/engine/datatypes/Vector3)

The Offset of a mesh determines the distance from the
[BasePart.Position](/docs/reference/engine/classes/BasePart#Position) of a [BasePart](/docs/reference/engine/classes/BasePart) that the mesh will be
displayed.

#### How to use mesh offset

The Offset property changes the relative position the mesh will be
rendered at. For example, an offset of 0, 5, 0 will cause the mesh to be
displayed 5 studs above the position of the [BasePart](/docs/reference/engine/classes/BasePart).

The position of the [BasePart](/docs/reference/engine/classes/BasePart) remains unchanged, meaning the
physics collision box of the part will remain in the same location. This
is demonstrated in the image below where the green outline (a
[SelectionBox](/docs/reference/engine/classes/SelectionBox)) shows the extents of the [BasePart](/docs/reference/engine/classes/BasePart).

#### Other uses for mesh offset

There are a number of interesting uses for the mesh offset property.

* Offset and [DataModelMesh.Scale](/docs/reference/engine/classes/DataModelMesh#Scale) can be animated using
  [TweenService](/docs/reference/engine/classes/TweenService) relatively inexpensively as the engine does not
  need to make any physics/collision calculations as the [BasePart](/docs/reference/engine/classes/BasePart)
  is not moved.
* Changing the relationship between the mesh and its collision extents
  (determined by the [BasePart](/docs/reference/engine/classes/BasePart))

Code Samples

Mesh Offset and Scale

In this code sample a BasePart is instanced with a SpecialMesh. The
[DataModelMesh.Scale](/docs/reference/engine/classes/DataModelMesh#Scale) and [DataModelMesh.Offset](/docs/reference/engine/classes/DataModelMesh#Offset) properties of the
SpecialMesh are then animated using TweenService.

```
local TweenService = game:GetService("TweenService")



-- instance a part and a mesh



local part = Instance.new("Part")



part.Size = Vector3.new(4, 8, 4)



part.Position = Vector3.new(0, 4, 0)



part.Anchored = true



part.CanCollide = false



local mesh = Instance.new("SpecialMesh")



mesh.MeshType = Enum.MeshType.FileMesh



mesh.MeshId = "rbxassetid://1086413449"



mesh.TextureId = "rbxassetid://1461576423"



mesh.Offset = Vector3.new(0, 0, 0)



mesh.Scale = Vector3.new(4, 4, 4)



mesh.Parent = part



-- selection box to show part extents



local box = Instance.new("SelectionBox")



box.Adornee = part



box.Parent = part



-- parent part to workspace



part.Parent = workspace



-- animate offset and scale with a tween



local tween = TweenService:Create(



mesh,



TweenInfo.new(1, Enum.EasingStyle.Linear, Enum.EasingDirection.Out, -1, true, 0),



{ Scale = Vector3.new(1, 1, 1), Offset = Vector3.new(0, 3, 0) }



)



tween:Play()
```

Provide feedback

---

Scale

Read Parallel

The Scale of a mesh determines the size of the mesh relative to its
original dimensions.

DataModelMesh.Scale:[Vector3](/docs/reference/engine/datatypes/Vector3)

The Scale of a mesh determines the size of the mesh relative to its
original dimensions.

#### How to use mesh scale

The scale property works slightly differently depending on the type of
mesh being used. Note the size of the [BasePart](/docs/reference/engine/classes/BasePart) remains unchanged,
meaning the physics collision box of the part will remain the same.

* [SpecialMesh](/docs/reference/engine/classes/SpecialMesh) objects with [SpecialMesh.FileType](/docs/reference/engine/classes/SpecialMesh#FileType) set to
  'FileMesh' scale relative to the original dimensions of the mesh when it
  was uploaded to Roblox
* [BlockMesh](/docs/reference/engine/classes/BlockMesh) objects or [SpecialMesh](/docs/reference/engine/classes/SpecialMesh) objects with
  [SpecialMesh.FileType](/docs/reference/engine/classes/SpecialMesh#FileType) set to 'Brick', 'Wedge' or 'Sphere' scale
  uniformly relative to the [BasePart.Size](/docs/reference/engine/classes/BasePart#Size) of their parent
* [CylinderMesh](/docs/reference/engine/classes/CylinderMesh) objects or [SpecialMesh](/docs/reference/engine/classes/SpecialMesh) objects with
  [SpecialMesh.FileType](/docs/reference/engine/classes/SpecialMesh#FileType) set to 'Cylinder' scale relative to the
  [BasePart.Size](/docs/reference/engine/classes/BasePart#Size) of their parent. Uniformly for the cylinders
  height axis and maintaining a 1:1 ratio for the length and width of the
  cylinder, using the lowest value.
* [SpecialMesh](/docs/reference/engine/classes/SpecialMesh) objects with [SpecialMesh.FileType](/docs/reference/engine/classes/SpecialMesh#FileType) set to
  'Head' currently scale in a non standard manner. Developers should not
  rely on this as there are plans to change this behavior.
* [SpecialMesh](/docs/reference/engine/classes/SpecialMesh) objects with [SpecialMesh.FileType](/docs/reference/engine/classes/SpecialMesh#FileType) set to
  'Torso' scale in a non standard manner. Developers should not rely on
  this as there are plans to deprecate this mesh type.

#### Mesh scale demonstration

The above behavior can be seen in the following demonstration images.

Linear scaling relative to part size for 'Brick', 'Wedge' and 'Sphere'
meshes.

Linear scaling relative to original uploaded mesh for 'FileMesh' meshes

Non-uniform constrained scaling for 'Cylinder' meshes

#### Other uses for mesh scale

There are a number of interesting uses for the mesh offset property.

* [DataModelMesh.Offset](/docs/reference/engine/classes/DataModelMesh#Offset) and Scale can be animated using
  [TweenService](/docs/reference/engine/classes/TweenService) relatively inexpensively as the engine does not
  need to make any physics/collision calculations as the [BasePart](/docs/reference/engine/classes/BasePart)
  is not changed.
* Changing the relationship between the mesh and its collision extents
  (determined by the [BasePart](/docs/reference/engine/classes/BasePart))

Code Samples

Mesh Offset and Scale

In this code sample a BasePart is instanced with a SpecialMesh. The
[DataModelMesh.Scale](/docs/reference/engine/classes/DataModelMesh#Scale) and [DataModelMesh.Offset](/docs/reference/engine/classes/DataModelMesh#Offset) properties of the
SpecialMesh are then animated using TweenService.

```
local TweenService = game:GetService("TweenService")



-- instance a part and a mesh



local part = Instance.new("Part")



part.Size = Vector3.new(4, 8, 4)



part.Position = Vector3.new(0, 4, 0)



part.Anchored = true



part.CanCollide = false



local mesh = Instance.new("SpecialMesh")



mesh.MeshType = Enum.MeshType.FileMesh



mesh.MeshId = "rbxassetid://1086413449"



mesh.TextureId = "rbxassetid://1461576423"



mesh.Offset = Vector3.new(0, 0, 0)



mesh.Scale = Vector3.new(4, 4, 4)



mesh.Parent = part



-- selection box to show part extents



local box = Instance.new("SelectionBox")



box.Adornee = part



box.Parent = part



-- parent part to workspace



part.Parent = workspace



-- animate offset and scale with a tween



local tween = TweenService:Create(



mesh,



TweenInfo.new(1, Enum.EasingStyle.Linear, Enum.EasingDirection.Out, -1, true, 0),



{ Scale = Vector3.new(1, 1, 1), Offset = Vector3.new(0, 3, 0) }



)



tween:Play()
```

Provide feedback

---

VertexColor

Read Parallel

Changes the hue of a mesh's texture, used with [FileMesh.TextureId](/docs/reference/engine/classes/FileMesh#TextureId).

DataModelMesh.VertexColor:[Vector3](/docs/reference/engine/datatypes/Vector3)

VertexColor determines the hue change of the
[Texture](/docs/reference/engine/classes/FileMesh#TextureId) of a [FileMesh](/docs/reference/engine/classes/FileMesh). Note that this
property is a [Vector3](/docs/reference/engine/datatypes/Vector3) rather than a [Color3](/docs/reference/engine/datatypes/Color3); to
convert, use the [Color3.R](/docs/reference/engine/datatypes/Color3#R), [Color3.G](/docs/reference/engine/datatypes/Color3#G), and
[Color3.B](/docs/reference/engine/datatypes/Color3#B) properties.

Although this property allows basic modification of a texture, changing a
texture entirely provides more control. See [MeshPart](/docs/reference/engine/classes/MeshPart) for more
details.

Provide feedback

---