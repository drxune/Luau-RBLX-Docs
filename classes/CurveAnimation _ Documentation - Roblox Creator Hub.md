# CurveAnimation | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/CurveAnimation
Scraped: 2026-01-11T02:27:24.807744Z

## Inherits
- AnimationClip
- CurveAnimation
- Instance
- Object
- Vector3Curve
- EulerRotationCurve
- RotationCurve
- Motor6Ds
- Bones
- Folder
- Motor6D
- Bone
- FaceControls
- FloatCurve
- KeyframeSequence
- AnimationClipProvider:RegisterAnimationClip()
- AnimationClipProvider:GetAnimationClipAsync()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [AnimationClip](/docs/reference/engine/classes/AnimationClip)
6. /
7. [CurveAnimation](/docs/reference/engine/classes/CurveAnimation)

English

Feedback

Engine Class

CurveAnimation

Stores animation data in the form of curves for each individual channel to
animate.

---

Summary

Inherited Members

2 inherited from [AnimationClip](/docs/reference/engine/classes/AnimationClip)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

CurveAnimation is a subtype of [AnimationClip](/docs/reference/engine/classes/AnimationClip) consumed by Roblox's
animation system. It stores animation data for each animated channel in a rig
as a separate, individual curve. For example, CurveAnimation stores the
position channel for an articulated joint as a [Vector3Curve](/docs/reference/engine/classes/Vector3Curve), and it
might store the rotation channel as a [EulerRotationCurve](/docs/reference/engine/classes/EulerRotationCurve) or
[RotationCurve](/docs/reference/engine/classes/RotationCurve).

#### Structure

CurveAnimation stores curves in a hierarchical manner, matching the
hierarchy of the structure of [Motor6Ds](/docs/reference/engine/classes/Motor6D) or [Bones](/docs/reference/engine/classes/Bone)
in the animated model. Under each CurveAnimation instance lies a hierarchy
of [Folder](/docs/reference/engine/classes/Folder) instances representing animated joints in the model. Under
each such folder instance, several possible instances may exist. An instance
named Position of type [Vector3Curve](/docs/reference/engine/classes/Vector3Curve) can drive the local translation
of the [Motor6D](/docs/reference/engine/classes/Motor6D) or [Bone](/docs/reference/engine/classes/Bone) on the animated model, while an
instance named Rotation of type [EulerRotationCurve](/docs/reference/engine/classes/EulerRotationCurve) or
[RotationCurve](/docs/reference/engine/classes/RotationCurve) can drive the local rotation of the [Motor6D](/docs/reference/engine/classes/Motor6D) or
[Bone](/docs/reference/engine/classes/Bone) on the animated model.

#### Partial matching of hierarchy

You can match partial hierarchies to a model when playing a CurveAnimation
in Roblox's animation system. This means that not all joints need to be
present in the hierarchy for the existing joints to apply properly.
Furthermore, you can match hierarchies in a "relative" manner. For example,
the first child [Folder](/docs/reference/engine/classes/Folder) instance root can be UpperTorso and the
animation system matches that to any existing sub-hierarchies in the model.

#### Animating miscellaneous channels

CurveAnimation can also animate other numerical values in a model. For
example, you can animate FACS controls for facial animations by creating a
[Folder](/docs/reference/engine/classes/Folder) under the CurveAnimation instance named after an existing
[FaceControls](/docs/reference/engine/classes/FaceControls) instance in the model. Then, to animate individual facial
controllers, you can store individual [FloatCurve](/docs/reference/engine/classes/FloatCurve) instances named after
the animated [FaceControls](/docs/reference/engine/classes/FaceControls) property.

#### Usage when making animations

As with other [AnimationClip](/docs/reference/engine/classes/AnimationClip) types such as [KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence),
you must first upload CurveAnimation instances to Roblox before playing
them. If you want to preview an animation before uploading it to Roblox, you
can generate a temporary ID using
[AnimationClipProvider:RegisterAnimationClip()](/docs/reference/engine/classes/AnimationClipProvider#RegisterAnimationClip); this generates a hash
ID that you can use for localized animation testing.

If you want to download the CurveAnimation corresponding to an existing
uploaded animation using Luau scripts, use
[AnimationClipProvider:GetAnimationClipAsync()](/docs/reference/engine/classes/AnimationClipProvider#GetAnimationClipAsync).