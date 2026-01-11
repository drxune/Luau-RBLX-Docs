# HumanoidHealthDisplayType | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/HumanoidHealthDisplayType
Scraped: 2026-01-11T02:43:03.210741Z

## Inherits
- Humanoid
- Humanoid.MaxHealth
1. [Enums](/docs/reference/engine/enums)
2. /
3. [HumanoidHealthDisplayType](/docs/reference/engine/enums/HumanoidHealthDisplayType)

English

Feedback

Engine Enum

HumanoidHealthDisplayType

---

Controls when the [Humanoid](/docs/reference/engine/classes/Humanoid) health bar is displayed. This works in
conjunction with the [Humanoid.MaxHealth](/docs/reference/engine/classes/Humanoid#MaxHealth) property which must have a
value higher than zero or the health bar doesn't display.

Items

| Name | Value | Summary |
| --- | --- | --- |
| DisplayWhenDamaged | 0 | The humanoid's health bar is only visible when the humanoid is not at full health (assuming MaxHealth is greater than zero). |
| AlwaysOn | 1 | The humanoid's health bar is always visible (assuming MaxHealth is greater than zero). |
| AlwaysOff | 2 | The humanoid's health bar is never visible. |