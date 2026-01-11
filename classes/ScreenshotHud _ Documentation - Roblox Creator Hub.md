# ScreenshotHud | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ScreenshotHud
Scraped: 2026-01-11T02:34:06.332526Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- Instance
- ScreenshotHud
- ScreenshotHud.ExperienceNameOverlayEnabled
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ScreenshotHud](/docs/reference/engine/classes/ScreenshotHud)

English

Feedback

Engine Class

ScreenshotHud

A 2D user interface that allows users to capture and save screenshots to their
local device.

Not Creatable

Not Replicated

---

Summary

Properties

|  |
| --- |
| [CameraButtonIcon](#CameraButtonIcon):ContentId |
| [CameraButtonPosition](#CameraButtonPosition):[UDim2](/docs/reference/engine/datatypes/UDim2) |
| [CloseButtonPosition](#CloseButtonPosition):[UDim2](/docs/reference/engine/datatypes/UDim2) |
| [CloseWhenScreenshotTaken](#CloseWhenScreenshotTaken):[boolean](/docs/luau/booleans) |
| [ExperienceNameOverlayEnabled](#ExperienceNameOverlayEnabled):[boolean](/docs/luau/booleans)  Deprecated |
| [HideCoreGuiForCaptures](#HideCoreGuiForCaptures):[boolean](/docs/luau/booleans) |
| [HidePlayerGuiForCaptures](#HidePlayerGuiForCaptures):[boolean](/docs/luau/booleans) |
| [OverlayFont](#OverlayFont):[Enum.Font](/docs/reference/engine/enums/Font)  Deprecated |
| [UsernameOverlayEnabled](#UsernameOverlayEnabled):[boolean](/docs/luau/booleans)  Deprecated |
| [Visible](#Visible):[boolean](/docs/luau/booleans) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The [ScreenshotHud](/docs/reference/engine/classes/ScreenshotHud) is a 2D user interface that allows users to capture
and save screenshots to their local device. It consists of the following UI
elements:

* An overlay containing the experience name and Roblox branding. These remain
  on screen when a screenshot is taken, although the experience name can be
  disabled through the [ScreenshotHud.ExperienceNameOverlayEnabled](/docs/reference/engine/classes/ScreenshotHud#ExperienceNameOverlayEnabled)
  property.
* A camera button that hides all UI except for the overlay and takes a
  screenshot.
* A close button that closes the [ScreenshotHud](/docs/reference/engine/classes/ScreenshotHud).

![](https://prod.docsiteassets.roblox.com/assets/engine-api/classes/ScreenshotHud/Diagram.jpg)

Code Samples

LocalScript

```
local GuiService = game:GetService("GuiService")



local screenshotHud = GuiService:WaitForChild("ScreenshotHud")



screenshotHud.ExperienceNameOverlayEnabled = true



screenshotHud.OverlayFont = Enum.Font.GothamMedium



screenshotHud.Visible = true
```

---

API Reference

Properties

CameraButtonIcon

Read Parallel

Asset ID of the icon used for the camera button.

ScreenshotHud.CameraButtonIcon:ContentId

Asset ID of the icon used for the camera button.

Provide feedback

---

CameraButtonPosition

Read Parallel

Screen location of the camera button.

ScreenshotHud.CameraButtonPosition:[UDim2](/docs/reference/engine/datatypes/UDim2)

Screen location of the camera button.

Provide feedback

---

CloseButtonPosition

Read Parallel

Screen location of the close button.

ScreenshotHud.CloseButtonPosition:[UDim2](/docs/reference/engine/datatypes/UDim2)

Screen location of the close button.

Provide feedback

---

CloseWhenScreenshotTaken

Read Parallel

Whether the [ScreenshotHud](/docs/reference/engine/classes/ScreenshotHud) closes automatically when a screenshot
is taken.

ScreenshotHud.CloseWhenScreenshotTaken:[boolean](/docs/luau/booleans)

Determines whether the [ScreenshotHud](/docs/reference/engine/classes/ScreenshotHud) closes automatically when a
screenshot is taken.

Provide feedback

---

ExperienceNameOverlayEnabled

Deprecated

Show details

---

HideCoreGuiForCaptures

Read Parallel

ScreenshotHud.HideCoreGuiForCaptures:[boolean](/docs/luau/booleans)

Provide feedback

---

HidePlayerGuiForCaptures

Read Parallel

ScreenshotHud.HidePlayerGuiForCaptures:[boolean](/docs/luau/booleans)

Provide feedback

---

OverlayFont

Deprecated

Show details

---

UsernameOverlayEnabled

Deprecated

Show details

---

Visible

Read Parallel

Determines whether the [ScreenshotHud](/docs/reference/engine/classes/ScreenshotHud) is visible.

ScreenshotHud.Visible:[boolean](/docs/luau/booleans)

Determines whether the [ScreenshotHud](/docs/reference/engine/classes/ScreenshotHud) is visible.

Provide feedback

---