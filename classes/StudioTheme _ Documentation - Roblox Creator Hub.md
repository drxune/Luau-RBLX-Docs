# StudioTheme | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/StudioTheme
Scraped: 2026-01-11T02:36:49.279189Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- Instance
- StudioTheme
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [StudioTheme](/docs/reference/engine/classes/StudioTheme)

English

Feedback

Engine Class

StudioTheme

Not Creatable

Not Replicated

---

Summary

Methods

|  |
| --- |
| [GetColor](#GetColor)(styleguideitem: [Enum.StudioStyleGuideColor](/docs/reference/engine/enums/StudioStyleGuideColor),modifier: [Enum.StudioStyleGuideModifier](/docs/reference/engine/enums/StudioStyleGuideModifier)):[Color3](/docs/reference/engine/datatypes/Color3) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

---

API Reference

Methods

GetColor

Plugin Security

Returns the color corresponding to the arguments provided.

StudioTheme:GetColor(

styleguideitem:[Enum.StudioStyleGuideColor](/docs/reference/engine/enums/StudioStyleGuideColor), modifier:[Enum.StudioStyleGuideModifier](/docs/reference/engine/enums/StudioStyleGuideModifier)

):[Color3](/docs/reference/engine/datatypes/Color3)

Parameters

|  |
| --- |
| styleguideitem:[Enum.StudioStyleGuideColor](/docs/reference/engine/enums/StudioStyleGuideColor)  The element you want to get the theme color for. |
| modifier:[Enum.StudioStyleGuideModifier](/docs/reference/engine/enums/StudioStyleGuideModifier) Default Value: "Default" The modifier you want to place on the StyleGuideColor element. |

Returns

[Color3](/docs/reference/engine/datatypes/Color3)

The corresponding Color3 theme value.

The GetColor() function returns the [Color3](/docs/reference/engine/datatypes/Color3) corresponding to
the arguments provided. For instance, if you would like to get the
[Color3](/docs/reference/engine/datatypes/Color3) of the Studio "MainButton" when it's disabled, you
can use the following code:

```
settings().Studio.Theme:GetColor(Enum.StudioStyleGuideColor.MainButton, Enum.StudioStyleGuideModifier.Disabled)
```

See the [Enum.StudioStyleGuideColor](/docs/reference/engine/enums/StudioStyleGuideColor) reference for a list of Studio
elements and [Enum.StudioStyleGuideModifier](/docs/reference/engine/enums/StudioStyleGuideModifier) for a list of modifiers.

Provide feedback

---