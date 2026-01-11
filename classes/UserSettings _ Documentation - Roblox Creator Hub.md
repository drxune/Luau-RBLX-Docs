# UserSettings | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/UserSettings
Scraped: 2026-01-11T02:30:32.775622Z

## Tags
- Not Creatable

## Inherits
- GenericSettings
- UserSettings
- ServiceProvider
- Instance
- Object
- UserGameSettings
- UserSettings()
- GlobalSettings:GetFFlag()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [GenericSettings](/docs/reference/engine/classes/GenericSettings)
6. /
7. [UserSettings](/docs/reference/engine/classes/UserSettings)

English

Feedback

Engine Class

UserSettings

A singleton object that houses basic user settings, which persist across all
games on Roblox.

Not Creatable

---

Summary

Methods

|  |
| --- |
| [IsUserFeatureEnabled](#IsUserFeatureEnabled)(name: [string](/docs/luau/strings)):[boolean](/docs/luau/booleans) |
| [Reset](#Reset)():() |

Inherited Members

7 inherited from [ServiceProvider](/docs/reference/engine/classes/ServiceProvider)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

UserSettings is a singleton object that is used to house basic user settings,
which persist across all games. Currently, it only stores the
[UserGameSettings](/docs/reference/engine/classes/UserGameSettings) object.

You can retrieve a reference to this object via the
[UserSettings()](/docs/reference/engine/classes/UserSettings) function, which returns it.

Code Samples

IsUserFeatureEnabled Sample

A basic sample of how the IsUserFeatureEnabled function is used by Roblox to
control certain features.

```
if UserSettings():IsUserFeatureEnabled("UserNoCameraClickToMove") then



print("'ClickToMove' should no longer be loaded from the CameraScript!")



else



print("'ClickToMove' is still loaded from the CameraScript!")



end
```

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

Methods

IsUserFeatureEnabled

Returns true if the specified user feature is enabled. This will throw an
error if the user feature does not exist.

UserSettings:IsUserFeatureEnabled(name:[string](/docs/luau/strings)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings) |

Returns

[boolean](/docs/luau/booleans)

Returns true if the specified user feature is enabled. This will throw an
error if the user feature does not exist.

This function checks against a list of FFlags, whose name starts with
"User". The function is intended to be used by Roblox-created scripts, and
functions similarly to [GlobalSettings:GetFFlag()](/docs/reference/engine/classes/GlobalSettings#GetFFlag).

Code Samples

IsUserFeatureEnabled Sample

A basic sample of how the IsUserFeatureEnabled function is used by Roblox to
control certain features.

```
if UserSettings():IsUserFeatureEnabled("UserNoCameraClickToMove") then



print("'ClickToMove' should no longer be loaded from the CameraScript!")



else



print("'ClickToMove' is still loaded from the CameraScript!")



end
```

Provide feedback

---

Reset

Erases the saved state of the UserSettings, and restores its default
values.

UserSettings:Reset():()

Returns

()

Erases the saved state of the UserSettings, and restores its values back
to default. This function will fail to run correctly from a LocalScript,
as it does not have permission to restore all of the properties in the
[UserGameSettings](/docs/reference/engine/classes/UserGameSettings) class.

Provide feedback

---