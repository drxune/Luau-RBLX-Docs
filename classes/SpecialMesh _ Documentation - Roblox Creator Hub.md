# SpecialMesh | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/SpecialMesh
Scraped: 2026-01-11T02:37:50.665200Z

## Inherits
- FileMesh
- SpecialMesh
- BasePart
- MeshType
- DataModelMesh
- Instance
- Object
- BlockMesh
- Part
- Part.Shape
- FileMesh.TextureId
- WedgePart
- SpecialMesh.MeshType
- DataModelMesh.Scale
- DataModelMesh.Offset
- SpecialMesh.FileType
- MeshPart
- BasePart.Material
- MeshParts
- MeshPart.CollisionFidelity
- BaseParts
- Size
- Offset
- Scale
- MeshId
- Script
- LocalScript
- DataModelMesh.VertexColor
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [FileMesh](/docs/reference/engine/classes/FileMesh)
6. /
7. [SpecialMesh](/docs/reference/engine/classes/SpecialMesh)

English

Feedback

Engine Class

![SpecialMesh](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/SpecialMesh-Dark.webp)SpecialMesh

The [SpecialMesh](/docs/reference/engine/classes/SpecialMesh) object applies a mesh to a [BasePart](/docs/reference/engine/classes/BasePart) depending
on the [MeshType](/docs/reference/engine/classes/SpecialMesh#MeshType) property.

---

Summary

Properties

|  |
| --- |
| [MeshType](#MeshType):[Enum.MeshType](/docs/reference/engine/enums/MeshType) |

Inherited Members

2 inherited from [FileMesh](/docs/reference/engine/classes/FileMesh)

3 inherited from [DataModelMesh](/docs/reference/engine/classes/DataModelMesh)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The [SpecialMesh](/docs/reference/engine/classes/SpecialMesh) object applies a mesh to a [BasePart](/docs/reference/engine/classes/BasePart) depending
on the [MeshType](/docs/reference/engine/classes/SpecialMesh#MeshType) property. A number of options are
available.

* Brick - A block shape, equivalent to a [BlockMesh](/docs/reference/engine/classes/BlockMesh)
* Cylinder - A cylinder, identical to a [Part](/docs/reference/engine/classes/Part) with a
  [Part.Shape](/docs/reference/engine/classes/Part#Shape) of 'Cylinder'
* FileMesh - A user uploaded Mesh, equivalent to [FileMesh](/docs/reference/engine/classes/FileMesh) that a
  texture can be applied to using the [FileMesh.TextureId](/docs/reference/engine/classes/FileMesh#TextureId) property
* Head - A character head shape
* Sphere - A sphere shape, similar to a [Part](/docs/reference/engine/classes/Part) with a
  [Part.Shape](/docs/reference/engine/classes/Part#Shape) of 'Ball' but can be freely resized on all axis
* Wedge - A wedge shape, identical to a [WedgePart](/docs/reference/engine/classes/WedgePart)
* Torso - A block with sloped sides, due to be deprecated

Note, each [SpecialMesh.MeshType](/docs/reference/engine/classes/SpecialMesh#MeshType) will scale differently when using
[DataModelMesh.Scale](/docs/reference/engine/classes/DataModelMesh#Scale), for more information on this please see the page
on [DataModelMesh.Scale](/docs/reference/engine/classes/DataModelMesh#Scale). The SpecialMesh object also exposes the
[DataModelMesh.Offset](/docs/reference/engine/classes/DataModelMesh#Offset) property.

It is important to remember that when using a SpecialMesh, only the appearance
of a part changes. The collision model of the part remains the same. For
example, a character will not be able to walk correctly over a mesh as the
mesh geometry is not taken into account.

#### SpecialMesh vs MeshPart

There are currently two ways of using a developer created mesh. They are using
a SpecialMesh with the [SpecialMesh.FileType](/docs/reference/engine/classes/SpecialMesh#FileType) set to 'FileMesh', or by
using a [MeshPart](/docs/reference/engine/classes/MeshPart). Although, on the whole, the [MeshPart](/docs/reference/engine/classes/MeshPart) object
has superseded the SpecialMesh there are some differences developers should be
aware of.

* [BasePart.Material](/docs/reference/engine/classes/BasePart#Material) displays correctly on the mesh when using a
  [MeshPart](/docs/reference/engine/classes/MeshPart) and not when using a SpecialMesh
* [MeshParts](/docs/reference/engine/classes/MeshPart) include the [MeshPart.CollisionFidelity](/docs/reference/engine/classes/MeshPart#CollisionFidelity)
  property, meaning the collision model of a [MeshPart](/docs/reference/engine/classes/MeshPart) can be set to
  resemble the geometry of the mesh. The SpecialMesh object by contrast, uses
  the parent [BaseParts](/docs/reference/engine/classes/BasePart) collision model
* The mesh of a [MeshPart](/docs/reference/engine/classes/MeshPart) scales on all axis depending on the
  [Size](/docs/reference/engine/classes/BasePart#Size) property of the [MeshPart](/docs/reference/engine/classes/MeshPart), the mesh of a
  SpecialMesh does not
* The SpecialMesh object includes the [Offset](/docs/reference/engine/classes/DataModelMesh#Offset) and
  [Scale](/docs/reference/engine/classes/DataModelMesh#Scale) properties whereas
  [MeshParts](/docs/reference/engine/classes/MeshPart) do not
* The [MeshId](/docs/reference/engine/classes/FileMesh#MeshId) property of a [SpecialMesh](/docs/reference/engine/classes/SpecialMesh) can be
  changed by a [Script](/docs/reference/engine/classes/Script) or [LocalScript](/docs/reference/engine/classes/LocalScript) during runtime. The
  [MeshId](/docs/reference/engine/classes/MeshPart#MeshId) property of a [MeshPart](/docs/reference/engine/classes/MeshPart) can not.

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

Mesh VertexColor

In this code sample a BasePart is instanced with a SpecialMesh. The
[DataModelMesh.VertexColor](/docs/reference/engine/classes/DataModelMesh#VertexColor) property of the SpecialMesh is then
animated using TweenService.

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



mesh.VertexColor = Vector3.new(1, 1, 1)



mesh.Parent = part



-- parent part to workspace



part.Parent = workspace



-- create tweens



local tweenInfo = TweenInfo.new(1, Enum.EasingStyle.Linear, Enum.EasingDirection.Out)



local blackTween = TweenService:Create(mesh, tweenInfo, { VertexColor = Vector3.new(0, 0, 0) })



local redTween = TweenService:Create(mesh, tweenInfo, { VertexColor = Vector3.new(1, 0, 0) })



local greenTween = TweenService:Create(mesh, tweenInfo, { VertexColor = Vector3.new(0, 1, 0) })



local blueTween = TweenService:Create(mesh, tweenInfo, { VertexColor = Vector3.new(0, 0, 1) })



local resetTween = TweenService:Create(mesh, tweenInfo, { VertexColor = Vector3.new(1, 1, 1) })



-- animate



while true do



blackTween:Play()



blackTween.Completed:Wait()



redTween:Play()



redTween.Completed:Wait()



greenTween:Play()



greenTween.Completed:Wait()



blueTween:Play()



blueTween.Completed:Wait()



resetTween:Play()



resetTween.Completed:Wait()



task.wait()



end
```

---

API Reference

Properties

MeshType

Read Parallel

Determines the type of mesh that will be applied to the [BasePart](/docs/reference/engine/classes/BasePart)
the [SpecialMesh](/docs/reference/engine/classes/SpecialMesh) is parented to.

SpecialMesh.MeshType:[Enum.MeshType](/docs/reference/engine/enums/MeshType)

The mesh that the [SpecialMesh](/docs/reference/engine/classes/SpecialMesh)object applies to the
[BasePart](/docs/reference/engine/classes/BasePart) depends on the MeshType property. A number of options are
available.

* Brick - A block shape, equivalent to a [BlockMesh](/docs/reference/engine/classes/BlockMesh)
* Cylinder - A cylinder, identical to a [Part](/docs/reference/engine/classes/Part) with a
  [Part.Shape](/docs/reference/engine/classes/Part#Shape) of 'Cylinder'
* FileMesh - A user uploaded Mesh, equivalent to [FileMesh](/docs/reference/engine/classes/FileMesh) that
  a texture can be applied to using the [FileMesh.TextureId](/docs/reference/engine/classes/FileMesh#TextureId)
  property
* Head - A character head shape
* Sphere - A sphere shape, similar to a [Part](/docs/reference/engine/classes/Part) with a
  [Part.Shape](/docs/reference/engine/classes/Part#Shape) of 'Ball' but can be freely resized on all axis
* Wedge - A wedge shape, identical to a [WedgePart](/docs/reference/engine/classes/WedgePart)
* Torso - A block with sloped sides, due to be deprecated

Note, each MeshType will scale differently when using
[DataModelMesh.Scale](/docs/reference/engine/classes/DataModelMesh#Scale), for more information on this please see the
page on [DataModelMesh.Scale](/docs/reference/engine/classes/DataModelMesh#Scale).

Code Samples

Mesh VertexColor

In this code sample a BasePart is instanced with a SpecialMesh. The
[DataModelMesh.VertexColor](/docs/reference/engine/classes/DataModelMesh#VertexColor) property of the SpecialMesh is then
animated using TweenService.

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



mesh.VertexColor = Vector3.new(1, 1, 1)



mesh.Parent = part



-- parent part to workspace



part.Parent = workspace



-- create tweens



local tweenInfo = TweenInfo.new(1, Enum.EasingStyle.Linear, Enum.EasingDirection.Out)



local blackTween = TweenService:Create(mesh, tweenInfo, { VertexColor = Vector3.new(0, 0, 0) })



local redTween = TweenService:Create(mesh, tweenInfo, { VertexColor = Vector3.new(1, 0, 0) })



local greenTween = TweenService:Create(mesh, tweenInfo, { VertexColor = Vector3.new(0, 1, 0) })



local blueTween = TweenService:Create(mesh, tweenInfo, { VertexColor = Vector3.new(0, 0, 1) })



local resetTween = TweenService:Create(mesh, tweenInfo, { VertexColor = Vector3.new(1, 1, 1) })



-- animate



while true do



blackTween:Play()



blackTween.Completed:Wait()



redTween:Play()



redTween.Completed:Wait()



greenTween:Play()



greenTween.Completed:Wait()



blueTween:Play()



blueTween.Completed:Wait()



resetTween:Play()



resetTween.Completed:Wait()



task.wait()



end
```

Provide feedback

---