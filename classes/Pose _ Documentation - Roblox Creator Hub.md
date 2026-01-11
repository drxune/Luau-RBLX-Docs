# Pose | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Pose
Scraped: 2026-01-11T02:28:22.910496Z

## Inherits
- PoseBase
- Pose
- Motor6D
- BasePart
- Instance
- Object
- Keyframe
- Pose.CFrame
- Motor6D.Transform
- C0
- C1
- Motor6D.C0
- Motor6D.C1
- Instance.Parent
- Poses
- Instance:GetChildren()
- Instances
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [PoseBase](/docs/reference/engine/classes/PoseBase)
6. /
7. [Pose](/docs/reference/engine/classes/Pose)

English

Feedback

Engine Class

Pose

Holds the [CFrame](/docs/reference/engine/datatypes/CFrame) applied to the [Motor6D](/docs/reference/engine/classes/Motor6D) connected to its
associated [BasePart](/docs/reference/engine/classes/BasePart). The part which is controlled depends on the name
of the Pose.

---

Summary

Properties

|  |
| --- |
| [CFrame](#CFrame):[CFrame](/docs/reference/engine/datatypes/CFrame) |
| [MaskWeight](#MaskWeight):[number](/docs/luau/numbers)  Deprecated |

Methods

|  |
| --- |
| [AddSubPose](#AddSubPose)(pose: [Instance](/docs/reference/engine/datatypes/Instance)):() |
| [GetSubPoses](#GetSubPoses)():Instances |
| [RemoveSubPose](#RemoveSubPose)(pose: [Instance](/docs/reference/engine/datatypes/Instance)):() |

Inherited Members

3 inherited from [PoseBase](/docs/reference/engine/classes/PoseBase)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A Pose holds the [CFrame](/docs/reference/engine/datatypes/CFrame) applied to the [Motor6D](/docs/reference/engine/classes/Motor6D) connected to
its associated [BasePart](/docs/reference/engine/classes/BasePart). The part which is controlled depends on the
name of the Pose.

Poses are the fundamental building blocks of animations and, with Keyframes,
make up KeyframeSequences.

Poses, joints and hierarchy
---------------------------

Although a Pose is assigned to a [BasePart](/docs/reference/engine/classes/BasePart) by name, the object
manipulated during animation playback is actually the [Motor6D](/docs/reference/engine/classes/Motor6D)
connected to this part. Animation rigs branch out from the model's root part
through such joints.

In a R15 character rig, the root part is the HumanoidRootPart. The LowerTorso
is connected to the HumanoidRootPart by the a motor named 'Root'. Therefore,
the [CFrame](/docs/reference/engine/datatypes/CFrame) of a Pose named 'LowerTorso' in a [Keyframe](/docs/reference/engine/classes/Keyframe) would
be applied to the motor named 'Root', and not the LowerTorso itself.

Poses are arranged in a [Keyframe](/docs/reference/engine/classes/Keyframe) based on joint hierarchy. This means,
the Pose's [CFrame](/docs/reference/engine/datatypes/CFrame) is applied to the motor connecting the part
associated with the pose to the part associated with the pose's parent. See
below for a visual example of the structure of Poses on a R15 character.

Pose CFrame
-----------

The Roblox animation system applies [Pose.CFrame](/docs/reference/engine/classes/Pose#CFrame) to the corresponding
[Motor6D](/docs/reference/engine/classes/Motor6D) by manipulating the relative transformation of the motor, the
[Motor6D.Transform](/docs/reference/engine/classes/Motor6D#Transform) property. The original [C0](/docs/reference/engine/classes/JointInstance#C1)
and [C1](/docs/reference/engine/classes/JointInstance#C1) values are not changed.

Code Samples

Keyframe Generate Poses

This sample includes a function that will generate a 'blank' keyframe
containing blank poses for all of the model's connected parts in the correct
hierarchical order.

```
local function generateKeyframe(model)



if not model.PrimaryPart then



warn("No primary part set")



return



end



local rootPart = model.PrimaryPart:GetRootPart()



if not rootPart then



warn("Root part not found")



return



end



local partsAdded = {}



partsAdded[rootPart] = true



local function addPoses(part, parentPose)



-- get all of the joints attached to the part



for _, joint in pairs(part:GetJoints()) do



-- we're only interested in Motor6Ds



if joint:IsA("Motor6D") then



-- find the connected part



local connectedPart = nil



if joint.Part0 == part then



connectedPart = joint.Part1



elseif joint.Part1 == part then



connectedPart = joint.Part0



end



if connectedPart then



-- make sure we haven't already added this part



if not partsAdded[connectedPart] then



partsAdded[connectedPart] = true



-- create a pose



local pose = Instance.new("Pose")



pose.Name = connectedPart.Name



parentPose:AddSubPose(pose)



-- recurse



addPoses(connectedPart, pose)



end



end



end



end



end



local keyframe = Instance.new("Keyframe")



-- populate the keyframe



local rootPose = Instance.new("Pose")



rootPose.Name = rootPart.Name



addPoses(rootPart, rootPose)



keyframe:AddPose(rootPose)



return keyframe



end



local character = script.Parent



local keyframe = generateKeyframe(character)



print(keyframe)
```

Keyframe Reset Poses

This code sample includes a function to reset the CFrame of the Poses in a
Keyframe.

```
local function resetPoses(parent)



-- both functions are equivalent to GetChildren



local poses = parent:IsA("Keyframe") and parent:GetPoses() or parent:IsA("Pose") and parent:GetSubPoses()



for _, pose in pairs(poses) do



if pose:IsA("Pose") then



pose.CFrame = CFrame.new()



-- recurse



resetPoses(pose)



end



end



end
```

---

API Reference

Properties

CFrame

Read Parallel

This [CFrame](/docs/reference/engine/datatypes/CFrame) applies to the [Motor6D](/docs/reference/engine/classes/Motor6D) corresponding with
the [Pose](/docs/reference/engine/classes/Pose) when the [Motor6D.Transform](/docs/reference/engine/classes/Motor6D#Transform) is changed.

Pose.CFrame:[CFrame](/docs/reference/engine/datatypes/CFrame)

This [CFrame](/docs/reference/engine/datatypes/CFrame) applies to the [Motor6D](/docs/reference/engine/classes/Motor6D) corresponding with
the [Pose](/docs/reference/engine/classes/Pose) when the [Motor6D.Transform](/docs/reference/engine/classes/Motor6D#Transform) is changed. The
original [Motor6D.C0](/docs/reference/engine/classes/Motor6D#C0) and [Motor6D.C1](/docs/reference/engine/classes/Motor6D#C1) values are not changed.

[Pose](/docs/reference/engine/classes/Pose) objects are arranged in a [Keyframe](/docs/reference/engine/classes/Keyframe) based on joint
hierarchy. This means, that the [Pose.CFrame](/docs/reference/engine/classes/Pose#CFrame) is applied to the
motor connecting the part associated with the pose to the part associated
with the pose's parent.

Provide feedback

---

MaskWeight

Deprecated

Show details

---

Methods

AddSubPose

Adds a sub [Pose](/docs/reference/engine/classes/Pose) to the [Pose](/docs/reference/engine/classes/Pose) by parenting it.

Pose:AddSubPose(pose:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| pose:[Instance](/docs/reference/engine/datatypes/Instance)  The [Pose](/docs/reference/engine/classes/Pose) to be added. |

Returns

()

Adds a sub [Pose](/docs/reference/engine/classes/Pose) to the [Pose](/docs/reference/engine/classes/Pose) by parenting it to it. It is
functionally identical to setting the new pose's [Instance.Parent](/docs/reference/engine/classes/Instance#Parent)
to the pose.

Note, this function will not error when an instance other than a
[Pose](/docs/reference/engine/classes/Pose) is given as the pose parameter and will parent it
successfully.

Code Samples

Keyframe Add/Remove Pose

This sample demonstrates quickly the Keyframe.AddPose, Keyframe.RemovePose and
Pose.AddSubPose and Pose.RemoveSubPose functions. Note these are functionally
equivalent to parenting and un-parenting the poses.

```
local keyframe = Instance.new("Keyframe")



keyframe.Parent = workspace



local pose = Instance.new("Pose")



pose.EasingStyle = Enum.PoseEasingStyle.Cubic



pose.EasingDirection = Enum.PoseEasingDirection.Out



local pose2 = Instance.new("Pose")



pose2.EasingStyle = Enum.PoseEasingStyle.Cubic



pose2.EasingDirection = Enum.PoseEasingDirection.Out



keyframe:AddPose(pose) -- pose.Parent = keyframe



task.wait(2)



keyframe:RemovePose(pose) -- pose.Parent = nil



task.wait(2)



keyframe:AddPose(pose) -- pose.Parent = keyframe



task.wait(2)



pose:AddSubPose(pose2) -- pose2.Parent = pose



task.wait(2)



pose:RemoveSubPose(pose2) -- pose2.Parent = nil
```

Provide feedback

---

GetSubPoses

Returns an array containing all sub [Poses](/docs/reference/engine/classes/Pose) that have been
added to a [Pose](/docs/reference/engine/classes/Pose).

Pose:GetSubPoses():Instances

Returns

Instances

An array of sub [Poses](/docs/reference/engine/classes/Pose).

Returns an array containing all sub [Poses](/docs/reference/engine/classes/Pose) that have been
added to a [Pose](/docs/reference/engine/classes/Pose). This is functionally the same as using the
[Instance:GetChildren()](/docs/reference/engine/classes/Instance#GetChildren) function on the [Pose](/docs/reference/engine/classes/Pose).

Note: this function returns all children of the [Pose](/docs/reference/engine/classes/Pose), including
non [Pose](/docs/reference/engine/classes/Pose) [Instances](/docs/reference/engine/classes/Instance) if any are present.

Code Samples

Keyframe Reset Poses

This code sample includes a function to reset the CFrame of the Poses in a
Keyframe.

```
local function resetPoses(parent)



-- both functions are equivalent to GetChildren



local poses = parent:IsA("Keyframe") and parent:GetPoses() or parent:IsA("Pose") and parent:GetSubPoses()



for _, pose in pairs(poses) do



if pose:IsA("Pose") then



pose.CFrame = CFrame.new()



-- recurse



resetPoses(pose)



end



end



end
```

Provide feedback

---

RemoveSubPose

Removes a sub [Pose](/docs/reference/engine/classes/Pose) from the [Pose](/docs/reference/engine/classes/Pose) by parenting it to nil.

Pose:RemoveSubPose(pose:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| pose:[Instance](/docs/reference/engine/datatypes/Instance)  The [Pose](/docs/reference/engine/classes/Pose) to be removed. |

Returns

()

Removes a sub [Pose](/docs/reference/engine/classes/Pose) from the [Pose](/docs/reference/engine/classes/Pose) by parenting it to nil.
This is functionally identical to setting the new pose's
[Instance.Parent](/docs/reference/engine/classes/Instance#Parent) to nil.

Note: If an [Instance](/docs/reference/engine/classes/Instance) other than [Pose](/docs/reference/engine/classes/Pose) is used as a
[Pose](/docs/reference/engine/classes/Pose) parameter, this function removes that [Instance](/docs/reference/engine/classes/Instance) and
does not provide an error.

Code Samples

Keyframe Add/Remove Pose

This sample demonstrates quickly the Keyframe.AddPose, Keyframe.RemovePose and
Pose.AddSubPose and Pose.RemoveSubPose functions. Note these are functionally
equivalent to parenting and un-parenting the poses.

```
local keyframe = Instance.new("Keyframe")



keyframe.Parent = workspace



local pose = Instance.new("Pose")



pose.EasingStyle = Enum.PoseEasingStyle.Cubic



pose.EasingDirection = Enum.PoseEasingDirection.Out



local pose2 = Instance.new("Pose")



pose2.EasingStyle = Enum.PoseEasingStyle.Cubic



pose2.EasingDirection = Enum.PoseEasingDirection.Out



keyframe:AddPose(pose) -- pose.Parent = keyframe



task.wait(2)



keyframe:RemovePose(pose) -- pose.Parent = nil



task.wait(2)



keyframe:AddPose(pose) -- pose.Parent = keyframe



task.wait(2)



pose:AddSubPose(pose2) -- pose2.Parent = pose



task.wait(2)



pose:RemoveSubPose(pose2) -- pose2.Parent = nil
```

Provide feedback

---