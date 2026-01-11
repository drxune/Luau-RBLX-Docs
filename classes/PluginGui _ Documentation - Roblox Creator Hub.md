# PluginGui | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/PluginGui
Scraped: 2026-01-11T02:35:02.017931Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- LayerCollector
- PluginGui
- GuiBase2d
- Instance
- Object
- DockWidgetPluginGui
- QWidgetPluginGui
- GuiObjects
- Enabled
- PluginGui.Enabled
- Plugin:CreateDockWidgetPluginGui()
- DataModel:BindToClose()
- Plugin:StartDrag()
- PluginGui.PluginDragEntered
- PluginGui.PluginDragLeft
- PluginGui.PluginDragMoved
- TextBox
- TextButton
- Script
- PluginDragLeft
- PluginDragDropped
- PluginGui.PluginDragDropped
- PluginDragEntered
- UserInputService.WindowFocused
- GuiObject.InputBegan
- WindowFocusReleased
- UserInputService.WindowFocusReleased
- WindowFocused()
- WindowFocusReleased()
- Title()
- WindowFocused
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [LayerCollector](/docs/reference/engine/classes/LayerCollector)
6. /
7. [PluginGui](/docs/reference/engine/classes/PluginGui)

English

Feedback

Engine Class

PluginGui

Not Creatable

Not Replicated

---

Summary

Properties

