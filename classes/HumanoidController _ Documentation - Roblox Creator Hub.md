# HumanoidController | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/HumanoidController
Scraped: 2026-01-11T02:38:34.265535Z

## Inherits
- Controller
- HumanoidController
- Instance
- Object
- Humanoid
- ControllerService
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Controller](/docs/reference/engine/classes/Controller)
6. /
7. [HumanoidController](/docs/reference/engine/classes/HumanoidController)

English

Feedback

Engine Class

HumanoidController

---

Summary

Inherited Members

6 inherited from [Controller](/docs/reference/engine/classes/Controller)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A HumanoidController is an internal object responsible for translating
PlayerAction movements to the user's character (specifically, their
[Humanoid](/docs/reference/engine/classes/Humanoid)).

This object can be found inside of the [ControllerService](/docs/reference/engine/classes/ControllerService), via:

```
local ControllerService = game:GetService("ControllerService")



local HumanoidController = ControllerService:FindFirstChildOfClass("HumanoidController")
```