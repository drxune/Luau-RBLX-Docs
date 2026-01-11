# Player | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Player
Scraped: 2026-01-11T02:36:52.714243Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- Player
- Model
- SpawnLocation
- Team
- BasePart
- Mouse
- HumanoidDescription
- Players
- Instance.Name
- UserId
- Players:GetPlayers()
- Instance:GetChildren()
- Players.PlayerAdded
- Instance.ChildAdded
- Players.PlayerRemoving
- Instance.ChildRemoved
- SetAccountAge()
- Character
- StarterPlayer.AutoJumpEnabled
- Humanoid.AutoJumpEnabled
- StarterPlayer.CameraMaxZoomDistance
- CameraMinZoomDistance
- StarterPlayer.CameraMinZoomDistance
- CameraMaxZoomDistance
- GuiButton.Modal
- StarterPlayer.LoadPlayerAppearance
- CharacterAppearanceId
- LoadCharacter()
- Humanoid
- Workspace
- Players.CharacterAutoLoads
- CharacterAdded
- CharacterRemoving
- Object:GetPropertyChangedSignal()
- LocalScripts
- StarterGui
- StarterPack
- PlayerGui
- Backpack
- Player.Character
- Parent
- LocalScript
- StarterPlayer.LoadCharacterAppearance
- StarterPlayer.DevCameraOcclusionMode
- Script
- StarterPlayer.DevComputerCameraMovementMode
- TouchEnabled
- DevTouchCameraMode
- StarterPlayer.DevComputerMovementMode
- DevTouchMovementMode
- StarterPlayer.EnableMouseLockOption
- Camera
- StarterPlayer.DevTouchCameraMovementMode
- DevComputerCameraMode
- StarterPlayer.DevTouchMovementMode
- DevComputerMovementMode
- Humanoid.DisplayName
- Player.DisplayName
- Players:GetNameFromUserIdAsync()
- StarterPlayerScripts
- StreamingEnabled
- Workspace.StreamingEnabled
- Workspace.StreamingIntegrityMode
- StarterPlayer.HealthDisplayDistance
- Humanoid.DisplayDistanceType
- LocalizationService.RobloxLocaleId
- StarterPlayer.NameDisplayDistance
- TeamColor
- SocialService:GetPlayersByPartyId()
- SocialService:GetPartyAsync()
- Player.PartyId
- PrimaryPart
- SpawnLocation.TeamColor
- SpawnLocation.Neutral
- SpawnLocations
- PVInstance:PivotTo()
- Teams
- Team.PlayerAdded
- Team.PlayerRemoved
- Team.TeamColor
- Player.Team
- DisplayName
- GlobalDataStores
- Player.ReplicationFocus
- Workspace.StreamingMinRadius
- Workspace.StreamingTargetRadius
- Accessory
- Shirt
- Pants
- CharacterMesh
- BodyColors
- Decal
- DataModel.JobId
- DataModel.GameId
- DataModel.PlaceId
- ExperienceInviteOptions.LaunchData
- GetJoinData()
- TeleportService:GetLocalPlayerTeleportData()
- Player:GetJoinData()
- UserInputService
- Players.LocalPlayer
- GroupService:PromptJoinAsync()
- Accessories
- Player:HasAppearanceLoaded()
- Player.UserId
- CharacterAppearance
- CharacterAppearanceLoaded
- Object.Changed
- DataModel
- Player.CharacterAdded
- Player.CharacterAppearanceLoaded
- Humanoids
- Player:Move()
- AccountAge
- TextService:FilterStringAsync()
- TextService
- TextFilterResult
- Hats
- Shirts
- Player.CharacterRemoving
- Humanoid.WalkSpeed
- Character()
- added
- RunService.Stepped
- Accoutrements
- CharacterMeshes
- StarterPlayer
- StarterGui:SetCoreGuiEnabled()
- RemoteEvent
- TeleportService:TeleportToSpawnByName()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Player](/docs/reference/engine/classes/Player)

English

Feedback

Engine Class

![Player](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Player-Dark.webp)Player

An object that represents a presently connected client to the experience.

---

Summary

Properties

