# UIFlexAlignment | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/UIFlexAlignment
Scraped: 2026-01-11T02:44:29.713627Z

## Inherits
- UIListLayout
- HorizontalFlex
- VerticalFlex
1. [Enums](/docs/reference/engine/enums)
2. /
3. [UIFlexAlignment](/docs/reference/engine/enums/UIFlexAlignment)

English

Feedback

Engine Enum

UIFlexAlignment

---

In a [UIListLayout](/docs/reference/engine/classes/UIListLayout) flex layout, specifies how to distribute extra
horizontal space in a [HorizontalFlex](/docs/reference/engine/classes/UIListLayout#HorizontalFlex)
layout or vertical space in a [VerticalFlex](/docs/reference/engine/classes/UIListLayout#VerticalFlex)
layout.

Items

| Name | Value | Summary |
| --- | --- | --- |
| None | 0 | No flex behavior; siblings maintain their defined width or height. |
| Fill | 1 | Siblings resize to fill the entire parent container, overriding their defined width or height. |
| SpaceAround | 2 | Siblings maintain their defined width or height. Equal spacing is added on both sides of each sibling. |
| SpaceBetween | 3 | Siblings maintain their defined width or height. Equal spacing is added between siblings, but no additional space is added around siblings. |
| SpaceEvenly | 4 | Siblings maintain their defined width or height. Equal spacing is added both between and around siblings. |