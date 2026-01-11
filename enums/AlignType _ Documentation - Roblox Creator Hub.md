# AlignType | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/AlignType
Scraped: 2026-01-11T02:45:42.988353Z

## Inherits
- Constraint.Attachment1
- AlignOrientation.LookAtPosition
- Constraint.Attachment0
- AlignOrientation.PrimaryAxis
- AlignOrientation.SecondaryAxis
1. [Enums](/docs/reference/engine/enums)
2. /
3. [AlignType](/docs/reference/engine/enums/AlignType)

English

Feedback

Engine Enum

AlignType

---

An enum that specifies how the constraint will attempt to align the body
associated with the constraint and attachment. Depending on the configuration,
it can be used to align specific axes to be parallel, perpendicular, or to
look at a specific point.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Parallel | 0 | Deprecated |
| Perpendicular | 1 | Deprecated |
| PrimaryAxisParallel | 2 | Aligns the primary axis to be parallel to the axis given by [Constraint.Attachment1](/docs/reference/engine/classes/Constraint#Attachment1). |
| PrimaryAxisPerpendicular | 3 | Aligns the primary axis to be perpendicular to the axis given by [Constraint.Attachment1](/docs/reference/engine/classes/Constraint#Attachment1). |
| PrimaryAxisLookAt | 4 | Aligns the primary axis to look at the point given by [Constraint.Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) or the [AlignOrientation.LookAtPosition](/docs/reference/engine/classes/AlignOrientation#LookAtPosition). |
| AllAxes | 5 | Aligns all of the axes of [Constraint.Attachment0](/docs/reference/engine/classes/Constraint#Attachment0) to the axes given by [Constraint.Attachment1](/docs/reference/engine/classes/Constraint#Attachment1) or to the target orientation provided by [AlignOrientation.PrimaryAxis](/docs/reference/engine/classes/AlignOrientation#PrimaryAxis) and [AlignOrientation.SecondaryAxis](/docs/reference/engine/classes/AlignOrientation#SecondaryAxis). |