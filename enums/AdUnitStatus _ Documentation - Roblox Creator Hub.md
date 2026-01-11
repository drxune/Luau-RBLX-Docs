# AdUnitStatus | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/AdUnitStatus
Scraped: 2026-01-11T02:43:06.717405Z

## Inherits
- AdGui
- AdPortal
1. [Enums](/docs/reference/engine/enums)
2. /
3. [AdUnitStatus](/docs/reference/engine/enums/AdUnitStatus)

English

Feedback

Engine Enum

AdUnitStatus

---

Exposes the status of an immersive ad.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Inactive | 0 | The ad unit isn't currently serving an ad and it may be configured incorrectly. An [AdGui](/docs/reference/engine/classes/AdGui) with this status will display its fallback image. |
| Active | 1 | The ad unit is currently serving an ad. Players will observe sponsored content in an [AdGui](/docs/reference/engine/classes/AdGui) and an [AdPortal](/docs/reference/engine/classes/AdPortal) will teleport users that walk through. |