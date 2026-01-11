# KeyInterpolationMode | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/KeyInterpolationMode
Scraped: 2026-01-11T02:45:46.311642Z

## Inherits
- FloatCurve
- RotationCurve
1. [Enums](/docs/reference/engine/enums)
2. /
3. [KeyInterpolationMode](/docs/reference/engine/enums/KeyInterpolationMode)

English

Feedback

Engine Enum

KeyInterpolationMode

---

Describes the interpolation method for a [FloatCurve](/docs/reference/engine/classes/FloatCurve) or
[RotationCurve](/docs/reference/engine/classes/RotationCurve) segment between the key for which this mode is set and
the next key in the curve.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Constant | 0 | The segment starting at this key will constantly evaluate to the value set at this key. |
| Linear | 1 | The segment starting at this key will evaluate using a linear interpolation at this key and the value at the next key. |
| Cubic | 2 | The segment starting at this key will evaluate using cubic interpolation of this key value using its right tangent and the next key value and its left tangent. |