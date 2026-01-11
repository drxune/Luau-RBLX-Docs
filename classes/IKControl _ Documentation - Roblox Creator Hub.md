# IKControl | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/IKControl
Scraped: 2026-01-11T02:39:01.674278Z

## Inherits
- Object
- Instance
- IKControl
- IKControls
- Humanoid
- AnimationController
- Animator
- Type
- EndEffector
- Target
- ChainRoot
- Enabled
- Weight
- BasePart
- Bone
- Motor6D
- Attachment
- Attachments
- EndEffectorOffset
- Pole
- Offset
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [IKControl](/docs/reference/engine/classes/IKControl)

English

Feedback

Engine Class

![IKControl](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/IKControl-Dark.webp)IKControl

Specifies a control to generate a procedural animation pose using Inverse
Kinematics.

---

Summary

Properties

|  |
| --- |
| [ChainRoot](#ChainRoot):[Instance](/docs/reference/engine/datatypes/Instance) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [EndEffector](#EndEffector):[Instance](/docs/reference/engine/datatypes/Instance) |
| [EndEffectorOffset](#EndEffectorOffset):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [Offset](#Offset):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [Pole](#Pole):[Instance](/docs/reference/engine/datatypes/Instance) |
| [Priority](#Priority):[number](/docs/luau/numbers) |
| [SmoothTime](#SmoothTime):[number](/docs/luau/numbers) |
| [Target](#Target):[Instance](/docs/reference/engine/datatypes/Instance) |
| [Type](#Type):[Enum.IKControlType](/docs/reference/engine/enums/IKControlType) |
| [Weight](#Weight):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [GetChainCount](#GetChainCount)():[number](/docs/luau/numbers) |
| [GetChainLength](#GetChainLength)():[number](/docs/luau/numbers) |
| [GetNodeLocalCFrame](#GetNodeLocalCFrame)(index: [number](/docs/luau/numbers)):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [GetNodeWorldCFrame](#GetNodeWorldCFrame)(index: [number](/docs/luau/numbers)):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [GetRawFinalTarget](#GetRawFinalTarget)():[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [GetSmoothedFinalTarget](#GetSmoothedFinalTarget)():[CFrame](/docs/reference/engine/datatypes/CFrame) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

IKControl instances generate procedural animation poses using Inverse
Kinematics (IK). They allow you to make characters respond realistically to
their environment.

For example, you can make a character place its hand on a door handle exactly,
and the character will do so independently of its position.
[IKControls](/docs/reference/engine/classes/IKControl) provide the advantage of needing to create much
fewer animations for your game while giving your experience a more realistic
and polished feel.

[IKControls](/docs/reference/engine/classes/IKControl) must be a child of a [Humanoid](/docs/reference/engine/classes/Humanoid) or
[AnimationController](/docs/reference/engine/classes/AnimationController) with an [Animator](/docs/reference/engine/classes/Animator) and have all of their
required properties set properly, otherwise they don't have any effect. The
required properties are [Type](/docs/reference/engine/classes/IKControl#Type),
[EndEffector](/docs/reference/engine/classes/IKControl#EndEffector), [Target](/docs/reference/engine/classes/IKControl#Target),
[ChainRoot](/docs/reference/engine/classes/IKControl#ChainRoot). As soon as those are set, the
[IKControl](/docs/reference/engine/classes/IKControl) modifies the pose of your character as you specify. The
following code sample demonstrates how to set up your first [IKControl](/docs/reference/engine/classes/IKControl)
and get started with creating more realistic animations for your game.

You can use [IKControls](/docs/reference/engine/classes/IKControl) to make a character:

* Rotate its head and torso to look at a point of interest in the world.
* Modify its feet positions to respond to dynamic terrain. Adjust its legs and
  feet to place them accordingly on terrain with rocks and slopes.
* Hold a gun and place its hands appropriately on the grip without needing to
  create animations for each gun in the game.
* Aim at a point in the world, so that the tip of the gun point exactly at
  what you want to shoot. Especially useful in third person shooters.
* Place its hands on the steering wheel of a car and follow it when it
  rotates.
* Much more!

[IKControl](/docs/reference/engine/classes/IKControl) will override the animation for all the parts between the
[ChainRoot](/docs/reference/engine/classes/IKControl#ChainRoot) and the
[EndEffector](/docs/reference/engine/classes/IKControl#EndEffector). You can enable/disable it using
[Enabled](/docs/reference/engine/classes/IKControl#Enabled) or change how much they have an effect over
the underlying animation using the [Weight](/docs/reference/engine/classes/IKControl#Weight). Be
careful: if you do not set up your [IKControls](/docs/reference/engine/classes/IKControl) correctly, you
might generate bad and unrealistic poses!

Code Samples

IKControl setup

This sample shows the basic setup for an [IKControl](/docs/reference/engine/classes/IKControl) that moves a
character's left arm to reach for a point in the world.

```
local character = script.Parent.Character



local humanoid = character.Humanoid



local root = character.HumanoidRootPart



-- Create a new attachment to use as the IKControl.Target



local target = Instance.new("Attachment")



target.CFrame = CFrame.new(-1, 0, -1)



target.Parent = root



local ikControl = Instance.new("IKControl")



ikControl.Type = Enum.IKControlType.Position



ikControl.EndEffector = character.LeftHand



ikControl.ChainRoot = character.LeftUpperArm



ikControl.Target = target



ikControl.Parent = humanoid
```

---

API Reference

Properties

ChainRoot

Read Parallel

The last part that you are interested in moving your character. For
example, the upper arm. Must be an ancestor of
[EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) and be a [BasePart](/docs/reference/engine/classes/BasePart) or a
[Bone](/docs/reference/engine/classes/Bone) in your character.

IKControl.ChainRoot:[Instance](/docs/reference/engine/datatypes/Instance)

By specifying a [ChainRoot](/docs/reference/engine/classes/IKControl#ChainRoot) and an
[EndEffector](/docs/reference/engine/classes/IKControl#EndEffector), you instruct the
[IKControl](/docs/reference/engine/classes/IKControl) that it's allowed to move and rotate all parts between
the two to move the [EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) to the
[Target](/docs/reference/engine/classes/IKControl#Target). For example, if you specify the LeftHand
as [EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) and LeftUpperArm as the
[ChainRoot](/docs/reference/engine/classes/IKControl#ChainRoot), the control moves 3 parts: the
LeftHand, the LeftLowerArm, and the LeftUpperArm. Avoid setting
[ChainRoot](/docs/reference/engine/classes/IKControl#ChainRoot) as the actual root of the character
because that produces unrealistic results.

Provide feedback

---

Enabled

Read Parallel

Toggles the control on and off. True by default.

IKControl.Enabled:[boolean](/docs/luau/booleans)

This property allows you to toggle the IK control on and off. It's on by
default. When [Enabled](/docs/reference/engine/classes/IKControl#Enabled) is false, the IK control
is off and isn't resolved by the underlying solver.

Provide feedback

---

EndEffector

Read Parallel

The part that you are interested in moving to reach the
[Target](/docs/reference/engine/classes/IKControl#Target). For example, the hand of your character.
Must be a descendant of [ChainRoot](/docs/reference/engine/classes/IKControl#ChainRoot) and be a
[BasePart](/docs/reference/engine/classes/BasePart) or a [Bone](/docs/reference/engine/classes/Bone) in your character.

IKControl.EndEffector:[Instance](/docs/reference/engine/datatypes/Instance)

The [EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) describes the last part in
the chain of your character that you want to affect. For example, it could
be the hand when you want to move the whole arm to reach a point. It can
be a [BasePart](/docs/reference/engine/classes/BasePart) on a character, that has a [Motor6D](/docs/reference/engine/classes/Motor6D) as its
child, a [Motor6D](/docs/reference/engine/classes/Motor6D) directly, a [Bone](/docs/reference/engine/classes/Bone), or a
[Attachment](/docs/reference/engine/classes/Attachment). The pivot of the selected
[EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) moves to the
[Target](/docs/reference/engine/classes/IKControl#Target), so you can use
[Attachments](/docs/reference/engine/classes/Attachment) to modify which point of a [BasePart](/docs/reference/engine/classes/BasePart)
should reach the [Target](/docs/reference/engine/classes/IKControl#Target).

Provide feedback

---

EndEffectorOffset

Read Parallel

An additional offset applied on top of the
[EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) in its local space to change
where it moves.

IKControl.EndEffectorOffset:[CFrame](/docs/reference/engine/datatypes/CFrame)

The end-effector offset is an additional [CFrame](/docs/reference/engine/datatypes/CFrame) applied on top
of the [Target](/docs/reference/engine/classes/IKControl#Target) [CFrame](/docs/reference/engine/datatypes/CFrame) that produces the
final [CFrame](/docs/reference/engine/datatypes/CFrame) used to place the
[EndEffector](/docs/reference/engine/classes/IKControl#EndEffector). By default, it's the identity
CFrame, so if you don't set it, it has no effect and the
[EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) uses the
[Target](/docs/reference/engine/classes/IKControl#Target) [CFrame](/docs/reference/engine/datatypes/CFrame) directly, which is
specified in the local space of the
[EndEffector](/docs/reference/engine/classes/IKControl#EndEffector).

Alternatively, you can use Attachments by setting an Attachment as
[EndEffector](/docs/reference/engine/classes/IKControl#EndEffector), which moves it to the
[Target](/docs/reference/engine/classes/IKControl#Target) instead of the parts it's attached to,
effectively obtaining the same result.

You can also use [EndEffectorOffset](/docs/reference/engine/classes/IKControl#EndEffectorOffset) to
modify which axis of the [EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) should
point at the [Target](/docs/reference/engine/classes/IKControl#Target) when using LookAt as
[Type](/docs/reference/engine/classes/IKControl#Type).

Provide feedback

---

Offset

Read Parallel

An additional offset applied on top of the [Target](/docs/reference/engine/classes/IKControl#Target)
to change where the [EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) moves.

IKControl.Offset:[CFrame](/docs/reference/engine/datatypes/CFrame)

The offset is an additional [CFrame](/docs/reference/engine/datatypes/CFrame) applied on top of the
[Target](/docs/reference/engine/classes/IKControl#Target) [CFrame](/docs/reference/engine/datatypes/CFrame) that produces the final
[CFrame](/docs/reference/engine/datatypes/CFrame) used to place the
[EndEffector](/docs/reference/engine/classes/IKControl#EndEffector). It's identity by default, so if
you don't set it, it has no effect and the
[EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) will use the
[Target](/docs/reference/engine/classes/IKControl#Target) [CFrame](/docs/reference/engine/datatypes/CFrame) directly. You can
animate it to create procedural animations such as typing on a keyboard.
It's useful when the [Target](/docs/reference/engine/classes/IKControl#Target) and
[EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) aren't aligned and you need to
fix it with an additional rotation or translation.

Provide feedback

---

Pole

Read Parallel

An optional instance that determines which way the chain bends. You can
use this to specify which way an elbow or knee bends.

IKControl.Pole:[Instance](/docs/reference/engine/datatypes/Instance)

The [Pole](/docs/reference/engine/classes/IKControl#Pole) is an optional [Instance](/docs/reference/engine/classes/Instance) that gives
you control over how intermediate parts in your character should bend. It
can be anything that has a position in the world, such as
[BasePart](/docs/reference/engine/classes/BasePart), [Attachment](/docs/reference/engine/classes/Attachment), [Bone](/docs/reference/engine/classes/Bone), [Motor6D](/docs/reference/engine/classes/Motor6D). It is
by default nil. When you specify it, the underlying solver will make the
parts bend towards it. When it is nil, the solver will try to make
elbows and knees bend appropriately based on the limb of the character.
The limb will be "Arm" when you select as
[EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) either the *LeftHand* or
*RightHand* and as [ChainRoot](/docs/reference/engine/classes/IKControl#ChainRoot) the corresponding
*LeftUpperArm* or *RightUpperArm*, and it will be "Leg" when you select as
[EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) either the *LeftFoot* or
*RightFoot* and as [ChainRoot](/docs/reference/engine/classes/IKControl#ChainRoot) the corresponding
*LeftUpperLeg* or *RightUpperLeg*. In all other cases, if you don't
specify a pole, the chain might not bend as you expect.

Provide feedback

---

Priority

Read Parallel

Specifies the order in which controls are solved. Higher values have
higher priority.

IKControl.Priority:[number](/docs/luau/numbers)

When multiple controls are active on a character, the order in which they
are solved by the underlying system affects the final generated pose. By
changing this value, you specify the ordering in which controls are
satisfied. Higher values have higher priority, and higher-priority
controls are resolved later because their result might override the
previous result of other controls. If you have multiple IK controls on a
character and one is more important than the other, specify a lower
priority for it. It is 0 by default, meaning all controls have the same
priority.

Provide feedback

---

SmoothTime

Read Parallel

Specifies the average number of seconds that it takes for the
[EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) to smoothly reach the
[Target](/docs/reference/engine/classes/IKControl#Target).

IKControl.SmoothTime:[number](/docs/luau/numbers)

This value specifies the average number of seconds that it takes for the
[EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) to reach the
[Target](/docs/reference/engine/classes/IKControl#Target). The behavior is that of a
critically-damped spring, where the rate of change is proportional to the
distance to the target and no oscillations are present when approaching
the target. Smaller values create a quicker convergence, and larger values
create a slower convergence. A value of 0 disables smoothing. The default
value is 0.05 to provide a very slight smoothing that makes the motion
feel realistic.

Provide feedback

---

Target

Read Parallel

The object that the [EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) reaches for
or points at. It can be anything that has a position in the world, such as
[BasePart](/docs/reference/engine/classes/BasePart), [Attachment](/docs/reference/engine/classes/Attachment), [Bone](/docs/reference/engine/classes/Bone), or [Motor6D](/docs/reference/engine/classes/Motor6D).

IKControl.Target:[Instance](/docs/reference/engine/datatypes/Instance)

The [Target](/docs/reference/engine/classes/IKControl#Target) represents a point ([CFrame](/docs/reference/engine/datatypes/CFrame))
in the world that you want your [EndEffector](/docs/reference/engine/classes/IKControl#EndEffector)
to reach. The exact behavior of reaching can be set via the
[Type](/docs/reference/engine/classes/IKControl#Type) property, and an additional
[Offset](/docs/reference/engine/classes/IKControl#Offset) can be applied on top of it to modify it.
If you set a [Target](/docs/reference/engine/classes/IKControl#Target) that will be moved either by
physics or a script, at each frame the [IKControl](/docs/reference/engine/classes/IKControl) will try to
satisfy it, automatically updating the point to reach.

Provide feedback

---

Type

Read Parallel

Specifies how the solver satisfies this control.

IKControl.Type:[Enum.IKControlType](/docs/reference/engine/enums/IKControlType)

By changing the [Type](/docs/reference/engine/classes/IKControl#Type), you can change the behavior
of the control. These are the available options:

* Transform: it's a full 6-DoF constraint. Aligns the
  [EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) [CFrame](/docs/reference/engine/datatypes/CFrame) to that of
  the [Target](/docs/reference/engine/classes/IKControl#Target).
* Position: aligns the [EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) position
  to that of the [Target](/docs/reference/engine/classes/IKControl#Target).
* Rotation: aligns the [EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) rotation
  to that of the [Target](/docs/reference/engine/classes/IKControl#Target).
* LookAt: moves and orients the whole chain to make an axis (by default
  the forward axis) on the [EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) point
  at a position in the world specified by [Target](/docs/reference/engine/classes/IKControl#Target).

Provide feedback

---

Weight

Read Parallel

Specifies the weight of the IK control target. Should be in the [0, 1]
range.

IKControl.Weight:[number](/docs/luau/numbers)

You can control how much a given control affects the character pose by
using this property. Values should be in the [0, 1] range. 0 means no
effect, and 1 means full effect of the IK control. Values outside this
range are truncated. Smoothly varying this value allows you to blend in or
out a specific control to avoid jarring motion. It is 1 by default.

The weight determines the interpolation factor between the End-Effector
and the IK target. Setting the weight to 0 doesn't disable the IK Control
because other factors, including the SmoothTime smoothing factor and Pole,
can still change the pose. To truly disable the IK Control, turn the
[Enabled](/docs/reference/engine/classes/IKControl#Enabled) property to false.

Provide feedback

---

Methods

GetChainCount

IKControl:GetChainCount():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

Provide feedback

---

GetChainLength

IKControl:GetChainLength():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

Provide feedback

---

GetNodeLocalCFrame

IKControl:GetNodeLocalCFrame(index:[number](/docs/luau/numbers)):[CFrame](/docs/reference/engine/datatypes/CFrame)

Parameters

|  |
| --- |
| index:[number](/docs/luau/numbers) |

Returns

[CFrame](/docs/reference/engine/datatypes/CFrame)

Provide feedback

---

GetNodeWorldCFrame

IKControl:GetNodeWorldCFrame(index:[number](/docs/luau/numbers)):[CFrame](/docs/reference/engine/datatypes/CFrame)

Parameters

|  |
| --- |
| index:[number](/docs/luau/numbers) |

Returns

[CFrame](/docs/reference/engine/datatypes/CFrame)

Provide feedback

---

GetRawFinalTarget

IKControl:GetRawFinalTarget():[CFrame](/docs/reference/engine/datatypes/CFrame)

Returns

[CFrame](/docs/reference/engine/datatypes/CFrame)

Provide feedback

---

GetSmoothedFinalTarget

IKControl:GetSmoothedFinalTarget():[CFrame](/docs/reference/engine/datatypes/CFrame)

Returns

[CFrame](/docs/reference/engine/datatypes/CFrame)

Provide feedback

---