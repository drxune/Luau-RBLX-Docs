# NumberPose | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/NumberPose
Scraped: 2026-01-11T02:30:09.037807Z

## Inherits
- PoseBase
- NumberPose
- Instance
- Object
- Keyframes
- KeyframeSequences
- Pose
- Folder
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [PoseBase](/docs/reference/engine/classes/PoseBase)
6. /
7. [NumberPose](/docs/reference/engine/classes/NumberPose)

English

Feedback

Engine Class

NumberPose

Holds the value applied to a specific FACS control.

---

Summary

Properties

|  |
| --- |
| [Value](#Value):[number](/docs/luau/numbers) |

Inherited Members

3 inherited from [PoseBase](/docs/reference/engine/classes/PoseBase)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A NumberPose holds the value applied to a specific FACS control. The
control which is affected depends on its name.

NumberPose instances are the building blocks of facial animation and, with
[Keyframes](/docs/reference/engine/classes/Keyframe), make up
[KeyframeSequences](/docs/reference/engine/classes/KeyframeSequence).

#### NumberPoses and Facial Animation

Although a NumberPose is assigned to a single FACS control by name, that
control can in turn affect multiple bones of the face rig. FACS controls act
as an abstraction layer between facial muscle movements and how they are
defined in the rig.

#### NumberPose Hierarchy

Contrary to [Pose](/docs/reference/engine/classes/Pose) Instances, NumberPose instances cannot be
parented together. However, they all must be stored in a [Folder](/docs/reference/engine/classes/Folder) named
FaceControls that is a child of the Head [Pose](/docs/reference/engine/classes/Pose).

#### NumberPose Value

The Roblox animation system applies NumberPose values to the corresponding
FACS controls. Because those controls only respond to values between 0 and 1,
the values calculated by the animation system are always clamped to that
range.

---

API Reference

Properties

Value

Read Parallel

The value that will be applied to the FACS control corresponding to the
[NumberPose](/docs/reference/engine/classes/NumberPose).

NumberPose.Value:[number](/docs/luau/numbers)

The value that will be applied to the FACS control corresponding with the
[NumberPose](/docs/reference/engine/classes/NumberPose).

Provide feedback

---