|  |
| --- |
| [AccountAge](#AccountAge):[number](/docs/luau/numbers) |
| [AutoJumpEnabled](#AutoJumpEnabled):[boolean](/docs/luau/booleans) |
| [CameraMaxZoomDistance](#CameraMaxZoomDistance):[number](/docs/luau/numbers) |
| [CameraMinZoomDistance](#CameraMinZoomDistance):[number](/docs/luau/numbers) |
| [CameraMode](#CameraMode):[Enum.CameraMode](/docs/reference/engine/enums/CameraMode) |
| [CanLoadCharacterAppearance](#CanLoadCharacterAppearance):[boolean](/docs/luau/booleans) |
| [Character](#Character):[Model](/docs/reference/engine/classes/Model) |
| [CharacterAppearance](#CharacterAppearance):[string](/docs/luau/strings)  Deprecated |
| [CharacterAppearanceId](#CharacterAppearanceId):[number](/docs/luau/numbers) |
| [DataComplexity](#DataComplexity):[number](/docs/luau/numbers)  Deprecated |
| [DataReady](#DataReady):[boolean](/docs/luau/booleans)  Deprecated |
| [DevCameraOcclusionMode](#DevCameraOcclusionMode):[Enum.DevCameraOcclusionMode](/docs/reference/engine/enums/DevCameraOcclusionMode) |
| [DevComputerCameraMode](#DevComputerCameraMode):[Enum.DevComputerCameraMovementMode](/docs/reference/engine/enums/DevComputerCameraMovementMode) |
| [DevComputerMovementMode](#DevComputerMovementMode):[Enum.DevComputerMovementMode](/docs/reference/engine/enums/DevComputerMovementMode) |
| [DevEnableMouseLock](#DevEnableMouseLock):[boolean](/docs/luau/booleans) |
| [DevTouchCameraMode](#DevTouchCameraMode):[Enum.DevTouchCameraMovementMode](/docs/reference/engine/enums/DevTouchCameraMovementMode) |
| [DevTouchMovementMode](#DevTouchMovementMode):[Enum.DevTouchMovementMode](/docs/reference/engine/enums/DevTouchMovementMode) |
| [DisplayName](#DisplayName):[string](/docs/luau/strings) |
| [FollowUserId](#FollowUserId):[number](/docs/luau/numbers) |
| [GameplayPaused](#GameplayPaused):[boolean](/docs/luau/booleans) |
| [HasVerifiedBadge](#HasVerifiedBadge):[boolean](/docs/luau/booleans) |
| [HealthDisplayDistance](#HealthDisplayDistance):[number](/docs/luau/numbers) |
| [LocaleId](#LocaleId):[string](/docs/luau/strings) |
| [MembershipType](#MembershipType):[Enum.MembershipType](/docs/reference/engine/enums/MembershipType) |
| [NameDisplayDistance](#NameDisplayDistance):[number](/docs/luau/numbers) |
| [Neutral](#Neutral):[boolean](/docs/luau/booleans) |
| [PartyId](#PartyId):[string](/docs/luau/strings) |
| [ReplicationFocus](#ReplicationFocus):[Instance](/docs/reference/engine/datatypes/Instance) |
| [RespawnLocation](#RespawnLocation):[SpawnLocation](/docs/reference/engine/classes/SpawnLocation) |
| [StepIdOffset](#StepIdOffset):[number](/docs/luau/numbers) |
| [Team](#Team):[Team](/docs/reference/engine/classes/Team) |
| [TeamColor](#TeamColor):[BrickColor](/docs/reference/engine/datatypes/BrickColor) |
| [ThirdPartyTextChatRestrictionStatus](#ThirdPartyTextChatRestrictionStatus):[Enum.ChatRestrictionStatus](/docs/reference/engine/enums/ChatRestrictionStatus) |
| [UserId](#UserId):[number](/docs/luau/numbers) |
| [userId](#userId):[number](/docs/luau/numbers)  Deprecated |

Methods

|  |
| --- |
| [AddReplicationFocus](#AddReplicationFocus)(part: [BasePart](/docs/reference/engine/classes/BasePart)):() |
| [ClearCharacterAppearance](#ClearCharacterAppearance)():() |
| [DistanceFromCharacter](#DistanceFromCharacter)(point: [Vector3](/docs/reference/engine/datatypes/Vector3)):[number](/docs/luau/numbers) |
| [GetFriendsOnlineAsync](#GetFriendsOnlineAsync)(maxFriends: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays) |
| [GetFriendsOnline](#GetFriendsOnline)(maxFriends: [number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)  Deprecated |
| [GetJoinData](#GetJoinData)():[Dictionary](/docs/luau/tables#dictionaries) |
| [GetMouse](#GetMouse)():[Mouse](/docs/reference/engine/classes/Mouse) |
| [GetNetworkPing](#GetNetworkPing)():[number](/docs/luau/numbers) |
| [GetRankInGroupAsync](#GetRankInGroupAsync)(groupId: [number](/docs/luau/numbers)):[number](/docs/luau/numbers) |
| [GetRankInGroup](#GetRankInGroup)(groupId: [number](/docs/luau/numbers)):[number](/docs/luau/numbers)  Deprecated |
| [GetRoleInGroupAsync](#GetRoleInGroupAsync)(groupId: [number](/docs/luau/numbers)):[string](/docs/luau/strings) |
| [GetRoleInGroup](#GetRoleInGroup)(groupId: [number](/docs/luau/numbers)):[string](/docs/luau/strings)  Deprecated |
| [HasAppearanceLoaded](#HasAppearanceLoaded)():[boolean](/docs/luau/booleans) |
| [IsBestFriendsWith](#IsBestFriendsWith)(userId: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans)  Deprecated |
| [IsFriendsWithAsync](#IsFriendsWithAsync)(userId: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans) |
| [IsFriendsWith](#IsFriendsWith)(userId: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans)  Deprecated |
| [isFriendsWith](#isFriendsWith)(userId: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans)  Deprecated |
| [IsInGroupAsync](#IsInGroupAsync)(groupId: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans) |
| [IsInGroup](#IsInGroup)(groupId: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans)  Deprecated |
| [IsVerified](#IsVerified)():[boolean](/docs/luau/booleans) |
| [Kick](#Kick)(message: [string](/docs/luau/strings)):() |
| [LoadBoolean](#LoadBoolean)(key: [string](/docs/luau/strings)):[boolean](/docs/luau/booleans)  Deprecated |
| [loadBoolean](#loadBoolean)(key: [string](/docs/luau/strings)):[boolean](/docs/luau/booleans)  Deprecated |
| [LoadCharacterAsync](#LoadCharacterAsync)():() |
| [LoadCharacter](#LoadCharacter)():()  Deprecated |
| [LoadCharacterAppearance](#LoadCharacterAppearance)(assetInstance: [Instance](/docs/reference/engine/datatypes/Instance)):()  Deprecated |
| [LoadCharacterWithHumanoidDescriptionAsync](#LoadCharacterWithHumanoidDescriptionAsync)(humanoidDescription: [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)):() |
| [LoadCharacterWithHumanoidDescription](#LoadCharacterWithHumanoidDescription)(humanoidDescription: [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)):()  Deprecated |
| [LoadInstance](#LoadInstance)(key: [string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance)  Deprecated |
| [loadInstance](#loadInstance)(key: [string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance)  Deprecated |
| [LoadNumber](#LoadNumber)(key: [string](/docs/luau/strings)):[number](/docs/luau/numbers)  Deprecated |
| [loadNumber](#loadNumber)(key: [string](/docs/luau/strings)):[number](/docs/luau/numbers)  Deprecated |
| [LoadString](#LoadString)(key: [string](/docs/luau/strings)):[string](/docs/luau/strings)  Deprecated |
| [loadString](#loadString)(key: [string](/docs/luau/strings)):[string](/docs/luau/strings)  Deprecated |
| [Move](#Move)(walkDirection: [Vector3](/docs/reference/engine/datatypes/Vector3),relativeToCamera: [boolean](/docs/luau/booleans)):() |
| [RemoveReplicationFocus](#RemoveReplicationFocus)(part: [BasePart](/docs/reference/engine/classes/BasePart)):() |
| [RequestStreamAroundAsync](#RequestStreamAroundAsync)(position: [Vector3](/docs/reference/engine/datatypes/Vector3),timeOut: [number](/docs/luau/numbers)):() |
| [SaveBoolean](#SaveBoolean)(key: [string](/docs/luau/strings),value: [boolean](/docs/luau/booleans)):()  Deprecated |
| [saveBoolean](#saveBoolean)(key: [string](/docs/luau/strings),value: [boolean](/docs/luau/booleans)):()  Deprecated |
| [SaveInstance](#SaveInstance)(key: [string](/docs/luau/strings),value: [Instance](/docs/reference/engine/datatypes/Instance)):()  Deprecated |
| [saveInstance](#saveInstance)(key: [string](/docs/luau/strings),value: [Instance](/docs/reference/engine/datatypes/Instance)):()  Deprecated |
| [SaveNumber](#SaveNumber)(key: [string](/docs/luau/strings),value: [number](/docs/luau/numbers)):()  Deprecated |
| [saveNumber](#saveNumber)(key: [string](/docs/luau/strings),value: [number](/docs/luau/numbers)):()  Deprecated |
| [SaveString](#SaveString)(key: [string](/docs/luau/strings),value: [string](/docs/luau/strings)):()  Deprecated |
| [saveString](#saveString)(key: [string](/docs/luau/strings),value: [string](/docs/luau/strings)):()  Deprecated |
| [SetAccountAge](#SetAccountAge)(accountAge: [number](/docs/luau/numbers)):() |
| [SetSuperSafeChat](#SetSuperSafeChat)(value: [boolean](/docs/luau/booleans)):() |
| [WaitForDataReady](#WaitForDataReady)():[boolean](/docs/luau/booleans)  Deprecated |
| [waitForDataReady](#waitForDataReady)():[boolean](/docs/luau/booleans)  Deprecated |

Events

|  |
| --- |
| [CharacterAdded](#CharacterAdded)(character: [Model](/docs/reference/engine/classes/Model)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [CharacterAppearanceLoaded](#CharacterAppearanceLoaded)(character: [Model](/docs/reference/engine/classes/Model)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [CharacterRemoving](#CharacterRemoving)(character: [Model](/docs/reference/engine/classes/Model)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Chatted](#Chatted)(message: [string](/docs/luau/strings),recipient: [Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Idled](#Idled)(time: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [OnTeleport](#OnTeleport)(teleportState: [Enum.TeleportState](/docs/reference/engine/enums/TeleportState),placeId: [number](/docs/luau/numbers),spawnName: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A Player object is a client that is currently connected. These objects are
added to the [Players](/docs/reference/engine/classes/Players) service when a new player connects, then removed
when they eventually disconnect from the server.

The [Instance.Name](/docs/reference/engine/classes/Instance#Name) property reflects the player's username. When saving
information about a player, you should use their [UserId](/docs/reference/engine/classes/Player#UserId)
since it is possible that a player can change their username.

There are several similar methods in the [Players](/docs/reference/engine/classes/Players) service for working
with Player objects. Use these over their respective [Instance](/docs/reference/engine/classes/Instance) methods:

* You can get a table of current Player objects using
  [Players:GetPlayers()](/docs/reference/engine/classes/Players#GetPlayers); again, use this instead of
  [Instance:GetChildren()](/docs/reference/engine/classes/Instance#GetChildren).
* To detect the addition of Player objects, it is recommended to use the
  [Players.PlayerAdded](/docs/reference/engine/classes/Players#PlayerAdded) event (instead of [Instance.ChildAdded](/docs/reference/engine/classes/Instance#ChildAdded) on
  the [Players](/docs/reference/engine/classes/Players) service).
* Similarly, you can detect the removal of Player objects using
  [Players.PlayerRemoving](/docs/reference/engine/classes/Players#PlayerRemoving), which fires just before the Player is
  removed (instead of [Instance.ChildRemoved](/docs/reference/engine/classes/Instance#ChildRemoved) which fires after). This
  is important if you are saving information about the player that might be
  removed or cleaned up on removal.

---

API Reference

Properties

AccountAge

Read Only

Not Replicated

Read Parallel

Describes the player's account age in days.

Player.AccountAge:[number](/docs/luau/numbers)

This property describes how long ago a player's account was registered in
days. It is set using the [SetAccountAge()](/docs/reference/engine/classes/Player#SetAccountAge)
method, which cannot be accessed by scripts.

Provide feedback

---

AutoJumpEnabled

Read Parallel

Determines whether the character of a player using a mobile device will
automatically jump upon hitting an obstacle.

Player.AutoJumpEnabled:[boolean](/docs/luau/booleans)

This property determines whether the [Character](/docs/reference/engine/classes/Player#Character) of
a [Player](/docs/reference/engine/classes/Player) using a mobile device will automatically jump when they
hit an obstacle. This can make levels more navigable while on a mobile
device.

When the player joins the experience, the
[StarterPlayer.AutoJumpEnabled](/docs/reference/engine/classes/StarterPlayer#AutoJumpEnabled) value determines the initial state
of this property. Then, this property determines the value of the
[Humanoid.AutoJumpEnabled](/docs/reference/engine/classes/Humanoid#AutoJumpEnabled) property of the
[Character](/docs/reference/engine/classes/Player#Character) on spawn. In other words, it is
possible to set the auto-jump behavior on a per-character, per-player, and
per-experience basis using these three properties.

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

CameraMaxZoomDistance

Read Parallel

The maximum distance the player's camera is allowed to zoom out.

Player.CameraMaxZoomDistance:[number](/docs/luau/numbers)

This property sets the maximum distance the player's camera is allowed to
zoom out, in studs.

The default value of this property is set by
[StarterPlayer.CameraMaxZoomDistance](/docs/reference/engine/classes/StarterPlayer#CameraMaxZoomDistance). If this value is set to a
lower value than
[CameraMinZoomDistance](/docs/reference/engine/classes/Player#CameraMinZoomDistance), it will be
increased to [CameraMinZoomDistance](/docs/reference/engine/classes/Player#CameraMinZoomDistance).

Provide feedback

---

CameraMinZoomDistance

Read Parallel

The minimum distance the player's camera is allowed to zoom in.

Player.CameraMinZoomDistance:[number](/docs/luau/numbers)

This property sets the minimum distance the player's camera is allowed to
zoom in, in studs.

The default value of this property is set by
[StarterPlayer.CameraMinZoomDistance](/docs/reference/engine/classes/StarterPlayer#CameraMinZoomDistance). If this value is set to a
higher value than
[CameraMaxZoomDistance](/docs/reference/engine/classes/Player#CameraMaxZoomDistance), it will be
decreased to [CameraMaxZoomDistance](/docs/reference/engine/classes/Player#CameraMaxZoomDistance).

Provide feedback

---

CameraMode

Read Parallel

Changes the camera's mode to either first or third person.

Player.CameraMode:[Enum.CameraMode](/docs/reference/engine/enums/CameraMode)

This property sets the player's camera mode, defaulting to third person.

#### Third Person

In the default third person mode ([Enum.CameraMode.Classic](/docs/reference/engine/enums/CameraMode#Classic)), the
character can be seen in the camera. While in this mode, the default
behavior is:

* Players can right-click and drag (mouse), tap and drag (mobile), use the
  secondary thumbstick (gamepad), or press the left/right arrows
  (keyboard) to rotate the camera around their character.
* When a player moves their character, it faces in the corresponding
  movement direction.
* Players can zoom in and out freely, even to first person on full zoom
  in.

#### First Person

In first person mode ([Enum.CameraMode.LockFirstPerson](/docs/reference/engine/enums/CameraMode#LockFirstPerson)), the player's
camera is zoomed all the way in. Unless there is a visible GUI present
with the [GuiButton.Modal](/docs/reference/engine/classes/GuiButton#Modal) property set to true, moving the mouse,
tap-dragging on mobile, or using the secondary thumbstick on a gamepad
will rotate the camera around the character.

Code Samples

Playing in First Person

This example demonstrates how to change the character's CameraMode to first
person using the LockFirstPerson value of the [Enum.CameraMode](/docs/reference/engine/enums/CameraMode) enum.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



player.CameraMode = Enum.CameraMode.LockFirstPerson
```

Provide feedback

---

CanLoadCharacterAppearance

Read Parallel

Determines whether the character's appearance will be loaded when the
player spawns. If false, the player will spawn with a default
appearance.

Player.CanLoadCharacterAppearance:[boolean](/docs/luau/booleans)

This property determines whether the character's appearance will be loaded
when the player spawns. The default value of this property is set by
[StarterPlayer.LoadPlayerAppearance](/docs/reference/engine/classes/StarterPlayer#LoadPlayerAppearance).

* If true, the character will load the appearance of the player
  corresponding to the player's
  [CharacterAppearanceId](/docs/reference/engine/classes/Player#CharacterAppearanceId).
* If false, the player will spawn with a default appearance.

Attempting to set the property after the character has spawned will not
change the character; you must call
[LoadCharacter()](/docs/reference/engine/classes/Player#LoadCharacter) to load the new appearance.

Provide feedback

---

Character

Read Parallel

A [Model](/docs/reference/engine/classes/Model) controlled by the player that contains a [Humanoid](/docs/reference/engine/classes/Humanoid),
body parts, scripts, and other objects.

Player.Character:[Model](/docs/reference/engine/classes/Model)

This property contains a reference to a [Model](/docs/reference/engine/classes/Model) containing a
[Humanoid](/docs/reference/engine/classes/Humanoid), body parts, scripts, and other objects required for
simulating the player's avatar in-experience. The model is parented to the
[Workspace](/docs/reference/engine/classes/Workspace) but it may be moved. It is automatically loaded when
[Players.CharacterAutoLoads](/docs/reference/engine/classes/Players#CharacterAutoLoads) is true and it can be manually loaded
otherwise using [LoadCharacter()](/docs/reference/engine/classes/Player#LoadCharacter).

Initially this property is nil and it is set when the player's character
first spawns. Use the [CharacterAdded](/docs/reference/engine/classes/Player#CharacterAdded) event
to detect when a player's character properly loads, and the
[CharacterRemoving](/docs/reference/engine/classes/Player#CharacterRemoving) event to detect when
the character is about to despawn. Avoid using
[Object:GetPropertyChangedSignal()](/docs/reference/engine/classes/Object#GetPropertyChangedSignal) on this property.

Note that [LocalScripts](/docs/reference/engine/classes/LocalScript) that are cloned from
[StarterGui](/docs/reference/engine/classes/StarterGui) or [StarterPack](/docs/reference/engine/classes/StarterPack) into a player's
[PlayerGui](/docs/reference/engine/classes/PlayerGui) or [Backpack](/docs/reference/engine/classes/Backpack) respectively are often run before
the old character model is replaced, so [Player.Character](/docs/reference/engine/classes/Player#Character) may refer
to the old model whose [Parent](/docs/reference/engine/classes/Instance#Parent) property is nil.
Therefore, in a [LocalScript](/docs/reference/engine/classes/LocalScript) under [StarterGui](/docs/reference/engine/classes/StarterGui) or
[StarterPack](/docs/reference/engine/classes/StarterPack), it is advisable to make sure the parent of
Character is not nil before using it, for example:

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local character = player.Character



if not character or character.Parent == nil then



character = player.CharacterAdded:Wait()



end
```

Provide feedback

---

CharacterAppearance

Deprecated

Show details

---

CharacterAppearanceId

Read Parallel

Determines the user ID of the account whose character appearance is used
for a player's [Character](/docs/reference/engine/classes/Player#Character).

Player.CharacterAppearanceId:[number](/docs/luau/numbers)

This property determines the user ID of the account whose character
appearance is used for a player's [Character](/docs/reference/engine/classes/Player#Character). By
default, this property is the [UserId](/docs/reference/engine/classes/Player#UserId), which uses the
player's avatar as they have created it on Roblox.

Changing this property to the user ID of another account will cause the
player to spawn with that account's appearance.

You can also toggle whether or not a player's character appearance is
loaded in experience by changing the
[StarterPlayer.LoadCharacterAppearance](/docs/reference/engine/classes/StarterPlayer#LoadCharacterAppearance) property.

Provide feedback

---

DataComplexity

Deprecated

Show details

---

DataReady

Deprecated

Show details

---

DevCameraOcclusionMode

Read Parallel

Sets how the default camera handles objects between the camera and the
player.

Player.DevCameraOcclusionMode:[Enum.DevCameraOcclusionMode](/docs/reference/engine/enums/DevCameraOcclusionMode)

Defines how the default camera scripts handle objects between the camera
and the camera subject. Set by
[StarterPlayer.DevCameraOcclusionMode](/docs/reference/engine/classes/StarterPlayer#DevCameraOcclusionMode) and can't be changed for
individual players.

The default value is [Zoom](/docs/reference/engine/enums/DevCameraOcclusionMode). See
[Enum.DevCameraOcclusionMode](/docs/reference/engine/enums/DevCameraOcclusionMode) for a list of available modes.

Provide feedback

---

DevComputerCameraMode

Read Parallel

Determines player's camera movement mode when using a device with a mouse
and keyboard.

Player.DevComputerCameraMode:[Enum.DevComputerCameraMovementMode](/docs/reference/engine/enums/DevComputerCameraMovementMode)

This property determines the manner in which a player moves their camera
when using a device with a mouse and keyboard. This property cannot be set
using a [LocalScript](/docs/reference/engine/classes/LocalScript) (it must be set on the server using a
[Script](/docs/reference/engine/classes/Script)).

The default value of this property is determined by
[StarterPlayer.DevComputerCameraMovementMode](/docs/reference/engine/classes/StarterPlayer#DevComputerCameraMovementMode).

This property doesn't affect players using a
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device. See
[DevTouchCameraMode](/docs/reference/engine/classes/Player#DevTouchCameraMode) instead.

Provide feedback

---

DevComputerMovementMode

Read Parallel

Determines player's character movement mode when using a device with a
mouse and keyboard.

Player.DevComputerMovementMode:[Enum.DevComputerMovementMode](/docs/reference/engine/enums/DevComputerMovementMode)

This property determines the manner in which a player moves their
character when using a device with a mouse and keyboard. This property
cannot be set using a [LocalScript](/docs/reference/engine/classes/LocalScript) (it must be set on the server
using a [Script](/docs/reference/engine/classes/Script)).

The default value of this property is determined by
[StarterPlayer.DevComputerMovementMode](/docs/reference/engine/classes/StarterPlayer#DevComputerMovementMode).

This property doesn't affect players using a
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device. See
[DevTouchMovementMode](/docs/reference/engine/classes/Player#DevTouchMovementMode) instead.

Provide feedback

---

DevEnableMouseLock

Read Parallel

Determines if the player can toggle mouse lock.

Player.DevEnableMouseLock:[boolean](/docs/luau/booleans)

This property determines if a player is able to toggle mouse lock by
pressing Shift. A player can disable the mouse lock switch in
the experience's settings during play. By default, this property is set to
the value of [StarterPlayer.EnableMouseLockOption](/docs/reference/engine/classes/StarterPlayer#EnableMouseLockOption). This can be set
server-side during runtime by using a [Script](/docs/reference/engine/classes/Script). It can not be set
client-side.

When mouse lock is enabled, the player's cursor is locked to the center of
the screen. Moving the mouse will orbit the camera around the player's
[Character](/docs/reference/engine/classes/Player#Character), and the character will face the same
direction as the [Camera](/docs/reference/engine/classes/Camera). It also offsets the camera view just over
the right shoulder of the player's character.

Provide feedback

---

DevTouchCameraMode

Read Parallel

Determines player's camera movement mode when using a touch-enabled
device.

Player.DevTouchCameraMode:[Enum.DevTouchCameraMovementMode](/docs/reference/engine/enums/DevTouchCameraMovementMode)

This property determines the manner in which a player moves their camera
when using a [TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device.
This property cannot be set using a [LocalScript](/docs/reference/engine/classes/LocalScript) (it must be set on
the server using a [Script](/docs/reference/engine/classes/Script)).

The default value of this property is determined by
[StarterPlayer.DevTouchCameraMovementMode](/docs/reference/engine/classes/StarterPlayer#DevTouchCameraMovementMode).

This property doesn't affect players who aren't using a
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device. See
[DevComputerCameraMode](/docs/reference/engine/classes/Player#DevComputerCameraMode) instead.

Provide feedback

---

DevTouchMovementMode

Read Parallel

Determines player's character movement mode when using a touch-enabled
device.

Player.DevTouchMovementMode:[Enum.DevTouchMovementMode](/docs/reference/engine/enums/DevTouchMovementMode)

This property determines the manner in which a player moves their
character when using a [TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled)
device. This property cannot be set using a [LocalScript](/docs/reference/engine/classes/LocalScript) (it must
be set on the server using a [Script](/docs/reference/engine/classes/Script)).

The default value of this property is determined by
[StarterPlayer.DevTouchMovementMode](/docs/reference/engine/classes/StarterPlayer#DevTouchMovementMode).

This property doesn't affect players who aren't using a
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) device. See
[DevComputerMovementMode](/docs/reference/engine/classes/Player#DevComputerMovementMode) instead.

Provide feedback

---

DisplayName

Read Parallel

The display name of the authenticated user associated with the
[Player](/docs/reference/engine/classes/Player).

Player.DisplayName:[string](/docs/luau/strings)

This property contains the display name of the authenticated user
associated with the [Player](/docs/reference/engine/classes/Player) object. Unlike
[UserId](/docs/reference/engine/classes/Player#UserId), display names are non-unique names a player
displays to others.

#### Usage Notes

* Since display names are non-unique, it's possible for two players in a
  single instance to have identical names. If you need a globally unique
  identifier for a player, use [UserId](/docs/reference/engine/classes/Player#UserId) instead.
* Characters generated with [LoadCharacter()](/docs/reference/engine/classes/Player#LoadCharacter)
  or by the Roblox engine will have their [Humanoid.DisplayName](/docs/reference/engine/classes/Humanoid#DisplayName)
  property assigned to the [Player.DisplayName](/docs/reference/engine/classes/Player#DisplayName) property.
* Display names may have unicode characters in the string. See
  [UTF-8](/docs/reference/engine/libraries/utf8) for more information on how to work with strings
  with unicode characters.

Provide feedback

---

FollowUserId

Read Only

Not Replicated

Read Parallel

Describes the user ID of the player who was followed into an experience by
a player.

Player.FollowUserId:[number](/docs/luau/numbers)

This property contains the [UserId](/docs/reference/engine/classes/Player#UserId) of the user that a
player followed into the experience, or 0 if the player did not follow
anyone in. This property is useful for alerting players who have been
followed by another player into the experience.

You can get the name of the player followed using this user ID and the
[Players:GetNameFromUserIdAsync()](/docs/reference/engine/classes/Players#GetNameFromUserIdAsync) method.

Code Samples

Followed Alert

This code sample alerts players if a new player follows the local player into
the game. Place this in a [LocalScript](/docs/reference/engine/classes/LocalScript) in [StarterPlayerScripts](/docs/reference/engine/classes/StarterPlayerScripts).

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local screenGui = Instance.new("ScreenGui")



screenGui.Parent = player:WaitForChild("PlayerGui")



local function onPlayerAdded(newPlayer)



if newPlayer.FollowUserId == player.UserId then



local textLabel = Instance.new("TextLabel")



textLabel.Parent = screenGui



textLabel.Text = "You were followed to this game by " .. newPlayer.Name .. "!"



task.delay(3, function()



if textLabel then



textLabel:Destroy()



end



end)



end



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Provide feedback

---

GameplayPaused

Hidden

Not Accessible Security

Read Parallel

Whether player client-side gameplay is currently paused.

Player.GameplayPaused:[boolean](/docs/luau/booleans)

This property indicates if the player is currently in a pause state in a
place with [StreamingEnabled](/docs/reference/engine/classes/Workspace#StreamingEnabled) activated.
It is set on the client but replicated to the server.

#### See Also

* [Workspace.StreamingEnabled](/docs/reference/engine/classes/Workspace#StreamingEnabled) which controls whether content
  streaming is enabled
* [Workspace.StreamingIntegrityMode](/docs/reference/engine/classes/Workspace#StreamingIntegrityMode) and
  [Enum.StreamingIntegrityMode](/docs/reference/engine/enums/StreamingIntegrityMode) for more details on when gameplay is
  paused.

Provide feedback

---

HasVerifiedBadge

Read Parallel

Indicates if a player has a Verified badge.

Player.HasVerifiedBadge:[boolean](/docs/luau/booleans)

This property indicates if the player has a Verified badge.

Provide feedback

---

HealthDisplayDistance

Read Parallel

Sets the distance at which this player will see other players' health
bars.

Player.HealthDisplayDistance:[number](/docs/luau/numbers)

This property sets the distance in studs at which this player will see
other [Humanoid](/docs/reference/engine/classes/Humanoid) health bars. If set to 0, the health bars will
not be displayed. This property is set to
[StarterPlayer.HealthDisplayDistance](/docs/reference/engine/classes/StarterPlayer#HealthDisplayDistance) by default.

If a humanoid's health bar is visible, you can set the display type using
[Humanoid.DisplayDistanceType](/docs/reference/engine/classes/Humanoid#DisplayDistanceType).

Provide feedback

---

LocaleId

Hidden

Read Only

Not Replicated

Read Parallel

This property shows the locale ID that the local player has set for their
Roblox account.

Player.LocaleId:[string](/docs/luau/strings)

This property shows the locale ID that the local player has set for their
Roblox account. It holds a string with the two letter code, for example
en-us.

See also [LocalizationService.RobloxLocaleId](/docs/reference/engine/classes/LocalizationService#RobloxLocaleId), the locale ID used
for localizing internal content. This will be a different value when
Roblox does not yet internally support the local player's set locale.

Provide feedback

---

MembershipType

Read Only

Not Replicated

Read Parallel

Describes the account's membership type.

Player.MembershipType:[Enum.MembershipType](/docs/reference/engine/enums/MembershipType)

This property can only be read from to determine membership (it cannot be
set to another membership type). It holds a [Enum.MembershipType](/docs/reference/engine/enums/MembershipType) enum of
the account's membership type.

Code Samples

Check Player Membership Status

The following example checks whether a player has [Premium](https://www.roblox.com/premium/membership) membership.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



if player.MembershipType == Enum.MembershipType.Premium then



-- Take some action specifically for Premium members



end
```

Provide feedback

---

NameDisplayDistance

Read Parallel

Sets the distance at which this player will see other players' names.

Player.NameDisplayDistance:[number](/docs/luau/numbers)

This property sets the distance in studs at which this player will see
other [Humanoid](/docs/reference/engine/classes/Humanoid) names. If the property is set to 0, names are
hidden. This property is set to [StarterPlayer.NameDisplayDistance](/docs/reference/engine/classes/StarterPlayer#NameDisplayDistance)
by default.

If a humanoid's name is visible, you can set the display type using
[Humanoid.DisplayDistanceType](/docs/reference/engine/classes/Humanoid#DisplayDistanceType).

Provide feedback

---

Neutral

Read Parallel

Determines whether the player is on a specific team.

Player.Neutral:[boolean](/docs/luau/booleans)

This property determines whether the player is on a specific team.

* When true, the player is not on a specific team. This also means that
  the [Team](/docs/reference/engine/classes/Player#Team) property will be nil and the
  [TeamColor](/docs/reference/engine/classes/Player#TeamColor) will be white.
* When false, the player is on a specific team. The
  [Team](/docs/reference/engine/classes/Player#Team) property will correspond to the [Team](/docs/reference/engine/classes/Team)
  that the player is on, as will the [TeamColor](/docs/reference/engine/classes/Player#TeamColor).

Provide feedback

---

PartyId

Hidden

Not Replicated

Roblox Security

Read Parallel

A unique identifier of the party a [Player](/docs/reference/engine/classes/Player) belongs to.

Player.PartyId:[string](/docs/luau/strings)

A read-only string identifying the party the player currently belongs to
within the experience. If the player is not in a party, this value is an
empty string.

This property is essential for integrating with the Roblox Party feature.
Use it in combination with [SocialService:GetPlayersByPartyId()](/docs/reference/engine/classes/SocialService#GetPlayersByPartyId) and
[SocialService:GetPartyAsync()](/docs/reference/engine/classes/SocialService#GetPartyAsync) to access information about a
player's party and its members.

To test this service in your experience, use the
[Party Simulator](/docs/studio/testing-modes#party-simulation) in
Roblox Studio or publish the experience and play it in the Roblox
application.

Code Samples

Player.PartyId

This example checks the [Player.PartyId](/docs/reference/engine/classes/Player#PartyId) of a [Player](/docs/reference/engine/classes/Player) when they join the experience. If the player is in a party, it outputs the [Player.PartyId](/docs/reference/engine/classes/Player#PartyId); otherwise, it outputs that the player is not in a party.

```
local Players = game:GetService("Players")



Players.PlayerAdded:Connect(function(player)



local partyId = player.PartyId



if partyId ~= "" then



print("Player is in a party with ID: " .. partyId)



else



print("Player is not in a party")



end



player:GetPropertyChangedSignal("PartyId"):Connect(function()



if player.PartyId ~= "" then



print("Player joined party with ID: " .. player.PartyId)



else



print("Player left party")



end



end)



end)
```

Provide feedback

---

ReplicationFocus

Read Parallel

Sets the part to focus replication around.

Player.ReplicationFocus:[Instance](/docs/reference/engine/datatypes/Instance)

This property sets the part to focus replication around a player.
Different Roblox systems that communicate over the network (such as
physics, streaming, etc.) replicate at different rates depending on how
close objects are to the replication focus.

When this property is nil, it reverts to its default behavior which is
to treat the local player's character's
[PrimaryPart](/docs/reference/engine/classes/Model#PrimaryPart) as the replication focus.

This property should only be set on the server with a [Script](/docs/reference/engine/classes/Script), not
a [LocalScript](/docs/reference/engine/classes/LocalScript). Note that this property does not change or update
network ownership of parts.

Provide feedback

---

RespawnLocation

Read Parallel

If set, the player will respawn at the given [SpawnLocation](/docs/reference/engine/classes/SpawnLocation).

Player.RespawnLocation:[SpawnLocation](/docs/reference/engine/classes/SpawnLocation)

If set, the player will respawn at the given [SpawnLocation](/docs/reference/engine/classes/SpawnLocation) which
must meet the following criteria:

* Descendant of [Workspace](/docs/reference/engine/classes/Workspace).
* The [SpawnLocation.TeamColor](/docs/reference/engine/classes/SpawnLocation#TeamColor) property is set to the player's
  [TeamColor](/docs/reference/engine/classes/Player#TeamColor) or the [SpawnLocation.Neutral](/docs/reference/engine/classes/SpawnLocation#Neutral)
  property is set to true.

#### Alternatives

* A [Player](/docs/reference/engine/classes/Player) will spawn from [SpawnLocations](/docs/reference/engine/classes/SpawnLocation)
  belonging to their team. In some cases it may be simpler to change the
  player's [Team](/docs/reference/engine/classes/Player#Team) instead.
* Implement your own custom spawn logic using [PVInstance:PivotTo()](/docs/reference/engine/classes/PVInstance#PivotTo)
  to manually move the [Character](/docs/reference/engine/classes/Player#Character).

Code Samples

Change Spawn on Touch

This code sample will set the player to always respawn from the last
SpawnLocation they touched. New players will respawn from the SpawnLocation
named 'FirstSpawn' until they touch a different SpawnLocation.

This is an alternative to using the AllowTeamChangeOnTouch property to switch
SpawnLocations and does not require Teams.

```
local Players = game:GetService("Players")



local function addSpawn(spawnLocation)



-- listen for the spawn being touched



spawnLocation.Touched:Connect(function(hit)



local character = hit:FindFirstAncestorOfClass("Model")



if character then



local player = Players:GetPlayerFromCharacter(character)



if player and player.RespawnLocation ~= spawnLocation then



local humanoid = character:FindFirstChildOfClass("Humanoid")



-- make sure the character isn't dead



if humanoid and humanoid:GetState() ~= Enum.HumanoidStateType.Dead then



print("spawn set")



player.RespawnLocation = spawnLocation



end



end



end



end)



end



local firstSpawn



-- look through the workspace for spawns



for _, descendant in pairs(workspace:GetDescendants()) do



if descendant:IsA("SpawnLocation") then



if descendant.Name == "FirstSpawn" then



firstSpawn = descendant



end



addSpawn(descendant)



end



end



local function playerAdded(player)



player.RespawnLocation = firstSpawn



end



-- listen for new players



Players.PlayerAdded:Connect(playerAdded)



-- go through existing players



for _, player in pairs(Players:GetPlayers()) do



playerAdded(player)



end
```

Provide feedback

---

StepIdOffset

Roblox Security

Read Parallel

Player.StepIdOffset:[number](/docs/luau/numbers)

Provide feedback

---

Team

Not Replicated

Read Parallel

Determines the [Team](/docs/reference/engine/classes/Team) with which the player is associated.

Player.Team:[Team](/docs/reference/engine/classes/Team)

This property is a reference to a [Team](/docs/reference/engine/classes/Team) object within the
[Teams](/docs/reference/engine/classes/Teams) service. If the player isn't on a team or has an invalid
[TeamColor](/docs/reference/engine/classes/Player#TeamColor), this property is nil. When this
property is set, the player has joined the [Team](/docs/reference/engine/classes/Team) and the
[Team.PlayerAdded](/docs/reference/engine/classes/Team#PlayerAdded) event fires on the associated team. Similarly,
[Team.PlayerRemoved](/docs/reference/engine/classes/Team#PlayerRemoved) fires when the property is unset from a certain
[Team](/docs/reference/engine/classes/Team).

Provide feedback

---

TeamColor

Read Parallel

Determines the [Team](/docs/reference/engine/classes/Team) with which the player is associated with
according to that team's [Team.TeamColor](/docs/reference/engine/classes/Team#TeamColor).

Player.TeamColor:[BrickColor](/docs/reference/engine/datatypes/BrickColor)

This property determines which [Team](/docs/reference/engine/classes/Team) a player is associated with
according to that team's [Team.TeamColor](/docs/reference/engine/classes/Team#TeamColor). If no [Team](/docs/reference/engine/classes/Team) object
has the associated [BrickColor](/docs/reference/engine/datatypes/BrickColor), the player will not be
associated with a team.

It's often a better idea to set [Player.Team](/docs/reference/engine/classes/Player#Team) to the respective
[Team](/docs/reference/engine/classes/Team) instead of using this property. Setting this property often
leads to repetition of the same [BrickColor](/docs/reference/engine/datatypes/BrickColor) value for a certain
team across many scripts.

Provide feedback

---

ThirdPartyTextChatRestrictionStatus

Read Only

Not Replicated

Roblox Script Security

Read Parallel

Player.ThirdPartyTextChatRestrictionStatus:[Enum.ChatRestrictionStatus](/docs/reference/engine/enums/ChatRestrictionStatus)

Provide feedback

---

UserId

Read Parallel

A unique identifying integer assigned to all user accounts.

Player.UserId:[number](/docs/luau/numbers)

This property contains a read-only integer that uniquely and
consistently identifies the user's account on Roblox. Unlike the
player's [DisplayName](/docs/reference/engine/classes/Player#DisplayName) which may change, this
value will never change for the same account.

This property is essential when saving/loading player data using
[GlobalDataStores](/docs/reference/engine/classes/GlobalDataStore).

Code Samples

Player.UserId

The below example would print the UserId of every user who entered a game.

```
local Players = game:GetService("Players")



local function onPlayerAdded(player)



print(player.UserId)



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Data Store to Leaderboard

This code sample retrieves a player's saved gold from a data store and puts
the returned value onto the leaderboard. Note that this sample does not save
players' gold — it only loads it.

```
local Players = game:GetService("Players")



local DataStoreService = game:GetService("DataStoreService")



local goldDataStore = DataStoreService:GetDataStore("Gold")



local STARTING_GOLD = 100



local function onPlayerAdded(player)



local playerKey = "Player_" .. player.UserId



local leaderstats = Instance.new("IntValue")



leaderstats.Name = "leaderstats"



local gold = Instance.new("IntValue")



gold.Name = "Gold"



gold.Parent = leaderstats



local success, result = pcall(function()



return goldDataStore:GetAsync(playerKey) or STARTING_GOLD



end)



if success then



gold.Value = result



else



-- Failed to retrieve data



warn(result)



end



leaderstats.Parent = player



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Provide feedback

---

userId

Deprecated

Show details

---

Methods

AddReplicationFocus

Adds an additional replication focus for the player.

Player:AddReplicationFocus(part:[BasePart](/docs/reference/engine/classes/BasePart)):()

Parameters

|  |
| --- |
| part:[BasePart](/docs/reference/engine/classes/BasePart)  The [BasePart](/docs/reference/engine/classes/BasePart) to use as a new replication focus. |

Returns

()

This method adds an additional replication focus for the player in order
to trigger streaming around the location of the specified part. In this
manner, streaming can occur around multiple locations, not just the
location of [Player.ReplicationFocus](/docs/reference/engine/classes/Player#ReplicationFocus). This has no effect in
experiences that are not streaming enabled.

Additional foci will use the same values of
[Workspace.StreamingMinRadius](/docs/reference/engine/classes/Workspace#StreamingMinRadius) and
[Workspace.StreamingTargetRadius](/docs/reference/engine/classes/Workspace#StreamingTargetRadius) as are used by the primary focus.

This method should only be called on the server. It has no effect when
called from a [LocalScript](/docs/reference/engine/classes/LocalScript).

Provide feedback

---

ClearCharacterAppearance

Removes all accessories and other character appearance objects from a
player's [Character](/docs/reference/engine/classes/Player#Character).

Player:ClearCharacterAppearance():()

Returns

()

This method removes all [Accessory](/docs/reference/engine/classes/Accessory), [Shirt](/docs/reference/engine/classes/Shirt), [Pants](/docs/reference/engine/classes/Pants),
[CharacterMesh](/docs/reference/engine/classes/CharacterMesh), and [BodyColors](/docs/reference/engine/classes/BodyColors) from the given player's
[Character](/docs/reference/engine/classes/Player#Character). In addition, it also removes the
T-Shirt [Decal](/docs/reference/engine/classes/Decal) on the player's torso. The character's body part
colors and face will remain unchanged. This method does nothing if the
player does not have a [Character](/docs/reference/engine/classes/Player#Character).

Code Samples

How to Clear a Character's Appearance

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local character = player.Character or player.CharacterAdded:Wait()



local function onChildRemoved(child)



print(child.ClassName, "removed from character")



end



character.ChildRemoved:Connect(onChildRemoved)



player:ClearCharacterAppearance()



--> BodyColors removed from character



--> ShirtGraphic removed from character



--> Shirt removed from character



--> Pants removed from character



--> CharacterMesh removed from character



--> Hat removed from character



--> Shirt removed from character
```

Provide feedback

---

DistanceFromCharacter

Returns the distance between the character's head and the given
[Vector3](/docs/reference/engine/datatypes/Vector3), or 0 if the player has no character.

Player:DistanceFromCharacter(point:[Vector3](/docs/reference/engine/datatypes/Vector3)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| point:[Vector3](/docs/reference/engine/datatypes/Vector3)  The location from which player's distance to is being measured. |

Returns

[number](/docs/luau/numbers)

The distance in studs between the player and the location.

This method returns the distance between the character's head and the
given [Vector3](/docs/reference/engine/datatypes/Vector3) point, or 0 if the player has no
[Character](/docs/reference/engine/classes/Player#Character).

This is useful when determining the distance between a player and another
object or location in experience.

If you would like to determine the distance between two non-player
instances or positions, you can use the following:

```
local distance = (position1 - position2).Magnitude
```

Code Samples

Measuring the Distance Between a Player and a Position

This example demonstrates how to measure the distance between a player's
[Player.Character](/docs/reference/engine/classes/Player#Character) and another location.

This code will print the distance of each player's character from the origin
(0, 0, 0):

```
local Players = game:GetService("Players")



for _, player in pairs(Players:GetPlayers()) do



print(player:DistanceFromCharacter(Vector3.new(0, 0, 0)))



end
```

Provide feedback

---

GetFriendsOnlineAsync

Yields

Returns a dictionary of online connections.

Player:GetFriendsOnlineAsync(maxFriends:[number](/docs/luau/numbers)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| maxFriends:[number](/docs/luau/numbers) Default Value: 200 The maximum number of online connections to return. |

Returns

[Array](/docs/luau/tables#arrays)

A dictionary of online connections (see the table above).

This function returns a dictionary array of online connections, using a 30
second cache. In the returned array, some fields are only present for
certain location types; for example, PlaceId won't be present when
LocationType is 0 (mobile website).

| Name | Type | Description |
| --- | --- | --- |
| VisitorId | number | The [UserId](/docs/reference/engine/classes/Player#UserId) of the connection. |
| UserName | string | The username of the connection. |
| DisplayName | string | The [DisplayName](/docs/reference/engine/classes/Player#DisplayName) of the connection. |
| LastOnline | string | When the connection was last online. |
| IsOnline | boolean | If the connection is currently online. |
| LastLocation | string | The name of the connection's current location. |
| PlaceId | number | The place ID of the connection's last location. |
| GameId | string | The [DataModel.JobId](/docs/reference/engine/classes/DataModel#JobId) of the connection's last location. |
| LocationType | number | The location type of the connection's last location. |

Code Samples

Get a List of Online Connections

This example demonstrates how to get a dictionary of a player's online
connections. It returns the maximum number of connections specified by the argument,
or 200 if an argument is not provided.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local success, result = pcall(player.GetFriendsOnline, player, 10)



if success then



for _, friend in pairs(result) do



print(friend.UserName)



end



else



warn("Failed to get online players: " .. result)



end
```

Provide feedback

---

GetFriendsOnline

Deprecated

Show details

---

GetJoinData

Returns a dictionary containing information describing how the player
joins the experience.

Player:GetJoinData():[Dictionary](/docs/luau/tables#dictionaries)

Returns

[Dictionary](/docs/luau/tables#dictionaries)

A dictionary containing PlaceId and UserId values (see table in
description).

Returns a dictionary containing information describing how the player
joins the experience. The dictionary contains any of the following fields:

| Key | Value Type | Description |
| --- | --- | --- |
| SourceGameId | number | The [DataModel.GameId](/docs/reference/engine/classes/DataModel#GameId) of the experience the Player teleported from. Only present if the player teleports to the current experience and if a server calls the teleport function. |
| SourcePlaceId | number | The [DataModel.PlaceId](/docs/reference/engine/classes/DataModel#PlaceId) of the place the Player teleported from. Only present if the player teleports to the current place and a server calls the teleport function. |
| ReferredByPlayerId | number | The [UserId](/docs/reference/engine/classes/Player#UserId) of the player who invited the current player to the experience. Use this data to identify the referrer and trigger reward logic. |
| Members | array | An array containing the [UserId](/docs/reference/engine/classes/Player#UserId) numbers of the users teleported alongside the player. Only present if the player teleported as part of a group. |
| TeleportData | variant | Reflects the teleportData specified in the original teleport. Useful for sharing information between servers the player teleports to. Only present if teleportData was specified and a server calls the teleport function. |
| LaunchData | string | A plain or JSON encoded string that contains launch data specified in a [share link](/docs/production/promotion/share-links) or [ExperienceInviteOptions.LaunchData](/docs/reference/engine/classes/ExperienceInviteOptions#LaunchData). |
| GameJoinContext | dictionary | A dictionary that includes relevant information based on the context of the join. It contains the following keys:    * JoinSource: [Enum.JoinSource](/docs/reference/engine/enums/JoinSource) * ItemType: optional [Enum.AvatarItemType](/docs/reference/engine/enums/AvatarItemType) * AssetId: optional string * OutfitId: optional string * AssetType: optional [Enum.AssetType](/docs/reference/engine/enums/AssetType) |

If a server initiates the player's teleport, the dictionary that this
method returns includes the player's teleport data. The
[GetJoinData()](/docs/reference/engine/classes/Player#GetJoinData) method can only be used to
fetch teleport data on the server. To fetch the data on the client, use
[TeleportService:GetLocalPlayerTeleportData()](/docs/reference/engine/classes/TeleportService#GetLocalPlayerTeleportData).

Unlike [TeleportService:GetLocalPlayerTeleportData()](/docs/reference/engine/classes/TeleportService#GetLocalPlayerTeleportData),
[GetJoinData()](/docs/reference/engine/classes/Player#GetJoinData) only provides teleport data
that meets the following security criteria:

* It's guaranteed to have been sent by a Roblox server in the past 48
  hours.
* It's guaranteed to have been sent with this [Player](/docs/reference/engine/classes/Player).
* The SourcePlaceId and SourceGameId are guaranteed to be the place
  and universe the data was sent from. This means you can verify the
  teleport data came from an approved place.

As this data is transmitted by the client, it can still potentially be
abused by an exploiter. Sensitive data such as player currency should be
transmitted via a secure solution like
[Memory Stores](/docs/cloud-services/memory-stores).

Code Samples

Tracking Traffic Sources

The following example tracks sources of traffic for analytics. By creating
URLs with unique launch data for each social platform, you can determine the
most popular traffic sources. The sample checks the source against a list of
possible samples and discards any invalid sources because users can modify the
launch data.

```
local DataStoreService = game:GetService("DataStoreService")



local Players = game:GetService("Players")



local analyticsStore = DataStoreService:GetDataStore("Analytics")



local ALLOWED_SOURCES = {



"twitter",



"youtube",



"discord",



}



local function onPlayerAdded(player)



local source = player:GetJoinData().LaunchData



-- check if the provided source is valid



if source and table.find(ALLOWED_SOURCES, source) then



-- update the data store to track the source popularity



local success, result = pcall(analyticsStore.IncrementAsync, analyticsStore, source)



if success then



print(player.Name, "joined from", source, "- total:", result)



else



warn("Failed to record join source: " .. result)



end



end



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Referral URL Generator

The following example generates a URL with the user's ID used as launch data.
It then displays the URL in a read-only text box that makes it easy for the
user to copy and share the link with their connections. When a user joins the game using a referral link, you can use the launch data to reward the referrer.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local DIRECT_JOIN_URL = "https://www.roblox.com/games/start?placeId=%d&launchData=%s"



local textBox = script.Parent



local function generateReferralURL(player)



return DIRECT_JOIN_URL:format(game.PlaceId, player.UserId)



end



local function highlightAll()



if -- avoid recursive property updates



textBox:IsFocused() and not (textBox.SelectionStart == 1 and textBox.CursorPosition == #textBox.Text + 1)



then



textBox.SelectionStart = 1



textBox.CursorPosition = #textBox.Text + 1



end



end



textBox.Focused:Connect(highlightAll)



textBox:GetPropertyChangedSignal("SelectionStart"):Connect(highlightAll)



textBox:GetPropertyChangedSignal("CursorPosition"):Connect(highlightAll)



textBox.TextEditable = false



textBox.ClearTextOnFocus = false



textBox.Text = generateReferralURL(player)
```

Using a Table as Launch Data

The following example is a function that converts a table into a string you
can use as launch data. The provided data is JSON encoded, checked for valid
character length, and escaped with percent signs.

```
local HttpService = game:GetService("HttpService")



local DATA_CHARACTER_LIMIT = 200



local function encodeTableAsLaunchData(data)



-- convert the table to a string



local jsonEncodedData = HttpService:JSONEncode(data)



if #jsonEncodedData <= DATA_CHARACTER_LIMIT then



-- escape potentially invalid characters, such as spaces



local urlEncodedData = HttpService:UrlEncode(jsonEncodedData)



return true, urlEncodedData



else



-- report character limit error



return false, ("Encoded table exceeds %d character limit"):format(DATA_CHARACTER_LIMIT)



end



end



local sampleData = {



joinMessage = "Hello!",



urlCreationDate = os.time(),



magicNumbers = {



534,



1337,



746733573,



},



}



local success, encodedData = encodeTableAsLaunchData(sampleData)



if success then



print(encodedData)



else



warn("failed to encode launch data: " .. encodedData)



end
```

Decoding JSON Launch Data

The following example attempts to decode launch data, using pcall to prevent
an error in case the data is corrupt.

```
local HttpService = game:GetService("HttpService")



local Players = game:GetService("Players")



local function onPlayerAdded(player)



local launchData = player:GetJoinData().LaunchData



if launchData then



-- attempt to decode the data



local success, result = pcall(HttpService.JSONDecode, HttpService, launchData)



if success then



print(player.Name, "joined with data:", result)



else



-- this is probably due to the user messing with the URL



warn("Failed to parse launch data:" .. result)



end



end



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Server TeleportData Example

The following code sample is an example of how teleport data can be retrieved
on the server using [Player:GetJoinData()](/docs/reference/engine/classes/Player#GetJoinData). This code, when ran in a
Script in ServerScriptService, will listen for new Player|Players
joining the game. When they join it will retrieve their teleport data
(verifying it came from a valid place) to find their current level.

```
local Players = game:GetService("Players")



local approvedPlaceIds = { 1 } -- insert approved PlaceIds here



local function isPlaceIdApproved(placeId)



for _, id in pairs(approvedPlaceIds) do



if id == placeId then



return true



end



end



return false



end



local function onPlayerAdded(player)



local joinData = player:GetJoinData()



-- verify this data was sent by an approved place



if isPlaceIdApproved(joinData.SourcePlaceId) then



local teleportData = joinData.TeleportData



if teleportData then



local currentLevel = teleportData.currentLevel



print(player.Name .. " is on level " .. currentLevel)



end



end



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Provide feedback

---

GetMouse

Returns the mouse being used by the client.

Player:GetMouse():[Mouse](/docs/reference/engine/classes/Mouse)

Returns

[Mouse](/docs/reference/engine/classes/Mouse)

This method returns the [Mouse](/docs/reference/engine/classes/Mouse) being used by the client. The
player's mouse instance can be used to track user mouse input including
left and right mouse button clicks and movement and location.

Note that [UserInputService](/docs/reference/engine/classes/UserInputService) provides additional methods,
properties, and events to track user input, especially for devices that do
not use a mouse.

Provide feedback

---

GetNetworkPing

Write Parallel

Returns the round-trip, isolated network latency in seconds.

Player:GetNetworkPing():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

Returns the round-trip, isolated network latency of the player in seconds.
"Ping" is a measurement of the time taken for data to be sent from the
client to the server, then back again. It doesn't involve data
deserialization or processing.

For client-side [LocalScripts](/docs/reference/engine/classes/LocalScript), this function can only
be called on the [Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer). This function is useful in
identifying and debugging issues that occur in high network latency
scenarios. It's also useful for masking latency, such as adjusting the
speed of throwing animations for projectiles.

Provide feedback

---

GetRankInGroupAsync

Yields

Returns the player's rank in the group as an integer.

Player:GetRankInGroupAsync(groupId:[number](/docs/luau/numbers)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| groupId:[number](/docs/luau/numbers)  The groupId of the specified group. |

Returns

[number](/docs/luau/numbers)

The player's rank in the group.

This method returns the player's rank in the group as an integer between
0 and 255, where 0 is a non-member and 255 is the group's owner.

This call may not yield the most up-to-date information. If a player
leaves a group while they are in the experience, GetRankInGroup() will
still think they're in that group until they leave. However, this does not
happen when used with a [LocalScript](/docs/reference/engine/classes/LocalScript) because the method caches
results, so multiple calls of GetRankInGroup() on the same player with
the same group ID will yield the same result as when the method was first
called with the given group ID. The caching behavior is on a per-peer
basis: a server does not share the same cache as a client.

When a player joins a group in-experience due to a call to
[GroupService:PromptJoinAsync()](/docs/reference/engine/classes/GroupService#PromptJoinAsync), any cached value for that player
will be cleared on the client where the prompt was shown.

Code Samples

How to Check a Player's Rank in a Group

The code below will check if a player that has entered the game has a rank
equal to 255, in a group with an ID of 2. If they are, it will print "Player
is the owner of the group, 'LOL'!", otherwise "Player is NOT the owner of the
group, 'LOL'!" will be printed to the output.

```
local Players = game:GetService("Players")



local function onPlayerAdded(player)



if player:GetRankInGroupAsync(2) == 255 then



print("Player is the owner of the group, 'LOL'!")



else



print("Player is NOT the owner of the group, 'LOL'!")



end



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Provide feedback

---

GetRankInGroup

Deprecated

Show details

---

GetRoleInGroupAsync

Yields

Returns the player's role in the group as a string, or Guest if the
player isn't part of the group.

Player:GetRoleInGroupAsync(groupId:[number](/docs/luau/numbers)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| groupId:[number](/docs/luau/numbers)  The group ID of the specified group. |

Returns

[string](/docs/luau/strings)

The player's role in the specified group, or Guest if the player is
not a member.

This method returns the player's role in the group as a string, or Guest
if the player isn't part of the group.

This call may not yield the most up-to-date information. If a player
leaves a group while they are in the experience, GetRoleInGroup() will
still think they're in that group until they leave. However, this does not
happen when used with a [LocalScript](/docs/reference/engine/classes/LocalScript) because the method caches
results, so multiple calls of GetRoleInGroup() on the same player with
the same group ID will yield the same result as when the method was first
called with the given group ID. The caching behavior is on a per-peer
basis: a server does not share the same cache as a client.

When a player joins a group in-experience due to a call to
[GroupService:PromptJoinAsync()](/docs/reference/engine/classes/GroupService#PromptJoinAsync), any cached value for that player
will be cleared on the client where the prompt was shown.

Code Samples

How to Check a Player's Role in a Group

The code below will print the name of the rank that the player is currently a
part of, in a specific group. In this instance we're checking what rank the
player is within a group which has a group ID of 2.

```
local Players = game:GetService("Players")



local function onPlayerAdded(player)



print("Player is ranked as '", player:GetRoleInGroupAsync(2), "' in group, 'LOL'!")



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Provide feedback

---

GetRoleInGroup

Deprecated

Show details

---

HasAppearanceLoaded

Returns whether or not the appearance of the player's character has
loaded.

Player:HasAppearanceLoaded():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

A boolean indicating whether or not the appearance of the player's
character has loaded.

This method returns whether or not the appearance of the player's
[Character](/docs/reference/engine/classes/Player#Character) has loaded. Appearance includes items
such as the player's [Shirt](/docs/reference/engine/classes/Shirt), [Pants](/docs/reference/engine/classes/Pants), and
[Accessories](/docs/reference/engine/classes/Accessory).

This is useful when determining whether a player's appearance has loaded
after they first join the experience, which can be tracked using the
[Players.PlayerAdded](/docs/reference/engine/classes/Players#PlayerAdded) event.

Code Samples

Check if a Player's Appearance Has Loaded

This example prints the result of [Player:HasAppearanceLoaded()](/docs/reference/engine/classes/Player#HasAppearanceLoaded) after a
player joins the game until the player's appearance has loaded.

```
local Players = game:GetService("Players")



local function onPlayerAdded(player)



local loaded = player:HasAppearanceLoaded()



print(loaded)



while not loaded do



loaded = player:HasAppearanceLoaded()



print(loaded)



task.wait()



end



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Provide feedback

---

IsBestFriendsWith

Deprecated

Show details

---

IsFriendsWithAsync

Yields

Checks whether a player is a connection of the user with the given
[Player.UserId](/docs/reference/engine/classes/Player#UserId).

Player:IsFriendsWithAsync(userId:[number](/docs/luau/numbers)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| userId:[number](/docs/luau/numbers)  The [Player.UserId](/docs/reference/engine/classes/Player#UserId) of the specified player. |

Returns

[boolean](/docs/luau/booleans)

A boolean indicating whether a player is a connection of the specified
user.

This method sends a request to Roblox asking whether a player is a
connection of another user, given the [UserId](/docs/reference/engine/classes/Player#UserId) of that
user. This method caches results so multiple calls on the same player with
the same userId may not yield the most up-to-date result.

Provide feedback

---

IsFriendsWith

Deprecated

Show details

---

isFriendsWith

Deprecated

Show details

---

IsInGroupAsync

Yields

Checks whether a player is a member of a group with the given ID.

Player:IsInGroupAsync(groupId:[number](/docs/luau/numbers)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| groupId:[number](/docs/luau/numbers)  The group ID of the specified group. |

Returns

[boolean](/docs/luau/booleans)

A boolean indicating whether the player is in the specified group.

This method sends a request to Roblox asking whether a player is a member
of a group, given the ID of that group.

This call may not yield the most up-to-date information. If a player
leaves a group while they are in the experience, IsInGroup() will still
think they're in that group until they leave. However, this does not
happen when used with a [LocalScript](/docs/reference/engine/classes/LocalScript) because the method caches
results, so multiple calls of IsInGroup() on the same player with the
same group ID will yield the same result as when the method was first
called with the given group ID. The caching behavior is on a per-peer
basis: a server does not share the same cache as a client.

When a player joins a group in-experience due to a call to
[GroupService:PromptJoinAsync()](/docs/reference/engine/classes/GroupService#PromptJoinAsync), any cached value for that player
will be cleared on the client where the prompt was shown.

Provide feedback

---

IsInGroup

Deprecated

Show details

---

IsVerified

Returns whether the player is verified with concrete, real-world signals.

Player:IsVerified():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

A boolean indicating whether the player is verified.

Returns a boolean value indicating that player's verification status. When
true, the player is verified. Verification includes, but isn't limited
to, non-VOIP phone number or government ID verification.

When implementing IsVerified, exercise caution to ensure that the
implementation does not inadvertently block all unverified users.

Note that the method can only be called on the backend server. Calling it
client-side results in an error. Additionally, this method will always
return false in Studio.

Code Samples

Using IsVerified

The following example prints "true" if the player is verified.

```
local Players = game:GetService("Players")



local function onPlayerAdded(player)



print(player:IsVerified())



end



for _, player in pairs(Players:GetPlayers()) do



onPlayerAdded(player)



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Provide feedback

---

Kick

Forcibly disconnect a player from the experience, optionally providing a
message.

Player:Kick(message:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| message:[string](/docs/luau/strings)  The message to show the user upon kicking. |

Returns

()

This method allows an experience to gracefully disconnect a client and
optionally provide a message to the disconnected user. This is useful for
moderating abusive users. You should only allow specific users whom you
trust to trigger this method on other users.

Calling this method on a [Player](/docs/reference/engine/classes/Player) with no arguments disconnects the
user from the server and provides a default notice message. Calling this
method on a [Player](/docs/reference/engine/classes/Player) along with a string as the first argument
replaces the default message with the provided string.

When using this method from a [LocalScript](/docs/reference/engine/classes/LocalScript), only the local user's
client can be kicked.

Provide feedback

---

LoadBoolean

Deprecated

Show details

---

loadBoolean

Deprecated

Show details

---

LoadCharacterAsync

Yields

Creates a new character for the player, removing the old one. Also clears
the player's [Backpack](/docs/reference/engine/classes/Backpack) and [PlayerGui](/docs/reference/engine/classes/PlayerGui).

Player:LoadCharacterAsync():()

Returns

()

This method creates a new character for the player, removing the old one.
It also clears the player's [Backpack](/docs/reference/engine/classes/Backpack) and [PlayerGui](/docs/reference/engine/classes/PlayerGui). This
is useful in cases where you want to reload the character without killing
the player, such as when you want to load a new character appearance after
changing the player's
[CharacterAppearance](/docs/reference/engine/classes/Player#CharacterAppearance).

After calling LoadCharacter() for an individual player, it is not
recommended to call it again for the same player until after that player's
[CharacterAppearanceLoaded](/docs/reference/engine/classes/Player#CharacterAppearanceLoaded) event
has fired.

#### Character Loading Event Order

Calling the LoadCharacter() method on any Player fires events in the
following order:

1. The character appearance initializes.
2. The character rig builds and scales.
3. The character moves to the spawn location.
4. [Player.Character](/docs/reference/engine/classes/Player#Character) sets, automatically removing old character.
5. [Object.Changed](/docs/reference/engine/classes/Object#Changed) fires on the [Player](/docs/reference/engine/classes/Player) with a value of
   Character.
6. The character's [Parent](/docs/reference/engine/classes/Instance#Parent) sets to the
   [DataModel](/docs/reference/engine/classes/DataModel).
7. [Player.CharacterAdded](/docs/reference/engine/classes/Player#CharacterAdded) fires.
8. [Player.CharacterAppearanceLoaded](/docs/reference/engine/classes/Player#CharacterAppearanceLoaded) fires.

Code Samples

Turn Off Auto-Loading and Simulate Character Respawn

This script turns off auto-loading and simulates character respawning.

```
local Players = game:GetService("Players")



local RESPAWN_DELAY = 5



Players.CharacterAutoLoads = false



local function onPlayerAdded(player)



local function onCharacterAdded(character)



local humanoid = character:WaitForChild("Humanoid")



local function onDied()



task.wait(RESPAWN_DELAY)



player:LoadCharacter()



end



humanoid.Died:Connect(onDied)



end



player.CharacterAdded:Connect(onCharacterAdded)



player:LoadCharacter()



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Provide feedback

---

LoadCharacter

Deprecated

Show details

---

LoadCharacterAppearance

Deprecated

Show details

---

LoadCharacterWithHumanoidDescriptionAsync

Yields

Spawns a player character with everything equipped in the passed in
[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).

Player:LoadCharacterWithHumanoidDescriptionAsync(humanoidDescription:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)):()

Parameters

|  |
| --- |
| humanoidDescription:[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription)  A [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) containing traits like body parts/colors, body scaling, accessories, clothing, and animations that will be equipped to the loaded character. |

Returns

()

This method spawns a player character with everything equipped in the
passed in [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).

After calling this method for an individual player, it is not recommended
to call it again for the same player until after that player's
[CharacterAppearanceLoaded](/docs/reference/engine/classes/Player#CharacterAppearanceLoaded) event
has fired.

See also
[HumanoidDescription System](/docs/characters/appearance#humanoiddescription),
an article which explains the humanoid description system in greater
detail and provides several scripting examples.

Code Samples

Spawn Characters With HumanoidDescription

To create a HumanoidDescription and then spawn a character with that
description applied, add a Script (not a LocalScript) to the workspace and
add this code to it.

```
local Players = game:GetService("Players")



Players.CharacterAutoLoads = false



local function onPlayerAdded(player)



local humanoidDescription = Instance.new("HumanoidDescription")



humanoidDescription.HatAccessory = "2551510151,2535600138"



humanoidDescription.BodyTypeScale = 0.1



humanoidDescription.ClimbAnimation = 619521311



humanoidDescription.Face = 86487700



humanoidDescription.GraphicTShirt = 1711661



humanoidDescription.HeadColor = Color3.new(0, 1, 0)



player:LoadCharacterWithHumanoidDescription(humanoidDescription)



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Provide feedback

---

LoadCharacterWithHumanoidDescription

Deprecated

Show details

---

LoadInstance

Deprecated

Show details

---

loadInstance

Deprecated

Show details

---

LoadNumber

Deprecated

Show details

---

loadNumber

Deprecated

Show details

---

LoadString

Deprecated

Show details

---

loadString

Deprecated

Show details

---

Move

Causes the player's character to walk in the given direction until
stopped, or interrupted by the player (by using their controls).

Player:Move(

walkDirection:[Vector3](/docs/reference/engine/datatypes/Vector3), relativeToCamera:[boolean](/docs/luau/booleans)

):()

Parameters

|  |
| --- |
| walkDirection:[Vector3](/docs/reference/engine/datatypes/Vector3)  The Vector3 direction that the player should move. |
| relativeToCamera:[boolean](/docs/luau/booleans) Default Value: false A boolean indicating whether the player should move relative to the player's camera. |

Returns

()

This method causes the player's character to walk in the given direction
until stopped, or interrupted by the player (by using their controls).

This is useful when scripting NPC [Humanoids](/docs/reference/engine/classes/Humanoid) that move
around a map but are not controlled by an actual player's input.

Note that the function's second argument indicates whether the provided
[Vector3](/docs/reference/engine/datatypes/Vector3) should move the player relative to world coordinates
(false) or the player's [Camera](/docs/reference/engine/classes/Camera) (true).

Code Samples

Moving the Player relative to their Camera

Demonstrates moving a player relative to their camera's position using [Player:Move()](/docs/reference/engine/classes/Player#Move).

The script first waits for the player's Character and Humanoid to load, as both are required before calling [Player:Move()](/docs/reference/engine/classes/Player#Move). Otherwise a warning will display in the Output.

```
local Players = game:GetService("Players")



local localPlayer = Players.LocalPlayer



-- Wait for the player's character and humanoid, which must exist before calling :Move()



local character = localPlayer.Character or localPlayer.CharacterAdded:Wait()



character:WaitForChild("Humanoid")



-- The player will move until they are 50 studs away from the camera's position at the time of running



localPlayer:Move(Vector3.new(0, 0, -50), true)
```

Provide feedback

---

RemoveReplicationFocus

Removes a previously added replication focus.

Player:RemoveReplicationFocus(part:[BasePart](/docs/reference/engine/classes/BasePart)):()

Parameters

|  |
| --- |
| part:[BasePart](/docs/reference/engine/classes/BasePart)  The [BasePart](/docs/reference/engine/classes/BasePart) to remove as a replication focus. |

Returns

()

This method removes a replication focus previously added by
`Class.Player:AddReplicationFocus()|AddReplicationFocus(). Has no effect
in experiences that are not streaming enabled.

This method should only be called on the server. It has no effect when
called from a [LocalScript](/docs/reference/engine/classes/LocalScript).

Provide feedback

---

RequestStreamAroundAsync

Yields

Requests that the server stream to the player around the specified
location.

Player:RequestStreamAroundAsync(

position:[Vector3](/docs/reference/engine/datatypes/Vector3), timeOut:[number](/docs/luau/numbers)

):()

Parameters

|  |
| --- |
| position:[Vector3](/docs/reference/engine/datatypes/Vector3)  World location where streaming is requested. |
| timeOut:[number](/docs/luau/numbers) Default Value: 0 Optional timeout for the request, the maximum duration that the engine attempts to stream regions around the position parameter before abandoning the request. If you don't specify a value, the timeout is effectively infinite. However, if the client is low on memory, the engine abandons all streaming requests, even those that are still within the timeout duration. |

Returns

()

For experiences where
[instance streaming](/docs/workspace/streaming) is enabled, requests
that the server stream to the player regions (parts and terrain) around
the specified X, Y, Z location in the 3D world. It is useful
if the experience knows that the player's [CFrame](/docs/reference/engine/datatypes/CFrame) will be set to
the specified location in the near future. Without providing the location
with this call, the player may not have streamed in content for the
destination, resulting in a streaming pause or other undesirable behavior.

The effect of this call will be temporary and there are no guarantees of
what will be streamed in around the specified location. Client memory
limits and network conditions may impact what will be available on the
client.

#### Usage Precaution

Requesting streaming around an area is not a guarantee that the
content will be present when the request completes, as streaming is
affected by the client's network bandwidth, memory limitations, and other
factors.

Provide feedback

---

SaveBoolean

Deprecated

Show details

---

saveBoolean

Deprecated

Show details

---

SaveInstance

Deprecated

Show details

---

saveInstance

Deprecated

Show details

---

SaveNumber

Deprecated

Show details

---

saveNumber

Deprecated

Show details

---

SaveString

Deprecated

Show details

---

saveString

Deprecated

Show details

---

SetAccountAge

Plugin Security

Sets the [AccountAge](/docs/reference/engine/classes/Player#AccountAge) of the player.

Player:SetAccountAge(accountAge:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| accountAge:[number](/docs/luau/numbers)  The age of the account in days. |

Returns

()

This method sets the [AccountAge](/docs/reference/engine/classes/Player#AccountAge) of the player in
days, meaning the age of the account itself relative to when it was first
created.

Provide feedback

---

SetSuperSafeChat

Plugin Security

Sets whether or not the player sees filtered chats, rather than normal
chats.

Player:SetSuperSafeChat(value:[boolean](/docs/luau/booleans)):()

Parameters

|  |
| --- |
| value:[boolean](/docs/luau/booleans)  A boolean indicating whether or not the player sees filtered chat. |

Returns

()

This method sets whether or not the player sees chat filtered by
[TextService:FilterStringAsync()](/docs/reference/engine/classes/TextService#FilterStringAsync) rather than normal chats.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



player:SetSuperSafeChat(true)
```

Regardless of whether a player has filtered chat enabled, all chat should
be filtered by [TextService](/docs/reference/engine/classes/TextService) when broadcast to other players or on
the player's own screen. [TextService:FilterStringAsync()](/docs/reference/engine/classes/TextService#FilterStringAsync) returns a
[TextFilterResult](/docs/reference/engine/classes/TextFilterResult) object that can be filtered differently according
to the message's intended use.

Provide feedback

---

WaitForDataReady

Deprecated

Show details

---

waitForDataReady

Deprecated

Show details

---

Events

CharacterAdded

Fires when a player's character spawns or respawns.

Player.CharacterAdded(character:[Model](/docs/reference/engine/classes/Model)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| character:[Model](/docs/reference/engine/classes/Model)  An instance of the character that spawned/respawned. |

This event fires when a player's character spawns or respawns. It fires
soon after setting [Character](/docs/reference/engine/classes/Player#Character) to a non-nil value
or calling [LoadCharacter()](/docs/reference/engine/classes/Player#LoadCharacter), which is before
the character is parented to the [Workspace](/docs/reference/engine/classes/Workspace).

This can be used alongside the
[CharacterRemoving](/docs/reference/engine/classes/Player#CharacterRemoving) event which fires right
before a player's character is about to be removed, typically after death.
As such, both of these events can potentially fire many times as players
die then respawn in a place.

Note that the [Humanoid](/docs/reference/engine/classes/Humanoid) and its default body parts (head, torso,
and limbs) will exist when this event fires, but clothing items like
[Hats](/docs/reference/engine/classes/Hat), [Shirts](/docs/reference/engine/classes/Shirt), and [Pants](/docs/reference/engine/classes/Pants) may take a few
seconds to be added to the character. Connect [Instance.ChildAdded](/docs/reference/engine/classes/Instance#ChildAdded)
on the added character to detect these, or wait for the
[CharacterAppearanceLoaded](/docs/reference/engine/classes/Player#CharacterAppearanceLoaded) event
to be sure the character has everything equipped.

If you instead need to track when a player joins/leaves the experience,
use the events [Players.PlayerAdded](/docs/reference/engine/classes/Players#PlayerAdded) and
[Players.PlayerRemoving](/docs/reference/engine/classes/Players#PlayerRemoving).

Code Samples

Detecting Player Spawns and Despawns

This code sample demonstrates the usage of [Players.PlayerAdded](/docs/reference/engine/classes/Players#PlayerAdded),
[Player.CharacterAdded](/docs/reference/engine/classes/Player#CharacterAdded) and [Player.CharacterRemoving](/docs/reference/engine/classes/Player#CharacterRemoving) in order to
detect the spawning and despawning of players' characters. You can use this as
a boilerplate script to make changes to players' characters as they spawn,
such as changing [Humanoid.WalkSpeed](/docs/reference/engine/classes/Humanoid#WalkSpeed).

```
local Players = game:GetService("Players")



local function onCharacterAdded(character)



print(character.Name .. " has spawned")



end



local function onCharacterRemoving(character)



print(character.Name .. " is despawning")



end



local function onPlayerAdded(player)



player.CharacterAdded:Connect(onCharacterAdded)



player.CharacterRemoving:Connect(onCharacterRemoving)



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Accessory Remover

This code sample automatically removes Accessory objects like hats from the
Player's character when they respawn. Warning: this includes hair, so this
script may cause acute baldness.

When the [Character()](/docs/reference/engine/classes/Player#Character) is
[added](/docs/reference/engine/classes/Player#CharacterAdded), we wait for [RunService.Stepped](/docs/reference/engine/classes/RunService#Stepped) to
fire once (using the wait function of events). This is so the accessory
removal logic runs one frame after the character spawns. A warning can appear
if you delete accessories too quickly after the player spawns, so waiting one
frame will avoid that.

```
local Players = game:GetService("Players")



local RunService = game:GetService("RunService")



local function destroyAccessory(object)



if object:IsA("Hat") or object:IsA("Accessory") then



object:Destroy()



end



end



local function onCharacterAdded(character)



-- Wait a brief moment before removing accessories to avoid the



-- "Something unexpectedly set ___ parent to NULL" warning



RunService.Stepped:Wait()



-- Check for any existing accessories in the player's character



for _, child in pairs(character:GetChildren()) do



destroyAccessory(child)



end



-- Hats may be added to the character a moment after



-- CharacterAdded fires, so we listen for those using ChildAdded



character.ChildAdded:Connect(destroyAccessory)



end



local function onPlayerAdded(player)



player.CharacterAdded:Connect(onCharacterAdded)



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Provide feedback

---

CharacterAppearanceLoaded

Fires when the full appearance of a [Character](/docs/reference/engine/classes/Player#Character) has
been inserted.

Player.CharacterAppearanceLoaded(character:[Model](/docs/reference/engine/classes/Model)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| character:[Model](/docs/reference/engine/classes/Model)  The [Player.Character](/docs/reference/engine/classes/Player#Character) [Model](/docs/reference/engine/classes/Model). |

This event fires when the full appearance of a
[Character](/docs/reference/engine/classes/Player#Character) has been inserted. It only fires on the
server.

A [Character](/docs/reference/engine/classes/Player#Character) generally has a range of objects
modifying its appearance, including [Accoutrements](/docs/reference/engine/classes/Accoutrement),
[Shirts](/docs/reference/engine/classes/Shirt), [Pants](/docs/reference/engine/classes/Pants) and
[CharacterMeshes](/docs/reference/engine/classes/CharacterMesh). This event will fire when all such
objects have been inserted into the character.

For custom character implementations, such as using a character model
named StarterCharacter inside [StarterPlayer](/docs/reference/engine/classes/StarterPlayer), use
[CharacterAdded](/docs/reference/engine/classes/Player#CharacterAdded) and handle your own
accessories.

One use for this event is to ensure all accessories have loaded before
destroying them. See below for an example of this.

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

CharacterRemoving

Fires right before a player's character is removed.

Player.CharacterRemoving(character:[Model](/docs/reference/engine/classes/Model)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| character:[Model](/docs/reference/engine/classes/Model)  An instance of the character that is being removed. |

This event fires right before a player's
[Character](/docs/reference/engine/classes/Player#Character) is removed, such as when the player is
respawning. This can be used alongside the
[CharacterAdded](/docs/reference/engine/classes/Player#CharacterAdded) event which fires when a
player's character spawns or respawns.

If you instead need to track when a player joins/leaves the experience,
use the events [Players.PlayerAdded](/docs/reference/engine/classes/Players#PlayerAdded) and
[Players.PlayerRemoving](/docs/reference/engine/classes/Players#PlayerRemoving).

Code Samples

Detecting Player Spawns and Despawns

This code sample demonstrates the usage of [Players.PlayerAdded](/docs/reference/engine/classes/Players#PlayerAdded),
[Player.CharacterAdded](/docs/reference/engine/classes/Player#CharacterAdded) and [Player.CharacterRemoving](/docs/reference/engine/classes/Player#CharacterRemoving) in order to
detect the spawning and despawning of players' characters. You can use this as
a boilerplate script to make changes to players' characters as they spawn,
such as changing [Humanoid.WalkSpeed](/docs/reference/engine/classes/Humanoid#WalkSpeed).

```
local Players = game:GetService("Players")



local function onCharacterAdded(character)



print(character.Name .. " has spawned")



end



local function onCharacterRemoving(character)



print(character.Name .. " is despawning")



end



local function onPlayerAdded(player)



player.CharacterAdded:Connect(onCharacterAdded)



player.CharacterRemoving:Connect(onCharacterRemoving)



end



Players.PlayerAdded:Connect(onPlayerAdded)
```

Provide feedback

---

Chatted

Fires when a player chats in experience using Roblox's provided chat bar.

Player.Chatted(

message:[string](/docs/luau/strings), recipient:[Player](/docs/reference/engine/classes/Player)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| message:[string](/docs/luau/strings)  The content of the message the player typed in chat. |
| recipient:[Player](/docs/reference/engine/classes/Player)  Deprecated. For whisper messages, this was the Player who was the intended target of the chat message. |

This event fires when a [Player](/docs/reference/engine/classes/Player) types a message and presses
Enter in Roblox's provided chat bar. This is done using some
Luau bindings by the default chat script. You can prevent players from
chatting by using [StarterGui:SetCoreGuiEnabled()](/docs/reference/engine/classes/StarterGui#SetCoreGuiEnabled) and setting
[Enum.CoreGuiType.Chat](/docs/reference/engine/enums/CoreGuiType#Chat) to false.

Provide feedback

---

Idled

This event fires approximately two minutes after the engine classifies the
player as idle. Time is the number of seconds that have elapsed since that
point.

Player.Idled(time:[number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| time:[number](/docs/luau/numbers)  The time in seconds the player has been idle. |

This event fires approximately two minutes after the engine classifies the
player as idle. Time is the number of seconds that have elapsed since that
point. The event continues to fire every 30 seconds for as long as the
player remains idle.

This event only fires in client scripts, not server scripts; use a
[RemoteEvent](/docs/reference/engine/classes/RemoteEvent) to notify the server of idle players.

Roblox automatically disconnects players that have been idle for at least
20 minutes, so this event is useful for warning players that they will be
disconnected soon, disconnecting players prior to those 20 minutes, or
other away from keyboard (AFK) features.

To track how often automatic disconnects occur, try correlating this event
with occurrences of [Players.PlayerRemoving](/docs/reference/engine/classes/Players#PlayerRemoving).

Provide feedback

---

OnTeleport

Fires when the teleport state of a player changes.

Player.OnTeleport(

teleportState:[Enum.TeleportState](/docs/reference/engine/enums/TeleportState), placeId:[number](/docs/luau/numbers), spawnName:[string](/docs/luau/strings)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| teleportState:[Enum.TeleportState](/docs/reference/engine/enums/TeleportState)  The new [Enum.TeleportState](/docs/reference/engine/enums/TeleportState) of the [Player](/docs/reference/engine/classes/Player). |
| placeId:[number](/docs/luau/numbers)  The ID of the place the [Player](/docs/reference/engine/classes/Player) is being teleported to. |
| spawnName:[string](/docs/luau/strings)  The name of the spawn to teleport to, if [TeleportService:TeleportToSpawnByName()](/docs/reference/engine/classes/TeleportService#TeleportToSpawnByName) has been used. |

This event fires when the [Enum.TeleportState](/docs/reference/engine/enums/TeleportState) of a player changes. This
event is useful for detecting whether a teleportation was successful.

Code Samples

Player.OnTeleport

This example prints which stage of a teleport a player is at, as well as
printing if the teleport was a failure.

```
local Players = game:GetService("Players")



Players.PlayerAdded:Connect(function(player)



local playerOnTeleport = player



player.OnTeleport:Connect(function(teleportState, _placeId, _spawnName)



if teleportState == Enum.TeleportState.Started then



print("Teleport started (" .. playerOnTeleport.Name .. ")")



elseif teleportState == Enum.TeleportState.WaitingForServer then



print("Teleport waiting for server (" .. playerOnTeleport.Name .. ")")



elseif teleportState == Enum.TeleportState.InProgress then



print("Teleport in progress (" .. playerOnTeleport.Name .. ")")



elseif teleportState == Enum.TeleportState.Failed then



print("Teleport failed! (" .. playerOnTeleport.Name .. ")")



end



end)



end)
```

Provide feedback

---