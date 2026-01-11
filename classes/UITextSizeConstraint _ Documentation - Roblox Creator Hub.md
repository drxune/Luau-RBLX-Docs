# UITextSizeConstraint | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/UITextSizeConstraint
Scraped: 2026-01-11T02:39:20.767400Z

## Inherits
- UIConstraint
- UITextSizeConstraint
- GuiObject
- MaxTextSize
- MinTextSize
- Instance
- Object
- TextLabel
- TextButton
- TextBox
- TextLabel.TextScaled
- TextScaled
- UITextSizeConstraint.MaxTextSize
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [UIConstraint](/docs/reference/engine/classes/UIConstraint)
6. /
7. [UITextSizeConstraint](/docs/reference/engine/classes/UITextSizeConstraint)

English

Feedback

Engine Class

![UITextSizeConstraint](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/UITextSizeConstraint-Dark.webp)UITextSizeConstraint

Ensures that the size of text rendered by certain [GuiObject](/docs/reference/engine/classes/GuiObject) classes
lies within the range described by
[MaxTextSize](/docs/reference/engine/classes/UITextSizeConstraint#MaxTextSize) and
[MinTextSize](/docs/reference/engine/classes/UITextSizeConstraint#MinTextSize).

---

Summary

Properties

|  |
| --- |
| [MaxTextSize](#MaxTextSize):[number](/docs/luau/numbers) |
| [MinTextSize](#MinTextSize):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A UITextSizeConstraint ensures that the size of text rendered by certain
[GuiObject](/docs/reference/engine/classes/GuiObject) classes ([TextLabel](/docs/reference/engine/classes/TextLabel), [TextButton](/docs/reference/engine/classes/TextButton), or
[TextBox](/docs/reference/engine/classes/TextBox)) lies within the range described by
[MaxTextSize](/docs/reference/engine/classes/UITextSizeConstraint#MaxTextSize) and
[MinTextSize](/docs/reference/engine/classes/UITextSizeConstraint#MinTextSize). It is meant to be used
alongside [TextLabel.TextScaled](/docs/reference/engine/classes/TextLabel#TextScaled), which automatically scales text to
fill its containing object. Like other UI constraints, it is applied when
parented to the object to be constrained.

It's recommended that no values lower than 9 be used for
[MinTextSize](/docs/reference/engine/classes/UITextSizeConstraint#MinTextSize) property, otherwise text
may not be readable to most users.

---

API Reference

Properties

MaxTextSize

Read Parallel

The largest size in pixels the font is allowed to be.

UITextSizeConstraint.MaxTextSize:[number](/docs/luau/numbers)

This property indicates the largest size in pixels the font is allowed to
be. It defaults to 1000 pixels and much be set larger than or equal to the
[MinTextSize](/docs/reference/engine/classes/UITextSizeConstraint#MinTextSize) property.

If the affected [GuiObject](/docs/reference/engine/classes/GuiObject) has its
[TextScaled](/docs/reference/engine/classes/TextLabel#TextScaled) property set to true the text size
constrained by this property will scale dynamically with the container's
size. It will scale upwards with the GuiObject's size until the max size
is reached, at which point it will stay constant if the UI element
continues to grow.

Provide feedback

---

MinTextSize

Read Parallel

The smallest size in pixels the font is allowed to be.

UITextSizeConstraint.MinTextSize:[number](/docs/luau/numbers)

This property indicated the smallest size in pixels the font is allowed to
be. This value defaults to 1 pixel and must be set less than or equal to
[UITextSizeConstraint.MaxTextSize](/docs/reference/engine/classes/UITextSizeConstraint#MaxTextSize).

If the affected [GuiObject](/docs/reference/engine/classes/GuiObject) has its
[TextScaled](/docs/reference/engine/classes/TextLabel#TextScaled) property set to true the text size
constrained by this property will scale dynamically with the container's
size. It will scale downwards with the GuiObject's size until the min size
is reached, at which point it will stay constant if the UI element
continues to shrink.

Provide feedback

---