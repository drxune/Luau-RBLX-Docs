# ForceLimitMode | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/ForceLimitMode
Scraped: 2026-01-11T02:45:53.041875Z
1. [Enums](/docs/reference/engine/enums)
2. /
3. [ForceLimitMode](/docs/reference/engine/enums/ForceLimitMode)

English

Feedback

Engine Enum

ForceLimitMode

---

This enum is used to determine how the maximum force for a constraint is
specified and how that limit will be enforced by the constraint.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Magnitude | 0 | A single number is used to specify the magnitude of the maximum constraint force. The constraint will ensure that the force it applies will have a magnitude that is less than this limit. |
| PerAxis | 1 | A vector is used to specify the maximum force value along each axis of a given reference frame. The constraint will ensure that each component of the force will have an absolute value that's less than the corresponding vector entry. |