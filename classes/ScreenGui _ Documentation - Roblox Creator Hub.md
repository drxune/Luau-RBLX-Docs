# ScreenGui | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ScreenGui
Scraped: 2026-01-11T02:41:07.360697Z

## Tags
- Not Replicated

## Inherits
- LayerCollector
- ScreenGui
- GuiBase2d
- Instance
- Object
- GuiMain
- GuiObjects
- PlayerGui
- StarterGui
- GuiObject
- ScreenInsets
- DisplayOrder
- UIStroke
- ClipToDeviceSafeArea
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [LayerCollector](/docs/reference/engine/classes/LayerCollector)
6. /
7. [ScreenGui](/docs/reference/engine/classes/ScreenGui)

English

Feedback

Engine Class

![ScreenGui](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/ScreenGui-Dark.webp)ScreenGui

Primary container of on-screen 2D user interface elements.

---

Summary

Properties

|  |
| --- |
| [ClipToDeviceSafeArea](#ClipToDeviceSafeArea):[boolean](/docs/luau/booleans) |
| [DisplayOrder](#DisplayOrder):[number](/docs/luau/numbers) |
| [IgnoreGuiInset](#IgnoreGuiInset):[boolean](/docs/luau/booleans) |
| [SafeAreaCompatibility](#SafeAreaCompatibility):[Enum.SafeAreaCompatibility](/docs/reference/engine/enums/SafeAreaCompatibility) |
| [ScreenInsets](#ScreenInsets):[Enum.ScreenInsets](/docs/reference/engine/enums/ScreenInsets) |

Inherited Members

4 inherited from [LayerCollector](/docs/reference/engine/classes/LayerCollector)

12 inherited from [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[GuiMain](/docs/reference/engine/classes/GuiMain)

[ScreenGui](/docs/reference/engine/classes/ScreenGui) is a storage container for 2D [GuiObjects](/docs/reference/engine/classes/GuiObject)
displayed on the user's screen. A [ScreenGui](/docs/reference/engine/classes/ScreenGui) only shows if parented to
a player's [PlayerGui](/docs/reference/engine/classes/PlayerGui); parenting a [ScreenGui](/docs/reference/engine/classes/ScreenGui) to
[StarterGui](/docs/reference/engine/classes/StarterGui) ensures it clones into each player's [PlayerGui](/docs/reference/engine/classes/PlayerGui) when
they join the experience and their character first spawns. See
[On‑Screen UI Containers](/docs/ui/on-screen-containers) for further
details.

![Example ScreenGui with various GuiObject children, including a Frame, TextLabel, TextBox, and ImageButton.](https://prod.docsiteassets.roblox.com/assets/ui/ui-objects/ScreenGui-Example.jpg)

For performance improvements, the appearance of a [ScreenGui](/docs/reference/engine/classes/ScreenGui) is cached
until one of the following events occurs:

* A descendant is added to or removed from it.
* A property of a descendant changes.
* A property of the [ScreenGui](/docs/reference/engine/classes/ScreenGui) itself changes.

If any of these events occur, the [ScreenGui](/docs/reference/engine/classes/ScreenGui) appearance is recomputed
on the next frame it gets rendered.

---

API Reference

Properties

ClipToDeviceSafeArea

Read Parallel

Whether to clip the contents of this [ScreenGui](/docs/reference/engine/classes/ScreenGui) to the device's
safe area.

ScreenGui.ClipToDeviceSafeArea:[boolean](/docs/luau/booleans)

If this property is true, all [GuiObject](/docs/reference/engine/classes/GuiObject) descendants of the
[ScreenGui](/docs/reference/engine/classes/ScreenGui) will be clipped to the device's safe area (see
[Enum.ScreenInsets](/docs/reference/engine/enums/ScreenInsets)). The default is true to maintain backwards
compatibility of UI that is intentionally hidden offscreen, such as
objects that slide into view from a screen edge when they're needed.

![Mobile device showing UI button clipped by device safe
area](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/ScreenGui/ClipToDeviceSafeArea-True.png)

If this property is false, [GuiObject](/docs/reference/engine/classes/GuiObject) descendants will not be
clipped to the device's safe area and may be obscured by the camera notch
or other screen cutouts.

![Mobile device showing UI button overflowing device safe
area, obscured by screen camera notch](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/ScreenGui/ClipToDeviceSafeArea-False.png)

Note that this property will be ignored if you set
[ScreenInsets](/docs/reference/engine/classes/ScreenGui#ScreenInsets) to [None](/docs/reference/engine/enums/ScreenInsets),
as doing so implies that you intentionally want to disregard the device's
safe insets.

Provide feedback

---

DisplayOrder

Read Parallel

Controls the Z-index order in which multiple [ScreenGui](/docs/reference/engine/classes/ScreenGui) containers
are drawn.

ScreenGui.DisplayOrder:[number](/docs/luau/numbers)

This property controls the Z-index order in which multiple
[ScreenGui](/docs/reference/engine/classes/ScreenGui) containers are drawn. Those with a higher
[DisplayOrder](/docs/reference/engine/classes/ScreenGui#DisplayOrder) will be drawn on top of those
with a lower value.

Provide feedback

---

IgnoreGuiInset

Not Replicated

Read Parallel

Determines whether the [ScreenGui](/docs/reference/engine/classes/ScreenGui) overflows into the range of
Roblox's core UI elements.

ScreenGui.IgnoreGuiInset:[boolean](/docs/luau/booleans)

If this property is false (default),
[ScreenInsets](/docs/reference/engine/classes/ScreenGui#ScreenInsets) is set to
[CoreUISafeInsets](/docs/reference/engine/enums/ScreenInsets), effectively keeping its bounds below
the Roblox top bar core UI.

If this property is changed to true and
[ScreenInsets](/docs/reference/engine/classes/ScreenGui#ScreenInsets) is currently set to
[CoreUISafeInsets](/docs/reference/engine/enums/ScreenInsets),
[ScreenInsets](/docs/reference/engine/classes/ScreenGui#ScreenInsets) will be set to
[DeviceSafeInsets](/docs/reference/engine/enums/ScreenInsets).

See [ScreenInsets](/docs/reference/engine/classes/ScreenGui#ScreenInsets) for details on how screen
insets affect the contents of a [ScreenGui](/docs/reference/engine/classes/ScreenGui).

Provide feedback

---

SafeAreaCompatibility

Read Parallel

Specifies whether automatic UI compatibility transformations are applied
to descendant "fullscreen" [GuiObjects](/docs/reference/engine/classes/GuiObject) on displays with
screen cutouts.

ScreenGui.SafeAreaCompatibility:[Enum.SafeAreaCompatibility](/docs/reference/engine/enums/SafeAreaCompatibility)

This property specifies whether automatic UI compatibility transformations
are applied to descendant "fullscreen" [GuiObjects](/docs/reference/engine/classes/GuiObject) of the
[ScreenGui](/docs/reference/engine/classes/ScreenGui) on displays with screen cutouts. Eligibility occurs if
the total area of the descendant [GuiObject](/docs/reference/engine/classes/GuiObject) (including any applied
border or [UIStroke](/docs/reference/engine/classes/UIStroke)) covers the device's safe area both
horizontally and vertically. See the [Enum.SafeAreaCompatibility](/docs/reference/engine/enums/SafeAreaCompatibility) enum
reference for details.

The default value is [FullscreenExtension](/docs/reference/engine/enums/SafeAreaCompatibility) in
order to automatically improve the appearance of UI that was authored for
screens without any cutouts. However, it's recommended that you avoid
fullscreen extensions for new work; instead, use the
[ScreenInsets](/docs/reference/engine/classes/ScreenGui#ScreenInsets) property to specify which
insets should be respected for different [ScreenGui](/docs/reference/engine/classes/ScreenGui) containers.

Note that descendant UI objects will continue to be clipped by the
device's safe area if
[ClipToDeviceSafeArea](/docs/reference/engine/classes/ScreenGui#ClipToDeviceSafeArea) is set to
true.

Provide feedback

---

ScreenInsets

Read Parallel

Controls the safe area insets that are applied to the contents of the
[ScreenGui](/docs/reference/engine/classes/ScreenGui).

ScreenGui.ScreenInsets:[Enum.ScreenInsets](/docs/reference/engine/enums/ScreenInsets)

This property controls the safe area insets that are applied to the
contents of the [ScreenGui](/docs/reference/engine/classes/ScreenGui).

The default of [CoreUISafeInsets](/docs/reference/engine/enums/ScreenInsets) keeps all descendant
[GuiObjects](/docs/reference/engine/classes/GuiObject) inside the core UI safe area, clear of the
Roblox top bar buttons and other screen cutouts like the device's camera
notch.

![Mobile device showing UI buttons inside core UI safe area](https://prod.docsiteassets.roblox.com/assets/engine-api/enums/ScreenInsets/CoreUISafeInsets.png)

If you set this property to [None](/docs/reference/engine/enums/ScreenInsets), UI objects may be
obscured behind core UI objects or device cutouts like the camera notch.
As a result, you should only use [None](/docs/reference/engine/enums/ScreenInsets) for a
[ScreenGui](/docs/reference/engine/classes/ScreenGui) that contains noninteractive content like background
images.

See
[On-Screen UI Containers](/docs/ui/on-screen-containers#screen-insets)
for alternative examples.

Provide feedback

---