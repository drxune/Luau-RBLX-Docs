# RaycastFilterType | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/RaycastFilterType
Scraped: 2026-01-11T02:43:26.580742Z

## Inherits
- BasePart
- BaseParts
1. [Enums](/docs/reference/engine/enums)
2. /
3. [RaycastFilterType](/docs/reference/engine/enums/RaycastFilterType)

English

Feedback

Engine Enum

RaycastFilterType

---

Used in a [RaycastParams](/docs/reference/engine/datatypes/RaycastParams) object to determine how its
[FilterDescendantsInstances](/docs/reference/engine/datatypes/RaycastParams#FilterDescendantsInstances)
list will be used.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Exclude | 0 | Every [BasePart](/docs/reference/engine/classes/BasePart) in the raycast operation will be considered except those that are descendants of objects in the filter list. |
| Include | 1 | Only [BaseParts](/docs/reference/engine/classes/BasePart) which are descendants of objects in the filter list will be considered in the raycast operation. |