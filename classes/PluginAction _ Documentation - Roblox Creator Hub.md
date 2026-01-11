# PluginAction | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/PluginAction
Scraped: 2026-01-11T02:40:37.510493Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- PluginAction
- PluginToolbarButton
- AllowBinding
- Plugin:CreatePluginAction()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [PluginAction](/docs/reference/engine/classes/PluginAction)

English

Feedback

Engine Class

PluginAction

Not Replicated

---

Summary

Properties

|  |
| --- |
| [ActionId](#ActionId):[string](/docs/luau/strings) |
| [AllowBinding](#AllowBinding):[boolean](/docs/luau/booleans) |
| [StatusTip](#StatusTip):[string](/docs/luau/strings) |
| [Text](#Text):[string](/docs/luau/strings) |

Events

|  |
| --- |
| [Triggered](#Triggered)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

PluginAction represents a generic performable action in Studio with no
directly‑associated [PluginToolbarButton](/docs/reference/engine/classes/PluginToolbarButton). If
[AllowBinding](/docs/reference/engine/classes/PluginAction#AllowBinding) is true, the action can be
assigned a keyboard shortcut through Studio's File ⟩ Customize
Shortcuts window.

A PluginAction must be created using the [Plugin:CreatePluginAction()](/docs/reference/engine/classes/Plugin#CreatePluginAction)
method in order to work as expected.

---

API Reference

Properties

ActionId

Read Only

Not Replicated

Read Parallel

A string that uniquely identifies this action.

PluginAction.ActionId:[string](/docs/luau/strings)

A string that uniquely identifies this action. This string is the key used
when saving and loading the action's state in Roblox Studio.

Provide feedback

---

AllowBinding

Read Only

Not Replicated

Read Parallel

Determines whether the action can be assigned a keyboard shortcut in
Studio.

PluginAction.AllowBinding:[boolean](/docs/luau/booleans)

This property determines whether the action can be assigned a keyboard
shortcut through Studio's File ⟩ Customize Shortcuts window.
Default is true.

Provide feedback

---

StatusTip

Read Only

Not Replicated

Read Parallel

The description of the action when viewing it from the keyboard shortcuts
window in Roblox Studio.

PluginAction.StatusTip:[string](/docs/luau/strings)

The description of the action when viewing it from the keyboard shortcuts
window in Roblox Studio.

Provide feedback

---

Text

Not Replicated

Roblox Script Security

Read Parallel

The text that is displayed when viewing this action in Roblox Studio.

PluginAction.Text:[string](/docs/luau/strings)

The text that is displayed when viewing this action in Roblox Studio.

Provide feedback

---

Events

Triggered

Plugin Security

Fires when the action is triggered.

PluginAction.Triggered():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Fires when the action is triggered, typically through the keyboard
shortcut that it was bound to.

Provide feedback

---