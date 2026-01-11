# InputActionType | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/InputActionType
Scraped: 2026-01-11T02:43:25.890721Z

## Inherits
- InputAction.Type
- InputAction
- UIButton
- InputBindings
- GuiButton
- Up
- Down
- Left
- Right
- Forward
- Backward
1. [Enums](/docs/reference/engine/enums)
2. /
3. [InputActionType](/docs/reference/engine/enums/InputActionType)

English

Feedback

Engine Enum

InputActionType

---

This enum is used by [InputAction.Type](/docs/reference/engine/classes/InputAction#Type) to determine which input data
type the [InputAction](/docs/reference/engine/classes/InputAction) will receive.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Bool | 0 | The [InputAction](/docs/reference/engine/classes/InputAction) will receive boolean values from button inputs, for example true/false on press/release from inputs such as [Enum.KeyCode.ButtonA](/docs/reference/engine/enums/KeyCode#ButtonA) or [Enum.KeyCode.E](/docs/reference/engine/enums/KeyCode#E). This setting also exposes the [UIButton](/docs/reference/engine/classes/InputBinding#UIButton) property on child [InputBindings](/docs/reference/engine/classes/InputBinding), allowing you to easily hook up press or release of a [GuiButton](/docs/reference/engine/classes/GuiButton) for the action. |
| Direction1D | 1 | The [InputAction](/docs/reference/engine/classes/InputAction) will receive numerical values, generally from analog gamepad triggers such as [Enum.KeyCode.ButtonL2](/docs/reference/engine/enums/KeyCode#ButtonL2) or [Enum.KeyCode.ButtonR2](/docs/reference/engine/enums/KeyCode#ButtonR2). This setting also exposes the [Up](/docs/reference/engine/classes/InputBinding#Up) and [Down](/docs/reference/engine/classes/InputBinding#Down) properties on child [InputBindings](/docs/reference/engine/classes/InputBinding), allowing for boolean inputs or "1D" inputs as composite directions for the action. |
| Direction2D | 2 | The [InputAction](/docs/reference/engine/classes/InputAction) will receive [Vector2](/docs/reference/engine/datatypes/Vector2) values, generally from thumbstick inputs such as [Enum.KeyCode.Thumbstick1](/docs/reference/engine/enums/KeyCode#Thumbstick1) and [Enum.KeyCode.Thumbstick2](/docs/reference/engine/enums/KeyCode#Thumbstick2). This setting also exposes the [Up](/docs/reference/engine/classes/InputBinding#Up), [Down](/docs/reference/engine/classes/InputBinding#Down), [Left](/docs/reference/engine/classes/InputBinding#Left), and [Right](/docs/reference/engine/classes/InputBinding#Right) properties on child [InputBindings](/docs/reference/engine/classes/InputBinding), allowing for "2D" inputs as composite directions for the action. |
| Direction3D | 3 | The [InputAction](/docs/reference/engine/classes/InputAction) will receive [Vector3](/docs/reference/engine/datatypes/Vector3) values from inputs assigned to the [Up](/docs/reference/engine/classes/InputBinding#Up), [Down](/docs/reference/engine/classes/InputBinding#Down), [Left](/docs/reference/engine/classes/InputBinding#Left), [Right](/docs/reference/engine/classes/InputBinding#Right), [Forward](/docs/reference/engine/classes/InputBinding#Forward), and/or [Backward](/docs/reference/engine/classes/InputBinding#Backward) properties on child [InputBindings](/docs/reference/engine/classes/InputBinding), allowing for "3D" inputs as composite directions for the action. |
| ViewportPosition | 4 | The [InputAction](/docs/reference/engine/classes/InputAction) will receive [Vector2](/docs/reference/engine/datatypes/Vector2) values representing the absolute pixel (X, Y) coordinates of a pointer input in the viewport. |