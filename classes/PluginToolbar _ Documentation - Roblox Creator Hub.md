# PluginToolbar | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/PluginToolbar
Scraped: 2026-01-11T02:40:24.174130Z

## Tags
- Not Creatable

## Inherits
- Object
- Instance
- PluginToolbar
- PluginToolbarButton
- Plugin:CreateToolbar()
- PluginToolbarButtons
- Click
- ServerScriptService
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [PluginToolbar](/docs/reference/engine/classes/PluginToolbar)

English

Feedback

Engine Class

PluginToolbar

Not Creatable

---

Summary

Methods

|  |
| --- |
| [CreateButton](#CreateButton)(buttonId: [string](/docs/luau/strings),tooltip: [string](/docs/luau/strings),iconname: [string](/docs/luau/strings),text: [string](/docs/luau/strings)):[PluginToolbarButton](/docs/reference/engine/classes/PluginToolbarButton) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A PluginToolbar object is created by calling the
[Plugin:CreateToolbar()](/docs/reference/engine/classes/Plugin#CreateToolbar) method and is used to contain
[PluginToolbarButtons](/docs/reference/engine/classes/PluginToolbarButton).

---

API Reference

Methods

CreateButton

Plugin Security

Creates a [PluginToolbarButton](/docs/reference/engine/classes/PluginToolbarButton) that allows the user to initiate a
single, one-off action in Studio.

PluginToolbar:CreateButton(

buttonId:[string](/docs/luau/strings), tooltip:[string](/docs/luau/strings), iconname:[string](/docs/luau/strings), text:[string](/docs/luau/strings)

):[PluginToolbarButton](/docs/reference/engine/classes/PluginToolbarButton)

Parameters

|  |
| --- |
| buttonId:[string](/docs/luau/strings)  A unique button ID. |
| tooltip:[string](/docs/luau/strings)  The text displayed in the tooltip shown when a user hovers over the button. |
| iconname:[string](/docs/luau/strings)  The asset ID of the icon displayed in the button. |
| text:[string](/docs/luau/strings)  Optional text displayed under the button icon. |

Returns

[PluginToolbarButton](/docs/reference/engine/classes/PluginToolbarButton)

The created [PluginToolbarButton](/docs/reference/engine/classes/PluginToolbarButton) instance.

Creates a [PluginToolbarButton](/docs/reference/engine/classes/PluginToolbarButton) that allows the user to initiate a
single, one-off action in Studio through its
[Click](/docs/reference/engine/classes/PluginToolbarButton#Click) event.

Code Samples

Adding a Plugin Toolbar Button

Creates a custom toolbar and Plugins menu folder
containing a button that, when clicked, inserts an empty script in
[ServerScriptService](/docs/reference/engine/classes/ServerScriptService).

```
local ServerScriptService = game:GetService("ServerScriptService")



-- Create a new toolbar section and Plugins menu folder titled "Custom"



local toolbar = plugin:CreateToolbar("Custom")



-- Add a toolbar button labeled "Empty Script"



local newScriptButton = toolbar:CreateButton("Empty Script", "Create an empty script", "rbxassetid://14978048121")



-- Make button clickable even if 3D viewport is hidden



newScriptButton.ClickableWhenViewportHidden = true



local function onPluginButtonClicked()



local newScript = Instance.new("Script")



newScript.Source = ""



newScript.Parent = ServerScriptService



end



newScriptButton.Click:Connect(onPluginButtonClicked)
```

Provide feedback

---