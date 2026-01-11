# IKCollisionsMode | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/IKCollisionsMode
Scraped: 2026-01-11T02:46:22.484748Z

## Inherits
- constraints
1. [Enums](/docs/reference/engine/enums)
2. /
3. [IKCollisionsMode](/docs/reference/engine/enums/IKCollisionsMode)

English

Feedback

Engine Enum

IKCollisionsMode

---

Items

| Name | Value | Summary |
| --- | --- | --- |
| NoCollisions | 0 | Only the part and any parts directly joined to it via joints/[constraints](/docs/reference/engine/classes/Constraint) be involved in the resolution, everything else in the workspace will be treated as though it doesn't exist. |
| OtherMechanismsAnchored | 1 | Only the part and any parts directly jointed to it via joints/[constraints](/docs/reference/engine/classes/Constraint) will be moved during resolution, but they will collide with other objects in the workspace. |
| IncludeContactedMechanisms | 2 | The part, any parts directly joined to it via joints/[constraints](/docs/reference/engine/classes/Constraint), and any parts which it comes into contact with during the solve will be moved during the resolution. That is, the moved parts will be allowed to "push" other unanchored parts in the workspace out of the way in order to get to the target position. |