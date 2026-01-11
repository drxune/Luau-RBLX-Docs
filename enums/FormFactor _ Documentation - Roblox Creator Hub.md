# FormFactor | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/FormFactor
Scraped: 2026-01-11T02:44:02.382529Z

## Inherits
- FormFactorPart.FormFactor
1. [Enums](/docs/reference/engine/enums)
2. /
3. [FormFactor](/docs/reference/engine/enums/FormFactor)

English

Feedback

Engine Enum

FormFactor

Deprecated

This item is deprecated as parts no longer contain a FormFactor to determine
their minimum size. The minimum size of all parts now behaves like "Custom" by
default.

---

The FormFactor Enum for [FormFactorPart.FormFactor](/docs/reference/engine/classes/FormFactorPart#FormFactor).

Minimum size along a given axis is 1 \* RateOfIncrease for that axis, except
in the case of the "Custom" FormFactor, which has a minimum size of 0.2 along
all axes.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Symmetric | 0 | Increases by a rate of 1 along all axes. |
| Brick | 1 | Increases by a rate of 1 along the x- and z- axes, 1.2 along the y-axis. |
| Plate | 2 | Increases by a rate of 1 along the x- and z- axes, 0.4 along the y-axis. |
| Custom | 3 | Increases by a rate as low as .001 along all axes. |