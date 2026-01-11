# Plugin | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Plugin
Scraped: 2026-01-11T02:31:56.008759Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- Instance
- Plugin
- DockWidgetPluginGui
- PluginAction
- PluginMenu
- PluginToolbar
- PluginMouse
- LuaSourceContainer
- Script
- ModuleScripts
- ModuleScript
- GetMouse()
- Deactivation
- IsActivatedWithExclusiveMouse()
- Unloading
- PluginToolbarButton
- CreatePluginMenu()
- PluginActions
- Plugin:CreatePluginAction()
- Triggered
- PluginMenus
- BoolValue
- Activate()
- Mouse
- KeyframeSequence
- Workspace
- IntersectOperation
- NegateOperations
- BasePart API page
- UnionOperations
- GetSetting()
- Plugin:GetSetting()
- Plugin:SetSetting()
- PluginGui.PluginDragEntered
- PluginGui.PluginDragMoved
- PluginGui.PluginDragDropped
- PluginGui.PluginDragLeft
- TextBox
- TextButton
- UnionOperation
- Deactivate()
- DataModel
- PluginToolbarButtons
- DockWidgetPluginGuis
- PluginGuis
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Plugin](/docs/reference/engine/classes/Plugin)

English

Feedback

Engine Class

Plugin

Not Creatable

---

Summary

Properties

