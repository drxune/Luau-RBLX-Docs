# UserGameSettings | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/UserGameSettings
Scraped: 2026-01-11T02:29:41.956031Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Instance
- UserGameSettings
- UserSettings
- Object
- LocalScript
- UserGameSettings:SetOnboardingCompleted()
- UserGameSettings:GetOnboardingCompleted()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [UserGameSettings](/docs/reference/engine/classes/UserGameSettings)

English

Feedback

Engine Class

UserGameSettings

The UserGameSettings is a singleton class found inside of the
[UserSettings](/docs/reference/engine/classes/UserSettings) singleton. It holds various persistent settings relating
to how the user wants to control their camera, and their character.

Not Creatable

Service

Not Replicated

---

Summary

Properties

|  |
| --- |
| [AllTutorialsDisabled](#AllTutorialsDisabled):[boolean](/docs/luau/booleans) |
| [BadgeVisible](#BadgeVisible):[boolean](/docs/luau/booleans) |
| [CameraMode](#CameraMode):[Enum.CustomCameraMode](/docs/reference/engine/enums/CustomCameraMode) |
| [ChatVisible](#ChatVisible):[boolean](/docs/luau/booleans) |
| [ComputerCameraMovementMode](#ComputerCameraMovementMode):[Enum.ComputerCameraMovementMode](/docs/reference/engine/enums/ComputerCameraMovementMode) |
| [ComputerMovementMode](#ComputerMovementMode):[Enum.ComputerMovementMode](/docs/reference/engine/enums/ComputerMovementMode) |
| [ControlMode](#ControlMode):[Enum.ControlMode](/docs/reference/engine/enums/ControlMode)  Deprecated |
| [Fullscreen](#Fullscreen):[boolean](/docs/luau/booleans) |
| [GamepadCameraSensitivity](#GamepadCameraSensitivity):[number](/docs/luau/numbers) |
| [GraphicsOptimizationMode](#GraphicsOptimizationMode):[Enum.GraphicsOptimizationMode](/docs/reference/engine/enums/GraphicsOptimizationMode) |
| [GraphicsQualityLevel](#GraphicsQualityLevel):[number](/docs/luau/numbers) |
| [HasEverUsedVR](#HasEverUsedVR):[boolean](/docs/luau/booleans) |
| [MasterVolume](#MasterVolume):[number](/docs/luau/numbers) |
| [MasterVolumeStudio](#MasterVolumeStudio):[number](/docs/luau/numbers) |
| [MaxQualityEnabled](#MaxQualityEnabled):[boolean](/docs/luau/booleans) |
| [MouseSensitivity](#MouseSensitivity):[number](/docs/luau/numbers) |
| [OnboardingsCompleted](#OnboardingsCompleted):[string](/docs/luau/strings) |
| [PartyVoiceVolume](#PartyVoiceVolume):[number](/docs/luau/numbers) |
| [PeoplePageLayout](#PeoplePageLayout):PeoplePageLayout |
| [PlayerListVisible](#PlayerListVisible):[boolean](/docs/luau/booleans) |
| [PlayerNamesEnabled](#PlayerNamesEnabled):[boolean](/docs/luau/booleans) |
| [RCCProfilerRecordFrameRate](#RCCProfilerRecordFrameRate):[number](/docs/luau/numbers) |
| [RCCProfilerRecordTimeFrame](#RCCProfilerRecordTimeFrame):[number](/docs/luau/numbers) |
| [RotationType](#RotationType):[Enum.RotationType](/docs/reference/engine/enums/RotationType) |
| [SavedQualityLevel](#SavedQualityLevel):[Enum.SavedQualitySetting](/docs/reference/engine/enums/SavedQualitySetting) |
| [StartMaximized](#StartMaximized):[boolean](/docs/luau/booleans) |
| [StartScreenPosition](#StartScreenPosition):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [StartScreenSize](#StartScreenSize):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [TouchCameraMovementMode](#TouchCameraMovementMode):[Enum.TouchCameraMovementMode](/docs/reference/engine/enums/TouchCameraMovementMode) |
| [TouchMovementMode](#TouchMovementMode):[Enum.TouchMovementMode](/docs/reference/engine/enums/TouchMovementMode) |
| [UsedCoreGuiIsVisibleToggle](#UsedCoreGuiIsVisibleToggle):[boolean](/docs/luau/booleans) |
| [UsedCustomGuiIsVisibleToggle](#UsedCustomGuiIsVisibleToggle):[boolean](/docs/luau/booleans) |
| [UsedHideHudShortcut](#UsedHideHudShortcut):[boolean](/docs/luau/booleans) |
| [VignetteEnabled](#VignetteEnabled):[boolean](/docs/luau/booleans) |
| [VREnabled](#VREnabled):[boolean](/docs/luau/booleans) |
| [VRRotationIntensity](#VRRotationIntensity):[number](/docs/luau/numbers) |
| [VRSmoothRotationEnabled](#VRSmoothRotationEnabled):[boolean](/docs/luau/booleans) |

Methods

|  |
| --- |
| [GetCameraYInvertValue](#GetCameraYInvertValue)():[number](/docs/luau/numbers) |
| [GetOnboardingCompleted](#GetOnboardingCompleted)(onboardingId: [string](/docs/luau/strings)):[boolean](/docs/luau/booleans) |
| [InFullScreen](#InFullScreen)():[boolean](/docs/luau/booleans) |
| [InStudioMode](#InStudioMode)():[boolean](/docs/luau/booleans) |
| [SetCameraYInvertVisible](#SetCameraYInvertVisible)():() |
| [SetGamepadCameraSensitivityVisible](#SetGamepadCameraSensitivityVisible)():() |
| [SetOnboardingCompleted](#SetOnboardingCompleted)(onboardingId: [string](/docs/luau/strings)):() |

Events

|  |
| --- |
| [FullscreenChanged](#FullscreenChanged)(isFullscreen: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [StudioModeChanged](#StudioModeChanged)(isStudioMode: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The UserGameSettings is a singleton class found inside of the
[UserSettings](/docs/reference/engine/classes/UserSettings) singleton. It holds various persistent settings relating
to how the user wants to control their camera, and their character.

You can access this object from a [LocalScript](/docs/reference/engine/classes/LocalScript) via:

```
UserSettings():GetService("UserGameSettings")
```

This object is intended to be used on the client only, as it serves no purpose
on the server. It will also reflect your own settings when testing in Roblox
Studio.

Code Samples

UserGameSettings Listener

A basic example that shows how you can listen to changes in the user's
settings. With this code pasted into a LocalScript running in the
StarterPlayerScripts, you can change settings in Roblox's game menu, and see
their values appear in the output as detected changes.

```
local gameSettings = UserSettings().GameSettings



local function onGameSettingChanged(nameOfSetting)



-- Fetch the value of this setting through a pcall to make sure we can retrieve it.



-- Sometimes the event fires with properties that LocalScripts can't access.



local canGetSetting, setting = pcall(function()



return gameSettings[nameOfSetting]



end)



if canGetSetting then



print("Your " .. nameOfSetting .. " has changed to: " .. tostring(setting))



end



end



gameSettings.Changed:Connect(onGameSettingChanged)
```

---

API Reference

Properties

AllTutorialsDisabled

Roblox Script Security

Read Parallel

UserGameSettings.AllTutorialsDisabled:[boolean](/docs/luau/booleans)

Provide feedback

---

BadgeVisible

Roblox Script Security

Read Parallel

UserGameSettings.BadgeVisible:[boolean](/docs/luau/booleans)

Provide feedback

---

CameraMode

Roblox Script Security

Read Parallel

UserGameSettings.CameraMode:[Enum.CustomCameraMode](/docs/reference/engine/enums/CustomCameraMode)

Provide feedback

---

ChatVisible

Roblox Script Security

Read Parallel

UserGameSettings.ChatVisible:[boolean](/docs/luau/booleans)

Provide feedback

---

ComputerCameraMovementMode

Read Parallel

The camera movement mode currently in-use by the client on desktop.

UserGameSettings.ComputerCameraMovementMode:[Enum.ComputerCameraMovementMode](/docs/reference/engine/enums/ComputerCameraMovementMode)

The camera movement mode currently in-use by the client on desktop.

Provide feedback

---

ComputerMovementMode

Read Parallel

The type of controls being used by the client on desktop.

UserGameSettings.ComputerMovementMode:[Enum.ComputerMovementMode](/docs/reference/engine/enums/ComputerMovementMode)

The type of controls being used by the client on desktop.

Provide feedback

---

ControlMode

Deprecated

Show details

---

Fullscreen

Roblox Script Security

Read Parallel

UserGameSettings.Fullscreen:[boolean](/docs/luau/booleans)

Provide feedback

---

GamepadCameraSensitivity

Read Parallel

Describes how sensitive the camera is when using a gamepad.

UserGameSettings.GamepadCameraSensitivity:[number](/docs/luau/numbers)

Describes how sensitive the camera is when using a gamepad.

Provide feedback

---

GraphicsOptimizationMode

Roblox Script Security

Read Parallel

UserGameSettings.GraphicsOptimizationMode:[Enum.GraphicsOptimizationMode](/docs/reference/engine/enums/GraphicsOptimizationMode)

Provide feedback

---

GraphicsQualityLevel

Roblox Script Security

Read Parallel

UserGameSettings.GraphicsQualityLevel:[number](/docs/luau/numbers)

Provide feedback

---

HasEverUsedVR

Roblox Script Security

Read Parallel

UserGameSettings.HasEverUsedVR:[boolean](/docs/luau/booleans)

Provide feedback

---

MasterVolume

Roblox Script Security

Read Parallel

A float between 0 and 1 representing the volume of the game's client.

UserGameSettings.MasterVolume:[number](/docs/luau/numbers)

A [float](/docs/luau/numbers) between 0 and 1
representing the volume of the game's client.

Provide feedback

---

MasterVolumeStudio

Roblox Script Security

Read Parallel

UserGameSettings.MasterVolumeStudio:[number](/docs/luau/numbers)

Provide feedback

---

MaxQualityEnabled

Roblox Script Security

Read Parallel

UserGameSettings.MaxQualityEnabled:[boolean](/docs/luau/booleans)

Provide feedback

---

MouseSensitivity

Read Parallel

A float between 0 and 4 representing the sensitivity of the client's
camera sensitivity.

UserGameSettings.MouseSensitivity:[number](/docs/luau/numbers)

A float between 0 and 4 representing the sensitivity of the client's
camera sensitivity.

Provide feedback

---

OnboardingsCompleted

Roblox Script Security

Read Parallel

UserGameSettings.OnboardingsCompleted:[string](/docs/luau/strings)

Provide feedback

---

PartyVoiceVolume

Roblox Script Security

Read Parallel

UserGameSettings.PartyVoiceVolume:[number](/docs/luau/numbers)

Provide feedback

---

PeoplePageLayout

Roblox Script Security

Read Parallel

UserGameSettings.PeoplePageLayout:PeoplePageLayout

Provide feedback

---

PlayerListVisible

Roblox Script Security

Read Parallel

UserGameSettings.PlayerListVisible:[boolean](/docs/luau/booleans)

Provide feedback

---

PlayerNamesEnabled

Roblox Script Security

Read Parallel

UserGameSettings.PlayerNamesEnabled:[boolean](/docs/luau/booleans)

Provide feedback

---

RCCProfilerRecordFrameRate

Read Parallel

UserGameSettings.RCCProfilerRecordFrameRate:[number](/docs/luau/numbers)

Provide feedback

---

RCCProfilerRecordTimeFrame

Read Parallel

UserGameSettings.RCCProfilerRecordTimeFrame:[number](/docs/luau/numbers)

Provide feedback

---

RotationType

Read Parallel

Controls how the client's character is rotated.

UserGameSettings.RotationType:[Enum.RotationType](/docs/reference/engine/enums/RotationType)

Controls how the client's character is rotated.

Provide feedback

---

SavedQualityLevel

Read Parallel

The graphics quality level set by the client.

UserGameSettings.SavedQualityLevel:[Enum.SavedQualitySetting](/docs/reference/engine/enums/SavedQualitySetting)

The graphics quality level set by the client.

Provide feedback

---

StartMaximized

Not Replicated

Not Scriptable

Roblox Script Security

Read Parallel

UserGameSettings.StartMaximized:[boolean](/docs/luau/booleans)

Provide feedback

---

StartScreenPosition

Not Replicated

Not Scriptable

Roblox Script Security

Read Parallel

UserGameSettings.StartScreenPosition:[Vector2](/docs/reference/engine/datatypes/Vector2)

Provide feedback

---

StartScreenSize

Not Replicated

Not Scriptable

Roblox Script Security

Read Parallel

UserGameSettings.StartScreenSize:[Vector2](/docs/reference/engine/datatypes/Vector2)

Provide feedback

---

TouchCameraMovementMode

Read Parallel

The camera type in-use by the client while on a mobile device.

UserGameSettings.TouchCameraMovementMode:[Enum.TouchCameraMovementMode](/docs/reference/engine/enums/TouchCameraMovementMode)

The camera type in-use by the client while on a mobile device.

Provide feedback

---

TouchMovementMode

Read Parallel

The type of controls being used by the client on a mobile device.

UserGameSettings.TouchMovementMode:[Enum.TouchMovementMode](/docs/reference/engine/enums/TouchMovementMode)

The type of controls being used by the client on a mobile device.

Provide feedback

---

UsedCoreGuiIsVisibleToggle

Roblox Script Security

Read Parallel

UserGameSettings.UsedCoreGuiIsVisibleToggle:[boolean](/docs/luau/booleans)

Provide feedback

---

UsedCustomGuiIsVisibleToggle

Roblox Script Security

Read Parallel

UserGameSettings.UsedCustomGuiIsVisibleToggle:[boolean](/docs/luau/booleans)

Provide feedback

---

UsedHideHudShortcut

Roblox Script Security

Read Parallel

UserGameSettings.UsedHideHudShortcut:[boolean](/docs/luau/booleans)

Provide feedback

---

VignetteEnabled

Roblox Script Security

Read Parallel

UserGameSettings.VignetteEnabled:[boolean](/docs/luau/booleans)

Provide feedback

---

VREnabled

Roblox Script Security

Read Parallel

UserGameSettings.VREnabled:[boolean](/docs/luau/booleans)

Provide feedback

---

VRRotationIntensity

Roblox Script Security

Read Parallel

UserGameSettings.VRRotationIntensity:[number](/docs/luau/numbers)

Provide feedback

---

VRSmoothRotationEnabled

Roblox Script Security

Read Parallel

UserGameSettings.VRSmoothRotationEnabled:[boolean](/docs/luau/booleans)

Provide feedback

---

Methods

GetCameraYInvertValue

Returns the camera's Y-invert value.

UserGameSettings:GetCameraYInvertValue():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

Returns the camera's Y-invert value.

Provide feedback

---

GetOnboardingCompleted

Checks if onboarding has been completed.

UserGameSettings:GetOnboardingCompleted(onboardingId:[string](/docs/luau/strings)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| onboardingId:[string](/docs/luau/strings)  The onboarding ID to inquire about. |

Returns

[boolean](/docs/luau/booleans)

Whether or not the onboarding in particular has been completed yet.

Checks whether or not the given onboarding has been completed yet, which
is useful for avoiding showing the onboarding animation again.

If onboardingId is not one of the accepted IDs, an error is thrown.

The onboarding process is one-way. This means that, as a developer, you
can force the onboarding process to completion but cannot reset it.

See also:

* [UserGameSettings:SetOnboardingCompleted()](/docs/reference/engine/classes/UserGameSettings#SetOnboardingCompleted), sets onboarding as
  completed

Provide feedback

---

InFullScreen

Returns true if the user's Roblox window is in full screen mode.

UserGameSettings:InFullScreen():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

Returns true if the user's Roblox window is in full screen mode.

Provide feedback

---

InStudioMode

Returns true if the client's game session is in Roblox Studio.

UserGameSettings:InStudioMode():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

Returns true if the client's game session is in Roblox Studio.

Provide feedback

---

SetCameraYInvertVisible

If called, Roblox toggles the menu option to invert the user's camera y
axis.

UserGameSettings:SetCameraYInvertVisible():()

Returns

()

If called, Roblox toggles the menu option to invert the user's camera y
axis.

Provide feedback

---

SetGamepadCameraSensitivityVisible

If called, Roblox toggles the menu option to control the camera
sensitivity with gamepads.

UserGameSettings:SetGamepadCameraSensitivityVisible():()

Returns

()

If called, Roblox toggles the menu option to control the camera
sensitivity with gamepads.

Provide feedback

---

SetOnboardingCompleted

Sets onboarding as completed.

UserGameSettings:SetOnboardingCompleted(onboardingId:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| onboardingId:[string](/docs/luau/strings)  The onboarding ID to set as completed. |

Returns

()

Sets the given onboarding as completed, so it won't be shown again to the
user the next time they play.

Currently, this function only accepts
[DynamicThumbstick](/docs/luau/strings), and it is used to
persistently track whether or not the player has finished the tutorial for
the Dynamic Thumbstick control scheme. If onboardingId is not one of the
accepted IDs, an error is thrown.

The onboarding process is one-way. This means that, as a developer, you
can force the onboarding process to completion but cannot reset it.

See also:

* [UserGameSettings:GetOnboardingCompleted()](/docs/reference/engine/classes/UserGameSettings#GetOnboardingCompleted), checks if onboarding
  has been completed

Provide feedback

---

Events

FullscreenChanged

Fires if the user's full screen mode is changed.

UserGameSettings.FullscreenChanged(isFullscreen:[boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| isFullscreen:[boolean](/docs/luau/booleans) |

Fires if the user's full screen mode is changed. The event will only fire
on desktop devices that can toggle full screen mode. The game will always
be in full screen on mobile devices and consoles.

Code Samples

Full Screen Mode Detection

A LocalScript that demonstrates how you can detect whether a game is in full
screen or not.

```
local gameSettings = UserSettings().GameSettings



local function checkFullScreenMode()



local inFullscreen = gameSettings:InFullScreen()



if inFullscreen then



print("Full Screen mode enabled!")



else



print("Full Screen mode disabled!")



end



end



checkFullScreenMode()



gameSettings.FullscreenChanged:Connect(checkFullScreenMode)
```

Provide feedback

---

StudioModeChanged

Fired when the user's client switches between Studio mode and in-game
mode. This gets fired periodically in Roblox Studio when a session starts.

UserGameSettings.StudioModeChanged(isStudioMode:[boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| isStudioMode:[boolean](/docs/luau/booleans) |

Fired when the user's client switches between Studio mode and in-game
mode. This gets fired periodically in Roblox Studio when a session starts.

Provide feedback

---