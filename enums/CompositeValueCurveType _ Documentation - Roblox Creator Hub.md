# CompositeValueCurveType | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/CompositeValueCurveType
Scraped: 2026-01-11T02:45:01.357531Z

## Inherits
- CompositeValueCurve
- FloatCurve
- CompositeValueCurve:GetValueAtTime()
1. [Enums](/docs/reference/engine/enums)
2. /
3. [CompositeValueCurveType](/docs/reference/engine/enums/CompositeValueCurveType)

English

Feedback

Engine Enum

CompositeValueCurveType

---

Describes the type of value animated by a [CompositeValueCurve](/docs/reference/engine/classes/CompositeValueCurve).

Items

| Name | Value | Summary |
| --- | --- | --- |
| ColorRGB | 0 | The [CompositeValueCurve](/docs/reference/engine/classes/CompositeValueCurve) will animate children of type [FloatCurve](/docs/reference/engine/classes/FloatCurve) named "R", "G", and "B" to animate the corresponding components of the [Color3](/docs/reference/engine/datatypes/Color3) value returned by the method [CompositeValueCurve:GetValueAtTime()](/docs/reference/engine/classes/CompositeValueCurve#GetValueAtTime). |
| ColorHSV | 1 | The [CompositeValueCurve](/docs/reference/engine/classes/CompositeValueCurve) will animate children of type [FloatCurve](/docs/reference/engine/classes/FloatCurve) named "H", "S", and "V" to animate hue, saturation, and value of a color that will be converted to RGB before returning a [Color3](/docs/reference/engine/datatypes/Color3) value from the method [CompositeValueCurve:GetValueAtTime()](/docs/reference/engine/classes/CompositeValueCurve#GetValueAtTime). |
| NumberRange | 2 | The [CompositeValueCurve](/docs/reference/engine/classes/CompositeValueCurve) will animate children of type [FloatCurve](/docs/reference/engine/classes/FloatCurve) named "Min" and "Max" to animate the corresponding components of the [NumberRange](/docs/reference/engine/datatypes/NumberRange) value returned by the method [CompositeValueCurve:GetValueAtTime()](/docs/reference/engine/classes/CompositeValueCurve#GetValueAtTime). |
| Rect | 3 | The [CompositeValueCurve](/docs/reference/engine/classes/CompositeValueCurve) will animate children of type [FloatCurve](/docs/reference/engine/classes/FloatCurve) named "MinX", "MaxX", "MinY", and "MaxY" to animate the corresponding components of the [Rect](/docs/reference/engine/datatypes/Rect) value returned by the method [CompositeValueCurve:GetValueAtTime()](/docs/reference/engine/classes/CompositeValueCurve#GetValueAtTime). |
| UDim | 4 | The [CompositeValueCurve](/docs/reference/engine/classes/CompositeValueCurve) will animate children of type [FloatCurve](/docs/reference/engine/classes/FloatCurve) named "Scale" and "Offset" to animate the corresponding components of the [UDim](/docs/reference/engine/datatypes/UDim) value returned by the method [CompositeValueCurve:GetValueAtTime()](/docs/reference/engine/classes/CompositeValueCurve#GetValueAtTime). |
| UDim2 | 5 | The [CompositeValueCurve](/docs/reference/engine/classes/CompositeValueCurve) will animate children of type [FloatCurve](/docs/reference/engine/classes/FloatCurve) named "ScaleX", "OffsetX", "ScaleY", and "OffsetY" to animate the corresponding components of the [UDim2](/docs/reference/engine/datatypes/UDim2) value returned by the method [CompositeValueCurve:GetValueAtTime()](/docs/reference/engine/classes/CompositeValueCurve#GetValueAtTime). |
| Vector2 | 6 | The [CompositeValueCurve](/docs/reference/engine/classes/CompositeValueCurve) will animate children of type [FloatCurve](/docs/reference/engine/classes/FloatCurve) named "X" and "Y" to animate the corresponding components of the [Vector2](/docs/reference/engine/datatypes/Vector2) value returned by the method [CompositeValueCurve:GetValueAtTime()](/docs/reference/engine/classes/CompositeValueCurve#GetValueAtTime). |
| Vector3 | 7 | The [CompositeValueCurve](/docs/reference/engine/classes/CompositeValueCurve) will animate children of type [FloatCurve](/docs/reference/engine/classes/FloatCurve) named "X", "Y", and "Z" to animate the corresponding components of the [Vector3](/docs/reference/engine/datatypes/Vector3) value returned by the method [CompositeValueCurve:GetValueAtTime()](/docs/reference/engine/classes/CompositeValueCurve#GetValueAtTime). |