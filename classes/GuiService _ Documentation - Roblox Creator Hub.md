# GuiService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/GuiService
Scraped: 2026-01-11T02:28:58.328430Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Object
- Instance
- GuiService
- GuiObjects
- GuiObject
- GuiNavigationEnabled
- SelectedObject
- CoreGui
- Object.GetPropertyChangedSignal()
- UITextSizeConstraint
- MinTextSize
- MaxTextSize
- TextScaled
- TextLabel
- TextButton
- PreferredTextSize
- AutomaticSize
- TextWrapped
- TextService:GetTextSize()
- TextService:GetTextBoundsAsync()
- GuiService.PreferredTextSize
- BackgroundTransparency
- PreferredTransparency
- GuiService.PreferredTransparency
- CollectionService
- SelectionGained
- SelectionLost
- Changed
- Health
- StarterGui:SetCoreGuiEnabled()
- Object:GetPropertyChangedSignal()
- ScreenGui
- Frame
- GetPropertyChangedSignal()
- GuiService.ViewportDisplaySize
- LocalScript
- InspectPlayerFromHumanoidDescription()
- HumanoidDescription
- InspectPlayerFromUserId()
- UserId
- SetEmotesMenuOpen()
- Player.GameplayPaused
- SetGameplayPausedNotificationEnabled()
- Workspace.StreamingIntegrityMode
- ScreenGuis
- IgnoreGuiInset
- SetInspectMenuEnabled()
- GuiService.SelectedObject
- PlayerGui
- SelectionOrder
- GetGameplayPausedNotificationEnabled()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [GuiService](/docs/reference/engine/classes/GuiService)

English

Feedback

Engine Class

GuiService

Offers numerous properties and methods for working with
[GuiObjects](/docs/reference/engine/classes/GuiObject), player preferences, and other UI‑related tasks.

Not Creatable

Service

Not Replicated

---

Summary

Properties

