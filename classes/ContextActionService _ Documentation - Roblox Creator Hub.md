# ContextActionService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ContextActionService
Scraped: 2026-01-11T02:32:03.711761Z

## Tags
- Not Creatable
- Service

## Inherits
- Instance
- ContextActionService
- Object
- BindAction
- UnbindAction
- LocalScripts
- Tool
- seated
- RemoteFunction:InvokeServer()
- UserInputService.InputBegan
- ImageButton
- TextButton
- UnbindAction()
- Sound
- played
- BindAction()
- InputObject
- BindActionAtPriority
- TouchEnabled
- ScreenGui
- PlayerGui
- Frame
- ImageButtons
- GetButton()
- ContextActionService:BindActionAtPriority()
- Tool.Activation
- ClickDetector
- Tools
- GuiButtons
- Mouse.Button1Down
- Tool.Equipped
- Tool.Activated
- Tool.ManualActivationOnly
- GetBoundActionInfo
- GetAllBoundActionInfo
- priority
- SetDescription
- SetTitle
- SetImage
- bound
- BackpackItem.TextureId
- equipped
- Player
- Character
- SetPosition
- SetImage()
- SetTitle()
- SetDescription()
- SetPosition()
- ImageButton.ImageColor3
- ImageLabel.Image
- ImageLabel
- GetButton
- GuiObject.Position
- TextLabel.Text
- TextLabel
- unequipping
- ContextActionService:BindActivate()
- HopperBin
- BindActivate
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ContextActionService](/docs/reference/engine/classes/ContextActionService)

English

Feedback

Engine Class

ContextActionService

A service used to bind user input to contextual actions.

Not Creatable

Service

---

Summary

Methods

