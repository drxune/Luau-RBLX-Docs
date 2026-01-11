# ButtonStyle | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/ButtonStyle
Scraped: 2026-01-11T02:42:59.670693Z

## Inherits
- GuiButton.Style
- GuiObject.BorderColor3
- GuiObject.BackgroundColor3
1. [Enums](/docs/reference/engine/enums)
2. /
3. [ButtonStyle](/docs/reference/engine/enums/ButtonStyle)

English

Feedback

Engine Enum

ButtonStyle

---

Used by [GuiButton.Style](/docs/reference/engine/classes/GuiButton#Style) to set a special hardcoded appearance.

These should generally be avoided in favor of setting other appearance
properties, but they can be useful for wireframing.

Despite the Roblox naming, these are not used by any official Roblox UI.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Custom | 0 | The button will respect the [GuiObject.BorderColor3](/docs/reference/engine/classes/GuiObject#BorderColor3) and [GuiObject.BackgroundColor3](/docs/reference/engine/classes/GuiObject#BackgroundColor3) properties. |
| RobloxButtonDefault | 1 | A black background with a red border, and rounded corners. |
| RobloxButton | 2 | A black background with a grey border, and rounded corners. |
| RobloxRoundButton | 3 | A grey background with rounded corners, and a slight drop shadow. |
| RobloxRoundDefaultButton | 4 | A blue background with rounded corners, and a slight drop shadow. |
| RobloxRoundDropdownButton | 5 | A white background with a thin grey border, rounded corners, and a slight drop shadow. |