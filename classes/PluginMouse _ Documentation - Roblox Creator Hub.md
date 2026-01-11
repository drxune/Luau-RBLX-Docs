# PluginMouse | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/PluginMouse
Scraped: 2026-01-11T02:37:01.018133Z

## Tags
- Not Creatable

## Inherits
- Mouse
- PluginMouse
- Plugins
- Plugin:GetMouse()
- Instance
- Object
- Plugin:Activate()
- PluginMouse.DragEnter
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Mouse](/docs/reference/engine/classes/Mouse)
6. /
7. [PluginMouse](/docs/reference/engine/classes/PluginMouse)

English

Feedback

Engine Class

PluginMouse

The PluginMouse object gives [Plugins](/docs/reference/engine/classes/Plugin) access to the mouse. It
works like the [Mouse](/docs/reference/engine/classes/Mouse) object and can be obtained using the plugin
[Plugin:GetMouse()](/docs/reference/engine/classes/Plugin#GetMouse) method.

Not Creatable

---

Summary

Events

|  |
| --- |
| [DragEnter](#DragEnter)(instances: Instances):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

25 inherited from [Mouse](/docs/reference/engine/classes/Mouse)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The PluginMouse object gives [Plugins](/docs/reference/engine/classes/Plugin) access to the mouse. It
works like the [Mouse](/docs/reference/engine/classes/Mouse) object and can be obtained using the plugin
[Plugin:GetMouse()](/docs/reference/engine/classes/Plugin#GetMouse) method.

Note the PluginMouse can only be used when the plugin has been activated using
[Plugin:Activate()](/docs/reference/engine/classes/Plugin#Activate).

In addition to the functions from the [Mouse](/docs/reference/engine/classes/Mouse) object, the PluginMouse
includes the [PluginMouse.DragEnter](/docs/reference/engine/classes/PluginMouse#DragEnter) function which keeps track of items
being selected while the mouse is dragging.

For more information on how to use mouse objects, see the [Mouse](/docs/reference/engine/classes/Mouse) page.

Code Samples

PluginMouse Get

The code below demonstrates how the PluginMouse object can be obtained and
used in a plugin. To use this code, paste it into a Script save that script
to the local Plugins Folder using right click, save to file. The plugins
folder can be found in the Plugins tab in the Roblox Studio toolbar.

```
plugin:Activate(false) -- gain non exclusive access to the mouse



local mouse = plugin:GetMouse()



local function button1Down()



print("Left mouse click")



end



mouse.Button1Down:Connect(button1Down)
```

---

API Reference

Events

DragEnter

Plugin Security

Fired when Instances are being selected while the mouse is dragging.

PluginMouse.DragEnter(instances:Instances):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| instances:Instances |

Fired when Instances are being selected while the mouse is dragging.

Provide feedback

---