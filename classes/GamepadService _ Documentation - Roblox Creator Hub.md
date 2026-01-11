# GamepadService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/GamepadService
Scraped: 2026-01-11T02:29:44.651398Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Instance
- GamepadService
- Object
- StarterGui
- GuiObject
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [GamepadService](/docs/reference/engine/classes/GamepadService)

English

Feedback

Engine Class

GamepadService

The GamepadService is internally responsible for handling inputs from various
controllers, such as Xbox One or PlayStation DualShock controllers.

Not Creatable

Service

Not Replicated

---

Summary

Properties

|  |
| --- |
| [GamepadCursorEnabled](#GamepadCursorEnabled):[boolean](/docs/luau/booleans) |

Methods

|  |
| --- |
| [DisableGamepadCursor](#DisableGamepadCursor)():() |
| [EnableGamepadCursor](#EnableGamepadCursor)(guiObject: [Instance](/docs/reference/engine/datatypes/Instance)):() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The GamepadService is internally responsible for handling inputs from various
controllers, such as Xbox One or PlayStation DualShock controllers. It also
handles APIs used with the gamepad virtual cursor. You can enable the gamepad
cursor for your experience by setting [Enum.VirtualCursorMode](/docs/reference/engine/enums/VirtualCursorMode) under
[StarterGui](/docs/reference/engine/classes/StarterGui) to Enabled.

---

API Reference

Properties

GamepadCursorEnabled

Roblox Script Security

Read Parallel

The state of the gamepad virtual cursor.

GamepadService.GamepadCursorEnabled:[boolean](/docs/luau/booleans)

This boolean is a read only variable that maintains the state of the
gamepad virtual cursor. You can read this property but not write to it.

Code Samples

GamepadService - Gamepad Cursor Enabled Property

```
local gamepadService = game.GamepadService



gamepadService:GetPropertyChangedSignal("GamepadCursorEnabled"):Connect(function()



local enabled = gamepadService.GamepadCursorEnabled



if enabled then



-- Custom code when the virtual cursor is enabled



else



-- Custom code when the virtual cursor is disabled



end



end)
```

Provide feedback

---

Methods

DisableGamepadCursor

Disables the gamepad cursor, if currently enabled.

GamepadService:DisableGamepadCursor():()

Returns

()

This function disables the gamepad cursor, if it's currently enabled.

Code Samples

GamepadService - Disable Gamepad Cursor

In this example, the cursor is disabled when the user presses
[Enum.KeyCode.ButtonB](/docs/reference/engine/enums/KeyCode#ButtonB).

```
local gamepadService = game.GamepadService



local userInputService = game.UserInputService



userInputService.InputBegan:Connect(function(inputObject, gameProcessed)



if inputObject.KeyCode == Enum.KeyCode.ButtonB then



gamepadService:DisableGamepadCursor()



end



end)
```

Provide feedback

---

EnableGamepadCursor

Enables the gamepad cursor or updates its position.

GamepadService:EnableGamepadCursor(guiObject:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| guiObject:[Instance](/docs/reference/engine/datatypes/Instance) |

Returns

()

This function enables the gamepad cursor if it's currently disabled. If
the cursor is already enabled, calling the API updates the cursor's
position. The function accepts a [GuiObject](/docs/reference/engine/classes/GuiObject) parameter,
but there are some invalid cases. Please note that in order to set the
cursor to the default position, nil must be passed in as a parameter.
Providing no argument will result in an error.

|  |  |
| --- | --- |
| Input GuiObject | Cursor Starting Position |
|  |  |
| --- | --- |
| Nil | Default position |
| Not a GuiObject | Cursor does not appear, errors |  |
| Not a child of BasePlayerGui | Cursor does not appear, errors |
| GuiObject has Visible 2 set to false or any parent visible set to false | Default position with warning |
| Child of ScreenGui 1 with Enabled 1 set to false | Default position with warning |
| Child of BillboardGui 4 or SurfaceGui | Default position with warning |
| GuiObject outside the viewport (Or, any part of the gui object that is off screen) | Default position with warning |
| Child of ScrollingFrame with clipping set to false: GuiObject outside of scrolling frame (Object child of scrolling frame and not visible on screen) | Default position with warning |
| Child of ScrollingFrame with clipping set to true: GuiObject outside scrolling frame window but inside viewport | GuiObject moves into the scrolling frame and starts the cursor centered over the object |
| GuiObject inside the frame and visible | Cursor starts centered on the GuiObject |

Code Samples

GamepadService - Enable Gamepad Cursor

In this example, the cursor is enabled when the user presses
[Enum.KeyCode.ButtonA](/docs/reference/engine/enums/KeyCode#ButtonA) with the starting button being this script's parent.

```
local gamepadService = game.GamepadService



local userInputService = game.UserInputService



local startObject = script.Parent



userInputService.InputBegan:Connect(function(inputObject, gameProcessed)



if inputObject.KeyCode == Enum.KeyCode.ButtonA then



gamepadService:EnableGamepadCursor(startObject)



end



end)
```

Provide feedback

---