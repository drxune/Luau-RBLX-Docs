# IKControlType | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/IKControlType
Scraped: 2026-01-11T02:45:05.487766Z

## Inherits
- IKControl
- Type
- EndEffector
- Target
1. [Enums](/docs/reference/engine/enums)
2. /
3. [IKControlType](/docs/reference/engine/enums/IKControlType)

English

Feedback

Engine Enum

IKControlType

---

Used on [IKControl](/docs/reference/engine/classes/IKControl) to specify their [Type](/docs/reference/engine/classes/IKControl#Type), to
change their behavior.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Transform | 0 | It is a full 6-DoF constraint. Aligns the [EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) [CFrame](/docs/reference/engine/datatypes/CFrame) to that of the [Target](/docs/reference/engine/classes/IKControl#Target). It is the default value. |
| Position | 1 | Aligns the [EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) position to that of the [Target](/docs/reference/engine/classes/IKControl#Target) . |
| Rotation | 2 | Aligns the [EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) rotation to that of the [Target](/docs/reference/engine/classes/IKControl#Target). |
| LookAt | 3 | Moves and orients the whole chain to make the forward axis on the [EndEffector](/docs/reference/engine/classes/IKControl#EndEffector) point at a position in the world specified by [Target](/docs/reference/engine/classes/IKControl#Target). |