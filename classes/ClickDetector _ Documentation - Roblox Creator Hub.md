# ClickDetector | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ClickDetector
Scraped: 2026-01-11T02:32:57.802841Z

## Inherits
- Object
- Instance
- ClickDetector
- BaseParts
- Models
- Player
- DragDetector
- Scripts
- LocalScripts
- MouseClick
- BasePart
- Model
- Folder
- TouchEnabled
- ClickDetectors
- ContextActionService:BindActivate()
- MouseHoverEnter
- MouseHoverLeave
- MaxActivationDistance
- LocalScript
- Character
- StarterPlayerScripts
- ContextActionService
- UserInputService.InputBegan
- Script
- GamepadEnabled
- RightMouseClick
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ClickDetector](/docs/reference/engine/classes/ClickDetector)

English

Feedback

Engine Class

![ClickDetector](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/ClickDetector-Dark.webp)ClickDetector

An object that provides user input on in-experience [BaseParts](/docs/reference/engine/classes/BasePart)
and [Models](/docs/reference/engine/classes/Model).

---

Summary

Properties

|  |
| --- |
| [CursorIcon](#CursorIcon):ContentId |
| [CursorIconContent](#CursorIconContent):[Content](/docs/reference/engine/datatypes/Content) |
| [MaxActivationDistance](#MaxActivationDistance):[number](/docs/luau/numbers) |

Events

|  |
| --- |
| [MouseClick](#MouseClick)(playerWhoClicked: [Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [mouseClick](#mouseClick)(playerWhoClicked: [Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |
| [MouseHoverEnter](#MouseHoverEnter)(playerWhoHovered: [Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MouseHoverLeave](#MouseHoverLeave)(playerWhoHovered: [Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [RightMouseClick](#RightMouseClick)(playerWhoClicked: [Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[DragDetector](/docs/reference/engine/classes/DragDetector)

ClickDetector allows [Scripts](/docs/reference/engine/classes/Script) and
[LocalScripts](/docs/reference/engine/classes/LocalScript) to receive pointer input on 3D objects
through their [MouseClick](/docs/reference/engine/classes/ClickDetector#MouseClick) event. They work
when parented to [BasePart](/docs/reference/engine/classes/BasePart), [Model](/docs/reference/engine/classes/Model), or [Folder](/docs/reference/engine/classes/Folder) objects.
They detect basic mouse events: enter, leave, left click and right click.
Touch input on [TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) devices also
fires click events.

The default control scripts bind [ButtonR2](/docs/reference/engine/enums/KeyCode) to interact with
[ClickDetectors](/docs/reference/engine/classes/ClickDetector) using
[ContextActionService:BindActivate()](/docs/reference/engine/classes/ContextActionService#BindActivate), which can also be used to
override this. When using gamepads, the center dot triggers
[MouseHoverEnter](/docs/reference/engine/classes/ClickDetector#MouseHoverEnter) and
[MouseHoverLeave](/docs/reference/engine/classes/ClickDetector#MouseHoverLeave). The bound activation
button fires [MouseClick](/docs/reference/engine/classes/ClickDetector#MouseClick).

[MaxActivationDistance](/docs/reference/engine/classes/ClickDetector#MaxActivationDistance) can be used
to limit the distance a player may be from a click detector before it is no
longer clickable.

[ClickDetector](/docs/reference/engine/classes/ClickDetector) events fire on both the client and the server. Since a
[LocalScript](/docs/reference/engine/classes/LocalScript) will only run if it descends from a [Player](/docs/reference/engine/classes/Player) or
player [Character](/docs/reference/engine/classes/Player#Character), it's usually not useful to put a
[LocalScript](/docs/reference/engine/classes/LocalScript) inside a [ClickDetector](/docs/reference/engine/classes/ClickDetector), since the script won't run
or the object won't be clickable. If you need a [LocalScript](/docs/reference/engine/classes/LocalScript) to detect
[ClickDetector](/docs/reference/engine/classes/ClickDetector) events, [StarterPlayerScripts](/docs/reference/engine/classes/StarterPlayerScripts) may be a better
place instead.

#### Input Priority

If multiple [ClickDetectors](/docs/reference/engine/classes/ClickDetector) may detect user input, only
the deepest will fire events. If two [ClickDetectors](/docs/reference/engine/classes/ClickDetector) are
siblings, the first will take priority.

If an action bound with [ContextActionService](/docs/reference/engine/classes/ContextActionService) uses the same input as a
[ClickDetector](/docs/reference/engine/classes/ClickDetector), the action bound with [ContextActionService](/docs/reference/engine/classes/ContextActionService) will
take priority over the click detector's events.

[UserInputService.InputBegan](/docs/reference/engine/classes/UserInputService#InputBegan) will fire before [ClickDetector](/docs/reference/engine/classes/ClickDetector)
events.

Code Samples

ClickDetector Example

Place this code inside a [Script](/docs/reference/engine/classes/Script) inside a [ClickDetector](/docs/reference/engine/classes/ClickDetector). The
code sample creates a reference to the parent and defines a function to show a
message that greets a player. Finally, it connects the
[MouseClick](/docs/reference/engine/classes/ClickDetector#MouseClick) event to the defined function.

```
local clickDetector = script.Parent



local function onClicked(player)



-- Show a message to the player



local msg = Instance.new("Message")



msg.Parent = player:FindFirstChild("PlayerGui")



msg.Text = "Hello, " .. player.Name



wait(2.5)



msg:Destroy()



end



-- Connect the function to the MouseClick event



clickDetector.MouseClick:Connect(onClicked)
```

Part Anchored Toggle

This code sample will allow a part to be clicked to toggle its anchored property. When toggled, the visual appearance of the part is updated (red means anchored, yellow means free).

```
local part = script.Parent



-- Create a ClickDetector so we can tell when the part is clicked



local cd = Instance.new("ClickDetector", part)



-- This function updates how the part looks based on its Anchored state



local function updateVisuals()



if part.Anchored then



-- When the part is anchored...



part.BrickColor = BrickColor.new("Bright red")



part.Material = Enum.Material.DiamondPlate



else



-- When the part is unanchored...



part.BrickColor = BrickColor.new("Bright yellow")



part.Material = Enum.Material.Wood



end



end



local function onToggle()



-- Toggle the anchored property



part.Anchored = not part.Anchored



-- Update visual state of the brick



updateVisuals()



end



-- Update, then start listening for clicks



updateVisuals()



cd.MouseClick:Connect(onToggle)
```

---

API Reference

Properties

CursorIcon

Read Parallel

Sets the cursor icon to display when the mouse is hovered over the parent
of this [ClickDetector](/docs/reference/engine/classes/ClickDetector) or [DragDetector](/docs/reference/engine/classes/DragDetector).

ClickDetector.CursorIcon:ContentId

Sets the cursor icon to display when the mouse is hovered over the parent
of this [ClickDetector](/docs/reference/engine/classes/ClickDetector) or [DragDetector](/docs/reference/engine/classes/DragDetector). If this property is
left blank, the detector will use the default icon.

To change the cursor icon, set this property to the asset ID of the image
you'd like to use.

Provide feedback

---

CursorIconContent

Read Parallel

Sets the cursor icon to display when the mouse is hovered over the parent
of this [ClickDetector](/docs/reference/engine/classes/ClickDetector) or [DragDetector](/docs/reference/engine/classes/DragDetector). Only supports asset
URIs.

ClickDetector.CursorIconContent:[Content](/docs/reference/engine/datatypes/Content)

Sets the cursor icon to display when the mouse is hovered over the parent
of this [ClickDetector](/docs/reference/engine/classes/ClickDetector) or [DragDetector](/docs/reference/engine/classes/DragDetector). If this property is
left blank, the detector will use the default icon.

To change the cursor icon, set this property to the asset ID of the image
you'd like to use. Only asset URIs are supported for this property.

Provide feedback

---

MaxActivationDistance

Read Parallel

Maximum distance between a character and the [ClickDetector](/docs/reference/engine/classes/ClickDetector) or
[DragDetector](/docs/reference/engine/classes/DragDetector) for the player to be able to interact with it.

ClickDetector.MaxActivationDistance:[number](/docs/luau/numbers)

This property controls the maximum distance, in studs, between a
[Character](/docs/reference/engine/classes/Player#Character) and the [ClickDetector](/docs/reference/engine/classes/ClickDetector) or
[DragDetector](/docs/reference/engine/classes/DragDetector) for the player to be able to interact with it. For
instance, a character within 10 studs of a [ClickDetector](/docs/reference/engine/classes/ClickDetector) or
[DragDetector](/docs/reference/engine/classes/DragDetector) with a max activation distance of 5 would not be able
to use the detector because they are out of range.

Provide feedback

---

Events

MouseClick

Fires when a player interacts with the parent of a [ClickDetector](/docs/reference/engine/classes/ClickDetector)
or [DragDetector](/docs/reference/engine/classes/DragDetector).

ClickDetector.MouseClick(playerWhoClicked:[Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| playerWhoClicked:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) who clicked on the parent of a [ClickDetector](/docs/reference/engine/classes/ClickDetector) or [DragDetector](/docs/reference/engine/classes/DragDetector). |

This event fires from either a [Script](/docs/reference/engine/classes/Script) or [LocalScript](/docs/reference/engine/classes/LocalScript) when
a player interacts with a [ClickDetector](/docs/reference/engine/classes/ClickDetector) or [DragDetector](/docs/reference/engine/classes/DragDetector)
via the following inputs:

* On platforms with a mouse, when the player left mouse clicks.
* On [TouchEnabled](/docs/reference/engine/classes/UserInputService#TouchEnabled) platforms, when
  the player taps.
* On [GamepadEnabled](/docs/reference/engine/classes/UserInputService#GamepadEnabled) platforms,
  when the center dot is over the same model and the A button is
  pressed and released.

Note that the player's [Character](/docs/reference/engine/classes/Player#Character) must be within
the [MaxActivationDistance](/docs/reference/engine/classes/ClickDetector#MaxActivationDistance) of
the detector.

Provide feedback

---

mouseClick

Deprecated

Show details

---

MouseHoverEnter

Fires when the parent of a [ClickDetector](/docs/reference/engine/classes/ClickDetector) or [DragDetector](/docs/reference/engine/classes/DragDetector)
is hovered over by a player.

ClickDetector.MouseHoverEnter(playerWhoHovered:[Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| playerWhoHovered:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) who started hovering over the parent of a [ClickDetector](/docs/reference/engine/classes/ClickDetector) or [DragDetector](/docs/reference/engine/classes/DragDetector). |

This event fires from either a [Script](/docs/reference/engine/classes/Script) or [LocalScript](/docs/reference/engine/classes/LocalScript) when
the parent of a [ClickDetector](/docs/reference/engine/classes/ClickDetector) or [DragDetector](/docs/reference/engine/classes/DragDetector) is hovered
over by a player. This does not entail explicit interaction with the
detector, for which you can listen to either
[MouseClick](/docs/reference/engine/classes/ClickDetector#MouseClick) and
[RightMouseClick](/docs/reference/engine/classes/ClickDetector#RightMouseClick) events.

Due to the nature of user input, you should not depend on all
[MouseHoverEnter](/docs/reference/engine/classes/ClickDetector#MouseHoverEnter) events firing a
corresponding [MouseHoverLeave](/docs/reference/engine/classes/ClickDetector#MouseHoverLeave) event.

Code Samples

Hovering Over and Off a ClickDetector

The following code will print "[PlayerName] hovered over my parent!" when a player's cursor hovers over the [ClickDetector](/docs/reference/engine/classes/ClickDetector) parent. It will also print "[PlayerName] hovered off my parent!" when the player's cursor moves off the [ClickDetector](/docs/reference/engine/classes/ClickDetector) parent.

In order for this example to work as expected, it must be placed in a Script or LocalScript whose parent is a [ClickDetector](/docs/reference/engine/classes/ClickDetector).

```
local clickDetector = script.Parent:FindFirstChildOfClass("ClickDetector")



clickDetector.MouseHoverEnter:Connect(function(player)



print(player.Name .. " hovered over my parent!")



end)



clickDetector.MouseHoverLeave:Connect(function(player)



print(player.Name .. " hovered off my parent!")



end)
```

Provide feedback

---

MouseHoverLeave

Fires when a player's cursor hovers off the parent of a
[ClickDetector](/docs/reference/engine/classes/ClickDetector) or [DragDetector](/docs/reference/engine/classes/DragDetector).

ClickDetector.MouseHoverLeave(playerWhoHovered:[Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| playerWhoHovered:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) whose cursor hovered off the parent of a [ClickDetector](/docs/reference/engine/classes/ClickDetector) or [DragDetector](/docs/reference/engine/classes/DragDetector). |

This event fires from either a [Script](/docs/reference/engine/classes/Script) or [LocalScript](/docs/reference/engine/classes/LocalScript) when
a player's cursor hovers off the parent of a [ClickDetector](/docs/reference/engine/classes/ClickDetector) or
[DragDetector](/docs/reference/engine/classes/DragDetector). This does not entail explicit interaction with the
detector, for which you can listen to either
[MouseClick](/docs/reference/engine/classes/ClickDetector#MouseClick) and
[RightMouseClick](/docs/reference/engine/classes/ClickDetector#RightMouseClick) events.

Due to the nature of user input, you should not depend on all
[MouseHoverLeave](/docs/reference/engine/classes/ClickDetector#MouseHoverLeave) events firing after
a corresponding [MouseHoverEnter](/docs/reference/engine/classes/ClickDetector#MouseHoverEnter)
event.

Code Samples

Hovering Over and Off a ClickDetector

The following code will print "[PlayerName] hovered over my parent!" when a player's cursor hovers over the [ClickDetector](/docs/reference/engine/classes/ClickDetector) parent. It will also print "[PlayerName] hovered off my parent!" when the player's cursor moves off the [ClickDetector](/docs/reference/engine/classes/ClickDetector) parent.

In order for this example to work as expected, it must be placed in a Script or LocalScript whose parent is a [ClickDetector](/docs/reference/engine/classes/ClickDetector).

```
local clickDetector = script.Parent:FindFirstChildOfClass("ClickDetector")



clickDetector.MouseHoverEnter:Connect(function(player)



print(player.Name .. " hovered over my parent!")



end)



clickDetector.MouseHoverLeave:Connect(function(player)



print(player.Name .. " hovered off my parent!")



end)
```

Provide feedback

---

RightMouseClick

Fires when a player right clicks their mouse cursor on a
[ClickDetector](/docs/reference/engine/classes/ClickDetector) or [DragDetector](/docs/reference/engine/classes/DragDetector).

ClickDetector.RightMouseClick(playerWhoClicked:[Player](/docs/reference/engine/classes/Player)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| playerWhoClicked:[Player](/docs/reference/engine/classes/Player)  The [Player](/docs/reference/engine/classes/Player) who right clicked their mouse cursor on the parent of a [ClickDetector](/docs/reference/engine/classes/ClickDetector) or [DragDetector](/docs/reference/engine/classes/DragDetector). |

This event fires from either a [Script](/docs/reference/engine/classes/Script) or [LocalScript](/docs/reference/engine/classes/LocalScript) when
a player right clicks their mouse cursor on a [ClickDetector](/docs/reference/engine/classes/ClickDetector) or
[DragDetector](/docs/reference/engine/classes/DragDetector). Note that the player's
[Character](/docs/reference/engine/classes/Player#Character) must be within the
[MaxActivationDistance](/docs/reference/engine/classes/ClickDetector#MaxActivationDistance) of the
detector.

Provide feedback

---