# StarterPlayer | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/StarterPlayer
Scraped: 2026-01-11T02:29:46.391182Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Object
- Instance
- StarterPlayer
- Player
- StarterPlayerScripts
- StarterCharacterScripts
- Humanoid
- Model
- Animations
- Humanoid.AutoJumpEnabled
- Motor6Ds
- AnimationConstraints
- BallSocketConstraints
- Player.CameraMaxZoomDistance
- StarterPlayer.CameraMinZoomDistance
- Player.CameraMinZoomDistance
- StarterPlayer.CameraMaxZoomDistance
- Player.CameraMode
- GuiButton.Modal
- Humanoid.BreakJointsOnDeath
- Player.Character
- StarterPlayer.AvatarJointUpgrade
- Humanoid.JumpHeight
- StarterPlayer.CharacterUseJumpPower
- Humanoid.JumpPower
- Humanoid.MaxSlopeAngle
- Humanoid.UseJumpPower
- CharacterJumpHeight
- StarterPlayer.CharacterJumpPower
- Humanoid.WalkSpeed
- Workspace.PlayerScriptsUseInputActionSystem
- Camera
- Player.DevEnableMouseLock
- UserInputService.MouseBehavior
- Player.HealthDisplayDistance
- Humanoid.DisplayDistanceType
- Player.NameDisplayDistance
- Player.CharacterAppearanceId
- Player:LoadCharacterWithHumanoidDescription()
- StarterPlayer.LoadCharacterAppearance
- HumanoidDescription
- Player:LoadCharacter()
- Workspace.MeshPartHeadsAndAccessories
- Workspace
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [StarterPlayer](/docs/reference/engine/classes/StarterPlayer)

English

Feedback

Engine Class

![StarterPlayer](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/StarterPlayer-Dark.webp)StarterPlayer

A service which allows the defaults of properties in the [Player](/docs/reference/engine/classes/Player) object
to be set.

Not Creatable

Service

---

Summary

Properties

