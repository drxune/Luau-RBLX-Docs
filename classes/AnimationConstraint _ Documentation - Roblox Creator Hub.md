# AnimationConstraint | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/AnimationConstraint
Scraped: 2026-01-11T02:27:25.552029Z

## Inherits
- Constraint
- AnimationConstraint
- BaseParts
- BasePart
- Instance
- Object
- Attachments
- Transform
- RunService.PreSimulation
- Animator
- AnimationConstraint.MaxForce
- AnimationConstraint.MaxTorque
- IsKinematic
- AnimationConstraint.Transform
- RunService.PreAnimation
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Constraint](/docs/reference/engine/classes/Constraint)
6. /
7. [AnimationConstraint](/docs/reference/engine/classes/AnimationConstraint)

English

Feedback

Engine Class

![AnimationConstraint](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/AnimationConstraint-Dark.webp)AnimationConstraint

Aligns two [BaseParts](/docs/reference/engine/classes/BasePart) with an animate-able kinematic or
force-based joint.

Not Browsable

---

Summary

Properties

|  |
| --- |
| [C0](#C0):[CFrame](/docs/reference/engine/datatypes/CFrame)  Deprecated |
| [C1](#C1):[CFrame](/docs/reference/engine/datatypes/CFrame)  Deprecated |
| [IsKinematic](#IsKinematic):[boolean](/docs/luau/booleans) |
| [MaxForce](#MaxForce):[number](/docs/luau/numbers) |
| [MaxTorque](#MaxTorque):[number](/docs/luau/numbers) |
| [Part0](#Part0):[BasePart](/docs/reference/engine/classes/BasePart)  Deprecated |
| [Part1](#Part1):[BasePart](/docs/reference/engine/classes/BasePart)  Deprecated |
| [Transform](#Transform):[CFrame](/docs/reference/engine/datatypes/CFrame) |

Inherited Members

8 inherited from [Constraint](/docs/reference/engine/classes/Constraint)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

An AnimationConstraint constrains its [Attachments](/docs/reference/engine/classes/Attachment) so
that they're offset by the [Transform](/docs/reference/engine/classes/AnimationConstraint#Transform)
CFrame. The [Transform](/docs/reference/engine/classes/AnimationConstraint#Transform) can be set
manually during [RunService.PreSimulation](/docs/reference/engine/classes/RunService#PreSimulation) or by an [Animator](/docs/reference/engine/classes/Animator).

---

API Reference

Properties

C0

Deprecated

Show details

---

C1

Deprecated

Show details

---

IsKinematic

Read Parallel

Toggles whether the [AnimationConstraint](/docs/reference/engine/classes/AnimationConstraint) is kinematic or physically
simulated.

AnimationConstraint.IsKinematic:[boolean](/docs/luau/booleans)

When true, the connected parts follow the
[Transform](/docs/reference/engine/classes/AnimationConstraint#Transform) perfectly without
participating in physics simulation. When false, the connected parts
follow the trajectory using forces and torques limited by
[AnimationConstraint.MaxForce](/docs/reference/engine/classes/AnimationConstraint#MaxForce) and
[AnimationConstraint.MaxTorque](/docs/reference/engine/classes/AnimationConstraint#MaxTorque).

Provide feedback

---

MaxForce

Read Parallel

Maximum force magnitude the constraint can apply to achieve its goal.

AnimationConstraint.MaxForce:[number](/docs/luau/numbers)

Maximum force magnitude the constraint can apply to achieve its goal. Only
used if [IsKinematic](/docs/reference/engine/classes/AnimationConstraint#IsKinematic) is false.

Provide feedback

---

MaxTorque

Read Parallel

Maximum torque the constraint can apply to reach its goal.

AnimationConstraint.MaxTorque:[number](/docs/luau/numbers)

Maximum torque the constraint can use to reach its goal. Only used if
[IsKinematic](/docs/reference/engine/classes/AnimationConstraint#IsKinematic) is false.

Provide feedback

---

Part0

Deprecated

Show details

---

Part1

Deprecated

Show details

---

Transform

Read Parallel

Describes the current animation offset of the [AnimationConstraint](/docs/reference/engine/classes/AnimationConstraint)
joint.

AnimationConstraint.Transform:[CFrame](/docs/reference/engine/datatypes/CFrame)

The internal [CFrame](/docs/reference/engine/datatypes/CFrame) that is manipulated when a
[AnimationConstraint](/docs/reference/engine/classes/AnimationConstraint) is being animated.

##### Timing

[AnimationConstraint](/docs/reference/engine/classes/AnimationConstraint) transforms are not applied immediately, but
rather as a batch in a parallel job after
[RunService.PreSimulation](/docs/reference/engine/classes/RunService#PreSimulation), immediately before physics steps. The
deferred batch update is much more efficient than many immediate updates.

If the [AnimationConstraint](/docs/reference/engine/classes/AnimationConstraint) is part of an animated model with an
[Animator](/docs/reference/engine/classes/Animator), then [AnimationConstraint.Transform](/docs/reference/engine/classes/AnimationConstraint#Transform) is usually
overwritten every frame by the [Animator](/docs/reference/engine/classes/Animator) after
[RunService.PreAnimation](/docs/reference/engine/classes/RunService#PreAnimation) and before
[RunService.PreSimulation](/docs/reference/engine/classes/RunService#PreSimulation).

Provide feedback

---