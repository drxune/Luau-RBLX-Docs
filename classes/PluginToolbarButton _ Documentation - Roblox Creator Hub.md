# PluginToolbarButton | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/PluginToolbarButton
Scraped: 2026-01-11T02:35:54.962439Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Instance
- PluginToolbarButton
- Object
- PluginToolbar:CreateButton()
- Click
- SetActive()
- Plugin:Activate()
- PluginToolbars
- Plugin:Deactivate()
- Enabled
- ClickableWhenViewportHidden
- Script
- Workspace
- BrickColor()
- Selection.SelectionChanged
- PluginToolbarButton.Click
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [PluginToolbarButton](/docs/reference/engine/classes/PluginToolbarButton)

English

Feedback

Engine Class

PluginToolbarButton

Not Creatable

---

Summary

Properties

|  |
| --- |
| [ClickableWhenViewportHidden](#ClickableWhenViewportHidden):[boolean](/docs/luau/booleans) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [Icon](#Icon):ContentId |

Methods

|  |
| --- |
| [SetActive](#SetActive)(active: [boolean](/docs/luau/booleans)):() |

Events

|  |
| --- |
| [Click](#Click)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A PluginToolbarButton object is created through the
[PluginToolbar:CreateButton()](/docs/reference/engine/classes/PluginToolbar#CreateButton) function. It allows the user to initiate
a single, one-off action in Roblox Studio through the
[Click](/docs/reference/engine/classes/PluginToolbarButton#Click) event. Toolbar buttons can also be
assigned a keyboard shortcut through Studio's File ⟩ Customize
Shortcuts window.

When pressed, the [Click](/docs/reference/engine/classes/PluginToolbarButton#Click) event fires. A
button will also remain in the pressed state, which may be set manually using
[SetActive()](/docs/reference/engine/classes/PluginToolbarButton#SetActive). Upon plugin activation
([Plugin:Activate()](/docs/reference/engine/classes/Plugin#Activate)), buttons in all other
[PluginToolbars](/docs/reference/engine/classes/PluginToolbar) will be toggled off. If all buttons in a
toolbar are off, the toolbar's plugin is deactivated
([Plugin:Deactivate()](/docs/reference/engine/classes/Plugin#Deactivate)).

When the game viewport is not visible, buttons will be disabled as if their
[Enabled](/docs/reference/engine/classes/PluginToolbarButton#Enabled) property were false. Disabled
buttons are desaturated and do not respond to user clicks. By setting
[ClickableWhenViewportHidden](/docs/reference/engine/classes/PluginToolbarButton#ClickableWhenViewportHidden)
to true, you can allow plugin buttons to remain clickable, such as during
script editing.

---

API Reference

Properties

ClickableWhenViewportHidden

Not Replicated

Read Parallel

Determines whether the button can be clicked when the 3D viewport is
hidden, such as when a [Script](/docs/reference/engine/classes/Script) is being edited in another tab.

PluginToolbarButton.ClickableWhenViewportHidden:[boolean](/docs/luau/booleans)

This property determines whether a [PluginToolbarButton](/docs/reference/engine/classes/PluginToolbarButton) may be
clicked while the 3D viewport is hidden, such as when a [Script](/docs/reference/engine/classes/Script) is
being edited in another tab.

Typically, this property should be enabled if an action triggered by a
plugin button's [Click](/docs/reference/engine/classes/PluginToolbarButton#Click) event doesn't
occur in the 3D world ([Workspace](/docs/reference/engine/classes/Workspace)). For example, a button that
opens a widget should have this property as true, since showing a widget
is visible to the user even if the 3D view isn't visible.

Provide feedback

---

Enabled

Not Replicated

Read Parallel

Determines whether the button is clickable in general.

PluginToolbarButton.Enabled:[boolean](/docs/luau/booleans)

This property determines whether a button is clickable in general. When
false, the button will be greyed out and unclickable, preventing the
user from firing the [Click](/docs/reference/engine/classes/PluginToolbarButton#Click) event.
Buttons are enabled by default.

When re-enabling this property, the plugin button's state won't be
remembered from the previous state in which the user left the button in.
Instead, it will default to the last state set by
[SetActive()](/docs/reference/engine/classes/PluginToolbarButton#SetActive) or to the inactive
state if [SetActive()](/docs/reference/engine/classes/PluginToolbarButton#SetActive) was never
used.

Plugins should disable their buttons when the button action isn't relevant
in the current context. For example, a plugin button that assigns random
colors to selected should not be enabled when the selection contains no
parts.

See also
[ClickableWhenViewportHidden](/docs/reference/engine/classes/PluginToolbarButton#ClickableWhenViewportHidden)
which determines whether a button is clickable when the game view is
hidden (and not just in general).

Code Samples

BrickColor Randomizer Plugin

This code sample is for a studio Plugin. The plugin creates a
PluginToolbarButton which randomizes the
[BrickColor()](/docs/reference/engine/classes/BasePart#BrickColor) of each selected part using
BrickColor.random(). Furthermore, the button is only enabled if at least one
part is selected. It does this by detecting changes in the Selection using
[Selection.SelectionChanged](/docs/reference/engine/classes/Selection#SelectionChanged).

```
assert(plugin, "This script must be run as a plugin")



local Selection = game:GetService("Selection")



local toolbar = plugin:CreateToolbar("Parts")



local pluginToolbarButton = toolbar:CreateButton(



"Randomize Colors",



"Click this button to assign random colors to selected parts",



"rbxassetid://5325741572" -- A rainbow



)



local function onClick()



local selection = Selection:Get()



for _, object in pairs(selection) do



if object:IsA("BasePart") then



object.BrickColor = BrickColor.random()



end



end



end



pluginToolbarButton.Click:Connect(onClick)



local function doesSelectionContainAPart()



local selection = Selection:Get()



for _, object in pairs(selection) do



if object:IsA("BasePart") then



return true



end



end



return false



end



local function onSelectionChanged()



pluginToolbarButton.Enabled = doesSelectionContainAPart()



end



Selection.SelectionChanged:Connect(onSelectionChanged)



onSelectionChanged()
```

Provide feedback

---

Icon

Not Replicated

Read Parallel

Determines what icon should represent the button.

PluginToolbarButton.Icon:ContentId

This property determines which [Content](/docs/reference/engine/datatypes/Content) should be shown for the
button's icon in the toolbar. When this property is not set, the button
will instead use the button's text given by
[PluginToolbar:CreateButton()](/docs/reference/engine/classes/PluginToolbar#CreateButton).

Provide feedback

---

Methods

SetActive

Plugin Security

Sets the state of the plugin button.

PluginToolbarButton:SetActive(active:[boolean](/docs/luau/booleans)):()

Parameters

|  |
| --- |
| active:[boolean](/docs/luau/booleans) |

Returns

()

This method can be used to manually set the active state of the plugin
button.

When the [Enabled](/docs/reference/engine/classes/PluginToolbarButton#Enabled) property is toggled
back on, the button will either revert to the last state set by this
method or default to inactive if this method hasn't been used previously.

Provide feedback

---

Events

Click

Plugin Security

Fires when the user presses and releases their cursor on the button.

PluginToolbarButton.Click():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires when the [PluginToolbarButton](/docs/reference/engine/classes/PluginToolbarButton) is pressed and
released by the user.

See also [SetActive()](/docs/reference/engine/classes/PluginToolbarButton#SetActive) to manually
set the state of the button.

Code Samples

PluginToolbarButton.Click

This code sample demonstrates creating a PluginToolbar and a
PluginToolbarButton on it, then connecting a function onClick to the
[PluginToolbarButton.Click](/docs/reference/engine/classes/PluginToolbarButton#Click) event. When pressed, the button will print
"Hello, world" to the output.

```
assert(plugin, "This script must be run as a plugin")



local toolbar = plugin:CreateToolbar("Hello World Plugin Toolbar")



local pluginToolbarButton =



toolbar:CreateButton("Print Hello World", "Click this button to print Hello World!", "rbxassetid://133293265")



local function onClick()



print("Hello, world")



end



pluginToolbarButton.Click:Connect(onClick)
```

Provide feedback

---