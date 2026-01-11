# Attachment | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Attachment
Scraped: 2026-01-11T02:37:47.033466Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- Attachment
- PVInstance
- Bone
- CFrame
- WorldCFrame
- Constraints
- BasePart
- ParticleEmitters
- PointLight
- SpotLight
- AudioEmitter
- Position
- Rotation
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Attachment](/docs/reference/engine/classes/Attachment)

English

Feedback

Engine Class

![Attachment](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Attachment-Dark.webp)Attachment

Defines a point and orientation relative to an ancestor [PVInstance](/docs/reference/engine/classes/PVInstance),
[Bone](/docs/reference/engine/classes/Bone), or another [Attachment](/docs/reference/engine/classes/Attachment).

---

Summary

Properties

|  |
| --- |
| [Axis](#Axis):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [CFrame](#CFrame):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [Orientation](#Orientation):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Position](#Position):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Rotation](#Rotation):[Vector3](/docs/reference/engine/datatypes/Vector3)  Deprecated |
| [SecondaryAxis](#SecondaryAxis):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Visible](#Visible):[boolean](/docs/luau/booleans) |
| [WorldAxis](#WorldAxis):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [WorldCFrame](#WorldCFrame):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [WorldOrientation](#WorldOrientation):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [WorldPosition](#WorldPosition):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [WorldRotation](#WorldRotation):[Vector3](/docs/reference/engine/datatypes/Vector3)  Deprecated |
| [WorldSecondaryAxis](#WorldSecondaryAxis):[Vector3](/docs/reference/engine/datatypes/Vector3) |

Methods

|  |
| --- |
| [GetAxis](#GetAxis)():[Vector3](/docs/reference/engine/datatypes/Vector3)  Deprecated |
| [GetConstraints](#GetConstraints)():Instances |
| [GetSecondaryAxis](#GetSecondaryAxis)():[Vector3](/docs/reference/engine/datatypes/Vector3)  Deprecated |
| [SetAxis](#SetAxis)(axis: [Vector3](/docs/reference/engine/datatypes/Vector3)):()  Deprecated |
| [SetSecondaryAxis](#SetSecondaryAxis)(axis: [Vector3](/docs/reference/engine/datatypes/Vector3)):()  Deprecated |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[Bone](/docs/reference/engine/classes/Bone)

An Attachment defines a point and orientation relative to an ancestor
[PVInstance](/docs/reference/engine/classes/PVInstance), [Bone](/docs/reference/engine/classes/Bone), or another Attachment. The offset is
stored in the [CFrame](/docs/reference/engine/classes/Attachment#CFrame) property. The offset can also
be set through other properties, such as
[WorldCFrame](/docs/reference/engine/classes/Attachment#WorldCFrame).

If no ancestral [PVInstance](/docs/reference/engine/classes/PVInstance) or [Attachment](/docs/reference/engine/classes/Attachment) exists, then
[CFrame](/docs/reference/engine/classes/Attachment#CFrame) and
[WorldCFrame](/docs/reference/engine/classes/Attachment#WorldCFrame) are the same.

Attachments are used by several kinds of [Constraints](/docs/reference/engine/classes/Constraint) and
are also valid alternatives to [BasePart](/docs/reference/engine/classes/BasePart) as a parent for objects such
as:

* [ParticleEmitters](/docs/reference/engine/classes/ParticleEmitter) which will emit particles from the
  attachment's specific position/orientation instead of the [BasePart](/docs/reference/engine/classes/BasePart)
  bounds.
* Light-emitting objects like [PointLight](/docs/reference/engine/classes/PointLight) and [SpotLight](/docs/reference/engine/classes/SpotLight) which
  will shine from the attachment's position/orientation instead of the
  [BasePart](/docs/reference/engine/classes/BasePart) center.
* [AudioEmitter](/docs/reference/engine/classes/AudioEmitter) which will use the attachment's position as the audio's
  point of emission.

---

API Reference

Properties

Axis

Not Replicated

Read Parallel

Direction of the X axis of the attachment, represented as a unit
[Vector3](/docs/reference/engine/datatypes/Vector3).

Attachment.Axis:[Vector3](/docs/reference/engine/datatypes/Vector3)

Direction of the X axis of the attachment, represented as a unit
[Vector3](/docs/reference/engine/datatypes/Vector3).

Provide feedback

---

CFrame

Read Parallel

[CFrame](/docs/reference/engine/datatypes/CFrame) offset of the attachment.

Attachment.CFrame:[CFrame](/docs/reference/engine/datatypes/CFrame)

The [CFrame](/docs/reference/engine/datatypes/CFrame) offset of the attachment. Changes to this property
will reflect onto the [Position](/docs/reference/engine/classes/Attachment#Position) and
[Rotation](/docs/reference/engine/classes/Attachment#Rotation) properties of this object. Similarly,
a change to either of those properties will reflect onto this property.

Provide feedback

---

Orientation

Hidden

Not Replicated

Read Parallel

Orientation of the attachment relative to the orientation of its parent.

Attachment.Orientation:[Vector3](/docs/reference/engine/datatypes/Vector3)

Orientation of the attachment relative to the orientation of its parent.
Rotations are in Z, X, Y order.

Provide feedback

---

Position

Hidden

Not Replicated

Read Parallel

Positional offset of the attachment, relative to the position and
orientation of its parent.

Attachment.Position:[Vector3](/docs/reference/engine/datatypes/Vector3)

Positional offset of the attachment, relative to the position and
orientation of its parent.

Provide feedback

---

Rotation

Deprecated

Show details

---

SecondaryAxis

Not Replicated

Read Parallel

Direction of the Y axis of the attachment, represented as a unit
[Vector3](/docs/reference/engine/datatypes/Vector3).

Attachment.SecondaryAxis:[Vector3](/docs/reference/engine/datatypes/Vector3)

Direction of the Y axis of the attachment, represented as a unit
[Vector3](/docs/reference/engine/datatypes/Vector3).

Provide feedback

---

Visible

Read Parallel

Toggles the in-experience visibility of the attachment.

Attachment.Visible:[boolean](/docs/luau/booleans)

Toggles the in-experience visibility of the attachment.

Provide feedback

---

WorldAxis

Not Replicated

Read Parallel

Direction of the X axis of the attachment relative to the world,
represented as a unit [Vector3](/docs/reference/engine/datatypes/Vector3) with a length of 1.

Attachment.WorldAxis:[Vector3](/docs/reference/engine/datatypes/Vector3)

Direction of the X axis of the attachment relative to the world,
represented as a unit [Vector3](/docs/reference/engine/datatypes/Vector3) with a length of 1.

Provide feedback

---

WorldCFrame

Not Replicated

Read Parallel

The exact [CFrame](/docs/reference/engine/datatypes/CFrame) of the attachment in world space coordinates.

Attachment.WorldCFrame:[CFrame](/docs/reference/engine/datatypes/CFrame)

The exact [CFrame](/docs/reference/engine/datatypes/CFrame) of the attachment in world space coordinates,
independent of its parent. The value of this property is equivalent to
multiplying the [CFrame](/docs/reference/engine/datatypes/CFrame) of the attachment's parent by its own
[CFrame](/docs/reference/engine/datatypes/CFrame).

Provide feedback

---

WorldOrientation

Hidden

Not Replicated

Read Parallel

Orientation of the attachment relative to the world rather than its own
parent.

Attachment.WorldOrientation:[Vector3](/docs/reference/engine/datatypes/Vector3)

Orientation of the attachment relative to the world rather than its own
parent. Rotations are in Z, X, Y order.

Provide feedback

---

WorldPosition

Hidden

Not Replicated

Read Parallel

Position of the attachment relative to the world rather than its own
parent.

Attachment.WorldPosition:[Vector3](/docs/reference/engine/datatypes/Vector3)

Position of the attachment relative to the world rather than its own
parent.

Provide feedback

---

WorldRotation

Deprecated

Show details

---

WorldSecondaryAxis

Not Replicated

Read Parallel

Direction of the Y axis of the attachment relative to the world,
represented as a unit [Vector3](/docs/reference/engine/datatypes/Vector3) with a length of 1.

Attachment.WorldSecondaryAxis:[Vector3](/docs/reference/engine/datatypes/Vector3)

Direction of the Y axis of the attachment relative to the world,
represented as a unit [Vector3](/docs/reference/engine/datatypes/Vector3) with a length of 1.

Provide feedback

---

Methods

GetAxis

Deprecated

Show details

---

GetConstraints

Returns a list of [Constraints](/docs/reference/engine/classes/Constraint) connected to the
attachment.

Attachment:GetConstraints():Instances

Returns

Instances

Returns a list of [Constraints](/docs/reference/engine/classes/Constraint) connected to the
attachment.

Provide feedback

---

GetSecondaryAxis

Deprecated

Show details

---

SetAxis

Deprecated

Show details

---

SetSecondaryAxis

Deprecated

Show details

---