# SafeAreaCompatibility | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/SafeAreaCompatibility
Scraped: 2026-01-11T02:45:21.332290Z

## Inherits
- GuiObjects
- ScreenGui
- GuiObject
- UIStroke
- ImageLabel
- ImageButton
- VideoFrame
- ScreenInsets
- ScreenGuis
1. [Enums](/docs/reference/engine/enums)
2. /
3. [SafeAreaCompatibility](/docs/reference/engine/enums/SafeAreaCompatibility)

English

Feedback

Engine Enum

SafeAreaCompatibility

---

This enum describes the automatic compatibility transformations that apply to
descendant "fullscreen" [GuiObjects](/docs/reference/engine/classes/GuiObject) of a [ScreenGui](/docs/reference/engine/classes/ScreenGui) on
displays with screen cutouts.

Items

| Name | Value | Summary |
| --- | --- | --- |
| None | 0 | Do not apply compatibility transformations to any descendants of the [ScreenGui](/docs/reference/engine/classes/ScreenGui). |
| FullscreenExtension | 1 | If the total area of any descendant [GuiObject](/docs/reference/engine/classes/GuiObject) within the [ScreenGui](/docs/reference/engine/classes/ScreenGui) (including any applied border or [UIStroke](/docs/reference/engine/classes/UIStroke)) covers the device's safe area both horizontally and vertically, its background area will be expanded to cover the fullscreen area. This expansion does not affect the size or position of the descendant's content, except in the case of [ImageLabel](/docs/reference/engine/classes/ImageLabel), [ImageButton](/docs/reference/engine/classes/ImageButton), or [VideoFrame](/docs/reference/engine/classes/VideoFrame) where the image/video is considered part of the background and will be expanded to fullscreen.  Note that this option is intended to automatically improve the appearance of UI that was authored for screens without any cutouts. However, it's recommended that you avoid fullscreen extensions for new work; instead, use the [ScreenInsets](/docs/reference/engine/classes/ScreenGui#ScreenInsets) property to specify which insets should be respected for different [ScreenGuis](/docs/reference/engine/classes/ScreenGui). |