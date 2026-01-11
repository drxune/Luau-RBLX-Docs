# ListenerType | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/ListenerType
Scraped: 2026-01-11T02:44:16.326758Z

## Inherits
- SoundService.SetListener
- SoundService.GetListener
1. [Enums](/docs/reference/engine/enums)
2. /
3. [ListenerType](/docs/reference/engine/enums/ListenerType)

English

Feedback

Engine Enum

ListenerType

---

Defines where and how the listener is positioned when picking up spatial
audio. Used in [SoundService.SetListener](/docs/reference/engine/classes/SoundService#SetListener) and
[SoundService.GetListener](/docs/reference/engine/classes/SoundService#GetListener).

Items

| Name | Value | Summary |
| --- | --- | --- |
| Camera | 0 | Uses the world CFrame of workspace.CurrentCamera. |
| CFrame | 1 | Uses a specified world CFrame. |
| ObjectPosition | 2 | Uses the world position of an instance and the rotation of workspace.CurrentCamera. |
| ObjectCFrame | 3 | Uses the world CFrame from an instance. |