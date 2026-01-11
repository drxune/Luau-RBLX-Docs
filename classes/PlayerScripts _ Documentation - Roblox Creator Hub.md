# PlayerScripts | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/PlayerScripts
Scraped: 2026-01-11T02:32:41.287559Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- Instance
- PlayerScripts
- Player
- Players
- LocalScripts
- StarterPlayerScripts
- StarterPlayer
- Backpack
- PlayerGui
- Script
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [PlayerScripts](/docs/reference/engine/classes/PlayerScripts)

English

Feedback

Engine Class

PlayerScripts

A container for LocalScripts to be run on the client.

Not Creatable

Not Replicated

---

Summary

Methods

|  |
| --- |
| [ClearComputerCameraMovementModes](#ClearComputerCameraMovementModes)():() |
| [ClearComputerMovementModes](#ClearComputerMovementModes)():() |
| [ClearTouchCameraMovementModes](#ClearTouchCameraMovementModes)():() |
| [ClearTouchMovementModes](#ClearTouchMovementModes)():() |
| [RegisterComputerCameraMovementMode](#RegisterComputerCameraMovementMode)(cameraMovementMode: [Enum.ComputerCameraMovementMode](/docs/reference/engine/enums/ComputerCameraMovementMode)):() |
| [RegisterComputerMovementMode](#RegisterComputerMovementMode)(movementMode: [Enum.ComputerMovementMode](/docs/reference/engine/enums/ComputerMovementMode)):() |
| [RegisterTouchCameraMovementMode](#RegisterTouchCameraMovementMode)(cameraMovementMode: [Enum.TouchCameraMovementMode](/docs/reference/engine/enums/TouchCameraMovementMode)):() |
| [RegisterTouchMovementMode](#RegisterTouchMovementMode)(movementMode: [Enum.TouchMovementMode](/docs/reference/engine/enums/TouchMovementMode)):() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

[PlayerScripts](/docs/reference/engine/classes/PlayerScripts) is a container object located inside [Player](/docs/reference/engine/classes/Player)
objects within the [Players](/docs/reference/engine/classes/Players) game service. It is created automatically
when a player joins the game. Its main purpose is to contain
[LocalScripts](/docs/reference/engine/classes/LocalScript) copied from the [StarterPlayerScripts](/docs/reference/engine/classes/StarterPlayerScripts)
container within the [StarterPlayer](/docs/reference/engine/classes/StarterPlayer) game service, which happens once
upon creation. Descendant LocalScripts of [PlayerScripts](/docs/reference/engine/classes/PlayerScripts) will run
code on the client of the [Player](/docs/reference/engine/classes/Player).

Unlike the [Backpack](/docs/reference/engine/classes/Backpack) and [PlayerGui](/docs/reference/engine/classes/PlayerGui) containers, the
[PlayerScripts](/docs/reference/engine/classes/PlayerScripts) container is not accessible to the server. Server
[Script](/docs/reference/engine/classes/Script) objects will not run when parented to [PlayerScripts](/docs/reference/engine/classes/PlayerScripts).

---

API Reference

Methods

ClearComputerCameraMovementModes

Unregisters all ComputerCameraMovementMode enums from the experience's
settings menu.

PlayerScripts:ClearComputerCameraMovementModes():()

Returns

()

Unregisters all ComputerCameraMovementMode enums from the experience's
settings menu.

Provide feedback

---

ClearComputerMovementModes

Unregisters all ComputerMovementMode enums from the experience's settings
menu.

PlayerScripts:ClearComputerMovementModes():()

Returns

()

Unregisters all ComputerMovementMode enums from the experience's settings
menu.

Provide feedback

---

ClearTouchCameraMovementModes

Unregisters all TouchCameraMovementMode enums from the experience's
settings menu.

PlayerScripts:ClearTouchCameraMovementModes():()

Returns

()

Unregisters all TouchCameraMovementMode enums from the experience's
settings menu.

Provide feedback

---

ClearTouchMovementModes

Unregisters all TouchMovementMode enums from the experience's settings
menu.

PlayerScripts:ClearTouchMovementModes():()

Returns

()

Unregisters all TouchMovementMode enums from the experience's settings
menu.

Provide feedback

---

RegisterComputerCameraMovementMode

Registers that a computer camera movement mode is available to be selected
from the game menu.

PlayerScripts:RegisterComputerCameraMovementMode(cameraMovementMode:[Enum.ComputerCameraMovementMode](/docs/reference/engine/enums/ComputerCameraMovementMode)):()

Parameters

|  |
| --- |
| cameraMovementMode:[Enum.ComputerCameraMovementMode](/docs/reference/engine/enums/ComputerCameraMovementMode) |

Returns

()

Registers that a computer camera movement mode is available to be selected
from the game menu.

Provide feedback

---

RegisterComputerMovementMode

Registers that a computer movement mode is available to be selected from
the game menu.

PlayerScripts:RegisterComputerMovementMode(movementMode:[Enum.ComputerMovementMode](/docs/reference/engine/enums/ComputerMovementMode)):()

Parameters

|  |
| --- |
| movementMode:[Enum.ComputerMovementMode](/docs/reference/engine/enums/ComputerMovementMode) |

Returns

()

Registers that a computer movement mode is available to be selected from
the game menu.

Provide feedback

---

RegisterTouchCameraMovementMode

Registers that a touch camera movement mode is available to be selected
from the game menu.

PlayerScripts:RegisterTouchCameraMovementMode(cameraMovementMode:[Enum.TouchCameraMovementMode](/docs/reference/engine/enums/TouchCameraMovementMode)):()

Parameters

|  |
| --- |
| cameraMovementMode:[Enum.TouchCameraMovementMode](/docs/reference/engine/enums/TouchCameraMovementMode) |

Returns

()

Registers that a touch camera movement mode is available to be selected
from the game menu.

Provide feedback

---

RegisterTouchMovementMode

Registers that a touch movement mode is available to be selected from the
game menu.

PlayerScripts:RegisterTouchMovementMode(movementMode:[Enum.TouchMovementMode](/docs/reference/engine/enums/TouchMovementMode)):()

Parameters

|  |
| --- |
| movementMode:[Enum.TouchMovementMode](/docs/reference/engine/enums/TouchMovementMode) |

Returns

()

Registers that a touch movement mode is available to be selected from the
game menu.

Provide feedback

---