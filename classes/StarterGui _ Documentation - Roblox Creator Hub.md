# StarterGui | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/StarterGui
Scraped: 2026-01-11T02:29:48.533169Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- BasePlayerGui
- StarterGui
- LayerCollector
- PlayerGui
- Players
- CoreGui
- Instance
- Object
- ScreenGuis
- Player.Character
- ResetOnSpawn
- Player
- StarterGui:SetCoreGuiEnabled()
- StarterGui:SetCore()
- PlayerGui.ScreenOrientation
- PlayerGui.CurrentScreenOrientation
- SetCore()
- UserIds
- BindableEvent
- VRService.VREnabled
- BindableEvents
- BindableFunctions
- SetCoreGuiEnabled()
- TextChatService.ChatVersion
- TextChatService
- TextChannel:DisplaySystemMessage()
- BindableFunction
- CoreGuis
- SetCoreGuiEnabled
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [BasePlayerGui](/docs/reference/engine/classes/BasePlayerGui)
6. /
7. [StarterGui](/docs/reference/engine/classes/StarterGui)

English

Feedback

Engine Class

![StarterGui](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/StarterGui-Dark.webp)StarterGui

A container for [LayerCollector](/docs/reference/engine/classes/LayerCollector) objects to be copied into the
[PlayerGui](/docs/reference/engine/classes/PlayerGui) of [Players](/docs/reference/engine/classes/Player). Also provides a range of
functions for interacting with the [CoreGui](/docs/reference/engine/classes/CoreGui).

Not Creatable

Service

---

Summary

Properties

