# FileMesh | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/FileMesh
Scraped: 2026-01-11T02:34:45.104333Z

## Inherits
- DataModelMesh
- FileMesh
- BasePart
- SpecialMesh
- Instance
- Object
- FileMesh.MeshId
- FileMesh.TextureId
- SpecialMesh.MeshType
- DataModelMesh.Scale
- DataModelMesh.Offset
- DataModelMesh.VertexColor
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [DataModelMesh](/docs/reference/engine/classes/DataModelMesh)
6. /
7. [FileMesh](/docs/reference/engine/classes/FileMesh)

English

Feedback

Engine Class

FileMesh

The FileMesh object applies a mesh to a [BasePart](/docs/reference/engine/classes/BasePart) when parented to it.
Its properties are inherited by the [SpecialMesh](/docs/reference/engine/classes/SpecialMesh) object.

---

Summary

Properties

|  |
| --- |
| [MeshId](#MeshId):ContentId |
| [TextureId](#TextureId):ContentId |

Inherited Members

3 inherited from [DataModelMesh](/docs/reference/engine/classes/DataModelMesh)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[SpecialMesh](/docs/reference/engine/classes/SpecialMesh)

The FileMesh object applies a textured mesh to a [BasePart](/docs/reference/engine/classes/BasePart) when
parented to it. Its properties are inherited by the [SpecialMesh](/docs/reference/engine/classes/SpecialMesh)
object.

What is a FileMesh?
-------------------

FileMeshes allow user uploaded meshes to be applied to a [BasePart](/docs/reference/engine/classes/BasePart). The
mesh that is applied is dependent on the [FileMesh.MeshId](/docs/reference/engine/classes/FileMesh#MeshId) property. A
texture can also be applied to this mesh using [FileMesh.TextureId](/docs/reference/engine/classes/FileMesh#TextureId).

Although it is not an abstract class, and can be used by developers, all
[FileMesh](/docs/reference/engine/classes/FileMesh) properties are inherited by the [SpecialMesh](/docs/reference/engine/classes/SpecialMesh) object. A
[SpecialMesh](/docs/reference/engine/classes/SpecialMesh) behaves identically to the FileMesh object when its
[SpecialMesh.MeshType](/docs/reference/engine/classes/SpecialMesh#MeshType) is set to 'FileMesh'. Although both objects are
functional, the [SpecialMesh](/docs/reference/engine/classes/SpecialMesh) object is the official supported class.

For more information on using meshes, please see the [SpecialMesh](/docs/reference/engine/classes/SpecialMesh) page.

Code Samples

FileMesh Offset and Scale

In this code sample a BasePart is instanced with a FileMesh. The
[DataModelMesh.Scale](/docs/reference/engine/classes/DataModelMesh#Scale) and [DataModelMesh.Offset](/docs/reference/engine/classes/DataModelMesh#Offset) properties of the
FileMesh are then animated using TweenService.

```
local TweenService = game:GetService("TweenService")



local part = Instance.new("Part")



part.Size = Vector3.new(4, 8, 4)



part.Position = Vector3.new(0, 4, 0)



part.Anchored = true



part.CanCollide = false



local mesh = Instance.new("FileMesh") -- advised to use SpecialMesh instead



mesh.MeshId = "rbxassetid://1086413449"



mesh.TextureId = "rbxassetid://1461576423"



mesh.Offset = Vector3.new(0, 0, 0)



mesh.Scale = Vector3.new(4, 4, 4)



mesh.Parent = part



local box = Instance.new("SelectionBox")



box.Adornee = part



box.Parent = part



part.Parent = workspace



local tween = TweenService:Create(



mesh,



TweenInfo.new(1, Enum.EasingStyle.Linear, Enum.EasingDirection.Out, -1, true, 0),



{ Scale = Vector3.new(1, 1, 1), Offset = Vector3.new(0, 3, 0) }



)



tween:Play()
```

---

API Reference

Properties

MeshId

Read Parallel

The MeshId is the content ID of the mesh that is to be displayed.

FileMesh.MeshId:ContentId

The MeshId is the content ID of the mesh that is to be displayed.

The content ID for a mesh is generated when a developer uploads a mesh to
Roblox.

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

TextureId

Read Parallel

The TextureId is the content ID of the texture that is to be applied to
the mesh.

FileMesh.TextureId:ContentId

The TextureId is the content ID of the image that is to be applied to used
for the meshes texture. When the TextureId property is set to an empty
string, no texture will be applied to the mesh.

#### How can I change the texture of a mesh?

Using the TextureId property, the texture of a mesh can be changed without
having to reupload the mesh. To do this, a new image will need to be
uploaded to Roblox with the desired texture. The original texture image
file can be obtained by exporting the mesh using the 'Export Selection'
option in Roblox Studio. The image file will be saved alongside the
exported .obj file.

The new texture can then be re-uploaded to Roblox as a Decal and its
content ID can be applied to the mesh using the TextureId property.

#### How can I make a textured mesh?

A mesh can only be textured if the mesh has been UV mapped. UV mapping
refers to the practice of projecting a texture map onto a mesh. This
cannot be done using Roblox Studio and has to be done using an external 3D
modelling application such as [Blender](https://www.blender.org/).

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