# ControlMode | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/ControlMode
Scraped: 2026-01-11T02:45:05.750711Z

## Inherits
- UserInputService.MouseBehavior
1. [Enums](/docs/reference/engine/enums)
2. /
3. [ControlMode](/docs/reference/engine/enums/ControlMode)

English

Feedback

Engine Enum

ControlMode

---

The ControlMode Enum sets how the player is controlled.

Note that shift-lock related APIs are in the process of being deprecated, so
it's recommended to use [UserInputService.MouseBehavior](/docs/reference/engine/classes/UserInputService#MouseBehavior) instead to lock
the mouse.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Classic | 0 | Allows the camera to be moved by clicking and dragging with the right mouse button. |
| MouseLockSwitch | 1 | Similar to classic, but allows the player to toggle mouse locking, causing the camera to rotate as the player moves the mouse (without holding down a button). |