|  |
| --- |
| [ProcessUserInput](#ProcessUserInput):[boolean](/docs/luau/booleans) |
| [ResetPlayerGuiOnSpawn](#ResetPlayerGuiOnSpawn):[boolean](/docs/luau/booleans)  Deprecated |
| [RtlTextSupport](#RtlTextSupport):[Enum.RtlTextSupport](/docs/reference/engine/enums/RtlTextSupport) |
| [ScreenOrientation](#ScreenOrientation):[Enum.ScreenOrientation](/docs/reference/engine/enums/ScreenOrientation) |
| [ShowDevelopmentGui](#ShowDevelopmentGui):[boolean](/docs/luau/booleans) |
| [VirtualCursorMode](#VirtualCursorMode):[Enum.VirtualCursorMode](/docs/reference/engine/enums/VirtualCursorMode) |

Methods

|  |
| --- |
| [GetCore](#GetCore)(parameterName: [string](/docs/luau/strings)):Variant |
| [GetCoreGuiEnabled](#GetCoreGuiEnabled)(coreGuiType: [Enum.CoreGuiType](/docs/reference/engine/enums/CoreGuiType)):[boolean](/docs/luau/booleans) |
| [SetCore](#SetCore)(parameterName: [string](/docs/luau/strings),value: Variant):() |
| [SetCoreGuiEnabled](#SetCoreGuiEnabled)(coreGuiType: [Enum.CoreGuiType](/docs/reference/engine/enums/CoreGuiType),enabled: [boolean](/docs/luau/booleans)):() |

Inherited Members

1 inherited from [BasePlayerGui](/docs/reference/engine/classes/BasePlayerGui)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[StarterGui](/docs/reference/engine/classes/StarterGui) is a container object designed to hold
[LayerCollector](/docs/reference/engine/classes/LayerCollector) objects such as [ScreenGuis](/docs/reference/engine/classes/ScreenGui).

When a [Player.Character](/docs/reference/engine/classes/Player#Character) spawns, the contents of their
[PlayerGui](/docs/reference/engine/classes/PlayerGui) (if any) are emptied. Children of the [StarterGui](/docs/reference/engine/classes/StarterGui) are
then copied along with their descendants into the [PlayerGui](/docs/reference/engine/classes/PlayerGui). Note,
however, that [LayerCollector](/docs/reference/engine/classes/LayerCollector) objects such as
[ScreenGuis](/docs/reference/engine/classes/ScreenGui) with their
[ResetOnSpawn](/docs/reference/engine/classes/LayerCollector#ResetOnSpawn) property set to false will
only be placed into each player's [PlayerGui](/docs/reference/engine/classes/PlayerGui) once and will not be
deleted when the [Player](/docs/reference/engine/classes/Player) respawns.

[StarterGui](/docs/reference/engine/classes/StarterGui) also includes a range of functions allowing you to interact
with the [CoreGui](/docs/reference/engine/classes/CoreGui). For example [StarterGui:SetCoreGuiEnabled()](/docs/reference/engine/classes/StarterGui#SetCoreGuiEnabled)
can be used to disable elements of the [CoreGui](/docs/reference/engine/classes/CoreGui), and
[StarterGui:SetCore()](/docs/reference/engine/classes/StarterGui#SetCore) can perform a range of functions including
creating notifications and system messages.

---

API Reference

Properties

ProcessUserInput

Hidden

Not Replicated

Plugin Security

Read Parallel

Allows this service to process input like [PlayerGui](/docs/reference/engine/classes/PlayerGui) and
[CoreGui](/docs/reference/engine/classes/CoreGui) do.

StarterGui.ProcessUserInput:[boolean](/docs/luau/booleans)

Allows [StarterGui](/docs/reference/engine/classes/StarterGui) to process input like [PlayerGui](/docs/reference/engine/classes/PlayerGui) and
[CoreGui](/docs/reference/engine/classes/CoreGui) do. The default value is false.

Provide feedback

---

ResetPlayerGuiOnSpawn

Deprecated

Show details

---

RtlTextSupport

Not Scriptable

Read Parallel

StarterGui.RtlTextSupport:[Enum.RtlTextSupport](/docs/reference/engine/enums/RtlTextSupport)

Provide feedback

---

ScreenOrientation

Read Parallel

Sets the default screen orientation mode for users with mobile devices.

StarterGui.ScreenOrientation:[Enum.ScreenOrientation](/docs/reference/engine/enums/ScreenOrientation)

This property sets the preferred screen orientation mode for users with
mobile devices. For the different modes available, see
[Enum.ScreenOrientation](/docs/reference/engine/enums/ScreenOrientation).

By default, this property is set to
[Sensor](/docs/reference/engine/enums/ScreenOrientation#Sensor), meaning the experience is
displayed depending on the best match to the device's current orientation,
either landscape (left/right) or portrait.

When a [Player](/docs/reference/engine/classes/Player) joins the experience on a mobile device, this
property determines the device's starting orientation and sets that
player's [PlayerGui.ScreenOrientation](/docs/reference/engine/classes/PlayerGui#ScreenOrientation) accordingly. You can also get
the player's current screen orientation through
[PlayerGui.CurrentScreenOrientation](/docs/reference/engine/classes/PlayerGui#CurrentScreenOrientation), useful when using one of the
"sensor" [Enum.ScreenOrientation](/docs/reference/engine/enums/ScreenOrientation) settings.

Note that changing this property will not change the screen orientation
for [Players](/docs/reference/engine/classes/Player) already in the experience. To change the
orientation for an existing player, use their
[PlayerGui.ScreenOrientation](/docs/reference/engine/classes/PlayerGui#ScreenOrientation) property.

Provide feedback

---

ShowDevelopmentGui

Read Parallel

Determines whether the contents of [StarterGui](/docs/reference/engine/classes/StarterGui) is visible in
Studio.

StarterGui.ShowDevelopmentGui:[boolean](/docs/luau/booleans)

This property determines whether the contents of [StarterGui](/docs/reference/engine/classes/StarterGui) is
visible in Studio.

Provide feedback

---

VirtualCursorMode

Not Scriptable

Read Parallel

StarterGui.VirtualCursorMode:[Enum.VirtualCursorMode](/docs/reference/engine/enums/VirtualCursorMode)

Provide feedback

---

Methods

GetCore

Yields

Returns a variable that has been specified by a Roblox core script.

StarterGui:GetCore(parameterName:[string](/docs/luau/strings)):Variant

Parameters

|  |
| --- |
| parameterName:[string](/docs/luau/strings) |

Returns

Variant

This method returns data set or made available by Roblox's core scripts.
The first and only parameter is a string that selects the information to
be fetched. The following sections describe the strings and the data they
return by this function.

Calling this method may yield. Many of these also register an equivalent
[SetCore()](/docs/reference/engine/classes/StarterGui#SetCore) function (these are marked with an
asterisk).

##### PointsNotificationsActive \*

Returns true if player point notifications are enabled.

##### BadgesNotificationsActive \*

Returns true if badge notifications are enabled.

##### AvatarContextMenuEnabled \*

Returns true if the
[Avatar Context Menu](/docs/players/avatar-context-menu) is enabled.

##### ChatActive \*

Returns whether the chat is active or not. This is indicated by the
selection state of the top bar's chat icon.

##### ChatWindowSize \*

Returns the size of the chat window as a [UDim2](/docs/reference/engine/datatypes/UDim2).

##### ChatWindowPosition \*

Returns the size of the chat window as a [UDim2](/docs/reference/engine/datatypes/UDim2).

##### ChatBarDisabled \*

Returns true if the chat bar is disabled.

##### GetBlockedUserIds

Returns a list of [UserIds](/docs/reference/engine/classes/Player#UserId) associated with users that
have been blocked by the local player.

##### PlayerBlockedEvent

Returns a [BindableEvent](/docs/reference/engine/classes/BindableEvent) that is fired whenever a player is blocked
by the local player.

##### PlayerUnblockedEvent

Returns a [BindableEvent](/docs/reference/engine/classes/BindableEvent) that is fired whenever a player is
unblocked by the local player.

##### PlayerMutedEvent

Returns a [BindableEvent](/docs/reference/engine/classes/BindableEvent) that is fired whenever a player is muted
by the local player.

##### PlayerUnmutedEvent

Returns a [BindableEvent](/docs/reference/engine/classes/BindableEvent) that is fired whenever a player is unmuted
by the local player.

##### PlayerFriendedEvent

Returns a [BindableEvent](/docs/reference/engine/classes/BindableEvent) that is fired whenever a player is
connected by the local player.

##### PlayerUnfriendedEvent

Returns a [BindableEvent](/docs/reference/engine/classes/BindableEvent) that is fired whenever a player is
unconnected by the local player.

##### DevConsoleVisible \*

Returns true if the
[Developer Console](/docs/studio/developer-console) is visible.

##### VRRotationIntensity

Returns a string describing the camera rotation sensitivity in VR: Low,
High and Smooth. This will not be available unless
[VRService.VREnabled](/docs/reference/engine/classes/VRService#VREnabled) is true.

Provide feedback

---

GetCoreGuiEnabled

Returns whether the given [Enum.CoreGuiType](/docs/reference/engine/enums/CoreGuiType)is enabled, or if it has been
disabled using [StarterGui:SetCoreGuiEnabled()](/docs/reference/engine/classes/StarterGui#SetCoreGuiEnabled).

StarterGui:GetCoreGuiEnabled(coreGuiType:[Enum.CoreGuiType](/docs/reference/engine/enums/CoreGuiType)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| coreGuiType:[Enum.CoreGuiType](/docs/reference/engine/enums/CoreGuiType)  The given [Enum.CoreGuiType](/docs/reference/engine/enums/CoreGuiType). |

Returns

[boolean](/docs/luau/booleans)

Whether the given [Enum.CoreGuiType](/docs/reference/engine/enums/CoreGuiType) is enabled.

This function returns whether the given [Enum.CoreGuiType](/docs/reference/engine/enums/CoreGuiType)is enabled, or
if it has been disabled using [StarterGui:SetCoreGuiEnabled()](/docs/reference/engine/classes/StarterGui#SetCoreGuiEnabled). This
function should be called on the client.

Note that setting "TopbarEnabled" to false using
[SetCore()](/docs/reference/engine/classes/StarterGui#SetCore) hides all
[CoreGuiTypes](/docs/reference/engine/enums/CoreGuiType) but does not affect the result of this
function.

Code Samples

Checking if a Core GUI is Enabled

The below example would print whether or not the player list is visible to the
LocalPlayer.

```
local StarterGui = game:GetService("StarterGui")



print(StarterGui:GetCoreGuiEnabled("PlayerList"))
```

Provide feedback

---

SetCore

Allows you to perform certain interactions with Roblox's core scripts.

StarterGui:SetCore(

parameterName:[string](/docs/luau/strings), value:Variant

):()

Parameters

|  |
| --- |
| parameterName:[string](/docs/luau/strings)  Selects the functionality with which the call will interact. |
| value:Variant  A table of [BindableEvents](/docs/reference/engine/classes/BindableEvent) and [BindableFunctions](/docs/reference/engine/classes/BindableFunction). |

Returns

()

This method (not to be confused with
[SetCoreGuiEnabled()](/docs/reference/engine/classes/StarterGui#SetCoreGuiEnabled)) exposes a
variety of functionality defined by Roblox's core scripts, such as sending
notifications, toggling notifications for badges/points, defining a
callback for the reset button, or toggling the topbar.

The first parameter is a string that selects the functionality with which
the call will interact. It may be necessary to call this method multiple
times using [pcall()](/docs/reference/engine/globals/LuaGlobals#pcall) in case the respective core script
has not yet loaded (or if it has been disabled entirely).

The following table describes the strings that may be accepted as the
first parameter. The parameters that should follow are dependent on the
functionality that will be used and are described in sub-tables.

##### ChatActive

Controls whether the chat is active.

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| active | boolean | (required) | Determines whether the chat should be made active. |

##### PointsNotificationsActive

Controls whether notifications for earned player points will appear.

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| active | boolean | (required) | Determines whether notifications for earned player points will appear. |

##### BadgesNotificationsActive

Controls whether notifications for earned badges will appear.

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| active | boolean | (required) | Determines whether notifications for earned badges will appear. |

##### ResetButtonCallback

Determines the behavior, if any, of the reset button given a boolean or a
[BindableEvent](/docs/reference/engine/classes/BindableEvent) to be fired when a player requests to reset.

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| enabled | boolean | (required) | Determines whether the reset button retains its default behavior. |
| **OR** | | | |
| callback | [BindableEvent](/docs/reference/engine/classes/BindableEvent) | (required) | A [BindableEvent](/docs/reference/engine/classes/BindableEvent) to be fired when the player confirms they want to reset. |

##### ChatMakeSystemMessage

Display a formatted message in the chat. Using this method requires the
experience's [TextChatService.ChatVersion](/docs/reference/engine/classes/TextChatService#ChatVersion) to be set to
[LegacyChatService](/docs/reference/engine/enums/ChatVersion), although legacy chat is
deprecated and usage is discouraged. For experiences using the current
[TextChatService](/docs/reference/engine/classes/TextChatService), refer to
[TextChannel:DisplaySystemMessage()](/docs/reference/engine/classes/TextChannel#DisplaySystemMessage).

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| configTable | dictionary | (required) | A dictionary of information describing the message (see below). |

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| Text | string | (required) | The message to display. |
| Color | [Color3](/docs/reference/engine/datatypes/Color3) | [Color3.fromRGB(255, 255, 243)](/docs/reference/engine/datatypes/Color3#fromRGB) | Text color of the message. |
| Font | [Enum.Font](/docs/reference/engine/enums/Font) | SourceSansBold | Font of the message. |
| TextSize | integer | 18 | Text size of the message. |

##### SendNotification

Causes a non-intrusive notification to appear at the bottom right of the
screen. The notification may have up to two buttons.

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| configTable | dictionary | (required) | A dictionary of information describing the notification (see below). |

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| Title | string | (required) | The title of the notification. |
| Text | string | (required) | The main text of the notification. |
| Icon | string |  | The image to display with the notification. |
| Duration | number | 5 | Duration (in seconds) the notification should stay visible. |
| Callback | [BindableFunction](/docs/reference/engine/classes/BindableFunction) |  | A [BindableFunction](/docs/reference/engine/classes/BindableFunction) that should be invoked with the text of the button pressed by the player. |
| Button1 | string |  | The text to display on the first button. |
| Button2 | string |  | The text to display on the second button. |

##### TopbarEnabled

Determines whether the topbar is displayed. Disabling the topbar will also
disable all [CoreGuis](/docs/reference/engine/classes/CoreGui) such as the chat, inventory, and
player list (for example, those set with
[SetCoreGuiEnabled](/docs/reference/engine/classes/StarterGui#SetCoreGuiEnabled)).

When disabled, the region the topbar once occupied will still capture
mouse events; however, buttons placed there will not respond to clicks.
The origin of GUI space will still be offset 36 pixels from the top of the
screen.

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| enabled | boolean | (required) | Determines whether the topbar should be visible. |

##### DevConsoleVisible

Determines whether the
[Developer Console](/docs/studio/developer-console) is visible.

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| visibility | boolean | (required) | Determines whether the console is visible. |

##### PromptSendFriendRequest

Prompts the current player to send a connection request to the given
[Player](/docs/reference/engine/classes/Player).

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| player | [Player](/docs/reference/engine/classes/Player) | (required) | The player to which the connection request should be sent. |

##### PromptUnfriend

Prompts the current player to remove a given [Player](/docs/reference/engine/classes/Player) from their
connections list.

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| player | [Player](/docs/reference/engine/classes/Player) | (required) | The player who should be unconnected. |

##### PromptBlockPlayer

Prompts the current player to block the given [Player](/docs/reference/engine/classes/Player).

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| player | [Player](/docs/reference/engine/classes/Player) | (required) | The player who should be blocked. |

##### PromptUnblockPlayer

Prompts the current player to unblock the given [Player](/docs/reference/engine/classes/Player).

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| player | [Player](/docs/reference/engine/classes/Player) | (required) | The player who should be unblocked. |

##### AvatarContextMenuEnabled

Determines whether the
[Avatar Context Menu](/docs/players/avatar-context-menu) is enabled.

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| enabled | boolean | (required) | Determines whether the context menu is enabled. |

##### AvatarContextMenuTarget

Forcibly opens the
[Avatar Context Menu](/docs/players/avatar-context-menu).

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| player | [Player](/docs/reference/engine/classes/Player) | (required) | The player on whom the context menu will be opened. |

##### AddAvatarContextMenuOption

Adds an option to the
[Avatar Context Menu](/docs/players/avatar-context-menu).

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| option | [Enum.AvatarContextMenuOption](/docs/reference/engine/enums/AvatarContextMenuOption) | (required) | Option to add. |
| **OR** | | | |
| option | table | (required) | A two-element table, where the first is the name of the custom action, and the second is a [BindableEvent](/docs/reference/engine/classes/BindableEvent) which will be fired with a player was selected when the option was activated. |

##### RemoveAvatarContextMenuOption

Removes an option to the
[Avatar Context Menu](/docs/players/avatar-context-menu). The
option argument must be the same as what was used with
"AddAvatarContextMenuOption" (see above).

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| option | Variant | (required) | The same value provided to **AddAvatarContextMenuOption**. |

##### AvatarContextMenuTheme

Configures the customizable
[Avatar Context Menu](/docs/players/avatar-context-menu) which is an
opt-in feature that allows easy player-to-player social interaction via
custom actions, such as initiating trades, battles, and more. For more
info on how to customize its theme, see the
[Avatar Context Menu](/docs/players/avatar-context-menu) article.

##### CoreGuiChatConnections

Sets up a bindable gateway connection between the [CoreGui](/docs/reference/engine/classes/CoreGui) topbar's
chat button and the legacy chat system. The second parameter must be a
table of [BindableEvents](/docs/reference/engine/classes/BindableEvent) and
[BindableFunctions](/docs/reference/engine/classes/BindableFunction).

Code Samples

StarterGui Setting Core GUI

```
local StarterGui = game:GetService("StarterGui")



StarterGui:SetCore("AvatarContextMenuTheme", {



BackgroundImage = "",



BackgroundTransparency = 0.5,



BackgroundColor = Color3.fromRGB(111, 145, 242),



NameTagColor = Color3.fromRGB(0, 0, 200),



NameUnderlineColor = Color3.fromRGB(213, 233, 255),



ButtonFrameColor = Color3.fromRGB(15, 24, 65),



ButtonFrameTransparency = 0.2,



ButtonUnderlineColor = Color3.fromRGB(213, 233, 255),



Font = Enum.Font.SciFi,



})
```

Provide feedback

---

SetCoreGuiEnabled

Sets whether the [CoreGui](/docs/reference/engine/classes/CoreGui) element associated with the given
[Enum.CoreGuiType](/docs/reference/engine/enums/CoreGuiType) is enabled or disabled.

StarterGui:SetCoreGuiEnabled(

coreGuiType:[Enum.CoreGuiType](/docs/reference/engine/enums/CoreGuiType), enabled:[boolean](/docs/luau/booleans)

):()

Parameters

|  |
| --- |
| coreGuiType:[Enum.CoreGuiType](/docs/reference/engine/enums/CoreGuiType)  The given [Enum.CoreGuiType](/docs/reference/engine/enums/CoreGuiType). |
| enabled:[boolean](/docs/luau/booleans)  Whether to enable or disable the given [Enum.CoreGuiType](/docs/reference/engine/enums/CoreGuiType). |

Returns

()

This function sets whether the [CoreGui](/docs/reference/engine/classes/CoreGui) element associated with the
given [Enum.CoreGuiType](/docs/reference/engine/enums/CoreGuiType) is enabled or disabled.

The top bar cannot be disabled using this function. To disable it, set
"TopbarEnabled" to false using [StarterGui:SetCore()](/docs/reference/engine/classes/StarterGui#SetCore).

Provide feedback

---