|  |
| --- |
| [CollisionEnabled](#CollisionEnabled):[boolean](/docs/luau/booleans) |
| [DisableUIDragDetectorDrags](#DisableUIDragDetectorDrags):[boolean](/docs/luau/booleans) |
| [GridSize](#GridSize):[number](/docs/luau/numbers) |
| [IsDebuggable](#IsDebuggable):[boolean](/docs/luau/booleans) |

Methods

|  |
| --- |
| [Activate](#Activate)(exclusiveMouse: [boolean](/docs/luau/booleans)):() |
| [CreateDockWidgetPluginGuiAsync](#CreateDockWidgetPluginGuiAsync)(pluginGuiId: [string](/docs/luau/strings),dockWidgetPluginGuiInfo: [DockWidgetPluginGuiInfo](/docs/reference/engine/datatypes/DockWidgetPluginGuiInfo)):[DockWidgetPluginGui](/docs/reference/engine/classes/DockWidgetPluginGui) |
| [CreateDockWidgetPluginGui](#CreateDockWidgetPluginGui)(pluginGuiId: [string](/docs/luau/strings),dockWidgetPluginGuiInfo: [DockWidgetPluginGuiInfo](/docs/reference/engine/datatypes/DockWidgetPluginGuiInfo)):[DockWidgetPluginGui](/docs/reference/engine/classes/DockWidgetPluginGui)  Deprecated |
| [CreatePluginAction](#CreatePluginAction)(actionId: [string](/docs/luau/strings),text: [string](/docs/luau/strings),statusTip: [string](/docs/luau/strings),iconName: [string](/docs/luau/strings),allowBinding: [boolean](/docs/luau/booleans)):[PluginAction](/docs/reference/engine/classes/PluginAction) |
| [CreatePluginMenu](#CreatePluginMenu)(id: [string](/docs/luau/strings),title: [string](/docs/luau/strings),icon: [string](/docs/luau/strings)):[PluginMenu](/docs/reference/engine/classes/PluginMenu) |
| [CreateToolbar](#CreateToolbar)(name: [string](/docs/luau/strings)):[PluginToolbar](/docs/reference/engine/classes/PluginToolbar) |
| [Deactivate](#Deactivate)():() |
| [GetJoinMode](#GetJoinMode)():[Enum.JointCreationMode](/docs/reference/engine/enums/JointCreationMode) |
| [GetMouse](#GetMouse)():[PluginMouse](/docs/reference/engine/classes/PluginMouse) |
| [GetSelectedRibbonTool](#GetSelectedRibbonTool)():[Enum.RibbonTool](/docs/reference/engine/enums/RibbonTool) |
| [GetSetting](#GetSetting)(key: [string](/docs/luau/strings)):Variant |
| [GetStudioUserId](#GetStudioUserId)():[number](/docs/luau/numbers)  Deprecated |
| [ImportFbxAnimationAsync](#ImportFbxAnimationAsync)(rigModel: [Instance](/docs/reference/engine/datatypes/Instance),isR15: [boolean](/docs/luau/booleans)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [ImportFbxAnimation](#ImportFbxAnimation)(rigModel: [Instance](/docs/reference/engine/datatypes/Instance),isR15: [boolean](/docs/luau/booleans)):[Instance](/docs/reference/engine/datatypes/Instance)  Deprecated |
| [ImportFbxRigAsync](#ImportFbxRigAsync)(isR15: [boolean](/docs/luau/booleans)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [ImportFbxRig](#ImportFbxRig)(isR15: [boolean](/docs/luau/booleans)):[Instance](/docs/reference/engine/datatypes/Instance)  Deprecated |
| [Intersect](#Intersect)(objects: Instances):[Instance](/docs/reference/engine/datatypes/Instance) |
| [IsActivated](#IsActivated)():[boolean](/docs/luau/booleans) |
| [IsActivatedWithExclusiveMouse](#IsActivatedWithExclusiveMouse)():[boolean](/docs/luau/booleans) |
| [Negate](#Negate)(objects: Instances):Instances |
| [OpenScript](#OpenScript)(script: [LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer),lineNumber: [number](/docs/luau/numbers)):()  Deprecated |
| [OpenWikiPage](#OpenWikiPage)(url: [string](/docs/luau/strings)):() |
| [PromptForExistingAssetIdAsync](#PromptForExistingAssetIdAsync)(assetType: [string](/docs/luau/strings)):[number](/docs/luau/numbers) |
| [PromptForExistingAssetId](#PromptForExistingAssetId)(assetType: [string](/docs/luau/strings)):[number](/docs/luau/numbers) |
| [PromptSaveSelectionAsync](#PromptSaveSelectionAsync)(suggestedFileName: [string](/docs/luau/strings)):[boolean](/docs/luau/booleans) |
| [PromptSaveSelection](#PromptSaveSelection)(suggestedFileName: [string](/docs/luau/strings)):[boolean](/docs/luau/booleans)  Deprecated |
| [SaveSelectedToRoblox](#SaveSelectedToRoblox)():() |
| [SelectRibbonTool](#SelectRibbonTool)(tool: [Enum.RibbonTool](/docs/reference/engine/enums/RibbonTool),position: [UDim2](/docs/reference/engine/datatypes/UDim2)):() |
| [Separate](#Separate)(objects: Instances):Instances |
| [SetSetting](#SetSetting)(key: [string](/docs/luau/strings),value: Variant):() |
| [StartDrag](#StartDrag)(dragData: [Dictionary](/docs/luau/tables#dictionaries)):() |
| [Union](#Union)(objects: Instances):[Instance](/docs/reference/engine/datatypes/Instance) |

Events

|  |
| --- |
| [Deactivation](#Deactivation)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Unloading](#Unloading)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Plugin is the main object responsible for creating custom Studio widgets,
plugin toolbars, plugin buttons, and more. The Plugin object can be accessed
through the [plugin](/docs/reference/engine/globals/RobloxGlobals#plugin) global reference in a [Script](/docs/reference/engine/classes/Script)
that is executed as a plugin.

Code Samples

Script - Pass the Plugin Global to a ModuleScript

The [plugin](/docs/reference/engine/globals/RobloxGlobals#plugin) global reference is not passed to
[ModuleScripts](/docs/reference/engine/classes/ModuleScript) within the plugin. In order to use it in a
[ModuleScript](/docs/reference/engine/classes/ModuleScript), you must explicitly pass it as seen in the example
below.

```
assert(plugin, "This script must be run as a plugin!")



-- Code beyond this point will execute only if the script is run as a plugin



-- Load the module and pass the plugin reference



local pluginModule = require(script.Parent.PluginModule)



pluginModule:Initialize(plugin)



-- Verify if the plugin reference was initialized



pluginModule:CheckForPluginGlobal()
```

ModuleScript - Receive and Store the Plugin Global

```
local pluginModule = {}



local plugin -- Local plugin reference



-- Initialize the plugin reference if not already set



function pluginModule:Initialize(pluginReference: Plugin)



if plugin ~= pluginReference then



plugin = pluginReference



else



error("Plugin is already initialized")



end



end



-- Check if the plugin reference is set and print out appropriate info



function pluginModule:CheckForPluginGlobal()



if plugin ~= nil then



print("Plugin reference is set!")



else



warn("Plugin reference is missing!")



end



end



return pluginModule
```

---

API Reference

Properties

CollisionEnabled

Read Only

Not Replicated

Read Parallel

Returns whether the user has enabled Collisions in Studio's toolbar.

Plugin.CollisionEnabled:[boolean](/docs/luau/booleans)

Returns whether the user has enabled Collisions in Studio's toolbar.

Provide feedback

---

DisableUIDragDetectorDrags

Roblox Script Security

Read Parallel

Plugin.DisableUIDragDetectorDrags:[boolean](/docs/luau/booleans)

Provide feedback

---

GridSize

Read Only

Not Replicated

Read Parallel

Returns the grid snapping size the user has set in Studio.

Plugin.GridSize:[number](/docs/luau/numbers)

Returns the grid snapping size the user has set in Studio's toolbar. Note
that this property may have slight rounding errors; for example it may be
0.0099999997764826 for a user setting of 1 or 0.4000000059604645 for
a user setting of 0.4.

Provide feedback

---

IsDebuggable

Roblox Script Security

Read Parallel

Plugin.IsDebuggable:[boolean](/docs/luau/booleans)

Provide feedback

---

Methods

Activate

Plugin Security

Sets the state of the calling plugin to activated.

Plugin:Activate(exclusiveMouse:[boolean](/docs/luau/booleans)):()

Parameters

|  |
| --- |
| exclusiveMouse:[boolean](/docs/luau/booleans)  A boolean specifying whether to activate the plugin with exclusive mouse. If true, a [PluginMouse](/docs/reference/engine/classes/PluginMouse) can be retrieved via [GetMouse()](/docs/reference/engine/classes/Plugin#GetMouse). |

Returns

()

This method sets the state of the calling plugin to activated. Activating
the plugin allows mouse control through the
[GetMouse()](/docs/reference/engine/classes/Plugin#GetMouse) method.

At any given time, there are either 0 or 1 activated plugins. Activating a
plugin will deactivate all other plugins and they will receive a
[Deactivation](/docs/reference/engine/classes/Plugin#Deactivation) event.

#### See Also

* [IsActivatedWithExclusiveMouse()](/docs/reference/engine/classes/Plugin#IsActivatedWithExclusiveMouse)
  which returns true if the plugin is currently active with an exclusive
  mouse, after having been activated via this method.
* [Unloading](/docs/reference/engine/classes/Plugin#Unloading) which fires immediately before the
  plugin is unloaded or reloaded via uninstallation, deactivation, or
  updating.

Provide feedback

---

CreateDockWidgetPluginGuiAsync

Yields

Plugin Security

Creates a [DockWidgetPluginGui](/docs/reference/engine/classes/DockWidgetPluginGui) given a
[DockWidgetPluginGuiInfo](/docs/reference/engine/datatypes/DockWidgetPluginGuiInfo).

Plugin:CreateDockWidgetPluginGuiAsync(

pluginGuiId:[string](/docs/luau/strings), dockWidgetPluginGuiInfo:[DockWidgetPluginGuiInfo](/docs/reference/engine/datatypes/DockWidgetPluginGuiInfo)

):[DockWidgetPluginGui](/docs/reference/engine/classes/DockWidgetPluginGui)

Parameters

|  |
| --- |
| pluginGuiId:[string](/docs/luau/strings)  A unique and consistent identifier used to storing the widget's dock state and other internal details. |
| dockWidgetPluginGuiInfo:[DockWidgetPluginGuiInfo](/docs/reference/engine/datatypes/DockWidgetPluginGuiInfo)  Describes the [DockWidgetPluginGui](/docs/reference/engine/classes/DockWidgetPluginGui) to create (initial state, size, etc). |

Returns

[DockWidgetPluginGui](/docs/reference/engine/classes/DockWidgetPluginGui)

This method creates a new [DockWidgetPluginGui](/docs/reference/engine/classes/DockWidgetPluginGui) from the given
[DockWidgetPluginGuiInfo](/docs/reference/engine/datatypes/DockWidgetPluginGuiInfo). The first parameter, pluginGuiId,
should be a unique and consistent string. It is used to save the state of
the widget's dock state and other internal details.

Code Samples

Widget GUI Text Button

This code, when ran inside a Plugin, creates a DockWidgetPluginGui with a
simple TextButton.

```
-- Create new 'DockWidgetPluginGuiInfo' object



local widgetInfo = DockWidgetPluginGuiInfo.new(



Enum.InitialDockState.Float, -- Widget will be initialized in floating panel



true, -- Widget will be initially enabled



false, -- Don't override the previous enabled state



200, -- Default width of the floating window



300, -- Default height of the floating window



150, -- Minimum width of the floating window (optional)



150 -- Minimum height of the floating window (optional)



)



-- Create new widget GUI



local testWidget = plugin:CreateDockWidgetPluginGuiAsync("TestWidget", widgetInfo)



local testButton = Instance.new("TextButton")



testButton.BorderSizePixel = 0



testButton.TextSize = 20



testButton.TextColor3 = Color3.new(1, 0.2, 0.4)



testButton.AnchorPoint = Vector2.new(0.5, 0.5)



testButton.Size = UDim2.new(1, 0, 1, 0)



testButton.Position = UDim2.new(0.5, 0, 0.5, 0)



testButton.SizeConstraint = Enum.SizeConstraint.RelativeYY



testButton.Text = "Click Me"



testButton.Parent = testWidget
```

Provide feedback

---

CreateDockWidgetPluginGui

Deprecated

Show details

---

CreatePluginAction

Plugin Security

Creates a [PluginAction](/docs/reference/engine/classes/PluginAction) which represents a generic performable
action in Studio with no directly‑associated [PluginToolbarButton](/docs/reference/engine/classes/PluginToolbarButton).

Plugin:CreatePluginAction(

actionId:[string](/docs/luau/strings), text:[string](/docs/luau/strings), statusTip:[string](/docs/luau/strings), iconName:[string](/docs/luau/strings), allowBinding:[boolean](/docs/luau/booleans)

):[PluginAction](/docs/reference/engine/classes/PluginAction)

Parameters

|  |
| --- |
| actionId:[string](/docs/luau/strings)  Must be a unique string that identifies this PluginAction from others. |
| text:[string](/docs/luau/strings)  The displayed name of the action. |
| statusTip:[string](/docs/luau/strings)  The displayed description of the action. |
| iconName:[string](/docs/luau/strings)  The name of the icon used to display the plugin. |
| allowBinding:[boolean](/docs/luau/booleans) Default Value: true Whether the [PluginAction](/docs/reference/engine/classes/PluginAction) will be hidden from Studio's shortcuts view. Useful for contextual actions. Defaults to true. |

Returns

[PluginAction](/docs/reference/engine/classes/PluginAction)

This method creates a [PluginAction](/docs/reference/engine/classes/PluginAction) which represents a generic
performable action in Studio with no directly‑associated
[PluginToolbarButton](/docs/reference/engine/classes/PluginToolbarButton).

See also [CreatePluginMenu()](/docs/reference/engine/classes/Plugin#CreatePluginMenu) which
creates a Studio [PluginMenu](/docs/reference/engine/classes/PluginMenu) that can display a list of
[PluginActions](/docs/reference/engine/classes/PluginAction).

Code Samples

Creating a PluginAction

This code sample visualizes how to create a [PluginAction](/docs/reference/engine/classes/PluginAction). These
must be created using the [Plugin:CreatePluginAction()](/docs/reference/engine/classes/Plugin#CreatePluginAction) method in
order to work.

In order to work as expected, the code block must but pasted into the Command
Bar, but only once. Consecutive attempts at executing the code in the Command
Bar will result in an error because a plugin cannot create more than one
[PluginMenu](/docs/reference/engine/classes/PluginMenu) with the same ID.

When the created action is bound and [Triggered](/docs/reference/engine/classes/PluginAction#Triggered),
it outputs Hello world!.

```
local pluginAction = plugin:CreatePluginAction(



"HelloWorldAction",



"Hello World",



"Prints a 'Hello world!'",



"rbxasset://textures/sparkle.png",



true



)



pluginAction.Name = "Test Action"



local function actionTriggered()



print("Hello world!")



end



pluginAction.Triggered:Connect(actionTriggered)
```

Provide feedback

---

CreatePluginMenu

Plugin Security

Creates a new plugin menu.

Plugin:CreatePluginMenu(

id:[string](/docs/luau/strings), title:[string](/docs/luau/strings), icon:[string](/docs/luau/strings)

):[PluginMenu](/docs/reference/engine/classes/PluginMenu)

Parameters

|  |
| --- |
| id:[string](/docs/luau/strings)  Unique ID for the menu. |
| title:[string](/docs/luau/strings)  The text to be displayed when used as a submenu. |
| icon:[string](/docs/luau/strings)  The icon to be displayed when used as a submenu. |

Returns

[PluginMenu](/docs/reference/engine/classes/PluginMenu)

This function creates a new [PluginMenu](/docs/reference/engine/classes/PluginMenu) which is a context menu
that can be shown in Studio that displays a list of
[PluginActions](/docs/reference/engine/classes/PluginAction) and also supports submenus.

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

Provide feedback

---

CreateToolbar

Plugin Security

Creates a new [PluginToolbar](/docs/reference/engine/classes/PluginToolbar) with the given name.

Plugin:CreateToolbar(name:[string](/docs/luau/strings)):[PluginToolbar](/docs/reference/engine/classes/PluginToolbar)

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  The visible text on the toolbar, labeling the group of buttons contained within. |

Returns

[PluginToolbar](/docs/reference/engine/classes/PluginToolbar)

This method creates a new [PluginToolbar](/docs/reference/engine/classes/PluginToolbar) with the given name. The
toolbar can then be used to create plugin buttons.

Code Samples

Plugin:CreateToolbar

This code creates a toolbar with the name "ExampleToolbar".

```
plugin:CreateToolbar("ExampleToolbar")
```

Provide feedback

---

Deactivate

Plugin Security

Deactivates the plugin.

Plugin:Deactivate():()

Returns

()

Deactivates the plugin. This will disengage the associated
[PluginMouse](/docs/reference/engine/classes/PluginMouse) if it has been activated.

#### See Also

* [Activate()](/docs/reference/engine/classes/Plugin#Activate) which sets the state of the calling
  plugin to activated.
* [Deactivation](/docs/reference/engine/classes/Plugin#Deactivation) which fires when the plugin is
  deactivated.
* [Unloading](/docs/reference/engine/classes/Plugin#Unloading) which fires immediately before the
  plugin is unloaded or reloaded via uninstallation, deactivation, or
  updating.

Provide feedback

---

GetJoinMode

Plugin Security

Returns the [Enum.JointCreationMode](/docs/reference/engine/enums/JointCreationMode) the user has set in Studio's toolbar.

Plugin:GetJoinMode():[Enum.JointCreationMode](/docs/reference/engine/enums/JointCreationMode)

Returns

[Enum.JointCreationMode](/docs/reference/engine/enums/JointCreationMode)

Returns the [Enum.JointCreationMode](/docs/reference/engine/enums/JointCreationMode) the user has set in Studio's toolbar.

Provide feedback

---

GetMouse

Plugin Security

Returns a [Mouse](/docs/reference/engine/classes/Mouse) that can be used while the plugin is active.

Plugin:GetMouse():[PluginMouse](/docs/reference/engine/classes/PluginMouse)

Returns

[PluginMouse](/docs/reference/engine/classes/PluginMouse)

This method returns a [PluginMouse](/docs/reference/engine/classes/PluginMouse) that can be used while the
plugin is active through [Activate()](/docs/reference/engine/classes/Plugin#Activate).

Code Samples

Plugin:GetMouse

This code would print Button 1 pressed from PluginMouse each time the mouse's
left button was clicked.

```
local mouse = plugin:GetMouse()



local function button1Down()



print("Button 1 pressed from PluginMouse")



end



mouse.Button1Down:Connect(button1Down)
```

Provide feedback

---

GetSelectedRibbonTool

Plugin Security

Returns the currently selected [Enum.RibbonTool](/docs/reference/engine/enums/RibbonTool).

Plugin:GetSelectedRibbonTool():[Enum.RibbonTool](/docs/reference/engine/enums/RibbonTool)

Returns

[Enum.RibbonTool](/docs/reference/engine/enums/RibbonTool)

This method returns the currently selected [Enum.RibbonTool](/docs/reference/engine/enums/RibbonTool).

Code Samples

Plugin:GetSelectedRibbonTool

This code must be run from a plugin. This code selects the move tool, checks
which tool is selected, then prints out to the console which tool is selected.
SelectRibbonTool will not return the value until the next frame.

```
plugin:SelectRibbonTool(Enum.RibbonTool.Move, UDim2.new())



task.wait() -- wait for next frame



local selectedRibbonTool = plugin:GetSelectedRibbonTool()



print("The selected RibbonTool is", selectedRibbonTool)
```

Provide feedback

---

GetSetting

Plugin Security

Retrieves a previously stored value with the given key, or nil if the
given key doesn't exist.

Plugin:GetSetting(key:[string](/docs/luau/strings)):Variant

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings) |

Returns

Variant

Retrieves a previously stored value with the given key, or nil if the
given key doesn't exist.

Because multiple instances of the same plugin can run simultaneously (for
example, if multiple Studio windows are open), you shouldn't depend on
this value staying the same over time. The other plugin instances can
update the setting at any time.

This call can silently fail and return nil if multiple instances of the
same plugin are actively reading and writing data. If your plugin expects
to write to settings frequently, you should double-check the returned
value from this call after a short while to distinguish between a setting
being temporarily unavailable and a setting not existing.

Code Samples

Plugin:GetSetting

The below example would print the value saved to the key FirstTime. If the key
doesn't exist, it would print nil.

```
local RAN_BEFORE_KEY = "RanBefore"



local didRunBefore = plugin:GetSetting(RAN_BEFORE_KEY)



if didRunBefore then



print("Welcome back!")



else



plugin:SetSetting(RAN_BEFORE_KEY, true)



print("Welcome! Thanks for installing this plugin!")



end
```

Provide feedback

---

GetStudioUserId

Deprecated

Show details

---

ImportFbxAnimationAsync

Yields

Plugin Security

Prompts the user to open a .fbx animation file that can be loaded onto
the rigModel, then proceeds to insert the animation as a
[KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) in the [Workspace](/docs/reference/engine/classes/Workspace).

Plugin:ImportFbxAnimationAsync(

rigModel:[Instance](/docs/reference/engine/datatypes/Instance), isR15:[boolean](/docs/luau/booleans)

):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| rigModel:[Instance](/docs/reference/engine/datatypes/Instance) |
| isR15:[boolean](/docs/luau/booleans) Default Value: true |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

This function prompts the user to open a .fbx animation file that can be
loaded onto the rigModel, then proceeds to insert the animation as a
[KeyframeSequence](/docs/reference/engine/classes/KeyframeSequence) in the [Workspace](/docs/reference/engine/classes/Workspace).

Provide feedback

---

ImportFbxAnimation

Deprecated

Show details

---

ImportFbxRigAsync

Yields

Plugin Security

Prompts the user to open a .fbx file, uploads the individual components
of the model as meshes, and generates a character rig for use in
animation, which is loaded into the [Workspace](/docs/reference/engine/classes/Workspace).

Plugin:ImportFbxRigAsync(isR15:[boolean](/docs/luau/booleans)):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| isR15:[boolean](/docs/luau/booleans) Default Value: true |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

Prompts the user to open a .fbx file, uploads the individual components
of the model as meshes, and generates a character rig for use in
animation, which is loaded into the [Workspace](/docs/reference/engine/classes/Workspace).

Provide feedback

---

ImportFbxRig

Deprecated

Show details

---

Intersect

Plugin Security

Intersects the given parts and returns the resulting
[IntersectOperation](/docs/reference/engine/classes/IntersectOperation).

Plugin:Intersect(objects:Instances):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| objects:Instances |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

Intersects the given parts and returns the resulting
[IntersectOperation](/docs/reference/engine/classes/IntersectOperation).

Provide feedback

---

IsActivated

Plugin Security

Returns true if this plugin is currently active, after having been
activated via the [Activate()](/docs/reference/engine/classes/Plugin#Activate) function.

Plugin:IsActivated():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

A boolean indicating whether the plugin is currently active.

This function returns true if this plugin is currently active, after
having been activated via the [Activate()](/docs/reference/engine/classes/Plugin#Activate)
function.

Provide feedback

---

IsActivatedWithExclusiveMouse

Plugin Security

Returns true if this plugin is currently active with an exclusive mouse.

Plugin:IsActivatedWithExclusiveMouse():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

Whether this plugin is currently active with an exclusive mouse.

This function returns true if this plugin is currently active with an
exclusive mouse, after having been activated via the
[Activate()](/docs/reference/engine/classes/Plugin#Activate) function. If this returns true, a
[PluginMouse](/docs/reference/engine/classes/PluginMouse) can be retrieved via
[GetMouse()](/docs/reference/engine/classes/Plugin#GetMouse).

#### See Also

* [Deactivation](/docs/reference/engine/classes/Plugin#Deactivation) which fires when the plugin is
  deactivated.
* [Unloading](/docs/reference/engine/classes/Plugin#Unloading) which fires immediately before the
  plugin is unloaded or reloaded via uninstallation, deactivation, or
  updating.

Provide feedback

---

Negate

Plugin Security

Negates the given parts and returns the resulting
[NegateOperations](/docs/reference/engine/classes/NegateOperation).

Plugin:Negate(objects:Instances):Instances

Parameters

|  |
| --- |
| objects:Instances |

Returns

Instances

Negates the given parts and returns the resulting
[NegateOperations](/docs/reference/engine/classes/NegateOperation).

Provide feedback

---

OpenScript

Deprecated

Show details

---

OpenWikiPage

Plugin Security

Opens the context help window to the wiki page that url links to.

Plugin:OpenWikiPage(url:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| url:[string](/docs/luau/strings) |

Returns

()

Opens the context help window to the wiki page that url links to.

Code Samples

Plugin:OpenWikiPage

The following, when executed in a plugin, will open the
[BasePart API page](/docs/reference/engine/classes/BasePart) in the context help.

```
plugin:OpenWikiPage("API:Class/BasePart")
```

Provide feedback

---

PromptForExistingAssetIdAsync

Yields

Plugin Security

Opens a window in Roblox Studio which prompts the user to select an asset
based on the assetType specified.

Plugin:PromptForExistingAssetIdAsync(assetType:[string](/docs/luau/strings)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| assetType:[string](/docs/luau/strings) |

Returns

[number](/docs/luau/numbers)

Opens a window in Roblox Studio which prompts the user to select an asset
based on the assetType specified. Returns what asset ID was selected, or
-1 if the window was closed.

Provide feedback

---

PromptForExistingAssetId

Yields

Plugin Security

Opens a window in Roblox Studio which prompts the user to select an asset
based on the assetType specified.

Plugin:PromptForExistingAssetId(assetType:[string](/docs/luau/strings)):[number](/docs/luau/numbers)

Parameters

|  |
| --- |
| assetType:[string](/docs/luau/strings) |

Returns

[number](/docs/luau/numbers)

Provide feedback

---

PromptSaveSelectionAsync

Yields

Plugin Security

Prompts the user to save their current selection with the specified file
name.

Plugin:PromptSaveSelectionAsync(suggestedFileName:[string](/docs/luau/strings)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| suggestedFileName:[string](/docs/luau/strings) |

Returns

[boolean](/docs/luau/booleans)

Prompts the user to save their current selection with the specified file
name. Returns true if the user did save the file.

Provide feedback

---

PromptSaveSelection

Deprecated

Show details

---

SaveSelectedToRoblox

Plugin Security

Opens an upload window for the user's current selection.

Plugin:SaveSelectedToRoblox():()

Returns

()

Opens an upload window for the user's current selection.

Provide feedback

---

SelectRibbonTool

Plugin Security

Activates the specified Roblox Studio tool.

Plugin:SelectRibbonTool(

tool:[Enum.RibbonTool](/docs/reference/engine/enums/RibbonTool), position:[UDim2](/docs/reference/engine/datatypes/UDim2)

):()

Parameters

|  |
| --- |
| tool:[Enum.RibbonTool](/docs/reference/engine/enums/RibbonTool) |
| position:[UDim2](/docs/reference/engine/datatypes/UDim2) |

Returns

()

Activates the specified Roblox Studio tool. If the tool opens a window,
the position parameter specifies where it should be shown on the screen.

An object must be selected in order for this to work correctly. Also note
that altering the scale fields of the position property will not affect
the dialog popups.

Provide feedback

---

Separate

Plugin Security

Separates the given [UnionOperations](/docs/reference/engine/classes/UnionOperation) and returns the
resulting parts.

Plugin:Separate(objects:Instances):Instances

Parameters

|  |
| --- |
| objects:Instances |

Returns

Instances

Separates the given [UnionOperations](/docs/reference/engine/classes/UnionOperation) and returns the
resulting parts.

Provide feedback

---

SetSetting

Plugin Security

Stores a given value for later use under the given key. The value will
persist even after Studio is closed.

Plugin:SetSetting(

key:[string](/docs/luau/strings), value:Variant

):()

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings) |
| value:Variant |

Returns

()

Stores a given value for later use under the given key. The value will
persist even after Roblox Studio is closed. These settings are saved in
.json format as a map with string keys. Arrays are automatically
converted to maps by converting the numeric keys to strings first.

Note that the .json format imposes additional restrictions, including
the following characters which can corrupt the settings file:

* Backslashes (\) in keys or values, in particular escaped quotes
  (\").
* Newlines (\n) in keys.
* Quotes (") in keys.
* Periods (.) in keys.

This call can silently fail if multiple instances of the same plugin are
actively reading and writing data. If your plugin expects to write to
settings frequently, you may check that the data has been properly written
by calling [GetSetting()](/docs/reference/engine/classes/Plugin#GetSetting).

Code Samples

Plugin:GetSetting and Plugin:SetSetting

This code sample demonstrates use of the [Plugin:GetSetting()](/docs/reference/engine/classes/Plugin#GetSetting) and
[Plugin:SetSetting()](/docs/reference/engine/classes/Plugin#SetSetting) functions. They detect if a plugin is running for
the first time by setting a key. If the key is true, it prints a "welcome
back" message; otherwise it prints a "first run" message and sets the key to
true.

```
local RAN_BEFORE_KEY = "RunBefore"



local hasRunBefore = plugin:GetSetting(RAN_BEFORE_KEY)



if hasRunBefore then



print("Welcome back!")



else



print("Thanks for installing this plugin!")



plugin:SetSetting(RAN_BEFORE_KEY, true)



end
```

Provide feedback

---

StartDrag

Plugin Security

Starts a drag action given a dictionary of parameters.

Plugin:StartDrag(dragData:[Dictionary](/docs/luau/tables#dictionaries)):()

Parameters

|  |
| --- |
| dragData:[Dictionary](/docs/luau/tables#dictionaries) |

Returns

()

This method initiates a drag action using a dictionary of parameters. The
parameters are as follows:

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| Sender | string | "" | Identifies the source of the drag action to the drop target |
| MimeType | string | "" | The MIME type of Data. |
| Data | string | "" | Information about the drag action, for example what is being dragged. Should be used by the drop target. |
| MouseIcon | [Content](/docs/reference/engine/datatypes/Content) | "" | The icon to use for the mouse cursor during the drag. If empty, uses the default cursor. |
| DragIcon | [Content](/docs/reference/engine/datatypes/Content) | "" | An image to render under the mouse cursor during the drag. This should represent the item being dragged. |
| HotSpot | [Vector2](/docs/reference/engine/datatypes/Vector2) | [Vector2.new(0, 0)](/docs/reference/engine/datatypes/Vector2#new) | The pixel offset from the top-left where the cursor should "hold" the DragIcon. |

See also [PluginGui.PluginDragEntered](/docs/reference/engine/classes/PluginGui#PluginDragEntered),
[PluginGui.PluginDragMoved](/docs/reference/engine/classes/PluginGui#PluginDragMoved), [PluginGui.PluginDragDropped](/docs/reference/engine/classes/PluginGui#PluginDragDropped),
and [PluginGui.PluginDragLeft](/docs/reference/engine/classes/PluginGui#PluginDragLeft).

Code Samples

Plugin Drag and Drop

This code sample creates two plugin widget windows: a drag source and a drop
target. In the source window, the script creates a [TextBox](/docs/reference/engine/classes/TextBox) and [TextButton](/docs/reference/engine/classes/TextButton)
to allow the user to begin a plugin drag action. The drop target window will
display the MIME type of whatever is dragged into it. If
the MIME type is text/plain, it will display the plain text data instead.

To run this code sample as a plugin, paste it into a [Script](/docs/reference/engine/classes/Script). Then,
right-click the script in the Explorer window and choose Save as Local
Plugin.

```
assert(plugin, "This script must be run as a Studio plugin")



local widgetInfo = DockWidgetPluginGuiInfo.new(Enum.InitialDockState.Float, true, true, 300, 200)



local dragSourceWidget = plugin:CreateDockWidgetPluginGui("Drag Source", widgetInfo)



dragSourceWidget.Title = "Drag Source"



local textBox = Instance.new("TextBox")



textBox.Parent = dragSourceWidget



textBox.Size = UDim2.new(1, 0, 0, 32)



textBox.Text = "Hello, plugin drags"



local dragButton = Instance.new("TextButton")



dragButton.Size = UDim2.new(1, 0, 1, -32)



dragButton.Position = UDim2.new(0, 0, 0, 32)



dragButton.Text = "Edit the text above, then start drag here"



dragButton.Parent = dragSourceWidget



function onMouseButton1Down()



local dragData = {



Sender = "SomeDragSource",



MimeType = "text/plain",



Data = textBox.Text,



MouseIcon = "",



DragIcon = "",



HotSpot = Vector2.new(0, 0),



}



plugin:StartDrag(dragData)



end



dragButton.MouseButton1Down:Connect(onMouseButton1Down)



-- This widget will receive drops



local dragTargetWidget = plugin:CreateDockWidgetPluginGui("Drop Target", widgetInfo)



dragTargetWidget.Title = "Drop Target"



-- This TextLabel will display what was dropped



local textLabel = Instance.new("TextLabel")



textLabel.Size = UDim2.new(1, 0, 1, 0)



textLabel.Text = "Drop here..."



textLabel.Parent = dragTargetWidget



local function onDragDrop(dragData)



if dragData.MimeType == "text/plain" then



textLabel.Text = dragData.Data



else



textLabel.Text = dragData.MimeType



end



end



dragTargetWidget.PluginDragDropped:Connect(onDragDrop)



dragTargetWidget.PluginDragEntered:Connect(function(_dragData)



print("PluginDragEntered")



end)



dragTargetWidget.PluginDragLeft:Connect(function(_dragData)



print("PluginDragLeft")



end)



dragTargetWidget.PluginDragMoved:Connect(function(_dragData)



print("PluginDragMoved")



end)
```

Provide feedback

---

Union

Plugin Security

Unions the given parts and returns the resulting [UnionOperation](/docs/reference/engine/classes/UnionOperation).

Plugin:Union(objects:Instances):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| objects:Instances |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

Unions the given parts and returns the resulting [UnionOperation](/docs/reference/engine/classes/UnionOperation).

Provide feedback

---

Events

Deactivation

Plugin Security

Fired when the plugin is deactivated.

Plugin.Deactivation():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Fired when the [Plugin](/docs/reference/engine/classes/Plugin) is deactivated. This occurs when either the
plugin code calls [Deactivate()](/docs/reference/engine/classes/Plugin#Deactivate), or because
some other plugin called [Activate()](/docs/reference/engine/classes/Plugin#Activate), which
forces all other plugins to lose their active state.

See also [Unloading](/docs/reference/engine/classes/Plugin#Unloading) which fires immediately before
the plugin is unloaded or reloaded via uninstallation, deactivation, or
updating.

Provide feedback

---

Unloading

Plugin Security

Fires immediately before the [Plugin](/docs/reference/engine/classes/Plugin) stops running.

Plugin.Unloading():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires immediately before the [Plugin](/docs/reference/engine/classes/Plugin) stops running.
Plugins are unloaded when disabled, uninstalled, about to be updated, or
when the place is closing.

It enables a plugin to clean up after itself before its scripts stop
running, e.g. to remove unnecessary instances from the [DataModel](/docs/reference/engine/classes/DataModel).
If a plugin does not clean up properly, the old copies will remain. When
this occurs, users may be forced to close and reopen the place which is a
bad user experience.

Plugin-related instances such as
[PluginToolbarButtons](/docs/reference/engine/classes/PluginToolbarButton),
[DockWidgetPluginGuis](/docs/reference/engine/classes/DockWidgetPluginGui), and
[PluginGuis](/docs/reference/engine/classes/PluginGui) are automatically cleaned up when the plugin
is unloaded so there is no need to remove them.

Provide feedback

---