|  |
| --- |
| [AllowCustomAnimations](#AllowCustomAnimations):[boolean](/docs/luau/booleans) |
| [AutoJumpEnabled](#AutoJumpEnabled):[boolean](/docs/luau/booleans) |
| [AvatarJointUpgrade](#AvatarJointUpgrade):[Enum.RolloutState](/docs/reference/engine/enums/RolloutState) |
| [CameraMaxZoomDistance](#CameraMaxZoomDistance):[number](/docs/luau/numbers) |
| [CameraMinZoomDistance](#CameraMinZoomDistance):[number](/docs/luau/numbers) |
| [CameraMode](#CameraMode):[Enum.CameraMode](/docs/reference/engine/enums/CameraMode) |
| [CharacterBreakJointsOnDeath](#CharacterBreakJointsOnDeath):[boolean](/docs/luau/booleans) |
| [CharacterJumpHeight](#CharacterJumpHeight):[number](/docs/luau/numbers) |
| [CharacterJumpPower](#CharacterJumpPower):[number](/docs/luau/numbers) |
| [CharacterMaxSlopeAngle](#CharacterMaxSlopeAngle):[number](/docs/luau/numbers) |
| [CharacterUseJumpPower](#CharacterUseJumpPower):[boolean](/docs/luau/booleans) |
| [CharacterWalkSpeed](#CharacterWalkSpeed):[number](/docs/luau/numbers) |
| [ClassicDeath](#ClassicDeath):[boolean](/docs/luau/booleans) |
| [CreateDefaultPlayerModule](#CreateDefaultPlayerModule):[boolean](/docs/luau/booleans) |
| [DevCameraOcclusionMode](#DevCameraOcclusionMode):[Enum.DevCameraOcclusionMode](/docs/reference/engine/enums/DevCameraOcclusionMode) |
| [DevComputerCameraMovementMode](#DevComputerCameraMovementMode):[Enum.DevComputerCameraMovementMode](/docs/reference/engine/enums/DevComputerCameraMovementMode) |
| [DevComputerMovementMode](#DevComputerMovementMode):[Enum.DevComputerMovementMode](/docs/reference/engine/enums/DevComputerMovementMode) |
| [DevTouchCameraMovementMode](#DevTouchCameraMovementMode):[Enum.DevTouchCameraMovementMode](/docs/reference/engine/enums/DevTouchCameraMovementMode) |
| [DevTouchMovementMode](#DevTouchMovementMode):[Enum.DevTouchMovementMode](/docs/reference/engine/enums/DevTouchMovementMode) |
| [EnableDynamicHeads](#EnableDynamicHeads):[Enum.LoadDynamicHeads](/docs/reference/engine/enums/LoadDynamicHeads) |
| [EnableMouseLockOption](#EnableMouseLockOption):[boolean](/docs/luau/booleans) |
| [HealthDisplayDistance](#HealthDisplayDistance):[number](/docs/luau/numbers) |
| [LoadCharacterAppearance](#LoadCharacterAppearance):[boolean](/docs/luau/booleans) |
| [LoadCharacterLayeredClothing](#LoadCharacterLayeredClothing-) :[Enum.LoadCharacterLayeredClothing](/docs/reference/engine/enums/LoadCharacterLayeredClothing) |
| [LuaCharacterController](#LuaCharacterController):[Enum.CharacterControlMode](/docs/reference/engine/enums/CharacterControlMode) |
| [NameDisplayDistance](#NameDisplayDistance):[number](/docs/luau/numbers) |
| [UserEmotesEnabled](#UserEmotesEnabled):[boolean](/docs/luau/booleans) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A service which allows the defaults of properties in the [Player](/docs/reference/engine/classes/Player) object
to be set. When a player enters the server, each property of the player object
is set to the current value of the corresponding property in
[StarterPlayer](/docs/reference/engine/classes/StarterPlayer).

Additionally, you may add four objects to this service:

* A [StarterPlayerScripts](/docs/reference/engine/classes/StarterPlayerScripts) instance with scripts that run once for each
  player.
* A [StarterCharacterScripts](/docs/reference/engine/classes/StarterCharacterScripts) instance with scripts to add to each
  player's character every time they spawn.
* A [Humanoid](/docs/reference/engine/classes/Humanoid) instance named StarterHumanoid which will be used as
  the default humanoid for each player's character.
* A [Model](/docs/reference/engine/classes/Model) instance named StarterCharacter which will be used as the
  character model for all players.

---

API Reference

Properties

AllowCustomAnimations

Hidden

Roblox Script Security

Read Parallel

Describes the current game's permission levels regarding custom avatar
animations from the website.

StarterPlayer.AllowCustomAnimations:[boolean](/docs/luau/booleans)

This property describes the current game's permission levels regarding
custom avatar [Animations](/docs/reference/engine/classes/Animation) from the website.

As such, this value cannot be changed from within the game. It can only be
changed by changing the game's permission levels within the game's
setting's page on the website.

This property is not intended for use in the game.

Provide feedback

---

AutoJumpEnabled

Read Parallel

Sets whether the character will automatically jump when hitting an
obstacle on a mobile device.

StarterPlayer.AutoJumpEnabled:[boolean](/docs/luau/booleans)

This property sets whether the character will automatically jump when
hitting an obstacle on a mobile device.

This property is copied from the [StarterPlayer](/docs/reference/engine/classes/StarterPlayer) to a [Player](/docs/reference/engine/classes/Player)
when they join the game. Following that. the value of this property is
copied to [Humanoid.AutoJumpEnabled](/docs/reference/engine/classes/Humanoid#AutoJumpEnabled) property of the character's
[Humanoid](/docs/reference/engine/classes/Humanoid) on spawn. In other words, it is possible to set the
auto-jump behavior on a per-character, per-player and per-game basis using
these three properties.

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

AvatarJointUpgrade

Not Replicated

Not Scriptable

Not Browsable

Read Parallel

Controls whether avatars spawn with AnimationConstraint joints for
physical simulation.

StarterPlayer.AvatarJointUpgrade:[Enum.RolloutState](/docs/reference/engine/enums/RolloutState)

This property controls the rollout state of new AnimationConstraint joints
in avatars. When Disabled, avatars spawn with legacy
[Motor6Ds](/docs/reference/engine/classes/Motor6D) connecting their limbs. When Enabled, avatars
spawn with [AnimationConstraints](/docs/reference/engine/classes/AnimationConstraint) and
[BallSocketConstraints](/docs/reference/engine/classes/BallSocketConstraint) connecting their limbs.
This makes it easier to write scripts that enable physical simulation,
like arm strength and ragdoll falling down.

For more info see the
[devforum announcement](https://devforum.roblox.com/t/studio-beta-avatar-joint-upgrade-enabling-physically-simulated-characters/3266099).

Provide feedback

---

CameraMaxZoomDistance

Read Parallel

The maximum distance the player's default camera is allowed to zoom out in
studs.

StarterPlayer.CameraMaxZoomDistance:[number](/docs/luau/numbers)

This property sets the maximum distance in studs the camera can be from
the character with the default cameras.

This property sets the default value of
[Player.CameraMaxZoomDistance](/docs/reference/engine/classes/Player#CameraMaxZoomDistance) for each player who joins the game.
If this value is set to a lower value than
[StarterPlayer.CameraMinZoomDistance](/docs/reference/engine/classes/StarterPlayer#CameraMinZoomDistance) it will be increased to
CameraMinZoomDistance.

Code Samples

Setting Camera Zoom Distance

The example demonstrates how to set a player's camera minimum and maximum
zoom distance.

In this example, we set the [Player.CameraMinZoomDistance](/docs/reference/engine/classes/Player#CameraMinZoomDistance) and
[Player.CameraMaxZoomDistance](/docs/reference/engine/classes/Player#CameraMaxZoomDistance) to set the min and max distance in studs
a player's camera can be from their character.

Note that since the example attempts to set the CameraMinZoomDistance to be
greater than the CameraMaxZoomDistance, the CameraMinZoomDistance value will
be decreased and set to the value of the max zoom distance.

To change the default min and max zoom distance values for a player when they
first enter the game, you can change the
StarterClass.Player.CameraMinZoomDistance and
StarterClass.Player.CameraMaxZoomDistance properties.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



player.CameraMaxZoomDistance = 50



player.CameraMinZoomDistance = 75
```

Provide feedback

---

CameraMinZoomDistance

Read Parallel

The minimum distance in studs the player's default camera is allowed to
zoom in.

StarterPlayer.CameraMinZoomDistance:[number](/docs/luau/numbers)

This property sets the minimum distance in studs the camera can be from
the character with the default cameras.

This property sets the default value of
[Player.CameraMinZoomDistance](/docs/reference/engine/classes/Player#CameraMinZoomDistance) for each player who joins the game.
If this value is set to a higher value than
[StarterPlayer.CameraMaxZoomDistance](/docs/reference/engine/classes/StarterPlayer#CameraMaxZoomDistance) it will be decreased to
CameraMaxZoomDistance.

Code Samples

Setting Camera Zoom Distance

The example demonstrates how to set a player's camera minimum and maximum
zoom distance.

In this example, we set the [Player.CameraMinZoomDistance](/docs/reference/engine/classes/Player#CameraMinZoomDistance) and
[Player.CameraMaxZoomDistance](/docs/reference/engine/classes/Player#CameraMaxZoomDistance) to set the min and max distance in studs
a player's camera can be from their character.

Note that since the example attempts to set the CameraMinZoomDistance to be
greater than the CameraMaxZoomDistance, the CameraMinZoomDistance value will
be decreased and set to the value of the max zoom distance.

To change the default min and max zoom distance values for a player when they
first enter the game, you can change the
StarterClass.Player.CameraMinZoomDistance and
StarterClass.Player.CameraMaxZoomDistance properties.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



player.CameraMaxZoomDistance = 50



player.CameraMinZoomDistance = 75
```

Provide feedback

---

CameraMode

Read Parallel

Changes the default camera's mode to either first or third person.

StarterPlayer.CameraMode:[Enum.CameraMode](/docs/reference/engine/enums/CameraMode)

Sets the default value for [Player.CameraMode](/docs/reference/engine/classes/Player#CameraMode) for each player in
the game. The camera has two modes:

##### First Person

In first person mode, the player's camera is zoomed all the way in. Unless
there is a visible GUI present with the [GuiButton.Modal](/docs/reference/engine/classes/GuiButton#Modal) property
set to true, the mouse will be locked and the user's camera will turn as
the mouse moves.

##### Third Person

In third person mode (default), the character can be seen in the camera.
While in third person mode on Roblox:

* You may right-click and drag to rotate your camera, or use the arrow
  keys at the bottom right-hand corner of the screen.
* When you move your mouse, your camera does not change (unless you move
  the mouse to the end of the screen).
* When you press any of the arrow keys, the user's character will face in
  the corresponding arrow key's direction.
* You can zoom in and out freely.

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

CharacterBreakJointsOnDeath

Read Parallel

Determines the starting value of [Humanoid.BreakJointsOnDeath](/docs/reference/engine/classes/Humanoid#BreakJointsOnDeath) for
[Player.Character](/docs/reference/engine/classes/Player#Character).

StarterPlayer.CharacterBreakJointsOnDeath:[boolean](/docs/luau/booleans)

This property determines the starting value of
[Humanoid.BreakJointsOnDeath](/docs/reference/engine/classes/Humanoid#BreakJointsOnDeath) for a player's
[Player.Character](/docs/reference/engine/classes/Player#Character).

Note, [StarterPlayer.AvatarJointUpgrade](/docs/reference/engine/classes/StarterPlayer#AvatarJointUpgrade) must be enabled for
CharacterBreakJointsOnDeath to take effect.

Provide feedback

---

CharacterJumpHeight

Read Parallel

Determines the starting value of [Humanoid.JumpHeight](/docs/reference/engine/classes/Humanoid#JumpHeight) for
[Player.Character](/docs/reference/engine/classes/Player#Character).

StarterPlayer.CharacterJumpHeight:[number](/docs/luau/numbers)

This property determines the starting value of [Humanoid.JumpHeight](/docs/reference/engine/classes/Humanoid#JumpHeight)
for a player's [Player.Character](/docs/reference/engine/classes/Player#Character). The value of this property
defaults to 7.2 studs.

This property is only visible in the Properties window If
[StarterPlayer.CharacterUseJumpPower](/docs/reference/engine/classes/StarterPlayer#CharacterUseJumpPower) is set to false, as it would
not be relevant otherwise.

Since this property is only relevant for characters being spawned in the
future, changing it will not change any existing player characters.
Changes to this property will only take effect when a player respawns.

Provide feedback

---

CharacterJumpPower

Read Parallel

Determines the starting value of [Humanoid.JumpPower](/docs/reference/engine/classes/Humanoid#JumpPower) for
[Player.Character](/docs/reference/engine/classes/Player#Character).

StarterPlayer.CharacterJumpPower:[number](/docs/luau/numbers)

This property determines the starting value of [Humanoid.JumpPower](/docs/reference/engine/classes/Humanoid#JumpPower)
for a player's [Player.Character](/docs/reference/engine/classes/Player#Character). The value of this property
defaults to 50 and when applied to the player's [Humanoid](/docs/reference/engine/classes/Humanoid) it will
be constrained between 0 and 1000.

This property is only visible in the Properties window If
[StarterPlayer.CharacterUseJumpPower](/docs/reference/engine/classes/StarterPlayer#CharacterUseJumpPower) is set to true, as it would
not be relevant otherwise.

Since this property is only relevant for characters being spawned in the
future, changing it will not change any existing player characters.
Changes to this property will only take effect when a player respawns.

Provide feedback

---

CharacterMaxSlopeAngle

Read Parallel

Determines the starting value of [Humanoid.MaxSlopeAngle](/docs/reference/engine/classes/Humanoid#MaxSlopeAngle) for
[Player.Character](/docs/reference/engine/classes/Player#Character).

StarterPlayer.CharacterMaxSlopeAngle:[number](/docs/luau/numbers)

This property determines the starting value of
[Humanoid.MaxSlopeAngle](/docs/reference/engine/classes/Humanoid#MaxSlopeAngle) for a player's [Player.Character](/docs/reference/engine/classes/Player#Character). It
defaults to 89°, so humanoids can climb pretty much any slope they want by
default. When applied to the player's [Humanoid](/docs/reference/engine/classes/Humanoid) it will be
constrained between 0 and 89.

Since this property is only relevant for characters being spawned in the
future, changing it will not change any existing player characters.
Changes to this property will only take effect when a player respawns.

Provide feedback

---

CharacterUseJumpPower

Read Parallel

Determines the starting state of [Humanoid.UseJumpPower](/docs/reference/engine/classes/Humanoid#UseJumpPower) for
[Player.Character](/docs/reference/engine/classes/Player#Character).

StarterPlayer.CharacterUseJumpPower:[boolean](/docs/luau/booleans)

CharacterUseJumpPower determines the starting value of
[Humanoid.UseJumpPower](/docs/reference/engine/classes/Humanoid#UseJumpPower) for a player's [Player.Character](/docs/reference/engine/classes/Player#Character).
Toggling it will change which property is visible in the properties
window: [CharacterJumpHeight](/docs/reference/engine/classes/StarterPlayer#CharacterJumpHeight)
(false) or [StarterPlayer.CharacterJumpPower](/docs/reference/engine/classes/StarterPlayer#CharacterJumpPower) (true). Defaults to
true.

Since this property is only relevant for characters being spawned in the
future, changing it will not change any existing player characters.
Changes to this property will only take effect when a player respawns.

Provide feedback

---

CharacterWalkSpeed

Read Parallel

Determines the starting value of [Humanoid.WalkSpeed](/docs/reference/engine/classes/Humanoid#WalkSpeed) for
[Player.Character](/docs/reference/engine/classes/Player#Character).

StarterPlayer.CharacterWalkSpeed:[number](/docs/luau/numbers)

This property determines the starting value of [Humanoid.WalkSpeed](/docs/reference/engine/classes/Humanoid#WalkSpeed)
for a player's [Player.Character](/docs/reference/engine/classes/Player#Character). This property defaults to 16.

Since this property is only relevant for characters being spawned in the
future, changing it will not change any existing player characters.
Changes to this property will only take effect when a player respawns.

Provide feedback

---

ClassicDeath

Not Browsable

Read Parallel

StarterPlayer.ClassicDeath:[boolean](/docs/luau/booleans)

Provide feedback

---

CreateDefaultPlayerModule

Not Scriptable

Read Parallel

Controls how the default player module and related scripts are handled.

StarterPlayer.CreateDefaultPlayerModule:[boolean](/docs/luau/booleans)

This property is only visible when
[Workspace.PlayerScriptsUseInputActionSystem](/docs/reference/engine/classes/Workspace#PlayerScriptsUseInputActionSystem) is enabled. When set
to true (default), the PlayerModule injection point occurs at
[StarterPlayer](/docs/reference/engine/classes/StarterPlayer). When set to false, the default camera and control
scripts will not be added to the place.

Provide feedback

---

DevCameraOcclusionMode

Read Parallel

Sets how the default camera handles objects between the camera and the
player.

StarterPlayer.DevCameraOcclusionMode:[Enum.DevCameraOcclusionMode](/docs/reference/engine/enums/DevCameraOcclusionMode)

Defines how the default camera scripts handle objects between the camera
and the camera subject. Applies to all players as they join the experience
and can't be changed for individual players.

The default value is [Zoom](/docs/reference/engine/enums/DevCameraOcclusionMode) (0). See
[Enum.DevCameraOcclusionMode](/docs/reference/engine/enums/DevCameraOcclusionMode) for a list of available modes.

Provide feedback

---

DevComputerCameraMovementMode

Read Parallel

Lets you overwrite the player's camera mode on a computer.

StarterPlayer.DevComputerCameraMovementMode:[Enum.DevComputerCameraMovementMode](/docs/reference/engine/enums/DevComputerCameraMovementMode)

This property lets you overwrite the player's camera mode on a computer.

If set to [UserChoice](/docs/reference/engine/enums/DevComputerCameraMovementMode), the player's
camera movement mode will be determined by whatever they set in the
experience's settings. Otherwise, the mode will be set based on this
property.

This property does not affect players who are not on a computer.

Provide feedback

---

DevComputerMovementMode

Read Parallel

Lets you overwrite the player's movement mode on a computer.

StarterPlayer.DevComputerMovementMode:[Enum.DevComputerMovementMode](/docs/reference/engine/enums/DevComputerMovementMode)

This property lets you overwrite the player's movement mode on a computer.

If set to [UserChoice](/docs/reference/engine/enums/DevComputerMovementMode), the player's movement
mode will be determined by whatever they set in the experience's settings.
Otherwise, the mode will be set based on this property.

This property does not affect players who are not on a computer.

Provide feedback

---

DevTouchCameraMovementMode

Read Parallel

Lets you overwrite the player's camera mode on a touch-enabled device.

StarterPlayer.DevTouchCameraMovementMode:[Enum.DevTouchCameraMovementMode](/docs/reference/engine/enums/DevTouchCameraMovementMode)

This property lets you overwrite the player's camera mode on a
touch-enabled device.

If set to [UserChoice](/docs/reference/engine/enums/DevTouchCameraMovementMode), the player's
camera movement mode will be determined by whatever they set in the
experience's settings. Otherwise, the mode will be set based on this
property.

This property does not affect players who are not on a touch-enabled
device.

Provide feedback

---

DevTouchMovementMode

Read Parallel

Lets you overwrite the player's movement mode on a touch-enabled device.

StarterPlayer.DevTouchMovementMode:[Enum.DevTouchMovementMode](/docs/reference/engine/enums/DevTouchMovementMode)

This property lets you overwrite the player's movement mode on a
touch-enabled device.

If set to [UserChoice](/docs/reference/engine/enums/DevTouchMovementMode), the player's movement
mode will be determined by whatever they set in the experience's settings.
Otherwise, the mode will be set based on this property.

This property does not affect players who are not on a touch-enabled
device.

Provide feedback

---

EnableDynamicHeads

Not Scriptable

Read Parallel

StarterPlayer.EnableDynamicHeads:[Enum.LoadDynamicHeads](/docs/reference/engine/enums/LoadDynamicHeads)

Provide feedback

---

EnableMouseLockOption

Read Parallel

Determines if a player can toggle mouse lock by default.

StarterPlayer.EnableMouseLockOption:[boolean](/docs/luau/booleans)

This property determines if a player can toggle mouse lock by default.

Mouselock will lock the player's cursor to the center of the screen.
Moving the mouse will rotate the [Camera](/docs/reference/engine/classes/Camera) and [Player](/docs/reference/engine/classes/Player) will
move relative to the current rotation of the camera.

This property sets the value of [Player.DevEnableMouseLock](/docs/reference/engine/classes/Player#DevEnableMouseLock).

Note that shift-lock related APIs are in the process of being deprecated,
so it's recommended to use [UserInputService.MouseBehavior](/docs/reference/engine/classes/UserInputService#MouseBehavior) instead
to lock the mouse.

Code Samples

Enabling a Player's Mouse Lock

The example demonstrates how to enable and disabled whether a player can lock
their mouse.

In this example, we set the use a while true loop to toggle the state of the
DevEnabledMouseLock property between *true* and *false* every 5 seconds. While
this example has little practical use, it demos how to change the property via
a LocalScript.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



while true do



player.DevEnableMouseLock = not player.DevEnableMouseLock



task.wait(5)



end
```

Provide feedback

---

HealthDisplayDistance

Read Parallel

Sets the distance at which this player will see other [Humanoid](/docs/reference/engine/classes/Humanoid)
health bars. If set to 0, the health bars will not be displayed.

StarterPlayer.HealthDisplayDistance:[number](/docs/luau/numbers)

This property sets the distance in studs at which this player will see
other [Humanoid](/docs/reference/engine/classes/Humanoid) health bars. If set to 0, the health bars will not
be displayed. This property is set to 100 studs by default.

To change the display distance for a player once they join the game, you
can set the [Player.HealthDisplayDistance](/docs/reference/engine/classes/Player#HealthDisplayDistance) property.

If a [Humanoid](/docs/reference/engine/classes/Humanoid) health bar is visible, you can set the display type
using [Humanoid.DisplayDistanceType](/docs/reference/engine/classes/Humanoid#DisplayDistanceType).

Code Samples

Hiding Player Health and Names

This example demonstrates how to hide other Humanoid's (Player and NPC)
health bars and names.

This is done by setting the player's [Player.HealthDisplayDistance](/docs/reference/engine/classes/Player#HealthDisplayDistance) and
[Player.NameDisplayDistance](/docs/reference/engine/classes/Player#NameDisplayDistance) properties to 0.

If you would like to display health bars and names, you set the properties to
a value greater than 0. For instance, setting the properties to 100 means that
the player will see other player's health and names up to 100 studs away.

To modify the default values for players, you can change the values of the
StarterClass.Player.HealthDisplayDistance and
StarterClass.Player.NameDisplayDistance properties.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



player.HealthDisplayDistance = 0



player.NameDisplayDistance = 0
```

Provide feedback

---

LoadCharacterAppearance

Read Parallel

Whether or not the appearance of a player's character should be loaded.

StarterPlayer.LoadCharacterAppearance:[boolean](/docs/luau/booleans)

This property sets whether or not the appearance of a player's character
should be loaded.

Setting this to false results in the player having no clothes (including
hats), body colors, body packages or anything else related to the
appearance of the player's avatar. By default, this property is set to
true.

Setting this to true results in the player loading the appearance
corresponding to the player's [Player.CharacterAppearanceId](/docs/reference/engine/classes/Player#CharacterAppearanceId).

If [Player:LoadCharacterWithHumanoidDescription()](/docs/reference/engine/classes/Player#LoadCharacterWithHumanoidDescription) is used, it can
be advantageous to set [StarterPlayer.LoadCharacterAppearance](/docs/reference/engine/classes/StarterPlayer#LoadCharacterAppearance) to
false as the player's avatar is not required as all asset IDs to equip on
the character will come from the passed in [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription).

Code Samples

Disabling a Player's Appearance

This example demonstrates how to disable loading a player's character
appearance. Instead, the player loads as a grey model without any hats,
shirts, pants, etc.

This is useful for games using custom clothing and accessories.

Note that if the character has already spawned, this change will not take affect
until the player respawns or the [Player:LoadCharacter()](/docs/reference/engine/classes/Player#LoadCharacter) function is
called.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



player.CanLoadCharacterAppearance = false
```

Provide feedback

---

LoadCharacterLayeredClothing

Not Replicated

Not Scriptable

Read Parallel

Indicates whether characters spawning into an experience will have layered
clothing accessories equipped on them.

StarterPlayer.LoadCharacterLayeredClothing :[Enum.LoadCharacterLayeredClothing](/docs/reference/engine/enums/LoadCharacterLayeredClothing)

Indicates whether characters spawning into an experience will have layered
clothing accessories equipped on them (Although
[Workspace.MeshPartHeadsAndAccessories](/docs/reference/engine/classes/Workspace#MeshPartHeadsAndAccessories) also need to be enabled in
the [Workspace](/docs/reference/engine/classes/Workspace)).

Provide feedback

---

LuaCharacterController

Read Parallel

StarterPlayer.LuaCharacterController:[Enum.CharacterControlMode](/docs/reference/engine/enums/CharacterControlMode)

Provide feedback

---

NameDisplayDistance

Read Parallel

Sets the distance at which this player will see other [Humanoid](/docs/reference/engine/classes/Humanoid)
names.

StarterPlayer.NameDisplayDistance:[number](/docs/luau/numbers)

Sets the distance at which this player will see other [Humanoid](/docs/reference/engine/classes/Humanoid)
names. If set to 0, names are hidden. This property is set to 100
studs by default.

To change the display distance for a player once they join the game, you
can set the [Player.NameDisplayDistance](/docs/reference/engine/classes/Player#NameDisplayDistance) property.

If a [Humanoid](/docs/reference/engine/classes/Humanoid) name is visible, you can set the display type using
[Humanoid.DisplayDistanceType](/docs/reference/engine/classes/Humanoid#DisplayDistanceType).

Code Samples

Hiding Player Health and Names

This example demonstrates how to hide other Humanoid's (Player and NPC)
health bars and names.

This is done by setting the player's [Player.HealthDisplayDistance](/docs/reference/engine/classes/Player#HealthDisplayDistance) and
[Player.NameDisplayDistance](/docs/reference/engine/classes/Player#NameDisplayDistance) properties to 0.

If you would like to display health bars and names, you set the properties to
a value greater than 0. For instance, setting the properties to 100 means that
the player will see other player's health and names up to 100 studs away.

To modify the default values for players, you can change the values of the
StarterClass.Player.HealthDisplayDistance and
StarterClass.Player.NameDisplayDistance properties.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



player.HealthDisplayDistance = 0



player.NameDisplayDistance = 0
```

Provide feedback

---

UserEmotesEnabled

Read Parallel

Determines if user-owned emotes are loaded when loading avatars.

StarterPlayer.UserEmotesEnabled:[boolean](/docs/luau/booleans)

This property determines if user-owned emotes are loaded when loading
avatars. Setting this property to false disables loading. Developers can
set the property in Studio directly.

When emote loading is disabled, the emotes UI will still work as long as
developers choose to use the emotes feature by adding emotes within their
game.

See also [Avatar Emotes](/docs/characters/emotes), an article
detailing how to control, customize, and play avatar emotes.

Provide feedback

---