|  |
| --- |
| [Title](#Title):[string](/docs/luau/strings) |

Methods

|  |
| --- |
| [BindToClose](#BindToClose)(function: [function](/docs/luau/functions)):() |
| [GetRelativeMousePosition](#GetRelativeMousePosition)():[Vector2](/docs/reference/engine/datatypes/Vector2) |

Events

|  |
| --- |
| [PluginDragDropped](#PluginDragDropped)(dragData: [Dictionary](/docs/luau/tables#dictionaries)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PluginDragEntered](#PluginDragEntered)(dragData: [Dictionary](/docs/luau/tables#dictionaries)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PluginDragLeft](#PluginDragLeft)(dragData: [Dictionary](/docs/luau/tables#dictionaries)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [PluginDragMoved](#PluginDragMoved)(dragData: [Dictionary](/docs/luau/tables#dictionaries)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [WindowFocused](#WindowFocused)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [WindowFocusReleased](#WindowFocusReleased)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

4 inherited from [LayerCollector](/docs/reference/engine/classes/LayerCollector)

12 inherited from [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[DockWidgetPluginGui](/docs/reference/engine/classes/DockWidgetPluginGui), [QWidgetPluginGui](/docs/reference/engine/classes/QWidgetPluginGui)

PluginGui is an abstract class for GUIs that allow the display of
[GuiObjects](/docs/reference/engine/classes/GuiObject) in various Roblox Studio widgets. As of right
now, the only available PluginGui type is [DockWidgetPluginGui](/docs/reference/engine/classes/DockWidgetPluginGui), but
there may be more in the future!

---

API Reference

Properties

Title

Read Parallel

The title that is displayed above the contents of the [PluginGui](/docs/reference/engine/classes/PluginGui).

PluginGui.Title:[string](/docs/luau/strings)

The title that is displayed above the contents of the [PluginGui](/docs/reference/engine/classes/PluginGui).
Defaults to empty string.

Provide feedback

---

Methods

BindToClose

Binds a function to the [PluginGui](/docs/reference/engine/classes/PluginGui) close button, overriding the
default behavior.

PluginGui:BindToClose(function:[function](/docs/luau/functions)):()

Parameters

|  |
| --- |
| function:[function](/docs/luau/functions) Default Value: "nil" The function to bind the close button to. If no function is specified then any previously specified function will be unbound. |

Returns

()

This function binds a function to the [PluginGui](/docs/reference/engine/classes/PluginGui) close button,
overriding the default behavior.

By default, when the user clicks the 'x' button in the top right corner of
the [PluginGui](/docs/reference/engine/classes/PluginGui) the [Enabled](/docs/reference/engine/classes/LayerCollector#Enabled) property
is set to *false*, closing the window. When a custom function is bound
using BindToClose this behavior is overwritten, allowing you to check if
the user really wants to close the window or give them an opportunity to
save their work.

As the default closing behavior is overwritten by this function, you'll
need to configure the [PluginGui](/docs/reference/engine/classes/PluginGui) to close manually by setting
[PluginGui.Enabled](/docs/reference/engine/classes/LayerCollector#Enabled) to *false*. For example,
in the below snippet users are required to click a confirm button to close
the GUI:

```
local closing = false



pluginGui:BindToClose(function()



-- make sure we haven't already made a button



if closing then



return



end



closing = true



-- create confirm button



local confirmButton = Instance.new("TextButton")



confirmButton.AnchorPoint = Vector2.new(0.5, 0.5)



confirmButton.Size = UDim2.new(0.5, 0, 0.5, 0)



confirmButton.Position = UDim2.new(0.5, 0, 0.5, 0)



confirmButton.BackgroundColor3 = Color3.new(1, 0, 0)



confirmButton.Text = "Close?"



confirmButton.Parent = pluginGui



-- listen for click



confirmButton.Activated:Connect(function()



-- close the gui



pluginGui.Enabled = false



-- remove confirm button



confirmButton:Destroy()



end)



end)
```

You can call BindToClose with no argument to 'unbind' and revert to the
default behavior described above. For example:

```
pluginGui:BindToClose()
```

See also:

* [Plugin:CreateDockWidgetPluginGui()](/docs/reference/engine/classes/Plugin#CreateDockWidgetPluginGui) to create a [PluginGui](/docs/reference/engine/classes/PluginGui)
* [DataModel:BindToClose()](/docs/reference/engine/classes/DataModel#BindToClose), which can be used to bind a function to
  the game ending and should not be confused with this function

Provide feedback

---

GetRelativeMousePosition

Plugin Security

Returns the position of the mouse relative to the PluginGui.

PluginGui:GetRelativeMousePosition():[Vector2](/docs/reference/engine/datatypes/Vector2)

Returns

[Vector2](/docs/reference/engine/datatypes/Vector2)

The screen position of the mouse relative to the PluginGui in pixels.

GetRelativeMousePosition returns the position of the mouse relative to the
top-left corner of the [PluginGui](/docs/reference/engine/classes/PluginGui). The returned value changes only
if a mouse input began on the PluginGui, or if the mouse is presently
hovering over the window.

Code Samples

PluginGui:GetRelativeMousePosition

```
local RunService = game:GetService("RunService")



local widgetInfo = DockWidgetPluginGuiInfo.new(



Enum.InitialDockState.Float,



true,



false, -- Enabled state, override



200,



300, -- Size



150,



150 -- Minimum size



)



local testWidget = plugin:CreateDockWidgetPluginGui("TestWidget", widgetInfo)



function update()



local v2 = testWidget:GetRelativeMousePosition()



testWidget.Title = ("(%d, %d)"):format(v2.x, v2.y)



end



RunService.Stepped:Connect(update)



update()
```

Provide feedback

---

Events

PluginDragDropped

Plugin Security

Fires when the user releases their mouse when hovering over a PluginGui
during a drag operation started by [Plugin:StartDrag()](/docs/reference/engine/classes/Plugin#StartDrag).

PluginGui.PluginDragDropped(dragData:[Dictionary](/docs/luau/tables#dictionaries)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| dragData:[Dictionary](/docs/luau/tables#dictionaries) |

PluginDragDropped fires when the user releases their mouse over a
[PluginGui](/docs/reference/engine/classes/PluginGui) during a drag operation started by
[Plugin:StartDrag()](/docs/reference/engine/classes/Plugin#StartDrag).

See also:

* [PluginGui.PluginDragEntered](/docs/reference/engine/classes/PluginGui#PluginDragEntered)
* [PluginGui.PluginDragLeft](/docs/reference/engine/classes/PluginGui#PluginDragLeft)
* [PluginGui.PluginDragMoved](/docs/reference/engine/classes/PluginGui#PluginDragMoved)

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

PluginDragEntered

Plugin Security

Fires when the user's mouse enters a PluginGui during a drag operation
started by [Plugin:StartDrag()](/docs/reference/engine/classes/Plugin#StartDrag).

PluginGui.PluginDragEntered(dragData:[Dictionary](/docs/luau/tables#dictionaries)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| dragData:[Dictionary](/docs/luau/tables#dictionaries)  A copy of the data originally passed to [Plugin:StartDrag()](/docs/reference/engine/classes/Plugin#StartDrag). |

PluginDragEntered fires when the user's mouse enters the
[PluginGui](/docs/reference/engine/classes/PluginGui) during a drag operation started by
[Plugin:StartDrag()](/docs/reference/engine/classes/Plugin#StartDrag).

This event is useful for displaying a "Drop Here" UI on PluginGuis where a
drag operation can be dropped. Such a UI should be hidden when either
[PluginDragLeft](/docs/reference/engine/classes/PluginGui#PluginDragLeft) or
[PluginDragDropped](/docs/reference/engine/classes/PluginGui#PluginDragDropped) fire.

See also:

* [PluginGui.PluginDragLeft](/docs/reference/engine/classes/PluginGui#PluginDragLeft)
* [PluginGui.PluginDragMoved](/docs/reference/engine/classes/PluginGui#PluginDragMoved)
* [PluginGui.PluginDragDropped](/docs/reference/engine/classes/PluginGui#PluginDragDropped)

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

PluginDragLeft

Plugin Security

Fires when the user's mouse leaves a PluginGui during a drag operation
started by [Plugin:StartDrag()](/docs/reference/engine/classes/Plugin#StartDrag).

PluginGui.PluginDragLeft(dragData:[Dictionary](/docs/luau/tables#dictionaries)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| dragData:[Dictionary](/docs/luau/tables#dictionaries)  A copy of the data originally passed to [Plugin:StartDrag()](/docs/reference/engine/classes/Plugin#StartDrag). |

PluginDragLeft fires when the user's mouse leaves a [PluginGui](/docs/reference/engine/classes/PluginGui)
during a drag operation started by [Plugin:StartDrag()](/docs/reference/engine/classes/Plugin#StartDrag).

This event and [PluginDragDropped](/docs/reference/engine/classes/PluginGui#PluginDragDropped) are
useful for hiding a "Drop Here" UI on PluginGuis where a drag operation
can be dropped. Such a UI should be shown when either
[PluginDragEntered](/docs/reference/engine/classes/PluginGui#PluginDragEntered) fires.

See also:

* [PluginGui.PluginDragEntered](/docs/reference/engine/classes/PluginGui#PluginDragEntered)
* [PluginGui.PluginDragMoved](/docs/reference/engine/classes/PluginGui#PluginDragMoved)
* [PluginGui.PluginDragDropped](/docs/reference/engine/classes/PluginGui#PluginDragDropped)

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

PluginDragMoved

Plugin Security

Fires when the user's mouse moves within a PluginGui during a drag
operation started by [Plugin:StartDrag()](/docs/reference/engine/classes/Plugin#StartDrag).

PluginGui.PluginDragMoved(dragData:[Dictionary](/docs/luau/tables#dictionaries)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| dragData:[Dictionary](/docs/luau/tables#dictionaries) |

PluginDragMoved fires when the user's mouse moves within a
[PluginGui](/docs/reference/engine/classes/PluginGui) during a drag operation started by
[Plugin:StartDrag()](/docs/reference/engine/classes/Plugin#StartDrag).

See also:

* [PluginGui.PluginDragEntered](/docs/reference/engine/classes/PluginGui#PluginDragEntered)
* [PluginGui.PluginDragLeft](/docs/reference/engine/classes/PluginGui#PluginDragLeft)
* [PluginGui.PluginDragDropped](/docs/reference/engine/classes/PluginGui#PluginDragDropped)

Provide feedback

---

WindowFocused

Plugin Security

Fires when the user begins interacting with the window of the PluginGui.

PluginGui.WindowFocused():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

WindowFocused fires immediately when the user starts interacting with
the PluginGui's window, usually by clicking on it. This functions works
similarly to the similarly-named [UserInputService.WindowFocused](/docs/reference/engine/classes/UserInputService#WindowFocused)
event. It fires before any [GuiObject.InputBegan](/docs/reference/engine/classes/GuiObject#InputBegan) events related to
mouse buttons.

If another [PluginGui](/docs/reference/engine/classes/PluginGui) is in focus and the user focuses this
PluginGui, then this event fires after the other's
[WindowFocusReleased](/docs/reference/engine/classes/PluginGui#WindowFocusReleased) event. However,
if the main game window was in focus, this event fires after
[UserInputService.WindowFocusReleased](/docs/reference/engine/classes/UserInputService#WindowFocusReleased).

Code Samples

Detecting PluginGui Focus State

This code sample demonstrates how the focus state of a PluginGui can be
tracked using the [WindowFocused()](/docs/reference/engine/classes/PluginGui#WindowFocused) and
[WindowFocusReleased()](/docs/reference/engine/classes/PluginGui#WindowFocusReleased) events. It changes
the [Title()](/docs/reference/engine/classes/PluginGui#Title) as the focus state changes.

```
local info = DockWidgetPluginGuiInfo.new(Enum.InitialDockState.Float, true, true, 200, 50, 1, 1)



local widget = plugin:CreateDockWidgetPluginGui("TestWidget", info)



local function onFocusReleased()



widget.Title = "I'm not in focus :("



end



local function onFocused()



widget.Title = "I'm in focus :D"



end



widget.WindowFocusReleased:Connect(onFocusReleased)



widget.WindowFocused:Connect(onFocused)
```

Provide feedback

---

WindowFocusReleased

Plugin Security

Fires when the user stops interacting with the window of the PluginGui.

PluginGui.WindowFocusReleased():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

WindowFocusReleased fires immediately when the user stops interacting
with the PluginGui's window, usually by clicking on something not in the
window. This functions works similarly to the similarly-named
[UserInputService.WindowFocusReleased](/docs/reference/engine/classes/UserInputService#WindowFocusReleased) event.

If focus is moving to another [PluginGui](/docs/reference/engine/classes/PluginGui) while the user had this
PluginGui in focus, then this event fires before the other's
[WindowFocused](/docs/reference/engine/classes/PluginGui#WindowFocused) event. However, if the main
game window is being put in focus, this event fires after
[UserInputService.WindowFocused](/docs/reference/engine/classes/UserInputService#WindowFocused).

Code Samples

Detecting PluginGui Focus State

This code sample demonstrates how the focus state of a PluginGui can be
tracked using the [WindowFocused()](/docs/reference/engine/classes/PluginGui#WindowFocused) and
[WindowFocusReleased()](/docs/reference/engine/classes/PluginGui#WindowFocusReleased) events. It changes
the [Title()](/docs/reference/engine/classes/PluginGui#Title) as the focus state changes.

```
local info = DockWidgetPluginGuiInfo.new(Enum.InitialDockState.Float, true, true, 200, 50, 1, 1)



local widget = plugin:CreateDockWidgetPluginGui("TestWidget", info)



local function onFocusReleased()



widget.Title = "I'm not in focus :("



end



local function onFocused()



widget.Title = "I'm in focus :D"



end



widget.WindowFocusReleased:Connect(onFocusReleased)



widget.WindowFocused:Connect(onFocused)
```

Provide feedback

---