|  |
| --- |
| [BindAction](#BindAction)(actionName: [string](/docs/luau/strings),functionToBind: [function](/docs/luau/functions),createTouchButton: [boolean](/docs/luau/booleans),inputTypes: [Tuple](/docs/luau/tuples)):() |
| [BindActionAtPriority](#BindActionAtPriority)(actionName: [string](/docs/luau/strings),functionToBind: [function](/docs/luau/functions),createTouchButton: [boolean](/docs/luau/booleans),priorityLevel: [number](/docs/luau/numbers),inputTypes: [Tuple](/docs/luau/tuples)):() |
| [BindActionToInputTypes](#BindActionToInputTypes)(actionName: [string](/docs/luau/strings),functionToBind: [function](/docs/luau/functions),createTouchButton: [boolean](/docs/luau/booleans),inputTypes: [Tuple](/docs/luau/tuples)):()  Deprecated |
| [BindActivate](#BindActivate)(userInputTypeForActivation: [Enum.UserInputType](/docs/reference/engine/enums/UserInputType),keyCodesForActivation: [Tuple](/docs/luau/tuples)):() |
| [GetAllBoundActionInfo](#GetAllBoundActionInfo)():[Dictionary](/docs/luau/tables#dictionaries) |
| [GetBoundActionInfo](#GetBoundActionInfo)(actionName: [string](/docs/luau/strings)):[Dictionary](/docs/luau/tables#dictionaries) |
| [GetButton](#GetButton)(actionName: [string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [GetCurrentLocalToolIcon](#GetCurrentLocalToolIcon)():[string](/docs/luau/strings) |
| [SetDescription](#SetDescription)(actionName: [string](/docs/luau/strings),description: [string](/docs/luau/strings)):() |
| [SetImage](#SetImage)(actionName: [string](/docs/luau/strings),image: [string](/docs/luau/strings)):() |
| [SetPosition](#SetPosition)(actionName: [string](/docs/luau/strings),position: [UDim2](/docs/reference/engine/datatypes/UDim2)):() |
| [SetTitle](#SetTitle)(actionName: [string](/docs/luau/strings),title: [string](/docs/luau/strings)):() |
| [UnbindAction](#UnbindAction)(actionName: [string](/docs/luau/strings)):() |
| [UnbindActivate](#UnbindActivate)(userInputTypeForActivation: [Enum.UserInputType](/docs/reference/engine/enums/UserInputType),keyCodeForActivation: [Enum.KeyCode](/docs/reference/engine/enums/KeyCode)):() |
| [UnbindAllActions](#UnbindAllActions)():() |

Events

|  |
| --- |
| [LocalToolEquipped](#LocalToolEquipped)(toolEquipped: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [LocalToolUnequipped](#LocalToolUnequipped)(toolUnequipped: [Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Allows an experience to bind user input to contextual actions, or actions that
are only enabled under some condition or period of time. For example, allowing
a player to open a door only while close by. In code, an action is simply a
string (the name of the action) used by the service to differentiate between
unique actions. The action string is provided to
[BindAction](/docs/reference/engine/classes/ContextActionService#BindAction) and
[UnbindAction](/docs/reference/engine/classes/ContextActionService#UnbindAction), among other member
functions. If two actions are bound to the same input, the most recently bound
will take priority. When the most recent action is unbound, the one bound
before that takes control again. Since this service deals with user input, you
can only use it in client-side [LocalScripts](/docs/reference/engine/classes/LocalScript).

#### Context and Action

A context is simply a condition during which a player may perform some
action. Some examples include holding a [Tool](/docs/reference/engine/classes/Tool), being
[seated](/docs/reference/engine/classes/Seat) in a car or standing near a door. Whatever the case may
be, it is up to your [LocalScripts](/docs/reference/engine/classes/LocalScript) to call
[BindAction](/docs/reference/engine/classes/ContextActionService#BindAction) when the context is
entered and [UnbindAction](/docs/reference/engine/classes/ContextActionService#UnbindAction) when the
context is left.

An action is simply some input that can be performed by the player while
in that context. Such an action could open/close some menu, trigger a
secondary tool action or send a request to the server using
[RemoteFunction:InvokeServer()](/docs/reference/engine/classes/RemoteFunction#InvokeServer). An action is identified by a unique
string as the first parameter of both
[BindAction](/docs/reference/engine/classes/ContextActionService#BindAction) and
[UnbindAction](/docs/reference/engine/classes/ContextActionService#UnbindAction). The string can be
anything, but it should reflect the action being performed, not the input
being used. For example, don't use "KeyH" as an action name - use "CarHorn"
instead. It is best to define your actions as a constant at the top of your
script since you will use it in at least three different places in your code.

#### Binding Actions Contextually

It's better to use ContextActionService's
[BindAction](/docs/reference/engine/classes/ContextActionService#BindAction) than
[UserInputService.InputBegan](/docs/reference/engine/classes/UserInputService#InputBegan) for most cases. For
[UserInputService.InputBegan](/docs/reference/engine/classes/UserInputService#InputBegan), your connected function would have to
check if the player is in the context of the action being performed. In most
cases, this is harder than just calling a function when a context is entered/
left. For example, if you want to have the H key trigger a car horn sound
while the player is sitting in it, the player might type "hello" in chat or
otherwise use the H key for something else. It is harder to determine if
something else is using the H key (like chat) - the car might honk when the
player didn't mean to. If you instead use
[BindAction](/docs/reference/engine/classes/ContextActionService#BindAction) and
[UnbindAction](/docs/reference/engine/classes/ContextActionService#UnbindAction) when the player
enters/leaves the car, [ContextActionService](/docs/reference/engine/classes/ContextActionService) will make sure that H
key presses trigger the honk action only when it is the most recently bound
action. If something else (like chat) takes control, you won't have to worry
about checking that.

#### Inspecting Bound Actions

To see a list of actions and their bound inputs, you can inspect the "Action
Bindings" tab in the Developer Console (F9 while in game). This shows all
bindings, including those bound by Roblox core scripts and default
camera/control scripts too. This is useful for debugging if your actions are
being bound/unbound at the correct times, or if some other action is stealing
input from your actions. For example, if you are attempting to bind
WASD, it may be the case that
default character movement scripts are binding over those same keys.
Similarly, the camera control script can steal right-click input if the script
runs after yours.

#### Keyboardless Input

This service is especially useful for supporting gamepad and touch input. For
gamepad input, you might choose to bind the B button to an action that returns
the user to the previous menu when they enter another menu. For touch,
on-screen touch buttons can be used in place of key presses: these buttons
display only while the action is bound, and the position, text and/or images
of these buttons can be configured through this service. They're somewhat
limited in the amount of customization provided by this service; it's usually
a better idea to make your own on-screen buttons using [ImageButton](/docs/reference/engine/classes/ImageButton) or
[TextButton](/docs/reference/engine/classes/TextButton).

Code Samples

ContextActionService Tool Reload

This example properly shows how to use ContextActionService in binding user
input to a contextual action. The context is the tool being equipped; the
action is reloading some weapon. Test this code sample by placing it in a
LocalScript parented to a Tool. When the Tool is equipped, a "Reload" action
is bound, and when the Tool is unequipped the "Reload" action is unbound. When
the player presses R with the Tool equipped, the message "Reloading!" will
appear.

```
local ContextActionService = game:GetService("ContextActionService")



local ACTION_RELOAD = "Reload"



local tool = script.Parent



local function handleAction(actionName, inputState, _inputObject)



if actionName == ACTION_RELOAD and inputState == Enum.UserInputState.Begin then



print("Reloading!")



end



end



tool.Equipped:Connect(function()



ContextActionService:BindAction(ACTION_RELOAD, handleAction, true, Enum.KeyCode.R)



end)



tool.Unequipped:Connect(function()



ContextActionService:UnbindAction(ACTION_RELOAD)



end)
```

---

API Reference

Methods

BindAction

Bind user input to an action given an action handling function.

ContextActionService:BindAction(

actionName:[string](/docs/luau/strings), functionToBind:[function](/docs/luau/functions), createTouchButton:[boolean](/docs/luau/booleans), inputTypes:[Tuple](/docs/luau/tuples)

):()

Parameters

|  |
| --- |
| actionName:[string](/docs/luau/strings)  A string representing the action being performed (e.g. "HonkHorn" or "OpenDoor"). |
| functionToBind:[function](/docs/luau/functions)  The action-handling function, called with the following parameters when the bound inputs are triggered: string (actionName), [Enum.UserInputState](/docs/reference/engine/enums/UserInputState) and an InputObject. |
| createTouchButton:[boolean](/docs/luau/booleans)  Whether a GUI button should be created for the action on touch input devices. |
| inputTypes:[Tuple](/docs/luau/tuples)  Any number of [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) or [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) representing the inputs to bind to the action. |

Returns

()

Bind an action to user input given an action handling function. Upon a
matching input being performed, the action handler function will be called
with the arguments listed below. Valid input enum items include those
within the following: [Enum.KeyCode](/docs/reference/engine/enums/KeyCode), [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) or
[Enum.PlayerActions](/docs/reference/engine/enums/PlayerActions) . Call this function when a player enters the
context in which an action can be performed. When the player leaves the
context, call [UnbindAction()](/docs/reference/engine/classes/ContextActionService#UnbindAction)
with the same actionName.

The code sample below shows how a [Sound](/docs/reference/engine/classes/Sound) can be
[played](/docs/reference/engine/classes/Sound#Play) while a key (H), game pad button,
or touch screen button is pressed.

```
local ContextActionService = game:GetService("ContextActionService")



-- A car horn sound



local honkSound = Instance.new("Sound", workspace)



honkSound.Looped = true



honkSound.SoundId = "rbxassetid://9120386436"



local function handleAction(actionName, inputState, inputObject)



if actionName == "HonkHorn" then



if inputState == Enum.UserInputState.Begin then



honkSound:Play()



else



honkSound:Pause()



end



end



end



-- When the player sits in the vehicle:



ContextActionService:BindAction("HonkHorn", handleAction, true, Enum.KeyCode.H, Enum.KeyCode.ButtonY)



-- When the player gets out:



ContextActionService:UnbindAction("HonkHorn")
```

#### Action Handler Parameters

The action handler functions are called with the following parameters:

|  |  |  |
| --- | --- | --- |
| # | Type | Description |
| 1 | string | The same string that was originally passed to [BindAction()](/docs/reference/engine/classes/ContextActionService#BindAction). This allows one function to handle multiple actions at once, if necessary. |
| 2 | [Enum.UserInputState](/docs/reference/engine/enums/UserInputState) | The state of the input. [Cancel](/docs/reference/engine/enums/UserInputState) is sent if some input was in progress and another action bound over that in-progress input, or if the in-progress bound action was unbound through [UnbindAction()](/docs/reference/engine/classes/ContextActionService#UnbindAction). |
| 3 | InputObject | An object that contains information about the input (varies based on [Enum.UserInputType](/docs/reference/engine/enums/UserInputType)). The [InputObject](/docs/reference/engine/classes/InputObject) sometimes won't match the inputs the action was bound to: when the [Cancel](/docs/reference/engine/enums/UserInputState) state is sent, this object will be [Enum.KeyCode.Unknown](/docs/reference/engine/enums/KeyCode#Unknown) and [Enum.UserInputType.None](/docs/reference/engine/enums/UserInputType#None). |

#### Action Bindings Stack

Action bindings behave like a stack: if two actions are bound to the same
user input, the most recently bound action handler will be used. If an
action handler returns [Enum.ContextActionResult.Pass](/docs/reference/engine/enums/ContextActionResult#Pass), the next most
recently bound action handler will be called, and so on until a handler
sinks the input (by returning nil or [Enum.ContextActionResult.Sink](/docs/reference/engine/enums/ContextActionResult#Sink)).
When [UnbindAction](/docs/reference/engine/classes/ContextActionService#UnbindAction) is called,
the action handler is removed from the stack. This stack behavior can be
overridden using
[BindActionAtPriority](/docs/reference/engine/classes/ContextActionService#BindActionAtPriority),
where an additional priority parameter after createTouchButton may
override the order in which actions are bound (higher before lower).

#### Touch Buttons

In addition to input types, this function's third parameter controls
whether a button is created for
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) devices. Upon the first
touch button's creation, a [ScreenGui](/docs/reference/engine/classes/ScreenGui) named "ContextActionGui" is
added to the [PlayerGui](/docs/reference/engine/classes/PlayerGui). Inside the ScreenGui is a [Frame](/docs/reference/engine/classes/Frame)
called "ContextButtonFrame" is added. It is in this frame in which
[ImageButtons](/docs/reference/engine/classes/ImageButton) for bound actions are parented; you can
use [GetButton()](/docs/reference/engine/classes/ContextActionService#GetButton) to retrieve such
buttons for customization. A maximum of 7 touch buttons can be created
through [BindAction()](/docs/reference/engine/classes/ContextActionService#BindAction).

Code Samples

ContextActionService Tool Reload

This example properly shows how to use ContextActionService in binding user
input to a contextual action. The context is the tool being equipped; the
action is reloading some weapon. Test this code sample by placing it in a
LocalScript parented to a Tool. When the Tool is equipped, a "Reload" action
is bound, and when the Tool is unequipped the "Reload" action is unbound. When
the player presses R with the Tool equipped, the message "Reloading!" will
appear.

```
local ContextActionService = game:GetService("ContextActionService")



local ACTION_RELOAD = "Reload"



local tool = script.Parent



local function handleAction(actionName, inputState, _inputObject)



if actionName == ACTION_RELOAD and inputState == Enum.UserInputState.Begin then



print("Reloading!")



end



end



tool.Equipped:Connect(function()



ContextActionService:BindAction(ACTION_RELOAD, handleAction, true, Enum.KeyCode.R)



end)



tool.Unequipped:Connect(function()



ContextActionService:UnbindAction(ACTION_RELOAD)



end)
```

General Action Handler

This code sample uses ContextActionService to bind an action named
"BoundAction" to a general action handler function on the F key. Place this
in a LocalScript inside StarterPlayerScripts and press F to see the message
"Handling action: BoundAction".

```
local ContextActionService = game:GetService("ContextActionService")



local function handleAction(actionName, inputState, inputObj)



if inputState == Enum.UserInputState.Begin then



print("Handling action: " .. actionName)



print(inputObj.UserInputType)



end



-- Since this function does not return anything, this handler will



-- "sink" the input and no other action handlers will be called after



-- this one.



end



ContextActionService:BindAction("BoundAction", handleAction, false, Enum.KeyCode.F)
```

Stacked Action Handlers

This code sample demonstrates how BindAction acts like a stack. It binds two
actions, FirstAction (Z, X, and C keys) and SecondAction (Z and X
keys) to two action handling functions. The second one will pass on a certain
input (the X key).

Both actions use the Z and X keys, however the second handler will pass
input only if X is pressed. So, when X is pressed, the second handler is
called and then the first. The first action is also bound to the C key, and
can be triggered even though the other two inputs are "covered" by the second
action.

Test this code out by pasting it into a LocalScript within
StarterPlayerScripts, then pressing Z, X and C. Observe which action
handlers are called with what actions.

```
local ContextActionService = game:GetService("ContextActionService")



-- Define an action handler for FirstAction



local function actionHandlerOne(actionName, inputState, _inputObj)



if inputState == Enum.UserInputState.Begin then



print("Action Handler One: " .. actionName)



end



-- This action handler returns nil, so it is assumed that



-- it properly handles the action.



end



-- Binding the action FirstAction (it's on the bottom of the stack)



ContextActionService:BindAction("FirstAction", actionHandlerOne, false, Enum.KeyCode.Z, Enum.KeyCode.X, Enum.KeyCode.C)



-- Define an action handler for SecondAction



local function actionHandlerTwo(actionName, inputState, inputObj)



if inputState == Enum.UserInputState.Begin then



print("Action Handler Two: " .. actionName)



end



if inputObj.KeyCode == Enum.KeyCode.X then



return Enum.ContextActionResult.Pass



else



-- Returning nil implicitly Sinks inputs



return Enum.ContextActionResult.Sink



end



end



-- Binding SecondAction over the first action (since it bound more recently, it is on the top of the stack)



-- Note that SecondAction uses the same keys as



ContextActionService:BindAction("SecondAction", actionHandlerTwo, false, Enum.KeyCode.Z, Enum.KeyCode.X)
```

Provide feedback

---

BindActionAtPriority

Behaves like [BindAction](/docs/reference/engine/classes/ContextActionService#BindAction) but also
allows a priority to be assigned to the bound action for overlapping input
types (higher before lower).

ContextActionService:BindActionAtPriority(

actionName:[string](/docs/luau/strings), functionToBind:[function](/docs/luau/functions), createTouchButton:[boolean](/docs/luau/booleans), priorityLevel:[number](/docs/luau/numbers), inputTypes:[Tuple](/docs/luau/tuples)

):()

Parameters

|  |
| --- |
| actionName:[string](/docs/luau/strings)  A string representing the action being performed (e.g. "HonkHorn" or "OpenDoor"). |
| functionToBind:[function](/docs/luau/functions)  The action-handling function, called with the following parameters when the bound inputs are triggered: string (actionName), [Enum.UserInputState](/docs/reference/engine/enums/UserInputState) and an InputObject. |
| createTouchButton:[boolean](/docs/luau/booleans)  Whether a GUI button should be created for the action on touch input devices. |
| priorityLevel:[number](/docs/luau/numbers)  The priority level at which the action should be bound (higher considered before lower). |
| inputTypes:[Tuple](/docs/luau/tuples)  Any number of Enum.KeyCode or Enum.UserInputType representing the inputs to bind to the action. |

Returns

()

BindActionAtPriority behaves like
[BindAction](/docs/reference/engine/classes/ContextActionService#BindAction) but also allows a
priority to be assigned to the bound action. If multiple actions are bound
to the same input, the higher priority function is called regardless of
the order in which the actions were bound. In other words, this function
overrides the normal "stack" behavior of BindAction.

Code Samples

ContextActionService BindAction Priorities

This code sample demonstrates how
[ContextActionService:BindActionAtPriority()](/docs/reference/engine/classes/ContextActionService#BindActionAtPriority) can be used to bind
actions out of order yet still have the same priority levels. Normally,
[BindAction()](/docs/reference/engine/classes/ContextActionService#BindAction) would operate on order
(last bound action has highest priority), but priority levels override this.
You can test this code by pasting it into a Script with RunContext = Client in ReplicatedStorage.

```
local ContextActionService = game:GetService("ContextActionService")



local INPUT_KEY1 = Enum.KeyCode.Q



local INPUT_KEY2 = Enum.KeyCode.E



local function handleThrow(actionName: string, inputState: Enum.UserInputState, inputObject: InputObject)



if inputState ~= Enum.UserInputState.Begin then



return Enum.ContextActionResult.Pass



end



print(`Action [{actionName}] occurred. KeyCode [{inputObject.KeyCode}] pressed.`)



return Enum.ContextActionResult.Sink



end



local function handlePunch(actionName: string, inputState: Enum.UserInputState, inputObject: InputObject)



if inputState ~= Enum.UserInputState.Begin then



return Enum.ContextActionResult.Pass



end



print(`Action [{actionName}] occurred. KeyCode [{inputObject.KeyCode}] pressed.`)



return Enum.ContextActionResult.Sink



end



-- Without specifying priority, the most recently bound action is called first,



-- so pressing INPUT_KEY1 prints "Punch" and then sinks the input.



ContextActionService:BindAction("DefaultThrow", handleThrow, false, INPUT_KEY1)



ContextActionService:BindAction("DefaultPunch", handlePunch, false, INPUT_KEY1)



-- Here we bind both functions in the same order as above, but with explicitly swapped priorities.



-- That is, we give "Throw" a higher priority of 2 so it will be called first,



-- despite "Punch" still being bound more recently.



-- Pressing INPUT_KEY2 prints "Throw" and then sinks the input.



ContextActionService:BindActionAtPriority("PriorityThrow", handleThrow, false, 2, INPUT_KEY2)



ContextActionService:BindActionAtPriority("PriorityPunch", handlePunch, false, 1, INPUT_KEY2)
```

Provide feedback

---

BindActionToInputTypes

Deprecated

Show details

---

BindActivate

Bind a [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) with a specific [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) to trigger
[Tool.Activation](/docs/reference/engine/classes/Tool#Activation) and [ClickDetector](/docs/reference/engine/classes/ClickDetector) events.

ContextActionService:BindActivate(

userInputTypeForActivation:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType), keyCodesForActivation:[Tuple](/docs/luau/tuples)

):()

Parameters

|  |
| --- |
| userInputTypeForActivation:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)  Must be Keyboard or Gamepad1 through Gamepad8. |
| keyCodesForActivation:[Tuple](/docs/luau/tuples) |

Returns

()

Bind a [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) that can be used with a [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) to
activate [ClickDetector](/docs/reference/engine/classes/ClickDetector) events, [Tools](/docs/reference/engine/classes/Tool), and
[GuiButtons](/docs/reference/engine/classes/GuiButton). When the given key/button is pressed, it
fires the [Mouse.Button1Down](/docs/reference/engine/classes/Mouse#Button1Down) event on the mouse sent to
[Tool.Equipped](/docs/reference/engine/classes/Tool#Equipped). This in turn fires the [Tool.Activated](/docs/reference/engine/classes/Tool#Activated) event
if [Tool.ManualActivationOnly](/docs/reference/engine/classes/Tool#ManualActivationOnly) is not set to true. For gamepad
input, this function is called by the default control scripts in order to
bind the ButtonR2 [Enum.KeyCode](/docs/reference/engine/enums/KeyCode).

Note that the [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) specified must be Keyboard or
Gamepad1 through Gamepad8 in order to be valid.

Provide feedback

---

GetAllBoundActionInfo

Get a table of information about all bound actions (key is the name passed
to [BindAction](/docs/reference/engine/classes/ContextActionService#BindAction), value is a table
from [GetBoundActionInfo](/docs/reference/engine/classes/ContextActionService#GetBoundActionInfo)
when called with the key).

ContextActionService:GetAllBoundActionInfo():[Dictionary](/docs/luau/tables#dictionaries)

Returns

[Dictionary](/docs/luau/tables#dictionaries)

GetAllBoundActioninfo returns a table which maps all actions' names (those
originally passed to [BindAction](/docs/reference/engine/classes/ContextActionService#BindAction))
to a table returned by
[GetBoundActionInfo](/docs/reference/engine/classes/ContextActionService#GetBoundActionInfo) when
called with the action name itself. Using this function, you can inspect
all presently bound actions. This is useful when debugging their priority
levels or stack orders.

Provide feedback

---

GetBoundActionInfo

Get a table of information about a bound action given its name originally
passed to [BindAction](/docs/reference/engine/classes/ContextActionService#BindAction).

ContextActionService:GetBoundActionInfo(actionName:[string](/docs/luau/strings)):[Dictionary](/docs/luau/tables#dictionaries)

Parameters

|  |
| --- |
| actionName:[string](/docs/luau/strings) |

Returns

[Dictionary](/docs/luau/tables#dictionaries)

GetBoundActionInfo returns a table with the following keys describing a
bound action given its name. To get the same information for all actions
at once, use
[GetAllBoundActionInfo](/docs/reference/engine/classes/ContextActionService#GetAllBoundActionInfo).

|  |  |  |
| --- | --- | --- |
| Name | Type | Description |
| stackOrder | number | Describes the index of the action on the stack (increasing) |
| priorityLevel\* | number | Describes the [priority](/docs/reference/engine/classes/ContextActionService#BindActionAtPriority) level of the action |
| createTouchButton | bool | Describes whether a touch button should be created on [TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) devices |
| inputTypes | table | The input types passed to [BindAction](/docs/reference/engine/classes/ContextActionService#BindAction) for which this action will trigger |
| description† | string | The description of action set by [SetDescription](/docs/reference/engine/classes/ContextActionService#SetDescription) |
| title† | string | The title of the action set by [SetTitle](/docs/reference/engine/classes/ContextActionService#SetTitle) |
| image† | string | The image of the action's touch button set by [SetImage](/docs/reference/engine/classes/ContextActionService#SetImage) |

\* Priority level will still be included even if
[BindActionAtPriority](/docs/reference/engine/classes/ContextActionService#BindActionAtPriority)
wasn't used - by default it will be 2000.

† Indicates that this field will be nil if the associated method was not
called for the given action.

Provide feedback

---

GetButton

Yields

Retrieves a [ImageButton](/docs/reference/engine/classes/ImageButton) of a
[bound](/docs/reference/engine/classes/ContextActionService#BindAction) action that had a touch
input button created.

ContextActionService:GetButton(actionName:[string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| actionName:[string](/docs/luau/strings)  The name of the action originally passed to BindAction. |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

An ImageButton created by BindAction.

GetButton returns the [ImageButton](/docs/reference/engine/classes/ImageButton) created by
[BindAction](/docs/reference/engine/classes/ContextActionService#BindAction) if its third
parameter was true and the device is
[TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled). The only parameter to
this function must match exactly the name of the action originally sent to
BindAction.

If no such action was bound or if a button was not created, this function
returns nil.

Provide feedback

---

GetCurrentLocalToolIcon

Return the [BackpackItem.TextureId](/docs/reference/engine/classes/BackpackItem#TextureId) of a [Tool](/docs/reference/engine/classes/Tool) currently
[equipped](/docs/reference/engine/classes/Tool#Equipped) by the [Player](/docs/reference/engine/classes/Player).

ContextActionService:GetCurrentLocalToolIcon():[string](/docs/luau/strings)

Returns

[string](/docs/luau/strings)

A content string from the Tool's TextureId, or nil if one could not
be found.

GetCurrentLocalToolIcon will return the [BackpackItem.TextureId](/docs/reference/engine/classes/BackpackItem#TextureId) of
a [Tool](/docs/reference/engine/classes/Tool) currently [equipped](/docs/reference/engine/classes/Tool#Equipped) by the
[Player](/docs/reference/engine/classes/Player), or nil if there is no such Tool or if the player lacks a
[Character](/docs/reference/engine/classes/Player#Character).

Provide feedback

---

SetDescription

Given the name of a bound action with a touch button, sets the description
of the action.

ContextActionService:SetDescription(

actionName:[string](/docs/luau/strings), description:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| actionName:[string](/docs/luau/strings)  The name of the action originally passed to BindAction. |
| description:[string](/docs/luau/strings)  A text description of the action, such as "Honk the car's horn" or "Open the inventory". |

Returns

()

SetDescription will set the description of an action bound by
[BindAction](/docs/reference/engine/classes/ContextActionService#BindAction). In a list of
available actions, this would be text that describes the given action.

Although the name may suggest that this method is related to the family of
functions that customize a touch button for actions that create them
([SetTitle](/docs/reference/engine/classes/ContextActionService#SetTitle),
[SetImage](/docs/reference/engine/classes/ContextActionService#SetImage) and
[SetPosition](/docs/reference/engine/classes/ContextActionService#SetPosition)), this method does
not affect such a button. This method merely sets a text description of an
action, and nothing more.

Code Samples

ContextActionService Touch Button

This code sample demonstrates binding an "Inspect" action to a touch button
created automatically by ContextActionService. The button is customized
using [SetImage()](/docs/reference/engine/classes/ContextActionService#SetImage),
[SetTitle()](/docs/reference/engine/classes/ContextActionService#SetTitle),
[SetDescription()](/docs/reference/engine/classes/ContextActionService#SetDescription) and
[SetPosition()](/docs/reference/engine/classes/ContextActionService#SetPosition). The button is
further customized by using
[GetButton()](/docs/reference/engine/classes/ContextActionService#GetButton) to get a reference to the
ImageButton itself and tinting it green by setting
[ImageButton.ImageColor3](/docs/reference/engine/classes/ImageButton#ImageColor3).

Paste this code into a LocalScript placed within StarterPlayerScripts to
test it. In Studio, be sure to toggle the touch device emulator in order for
the button to actually be created.

```
local ContextActionService = game:GetService("ContextActionService")



local ACTION_INSPECT = "Inspect"



local INPUT_INSPECT = Enum.KeyCode.E



local IMAGE_INSPECT = "rbxassetid://1826746856" -- Image of a speech bubble with ? in it



local function handleAction(actionName, inputState, _inputObject)



if actionName == ACTION_INSPECT and inputState == Enum.UserInputState.End then



print("Inspecting")



end



end



-- For touch devices, a button is created on-screen automatically via the 3rd parameter



ContextActionService:BindAction(ACTION_INSPECT, handleAction, true, INPUT_INSPECT)



-- We can use these functions to customize the button:



ContextActionService:SetImage(ACTION_INSPECT, IMAGE_INSPECT)



ContextActionService:SetTitle(ACTION_INSPECT, "Look")



ContextActionService:SetDescription(ACTION_INSPECT, "Inspect something.")



ContextActionService:SetPosition(ACTION_INSPECT, UDim2.new(0, 0, 0, 0))



-- We can manipulate the button directly using ContextActionService:GetButton



local imgButton = ContextActionService:GetButton(ACTION_INSPECT)



if imgButton then -- Remember: non-touch devices won't return anything!



imgButton.ImageColor3 = Color3.new(0.5, 1, 0.5) -- Tint the ImageButton green



end
```

Provide feedback

---

SetImage

If actionName key contains a bound action, then image is set as the
image of the touch button.

ContextActionService:SetImage(

actionName:[string](/docs/luau/strings), image:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| actionName:[string](/docs/luau/strings)  The name of the action originally passed to BindAction. |
| image:[string](/docs/luau/strings)  The value to which the Image property should be set. |

Returns

()

This method sets the image shown on a touch button created by
[BindAction()](/docs/reference/engine/classes/ContextActionService#BindAction). Specifically, it
sets the [ImageLabel.Image](/docs/reference/engine/classes/ImageLabel#Image) property of the [ImageLabel](/docs/reference/engine/classes/ImageLabel)
within the [ImageButton](/docs/reference/engine/classes/ImageButton) that would be returned by
[GetButton](/docs/reference/engine/classes/ContextActionService#GetButton). If no such bound
action exists (e.g. nothing is returned by GetButton), this function does
nothing and throws no error.

This function is part of a family of methods that customize the touch
button of an action. Others in this family include
[SetPosition](/docs/reference/engine/classes/ContextActionService#SetPosition) and
[SetTitle](/docs/reference/engine/classes/ContextActionService#SetTitle).

Code Samples

ContextActionService Touch Button

This code sample demonstrates binding an "Inspect" action to a touch button
created automatically by ContextActionService. The button is customized
using [SetImage()](/docs/reference/engine/classes/ContextActionService#SetImage),
[SetTitle()](/docs/reference/engine/classes/ContextActionService#SetTitle),
[SetDescription()](/docs/reference/engine/classes/ContextActionService#SetDescription) and
[SetPosition()](/docs/reference/engine/classes/ContextActionService#SetPosition). The button is
further customized by using
[GetButton()](/docs/reference/engine/classes/ContextActionService#GetButton) to get a reference to the
ImageButton itself and tinting it green by setting
[ImageButton.ImageColor3](/docs/reference/engine/classes/ImageButton#ImageColor3).

Paste this code into a LocalScript placed within StarterPlayerScripts to
test it. In Studio, be sure to toggle the touch device emulator in order for
the button to actually be created.

```
local ContextActionService = game:GetService("ContextActionService")



local ACTION_INSPECT = "Inspect"



local INPUT_INSPECT = Enum.KeyCode.E



local IMAGE_INSPECT = "rbxassetid://1826746856" -- Image of a speech bubble with ? in it



local function handleAction(actionName, inputState, _inputObject)



if actionName == ACTION_INSPECT and inputState == Enum.UserInputState.End then



print("Inspecting")



end



end



-- For touch devices, a button is created on-screen automatically via the 3rd parameter



ContextActionService:BindAction(ACTION_INSPECT, handleAction, true, INPUT_INSPECT)



-- We can use these functions to customize the button:



ContextActionService:SetImage(ACTION_INSPECT, IMAGE_INSPECT)



ContextActionService:SetTitle(ACTION_INSPECT, "Look")



ContextActionService:SetDescription(ACTION_INSPECT, "Inspect something.")



ContextActionService:SetPosition(ACTION_INSPECT, UDim2.new(0, 0, 0, 0))



-- We can manipulate the button directly using ContextActionService:GetButton



local imgButton = ContextActionService:GetButton(ACTION_INSPECT)



if imgButton then -- Remember: non-touch devices won't return anything!



imgButton.ImageColor3 = Color3.new(0.5, 1, 0.5) -- Tint the ImageButton green



end
```

Provide feedback

---

SetPosition

Given the name of a bound action with a touch button, sets the position of
the button within the ContextButtonFrame.

ContextActionService:SetPosition(

actionName:[string](/docs/luau/strings), position:[UDim2](/docs/reference/engine/datatypes/UDim2)

):()

Parameters

|  |
| --- |
| actionName:[string](/docs/luau/strings)  The name of the action originally passed to BindAction. |
| position:[UDim2](/docs/reference/engine/datatypes/UDim2)  The position within the ContextButtonFrame. |

Returns

()

This method sets the position of a touch button created by
[BindAction()](/docs/reference/engine/classes/ContextActionService#BindAction). Specifically, it
sets the [GuiObject.Position](/docs/reference/engine/classes/GuiObject#Position) property of the [ImageButton](/docs/reference/engine/classes/ImageButton)
that would be returned by
[GetButton](/docs/reference/engine/classes/ContextActionService#GetButton). If no such bound
action exists (e.g. nothing is returned by GetButton), this function does
nothing and throws no error.

This function is part of a family of methods that customize the touch
button of an action. Others in this family include
[SetImage](/docs/reference/engine/classes/ContextActionService#SetImage) and
[SetTitle](/docs/reference/engine/classes/ContextActionService#SetTitle).

Code Samples

ContextActionService Touch Button

This code sample demonstrates binding an "Inspect" action to a touch button
created automatically by ContextActionService. The button is customized
using [SetImage()](/docs/reference/engine/classes/ContextActionService#SetImage),
[SetTitle()](/docs/reference/engine/classes/ContextActionService#SetTitle),
[SetDescription()](/docs/reference/engine/classes/ContextActionService#SetDescription) and
[SetPosition()](/docs/reference/engine/classes/ContextActionService#SetPosition). The button is
further customized by using
[GetButton()](/docs/reference/engine/classes/ContextActionService#GetButton) to get a reference to the
ImageButton itself and tinting it green by setting
[ImageButton.ImageColor3](/docs/reference/engine/classes/ImageButton#ImageColor3).

Paste this code into a LocalScript placed within StarterPlayerScripts to
test it. In Studio, be sure to toggle the touch device emulator in order for
the button to actually be created.

```
local ContextActionService = game:GetService("ContextActionService")



local ACTION_INSPECT = "Inspect"



local INPUT_INSPECT = Enum.KeyCode.E



local IMAGE_INSPECT = "rbxassetid://1826746856" -- Image of a speech bubble with ? in it



local function handleAction(actionName, inputState, _inputObject)



if actionName == ACTION_INSPECT and inputState == Enum.UserInputState.End then



print("Inspecting")



end



end



-- For touch devices, a button is created on-screen automatically via the 3rd parameter



ContextActionService:BindAction(ACTION_INSPECT, handleAction, true, INPUT_INSPECT)



-- We can use these functions to customize the button:



ContextActionService:SetImage(ACTION_INSPECT, IMAGE_INSPECT)



ContextActionService:SetTitle(ACTION_INSPECT, "Look")



ContextActionService:SetDescription(ACTION_INSPECT, "Inspect something.")



ContextActionService:SetPosition(ACTION_INSPECT, UDim2.new(0, 0, 0, 0))



-- We can manipulate the button directly using ContextActionService:GetButton



local imgButton = ContextActionService:GetButton(ACTION_INSPECT)



if imgButton then -- Remember: non-touch devices won't return anything!



imgButton.ImageColor3 = Color3.new(0.5, 1, 0.5) -- Tint the ImageButton green



end
```

Provide feedback

---

SetTitle

Given the name of a bound action with a touch button, sets the text shown
on the button.

ContextActionService:SetTitle(

actionName:[string](/docs/luau/strings), title:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| actionName:[string](/docs/luau/strings)  The name of the action originally passed to BindAction. |
| title:[string](/docs/luau/strings)  The text to display on the button. |

Returns

()

SetTitle will set the text shown on a touch button created by
[BindAction](/docs/reference/engine/classes/ContextActionService#BindAction). Specifically, this
sets the [TextLabel.Text](/docs/reference/engine/classes/TextLabel#Text) property of a [TextLabel](/docs/reference/engine/classes/TextLabel) within the
[ImageButton](/docs/reference/engine/classes/ImageButton) that would be returned by
[GetButton](/docs/reference/engine/classes/ContextActionService#GetButton). If no such bound
action exists (e.g. nothing is returned by GetButton), this function does
nothing and throws no error.

This function is part of a family of methods that customize the touch
button of an action. Others in this family include
[SetImage](/docs/reference/engine/classes/ContextActionService#SetImage) and
[SetPosition](/docs/reference/engine/classes/ContextActionService#SetPosition).

Code Samples

ContextActionService Touch Button

This code sample demonstrates binding an "Inspect" action to a touch button
created automatically by ContextActionService. The button is customized
using [SetImage()](/docs/reference/engine/classes/ContextActionService#SetImage),
[SetTitle()](/docs/reference/engine/classes/ContextActionService#SetTitle),
[SetDescription()](/docs/reference/engine/classes/ContextActionService#SetDescription) and
[SetPosition()](/docs/reference/engine/classes/ContextActionService#SetPosition). The button is
further customized by using
[GetButton()](/docs/reference/engine/classes/ContextActionService#GetButton) to get a reference to the
ImageButton itself and tinting it green by setting
[ImageButton.ImageColor3](/docs/reference/engine/classes/ImageButton#ImageColor3).

Paste this code into a LocalScript placed within StarterPlayerScripts to
test it. In Studio, be sure to toggle the touch device emulator in order for
the button to actually be created.

```
local ContextActionService = game:GetService("ContextActionService")



local ACTION_INSPECT = "Inspect"



local INPUT_INSPECT = Enum.KeyCode.E



local IMAGE_INSPECT = "rbxassetid://1826746856" -- Image of a speech bubble with ? in it



local function handleAction(actionName, inputState, _inputObject)



if actionName == ACTION_INSPECT and inputState == Enum.UserInputState.End then



print("Inspecting")



end



end



-- For touch devices, a button is created on-screen automatically via the 3rd parameter



ContextActionService:BindAction(ACTION_INSPECT, handleAction, true, INPUT_INSPECT)



-- We can use these functions to customize the button:



ContextActionService:SetImage(ACTION_INSPECT, IMAGE_INSPECT)



ContextActionService:SetTitle(ACTION_INSPECT, "Look")



ContextActionService:SetDescription(ACTION_INSPECT, "Inspect something.")



ContextActionService:SetPosition(ACTION_INSPECT, UDim2.new(0, 0, 0, 0))



-- We can manipulate the button directly using ContextActionService:GetButton



local imgButton = ContextActionService:GetButton(ACTION_INSPECT)



if imgButton then -- Remember: non-touch devices won't return anything!



imgButton.ImageColor3 = Color3.new(0.5, 1, 0.5) -- Tint the ImageButton green



end
```

Provide feedback

---

UnbindAction

Unbind an action from input given its name.

ContextActionService:UnbindAction(actionName:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| actionName:[string](/docs/luau/strings) |

Returns

()

UnbindAction will unbind an action by name from user inputs so that the
action handler function will no longer be called. Call this function when
the context for some action is no longer applicable, such as closing a
user interface, exiting a car or [unequipping](/docs/reference/engine/classes/Tool#Unequipped) a
[Tool](/docs/reference/engine/classes/Tool). See [BindAction](/docs/reference/engine/classes/ContextActionService#BindAction) for
more information on how bound actions operate.

This function will not throw an error if there is no such action bound
with the given string. Using
[GetAllBoundActionInfo](/docs/reference/engine/classes/ContextActionService#GetAllBoundActionInfo)
or the Developer Console's "Action Bindings" tab, you can find out what
actions are presently bound.

Code Samples

ContextActionService Tool Reload

This example properly shows how to use ContextActionService in binding user
input to a contextual action. The context is the tool being equipped; the
action is reloading some weapon. Test this code sample by placing it in a
LocalScript parented to a Tool. When the Tool is equipped, a "Reload" action
is bound, and when the Tool is unequipped the "Reload" action is unbound. When
the player presses R with the Tool equipped, the message "Reloading!" will
appear.

```
local ContextActionService = game:GetService("ContextActionService")



local ACTION_RELOAD = "Reload"



local tool = script.Parent



local function handleAction(actionName, inputState, _inputObject)



if actionName == ACTION_RELOAD and inputState == Enum.UserInputState.Begin then



print("Reloading!")



end



end



tool.Equipped:Connect(function()



ContextActionService:BindAction(ACTION_RELOAD, handleAction, true, Enum.KeyCode.R)



end)



tool.Unequipped:Connect(function()



ContextActionService:UnbindAction(ACTION_RELOAD)



end)
```

Provide feedback

---

UnbindActivate

Unbind a [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) with a specific [Enum.UserInputType](/docs/reference/engine/enums/UserInputType) from
triggering [Tool.Activation](/docs/reference/engine/classes/Tool#Activation) when bound with
[ContextActionService:BindActivate()](/docs/reference/engine/classes/ContextActionService#BindActivate).

ContextActionService:UnbindActivate(

userInputTypeForActivation:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType), keyCodeForActivation:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)

):()

Parameters

|  |
| --- |
| userInputTypeForActivation:[Enum.UserInputType](/docs/reference/engine/enums/UserInputType)  The same UserInputType originally sent to BindActivate. |
| keyCodeForActivation:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode) Default Value: "Unknown" The same KeyCode originally sent to BindActivate. |

Returns

()

UnbindActivate unbinds an [Enum.KeyCode](/docs/reference/engine/enums/KeyCode) used with an [Enum.UserInputType](/docs/reference/engine/enums/UserInputType)
for activating a [Tool](/docs/reference/engine/classes/Tool) (or a [HopperBin](/docs/reference/engine/classes/HopperBin)) using
[BindActivate](/docs/reference/engine/classes/ContextActionService#BindActivate). This function
essentially undoes the action performed by that function.

Provide feedback

---

UnbindAllActions

Removes all functions bound. No actionNames will remain. All touch buttons
will be removed.

ContextActionService:UnbindAllActions():()

Returns

()

Removes all functions bound. No actionNames will remain. All touch buttons
will be removed. If a button was manipulated manually there is no
guarantee it will be cleaned up.

Provide feedback

---

Events

LocalToolEquipped

Fires when the current player equips a [Tool](/docs/reference/engine/classes/Tool).

ContextActionService.LocalToolEquipped(toolEquipped:[Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| toolEquipped:[Instance](/docs/reference/engine/datatypes/Instance) |

Fires when the current player equips a [Tool](/docs/reference/engine/classes/Tool).

Provide feedback

---

LocalToolUnequipped

Fires when the current player unequips a [Tool](/docs/reference/engine/classes/Tool).

ContextActionService.LocalToolUnequipped(toolUnequipped:[Instance](/docs/reference/engine/datatypes/Instance)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| toolUnequipped:[Instance](/docs/reference/engine/datatypes/Instance) |

Fires when the current player unequips a [Tool](/docs/reference/engine/classes/Tool).

Provide feedback

---