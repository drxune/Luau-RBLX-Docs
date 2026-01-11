# Motor6D | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Motor6D
Scraped: 2026-01-11T02:27:14.060475Z

## Tags
- Not Replicated

## Inherits
- Motor
- Motor6D
- BaseParts
- JointInstance
- Instance
- Object
- Part0
- Part1
- Transform
- RunService.PreSimulation
- Animator
- Humanoids
- JointInstance.C0
- JointInstance.C1
- C0
- C1
- Motor6D.Transform
- RunService.PreAnimation
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Motor](/docs/reference/engine/classes/Motor)
6. /
7. [Motor6D](/docs/reference/engine/classes/Motor6D)

English

Feedback

Engine Class

![Motor6D](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Motor6D-Dark.webp)Motor6D

Creates an animatable joint between two [BaseParts](/docs/reference/engine/classes/BasePart).

---

Summary

Properties

|  |
| --- |
| [ChildName](#ChildName):[string](/docs/luau/strings) |
| [ParentName](#ParentName):[string](/docs/luau/strings) |
| [Transform](#Transform):[CFrame](/docs/reference/engine/datatypes/CFrame) |

Inherited Members

4 inherited from [Motor](/docs/reference/engine/classes/Motor)

7 inherited from [JointInstance](/docs/reference/engine/classes/JointInstance)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Motor6D joins two [BaseParts](/docs/reference/engine/classes/BasePart)
([Part0](/docs/reference/engine/classes/JointInstance#Part0) and [Part1](/docs/reference/engine/classes/JointInstance#Part1))
together in an animatable way. The [Transform](/docs/reference/engine/classes/Motor6D#Transform)
property determines the offset between these parts. This can be set manually
using [RunService.PreSimulation](/docs/reference/engine/classes/RunService#PreSimulation) or through an [Animator](/docs/reference/engine/classes/Animator).

Models whose parts are joined by [Motor6D](/docs/reference/engine/classes/Motor6D) are usually referred to as
rigs, typically for [Humanoids](/docs/reference/engine/classes/Humanoid).

---

API Reference

Properties

ChildName

Read Only

Not Replicated

Not Scriptable

Read Parallel

Motor6D.ChildName:[string](/docs/luau/strings)

Provide feedback

---

ParentName

Read Only

Not Replicated

Not Scriptable

Read Parallel

Motor6D.ParentName:[string](/docs/luau/strings)

Provide feedback

---

Transform

Hidden

Not Replicated

Read Parallel

Describes the current animation offset of the [Motor6D](/docs/reference/engine/classes/Motor6D) joint.

Motor6D.Transform:[CFrame](/docs/reference/engine/datatypes/CFrame)

The internal [CFrame](/docs/reference/engine/datatypes/CFrame) that is manipulated when a [Motor6D](/docs/reference/engine/classes/Motor6D)
is being animated. It is recommended to use this property for custom
animations rather than [JointInstance.C0](/docs/reference/engine/classes/JointInstance#C0) and
[JointInstance.C1](/docs/reference/engine/classes/JointInstance#C1).

##### Timing

[Motor6D](/docs/reference/engine/classes/Motor6D) transforms are not applied immediately, unlike updating
[C0](/docs/reference/engine/classes/JointInstance#C0) and [C1](/docs/reference/engine/classes/JointInstance#C1), but rather as
a batch in a parallel job after [RunService.PreSimulation](/docs/reference/engine/classes/RunService#PreSimulation),
immediately before physics steps. The deferred batch update is much more
efficient than many immediate updates.

If the [Motor6D](/docs/reference/engine/classes/Motor6D) is part of an animated model with an
[Animator](/docs/reference/engine/classes/Animator), then [Motor6D.Transform](/docs/reference/engine/classes/Motor6D#Transform) will usually be
overwritten every frame by the [Animator](/docs/reference/engine/classes/Animator) after
[RunService.PreAnimation](/docs/reference/engine/classes/RunService#PreAnimation) and before
[RunService.PreSimulation](/docs/reference/engine/classes/RunService#PreSimulation).

Provide feedback

---