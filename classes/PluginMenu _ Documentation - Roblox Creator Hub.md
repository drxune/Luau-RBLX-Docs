# PluginMenu | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/PluginMenu
Scraped: 2026-01-11T02:29:09.339533Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- Instance
- PluginMenu
- PluginActions
- Plugin:CreatePluginMenu()
- PluginMenus
- Plugin
- BoolValue
- Title
- Icon
- PluginAction
- PluginAction.Triggered
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [PluginMenu](/docs/reference/engine/classes/PluginMenu)

English

Feedback

Engine Class

PluginMenu

A context menu that can be shown in Studio. Displays a list of
[PluginActions](/docs/reference/engine/classes/PluginAction) and supports submenus.

Not Creatable

Not Replicated

---

Summary

Properties

|  |
| --- |
| [Icon](#Icon):[string](/docs/luau/strings) |
| [Title](#Title):[string](/docs/luau/strings) |

Methods

|  |
| --- |
| [AddAction](#AddAction)(action: [Instance](/docs/reference/engine/datatypes/Instance)):() |
| [AddMenu](#AddMenu)(menu: [Instance](/docs/reference/engine/datatypes/Instance)):() |
| [AddNewAction](#AddNewAction)(actionId: [string](/docs/luau/strings),text: [string](/docs/luau/strings),icon: [string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [AddSeparator](#AddSeparator)():() |
| [Clear](#Clear)():() |
| [ShowAsync](#ShowAsync)():[Instance](/docs/reference/engine/datatypes/Instance) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

PluginMenu represents a context menu which can be shown in Studio to display
a list of [PluginActions](/docs/reference/engine/classes/PluginAction) and which also supports submenus.
A PluginMenu must be created using the [Plugin:CreatePluginMenu()](/docs/reference/engine/classes/Plugin#CreatePluginMenu)
method in order to work as expected.

Code Samples

Creating a PluginMenu and PluginMenuAction

This code sample visualizes how [PluginMenus](/docs/reference/engine/classes/PluginMenu) and
[PluginActions](/docs/reference/engine/classes/PluginAction) behave when created for a [Plugin](/docs/reference/engine/classes/Plugin).
Outside of this example, you should not parent the plugin or its functional
components to the experience's workspace.

After executing the code, changing the created [BoolValue](/docs/reference/engine/classes/BoolValue) in the
experience's workspace opens the plugin's menus. Selecting an action from the
menus the function connected to the trigger signal.

```
-- This code can be pasted into the Command Bar, but only once



local pluginMenu = plugin:CreatePluginMenu(math.random(), "Test Menu")



pluginMenu.Name = "Test Menu"



pluginMenu:AddNewAction("ActionA", "A", "rbxasset://textures/loading/robloxTiltRed.png")



pluginMenu:AddNewAction("ActionB", "B", "rbxasset://textures/loading/robloxTilt.png")



local subMenu = plugin:CreatePluginMenu(math.random(), "C", "rbxasset://textures/explosion.png")



subMenu.Name = "Sub Menu"



subMenu:AddNewAction("ActionD", "D", "rbxasset://textures/whiteCircle.png")



subMenu:AddNewAction("ActionE", "E", "rbxasset://textures/icon_ROBUX.png")



pluginMenu:AddMenu(subMenu)



pluginMenu:AddSeparator()



pluginMenu:AddNewAction("ActionF", "F", "rbxasset://textures/sparkle.png")



local toggle = Instance.new("BoolValue")



toggle.Name = "TogglePluginMenu"



toggle.Parent = workspace



local function onToggled()



if toggle.Value then



toggle.Value = false



local selectedAction = pluginMenu:ShowAsync()



if selectedAction then



print("Selected Action:", selectedAction.Text, "with ActionId:", selectedAction.ActionId)



else



print("User did not select an action!")



end



end



end



toggle.Changed:Connect(onToggled)
```

---

API Reference

Properties

Icon

Not Replicated

Read Parallel

The icon to be displayed when used as a submenu.

PluginMenu.Icon:[string](/docs/luau/strings)

This property determines the icon to be displayed when used as a submenu.
It defaults to an empty string "".

Provide feedback

---

Title

Not Replicated

Read Parallel

The text to be displayed when used as a submenu.

PluginMenu.Title:[string](/docs/luau/strings)

This property determines the text to be displayed when a
[PluginMenu](/docs/reference/engine/classes/PluginMenu) is used as a submenu. It defaults to an empty string
"".

Provide feedback

---

Methods

AddAction

Plugin Security

Adds the given action to the menu.

PluginMenu:AddAction(action:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| action:[Instance](/docs/reference/engine/datatypes/Instance)  The action to add. |

Returns

()

Adds the given action to the menu.

Provide feedback

---

AddMenu

Plugin Security

Adds the given menu as a separator.

PluginMenu:AddMenu(menu:[Instance](/docs/reference/engine/datatypes/Instance)):()

Parameters

|  |
| --- |
| menu:[Instance](/docs/reference/engine/datatypes/Instance)  The menu to add as a submenu. Uses its [Title](/docs/reference/engine/classes/PluginMenu#Title) and [Icon](/docs/reference/engine/classes/PluginMenu#Icon) to display. |

Returns

()

Adds the given menu as a separator.

Provide feedback

---

AddNewAction

Plugin Security

Creates a temporary action that is hidden from Studio's customize
shortcuts window.

PluginMenu:AddNewAction(

actionId:[string](/docs/luau/strings), text:[string](/docs/luau/strings), icon:[string](/docs/luau/strings)

):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| actionId:[string](/docs/luau/strings)  Must be a unique string that identifies this [PluginAction](/docs/reference/engine/classes/PluginAction) from others. |
| text:[string](/docs/luau/strings)  The text to be displayed. |
| icon:[string](/docs/luau/strings)  The icon to be displayed. |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

The created [PluginAction](/docs/reference/engine/classes/PluginAction).

Creates a temporary action that is hidden from Studio's File ⟩
Customize Shortcuts window.

Provide feedback

---

AddSeparator

Plugin Security

Adds a separator between items in the menu.

PluginMenu:AddSeparator():()

Returns

()

Adds a separator between items in the menu.

Provide feedback

---

Clear

Plugin Security

Clears the menu.

PluginMenu:Clear():()

Returns

()

Clears the menu.

Provide feedback

---

ShowAsync

Yields

Plugin Security

Shows the menu at the mouse cursor. Yields until either an item is
selected or the menu is closed.

PluginMenu:ShowAsync():[Instance](/docs/reference/engine/datatypes/Instance)

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

The [PluginAction](/docs/reference/engine/classes/PluginAction) item that was selected or nil.

Shows the menu at the mouse cursor. It yields until either an item is
selected or the menu is closed. The selected action fires its
[PluginAction.Triggered](/docs/reference/engine/classes/PluginAction#Triggered) event.

Provide feedback

---