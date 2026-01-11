# Bone | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Bone
Scraped: 2026-01-11T02:31:02.691538Z

## Tags
- Not Replicated

## Inherits
- Attachment
- Bone
- Instance
- Object
- Model
- MeshPart
- Bones
- Motor6D
- Bone.Transform
- Motor6D.Transform
- CFrame
- Attachments
- WorldCFrame
- TransformedCFrame
- TransformedWorldCFrame
- Transform
- Bone.TransformedWorldCFrame
- Bone.TransformedCFrame
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Attachment](/docs/reference/engine/classes/Attachment)
6. /
7. [Bone](/docs/reference/engine/classes/Bone)

English

Feedback

Engine Class

![Bone](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Bone-Dark.webp)Bone

Bones are non-rendered objects that drive the movement of one or more parts
for the purposes of animation, or creating clothing and characters.

---

Summary

Properties

|  |
| --- |
| [Transform](#Transform):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [TransformedCFrame](#TransformedCFrame):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [TransformedWorldCFrame](#TransformedWorldCFrame):[CFrame](/docs/reference/engine/datatypes/CFrame) |

Inherited Members

18 inherited from [Attachment](/docs/reference/engine/classes/Attachment)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Bones are non-rendered objects that drive the movement of one or more parts
for the purposes of animation, or creating clothing and characters. Bones are
part of a [Model](/docs/reference/engine/classes/Model) or [MeshPart](/docs/reference/engine/classes/MeshPart) object's skeletal rig that you
typically access and animate through the
[Animation Editor](/docs/animation/editor).

Rigs are created during the modeling process in third-party software such as
Blender or Maya. After importing the rigged model into Studio, you can add the
model directly to your experience, or save and share the model as an asset.
See [Rigging](/docs/art/modeling/rigging) for more details on creating
and using rigged models.

Note that you can parent [Bones](/docs/reference/engine/classes/Bone) under other [Bones](/docs/reference/engine/classes/Bone) and
parts. When parenting a bone to another bone, the child bone's world position
will be relative to the parent bone's position, and the hierarchy of parented
[Bone](/docs/reference/engine/classes/Bone) objects can change the behavior of affected parts during posing
or animation.

##### Relationship with Motor6D

To support animations with older rigs using joints, such as [Motor6D](/docs/reference/engine/classes/Motor6D),
you can use the [Bone.Transform](/docs/reference/engine/classes/Bone#Transform) property in the same way as
[Motor6D.Transform](/docs/reference/engine/classes/Motor6D#Transform). Roblox uses the offset of the bones from the
default pose to drive an animation, and bones are not replicated or
serialized.

##### Bone.CFrame

Bones inherit the [CFrame](/docs/reference/engine/classes/Attachment#CFrame) property of
[Attachments](/docs/reference/engine/classes/Attachment) which Roblox uses as the bone's reference
position. The inherited [WorldCFrame](/docs/reference/engine/classes/Attachment#WorldCFrame) and other
world properties return the initial un-transformed position.

---

API Reference

Properties

Transform

Not Replicated

Read Parallel

Determines the current animated offset of the bone in its local space.

Bone.Transform:[CFrame](/docs/reference/engine/datatypes/CFrame)

Transform determines the current animated offset of the bone relative
to its [CFrame](/docs/reference/engine/classes/Attachment#CFrame). This property is set by Roblox
when animations on skinned meshes are played, although it can be
manipulated manually in a manner similar to [Motor6D.Transform](/docs/reference/engine/classes/Motor6D#Transform).

See also:

* [Motor6D.Transform](/docs/reference/engine/classes/Motor6D#Transform), a property which plays a similar role in
  character rig animation
* [TransformedCFrame](/docs/reference/engine/classes/Bone#TransformedCFrame) and
  [TransformedWorldCFrame](/docs/reference/engine/classes/Bone#TransformedWorldCFrame), whose values
  are partially determined by this property

Provide feedback

---

TransformedCFrame

Hidden

Read Only

Not Replicated

Read Parallel

Describes the combined [CFrame](/docs/reference/engine/classes/Attachment#CFrame) offset of the bone
and the current animation offset in the bone local space.

Bone.TransformedCFrame:[CFrame](/docs/reference/engine/datatypes/CFrame)

TransformedCFrame describes the combined
[CFrame](/docs/reference/engine/classes/Attachment#CFrame) offset of the bone and the current
animation offset ([Transform](/docs/reference/engine/classes/Bone#Transform)) in the bone's local
space.

See also:

* [Transform](/docs/reference/engine/classes/Bone#Transform), a property which partially determines
  this property's value
* [Bone.TransformedWorldCFrame](/docs/reference/engine/classes/Bone#TransformedWorldCFrame), a world-space variant of this
  property

Provide feedback

---

TransformedWorldCFrame

Read Only

Not Replicated

Describes the combined [CFrame](/docs/reference/engine/classes/Attachment#CFrame) offset of the bone
and the current animation offset in world space.

Bone.TransformedWorldCFrame:[CFrame](/docs/reference/engine/datatypes/CFrame)

TransformedWorldCFrame describes the combined
[CFrame](/docs/reference/engine/classes/Attachment#CFrame) offset of the bone and the current
animation offset ([Transform](/docs/reference/engine/classes/Bone#Transform)) in world space.

See also:

* [Transform](/docs/reference/engine/classes/Bone#Transform), a property which partially determines
  this property's value
* [Bone.TransformedCFrame](/docs/reference/engine/classes/Bone#TransformedCFrame), a local-space variant of this property

Provide feedback

---