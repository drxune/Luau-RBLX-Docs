# Humanoid | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Humanoid
Scraped: 2026-01-11T02:40:23.750933Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- Humanoid
- BasePart
- HumanoidDescription
- Animation
- AnimationTrack
- Model
- Motor6D
- CharacterMesh
- Humanoid.LeftLeg
- Humanoid.RightLeg
- NumberValue
- Vector3Value
- Player.Character
- Player
- Player.AutoJumpEnabled
- StarterPlayer.AutoJumpEnabled
- Camera.CameraSubject
- Humanoid.DisplayerDistanceType
- Humanoid.HealthDisplayDistance
- Humanoid.NameDisplayDistance
- LoadCharacter()
- StarterPlayer
- Humanoid.DisplayName
- Part.CanCollide
- StateChanged
- Players
- Humanoid.RootPart
- Humanoid.MoveDirection
- Humanoid:Move()
- PlayerScripts
- Parts
- Terrain
- Object:GetPropertyChangedSignal()
- Humanoid:GetState()
- Humanoid.MaxHealth
- MaxHealth
- TakeDamage()
- Health
- Script
- StarterCharacterScripts
- HealthDisplayDistance
- HealthDisplayType
- DisplayDistanceType
- RootPart
- RigType
- HipHeight
- Humanoid.JumpPower
- Humanoid.JumpHeight
- Humanoid.UseJumpPower
- StarterPlayer.CharacterJumpHeight
- Humanoid:SetStateEnabled()
- StarterPlayer.CharacterJumpPower
- Workspace.Gravity
- StarterPlayer.CharacterMaxSlopeAngle
- Players.LocalPlayer
- LocalScript
- Humanoid.DisplayDistanceType
- LocalPlayer
- Model.PrimaryPart
- Seat
- VehicleSeat
- Humanoid.Sit
- Humanoids
- Humanoid.SeatPart
- Humanoid.Seated
- Tool
- Tool:Activate()
- JumpHeight
- StarterPlayer.CharacterUseJumpPower
- StarterPlayer.CharacterWalkSpeed
- WalkSpeed
- Running
- MoveTo()
- WalkToPoint
- Humanoid:MoveTo()
- WalkToPart
- Accessory
- Attachment
- Part
- Weld
- Attachments
- AddAccessory()
- BuildRigFromAttachments()
- Humanoid:ApplyDescriptionReset()
- Humanoid:GetAppliedDescription()
- Players:GetHumanoidDescriptionFromUserId()
- Players:GetHumanoidDescriptionFromOutfitId()
- Player:LoadCharacterWithHumanoidDescription()
- ApplyDescriptionReset()
- ApplyDescription()
- Animations
- CFrame
- Humanoid:BuildRigFromAttachments()
- StarterPlayer.StarterCharacterScripts
- Tools
- Tool.RequiresHandle
- Humanoid:UnequipTools()
- Humanoid:AddAccessory()
- Humanoid:ApplyDescription()
- Humanoid:ReplaceBodyPartR15()
- Humanoid:GetLimb()
- Humanoid:ChangeState()
- Humanoid.StateEnabledChanged
- Humanoid:GetStateEnabled()
- CurrentCamera
- RunService:BindToRenderStep()
- StarterPlayerScripts
- Player:Move()
- Character
- Camera
- Humanoid.WalkToPoint
- Humanoid.WalkToPart
- MoveToFinished
- Move()
- Characters
- Instance:Destroy()
- Parent
- Humanoid:GetAccessories()
- GetBodyPartR15
- Humanoid.Health
- ForceField
- Instance.Parent
- Workspace
- ForceFields
- Backpack
- Humanoid:EquipTool()
- TrussParts
- Humanoid.WalkSpeed
- Humanoid.Swimming
- Humanoid.Running
- Humanoid.StateChanged
- Humanoid.Torso
- Humanoid.GettingUp
- Humanoid.Died
- Humanoid.PlatformStand
- Platform
- Humanoid.FallingDown
- Humanoid.Climbing
- Velocity
- Humanoid.Touched
- BasePart.Touched
- BaseParts
- Touched
- Humanoid.FloorMaterial
- TouchTransmitter
- BasePart.TouchEnded
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Humanoid](/docs/reference/engine/classes/Humanoid)

English

Feedback

Engine Class

![Humanoid](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Humanoid-Dark.webp)Humanoid

A special object that gives models the functionality of a character.

---

Summary

Properties

