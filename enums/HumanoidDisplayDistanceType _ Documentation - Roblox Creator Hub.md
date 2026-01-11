# HumanoidDisplayDistanceType | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/HumanoidDisplayDistanceType
Scraped: 2026-01-11T02:45:58.733724Z

## Inherits
- Humanoid.HealthDisplayDistance
- Humanoid.NameDisplayDistance
- Humanoid
1. [Enums](/docs/reference/engine/enums)
2. /
3. [HumanoidDisplayDistanceType](/docs/reference/engine/enums/HumanoidDisplayDistanceType)

English

Feedback

Engine Enum

HumanoidDisplayDistanceType

---

HumanoidDisplayDistanceType determines how
[Humanoid.HealthDisplayDistance](/docs/reference/engine/classes/Humanoid#HealthDisplayDistance), and
[Humanoid.NameDisplayDistance](/docs/reference/engine/classes/Humanoid#NameDisplayDistance) are used in determining whether a
players's name and health are visible to other players.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Viewer | 0 | A player selecting Viewer on their [Humanoid](/docs/reference/engine/classes/Humanoid) will see the Name and healthbar of other players if those other players are within the distance settings set in the [Humanoid](/docs/reference/engine/classes/Humanoid) selecting Viewer (this can be thought of as the lowest priority, and will not be taken into account if other players are selecting 'Subject' or 'None'). |
| Subject | 1 | A player selecting Subject on their [Humanoid](/docs/reference/engine/classes/Humanoid) will allow other players to see their Name and healthbar if those other players are within the distance settings set in the [Humanoid](/docs/reference/engine/classes/Humanoid) selecting Subject (this can be thought of as the second highest priority). |
| None | 2 | A player selecting None on their [Humanoid](/docs/reference/engine/classes/Humanoid) will not have their Name and healthbar displayed to other players under any circumstance (this can be thought of as the highest priority). |