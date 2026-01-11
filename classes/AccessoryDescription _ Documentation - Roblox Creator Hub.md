# AccessoryDescription | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AccessoryDescription
Scraped: 2026-01-11T02:28:28.759313Z

## Inherits
- Instance
- AccessoryDescription
- Accessory
- HumanoidDescription
- Object
- Humanoid:ApplyDescription()
- AssetId
- WrapLayer.Order
- WrapLayer.Puffiness
- Humanoid
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [AccessoryDescription](/docs/reference/engine/classes/AccessoryDescription)

English

Feedback

Engine Class

![AccessoryDescription](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/HumanoidDescription-Dark.webp)AccessoryDescription

Describes the appearance of an [Accessory](/docs/reference/engine/classes/Accessory) for the
[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).

---

Summary

Properties

|  |
| --- |
| [AccessoryType](#AccessoryType):[Enum.AccessoryType](/docs/reference/engine/enums/AccessoryType) |
| [AssetId](#AssetId):[number](/docs/luau/numbers) |
| [Instance](#Instance):[Instance](/docs/reference/engine/datatypes/Instance) |
| [IsLayered](#IsLayered):[boolean](/docs/luau/booleans) |
| [Order](#Order):[number](/docs/luau/numbers) |
| [Position](#Position):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Puffiness](#Puffiness):[number](/docs/luau/numbers) |
| [Rotation](#Rotation):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Scale](#Scale):[Vector3](/docs/reference/engine/datatypes/Vector3) |

Methods

|  |
| --- |
| [GetAppliedInstance](#GetAppliedInstance)():[Instance](/docs/reference/engine/datatypes/Instance) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

AccessoryDescription is an object that stores the description for an
[Accessory](/docs/reference/engine/classes/Accessory). It is meant to be placed underneath a
[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) in order to work with
[Humanoid:ApplyDescription()](/docs/reference/engine/classes/Humanoid#ApplyDescription).

---

API Reference

Properties

AccessoryType

Read Parallel

The [Enum.AccessoryType](/docs/reference/engine/enums/AccessoryType) of the [Accessory](/docs/reference/engine/classes/Accessory) referred to by this
description.

AccessoryDescription.AccessoryType:[Enum.AccessoryType](/docs/reference/engine/enums/AccessoryType)

The [Enum.AccessoryType](/docs/reference/engine/enums/AccessoryType) of the [Accessory](/docs/reference/engine/classes/Accessory) referred to by this
description.

Provide feedback

---

AssetId

Read Parallel

The asset ID that should be applied when applying this
[AccessoryDescription](/docs/reference/engine/classes/AccessoryDescription).

AccessoryDescription.AssetId:[number](/docs/luau/numbers)

The asset ID that should be applied when applying this
[AccessoryDescription](/docs/reference/engine/classes/AccessoryDescription).

Provide feedback

---

Instance

Read Parallel

A reference to the [Instance](/docs/reference/engine/classes/Instance) that should be applied when applying
this [AccessoryDescription](/docs/reference/engine/classes/AccessoryDescription).

AccessoryDescription.Instance:[Instance](/docs/reference/engine/datatypes/Instance)

A reference to the [Instance](/docs/reference/engine/classes/Instance) that should be applied when applying
this [AccessoryDescription](/docs/reference/engine/classes/AccessoryDescription). This property can be used instead of
[AssetId](/docs/reference/engine/classes/AccessoryDescription#AssetId) to apply accessories without
uploading them to the platform.

Provide feedback

---

IsLayered

Read Parallel

Whether the [Accessory](/docs/reference/engine/classes/Accessory) is layered or rigid.

AccessoryDescription.IsLayered:[boolean](/docs/luau/booleans)

Whether the [Accessory](/docs/reference/engine/classes/Accessory) is layered or rigid. This will be updated
after calling [Humanoid:ApplyDescription()](/docs/reference/engine/classes/Humanoid#ApplyDescription) if this property doesn't
match the actual [Accessory](/docs/reference/engine/classes/Accessory) contents.

Provide feedback

---

Order

Read Parallel

The layered clothing sort order, if the [Accessory](/docs/reference/engine/classes/Accessory) is layered.

AccessoryDescription.Order:[number](/docs/luau/numbers)

The [WrapLayer.Order](/docs/reference/engine/classes/WrapLayer#Order) value when applying the [Accessory](/docs/reference/engine/classes/Accessory), if
it is layered.

Provide feedback

---

Position

Read Parallel

The accessory adjustment position offset, if the [Accessory](/docs/reference/engine/classes/Accessory) is
rigid.

AccessoryDescription.Position:[Vector3](/docs/reference/engine/datatypes/Vector3)

The accessory adjustment position offset. Only applies if the
[Accessory](/docs/reference/engine/classes/Accessory) is rigid.

Provide feedback

---

Puffiness

Read Parallel

The layered clothing puffiness, if the [Accessory](/docs/reference/engine/classes/Accessory) is layered.

AccessoryDescription.Puffiness:[number](/docs/luau/numbers)

The [WrapLayer.Puffiness](/docs/reference/engine/classes/WrapLayer#Puffiness) value when applying the [Accessory](/docs/reference/engine/classes/Accessory),
if it is layered.

Provide feedback

---

Rotation

Read Parallel

The accessory adjustment rotation offset, if the [Accessory](/docs/reference/engine/classes/Accessory) is
rigid.

AccessoryDescription.Rotation:[Vector3](/docs/reference/engine/datatypes/Vector3)

The accessory adjustment rotation offset. Only applies if the
[Accessory](/docs/reference/engine/classes/Accessory) is rigid.

Provide feedback

---

Scale

Read Parallel

The accessory adjustment scale, if the [Accessory](/docs/reference/engine/classes/Accessory) is rigid.

AccessoryDescription.Scale:[Vector3](/docs/reference/engine/datatypes/Vector3)

The accessory adjustment scale. Only applies if the [Accessory](/docs/reference/engine/classes/Accessory) is
rigid.

Provide feedback

---

Methods

GetAppliedInstance

Returns the applied [Accessory](/docs/reference/engine/classes/Accessory).

AccessoryDescription:GetAppliedInstance():[Instance](/docs/reference/engine/datatypes/Instance)

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

Returns the applied [Accessory](/docs/reference/engine/classes/Accessory) if this [AccessoryDescription](/docs/reference/engine/classes/AccessoryDescription)
is the child of an applied [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) parented to a
[Humanoid](/docs/reference/engine/classes/Humanoid).

Provide feedback

---