|  |
| --- |
| [AutoJumpEnabled](#AutoJumpEnabled):[boolean](/docs/luau/booleans) |
| [AutomaticScalingEnabled](#AutomaticScalingEnabled):[boolean](/docs/luau/booleans) |
| [AutoRotate](#AutoRotate):[boolean](/docs/luau/booleans) |
| [BreakJointsOnDeath](#BreakJointsOnDeath):[boolean](/docs/luau/booleans) |
| [CameraOffset](#CameraOffset):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [CollisionType](#CollisionType):[Enum.HumanoidCollisionType](/docs/reference/engine/enums/HumanoidCollisionType)  Deprecated |
| [DisplayDistanceType](#DisplayDistanceType):[Enum.HumanoidDisplayDistanceType](/docs/reference/engine/enums/HumanoidDisplayDistanceType) |
| [DisplayName](#DisplayName):[string](/docs/luau/strings) |
| [EvaluateStateMachine](#EvaluateStateMachine):[boolean](/docs/luau/booleans) |
| [FloorMaterial](#FloorMaterial):[Enum.Material](/docs/reference/engine/enums/Material) |
| [Health](#Health):[number](/docs/luau/numbers) |
| [HealthDisplayDistance](#HealthDisplayDistance):[number](/docs/luau/numbers) |
| [HealthDisplayType](#HealthDisplayType):[Enum.HumanoidHealthDisplayType](/docs/reference/engine/enums/HumanoidHealthDisplayType) |
| [HipHeight](#HipHeight):[number](/docs/luau/numbers) |
| [Jump](#Jump):[boolean](/docs/luau/booleans) |
| [JumpHeight](#JumpHeight):[number](/docs/luau/numbers) |
| [JumpPower](#JumpPower):[number](/docs/luau/numbers) |
| [LeftLeg](#LeftLeg):[BasePart](/docs/reference/engine/classes/BasePart)  Deprecated |
| [MaxHealth](#MaxHealth):[number](/docs/luau/numbers) |
| [maxHealth](#maxHealth):[number](/docs/luau/numbers)  Deprecated |
| [MaxSlopeAngle](#MaxSlopeAngle):[number](/docs/luau/numbers) |
| [MoveDirection](#MoveDirection):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [NameDisplayDistance](#NameDisplayDistance):[number](/docs/luau/numbers) |
| [NameOcclusion](#NameOcclusion):[Enum.NameOcclusion](/docs/reference/engine/enums/NameOcclusion) |
| [PlatformStand](#PlatformStand):[boolean](/docs/luau/booleans) |
| [RequiresNeck](#RequiresNeck):[boolean](/docs/luau/booleans) |
| [RightLeg](#RightLeg):[BasePart](/docs/reference/engine/classes/BasePart)  Deprecated |
| [RigType](#RigType):[Enum.HumanoidRigType](/docs/reference/engine/enums/HumanoidRigType) |
| [RootPart](#RootPart):[BasePart](/docs/reference/engine/classes/BasePart) |
| [SeatPart](#SeatPart):[BasePart](/docs/reference/engine/classes/BasePart) |
| [Sit](#Sit):[boolean](/docs/luau/booleans) |
| [TargetPoint](#TargetPoint):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [Torso](#Torso):[BasePart](/docs/reference/engine/classes/BasePart)  Deprecated |
| [UseJumpPower](#UseJumpPower):[boolean](/docs/luau/booleans) |
| [WalkSpeed](#WalkSpeed):[number](/docs/luau/numbers) |
| [WalkToPart](#WalkToPart):[BasePart](/docs/reference/engine/classes/BasePart) |
| [WalkToPoint](#WalkToPoint):[Vector3](/docs/reference/engine/datatypes/Vector3) |

Methods

|  |
| --- |
| [AddAccessory](#AddAccessory)(accessory: [Instance](/docs/reference/engine/datatypes/Instance)):() |
| [AddCustomStatus](#AddCustomStatus)(status: [string](/docs/luau/strings)):[boolean](/docs/luau/booleans)  Deprecated |
| [AddStatus](#AddStatus)(status: [Enum.Status](/docs/reference/engine/enums/Status)):[boolean](/docs/luau/booleans)  Deprecated |
| [ApplyDescriptionAsync](#ApplyDescriptionAsync)(humanoidDescription: [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription),assetTypeVerification: [Enum.AssetTypeVerification](/docs/reference/engine/enums/AssetTypeVerification)):() |
| [ApplyDescription](#ApplyDescription)(humanoidDescription: [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription),assetTypeVerification: [Enum.AssetTypeVerification](/docs/reference/engine/enums/AssetTypeVerification)):()  Deprecated |
| [ApplyDescriptionResetAsync](#ApplyDescriptionResetAsync)(humanoidDescription: [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription),assetTypeVerification: [Enum.AssetTypeVerification](/docs/reference/engine/enums/AssetTypeVerification)):() |
| [ApplyDescriptionReset](#ApplyDescriptionReset)(humanoidDescription: [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription),assetTypeVerification: [Enum.AssetTypeVerification](/docs/reference/engine/enums/AssetTypeVerification)):()  Deprecated |
| [BuildRigFromAttachments](#BuildRigFromAttachments)():() |
| [ChangeState](#ChangeState)(state: [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType)):() |
| [EquipTool](#EquipTool)(tool: [Instance](/docs/reference/engine/datatypes/Instance)):() |
| [GetAccessories](#GetAccessories)():[Array](/docs/luau/tables#arrays) |
| [GetAppliedDescription](#GetAppliedDescription)():[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) |
| [GetBodyPartR15](#GetBodyPartR15)(part: [Instance](/docs/reference/engine/datatypes/Instance)):[Enum.BodyPartR15](/docs/reference/engine/enums/BodyPartR15) |
| [GetLimb](#GetLimb)(part: [Instance](/docs/reference/engine/datatypes/Instance)):[Enum.Limb](/docs/reference/engine/enums/Limb) |
| [GetMoveVelocity](#GetMoveVelocity)():[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [GetPlayingAnimationTracks](#GetPlayingAnimationTracks)():[Array](/docs/luau/tables#arrays)  Deprecated |
| [GetState](#GetState)():[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType) |
| [GetStateEnabled](#GetStateEnabled)(state: [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType)):[boolean](/docs/luau/booleans) |
| [GetStatuses](#GetStatuses)():[Array](/docs/luau/tables#arrays)  Deprecated |
| [HasCustomStatus](#HasCustomStatus)(status: [string](/docs/luau/strings)):[boolean](/docs/luau/booleans)  Deprecated |
| [HasStatus](#HasStatus)(status: [Enum.Status](/docs/reference/engine/enums/Status)):[boolean](/docs/luau/booleans)  Deprecated |
| [LoadAnimation](#LoadAnimation)(animation: [Animation](/docs/reference/engine/classes/Animation)):[AnimationTrack](/docs/reference/engine/classes/AnimationTrack)  Deprecated |
| [loadAnimation](#loadAnimation)(animation: [Animation](/docs/reference/engine/classes/Animation)):[AnimationTrack](/docs/reference/engine/classes/AnimationTrack)  Deprecated |
| [Move](#Move)(moveDirection: [Vector3](/docs/reference/engine/datatypes/Vector3),relativeToCamera: [boolean](/docs/luau/booleans)):() |
| [MoveTo](#MoveTo)(location: [Vector3](/docs/reference/engine/datatypes/Vector3),part: [Instance](/docs/reference/engine/datatypes/Instance)):() |
| [PlayEmoteAsync](#PlayEmoteAsync)(emoteName: [string](/docs/luau/strings)):[boolean](/docs/luau/booleans) |
| [PlayEmote](#PlayEmote)(emoteName: [string](/docs/luau/strings)):[boolean](/docs/luau/booleans)  Deprecated |
| [RemoveAccessories](#RemoveAccessories)():() |
| [RemoveCustomStatus](#RemoveCustomStatus)(status: [string](/docs/luau/strings)):[boolean](/docs/luau/booleans)  Deprecated |
| [RemoveStatus](#RemoveStatus)(status: [Enum.Status](/docs/reference/engine/enums/Status)):[boolean](/docs/luau/booleans)  Deprecated |
| [ReplaceBodyPartR15](#ReplaceBodyPartR15)(bodyPart: [Enum.BodyPartR15](/docs/reference/engine/enums/BodyPartR15),part: [BasePart](/docs/reference/engine/classes/BasePart)):[boolean](/docs/luau/booleans) |
| [SetStateEnabled](#SetStateEnabled)(state: [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType),enabled: [boolean](/docs/luau/booleans)):() |
| [TakeDamage](#TakeDamage)(amount: [number](/docs/luau/numbers)):() |
| [takeDamage](#takeDamage)(amount: [number](/docs/luau/numbers)):()  Deprecated |
| [UnequipTools](#UnequipTools)():() |

Events

|  |
| --- |
| [AnimationPlayed](#AnimationPlayed)(animationTrack: [AnimationTrack](/docs/reference/engine/classes/AnimationTrack)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |
| [ApplyDescriptionFinished](#ApplyDescriptionFinished)(description: [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Climbing](#Climbing)(speed: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [CustomStatusAdded](#CustomStatusAdded)(status: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |
| [CustomStatusRemoved](#CustomStatusRemoved)(status: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |
| [Died](#Died)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [FallingDown](#FallingDown)(active: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [FreeFalling](#FreeFalling)(active: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [GettingUp](#GettingUp)(active: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [HealthChanged](#HealthChanged)(health: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Jumping](#Jumping)(active: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MoveToFinished](#MoveToFinished)(reached: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PlatformStanding](#PlatformStanding)(active: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Ragdoll](#Ragdoll)(active: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Running](#Running)(speed: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Seated](#Seated)(active: [boolean](/docs/luau/booleans),currentSeatPart: [BasePart](/docs/reference/engine/classes/BasePart)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [StateChanged](#StateChanged)(old: [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType),new: [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [StateEnabledChanged](#StateEnabledChanged)(state: [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType),isEnabled: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [StatusAdded](#StatusAdded)(status: [Enum.Status](/docs/reference/engine/enums/Status)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |
| [StatusRemoved](#StatusRemoved)(status: [Enum.Status](/docs/reference/engine/enums/Status)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |
| [Strafing](#Strafing)(active: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Swimming](#Swimming)(speed: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Touched](#Touched)(touchingPart: [BasePart](/docs/reference/engine/classes/BasePart),humanoidPart: [BasePart](/docs/reference/engine/classes/BasePart)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The Humanoid is a special object that gives models the functionality of a
character. It grants the model with the ability to physically walk around and
interact with various components of a Roblox experience. Humanoids are always
parented inside of a [Model](/docs/reference/engine/classes/Model), and the model is expected to be an
assembly of [BasePart](/docs/reference/engine/classes/BasePart) and [Motor6D](/docs/reference/engine/classes/Motor6D); the root part of the
assembly is expected to be named HumanoidRootPart. It also expects a part
named Head to be connected to the character's torso part, either directly or
indirectly. By default, there are two official types of character rigs
supplied by Roblox, each with their own set of rules:

R6
--

* A basic character rig that uses 6 parts for limbs.
* The Head part must be attached to a part named Torso, or the Humanoid
  will die immediately.
* BodyPart appearances are applied using [CharacterMesh](/docs/reference/engine/classes/CharacterMesh) objects.
* Certain properties, such as [Humanoid.LeftLeg](/docs/reference/engine/classes/Humanoid#LeftLeg) and
  [Humanoid.RightLeg](/docs/reference/engine/classes/Humanoid#RightLeg), only work with R6.

R15
---

* More complex than R6, but also far more flexible and robust.
* Uses 15 parts for limbs.
* The Head part must be attached to a part named UpperTorso or the
  Humanoid will die immediately.
* BodyPart appearances have to be assembled directly.
* Can be dynamically rescaled by using special [NumberValue](/docs/reference/engine/classes/NumberValue) objects
  parented inside of the Humanoid.
* The Humanoid will automatically create [Vector3Value](/docs/reference/engine/classes/Vector3Value) objects named
  OriginalSize inside of each limb.
* If a NumberValue is parented inside of the Humanoid and is named one of the
  following, it will be used to control the scaling functionality:
  + BodyDepthScale
  + BodyHeightScale
  + BodyWidthScale
  + HeadScale

Code Samples

Walking Camera Bobble Effect

This LocalScript makes the camera bobble as the player's character walks
around, utilizing both the Humanoid's CameraOffset and MoveDirection. It
should be parented inside of the StarterCharacterScripts so that it is
distributed into a player's character as expected.

```
local RunService = game:GetService("RunService")



local playerModel = script.Parent



local humanoid = playerModel:WaitForChild("Humanoid")



local function updateBobbleEffect()



local now = tick()



if humanoid.MoveDirection.Magnitude > 0 then -- Is the character walking?



local velocity = humanoid.RootPart.Velocity



local bobble_X = math.cos(now * 9) / 5



local bobble_Y = math.abs(math.sin(now * 12)) / 5



local bobble = Vector3.new(bobble_X, bobble_Y, 0) * math.min(1, velocity.Magnitude / humanoid.WalkSpeed)



humanoid.CameraOffset = humanoid.CameraOffset:lerp(bobble, 0.25)



else



-- Scale down the CameraOffset so that it shifts back to its regular position.



humanoid.CameraOffset = humanoid.CameraOffset * 0.75



end



end



RunService.RenderStepped:Connect(updateBobbleEffect)
```

---

API Reference

Properties

AutoJumpEnabled

Read Parallel

Sets whether the character will automatically jump when they hit an
obstacle as a player on a mobile device.

Humanoid.AutoJumpEnabled:[boolean](/docs/luau/booleans)

AutoJumpEnabled sets whether or not the [Humanoid](/docs/reference/engine/classes/Humanoid) will attempt to
automatically jump over an obstacle it is walking towards.

Currently, this property only works when the following conditions are
true:

* The Humanoid's character model is the [Player.Character](/docs/reference/engine/classes/Player#Character) of a
  [Player](/docs/reference/engine/classes/Player).
* The Player in question is using touch controls.

When a player's character spawns, the property's value matches the
player's [Player.AutoJumpEnabled](/docs/reference/engine/classes/Player#AutoJumpEnabled) property - which in turn matches
the [StarterPlayer.AutoJumpEnabled](/docs/reference/engine/classes/StarterPlayer#AutoJumpEnabled) property.

Code Samples

Auto-Jump Toggle

This code sample is meant for a TextButton. It allows the player to toggle the
auto-jumping behavior while on a mobile device.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local button = script.Parent



local function update()



-- Update button text



if player.AutoJumpEnabled then



button.Text = "Auto-Jump is ON"



else



button.Text = "Auto-Jump is OFF"



end



-- Reflect the property in the player's character, if they have one



if player.Character then



local human = player.Character:FindFirstChild("Humanoid")



if human then



human.AutoJumpEnabled = player.AutoJumpEnabled



end



end



end



local function onActivated()



-- Toggle auto-jump



player.AutoJumpEnabled = not player.AutoJumpEnabled



-- Update everything else



update()



end



button.Activated:Connect(onActivated)



update()
```

Provide feedback

---

AutomaticScalingEnabled

Read Parallel

When Enabled, AutomaticScalingEnabled causes the size of the character to
change in response to the values in the humanoid's child scale values
changing.

Humanoid.AutomaticScalingEnabled:[boolean](/docs/luau/booleans)

The Humanoid has six child scale values including BodyDepthScale,
BodyHeightScale, BodyProportionScale, BodyTypeScale,
BodyWidthScale, HeadScale. Changing the value of any of these causes
the character's body parts and accessories to change size, but only if
AutomaticScalingEnabled is true.

Provide feedback

---

AutoRotate

Read Parallel

AutoRotate sets whether or not the Humanoid will automatically rotate to
face in the direction they are moving in.

Humanoid.AutoRotate:[boolean](/docs/luau/booleans)

The AutoRotate property describes whether or not the Humanoid will
automatically rotate to face in the direction they are moving. When set to
true, the character model will gradually turn to face their movement
direction as the Humanoid walks around. When set to false, the character
model will remain fixated in its current rotation, unless a rotating force
is applied to the *HumanoidRootPart*.

If the character model happens to be the character of a player, then the
behavior of the Humanoid's rotation is influenced by the UserGameSetting's
RotateType property.

When the AutoRotate property is set to true, the RotateType property has
the following effects on the Humanoid's rotation:

| RotationType | Behavior | Context |
| --- | --- | --- |
| MovementRelative |  |  |
| CameraRelative | Character will rotate to face in the direction of the camera. | Player has their camera zoomed into first-person, or they are in shift-lock mode. |

Code Samples

AutoRotate Button

This script adds the functionality of a button to a part, which switches the
AutoRotate property of whoever touches it.

```
local button = script.Parent



local enabled = true



local ON_COLOR = BrickColor.Green()



local OFF_COLOR = BrickColor.Red()



local function touchButton(humanoid)



if enabled then



enabled = false



button.BrickColor = OFF_COLOR



if humanoid.AutoRotate then



print(humanoid:GetFullName() .. " can no longer auto-rotate!")



humanoid.AutoRotate = false



else



print(humanoid:GetFullName() .. " can now auto-rotate!")



humanoid.AutoRotate = true



end



task.wait(1)



button.BrickColor = ON_COLOR



enabled = true



end



end



local function onTouched(hit)



local char = hit:FindFirstAncestorWhichIsA("Model")



if char then



local humanoid = char:FindFirstChildOfClass("Humanoid")



if humanoid then



touchButton(humanoid)



end



end



end



button.Touched:Connect(onTouched)



button.BrickColor = ON_COLOR
```

Provide feedback

---

BreakJointsOnDeath

Read Parallel

Determines whether the humanoid's joints break when in the
[Enum.HumanoidStateType.Dead](/docs/reference/engine/enums/HumanoidStateType#Dead) state.

Humanoid.BreakJointsOnDeath:[boolean](/docs/luau/booleans)

Determines whether the humanoid's joints break when in the
[Enum.HumanoidStateType.Dead](/docs/reference/engine/enums/HumanoidStateType#Dead) state. Defaults to true.

Provide feedback

---

CameraOffset

Read Parallel

An offset applied to the Camera's subject position when its CameraSubject
is set to this Humanoid.

Humanoid.CameraOffset:[Vector3](/docs/reference/engine/datatypes/Vector3)

The CameraOffset property specifies an offset to the camera's subject
position when its [Camera.CameraSubject](/docs/reference/engine/classes/Camera#CameraSubject) is set to this
[Humanoid](/docs/reference/engine/classes/Humanoid).

The offset is applied in object-space, relative to the orientation of the
Humanoid's *HumanoidRootPart*. For example, an offset [Vector3](/docs/reference/engine/datatypes/Vector3)
value of *(0, 10, 0)* offsets the player's camera to 10 studs above the
player's humanoid.

Code Samples

Walking Camera Bobble Effect

This LocalScript makes the camera bobble as the player's character walks
around, utilizing both the Humanoid's CameraOffset and MoveDirection. It
should be parented inside of the StarterCharacterScripts so that it is
distributed into a player's character as expected.

```
local RunService = game:GetService("RunService")



local playerModel = script.Parent



local humanoid = playerModel:WaitForChild("Humanoid")



local function updateBobbleEffect()



local now = tick()



if humanoid.MoveDirection.Magnitude > 0 then -- Is the character walking?



local velocity = humanoid.RootPart.Velocity



local bobble_X = math.cos(now * 9) / 5



local bobble_Y = math.abs(math.sin(now * 12)) / 5



local bobble = Vector3.new(bobble_X, bobble_Y, 0) * math.min(1, velocity.Magnitude / humanoid.WalkSpeed)



humanoid.CameraOffset = humanoid.CameraOffset:lerp(bobble, 0.25)



else



-- Scale down the CameraOffset so that it shifts back to its regular position.



humanoid.CameraOffset = humanoid.CameraOffset * 0.75



end



end



RunService.RenderStepped:Connect(updateBobbleEffect)
```

Provide feedback

---

CollisionType

Deprecated

Show details

---

DisplayDistanceType

Read Parallel

Controls the distance behavior of the humanoid's name and health display.

Humanoid.DisplayDistanceType:[Enum.HumanoidDisplayDistanceType](/docs/reference/engine/enums/HumanoidDisplayDistanceType)

The DisplayDistanceType property controls the distance behavior of the
humanoid's name and health display. This property is set using the
[Enum.HumanoidDisplayDistanceType](/docs/reference/engine/enums/HumanoidDisplayDistanceType) enum with three available values, each
with their own set of rules:

* When set to [Viewer](/docs/reference/engine/enums/HumanoidDisplayDistanceType), the humanoid sees
  the name/health of other humanoids within range of its own
  NameDisplayDistance and HealthDisplayDistance.
* When set to [Subject](/docs/reference/engine/enums/HumanoidDisplayDistanceType), the humanoid
  takes full control over its own name and health display through its
  NameDisplayDistance and HealthDisplayDistance values.
* When set to [None](/docs/reference/engine/enums/HumanoidDisplayDistanceType), the humanoid's name
  and health bar do not appear under any circumstances.

See
[Character Name/Health Display](/docs/characters/name-health-display)
for an in-depth guide on controlling the appearance of character names and
health bars.

Code Samples

Displaying a Humanoid's Health and Name

This example demonstrates how to set a Humanoid's
[Humanoid.DisplayerDistanceType](/docs/reference/engine/classes/Humanoid#DisplayerDistanceType),
[Humanoid.HealthDisplayDistance](/docs/reference/engine/classes/Humanoid#HealthDisplayDistance), and
[Humanoid.NameDisplayDistance](/docs/reference/engine/classes/Humanoid#NameDisplayDistance) properties. These properties determine
how a humanoid's healthbar and name are rendered for a player.

First, we change the DisplayDistanceType to Viewer using
[Enum.HumanoidDisplayDistanceType](/docs/reference/engine/enums/HumanoidDisplayDistanceType). When set to viewer, the humanoid's Name
and healthbar will be displayed based on the distance settings of the humanoid
viewing them.

Then, the humanoid's HealthDisplayDistance is set to 0. Setting the property
to 0 hides the healthbar completely. It is not displayed at any distance.

Finally, the humanoid's NameDisplayDistance is set to 100. This means that the
humanoid's name will be visible to other humanoid's within 100 studs.

This example should work as expected when placed inside a Script that is a
child of the humanoid.

```
local humanoid = script.Parent



humanoid.DisplayDistanceType = Enum.HumanoidDisplayDistanceType.Viewer



humanoid.HealthDisplayDistance = 0



humanoid.NameDisplayDistance = 100
```

Provide feedback

---

DisplayName

Read Parallel

Sets the text of a Humanoid, displayed above their head.

Humanoid.DisplayName:[string](/docs/luau/strings)

DisplayName is a property that determines the Humanoid's name display
when visible. By default, a new Humanoid will have the value of an empty
string. If DisplayName is an empty string, the humanoid's name display
will default to the humanoid's parent's name property.

#### Player Character Loading

When players load their character, either automatically or through the use
of [LoadCharacter()](/docs/reference/engine/classes/Player#LoadCharacter), the Humanoid that is
created by the engine will have its DisplayName property set to the
player's DisplayName property.

#### StarterCharacter and StarterHumanoid

When a [Humanoid](/docs/reference/engine/classes/Humanoid) named StarterHumanoid is parented to
[StarterPlayer](/docs/reference/engine/classes/StarterPlayer), or when a Humanoid is present in a Model named
StarterCharacter, the DisplayName property will be respected when
Characters are loaded by Players in the game. The engine will only
override the DisplayName property of the Humanoid with the DisplayName
property of the player if the [Humanoid.DisplayName](/docs/reference/engine/classes/Humanoid#DisplayName) of
StarterHumanoid is an empty string.

Provide feedback

---

EvaluateStateMachine

Read Parallel

Used to disable the internal physics and state machine of the Humanoid.

Humanoid.EvaluateStateMachine:[boolean](/docs/luau/booleans)

Used to disable the internal physics and state machine of the Humanoid.

#### What does turning this off do?

* No forces - The humanoid will not apply forces to any of its parts.
  The humanoid will not move the character in any way.
* No sensors - The humanoid will not run any spatial queries to detect
  floors, ladders, or other obstacles (such as auto-jump).
* No collision changes - The humanoid will not alter the collision
  state of any of the character parts. By default, only the torso and head
  have [Part.CanCollide](/docs/reference/engine/classes/Part#CanCollide) enabled.
* No state transitions or replication - The humanoid will not
  automatically update its state. You can still set humanoid state with a
  script, but it will not automatically replicate.

#### What does turning this off not do?

* State events - If manually setting humanoid states, the events for
  each of the humanoid's states and
  [StateChanged](/docs/reference/engine/classes/Humanoid#StateChanged) will still fire, which means
  the Animate script will still receive them and animate the character
  based on its current humanoid state.
* Appearance - [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription), clothes, accessories and
  other humanoid rendering behavior.
* Camera and player scripts - The humanoid is still linked to
  [Players](/docs/reference/engine/classes/Players) and camera scripts, which ensures the camera will
  continue to follow the [Humanoid.RootPart](/docs/reference/engine/classes/Humanoid#RootPart).
* Player input handling - The [Humanoid.MoveDirection](/docs/reference/engine/classes/Humanoid#MoveDirection) property
  will still be updated via the [Humanoid:Move()](/docs/reference/engine/classes/Humanoid#Move) function and
  [PlayerScripts](/docs/reference/engine/classes/PlayerScripts) for input.

Provide feedback

---

FloorMaterial

Read Only

Not Replicated

Read Parallel

Describes the [Enum.Material](/docs/reference/engine/enums/Material) that the [Humanoid](/docs/reference/engine/classes/Humanoid) is currently
standing on. If the [Humanoid](/docs/reference/engine/classes/Humanoid) isn't standing on anything, the value
of this property will be *Air*.

Humanoid.FloorMaterial:[Enum.Material](/docs/reference/engine/enums/Material)

This is a read-only property that describes the [Enum.Material](/docs/reference/engine/enums/Material) the
[Humanoid](/docs/reference/engine/classes/Humanoid) is currently standing on. It works with both regular
[Parts](/docs/reference/engine/classes/BasePart) and [Terrain](/docs/reference/engine/classes/Terrain) voxels.

The code sample below demonstrates how to listen to when this property
changes using [Object:GetPropertyChangedSignal()](/docs/reference/engine/classes/Object#GetPropertyChangedSignal). When the material
the humanoid is standing on changes, it will print a message indicating
the new material being stood on.

```
local Humanoid = route.to.humanoid



Humanoid:GetPropertyChangedSignal("FloorMaterial"):Connect(function()



print("New value for FloorMaterial: " .. tostring(Humanoid.FloorMaterial))



end)
```

#### Caveats

* When the [Humanoid](/docs/reference/engine/classes/Humanoid) is not standing on a floor, the value of this
  property will be set to *Air*.
  + This occurs because Enum properties cannot have an empty value.
  + This can cause some confusion if a part has its material is set to
    Air, though in practice, parts are not supposed to use that material
    in the first place.
* The character model of the [Humanoid](/docs/reference/engine/classes/Humanoid) must be able to collide with
  the floor, or else it will not be detected.
  + You cannot test if the [Humanoid](/docs/reference/engine/classes/Humanoid) is swimming with this
    property. You should instead use its [Humanoid:GetState()](/docs/reference/engine/classes/Humanoid#GetState)
    function.

Provide feedback

---

Health

Not Replicated

Read Parallel

Describes the current health of the Humanoid on the range [0,
[Humanoid.MaxHealth](/docs/reference/engine/classes/Humanoid#MaxHealth)].

Humanoid.Health:[number](/docs/luau/numbers)

This property represents the current health of the [Humanoid](/docs/reference/engine/classes/Humanoid). The
value is restricted to the range between 0 and
[MaxHealth](/docs/reference/engine/classes/Humanoid#MaxHealth). If the humanoid is dead, this
property is continually set to 0.

Note that the [TakeDamage()](/docs/reference/engine/classes/Humanoid#TakeDamage) function may be
used to subtract from [Health](/docs/reference/engine/classes/Humanoid#Health) instead of setting
the property directly.

#### Health Regeneration

By default, a passive health regeneration script is automatically inserted
into humanoids. This causes non-dead player characters to regenerate 1% of
[MaxHealth](/docs/reference/engine/classes/Humanoid#MaxHealth) each second. To disable this
regeneration behavior, add an empty [Script](/docs/reference/engine/classes/Script) named Health to
[StarterCharacterScripts](/docs/reference/engine/classes/StarterCharacterScripts).

#### Health Bar Display

When [Health](/docs/reference/engine/classes/Humanoid#Health) is less than
[MaxHealth](/docs/reference/engine/classes/Humanoid#MaxHealth), a health bar is displayed
in-experience. The display behavior of the health bar is dependent on the
[HealthDisplayDistance](/docs/reference/engine/classes/Humanoid#HealthDisplayDistance) and
[HealthDisplayType](/docs/reference/engine/classes/Humanoid#HealthDisplayType).

See
[Character Name/Health Display](/docs/characters/name-health-display)
for an in-depth guide on controlling the appearance of character names and
health bars.

#### Death

When the value of the character's health reaches 0, the [Humanoid](/docs/reference/engine/classes/Humanoid)
automatically transitions to the [Enum.HumanoidStateType.Dead](/docs/reference/engine/enums/HumanoidStateType#Dead) state. In
this state, [Health](/docs/reference/engine/classes/Humanoid#Health) is locked to 0; however, there
is no error or warning for setting the [Health](/docs/reference/engine/classes/Humanoid#Health) of a
dead humanoid to a positive nonzero value.

Provide feedback

---

HealthDisplayDistance

Read Parallel

Used in conjunction with the
[DisplayDistanceType](/docs/reference/engine/classes/Humanoid#DisplayDistanceType) property to
control the distance from which a humanoid's health bar can be seen.

Humanoid.HealthDisplayDistance:[number](/docs/luau/numbers)

This property is a number used in conjunction with the
[DisplayDistanceType](/docs/reference/engine/classes/Humanoid#DisplayDistanceType) property to
control the distance from which a humanoid's health bar can be seen.

See
[Character Name/Health Display](/docs/characters/name-health-display)
for an in-depth guide on controlling the appearance of character names and
health bars.

Provide feedback

---

HealthDisplayType

Read Parallel

Controls when the humanoid's health bar is allowed to be displayed.

Humanoid.HealthDisplayType:[Enum.HumanoidHealthDisplayType](/docs/reference/engine/enums/HumanoidHealthDisplayType)

This property controls when a humanoid's health bar is allowed to be
displayed. By default, this property is set to
[DisplayWhenDamaged](/docs/reference/engine/enums/HumanoidHealthDisplayType), which makes the
health bar only display when a humanoid's [Health](/docs/reference/engine/classes/Humanoid#Health)
is less than its [MaxHealth](/docs/reference/engine/classes/Humanoid#MaxHealth). It can also be set
to [AlwaysOn](/docs/reference/engine/enums/HumanoidHealthDisplayType), which makes the health bar
always display, or [AlwaysOff](/docs/reference/engine/enums/HumanoidHealthDisplayType), which
prevents it from ever displaying.

Note that this property functions independently of the humanoid's
[HealthDisplayDistance](/docs/reference/engine/classes/Humanoid#HealthDisplayDistance) property
which is responsible for making the health bar fade out at certain
distances. If Humanoid.HealthDisplayType|HealthDisplayType is set to
[AlwaysOn](/docs/reference/engine/enums/HumanoidHealthDisplayType), it will still fade out
depending the how
[HealthDisplayDistance](/docs/reference/engine/classes/Humanoid#HealthDisplayDistance) is
configured.

See
[Character Name/Health Display](/docs/characters/name-health-display)
for an in-depth guide on controlling the appearance of character names and
health bars.

Provide feedback

---

HipHeight

Read Parallel

Determines the distance off the ground the [Humanoid.RootPart](/docs/reference/engine/classes/Humanoid#RootPart)
should be.

Humanoid.HipHeight:[number](/docs/luau/numbers)

Determines the distance (in studs) off the ground the
[RootPart](/docs/reference/engine/classes/Humanoid#RootPart) should be when the humanoid is
standing. The [RigType](/docs/reference/engine/classes/Humanoid#RigType) influences the way this
property behaves.

For R15 rigs, a suitable hip height is preset to ensure the height of the
[RootPart](/docs/reference/engine/classes/Humanoid#RootPart) is correct. The height of the legs is
not used. The overall height of the humanoid can be described in the
following formula:

```
Height = (0.5 * RootPart.Size.Y) + HipHeight
```

For R6 rigs, [HipHeight](/docs/reference/engine/classes/Humanoid#HipHeight) instead describes a
relative offset. The overall height of the humanoid can be described in
the following formula:

```
Height = LeftLeg.Size.Y + (0.5 * RootPart.Size.Y) + HipHeight
```

Provide feedback

---

Jump

Not Replicated

Read Parallel

If true, the [Humanoid](/docs/reference/engine/classes/Humanoid) jumps with an upwards force.

Humanoid.Jump:[boolean](/docs/luau/booleans)

If true, the [Humanoid](/docs/reference/engine/classes/Humanoid) jumps with an upwards force equal to the
value of [Humanoid.JumpPower](/docs/reference/engine/classes/Humanoid#JumpPower) or the height of
[Humanoid.JumpHeight](/docs/reference/engine/classes/Humanoid#JumpHeight), depending on the value of
[Humanoid.UseJumpPower](/docs/reference/engine/classes/Humanoid#UseJumpPower).

Provide feedback

---

JumpHeight

Read Parallel

Provides control over the height that the [Humanoid](/docs/reference/engine/classes/Humanoid) jumps to.

Humanoid.JumpHeight:[number](/docs/luau/numbers)

Provides control over the height a [Humanoid](/docs/reference/engine/classes/Humanoid) jumps, in studs. The
starting value of this property is determined by the value of
[StarterPlayer.CharacterJumpHeight](/docs/reference/engine/classes/StarterPlayer#CharacterJumpHeight) which defaults to 7.2.

Although setting this property to 0 will effectively prevent the humanoid
from jumping, it's recommended to disable jumping by disabling the
[Enum.HumanoidStateType.Jumping](/docs/reference/engine/enums/HumanoidStateType#Jumping) state through
[Humanoid:SetStateEnabled()](/docs/reference/engine/classes/Humanoid#SetStateEnabled).

This property is only visible in the
[Properties](/docs/studio/properties) window if
[Humanoid.UseJumpPower](/docs/reference/engine/classes/Humanoid#UseJumpPower) is set to false, as it is not relevant
otherwise (instead, [Humanoid.JumpPower](/docs/reference/engine/classes/Humanoid#JumpPower) is used).

Provide feedback

---

JumpPower

Read Parallel

Determines how much upwards force is applied to the [Humanoid](/docs/reference/engine/classes/Humanoid) when
jumping.

Humanoid.JumpPower:[number](/docs/luau/numbers)

Determines how much upwards force is applied to the [Humanoid](/docs/reference/engine/classes/Humanoid) when
jumping. The starting value of this property is determined by the value of
[StarterPlayer.CharacterJumpPower](/docs/reference/engine/classes/StarterPlayer#CharacterJumpPower) which defaults to 50 and is
constrained between 0 and 1000. Note that jumps are also influenced by the
[Workspace.Gravity](/docs/reference/engine/classes/Workspace#Gravity) property which determines the acceleration due
to gravity.

Although setting this property to 0 will effectively prevent the humanoid
from jumping, it's recommended to disable jumping by disabling the
[Enum.HumanoidStateType.Jumping](/docs/reference/engine/enums/HumanoidStateType#Jumping) state through
[Humanoid:SetStateEnabled()](/docs/reference/engine/classes/Humanoid#SetStateEnabled).

This property is only visible in the
[Properties](/docs/studio/properties) window if
[Humanoid.UseJumpPower](/docs/reference/engine/classes/Humanoid#UseJumpPower) is set to true, as it is not relevant
otherwise (instead, [Humanoid.JumpHeight](/docs/reference/engine/classes/Humanoid#JumpHeight) is used).

Provide feedback

---

LeftLeg

Deprecated

Show details

---

MaxHealth

Read Parallel

The maximum value of a humanoid's [Health](/docs/reference/engine/classes/Humanoid#Health).

Humanoid.MaxHealth:[number](/docs/luau/numbers)

The maximum value of a humanoid's [Health](/docs/reference/engine/classes/Humanoid#Health).

The value of this property is used alongside the
[Health](/docs/reference/engine/classes/Humanoid#Health) property to size the default health bar
display. When a humanoid's [Health](/docs/reference/engine/classes/Humanoid#Health) reaches
[MaxHealth](/docs/reference/engine/classes/Humanoid#MaxHealth), its health bar may not be displayed,
depending on its [HealthDisplayType](/docs/reference/engine/classes/Humanoid#HealthDisplayType)
property.

Provide feedback

---

maxHealth

Deprecated

Show details

---

MaxSlopeAngle

Read Parallel

The maximum slope angle that a humanoid can walk on without slipping.

Humanoid.MaxSlopeAngle:[number](/docs/luau/numbers)

This property determines the maximum slope angle that a humanoid can
climb. If the angle of a slope is greater than a humanoid's MaxSlopeAngle,
they will slide down the slope.

When a character spawns, this property is set according to the value of
[StarterPlayer.CharacterMaxSlopeAngle](/docs/reference/engine/classes/StarterPlayer#CharacterMaxSlopeAngle).

The value of this property is constrained to values between 0° and 89°. It
defaults to 89°, so humanoids can climb pretty much any slope they want by
default.

Code Samples

Limiting The Slope a Humanoid Can Walk Up

The example below demonstrates the effect of the MaxSlopAngle property by
limiting the maximum slope the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) can walk up to 30°.
The local player will slide down any slope greater than 30°.

This code below works as expected when placed in a LocalScript.

```
local player = game.Players.LocalPlayer



local char = player.CharacterAdded:wait()



local h = char:FindFirstChild("Humanoid")



h.MaxSlopeAngle = 30
```

Provide feedback

---

MoveDirection

Read Only

Not Replicated

Read Parallel

Describes the direction that the [Humanoid](/docs/reference/engine/classes/Humanoid) is walking in.

Humanoid.MoveDirection:[Vector3](/docs/reference/engine/datatypes/Vector3)

MoveDirection is a read-only property that describes the direction a
[Humanoid](/docs/reference/engine/classes/Humanoid) is walking in, as a unit vector or zero length vector.
The direction is described in world space.

Because this property is read-only, it cannot be set by a [Script](/docs/reference/engine/classes/Script)
or [LocalScript](/docs/reference/engine/classes/LocalScript).

Code Samples

Walking Camera Bobble Effect

This LocalScript makes the camera bobble as the player's character walks
around, utilizing both the Humanoid's CameraOffset and MoveDirection. It
should be parented inside of the StarterCharacterScripts so that it is
distributed into a player's character as expected.

```
local RunService = game:GetService("RunService")



local playerModel = script.Parent



local humanoid = playerModel:WaitForChild("Humanoid")



local function updateBobbleEffect()



local now = tick()



if humanoid.MoveDirection.Magnitude > 0 then -- Is the character walking?



local velocity = humanoid.RootPart.Velocity



local bobble_X = math.cos(now * 9) / 5



local bobble_Y = math.abs(math.sin(now * 12)) / 5



local bobble = Vector3.new(bobble_X, bobble_Y, 0) * math.min(1, velocity.Magnitude / humanoid.WalkSpeed)



humanoid.CameraOffset = humanoid.CameraOffset:lerp(bobble, 0.25)



else



-- Scale down the CameraOffset so that it shifts back to its regular position.



humanoid.CameraOffset = humanoid.CameraOffset * 0.75



end



end



RunService.RenderStepped:Connect(updateBobbleEffect)
```

Provide feedback

---

NameDisplayDistance

Read Parallel

Used in conjunction with the [Humanoid.DisplayDistanceType](/docs/reference/engine/classes/Humanoid#DisplayDistanceType) property
to control the distance from which a humanoid's name can be seen.

Humanoid.NameDisplayDistance:[number](/docs/luau/numbers)

The NameDisplayDistance property is a number used in conjunction with
the [Humanoid.DisplayDistanceType](/docs/reference/engine/classes/Humanoid#DisplayDistanceType) property to control the distance
from which a humanoid's name can be seen.

See
[Character Name/Health Display](/docs/characters/name-health-display)
for an in-depth guide on controlling the appearance of character names and
health bars.

Provide feedback

---

NameOcclusion

Read Parallel

Controls whether a humanoid's name and health bar can be seen behind walls
or other objects.

Humanoid.NameOcclusion:[Enum.NameOcclusion](/docs/reference/engine/enums/NameOcclusion)

Controls whether a humanoid's name and health bar can be seen behind walls
or other objects. This property is a [Enum.NameOcclusion](/docs/reference/engine/enums/NameOcclusion) value and can be
configured to occlude all names, enemy names, or disable occlusion
entirely.

In cases where the [LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer) has no
[Humanoid](/docs/reference/engine/classes/Humanoid) associated with it, this property instead applies to the
subject [Humanoid](/docs/reference/engine/classes/Humanoid).

See
[Character Name/Health Display](/docs/characters/name-health-display)
for an in-depth guide on controlling the appearance of character names and
health bars.

Code Samples

Occlude Player Names

In the below example, Player|Players will not be able to see each other's
[Player.Character](/docs/reference/engine/classes/Player#Character) names when they are obscured behind
BasePart|BaseParts.

```
local Players = game:GetService("Players")



local function onCharacterAdded(character)



local humanoid = character:WaitForChild("Humanoid")



humanoid.NamOcclusion = Enum.NameOcclusion.OccludeAll



end



local function onPlayerAdded(player)



player.CharacterAdded:Connect(onCharacterAdded)



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Provide feedback

---

PlatformStand

Read Parallel

Determines whether the [Humanoid](/docs/reference/engine/classes/Humanoid) is currently in the
[Enum.HumanoidStateType.PlatformStanding](/docs/reference/engine/enums/HumanoidStateType#PlatformStanding) state.

Humanoid.PlatformStand:[boolean](/docs/luau/booleans)

Determines whether the [Humanoid](/docs/reference/engine/classes/Humanoid) is currently in the
[Enum.HumanoidStateType.PlatformStanding](/docs/reference/engine/enums/HumanoidStateType#PlatformStanding) state. When true, the Humanoid
is in a state where it is free-falling and cannot move. This state behaves
similar to sitting, except that jumping does not free the humanoid from
the state.

Provide feedback

---

RequiresNeck

Read Parallel

Allows developers to disable the behavior where a player
Character|character dies if the Neck [Motor6D](/docs/reference/engine/classes/Motor6D) is removed or
disconnected even momentarily.

Humanoid.RequiresNeck:[boolean](/docs/luau/booleans)

Allows developers to disable the behavior where a player
Character|character dies if the Neck [Motor6D](/docs/reference/engine/classes/Motor6D) is removed or
disconnected even momentarily. This property defaults to true.

Provide feedback

---

RightLeg

Deprecated

Show details

---

RigType

Read Parallel

Describes whether this [Humanoid](/docs/reference/engine/classes/Humanoid) is utilizing the legacy R6
character rig, or the new R15 character rig.

Humanoid.RigType:[Enum.HumanoidRigType](/docs/reference/engine/enums/HumanoidRigType)

RigType describes whether a [Humanoid](/docs/reference/engine/classes/Humanoid) is utilizing the legacy
R6 character rig, or the newer R15 character rig.

The R6 rig uses 6 visible [Parts](/docs/reference/engine/classes/Part) while the R15 rig uses 15
visible [Parts](/docs/reference/engine/classes/Part). R15 rigs have more joints than R6 rigs, making
them much more versatile when being animated.

Note that if this property is set incorrectly, the [Humanoid](/docs/reference/engine/classes/Humanoid) will
not function correctly. For example, if a R15 humanoid's RigType is
set to R6, the [Humanoid](/docs/reference/engine/classes/Humanoid) will die as there is no [BasePart](/docs/reference/engine/classes/BasePart)
called Torso connected to a [BasePart](/docs/reference/engine/classes/BasePart) called Head.

Provide feedback

---

RootPart

Read Only

Not Replicated

Read Parallel

A reference to the humanoid's HumanoidRootPart object.

Humanoid.RootPart:[BasePart](/docs/reference/engine/classes/BasePart)

A reference to the humanoid's HumanoidRootPart object, the root
driving part of the [Humanoid](/docs/reference/engine/classes/Humanoid) that controls a humanoid's movement
through the 3D world. This part is normally invisible.

For R15 characters, [Model.PrimaryPart](/docs/reference/engine/classes/Model#PrimaryPart) of the
[Player.Character](/docs/reference/engine/classes/Player#Character) model is set to HumanoidRootPart.

For R6 characters, [Model.PrimaryPart](/docs/reference/engine/classes/Model#PrimaryPart) is set to the Head part.

Provide feedback

---

SeatPart

Read Only

Not Replicated

Read Parallel

A reference to the seat that a [Humanoid](/docs/reference/engine/classes/Humanoid) is currently sitting in,
if any.

Humanoid.SeatPart:[BasePart](/docs/reference/engine/classes/BasePart)

SeatPart is a reference to the seat that a [Humanoid](/docs/reference/engine/classes/Humanoid) is currently
sitting in, if any. The value of this property can be either a
[Seat](/docs/reference/engine/classes/Seat), or a [VehicleSeat](/docs/reference/engine/classes/VehicleSeat). It will be *nil* if the Humanoid
is not currently sitting in a seat.

Note:

* For a bool describing if the [Humanoid](/docs/reference/engine/classes/Humanoid) is currently sitting or
  not, see [Humanoid.Sit](/docs/reference/engine/classes/Humanoid#Sit)

Provide feedback

---

Sit

Read Parallel

Describes whether the [Humanoid](/docs/reference/engine/classes/Humanoid) is currently sitting.

Humanoid.Sit:[boolean](/docs/luau/booleans)

The Sit property is a boolean that indicates whether the [Humanoid](/docs/reference/engine/classes/Humanoid)
is currently sitting. [Humanoids](/docs/reference/engine/classes/Humanoid) can be forced into a
sitting state by setting this property's value to true. If the
[Humanoid](/docs/reference/engine/classes/Humanoid) isn't attached to a seat while in its sitting state, it
will trip over with no collision in its legs. A [Humanoid](/docs/reference/engine/classes/Humanoid) can
escape from the sitting state by jumping.

Note:

* The [Seat](/docs/reference/engine/classes/Seat) or [VehicleSeat](/docs/reference/engine/classes/VehicleSeat) the [Humanoid](/docs/reference/engine/classes/Humanoid) is sitting
  on can be obtained using the [Humanoid.SeatPart](/docs/reference/engine/classes/Humanoid#SeatPart) property
* It is possible to detect when a Humanoid sits by connecting to the
  [Humanoid.Seated](/docs/reference/engine/classes/Humanoid#Seated) event.

Provide feedback

---

TargetPoint

Read Parallel

Describes the 3D position where the [Player](/docs/reference/engine/classes/Player) controlling the
[Humanoid](/docs/reference/engine/classes/Humanoid) last clicked in the world while using a [Tool](/docs/reference/engine/classes/Tool).

Humanoid.TargetPoint:[Vector3](/docs/reference/engine/datatypes/Vector3)

Do not use This property only works with Experimental Mode enabled,
which has been entirely discontinued.

This property describes a 3D position in space where the [Player](/docs/reference/engine/classes/Player)
controlling this [Humanoid](/docs/reference/engine/classes/Humanoid) last clicked with a [Tool](/docs/reference/engine/classes/Tool)
equipped.

This property is primarily used by classic tools to determine what a
humanoid is targeting when they activate a tool. If you give an NPC a
classic rocket launcher, set their TargetPoint, and then call the
tool's [Tool:Activate()](/docs/reference/engine/classes/Tool#Activate) function, you can make the NPC fire a
rocket at the target point.

Provide feedback

---

Torso

Deprecated

Show details

---

UseJumpPower

Read Parallel

Determines whether the [JumpHeight](/docs/reference/engine/classes/Humanoid#JumpHeight) (false) or
[Humanoid.JumpPower](/docs/reference/engine/classes/Humanoid#JumpPower) (true) property is used.

Humanoid.UseJumpPower:[boolean](/docs/luau/booleans)

When a character spawns, this property is set according to the value of
[StarterPlayer.CharacterUseJumpPower](/docs/reference/engine/classes/StarterPlayer#CharacterUseJumpPower), which defaults to true.

When jumping, with this set to false, the [Humanoid.JumpHeight](/docs/reference/engine/classes/Humanoid#JumpHeight)
value is used to ensure the humanoid jumps to that height. With this set
to true, the [Humanoid.JumpPower](/docs/reference/engine/classes/Humanoid#JumpPower) value is used to apply an upward
force.

Provide feedback

---

WalkSpeed

Read Parallel

Describes the humanoid's maximum movement speed in studs per second.

Humanoid.WalkSpeed:[number](/docs/luau/numbers)

This property describes how quickly the [Humanoid](/docs/reference/engine/classes/Humanoid) is able to walk,
in studs per second. It defaults to the value of
[StarterPlayer.CharacterWalkSpeed](/docs/reference/engine/classes/StarterPlayer#CharacterWalkSpeed) (16), meaning a player
character can move 16 studs in any direction each second.

#### Notes

* When controlled on a mobile device or a gamepad, a humanoid can walk
  slower than its [WalkSpeed](/docs/reference/engine/classes/Humanoid#WalkSpeed) if the controlling
  thumbstick is moved just a gradual degree from center.
* You can freeze a humanoid in place by setting
  [WalkSpeed](/docs/reference/engine/classes/Humanoid#WalkSpeed) to 0, effectively preventing the
  controlling player from moving it through the default movement
  mechanisms. Note, however, that [WalkSpeed](/docs/reference/engine/classes/Humanoid#WalkSpeed) is
  a client‑replicated property which can be modified locally, so it should
  not be used as a security mechanism or as the sole method for
  preventing humanoid movement.
* The default animation script scales a humanoid's movement animations
  based on how fast it is moving relative to the default speed of 16
  studs/second.
* The speed at which the [Humanoid](/docs/reference/engine/classes/Humanoid) is currently walking can be
  obtained using the [Running](/docs/reference/engine/classes/Humanoid#Running) event.

Provide feedback

---

WalkToPart

Read Parallel

A reference to a part whose position is trying to be reached by a
humanoid.

Humanoid.WalkToPart:[BasePart](/docs/reference/engine/classes/BasePart)

WalkToPart is a reference to a [BasePart](/docs/reference/engine/classes/BasePart) that the humanoid is
trying to reach, after having been prompted to do so via the
[MoveTo()](/docs/reference/engine/classes/Humanoid#MoveTo) method.

When WalkToPart is set and a humanoid is actively trying to reach the
part, it will keep updating its [Vector3](/docs/reference/engine/datatypes/Vector3) goal to be the position
of the part, plus the [WalkToPoint](/docs/reference/engine/classes/Humanoid#WalkToPoint) translated
in object space relative to the rotation of the part. This can be
described in Luau as:

```
goal = humanoid.WalkToPart.CFrame:PointToObjectSpace(humanoid.WalkToPoint)
```

Note that simply setting the value of WalkToPart is not sufficient to
make a humanoid start "following" a part. Call
[MoveTo()](/docs/reference/engine/classes/Humanoid#MoveTo) to initiate movement.

Provide feedback

---

WalkToPoint

Read Parallel

The position that a humanoid is trying to reach, after a call to
[Humanoid:MoveTo()](/docs/reference/engine/classes/Humanoid#MoveTo) is made.

Humanoid.WalkToPoint:[Vector3](/docs/reference/engine/datatypes/Vector3)

WalkToPoint describes the 3D position in space that a humanoid is trying
to reach, after having been prompted to do so via the
[MoveTo()](/docs/reference/engine/classes/Humanoid#MoveTo) method.

If a humanoid's [WalkToPart](/docs/reference/engine/classes/Humanoid#WalkToPart) is set, the goal is
set by transforming WalkToPoint relative to the part's position and
rotation. Otherwise, the humanoid will try to reach the 3D position
specified by WalkToPoint directly.

Note that simply setting the value of WalkToPoint is not sufficient to
make a humanoid start moving toward a point. Call
[MoveTo()](/docs/reference/engine/classes/Humanoid#MoveTo) to initiate movement.

Provide feedback

---

Methods

AddAccessory

Attaches the specified [Accessory](/docs/reference/engine/classes/Accessory) to the humanoid's parent.

Humanoid:AddAccessory(accessory:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| accessory:[Instance](/docs/reference/engine/datatypes/Instance)  The [Accessory](/docs/reference/engine/classes/Accessory) to be attached. |

Returns

()

This method attaches the specified [Accessory](/docs/reference/engine/classes/Accessory) to the humanoid's
parent.

When this method is called, an [Accessory](/docs/reference/engine/classes/Accessory) is attached to the
character by searching for an [Attachment](/docs/reference/engine/classes/Attachment) in the humanoid's parent
that shares the same name as an [Attachment](/docs/reference/engine/classes/Attachment) in the accessory's
Handle [Part](/docs/reference/engine/classes/Part). If one is found, the Handle part will be
connected to the parent of the [Attachment](/docs/reference/engine/classes/Attachment) using a [Weld](/docs/reference/engine/classes/Weld),
and the weld will be configured so the [Attachments](/docs/reference/engine/classes/Attachment)
occupy the same space.

If the required [Attachment](/docs/reference/engine/classes/Attachment) can not be found, then the
[Accessory](/docs/reference/engine/classes/Accessory) will remain parented to the humanoid's parent but it
will be unattached.

Typically, accessory welds are created on the server, but they can be
created on the client under certain circumstances. In these situations,
client-sided calls to [AddAccessory()](/docs/reference/engine/classes/Humanoid#AddAccessory) may
not always produce the desired behavior and you can use
[BuildRigFromAttachments()](/docs/reference/engine/classes/Humanoid#BuildRigFromAttachments) to
force the expected weld creation.

Code Samples

[Humanoid] AddAccessory Example

This script generates the "Clockwork's Shades" Accessory from scratch, and
then attaches it to the player's character using Humanoid.AddAccessory You
should paste this code into a regular script, and then parent it inside of the
StarterPlayer's StarterCharacterScripts folder.

```
local playerModel = script.Parent



local humanoid = playerModel:WaitForChild("Humanoid")



local clockworksShades = Instance.new("Accessory")



clockworksShades.Name = "ClockworksShades"



local handle = Instance.new("Part")



handle.Name = "Handle"



handle.Size = Vector3.new(1, 1.6, 1)



handle.Parent = clockworksShades



local faceFrontAttachment = Instance.new("Attachment")



faceFrontAttachment.Name = "FaceFrontAttachment"



faceFrontAttachment.Position = Vector3.new(0, -0.24, -0.45)



faceFrontAttachment.Parent = handle



local mesh = Instance.new("SpecialMesh")



mesh.Name = "Mesh"



mesh.Scale = Vector3.new(1, 1.3, 1)



mesh.MeshId = "rbxassetid://1577360"



mesh.TextureId = "rbxassetid://1577349"



mesh.Parent = handle



humanoid:AddAccessory(clockworksShades)
```

Provide feedback

---

AddCustomStatus

Deprecated

Show details

---

AddStatus

Deprecated

Show details

---

ApplyDescriptionAsync

Yields

Makes the character's look match that of the passed in
[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).

Humanoid:ApplyDescriptionAsync(

humanoidDescription:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription), assetTypeVerification:[Enum.AssetTypeVerification](/docs/reference/engine/enums/AssetTypeVerification)

):()

Parameters

|  |
| --- |
| humanoidDescription:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)  The [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) instance which you want to set the character to match. |
| assetTypeVerification:[Enum.AssetTypeVerification](/docs/reference/engine/enums/AssetTypeVerification) Default Value: "Default" The asset type verification mode. |

Returns

()

This yielding method makes the character's look match that of the passed
in [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription). A copy of the passed
[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) is cached as the [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)
for the [Humanoid](/docs/reference/engine/classes/Humanoid).

This method is optimized through making the assumption that only this
method is used to change the appearance of the character, and no changes
are made through other means between calls. If changes are made to the
character between calls, then this method may not make the character
reflect the passed in [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) accurately. If you want
to use this method in conjunction with other means of updating the
character, [Humanoid:ApplyDescriptionReset()](/docs/reference/engine/classes/Humanoid#ApplyDescriptionReset) will always ensure the
character reflects the passed in [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).

#### See Also

* [Humanoid:GetAppliedDescription()](/docs/reference/engine/classes/Humanoid#GetAppliedDescription) which returns the
  [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) currently applied to the humanoid.
* [Players:GetHumanoidDescriptionFromUserId()](/docs/reference/engine/classes/Players#GetHumanoidDescriptionFromUserId) which returns a
  [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) describing the avatar for the passed in
  user.
* [Players:GetHumanoidDescriptionFromOutfitId()](/docs/reference/engine/classes/Players#GetHumanoidDescriptionFromOutfitId) which returns a
  [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) whose parameters are initialized to match
  that of the passed in server-side outfit asset.
* [Player:LoadCharacterWithHumanoidDescription()](/docs/reference/engine/classes/Player#LoadCharacterWithHumanoidDescription) which spawns a
  player with the look from the passed in [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).

Provide feedback

---

ApplyDescription

Deprecated

Show details

---

ApplyDescriptionResetAsync

Yields

Makes the character's look match that of the passed in
[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription), even after external changes.

Humanoid:ApplyDescriptionResetAsync(

humanoidDescription:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription), assetTypeVerification:[Enum.AssetTypeVerification](/docs/reference/engine/enums/AssetTypeVerification)

):()

Parameters

|  |
| --- |
| humanoidDescription:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)  The [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) instance which you want to set the character to match. |
| assetTypeVerification:[Enum.AssetTypeVerification](/docs/reference/engine/enums/AssetTypeVerification) Default Value: "Default" The asset type verification mode. |

Returns

()

This yielding method makes the character's look match that of the passed
in [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription), even after external changes. A copy of the
passed [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) is cached as the
[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) for the [Humanoid](/docs/reference/engine/classes/Humanoid).

This method will always ensure the character reflects the passed in
[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription), even if changes have been made to the
character not using the [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) system (for example
not using [ApplyDescriptionReset()](/docs/reference/engine/classes/Humanoid#ApplyDescriptionReset)
or [ApplyDescription()](/docs/reference/engine/classes/Humanoid#ApplyDescription)). This is in
contrast to [ApplyDescription()](/docs/reference/engine/classes/Humanoid#ApplyDescription) which
is optimized and may incorrectly apply a [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) if
the character has been changed by means other than through the
[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) system.

Provide feedback

---

ApplyDescriptionReset

Deprecated

Show details

---

BuildRigFromAttachments

Assembles a tree of [Motor6D](/docs/reference/engine/classes/Motor6D) joints by attaching together
[Attachment](/docs/reference/engine/classes/Attachment) objects in a humanoid's character.

Humanoid:BuildRigFromAttachments():()

Returns

()

This method assembles a tree of [Motor6D](/docs/reference/engine/classes/Motor6D) joints for the
[Humanoid](/docs/reference/engine/classes/Humanoid). [Motor6D](/docs/reference/engine/classes/Motor6D) joints are required for the playback of
[Animations](/docs/reference/engine/classes/Animation).

Starting from the humanoid's [RootPart](/docs/reference/engine/classes/Humanoid#RootPart), this
method collects all [Attachments](/docs/reference/engine/classes/Attachment) parented in the current
part whose name ends with RigAttachment. It then searches for a
matching attachment in the character that shares the same name as the
attachment. Using those two attachments, a [Motor6D](/docs/reference/engine/classes/Motor6D) joint is
generated based on the parts associated with the two attachments and the
[CFrame](/docs/reference/engine/classes/Attachment#CFrame) of the attachments.

[Humanoid:BuildRigFromAttachments()](/docs/reference/engine/classes/Humanoid#BuildRigFromAttachments) also scales the character and
sets body colors.

Code Samples

Lua Port of BuildRigFromAttachments

A Lua port of the Humanoid's BuildRigFromAttachments function, so that the
recursive behavior of the function can be seen.

```
local function createJoint(jointName, att0, att1)



local part0, part1 = att0.Parent, att1.Parent



local newMotor = part1:FindFirstChild(jointName)



if not (newMotor and newMotor:IsA("Motor6D")) then



newMotor = Instance.new("Motor6D")



end



newMotor.Name = jointName



newMotor.Part0 = part0



newMotor.Part1 = part1



newMotor.C0 = att0.CFrame



newMotor.C1 = att1.CFrame



newMotor.Parent = part1



end



local function buildJointsFromAttachments(part, characterParts)



if not part then



return



end



-- first, loop thru all of the part's children to find attachments



for _, attachment in pairs(part:GetChildren()) do



if attachment:IsA("Attachment") then



-- only do joint build from "RigAttachments"



local attachmentName = attachment.Name



local findPos = attachmentName:find("RigAttachment")



if findPos then



-- also don't make double joints (there is the same named



-- rigattachment under two parts)



local jointName = attachmentName:sub(1, findPos - 1)



if not part:FindFirstChild(jointName) then



-- try to find other part with same rig attachment name



for _, characterPart in pairs(characterParts) do



if part ~= characterPart then



local matchingAttachment = characterPart:FindFirstChild(attachmentName)



if matchingAttachment and matchingAttachment:IsA("Attachment") then



createJoint(jointName, attachment, matchingAttachment)



buildJointsFromAttachments(characterPart, characterParts)



break



end



end



end



end



end



end



end



end



local function buildRigFromAttachments(humanoid)



local rootPart = humanoid.RootPart



assert(rootPart, "Humanoid has no HumanoidRootPart.")



local characterParts = {}



for _, descendant in ipairs(humanoid.Parent:GetDescendants()) do



if descendant:IsA("BasePart") then



table.insert(characterParts, descendant)



end



end



buildJointsFromAttachments(rootPart, characterParts)



end



local humanoid = script.Parent:WaitForChild("Humanoid")



buildRigFromAttachments(humanoid)
```

R15 Package Importer

A script that generates an R15 character from scratch using a package's
assetId.

```
local AssetService = game:GetService("AssetService")



local InsertService = game:GetService("InsertService")



local MarketplaceService = game:GetService("MarketplaceService")



local PACKAGE_ASSET_ID = 193700907 -- Circuit Breaker



local function addAttachment(part, name, position, orientation)



local attachment = Instance.new("Attachment")



attachment.Name = name



attachment.Parent = part



if position then



attachment.Position = position



end



if orientation then



attachment.Orientation = orientation



end



return attachment



end



local function createBaseCharacter()



local character = Instance.new("Model")



local humanoid = Instance.new("Humanoid")



humanoid.Parent = character



local rootPart = Instance.new("Part")



rootPart.Name = "HumanoidRootPart"



rootPart.Size = Vector3.new(2, 2, 1)



rootPart.Transparency = 1



rootPart.Parent = character



addAttachment(rootPart, "RootRigAttachment")



local head = Instance.new("Part")



head.Name = "Head"



head.Size = Vector3.new(2, 1, 1)



head.Parent = character



local headMesh = Instance.new("SpecialMesh")



headMesh.Scale = Vector3.new(1.25, 1.25, 1.25)



headMesh.MeshType = Enum.MeshType.Head



headMesh.Parent = head



local face = Instance.new("Decal")



face.Name = "face"



face.Texture = "rbxasset://textures/face.png"



face.Parent = head



addAttachment(head, "FaceCenterAttachment")



addAttachment(head, "FaceFrontAttachment", Vector3.new(0, 0, -0.6))



addAttachment(head, "HairAttachment", Vector3.new(0, 0.6, 0))



addAttachment(head, "HatAttachment", Vector3.new(0, 0.6, 0))



addAttachment(head, "NeckRigAttachment", Vector3.new(0, -0.5, 0))



return character, humanoid



end



local function createR15Package(packageAssetId)



local packageAssetInfo = MarketplaceService:GetProductInfo(packageAssetId)



local character, humanoid = createBaseCharacter()



character.Name = packageAssetInfo.Name



local assetIds = AssetService:GetAssetIdsForPackage(packageAssetId)



for _, assetId in pairs(assetIds) do



local limb = InsertService:LoadAsset(assetId)



local r15 = limb:FindFirstChild("R15")



if r15 then



for _, part in pairs(r15:GetChildren()) do



part.Parent = character



end



else



for _, child in pairs(limb:GetChildren()) do



child.Parent = character



end



end



end



humanoid:BuildRigFromAttachments()



return character



end



local r15Package = createR15Package(PACKAGE_ASSET_ID)



r15Package.Parent = workspace
```

Provide feedback

---

ChangeState

Sets the [Humanoid](/docs/reference/engine/classes/Humanoid) to enter the given [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType).

Humanoid:ChangeState(state:[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType)):()

Parameters

|  |
| --- |
| state:[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType) Default Value: "None" The [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType) that the [Humanoid](/docs/reference/engine/classes/Humanoid) is to perform. |

Returns

()

This method causes the [Humanoid](/docs/reference/engine/classes/Humanoid) to enter the given
[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType), describing the activity the [Humanoid](/docs/reference/engine/classes/Humanoid) is
currently doing.

Please review the [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType) page for more information on
the particular states, as some have unintuitive names. For example,
[Enum.HumanoidStateType.Running](/docs/reference/engine/enums/HumanoidStateType#Running) describes a state where the humanoid's
legs are on the ground, including when stationary.

Due to the default behavior of the [Humanoid](/docs/reference/engine/classes/Humanoid), some states will
automatically be changed when set. For example:

* Setting the state to [Enum.HumanoidStateType.Swimming](/docs/reference/engine/enums/HumanoidStateType#Swimming) when the humanoid
  is not in the water will cause it to be automatically set to
  [Enum.HumanoidStateType.GettingUp](/docs/reference/engine/enums/HumanoidStateType#GettingUp).
* As it is unused, setting the state to
  [Enum.HumanoidStateType.PlatformStanding](/docs/reference/engine/enums/HumanoidStateType#PlatformStanding) will cause the humanoid state
  to be automatically set to [Enum.HumanoidStateType.Running](/docs/reference/engine/enums/HumanoidStateType#Running).

Note that in order to set the [Humanoid](/docs/reference/engine/classes/Humanoid) state using this method,
you must do so from a [LocalScript](/docs/reference/engine/classes/LocalScript) and the client must have
[network ownership](/docs/physics/network-ownership) of the
[Player.Character](/docs/reference/engine/classes/Player#Character). Alternatively, you can call this method from a
server-side [Script](/docs/reference/engine/classes/Script), but the server must have network ownership of
the player character.

See also [Humanoid:SetStateEnabled()](/docs/reference/engine/classes/Humanoid#SetStateEnabled) to enable or disable a
particular state, and [Humanoid:GetState()](/docs/reference/engine/classes/Humanoid#GetState) to get the current
humanoid state.

Code Samples

Double Jump

This code, when placed inside a [LocalScript](/docs/reference/engine/classes/LocalScript) in
[StarterPlayer.StarterCharacterScripts](/docs/reference/engine/classes/StarterPlayer#StarterCharacterScripts), will allow the player's
character to perform a double jump.

```
local UserInputService = game:GetService("UserInputService")



local character = script.Parent



local humanoid = character:WaitForChild("Humanoid")



local doubleJumpEnabled = false



humanoid.StateChanged:Connect(function(_oldState, newState)



if newState == Enum.HumanoidStateType.Jumping then



if not doubleJumpEnabled then



task.wait(0.2)



if humanoid:GetState() == Enum.HumanoidStateType.Freefall then



doubleJumpEnabled = true



end



end



elseif newState == Enum.HumanoidStateType.Landed then



doubleJumpEnabled = false



end



end)



UserInputService.InputBegan:Connect(function(inputObject)



if inputObject.KeyCode == Enum.KeyCode.Space then



if doubleJumpEnabled then



if humanoid:GetState() ~= Enum.HumanoidStateType.Jumping then



humanoid:ChangeState(Enum.HumanoidStateType.Jumping)



task.spawn(function()



doubleJumpEnabled = false



end)



end



end



end



end)
```

Provide feedback

---

EquipTool

Makes the [Humanoid](/docs/reference/engine/classes/Humanoid) equip the given [Tool](/docs/reference/engine/classes/Tool).

Humanoid:EquipTool(tool:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| tool:[Instance](/docs/reference/engine/datatypes/Instance)  The [Tool](/docs/reference/engine/classes/Tool) to equip. |

Returns

()

This method makes the [Humanoid](/docs/reference/engine/classes/Humanoid) equip the given [Tool](/docs/reference/engine/classes/Tool).

When this method is called, the [Humanoid](/docs/reference/engine/classes/Humanoid) will first automatically
unequip all [Tools](/docs/reference/engine/classes/Tool) that it currently has equipped.

Although they will be equipped, [Tools](/docs/reference/engine/classes/Tool) for which
[Tool.RequiresHandle](/docs/reference/engine/classes/Tool#RequiresHandle) is true will not function if they have no
handle, regardless if this method is used to equip them or not.

See also [Humanoid:UnequipTools()](/docs/reference/engine/classes/Humanoid#UnequipTools).

Provide feedback

---

GetAccessories

Returns an array of [Accessory](/docs/reference/engine/classes/Accessory) objects that the humanoid's parent
is currently wearing.

Humanoid:GetAccessories():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

An array of [Accessory](/docs/reference/engine/classes/Accessory) objects that are parented to the
humanoid's parent.

This method returns an array of [Accessory](/docs/reference/engine/classes/Accessory) objects that the
humanoid's parent is currently wearing. All such [Accessory](/docs/reference/engine/classes/Accessory) objects
will be included, regardless of whether they're attached or not.

If the [Humanoid](/docs/reference/engine/classes/Humanoid) has no [Accessory](/docs/reference/engine/classes/Accessory) objects, an empty array
will be returned.

See also [Humanoid:AddAccessory()](/docs/reference/engine/classes/Humanoid#AddAccessory) to attach an [Accessory](/docs/reference/engine/classes/Accessory) to
a humanoid's parent.

Code Samples

Remove Accessories After Loading

This code sample will wait for accessories to fully load, print out
how many there are, and then destroy them all.

```
local Players = game:GetService("Players")



local function onPlayerAddedAsync(player)



local connection = player.CharacterAppearanceLoaded:Connect(function(character)



-- All accessories have loaded at this point



local humanoid = character:FindFirstChildOfClass("Humanoid")



local numAccessories = #humanoid:GetAccessories()



print(("Destroying %d accessories for %s"):format(numAccessories, player.Name))



humanoid:RemoveAccessories()



end)



-- Make sure we disconnect our connection to the player after they leave



-- to allow the player to get garbage collected



player.AncestryChanged:Wait()



connection:Disconnect()



end



for _, player in Players:GetPlayers() do



task.spawn(onPlayerAddedAsync, player)



end



Players.PlayerAdded:Connect(onPlayerAddedAsync)
```

Provide feedback

---

GetAppliedDescription

Returns a copy of the humanoid's cached [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) which
describes its current look.

Humanoid:GetAppliedDescription():[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)

Returns

[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)

This method returns a copy of the humanoid's cached
[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) which describes its current look. This can be
used to quickly determine a character's look and to assign their look to
other characters using the [Humanoid:ApplyDescription()](/docs/reference/engine/classes/Humanoid#ApplyDescription) method.

#### See Also

* [Players:GetHumanoidDescriptionFromUserId()](/docs/reference/engine/classes/Players#GetHumanoidDescriptionFromUserId) which returns a
  [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) describing the avatar for the passed in
  user.
* [Players:GetHumanoidDescriptionFromOutfitId()](/docs/reference/engine/classes/Players#GetHumanoidDescriptionFromOutfitId) which returns a
  [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) whose parameters are initialized to match
  that of the passed in server-side outfit asset.
* [Player:LoadCharacterWithHumanoidDescription()](/docs/reference/engine/classes/Player#LoadCharacterWithHumanoidDescription) which spawns a
  player with the look from the passed in [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).

Provide feedback

---

GetBodyPartR15

Pass a body part to this method (the body part should be a sibling of
Humanoid, and a child of a Model) to get the [Enum.BodyPartR15](/docs/reference/engine/enums/BodyPartR15) of the
[Part](/docs/reference/engine/classes/Part).

Humanoid:GetBodyPartR15(part:[Instance](/docs/reference/engine/datatypes/Instance)):[Enum.BodyPartR15](/docs/reference/engine/enums/BodyPartR15)

Parameters

|  |
| --- |
| part:[Instance](/docs/reference/engine/datatypes/Instance)  The specified part being checked to see if it is an R15 body part. |

Returns

[Enum.BodyPartR15](/docs/reference/engine/enums/BodyPartR15)

The specified part's R15 body part type or unknown if the part is not
a body part.

This method returns what [Enum.BodyPartR15](/docs/reference/engine/enums/BodyPartR15) a [Part](/docs/reference/engine/classes/Part) is, or
[Enum.BodyPartR15.Unknown](/docs/reference/engine/enums/BodyPartR15#Unknown) if the part is not an R15 body part. This
method allows developers to retrieve player body parts independent of what
the actual body part names are, instead returning an enum.

It can be used in conjunction with [Humanoid:ReplaceBodyPartR15()](/docs/reference/engine/classes/Humanoid#ReplaceBodyPartR15).
For example, if a player's body part touches something, this function will
return get a part instance. Developers can then look up what part of the
body that was, like head or arm. Then depending on what that part was,
developers can either perform some gameplay action or replace that part
with some other part - perhaps showing damage.

This method can be useful for games where hit location is important. For
example, it can be used to determine if a player is hit in the leg and
then slow them down based on the injury.

Provide feedback

---

GetLimb

Returns the [Enum.Limb](/docs/reference/engine/enums/Limb) enum that is associated with the given
[Part](/docs/reference/engine/classes/Part).

Humanoid:GetLimb(part:[Instance](/docs/reference/engine/datatypes/Instance)):[Enum.Limb](/docs/reference/engine/enums/Limb)

Parameters

|  |
| --- |
| part:[Instance](/docs/reference/engine/datatypes/Instance)  The [Part](/docs/reference/engine/classes/Part) for which the [Enum.Limb](/docs/reference/engine/enums/Limb) is to be retrieved. |

Returns

[Enum.Limb](/docs/reference/engine/enums/Limb)

The [Enum.Limb](/docs/reference/engine/enums/Limb) the part corresponds with.

This method returns the [Enum.Limb](/docs/reference/engine/enums/Limb) enum that is associated with the given
[Part](/docs/reference/engine/classes/Part). It works for both R15 and R6 rigs, for example:

```
-- For R15



print(humanoid:GetLimb(character.LeftUpperLeg))  -- Enum.Limb.LeftLeg



print(humanoid:GetLimb(character.LeftLowerLeg))  -- Enum.Limb.LeftLeg



print(humanoid:GetLimb(character.LeftFoot))  -- Enum.Limb.LeftLeg



-- For R6



print(humanoid:GetLimb(character:FindFirstChild("Left Leg")))  -- Enum.Limb.LeftLeg
```

Note that [Humanoid:GetLimb()](/docs/reference/engine/classes/Humanoid#GetLimb) will throw an error if the part's
parent is not set to the humanoid's parent.

Code Samples

Getting a Humanoid's Limbs

Put this in a LocalScript. The output will vary based on if the humanoid is R6
or R15.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local character = player.Character or player.CharacterAdded:Wait()



local humanoid = character:WaitForChild("Humanoid")



for _, child in pairs(character:GetChildren()) do



local limb = humanoid:GetLimb(child)



if limb ~= Enum.Limb.Unknown then



print(child.Name .. " is part of limb " .. limb.Name)



end



end
```

Provide feedback

---

GetMoveVelocity

Humanoid:GetMoveVelocity():[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

Provide feedback

---

GetPlayingAnimationTracks

Deprecated

Show details

---

GetState

Write Parallel

Returns the humanoid's current [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType).

Humanoid:GetState():[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType)

Returns

[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType)

The current [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType) of the [Humanoid](/docs/reference/engine/classes/Humanoid).

This method returns the humanoid's current [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType),
describing the activity the [Humanoid](/docs/reference/engine/classes/Humanoid) is currently doing, such as
jumping or swimming.

See also [Humanoid:SetStateEnabled()](/docs/reference/engine/classes/Humanoid#SetStateEnabled) to enable or disable a
particular state, and [Humanoid:ChangeState()](/docs/reference/engine/classes/Humanoid#ChangeState) to change the current
humanoid state.

Code Samples

Double Jump

This code, when placed inside a [LocalScript](/docs/reference/engine/classes/LocalScript) in
[StarterPlayer.StarterCharacterScripts](/docs/reference/engine/classes/StarterPlayer#StarterCharacterScripts), will allow the player's
character to perform a double jump.

```
local UserInputService = game:GetService("UserInputService")



local character = script.Parent



local humanoid = character:WaitForChild("Humanoid")



local doubleJumpEnabled = false



humanoid.StateChanged:Connect(function(_oldState, newState)



if newState == Enum.HumanoidStateType.Jumping then



if not doubleJumpEnabled then



task.wait(0.2)



if humanoid:GetState() == Enum.HumanoidStateType.Freefall then



doubleJumpEnabled = true



end



end



elseif newState == Enum.HumanoidStateType.Landed then



doubleJumpEnabled = false



end



end)



UserInputService.InputBegan:Connect(function(inputObject)



if inputObject.KeyCode == Enum.KeyCode.Space then



if doubleJumpEnabled then



if humanoid:GetState() ~= Enum.HumanoidStateType.Jumping then



humanoid:ChangeState(Enum.HumanoidStateType.Jumping)



task.spawn(function()



doubleJumpEnabled = false



end)



end



end



end



end)
```

Provide feedback

---

GetStateEnabled

Write Parallel

Returns whether a [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType) is enabled for the
[Humanoid](/docs/reference/engine/classes/Humanoid).

Humanoid:GetStateEnabled(state:[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| state:[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType)  The given [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType). |

Returns

[boolean](/docs/luau/booleans)

Whether the given [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType) is enabled.

The GetStateEnabled method returns whether a [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType) is
enabled for the [Humanoid](/docs/reference/engine/classes/Humanoid).

The humanoid state describes the activity the humanoid is currently doing.

When a particular [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType) is disabled, the humanoid can
never enter that state. This is true regardless if the attempt to change
state is made using [Humanoid:ChangeState()](/docs/reference/engine/classes/Humanoid#ChangeState) or Roblox internal
humanoid code.

See also:

* For an event that fires when a humanoid state is enabled or disabled see
  [Humanoid.StateEnabledChanged](/docs/reference/engine/classes/Humanoid#StateEnabledChanged)
* To enable or disable a [Humanoid](/docs/reference/engine/classes/Humanoid) state use
  [Humanoid:SetStateEnabled()](/docs/reference/engine/classes/Humanoid#SetStateEnabled)

Code Samples

Setting and Getting Humanoid States

The code below sets the value of the
[humanoid jumping state](/docs/reference/engine/enums/HumanoidStateType) to *false* using
[Humanoid:SetStateEnabled()](/docs/reference/engine/classes/Humanoid#SetStateEnabled) and then retrieves and prints the value of
this state (*false*) using [Humanoid:GetStateEnabled()](/docs/reference/engine/classes/Humanoid#GetStateEnabled).

```
local humanoid = script.Parent:WaitForChild("Humanoid")



-- Set state



humanoid:SetStateEnabled(Enum.HumanoidStateType.Jumping, false)



-- Get state



print(humanoid:GetStateEnabled(Enum.HumanoidStateType.Jumping)) -- false
```

Provide feedback

---

GetStatuses

Deprecated

Show details

---

HasCustomStatus

Deprecated

Show details

---

HasStatus

Deprecated

Show details

---

LoadAnimation

Deprecated

Show details

---

loadAnimation

Deprecated

Show details

---

Move

Causes the [Humanoid](/docs/reference/engine/classes/Humanoid) to walk in the given direction.

Humanoid:Move(

moveDirection:[Vector3](/docs/reference/engine/datatypes/Vector3), relativeToCamera:[boolean](/docs/luau/booleans)

):()

Parameters

|  |
| --- |
| moveDirection:[Vector3](/docs/reference/engine/datatypes/Vector3)  The direction to walk in. |
| relativeToCamera:[boolean](/docs/luau/booleans) Default Value: false Set to true if the moveDirection parameter should be taken as relative to the [CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera). |

Returns

()

This method causes the [Humanoid](/docs/reference/engine/classes/Humanoid) to walk in the given
[Vector3](/docs/reference/engine/datatypes/Vector3) direction.

By default, the direction is in world terms, but if the relativeToCamera
parameter is true, the direction is relative to the [CFrame](/docs/reference/engine/datatypes/CFrame) of
the [CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera). As the negative Z
direction is considered "forwards" in Roblox, the following code will make
the humanoid walk in the direction of the
[CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera).

```
humanoid:Move(Vector3.new(0, 0, -1), true)
```

When this method is called, the [Humanoid](/docs/reference/engine/classes/Humanoid) will move until the
method is called again. However, this method will be overwritten in the
next frame by Roblox's default character control script. This can be
avoided by either calling this function every frame using
[RunService:BindToRenderStep()](/docs/reference/engine/classes/RunService#BindToRenderStep) (see example), or overwriting the
control scripts in [StarterPlayerScripts](/docs/reference/engine/classes/StarterPlayerScripts).

This method can be called on the server, but this should only be done when
the server has [network ownership](/docs/physics/network-ownership)
of the humanoid's assembly.

See also [Humanoid:MoveTo()](/docs/reference/engine/classes/Humanoid#MoveTo) which makes a[Humanoid](/docs/reference/engine/classes/Humanoid) walk to a
point, and [Player:Move()](/docs/reference/engine/classes/Player#Move) which effectively calls this function.

Code Samples

Moving a Humanoid Forwards

This code sample uses the [Humanoid:Move()](/docs/reference/engine/classes/Humanoid#Move) function to make the
player's [Character](/docs/reference/engine/classes/Player#Character) walk in the direction of the
[Camera](/docs/reference/engine/classes/Camera). [RunService:BindToRenderStep()](/docs/reference/engine/classes/RunService#BindToRenderStep) is required here as the
default control scripts will overwrite the player's movement every frame.

To run this sample, place it inside a [LocalScript](/docs/reference/engine/classes/LocalScript) parented to
[StarterCharacterScripts](/docs/reference/engine/classes/StarterCharacterScripts).

```
local RunService = game:GetService("RunService")



local Players = game:GetService("Players")



local player = Players.LocalPlayer



RunService:BindToRenderStep("move", Enum.RenderPriority.Character.Value + 1, function()



if player.Character then



local humanoid = player.Character:FindFirstChild("Humanoid")



if humanoid then



humanoid:Move(Vector3.new(0, 0, -1), true)



end



end



end)
```

Provide feedback

---

MoveTo

Causes the [Humanoid](/docs/reference/engine/classes/Humanoid) to attempt to walk to the given location by
setting the [Humanoid.WalkToPoint](/docs/reference/engine/classes/Humanoid#WalkToPoint) and [Humanoid.WalkToPart](/docs/reference/engine/classes/Humanoid#WalkToPart)
properties.

Humanoid:MoveTo(

location:[Vector3](/docs/reference/engine/datatypes/Vector3), part:[Instance](/docs/reference/engine/datatypes/Instance)

):()

Parameters

|  |
| --- |
| location:[Vector3](/docs/reference/engine/datatypes/Vector3)  The position to set [Humanoid.WalkToPoint](/docs/reference/engine/classes/Humanoid#WalkToPoint) to. |
| part:[Instance](/docs/reference/engine/datatypes/Instance) Default Value: "nil" The [BasePart](/docs/reference/engine/classes/BasePart) to set [Humanoid.WalkToPart](/docs/reference/engine/classes/Humanoid#WalkToPart) to. |

Returns

()

This method causes the [Humanoid](/docs/reference/engine/classes/Humanoid) to attempt to walk to a given
location by setting the [WalkToPoint](/docs/reference/engine/classes/Humanoid#WalkToPoint) and
[WalkToPart](/docs/reference/engine/classes/Humanoid#WalkToPart) properties, corresponding to the
location and part parameters.

If the part parameter is specified, the [Humanoid](/docs/reference/engine/classes/Humanoid) will still
attempt to walk to the location parameter's point. However, if the
part moves, the point will move to be at the same position relative to
the part.

Note that the movement operation will time out after 8 seconds if the
humanoid doesn't reach its goal (this timeout exists so that humanoids do
not get stuck waiting for [MoveToFinished](/docs/reference/engine/classes/Humanoid#MoveToFinished)
to fire). If you don't want this to happen, call MoveTo() at a repeated
interval so that the timeout keeps resetting.

[MoveTo()](/docs/reference/engine/classes/Humanoid#MoveTo) ends if any of the following conditions
apply:

* The character arrives at its destination, assuming a ~1 stud threshold
  to account for various humanoid speeds and framerates.
* The character gets stuck and the timer expires.
* The value of either [WalkToPoint](/docs/reference/engine/classes/Humanoid#WalkToPoint) or
  [WalkToPart](/docs/reference/engine/classes/Humanoid#WalkToPart) changes.
* A script calls [Move()](/docs/reference/engine/classes/Humanoid#Move) with a new moveDirection
  parameter.
* A script changes the [CFrame](/docs/reference/engine/classes/BasePart#CFrame) property of the
  humanoid's [RootPart](/docs/reference/engine/classes/Humanoid#RootPart).

Code Samples

Humanoid MoveTo Without Time out

This code sample includes a function that avoids the timeout on
[Humanoid:MoveTo()](/docs/reference/engine/classes/Humanoid#MoveTo) by calling [Humanoid:MoveTo()](/docs/reference/engine/classes/Humanoid#MoveTo) again before
the timeout elapses. It also includes an optional andThen parameter for which
you can pass a function to be called when the humanoid reaches its
destination.

```
local function moveTo(humanoid, targetPoint, andThen)



local targetReached = false



-- listen for the humanoid reaching its target



local connection



connection = humanoid.MoveToFinished:Connect(function(reached)



targetReached = true



connection:Disconnect()



connection = nil



if andThen then



andThen(reached)



end



end)



-- start walking



humanoid:MoveTo(targetPoint)



-- execute on a new thread so as to not yield function



task.spawn(function()



while not targetReached do



-- does the humanoid still exist?



if not (humanoid and humanoid.Parent) then



break



end



-- has the target changed?



if humanoid.WalkToPoint ~= targetPoint then



break



end



-- refresh the timeout



humanoid:MoveTo(targetPoint)



task.wait(6)



end



-- disconnect the connection if it is still connected



if connection then



connection:Disconnect()



connection = nil



end



end)



end



local function andThen(reached)



print((reached and "Destination reached!") or "Failed to reach destination!")



end



moveTo(script.Parent:WaitForChild("Humanoid"), Vector3.new(50, 0, 50), andThen)
```

Provide feedback

---

PlayEmoteAsync

Yields

Plays emotes and returns if was successfully ran.

Humanoid:PlayEmoteAsync(emoteName:[string](/docs/luau/strings)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| emoteName:[string](/docs/luau/strings)  name of the emote to play. |

Returns

[boolean](/docs/luau/booleans)

successfully played.

If the emote could not be played because the emoteName is not found in the
HumanoidDescription, this method will give an error. The method will
return true to indicate that the emote was played successfully.

Provide feedback

---

PlayEmote

Deprecated

Show details

---

RemoveAccessories

Removes all [Accessory](/docs/reference/engine/classes/Accessory) objects worn by the humanoid's parent.

Humanoid:RemoveAccessories():()

Returns

()

This method removes all [Accessory](/docs/reference/engine/classes/Accessory) objects worn by the humanoid's
parent. For player [Characters](/docs/reference/engine/classes/Player#Character), this will remove
all hats and other accessories.

This method removes [Accessory](/docs/reference/engine/classes/Accessory) object by calling
[Instance:Destroy()](/docs/reference/engine/classes/Instance#Destroy) on them, meaning the
[Parent](/docs/reference/engine/classes/Instance#Parent) of the accessories are set to nil and
locked.

See also [Humanoid:AddAccessory()](/docs/reference/engine/classes/Humanoid#AddAccessory) to attach an [Accessory](/docs/reference/engine/classes/Accessory),
and [Humanoid:GetAccessories()](/docs/reference/engine/classes/Humanoid#GetAccessories) to get all [Accessory](/docs/reference/engine/classes/Accessory) objects
belonging to a [Humanoid](/docs/reference/engine/classes/Humanoid).

Code Samples

Remove Accessories After Loading

This code sample will wait for accessories to fully load, print out
how many there are, and then destroy them all.

```
local Players = game:GetService("Players")



local function onPlayerAddedAsync(player)



local connection = player.CharacterAppearanceLoaded:Connect(function(character)



-- All accessories have loaded at this point



local humanoid = character:FindFirstChildOfClass("Humanoid")



local numAccessories = #humanoid:GetAccessories()



print(("Destroying %d accessories for %s"):format(numAccessories, player.Name))



humanoid:RemoveAccessories()



end)



-- Make sure we disconnect our connection to the player after they leave



-- to allow the player to get garbage collected



player.AncestryChanged:Wait()



connection:Disconnect()



end



for _, player in Players:GetPlayers() do



task.spawn(onPlayerAddedAsync, player)



end



Players.PlayerAdded:Connect(onPlayerAddedAsync)
```

Provide feedback

---

RemoveCustomStatus

Deprecated

Show details

---

RemoveStatus

Deprecated

Show details

---

ReplaceBodyPartR15

Dynamically replaces a Humanoid body part with a different part.

Humanoid:ReplaceBodyPartR15(

bodyPart:[Enum.BodyPartR15](/docs/reference/engine/enums/BodyPartR15), part:[BasePart](/docs/reference/engine/classes/BasePart)

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| bodyPart:[Enum.BodyPartR15](/docs/reference/engine/enums/BodyPartR15)  The body part to replace. [Enum.BodyPartR15.Unknown](/docs/reference/engine/enums/BodyPartR15#Unknown) will fail. |
| part:[BasePart](/docs/reference/engine/classes/BasePart)  The [Part](/docs/reference/engine/classes/Part) [Instance](/docs/reference/engine/classes/Instance) which will be parented to the character. |

Returns

[boolean](/docs/luau/booleans)

Dynamically replaces a R15/Rthro limb part in a Humanoid with a different
part. The part is automatically scaled as normal.

This method is useful for modifying characters during gameplay or building
characters from a base rig. The related method
[GetBodyPartR15](/docs/reference/engine/classes/Humanoid#GetBodyPartR15) can come in handy when
using this method.

The name of the part passed in should match with the name of the
BodyPartR15 Enum passed in.

Provide feedback

---

SetStateEnabled

Sets whether a given [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType) is enabled for the
[Humanoid](/docs/reference/engine/classes/Humanoid).

Humanoid:SetStateEnabled(

state:[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType), enabled:[boolean](/docs/luau/booleans)

):()

Parameters

|  |
| --- |
| state:[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType)  The [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType) to be enabled or disabled. |
| enabled:[boolean](/docs/luau/booleans)  true if state is to be enabled, false if state is to be disabled. |

Returns

()

This method sets whether a given [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType) is enabled for
the [Humanoid](/docs/reference/engine/classes/Humanoid). When a particular [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType) is
disabled, the [Humanoid](/docs/reference/engine/classes/Humanoid) can never enter that state. This is true
regardless if the attempt to change state is made using
[Humanoid:ChangeState()](/docs/reference/engine/classes/Humanoid#ChangeState) or Roblox internal [Humanoid](/docs/reference/engine/classes/Humanoid) code.

Note that using SetStateEnabled() on the server does not replicate the
change to the client, nor vice-versa.

Code Samples

Jump Cooldown

The following sample will require a one second cooldown after a Humanoid has
landed before it is able to jump again.

To try this sample, place it inside a LocalScript in
StarterCharacterScripts|StarterPlayer.StarterCharacterScripts.

```
local character = script.Parent



local JUMP_DEBOUNCE = 1



local humanoid = character:WaitForChild("Humanoid")



local isJumping = false



humanoid.StateChanged:Connect(function(_oldState, newState)



if newState == Enum.HumanoidStateType.Jumping then



if not isJumping then



isJumping = true



humanoid:SetStateEnabled(Enum.HumanoidStateType.Jumping, false)



end



elseif newState == Enum.HumanoidStateType.Landed then



if isJumping then



isJumping = false



task.wait(JUMP_DEBOUNCE)



humanoid:SetStateEnabled(Enum.HumanoidStateType.Jumping, true)



end



end



end)
```

Provide feedback

---

TakeDamage

Lowers the [Humanoid.Health](/docs/reference/engine/classes/Humanoid#Health) of the [Humanoid](/docs/reference/engine/classes/Humanoid) by the given
*amount* if it is not protected by a [ForceField](/docs/reference/engine/classes/ForceField).

Humanoid:TakeDamage(amount:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| amount:[number](/docs/luau/numbers)  The damage, or amount to be deduced from the [Humanoid.Health](/docs/reference/engine/classes/Humanoid#Health). |

Returns

()

This method lowers the [Humanoid.Health](/docs/reference/engine/classes/Humanoid#Health) of the [Humanoid](/docs/reference/engine/classes/Humanoid) by
the given *amount* if it is not protected by a [ForceField](/docs/reference/engine/classes/ForceField)

This method accepts negative values for the *amount* parameter. This will
increase the humanoid's [Humanoid.Health](/docs/reference/engine/classes/Humanoid#Health). However this will only
have an effect if no [ForceField](/docs/reference/engine/classes/ForceField) is present.

#### How do ForceFields protect against TakeDamage

A [Humanoid](/docs/reference/engine/classes/Humanoid) is considered protected by a [ForceField](/docs/reference/engine/classes/ForceField) if a
[ForceField](/docs/reference/engine/classes/ForceField) meets one of the following criteria:

* The [ForceField](/docs/reference/engine/classes/ForceField) shares the same [Instance.Parent](/docs/reference/engine/classes/Instance#Parent) as the
  [Humanoid](/docs/reference/engine/classes/Humanoid)
* The [ForceField](/docs/reference/engine/classes/ForceField) is parented to the [Humanoid.RootPart](/docs/reference/engine/classes/Humanoid#RootPart) of
  the [Humanoid](/docs/reference/engine/classes/Humanoid)
* The [ForceField](/docs/reference/engine/classes/ForceField) is parented to an ancestor of the
  [Humanoid](/docs/reference/engine/classes/Humanoid) other than the [Workspace](/docs/reference/engine/classes/Workspace)

To do damage to a [Humanoid](/docs/reference/engine/classes/Humanoid) irrespective of any
[ForceFields](/docs/reference/engine/classes/ForceField) present, set [Humanoid.Health](/docs/reference/engine/classes/Humanoid#Health)
directly.

For more information on how [ForceFields](/docs/reference/engine/classes/ForceField) protect
[Humanoids](/docs/reference/engine/classes/Humanoid) see the [ForceField](/docs/reference/engine/classes/ForceField) page.

Code Samples

Damaging a Humanoid

This code, put in a LocalScript, would make the local player take 99 damage
*only* if a ForceField wasn't present.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local character = player.Character or player.CharacterAdded:Wait()



local humanoid = character:WaitForChild("Humanoid")



humanoid:TakeDamage(99)
```

Provide feedback

---

takeDamage

Deprecated

Show details

---

UnequipTools

Unequips any [Tool](/docs/reference/engine/classes/Tool) currently equipped by the [Humanoid](/docs/reference/engine/classes/Humanoid).

Humanoid:UnequipTools():()

Returns

()

This method unequips any [Tool](/docs/reference/engine/classes/Tool) currently equipped by the
[Humanoid](/docs/reference/engine/classes/Humanoid). The unequipped [Tool](/docs/reference/engine/classes/Tool) will be parented to the
[Backpack](/docs/reference/engine/classes/Backpack) of the [Player](/docs/reference/engine/classes/Player) associated with the
[Humanoid](/docs/reference/engine/classes/Humanoid).

If no [Tool](/docs/reference/engine/classes/Tool) is equipped, this method will do nothing.

Although [Tools](/docs/reference/engine/classes/Tool) can be equipped by NPCs, this method only
works on [Humanoids](/docs/reference/engine/classes/Humanoid) with a corresponding [Player](/docs/reference/engine/classes/Player),
as a [Backpack](/docs/reference/engine/classes/Backpack) object is required to parent the unequipped
[Tool](/docs/reference/engine/classes/Tool) to.

See also [Humanoid:EquipTool()](/docs/reference/engine/classes/Humanoid#EquipTool).

Provide feedback

---

Events

AnimationPlayed

Deprecated

Show details

---

ApplyDescriptionFinished

Humanoid.ApplyDescriptionFinished(description:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| description:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) |

Provide feedback

---

Climbing

Fires when the speed at which a [Humanoid](/docs/reference/engine/classes/Humanoid) is climbing changes.

Humanoid.Climbing(speed:[number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| speed:[number](/docs/luau/numbers)  The speed at which the [Humanoid](/docs/reference/engine/classes/Humanoid) is currently climbing. |

Fires when the speed at which a [Humanoid](/docs/reference/engine/classes/Humanoid) is climbing changes.

[Humanoids](/docs/reference/engine/classes/Humanoid) can climb up ladders made out of
[Parts](/docs/reference/engine/classes/BasePart) or [TrussParts](/docs/reference/engine/classes/TrussPart).

[Humanoids](/docs/reference/engine/classes/Humanoid) climb at 70% of their
[Humanoid.WalkSpeed](/docs/reference/engine/classes/Humanoid#WalkSpeed).

This event will not always fire with a speed of 0 when the
[Humanoid](/docs/reference/engine/classes/Humanoid) stops climbing.

See also:

* For swimming and running see the [Humanoid.Swimming](/docs/reference/engine/classes/Humanoid#Swimming) and
  [Humanoid.Running](/docs/reference/engine/classes/Humanoid#Running) events
* You can also detect when a [Humanoid](/docs/reference/engine/classes/Humanoid) is climbing using the
  [Humanoid.StateChanged](/docs/reference/engine/classes/Humanoid#StateChanged) event
* You can disable climbing using the [Humanoid:SetStateEnabled()](/docs/reference/engine/classes/Humanoid#SetStateEnabled)
  function

Code Samples

Humanoid.Climbing

```
local Players = game:GetService("Players")



local function onCharacterClimbing(character, speed)



print(character.Name, "is climbing at a speed of", speed, "studs / second.")



end



local function onCharacterAdded(character)



character.Humanoid.Climbing:Connect(function(speed)



onCharacterClimbing(character, speed)



end)



end



local function onPlayerAdded(player)



player.CharacterAdded:Connect(onCharacterAdded)



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Provide feedback

---

CustomStatusAdded

Deprecated

Show details

---

CustomStatusRemoved

Deprecated

Show details

---

Died

Fires when the [Humanoid](/docs/reference/engine/classes/Humanoid) dies.

Humanoid.Died():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires when the [Humanoid](/docs/reference/engine/classes/Humanoid) dies, usually when
[Humanoid.Health](/docs/reference/engine/classes/Humanoid#Health) reaches 0. This could be caused either by
disconnecting their head from their [Humanoid.Torso](/docs/reference/engine/classes/Humanoid#Torso), or directly
setting the health property.

This event only fires if the [Humanoid](/docs/reference/engine/classes/Humanoid) is a descendant of the
[Workspace](/docs/reference/engine/classes/Workspace). If the Dead [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType) is disabled it
will not fire.

Code Samples

Humanoid.Died

The code below would print the player's name, followed by "has died!",
whenever a player dies. For example, if the player was named "Shedletsky",
"Shedletsky has died!" would be printed to the output when they died.

```
local Players = game:GetService("Players")



local function onPlayerAdded(player)



local function onCharacterAdded(character)



local humanoid = character:WaitForChild("Humanoid")



local function onDied()



print(player.Name, "has died!")



end



humanoid.Died:Connect(onDied)



end



player.CharacterAdded:Connect(onCharacterAdded)



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Provide feedback

---

FallingDown

Fires when the [Humanoid](/docs/reference/engine/classes/Humanoid) enters or leaves the FallingDown
[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType).

Humanoid.FallingDown(active:[boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| active:[boolean](/docs/luau/booleans)  Describes whether the [Humanoid](/docs/reference/engine/classes/Humanoid) is entering or leaving the FallingDown [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType). |

The FallingDown event fires when the [Humanoid](/docs/reference/engine/classes/Humanoid) enters and leaves
the FallingDown [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType).

The [Humanoid](/docs/reference/engine/classes/Humanoid) will enter the GettingUp state 3 seconds after the
FallingDown state is enabled. When this happens this event will fire
with an *active* value of *false*, and [Humanoid.GettingUp](/docs/reference/engine/classes/Humanoid#GettingUp) will
fire with an *active* value of *true*.

Provide feedback

---

FreeFalling

Fires when the [Humanoid](/docs/reference/engine/classes/Humanoid) enters or leaves the Freefall
[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType).

Humanoid.FreeFalling(active:[boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| active:[boolean](/docs/luau/booleans)  Whether the [Humanoid](/docs/reference/engine/classes/Humanoid) is entering or leaving the Freefall [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType). |

This event fires when the [Humanoid](/docs/reference/engine/classes/Humanoid) enters or leaves the Freefall
[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType).

The *active* parameter represents whether the [Humanoid](/docs/reference/engine/classes/Humanoid) is entering
or leaving the Freefall state.

Although the Freefall state generally ends when the [Humanoid](/docs/reference/engine/classes/Humanoid)
reaches the ground, this event may fire with *active* equal to *false* if
the state is changed while the [Humanoid](/docs/reference/engine/classes/Humanoid) is falling. For this
reason, you should use [Humanoid.StateChanged](/docs/reference/engine/classes/Humanoid#StateChanged) and listen for the
Landed state to work out when a [Humanoid](/docs/reference/engine/classes/Humanoid) has landed.

Provide feedback

---

GettingUp

Fires when the [Humanoid](/docs/reference/engine/classes/Humanoid) enters or leaves the GettingUp
[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType).

Humanoid.GettingUp(active:[boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| active:[boolean](/docs/luau/booleans)  Whether the [Humanoid](/docs/reference/engine/classes/Humanoid) is entering or leaving the GettingUp [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType). |

This event fires when the [Humanoid](/docs/reference/engine/classes/Humanoid) enters or leaves the
[Enum.HumanoidStateType.GettingUp](/docs/reference/engine/enums/HumanoidStateType#GettingUp) state, a transition state that is
activated shortly after the [Humanoid](/docs/reference/engine/classes/Humanoid) enters the
[FallingDown](/docs/reference/engine/enums/HumanoidStateType#FallingDown) (3 seconds) or
[Ragdoll](/docs/reference/engine/enums/HumanoidStateType#Ragdoll) (1 second) states.

When a [Humanoid](/docs/reference/engine/classes/Humanoid) attempts to get back up, this event will first
fire with an active parameter of true before shortly after firing
again with an active parameter of false.

To force a [Humanoid](/docs/reference/engine/classes/Humanoid) to fall over, use the
[Humanoid:ChangeState()](/docs/reference/engine/classes/Humanoid#ChangeState) function with
[Enum.HumanoidStateType.FallingDown](/docs/reference/engine/enums/HumanoidStateType#FallingDown).

Provide feedback

---

HealthChanged

Fires when the [Humanoid.Health](/docs/reference/engine/classes/Humanoid#Health) changes (or when the
[Humanoid.MaxHealth](/docs/reference/engine/classes/Humanoid#MaxHealth) is set).

Humanoid.HealthChanged(health:[number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| health:[number](/docs/luau/numbers)  The new value of [Humanoid.Health](/docs/reference/engine/classes/Humanoid#Health). |

This event fires when the [Humanoid.Health](/docs/reference/engine/classes/Humanoid#Health) changes. However, it
will not fire if the health is increasing from a value equal to or greater
than the [Humanoid.MaxHealth](/docs/reference/engine/classes/Humanoid#MaxHealth).

When [Humanoid.Health](/docs/reference/engine/classes/Humanoid#Health) reaches zero, the [Humanoid](/docs/reference/engine/classes/Humanoid) will die
and the [Humanoid.Died](/docs/reference/engine/classes/Humanoid#Died) event will fire. This event will fire with a
value of zero.

Code Samples

Humanoid.HealthChanged

The following example determines the change in health, printing it to the
output. It will only work in a LocalScript.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local function onCharacterAdded(character)



local humanoid = character:WaitForChild("Humanoid")



local currentHealth = humanoid.Health



local function onHealthChanged(health)



local change = math.abs(currentHealth - health)



print("The humanoid's health", (currentHealth > health and "decreased by" or "increased by"), change)



currentHealth = health



end



humanoid.HealthChanged:Connect(onHealthChanged)



end



player.CharacterAdded:Connect(onCharacterAdded)
```

Health Bar

This code sample allows you to create a simple color-changing health bar using
two nested Frames. Paste this into a LocalScript on the inner frame.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



-- Paste script into a LocalScript that is



-- parented to a Frame within a Frame



local frame = script.Parent



local container = frame.Parent



container.BackgroundColor3 = Color3.new(0, 0, 0) -- black



-- This function is called when the humanoid's health changes



local function onHealthChanged()



local human = player.Character.Humanoid



local percent = human.Health / human.MaxHealth



-- Change the size of the inner bar



frame.Size = UDim2.new(percent, 0, 1, 0)



-- Change the color of the health bar



if percent < 0.1 then



frame.BackgroundColor3 = Color3.new(1, 0, 0) -- black



elseif percent < 0.4 then



frame.BackgroundColor3 = Color3.new(1, 1, 0) -- yellow



else



frame.BackgroundColor3 = Color3.new(0, 1, 0) -- green



end



end



-- This function runs is called the player spawns in



local function onCharacterAdded(character)



local human = character:WaitForChild("Humanoid")



-- Pattern: update once now, then any time the health changes



human.HealthChanged:Connect(onHealthChanged)



onHealthChanged()



end



-- Connect our spawn listener; call it if already spawned



player.CharacterAdded:Connect(onCharacterAdded)



if player.Character then



onCharacterAdded(player.Character)



end
```

Provide feedback

---

Jumping

Fires when the [Humanoid](/docs/reference/engine/classes/Humanoid) enters and leaves the Jumping
[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType).

Humanoid.Jumping(active:[boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| active:[boolean](/docs/luau/booleans)  Whether the [Humanoid](/docs/reference/engine/classes/Humanoid) is entering or leaving the Jumping [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType). |

This event fires when the [Humanoid](/docs/reference/engine/classes/Humanoid) enters and leaves the Jumping
[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType).

When a [Humanoid](/docs/reference/engine/classes/Humanoid) jumps, this event fires with an active parameter
of true before shortly afterwards firing again with an active
parameter of false. This second firing does not correspond with a
[Humanoid](/docs/reference/engine/classes/Humanoid) landing; for that, listen for the Landed
[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType) using [Humanoid.StateChanged](/docs/reference/engine/classes/Humanoid#StateChanged).

You can disable jumping using the [Humanoid:SetStateEnabled()](/docs/reference/engine/classes/Humanoid#SetStateEnabled)
function.

Provide feedback

---

MoveToFinished

Fires when the [Humanoid](/docs/reference/engine/classes/Humanoid) finishes walking to a goal declared by
[Humanoid:MoveTo()](/docs/reference/engine/classes/Humanoid#MoveTo).

Humanoid.MoveToFinished(reached:[boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| reached:[boolean](/docs/luau/booleans)  A boolean indicating whether the [Humanoid](/docs/reference/engine/classes/Humanoid) reached is goal. *True* if the [Humanoid](/docs/reference/engine/classes/Humanoid) is reached its goal, *false* if the walk timed out before the goal could be reached. |

This event fires when the [Humanoid](/docs/reference/engine/classes/Humanoid) finishes walking to a goal
declared by the [Humanoid.WalkToPoint](/docs/reference/engine/classes/Humanoid#WalkToPoint) and
[Humanoid.WalkToPart](/docs/reference/engine/classes/Humanoid#WalkToPart) properties.

The [Humanoid.WalkToPoint](/docs/reference/engine/classes/Humanoid#WalkToPoint) and [Humanoid.WalkToPart](/docs/reference/engine/classes/Humanoid#WalkToPart)
properties can be set individually, or using the [Humanoid:MoveTo()](/docs/reference/engine/classes/Humanoid#MoveTo)
function.

If the [Humanoid](/docs/reference/engine/classes/Humanoid) reaches its goal within 8 seconds, this event will
return with *reached* as true. If the goal is not reached within 8 seconds
the [Humanoid](/docs/reference/engine/classes/Humanoid) will stop walking and *reached* will be false. This
timeout can be reset be calling [Humanoid:MoveTo()](/docs/reference/engine/classes/Humanoid#MoveTo) again within the
timeout period.

Code Samples

Humanoid MoveTo Without Time out

This code sample includes a function that avoids the timeout on
[Humanoid:MoveTo()](/docs/reference/engine/classes/Humanoid#MoveTo) by calling [Humanoid:MoveTo()](/docs/reference/engine/classes/Humanoid#MoveTo) again before
the timeout elapses. It also includes an optional andThen parameter for which
you can pass a function to be called when the humanoid reaches its
destination.

```
local function moveTo(humanoid, targetPoint, andThen)



local targetReached = false



-- listen for the humanoid reaching its target



local connection



connection = humanoid.MoveToFinished:Connect(function(reached)



targetReached = true



connection:Disconnect()



connection = nil



if andThen then



andThen(reached)



end



end)



-- start walking



humanoid:MoveTo(targetPoint)



-- execute on a new thread so as to not yield function



task.spawn(function()



while not targetReached do



-- does the humanoid still exist?



if not (humanoid and humanoid.Parent) then



break



end



-- has the target changed?



if humanoid.WalkToPoint ~= targetPoint then



break



end



-- refresh the timeout



humanoid:MoveTo(targetPoint)



task.wait(6)



end



-- disconnect the connection if it is still connected



if connection then



connection:Disconnect()



connection = nil



end



end)



end



local function andThen(reached)



print((reached and "Destination reached!") or "Failed to reach destination!")



end



moveTo(script.Parent:WaitForChild("Humanoid"), Vector3.new(50, 0, 50), andThen)
```

Provide feedback

---

PlatformStanding

Fires when the [Humanoid](/docs/reference/engine/classes/Humanoid) enters or leaves the PlatformStanding
[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType).

Humanoid.PlatformStanding(active:[boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| active:[boolean](/docs/luau/booleans)  Whether the [Humanoid](/docs/reference/engine/classes/Humanoid) is entering or leaving the PlatformStanding [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType). |

This event fires when the [Humanoid](/docs/reference/engine/classes/Humanoid) enters or leaves the
PlatformStanding [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType).

Whilst the [Humanoid](/docs/reference/engine/classes/Humanoid) is in the PlatformStanding state, the
[Humanoid.PlatformStand](/docs/reference/engine/classes/Humanoid#PlatformStand) property will be *true*.

Whilst [Humanoid.PlatformStand](/docs/reference/engine/classes/Humanoid#PlatformStand) is set to *true*, the
[Humanoid](/docs/reference/engine/classes/Humanoid) will be unable to move. For more information please see
the page for [Humanoid.PlatformStand](/docs/reference/engine/classes/Humanoid#PlatformStand).

The PlatformStand [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType) was associated with the now
disabled [Platform](/docs/reference/engine/classes/Platform) part. Despite this, it can still be used by
developers.

Provide feedback

---

Ragdoll

Fires when the [Humanoid](/docs/reference/engine/classes/Humanoid) enters or leaves the Ragdoll
[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType).

Humanoid.Ragdoll(active:[boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| active:[boolean](/docs/luau/booleans)  Whether the [Humanoid](/docs/reference/engine/classes/Humanoid) is entering or leaving the Ragdoll [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType). |

This event fires when the [Humanoid](/docs/reference/engine/classes/Humanoid) enters or leaves the Ragdoll
[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType).

The active parameter will have the value true or false to indicate
entering or leaving.

Use [Humanoid:SetStateEnabled()](/docs/reference/engine/classes/Humanoid#SetStateEnabled) to disable the GettingUp state to
stay in the Ragdoll state.

See also:

* [Humanoid.FallingDown](/docs/reference/engine/classes/Humanoid#FallingDown) for the [Humanoid](/docs/reference/engine/classes/Humanoid) event connected
  with the FallingDown state, which behaves similarly to Ragdoll

Provide feedback

---

Running

Fires when the speed at which a [Humanoid](/docs/reference/engine/classes/Humanoid) is running changes.

Humanoid.Running(speed:[number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| speed:[number](/docs/luau/numbers)  The speed at which the [Humanoid](/docs/reference/engine/classes/Humanoid) is running. |

This event fires when the speed at which a [Humanoid](/docs/reference/engine/classes/Humanoid) is running
changes.

While running [Humanoids](/docs/reference/engine/classes/Humanoid) cover, on average, their
[Humanoid.WalkSpeed](/docs/reference/engine/classes/Humanoid#WalkSpeed) in studs per second.

When the [Humanoid](/docs/reference/engine/classes/Humanoid) stops running this event will fire with a speed
of 0.

See also:

* For swimming and climbing see the [Humanoid.Swimming](/docs/reference/engine/classes/Humanoid#Swimming) and
  [Humanoid.Climbing](/docs/reference/engine/classes/Humanoid#Climbing) events
* You can also detect when a [Humanoid](/docs/reference/engine/classes/Humanoid) is running using the
  [Humanoid.StateChanged](/docs/reference/engine/classes/Humanoid#StateChanged) event

Code Samples

Humanoid Running

Demonstrates connecting to the [Humanoid.Running](/docs/reference/engine/classes/Humanoid#Running) event. The event is connected to every player's humanoid that joins.

The function connected will print whether or not the humanoid is running based on the speed.

```
local Players = game:GetService("Players")



local localPlayer = Players.LocalPlayer



local character = localPlayer.Character or localPlayer.CharacterAdded:Wait()



local humanoid = character:WaitForChild("Humanoid")



local function onRunning(speed: number)



if speed > 0 then



print(`{localPlayer.Name} is running`)



else



print(`{localPlayer.Name} has stopped`)



end



end



humanoid.Running:Connect(function(speed: number)



onRunning(speed)



end)
```

Provide feedback

---

Seated

Fired when a [Humanoid](/docs/reference/engine/classes/Humanoid) either sits in a [Seat](/docs/reference/engine/classes/Seat) or
[VehicleSeat](/docs/reference/engine/classes/VehicleSeat) or gets up.

Humanoid.Seated(

active:[boolean](/docs/luau/booleans), currentSeatPart:[BasePart](/docs/reference/engine/classes/BasePart)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| active:[boolean](/docs/luau/booleans)  True if the [Humanoid](/docs/reference/engine/classes/Humanoid) is sitting down. |
| currentSeatPart:[BasePart](/docs/reference/engine/classes/BasePart)  The seat the [Humanoid](/docs/reference/engine/classes/Humanoid) is sat in if it is sitting down. |

This event fires when a [Humanoid](/docs/reference/engine/classes/Humanoid) either sits in or gets up from a
[Seat](/docs/reference/engine/classes/Seat) or [VehicleSeat](/docs/reference/engine/classes/VehicleSeat).

When a character comes into contact with a seat, they are attached to the
seat and a sitting animation plays. For more information on this, see the
[Seat](/docs/reference/engine/classes/Seat) page.

* If the character is sitting down, the active parameter will be
  true and currentSeatPart will be the seat they are currently
  sitting in.
* If the character got up from a seat, the active parameter will be
  false and currentSeatPart will be nil.

See also:

* [Humanoid.Sit](/docs/reference/engine/classes/Humanoid#Sit), which indicates if a Humanoid is currently sitting
* [Humanoid.SeatPart](/docs/reference/engine/classes/Humanoid#SeatPart), which indicates the seat a Humanoid is
  currently sitting in, if any.

Code Samples

Finding a Player's Seat

This code sample demonstrates when the local player's
[Character](/docs/reference/engine/classes/Player#Character) sits down or stands up. It should be placed
inside a [LocalScript](/docs/reference/engine/classes/LocalScript) within [StarterCharacterScripts](/docs/reference/engine/classes/StarterCharacterScripts) in order
to run when the player's character spawns in.

```
local character = script.Parent



local humanoid = character:WaitForChild("Humanoid")



local function onSeated(isSeated, seat)



if isSeated then



print("I'm now sitting on: " .. seat.Name .. "!")



else



print("I'm not sitting on anything")



end



end



humanoid.Seated:Connect(onSeated)
```

Provide feedback

---

StateChanged

Fires when the state of the [Humanoid](/docs/reference/engine/classes/Humanoid) is changed.

Humanoid.StateChanged(

old:[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType), new:[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| old:[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType)  The humanoid's previous state type. |
| new:[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType)  The humanoid's current state type. |

This event fires when the state of the [Humanoid](/docs/reference/engine/classes/Humanoid) is changed.

As there is no "idle" humanoid state, you should instead use the
[Humanoid.Running](/docs/reference/engine/classes/Humanoid#Running) event or listen to the
[RootPart](/docs/reference/engine/classes/Humanoid#RootPart) part's
[Velocity](/docs/reference/engine/classes/BasePart#Velocity) to work out when the [Humanoid](/docs/reference/engine/classes/Humanoid)
is standing still.

#### See Also

* [Humanoid:GetState()](/docs/reference/engine/classes/Humanoid#GetState) and [Humanoid:ChangeState()](/docs/reference/engine/classes/Humanoid#ChangeState) to get
  and set the state.
* [Humanoid:SetStateEnabled()](/docs/reference/engine/classes/Humanoid#SetStateEnabled) to enable and disable specific
  states.

Code Samples

Jumping Particles

Emits particles from the local player's [Player.Character](/docs/reference/engine/classes/Player#Character) when they
jump. To try this code sample, place it inside a [LocalScript](/docs/reference/engine/classes/LocalScript) parented to [StarterCharacterScripts](/docs/reference/engine/classes/StarterCharacterScripts).

```
local character = script.Parent



local primaryPart = character.PrimaryPart



-- create particles



local particles = Instance.new("ParticleEmitter")



particles.Size = NumberSequence.new(1)



particles.Transparency = NumberSequence.new(0, 1)



particles.Acceleration = Vector3.new(0, -10, 0)



particles.Lifetime = NumberRange.new(1)



particles.Rate = 20



particles.EmissionDirection = Enum.NormalId.Back



particles.Enabled = false



particles.Parent = primaryPart



local humanoid = character:WaitForChild("Humanoid")



local isJumping = false



-- listen to humanoid state



local function onStateChanged(_oldState, newState)



if newState == Enum.HumanoidStateType.Jumping then



if not isJumping then



isJumping = true



particles.Enabled = true



end



elseif newState == Enum.HumanoidStateType.Landed then



if isJumping then



isJumping = false



particles.Enabled = false



end



end



end



humanoid.StateChanged:Connect(onStateChanged)
```

Jump Cooldown

The following sample will require a one second cooldown after a Humanoid has
landed before it is able to jump again.

To try this sample, place it inside a LocalScript in
StarterCharacterScripts|StarterPlayer.StarterCharacterScripts.

```
local character = script.Parent



local JUMP_DEBOUNCE = 1



local humanoid = character:WaitForChild("Humanoid")



local isJumping = false



humanoid.StateChanged:Connect(function(_oldState, newState)



if newState == Enum.HumanoidStateType.Jumping then



if not isJumping then



isJumping = true



humanoid:SetStateEnabled(Enum.HumanoidStateType.Jumping, false)



end



elseif newState == Enum.HumanoidStateType.Landed then



if isJumping then



isJumping = false



task.wait(JUMP_DEBOUNCE)



humanoid:SetStateEnabled(Enum.HumanoidStateType.Jumping, true)



end



end



end)
```

Provide feedback

---

StateEnabledChanged

Fires when [Humanoid:SetStateEnabled()](/docs/reference/engine/classes/Humanoid#SetStateEnabled) is called on the
[Humanoid](/docs/reference/engine/classes/Humanoid).

Humanoid.StateEnabledChanged(

state:[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType), isEnabled:[boolean](/docs/luau/booleans)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| state:[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType)  The [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType) for which the enabled state has been changed. |
| isEnabled:[boolean](/docs/luau/booleans)  True if the state is now enabled. |

The StateEnableChanged event fires when [Humanoid:SetStateEnabled()](/docs/reference/engine/classes/Humanoid#SetStateEnabled)
is called on the [Humanoid](/docs/reference/engine/classes/Humanoid).

Parameters include the [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType) in question along with a
bool indicating if this state is now enabled.

See also:

* To find if a state is currently enabled, use
  [Humanoid:GetStateEnabled()](/docs/reference/engine/classes/Humanoid#GetStateEnabled)
* To listen to [Humanoid](/docs/reference/engine/classes/Humanoid) state changes use
  [Humanoid.StateChanged](/docs/reference/engine/classes/Humanoid#StateChanged)

Code Samples

Humanoid State Change Detector

When a humanoid state changes for the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer), the code
below prints whether the state has been enabled or disabled.

This code should work as expected when placed in a LocalScript.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local character = player.Character or player.CharacterAdded:Wait()



local humanoid = character:WaitForChild("Humanoid")



local function onStateEnabledChanged(state, enabled)



if enabled then



print(state.Name .. " has been enabled")



else



print(state.Name .. " has been disabled")



end



end



humanoid.StateEnabledChanged:Connect(onStateEnabledChanged)
```

Provide feedback

---

StatusAdded

Deprecated

Show details

---

StatusRemoved

Deprecated

Show details

---

Strafing

Fires when the [Humanoid](/docs/reference/engine/classes/Humanoid) enters or leaves the StrafingNoPhysics
[Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType).

Humanoid.Strafing(active:[boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| active:[boolean](/docs/luau/booleans)  Whether the [Humanoid](/docs/reference/engine/classes/Humanoid) is entering or leaving the StrafingNoPhysics [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType). |

This event does not fire when the [Humanoid](/docs/reference/engine/classes/Humanoid) is strafing and should
not be used by developers

This event is fired when the [Humanoid](/docs/reference/engine/classes/Humanoid) enters or leaves the
StrafingNoPhysics [Enum.HumanoidStateType](/docs/reference/engine/enums/HumanoidStateType).

When the [Humanoid](/docs/reference/engine/classes/Humanoid) enters the StrafingNoPhysics state this event
will fire with an *active* parameter of *true*. The event will fire again
with *active* equal to *false* when the [Humanoid](/docs/reference/engine/classes/Humanoid) leaves the
StrafingNoPhysics state.

This event is associated with the StrafingNoPhysics [Humanoid](/docs/reference/engine/classes/Humanoid)
state and does not fire when the [Humanoid](/docs/reference/engine/classes/Humanoid) is moving
perpendicular to the direction it is facing. This state is currently
unused, if it is set using [Humanoid:ChangeState()](/docs/reference/engine/classes/Humanoid#ChangeState) the state will
revert to RunningNoPhysics.

Provide feedback

---

Swimming

Fires when the speed at which a [Humanoid](/docs/reference/engine/classes/Humanoid) is swimming in
[Terrain](/docs/reference/engine/classes/Terrain) water changes.

Humanoid.Swimming(speed:[number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| speed:[number](/docs/luau/numbers)  The speed the [Humanoid](/docs/reference/engine/classes/Humanoid) is currently swimming at. |

This event fires when the speed at which a [Humanoid](/docs/reference/engine/classes/Humanoid) is swimming in
[Terrain](/docs/reference/engine/classes/Terrain) water changes.

[Humanoids](/docs/reference/engine/classes/Humanoid) swim at 87.5% of their
[Humanoid.WalkSpeed](/docs/reference/engine/classes/Humanoid#WalkSpeed).

This event will not always fire with a speed of 0 when the
[Humanoid](/docs/reference/engine/classes/Humanoid) stops swimming.

See also:

* For running and climbing see the [Humanoid.Running](/docs/reference/engine/classes/Humanoid#Running) and
  [Humanoid.Climbing](/docs/reference/engine/classes/Humanoid#Climbing) events
* You can also detect when a [Humanoid](/docs/reference/engine/classes/Humanoid) is swimming using the
  [Humanoid.StateChanged](/docs/reference/engine/classes/Humanoid#StateChanged) event
* You can disable swimming using the [Humanoid:SetStateEnabled()](/docs/reference/engine/classes/Humanoid#SetStateEnabled)
  function

Provide feedback

---

Touched

Fires when one of the humanoid's limbs come in contact with another
[BasePart](/docs/reference/engine/classes/BasePart).

Humanoid.Touched(

touchingPart:[BasePart](/docs/reference/engine/classes/BasePart), humanoidPart:[BasePart](/docs/reference/engine/classes/BasePart)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| touchingPart:[BasePart](/docs/reference/engine/classes/BasePart)  The [BasePart](/docs/reference/engine/classes/BasePart) the [Humanoid](/docs/reference/engine/classes/Humanoid) has come in contact with. |
| humanoidPart:[BasePart](/docs/reference/engine/classes/BasePart)  The limb of the [Humanoid](/docs/reference/engine/classes/Humanoid) that has been touched. |

This event fires when one of the humanoid's limbs comes in contact with
another [BasePart](/docs/reference/engine/classes/BasePart). The [BasePart](/docs/reference/engine/classes/BasePart) which the limb is touching,
along with the limb itself, is given.

This event will not fire when limbs belonging to the [Humanoid](/docs/reference/engine/classes/Humanoid) come
into contact with themselves.

#### Alternatives

Although the [Humanoid.Touched](/docs/reference/engine/classes/Humanoid#Touched) event is useful, you should consider
if there are alternatives that better suit your needs.

* In most cases, it's advised to connect a [BasePart.Touched](/docs/reference/engine/classes/BasePart#Touched) event
  for [BaseParts](/docs/reference/engine/classes/BasePart) of interest instead, as the
  [Humanoid.Touched](/docs/reference/engine/classes/Humanoid#Touched) event will constantly fire when the humanoid is
  moving. For example, in a dodgeball game, it would be more practical to
  connect a [Touched](/docs/reference/engine/classes/BasePart#Touched) event for the balls rather
  than use [Humanoid.Touched](/docs/reference/engine/classes/Humanoid#Touched).
* When trying to work out when the [Humanoid](/docs/reference/engine/classes/Humanoid) has landed on the
  ground, the [Humanoid.StateChanged](/docs/reference/engine/classes/Humanoid#StateChanged) event is more suitable.
  Alternatively, you can check [Humanoid.FloorMaterial](/docs/reference/engine/classes/Humanoid#FloorMaterial) to see if
  the humanoid is standing on any non-air material.

#### Notes

* Connecting to this event will cause a [TouchTransmitter](/docs/reference/engine/classes/TouchTransmitter) to be
  created in every limb.
* There is currently no equivalent of [BasePart.TouchEnded](/docs/reference/engine/classes/BasePart#TouchEnded) for
  [Humanoids](/docs/reference/engine/classes/Humanoid).

Code Samples

Midas Touch

When placed inside a [Player.Character](/docs/reference/engine/classes/Player#Character) model this code will give a
player the 'Midas touch'. Everything their character touches will change to
gold.

When the Humanoid dies, this change is undone and the golden
BasePart|BaseParts are returned to their original state.

To test this out, place this code inside a Script and place it in
StarterCharacterScripts|StarterPlayer.StarterCharacterScripts.

```
local character = script.Parent



local humanoid = character:WaitForChild("Humanoid")



local partInfo = {}



local debounce = false



local function onHumanoidTouched(hit, _limb)



if debounce then



return



end



if not hit.CanCollide or hit.Transparency ~= 0 then



return



end



if not partInfo[hit] then



partInfo[hit] = {



BrickColor = hit.BrickColor,



Material = hit.Material,



}



hit.BrickColor = BrickColor.new("Gold")



hit.Material = Enum.Material.Ice



debounce = true



task.wait(0.2)



debounce = false



end



end



local touchedConnection = humanoid.Touched:Connect(onHumanoidTouched)



local function onHumanoidDied()



if touchedConnection then



touchedConnection:Disconnect()



end



-- undo all of the gold



for part, info in pairs(partInfo) do



if part and part.Parent then



part.BrickColor = info.BrickColor



part.Material = info.Material



end



end



end



humanoid.Died:Connect(onHumanoidDied)
```

Provide feedback

---