|  |
| --- |
| [AutoSelectGuiEnabled](#AutoSelectGuiEnabled):[boolean](/docs/luau/booleans) |
| [CoreGuiNavigationEnabled](#CoreGuiNavigationEnabled):[boolean](/docs/luau/booleans) |
| [GuiNavigationEnabled](#GuiNavigationEnabled):[boolean](/docs/luau/booleans) |
| [IsModalDialog](#IsModalDialog):[boolean](/docs/luau/booleans)  Deprecated |
| [IsWindows](#IsWindows):[boolean](/docs/luau/booleans)  Deprecated |
| [MenuIsOpen](#MenuIsOpen):[boolean](/docs/luau/booleans) |
| [PreferredTextSize](#PreferredTextSize):[Enum.PreferredTextSize](/docs/reference/engine/enums/PreferredTextSize) |
| [PreferredTransparency](#PreferredTransparency):[number](/docs/luau/numbers) |
| [ReducedMotionEnabled](#ReducedMotionEnabled):[boolean](/docs/luau/booleans) |
| [SelectedObject](#SelectedObject):[GuiObject](/docs/reference/engine/classes/GuiObject) |
| [TopbarInset](#TopbarInset):[Rect](/docs/reference/engine/datatypes/Rect) |
| [TouchControlsEnabled](#TouchControlsEnabled):[boolean](/docs/luau/booleans) |
| [ViewportDisplaySize](#ViewportDisplaySize):[Enum.DisplaySize](/docs/reference/engine/enums/DisplaySize) |

Methods

|  |
| --- |
| [AddSelectionParent](#AddSelectionParent)(selectionName: [string](/docs/luau/strings),selectionParent: [Instance](/docs/reference/engine/datatypes/Instance)):()  Deprecated |
| [AddSelectionTuple](#AddSelectionTuple)(selectionName: [string](/docs/luau/strings),selections: [Tuple](/docs/luau/tuples)):()  Deprecated |
| [CloseInspectMenu](#CloseInspectMenu)():() |
| [DismissNotification](#DismissNotification)(notificationId: [string](/docs/luau/strings)):[boolean](/docs/luau/booleans) |
| [GetEmotesMenuOpen](#GetEmotesMenuOpen)():[boolean](/docs/luau/booleans) |
| [GetGameplayPausedNotificationEnabled](#GetGameplayPausedNotificationEnabled)():[boolean](/docs/luau/booleans) |
| [GetGuiInset](#GetGuiInset)():[Tuple](/docs/luau/tuples) |
| [GetInspectMenuEnabled](#GetInspectMenuEnabled)():[boolean](/docs/luau/booleans) |
| [InspectPlayerFromHumanoidDescription](#InspectPlayerFromHumanoidDescription)(humanoidDescription: [Instance](/docs/reference/engine/datatypes/Instance),name: [string](/docs/luau/strings)):() |
| [InspectPlayerFromUserId](#InspectPlayerFromUserId)(userId: [number](/docs/luau/numbers)):() |
| [IsTenFootInterface](#IsTenFootInterface)():[boolean](/docs/luau/booleans) |
| [RemoveSelectionGroup](#RemoveSelectionGroup)(selectionName: [string](/docs/luau/strings)):()  Deprecated |
| [Select](#Select)(selectionParent: [Instance](/docs/reference/engine/datatypes/Instance)):() |
| [SendNotification](#SendNotification)(notificationInfo: [Dictionary](/docs/luau/tables#dictionaries)):[string](/docs/luau/strings) |
| [SetEmotesMenuOpen](#SetEmotesMenuOpen)(isOpen: [boolean](/docs/luau/booleans)):() |
| [SetGameplayPausedNotificationEnabled](#SetGameplayPausedNotificationEnabled)(enabled: [boolean](/docs/luau/booleans)):() |
| [SetInspectMenuEnabled](#SetInspectMenuEnabled)(enabled: [boolean](/docs/luau/booleans)):() |

Events

|  |
| --- |
| [MenuClosed](#MenuClosed)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MenuOpened](#MenuOpened)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

GuiService offers numerous properties and methods for working with
[GuiObjects](/docs/reference/engine/classes/GuiObject), player preferences, and other UI‑related tasks.

---

API Reference

Properties

AutoSelectGuiEnabled

Read Parallel

If activated, the Select button on a gamepad or
Backslash will automatically set a GUI as the selected object.

GuiService.AutoSelectGuiEnabled:[boolean](/docs/luau/booleans)

If activated, the Select button on a gamepad or
Backslash will automatically set a GUI as the selected object.
Disabling this means that GUI navigation will still work if
[GuiNavigationEnabled](/docs/reference/engine/classes/GuiService#GuiNavigationEnabled) is enabled,
but you will have to set [SelectedObject](/docs/reference/engine/classes/GuiService#SelectedObject)
manually to start navigation.

Provide feedback

---

CoreGuiNavigationEnabled

Hidden

Not Replicated

Read Parallel

Toggles whether or not objects in the [CoreGui](/docs/reference/engine/classes/CoreGui) can be navigated
using a gamepad.

GuiService.CoreGuiNavigationEnabled:[boolean](/docs/luau/booleans)

Toggles whether or not objects in the [CoreGui](/docs/reference/engine/classes/CoreGui) can be navigated
using a gamepad.

Provide feedback

---

GuiNavigationEnabled

Read Parallel

Used to enable and disable the default controller GUI navigation.

GuiService.GuiNavigationEnabled:[boolean](/docs/luau/booleans)

Used to enable and disable the default controller GUI navigation.

Provide feedback

---

IsModalDialog

Deprecated

Show details

---

IsWindows

Deprecated

Show details

---

MenuIsOpen

Read Only

Not Replicated

Read Parallel

Returns true if any menu of [CoreGui](/docs/reference/engine/classes/CoreGui) is open.

GuiService.MenuIsOpen:[boolean](/docs/luau/booleans)

Returns true if any menu of [CoreGui](/docs/reference/engine/classes/CoreGui) is open.

Provide feedback

---

PreferredTextSize

Read Only

Not Replicated

Read Parallel

Gets the player's preferred text size as an [Enum.PreferredTextSize](/docs/reference/engine/enums/PreferredTextSize)
value.

GuiService.PreferredTextSize:[Enum.PreferredTextSize](/docs/reference/engine/enums/PreferredTextSize)

Gets the player's preferred text size as an [Enum.PreferredTextSize](/docs/reference/engine/enums/PreferredTextSize) value
of [Medium](/docs/reference/engine/enums/PreferredTextSize#Medium) (default),
[Large](/docs/reference/engine/enums/PreferredTextSize#Large),
[Larger](/docs/reference/engine/enums/PreferredTextSize#Larger), or
[Largest](/docs/reference/engine/enums/PreferredTextSize#Largest). This property maps to the
Text Size setting available to players from the Roblox and
in‑game Settings menus, and it can be combined with
[Object.GetPropertyChangedSignal()](/docs/reference/engine/classes/Object#GetPropertyChangedSignal) to detect text size setting
changes for purposes of adjusting UI.

When working with UI elements, note the following behaviors:

* Text that is constrained to a minimum and/or maximum size through a
  [UITextSizeConstraint](/docs/reference/engine/classes/UITextSizeConstraint) will not shrink below or expand above
  the set
  [MinTextSize](/docs/reference/engine/classes/UITextSizeConstraint#MinTextSize)/[MaxTextSize](/docs/reference/engine/classes/UITextSizeConstraint#MaxTextSize),
  regardless of the player's text size setting.
* When [TextScaled](/docs/reference/engine/classes/TextLabel#TextScaled) is enabled for a
  [TextLabel](/docs/reference/engine/classes/TextLabel#TextScaled) or
  [TextButton](/docs/reference/engine/classes/TextButton#TextScaled), the element's text will
  not be scaled by the
  [PreferredTextSize](/docs/reference/engine/classes/GuiService#PreferredTextSize) value.
* UI elements with [AutomaticSize](/docs/reference/engine/classes/GuiObject#AutomaticSize) enabled
  will shrink/grow as
  [PreferredTextSize](/docs/reference/engine/classes/GuiService#PreferredTextSize)
  decreases/increases (element bounds will resize to fit the resized
  text).
* When [TextWrapped](/docs/reference/engine/classes/TextLabel#TextWrapped) is enabled for a
  [TextLabel](/docs/reference/engine/classes/TextLabel#TextWrapped) or
  [TextButton](/docs/reference/engine/classes/TextButton#TextWrapped), the element's text will wrap
  to additional lines as
  [PreferredTextSize](/docs/reference/engine/classes/GuiService#PreferredTextSize) increases, within
  limits of the element's absolute size.
* The results returned by [TextService:GetTextSize()](/docs/reference/engine/classes/TextService#GetTextSize) and
  [TextService:GetTextBoundsAsync()](/docs/reference/engine/classes/TextService#GetTextBoundsAsync) honor changes related to
  [PreferredTextSize](/docs/reference/engine/classes/GuiService#PreferredTextSize).

Code Samples

Detect/Apply Changes to Preferred Text Size

Listens for changes to [GuiService.PreferredTextSize](/docs/reference/engine/classes/GuiService#PreferredTextSize) to appropriately update a UI element's size.

```
local GuiService = game:GetService("GuiService")



local TextService = game:GetService("TextService")



local FONT_SIZE = 25



local PADDING = 8



local textLabel = Instance.new("TextLabel")



textLabel.Position = UDim2.new(0.5, 0, 0.5, 0)



textLabel.AnchorPoint = Vector2.new(0.5, 0.5)



textLabel.AutomaticSize = Enum.AutomaticSize.X



textLabel.TextSize = FONT_SIZE + PADDING



textLabel.Text = "Text Label Test"



textLabel.Parent = script.Parent



local function applyAddedTextHeight()



local finalTextHeight = TextService:GetTextSize("", FONT_SIZE, Enum.Font.BuilderSans, Vector2.new(math.huge, math.huge)).Y



local addedTextHeight = finalTextHeight - FONT_SIZE



print("PreferredTextSize adds", addedTextHeight, " to default text size")



textLabel.Size = UDim2.new(0, 0, 0, FONT_SIZE + addedTextHeight + PADDING)



end



applyAddedTextHeight()



GuiService:GetPropertyChangedSignal("PreferredTextSize"):Connect(applyAddedTextHeight)
```

Provide feedback

---

PreferredTransparency

Hidden

Read Only

Not Replicated

Read Parallel

Gets the player's preferred transparency as a number between 0 and 1.

GuiService.PreferredTransparency:[number](/docs/luau/numbers)

Gets the player's preferred transparency as a number between 0 and 1.
This property maps to the Background Transparency setting
available to players from the Roblox and in‑experience Settings menus,
and it can be combined with [Object.GetPropertyChangedSignal()](/docs/reference/engine/classes/Object#GetPropertyChangedSignal) to
detect transparency setting changes for purposes of adjusting UI.

A value of 1 (default) indicates the player prefers the default
background transparency, while a value of 0 indicates the player prefers
fully opaque (non‑transparent) background transparency for improved
readability and contrast. Multiplying a UI element's
[BackgroundTransparency](/docs/reference/engine/classes/GuiObject#BackgroundTransparency) with
[PreferredTransparency](/docs/reference/engine/classes/GuiService#PreferredTransparency) is the
recommended approach, such that backgrounds become more opaque as
[PreferredTransparency](/docs/reference/engine/classes/GuiService#PreferredTransparency) approaches
0.

Code Samples

Detect/Apply Changes to Preferred Transparency

Listens for changes to [GuiService.PreferredTransparency](/docs/reference/engine/classes/GuiService#PreferredTransparency) to adjust the background opacity of UI objects tagged with TransparentBack through [CollectionService](/docs/reference/engine/classes/CollectionService).

```
local GuiService = game:GetService("GuiService")



local CollectionService = game:GetService("CollectionService")



local TAG = "TransparentBack"



local transparentBackObjects = {}



local function onInstanceAdded(object)



if object.BackgroundTransparency then



local defaultTransparency = object.BackgroundTransparency



transparentBackObjects[object] = defaultTransparency



object.BackgroundTransparency = defaultTransparency * GuiService.PreferredTransparency



end



end



local function onInstanceRemoved(object)



transparentBackObjects[object] = nil



end



-- Store initial tagged instances



for _, object in CollectionService:GetTagged(TAG) do



onInstanceAdded(object)



end



-- Detect when tagged instance is added or removed



CollectionService:GetInstanceAddedSignal(TAG):Connect(onInstanceAdded)



CollectionService:GetInstanceRemovedSignal(TAG):Connect(onInstanceRemoved)



-- When in-game setting is changed, adjust tagged instances



GuiService:GetPropertyChangedSignal("PreferredTransparency"):Connect(function()



for object, defaultTransparency in transparentBackObjects do



object.BackgroundTransparency = defaultTransparency * GuiService.PreferredTransparency



end



end)
```

Provide feedback

---

ReducedMotionEnabled

Hidden

Read Only

Not Replicated

Read Parallel

Returns true if the player has enabled reduced motion.

GuiService.ReducedMotionEnabled:[boolean](/docs/luau/booleans)

Returns true if the player has enabled reduced motion, indicating that
they want motion effects and animations to be reduced or completely
removed. This property maps to the Reduce Motion toggle available
from the Roblox and in‑experience Settings menus. See
[accessibility guidelines](/docs/production/publishing/accessibility#reduced-motion)
for usage recommendations.

Provide feedback

---

SelectedObject

Read Parallel

Sets the [GuiObject](/docs/reference/engine/classes/GuiObject) currently being focused on by the GUI
navigator.

GuiService.SelectedObject:[GuiObject](/docs/reference/engine/classes/GuiObject)

Sets the [GuiObject](/docs/reference/engine/classes/GuiObject) currently being focused on by the GUI
navigator. This may reset to nil if the object is off screen.

This property is changed by the
[SelectionGained](/docs/reference/engine/classes/GuiObject#SelectionGained) and
[SelectionLost](/docs/reference/engine/classes/GuiObject#SelectionLost) events. If you would like to
determine when this property changes without tracking these events for all
GUI elements, you can use the [Changed](/docs/reference/engine/classes/Object#Changed) event.

Provide feedback

---

TopbarInset

Read Only

Not Replicated

Read Parallel

Used to determine the absolute size and position of unobstructed area
within top bar space.

GuiService.TopbarInset:[Rect](/docs/reference/engine/datatypes/Rect)

Returns a [Rect](/docs/reference/engine/datatypes/Rect) object representing the unoccupied area between
the Roblox left-most controls and the edge of the device safe area.

The value is dynamic and can be expected to change based on the visibility
of UI controls such as changing the local player's
[Health](/docs/reference/engine/classes/Humanoid#Health) property, usage of
[StarterGui:SetCoreGuiEnabled()](/docs/reference/engine/classes/StarterGui#SetCoreGuiEnabled), changing the size and position of
Roblox UI Controls, and/or others. For this reason, it's recommend that
you detect and react to changes of this property with
[Object:GetPropertyChangedSignal()](/docs/reference/engine/classes/Object#GetPropertyChangedSignal).

Code Samples

Responsive Frame Within Available Top Bar Space

This code snippet creates a new [ScreenGui](/docs/reference/engine/classes/ScreenGui) with a [Frame](/docs/reference/engine/classes/Frame) that automatically adapts its size and position to a top bar space unoccupied by Roblox UI.

```
local GuiService = game:GetService("GuiService")



local Players = game:GetService("Players")



local screenGui = Instance.new("ScreenGui")



screenGui.IgnoreGuiInset = true



screenGui.Parent = Players.LocalPlayer.PlayerGui



local frame = Instance.new("Frame")



frame.BackgroundColor3 = Color3.fromRGB(0, 255, 0)



frame.Parent = screenGui



GuiService:GetPropertyChangedSignal("TopbarInset"):Connect(function()



local inset = GuiService.TopbarInset



frame.Size = UDim2.new(0, inset.Width, 0, inset.Height)



frame.Position = UDim2.new(0, inset.Min.X, 0, inset.Min.Y)



end)
```

Provide feedback

---

TouchControlsEnabled

Read Parallel

Used to enable and disable touch controls and touch control display UI.
Defaults to true.

GuiService.TouchControlsEnabled:[boolean](/docs/luau/booleans)

Used to enable and disable touch controls and touch control display UI.
Defaults to true.

Provide feedback

---

ViewportDisplaySize

Read Only

Not Replicated

Read Parallel

Read-only property which represents the physical rendering size of the
viewport.

GuiService.ViewportDisplaySize:[Enum.DisplaySize](/docs/reference/engine/enums/DisplaySize)

Read-only property which represents the physical rendering size of the
viewport. You can listen for changes to this property through the
[GetPropertyChangedSignal()](/docs/reference/engine/classes/Object#GetPropertyChangedSignal)
method to adapt UI to various display sizes.

Code Samples

ViewportDisplaySize Changes

This code snippet listens to [GuiService.ViewportDisplaySize](/docs/reference/engine/classes/GuiService#ViewportDisplaySize) property change signals to adapt UI to various display sizes.

```
local GuiService = game:GetService("GuiService")



local function updateUI()



if (GuiService.ViewportDisplaySize == Enum.DisplaySize.Small) then



-- Update UI to small screen



elseif (GuiService.ViewportDisplaySize == Enum.DisplaySize.Large) then



-- Update UI to large screen



else



-- Update UI to medium/default screen



end



end



GuiService:GetPropertyChangedSignal("ViewportDisplaySize"):Connect(updateUI)



updateUI()
```

Provide feedback

---

Methods

AddSelectionParent

Deprecated

Show details

---

AddSelectionTuple

Deprecated

Show details

---

CloseInspectMenu

Closes the avatar inspection menu, if open.

GuiService:CloseInspectMenu():()

Returns

()

This method closes the
[Avatar Inspect Menu](/docs/players/avatar-inspect-menu), if open,
when run from a [LocalScript](/docs/reference/engine/classes/LocalScript).

#### See Also

* [InspectPlayerFromHumanoidDescription()](/docs/reference/engine/classes/GuiService#InspectPlayerFromHumanoidDescription)
  which allows the avatar inspection menu to appear showing the assets
  listed in a [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) object.
* [InspectPlayerFromUserId()](/docs/reference/engine/classes/GuiService#InspectPlayerFromUserId)
  which allows the avatar inspection menu to appear showing the user that
  has the given [UserId](/docs/reference/engine/classes/Player#UserId).

Provide feedback

---

DismissNotification

GuiService:DismissNotification(notificationId:[string](/docs/luau/strings)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| notificationId:[string](/docs/luau/strings) |

Returns

[boolean](/docs/luau/booleans)

Provide feedback

---

GetEmotesMenuOpen

Checks if the player emotes menu is open.

GuiService:GetEmotesMenuOpen():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

Whether the emotes menu is open.

Returns a boolean indicating whether or not the player emotes menu is
open. You can open or close the emotes menu by calling the
[SetEmotesMenuOpen()](/docs/reference/engine/classes/GuiService#SetEmotesMenuOpen) method.

Provide feedback

---

GetGameplayPausedNotificationEnabled

Returns whether or not the [Player.GameplayPaused](/docs/reference/engine/classes/Player#GameplayPaused) notification has
been disabled.

GuiService:GetGameplayPausedNotificationEnabled():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

Whether or not the [Player.GameplayPaused](/docs/reference/engine/classes/Player#GameplayPaused) notification has been
disabled.

This method returns whether or not the [Player.GameplayPaused](/docs/reference/engine/classes/Player#GameplayPaused)
notification has been disabled through
[SetGameplayPausedNotificationEnabled()](/docs/reference/engine/classes/GuiService#SetGameplayPausedNotificationEnabled).

See also [Workspace.StreamingIntegrityMode](/docs/reference/engine/classes/Workspace#StreamingIntegrityMode) and
[Enum.StreamingIntegrityMode](/docs/reference/engine/enums/StreamingIntegrityMode) for more details on when gameplay is paused.

Provide feedback

---

GetGuiInset

Returns two [Vector2](/docs/reference/engine/datatypes/Vector2) values representing the inset of user GUIs
in pixels, from the top‑left corner of the screen and the bottom‑right
corner of the screen respectively.

GuiService:GetGuiInset():[Tuple](/docs/luau/tuples)

Returns

[Tuple](/docs/luau/tuples)

A tuple of two [Vector2](/docs/reference/engine/datatypes/Vector2) values describing the current
specified GUI inset.

Returns two [Vector2](/docs/reference/engine/datatypes/Vector2) values representing the inset of user GUIs
in pixels, from the top‑left corner of the screen and the bottom‑right
corner of the screen respectively.

The inset values supplied by this method only take effect on
[ScreenGuis](/docs/reference/engine/classes/ScreenGui) that have their
[IgnoreGuiInset](/docs/reference/engine/classes/ScreenGui#IgnoreGuiInset) property set to false.

Provide feedback

---

GetInspectMenuEnabled

Returns whether the avatar inspection menu is enabled.

GuiService:GetInspectMenuEnabled():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

Whether the avatar inspection menu is enabled.

This method returns whether the
[Avatar Inspect Menu](/docs/players/avatar-inspect-menu) is
currently enabled. The feature is enabled by default and can be disabled
using the
[SetInspectMenuEnabled()](/docs/reference/engine/classes/GuiService#SetInspectMenuEnabled) method.

Provide feedback

---

InspectPlayerFromHumanoidDescription

Allows the avatar inspection menu to appear showing the assets listed in a
[HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) object.

GuiService:InspectPlayerFromHumanoidDescription(

humanoidDescription:[Instance](/docs/reference/engine/datatypes/Instance), name:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| humanoidDescription:[Instance](/docs/reference/engine/datatypes/Instance)  A [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) object that contains the assets to show in the inspection menu. |
| name:[string](/docs/luau/strings)  The name of the player being inspected to show in the menu. |

Returns

()

This method allows the
[Avatar Inspect Menu](/docs/players/avatar-inspect-menu) to appear
showing the assets listed in a [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) object. This
allows further customization with what is shown in the inspection menu
when players inspect other players in your experience.

See also
[InspectPlayerFromUserId()](/docs/reference/engine/classes/GuiService#InspectPlayerFromUserId)
which allows the avatar inspection menu to appear showing the user that
has the given [UserId](/docs/reference/engine/classes/Player#UserId).

Provide feedback

---

InspectPlayerFromUserId

Allows the avatar inspection menu to appear showing the user that has the
given [UserId](/docs/reference/engine/classes/Player#UserId).

GuiService:InspectPlayerFromUserId(userId:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| userId:[number](/docs/luau/numbers)  The [UserId](/docs/reference/engine/classes/Player#UserId) of the player to inspect. |

Returns

()

This method allows the
[Avatar Inspect Menu](/docs/players/avatar-inspect-menu) to appear
showing the user that has the given [UserId](/docs/reference/engine/classes/Player#UserId). This is
especially useful when you want to inspect players who aren't in the
current experience.

See also
[InspectPlayerFromHumanoidDescription()](/docs/reference/engine/classes/GuiService#InspectPlayerFromHumanoidDescription)
which allows you to bring up the avatar inspection menu showing the assets
listed in a [HumanoidDescription](/docs/reference/engine/classes/HumanoidDescription) object.

Provide feedback

---

IsTenFootInterface

Returns true if the client is using the ten foot interface, a special
version of Roblox's UI exclusive to consoles.

GuiService:IsTenFootInterface():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

Returns true if the client is using the ten foot interface, a special
version of Roblox's UI exclusive to consoles. This is the only guaranteed
way to verify if the user is on a console or not.

Provide feedback

---

RemoveSelectionGroup

Deprecated

Show details

---

Select

Sets [GuiService.SelectedObject](/docs/reference/engine/classes/GuiService#SelectedObject) to a child of a provided instance
that is the [PlayerGui](/docs/reference/engine/classes/PlayerGui) or its descendants.

GuiService:Select(selectionParent:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| selectionParent:[Instance](/docs/reference/engine/datatypes/Instance)  The parent of selection whose descendants are searched. |

Returns

()

When called on an instance selectionParent that is the [PlayerGui](/docs/reference/engine/classes/PlayerGui)
or a descendant of it, the engine searches all available selectable,
visible and on-screen [GuiObjects](/docs/reference/engine/classes/GuiObject) that are descendants of
selectionParent and sets the
[SelectedObject](/docs/reference/engine/classes/GuiService#SelectedObject) to the [GuiObject](/docs/reference/engine/classes/GuiObject)
with the smallest [SelectionOrder](/docs/reference/engine/classes/GuiObject#SelectionOrder).

Provide feedback

---

SendNotification

GuiService:SendNotification(notificationInfo:[Dictionary](/docs/luau/tables#dictionaries)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| notificationInfo:[Dictionary](/docs/luau/tables#dictionaries) |

Returns

[string](/docs/luau/strings)

Provide feedback

---

SetEmotesMenuOpen

Opens or closes the player emotes menu.

GuiService:SetEmotesMenuOpen(isOpen:[boolean](/docs/luau/booleans)):()

Parameters

|  |
| --- |
| isOpen:[boolean](/docs/luau/booleans) |

Returns

()

Opens or closes the player emotes menu.

Provide feedback

---

SetGameplayPausedNotificationEnabled

Lets you disable the built-in notification when a player's gameplay is
paused.

GuiService:SetGameplayPausedNotificationEnabled(enabled:[boolean](/docs/luau/booleans)):()

Parameters

|  |
| --- |
| enabled:[boolean](/docs/luau/booleans)  Whether or not the built-in notification GUI is disabled. |

Returns

()

This method lets you disable the built-in notification when a player's
gameplay is paused. You can then add in your own UI and customize it.

You can query whether the notification is enabled by calling the
[GetGameplayPausedNotificationEnabled()](/docs/reference/engine/classes/GuiService#GetGameplayPausedNotificationEnabled)
method.

See also [Workspace.StreamingIntegrityMode](/docs/reference/engine/classes/Workspace#StreamingIntegrityMode) and
[Enum.StreamingIntegrityMode](/docs/reference/engine/enums/StreamingIntegrityMode) for more details on when gameplay is paused.

Provide feedback

---

SetInspectMenuEnabled

Allows you to enable or disable the avatar inspection menu.

GuiService:SetInspectMenuEnabled(enabled:[boolean](/docs/luau/booleans)):()

Parameters

|  |
| --- |
| enabled:[boolean](/docs/luau/booleans)  A boolean indicating whether to enable or disable the menu. |

Returns

()

This method allows you to enable or disable the
[Avatar Inspect Menu](/docs/players/avatar-inspect-menu). The
feature is enabled by default.

Provide feedback

---

Events

MenuClosed

Fires when the user closes the Roblox [CoreGui](/docs/reference/engine/classes/CoreGui) escape menu.

GuiService.MenuClosed():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Fires when the user closes the Roblox [CoreGui](/docs/reference/engine/classes/CoreGui) escape menu.

Provide feedback

---

MenuOpened

Fires when the user opens the Roblox [CoreGui](/docs/reference/engine/classes/CoreGui) escape menu.

GuiService.MenuOpened():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Fires when the user opens the Roblox [CoreGui](/docs/reference/engine/classes/CoreGui) escape menu.

Provide feedback

---