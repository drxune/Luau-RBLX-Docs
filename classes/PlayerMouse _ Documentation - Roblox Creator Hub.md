# PlayerMouse | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/PlayerMouse
Scraped: 2026-01-11T02:36:48.949312Z

## Tags
- Not Creatable

## Inherits
- Mouse
- PlayerMouse
- Tool.Equipped
- UserInputService
- Instance
- Object
- LocalScripts
- Player:GetMouse()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Mouse](/docs/reference/engine/classes/Mouse)
6. /
7. [PlayerMouse](/docs/reference/engine/classes/PlayerMouse)

English

Feedback

Engine Class

PlayerMouse

The PlayerMouse behaves identically to the [Mouse](/docs/reference/engine/classes/Mouse) object that is
obtained using [Tool.Equipped](/docs/reference/engine/classes/Tool#Equipped). Both PlayerMouse and [Mouse](/docs/reference/engine/classes/Mouse) are
legacy APIs, superseded by [UserInputService](/docs/reference/engine/classes/UserInputService).

Not Creatable

---

Summary

Inherited Members

25 inherited from [Mouse](/docs/reference/engine/classes/Mouse)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The PlayerMouse behaves identically to the [Mouse](/docs/reference/engine/classes/Mouse) object that is
obtained using [Tool.Equipped](/docs/reference/engine/classes/Tool#Equipped). It can be accessed from
[LocalScripts](/docs/reference/engine/classes/LocalScript) using the local player's
[Player:GetMouse()](/docs/reference/engine/classes/Player#GetMouse) method. Both PlayerMouse and [Mouse](/docs/reference/engine/classes/Mouse) are
legacy APIs, superseded by [UserInputService](/docs/reference/engine/classes/UserInputService).

The only difference between the PlayerMouse and the [Mouse](/docs/reference/engine/classes/Mouse) object is
the PlayerMouse can be obtained using the [Player:GetMouse()](/docs/reference/engine/classes/Player#GetMouse) method.

In most cases developers are advised to use the new [UserInputService](/docs/reference/engine/classes/UserInputService).
However the PlayerMouse and Mouse objects remain supported for a number of
reasons. See [Input and Camera](/docs/input) for more information
on customizing inputs in your experience.

Code Samples

PlayerMouse

This code sample includes a simple example of how the local player's
PlayerMouse can be retrieved using the [Player:GetMouse()](/docs/reference/engine/classes/Player#GetMouse) function in
a LocalScript. This code should be placed in a LocalScript in
StarterPlayerScripts.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



local mouse = player:GetMouse()



local function onMouseMove()



print("mouse screen position: ", mouse.X, mouse.Y)



end



mouse.Move:Connect(onMouseMove)
```