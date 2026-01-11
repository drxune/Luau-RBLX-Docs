# BodyPartDescription | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BodyPartDescription
Scraped: 2026-01-11T02:36:08.897293Z

## Inherits
- Instance
- BodyPartDescription
- HumanoidDescription
- Object
- Color
- Humanoid:ApplyDescription()
- AssetId
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [BodyPartDescription](/docs/reference/engine/classes/BodyPartDescription)

English

Feedback

Engine Class

BodyPartDescription

Describes the appearance of an avatar body part for the
[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).

---

Summary

Properties

|  |
| --- |
| [AssetId](#AssetId):[number](/docs/luau/numbers) |
| [BodyPart](#BodyPart):[Enum.BodyPart](/docs/reference/engine/enums/BodyPart) |
| [Color](#Color):[Color3](/docs/reference/engine/datatypes/Color3) |
| [HeadShape](#HeadShape):[string](/docs/luau/strings) |
| [Instance](#Instance):[Instance](/docs/reference/engine/datatypes/Instance) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

BodyPartDescription is an object that stores the description for an
avatar's body parts, such as the [Color](/docs/reference/engine/classes/BodyPartDescription#Color). It
is meant to be placed underneath a [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) in order to
work with [Humanoid:ApplyDescription()](/docs/reference/engine/classes/Humanoid#ApplyDescription).

---

API Reference

Properties

AssetId

Read Parallel

The asset ID that should be applied when applying this
[BodyPartDescription](/docs/reference/engine/classes/BodyPartDescription).

BodyPartDescription.AssetId:[number](/docs/luau/numbers)

The asset ID that should be applied when applying this
[BodyPartDescription](/docs/reference/engine/classes/BodyPartDescription).

Provide feedback

---

BodyPart

Read Parallel

The type of body part.

BodyPartDescription.BodyPart:[Enum.BodyPart](/docs/reference/engine/enums/BodyPart)

The type of body part.

Provide feedback

---

Color

Read Parallel

The [Color3](/docs/reference/engine/datatypes/Color3) for this body part.

BodyPartDescription.Color:[Color3](/docs/reference/engine/datatypes/Color3)

The [Color3](/docs/reference/engine/datatypes/Color3) for this body part.

Provide feedback

---

HeadShape

Read Parallel

BodyPartDescription.HeadShape:[string](/docs/luau/strings)

Provide feedback

---

Instance

Read Parallel

A reference to the [Instance](/docs/reference/engine/classes/Instance) that should be applied when applying
this [BodyPartDescription](/docs/reference/engine/classes/BodyPartDescription).

BodyPartDescription.Instance:[Instance](/docs/reference/engine/datatypes/Instance)

A reference to the [Instance](/docs/reference/engine/classes/Instance) that should be applied when applying
this [BodyPartDescription](/docs/reference/engine/classes/BodyPartDescription). This property can be used instead of
[AssetId](/docs/reference/engine/classes/BodyPartDescription#AssetId) to apply accessories without
uploading them to the platform. This can reference either a body part with
R15, R15ArtistIntent and R6 folders, or only reference a single
subfolder.

Provide feedback

---