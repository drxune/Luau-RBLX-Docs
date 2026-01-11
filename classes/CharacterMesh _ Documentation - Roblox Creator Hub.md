# CharacterMesh | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/CharacterMesh
Scraped: 2026-01-11T02:28:39.552057Z

## Inherits
- CharacterAppearance
- CharacterMesh
- Instance
- Object
- CharacterMesh.OverlayTextureId
- CharacterMesh.BaseTextureId
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [CharacterAppearance](/docs/reference/engine/classes/CharacterAppearance)
6. /
7. [CharacterMesh](/docs/reference/engine/classes/CharacterMesh)

English

Feedback

Engine Class

![CharacterMesh](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/CharacterMesh-Dark.webp)CharacterMesh

Modifies the appearance of an R6 body part.

---

Summary

Properties

|  |
| --- |
| [BaseTextureId](#BaseTextureId):[number](/docs/luau/numbers) |
| [BodyPart](#BodyPart):[Enum.BodyPart](/docs/reference/engine/enums/BodyPart) |
| [MeshId](#MeshId):[number](/docs/luau/numbers) |
| [OverlayTextureId](#OverlayTextureId):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

This property modifies the appearance of an R6 body part. It has no effect in
R15 characters.

---

API Reference

Properties

BaseTextureId

Read Parallel

The texture of a CharacterMesh. It can be overridden by Shirts, Pants,
T-Shirts, and the [CharacterMesh.OverlayTextureId](/docs/reference/engine/classes/CharacterMesh#OverlayTextureId) property.

CharacterMesh.BaseTextureId:[number](/docs/luau/numbers)

The texture of a CharacterMesh. It can be overridden by Shirts, Pants,
T-Shirts, and the [CharacterMesh.OverlayTextureId](/docs/reference/engine/classes/CharacterMesh#OverlayTextureId) property.

Provide feedback

---

BodyPart

Read Parallel

The part of the Character's body that is affected.

CharacterMesh.BodyPart:[Enum.BodyPart](/docs/reference/engine/enums/BodyPart)

The part of the Character's body that is affected.

Provide feedback

---

MeshId

Read Parallel

Used to load a mesh file, and apply it to the given BodyPart.

CharacterMesh.MeshId:[number](/docs/luau/numbers)

Used to load a mesh file, and apply it to the given BodyPart.

Provide feedback

---

OverlayTextureId

Read Parallel

The assetId of the overlay texture. The overlay covers Shirts, Pants,
T-Shirts, and the [CharacterMesh.BaseTextureId](/docs/reference/engine/classes/CharacterMesh#BaseTextureId).

CharacterMesh.OverlayTextureId:[number](/docs/luau/numbers)

The assetId of the overlay texture. The overlay covers Shirts, Pants,
T-Shirts, and the [CharacterMesh.BaseTextureId](/docs/reference/engine/classes/CharacterMesh#BaseTextureId).

Provide feedback

---