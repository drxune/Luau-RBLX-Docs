# CameraMode | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/CameraMode
Scraped: 2026-01-11T02:43:04.760728Z

## Inherits
- Player.CameraMode
- GuiButton.Modal
1. [Enums](/docs/reference/engine/enums)
2. /
3. [CameraMode](/docs/reference/engine/enums/CameraMode)

English

Feedback

Engine Enum

CameraMode

---

The CameraMode enum is used to set [Player.CameraMode](/docs/reference/engine/classes/Player#CameraMode) to determine
when first person and third person cameras should be used.

#### Third Person

In the default third person mode ([Classic](/docs/reference/engine/enums/CameraMode)), the character
can be seen in the camera. While in this mode, the default behavior is:

* Players can right-click and drag (mouse), tap and drag (mobile), use the
  secondary thumbstick (gamepad), or press the left/right arrows (keyboard) to
  rotate the camera around their character.
* When a player moves their character, it faces in the corresponding movement
  direction.
* Players can zoom in and out freely, even to first person on full zoom in.

#### First Person

In first person mode ([LockFirstPerson](/docs/reference/engine/enums/CameraMode)), the player's camera
is zoomed all the way in. Unless there is a visible GUI present with the
[GuiButton.Modal](/docs/reference/engine/classes/GuiButton#Modal) property set to true, moving the mouse, tap-dragging
on mobile, or using the secondary thumbstick on a gamepad will rotate the
camera around the character.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Classic | 0 | Third person camera which can be zoomed into first person. |
| LockFirstPerson | 1 | Exclusively first person camera. |