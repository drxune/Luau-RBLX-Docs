# ExperienceNotificationService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ExperienceNotificationService
Scraped: 2026-01-11T02:34:39.973929Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Instance
- ExperienceNotificationService
- Object
- CanPromptOptInAsync()
- PromptOptIn()
- Players.LocalPlayer
- LocalScript
- Script
- RunContext
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ExperienceNotificationService](/docs/reference/engine/classes/ExperienceNotificationService)

English

Feedback

Engine Class

ExperienceNotificationService

Service containing methods to validate users and prompt them to enable
experience notifications.

Not Creatable

Service

Not Replicated

---

Summary

Methods

|  |
| --- |
| [CanPromptOptInAsync](#CanPromptOptInAsync)():[boolean](/docs/luau/booleans) |
| [PromptOptIn](#PromptOptIn)():() |

Events

|  |
| --- |
| [OptInPromptClosed](#OptInPromptClosed)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[Experience notifications](/docs/production/promotion/experience-notifications)
are a way for 13+ users to keep up with their favorite experiences through
timely, personalized notifications. This service contains methods to validate
users and prompt them to enable notifications.

---

API Reference

Methods

CanPromptOptInAsync

Yields

Indicates whether the local player can be prompted to enable
notifications.

ExperienceNotificationService:CanPromptOptInAsync():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

Whether the local player can be prompted to enable notifications.

[CanPromptOptInAsync()](/docs/reference/engine/classes/ExperienceNotificationService#CanPromptOptInAsync)
returns true if the local player can be prompted to enable
notifications. You should always use the result of this method before
calling [PromptOptIn()](/docs/reference/engine/classes/ExperienceNotificationService#PromptOptIn)
since the ability to be prompted depends on various factors like the
player's age or whether they've already enabled notifications for your
experience.

This method always infers the local player
([Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer)) and it can only be called from a
[LocalScript](/docs/reference/engine/classes/LocalScript) or from a [Script](/docs/reference/engine/classes/Script) with
[RunContext](/docs/reference/engine/classes/BaseScript#RunContext) set to
[Client](/docs/reference/engine/enums/RunContext#Client). It should also be called in a
[pcall()](/docs/reference/engine/globals/LuaGlobals#pcall) since it's an asynchronous network call
that may occasionally fail.

See
[Experience notifications](/docs/production/promotion/experience-notifications)
for more details on implementing and customizing notifications, using
launch data, and more.

Code Samples

LocalScript - Notification Permission Prompt Implementation

```
local ExperienceNotificationService = game:GetService("ExperienceNotificationService")



-- Function to check whether the player can be prompted to enable notifications



local function canPromptOptIn()



local success, canPrompt = pcall(function()



return ExperienceNotificationService:CanPromptOptInAsync()



end)



return success and canPrompt



end



local canPrompt = canPromptOptIn()



if canPrompt then



local success, errorMessage = pcall(function()



ExperienceNotificationService:PromptOptIn()



end)



end



-- Listen to opt-in prompt closed event



ExperienceNotificationService.OptInPromptClosed:Connect(function()



print("Opt-in prompt closed")



end)
```

Provide feedback

---

PromptOptIn

Shows an in-experience prompt for the local player to enable
notifications.

ExperienceNotificationService:PromptOptIn():()

Returns

()

[PromptOptIn()](/docs/reference/engine/classes/ExperienceNotificationService#PromptOptIn) prompts
the local player to enable notifications through an in-experience modal.
You should always use the result of
[CanPromptOptInAsync()](/docs/reference/engine/classes/ExperienceNotificationService#CanPromptOptInAsync)
before calling this method since the ability to be prompted depends on
various factors like the player's age or whether they've already enabled
notifications for your experience.

This method always infers the local player
([Players.LocalPlayer](/docs/reference/engine/classes/Players#LocalPlayer)) and it can only be called from a
[LocalScript](/docs/reference/engine/classes/LocalScript) or from a [Script](/docs/reference/engine/classes/Script) with
[RunContext](/docs/reference/engine/classes/BaseScript#RunContext) set to
[Client](/docs/reference/engine/enums/RunContext#Client).

See
[Experience notifications](/docs/production/promotion/experience-notifications)
for more details on implementing and customizing notifications, using
launch data, and more.

Code Samples

LocalScript - Notification Permission Prompt Implementation

```
local ExperienceNotificationService = game:GetService("ExperienceNotificationService")



-- Function to check whether the player can be prompted to enable notifications



local function canPromptOptIn()



local success, canPrompt = pcall(function()



return ExperienceNotificationService:CanPromptOptInAsync()



end)



return success and canPrompt



end



local canPrompt = canPromptOptIn()



if canPrompt then



local success, errorMessage = pcall(function()



ExperienceNotificationService:PromptOptIn()



end)



end



-- Listen to opt-in prompt closed event



ExperienceNotificationService.OptInPromptClosed:Connect(function()



print("Opt-in prompt closed")



end)
```

Provide feedback

---

Events

OptInPromptClosed

Fires when the local player closes the prompt.

ExperienceNotificationService.OptInPromptClosed():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires when the local player closes a prompt that was displayed
through [PromptOptIn()](/docs/reference/engine/classes/ExperienceNotificationService#PromptOptIn).
It can only be connected in a [LocalScript](/docs/reference/engine/classes/LocalScript) or in a [Script](/docs/reference/engine/classes/Script)
with [RunContext](/docs/reference/engine/classes/BaseScript#RunContext) set to
[Client](/docs/reference/engine/enums/RunContext#Client).

See
[Experience notifications](/docs/production/promotion/experience-notifications)
for more details on implementing and customizing notifications, using
launch data, and more.

Code Samples

LocalScript - Notification Permission Prompt Implementation

```
local ExperienceNotificationService = game:GetService("ExperienceNotificationService")



-- Function to check whether the player can be prompted to enable notifications



local function canPromptOptIn()



local success, canPrompt = pcall(function()



return ExperienceNotificationService:CanPromptOptInAsync()



end)



return success and canPrompt



end



local canPrompt = canPromptOptIn()



if canPrompt then



local success, errorMessage = pcall(function()



ExperienceNotificationService:PromptOptIn()



end)



end



-- Listen to opt-in prompt closed event



ExperienceNotificationService.OptInPromptClosed:Connect(function()



print("Opt-in prompt closed")



end)
```

Provide feedback

---