# Selection | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Selection
Scraped: 2026-01-11T02:28:06.033425Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Object
- Instance
- Selection
- Instances
- Plugins
- Selection:Get()
- Selection:Set()
- Selection.SelectionChanged
- Plugin
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Selection](/docs/reference/engine/classes/Selection)

English

Feedback

Engine Class

Selection

The Selection service controls the [Instances](/docs/reference/engine/classes/Instance) that are
selected in Roblox Studio.

Not Creatable

Service

---

Summary

Properties

|  |
| --- |
| [SelectionThickness](#SelectionThickness):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [Add](#Add)(instancesToAdd: Instances):() |
| [Get](#Get)():Instances |
| [Remove](#Remove)(instancesToRemove: Instances):() |
| [Set](#Set)(selection: Instances):() |

Events

|  |
| --- |
| [SelectionChanged](#SelectionChanged)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The Selection service controls the [Instances](/docs/reference/engine/classes/Instance) that are
selected in Roblox Studio.

This service is particularly useful when developing [Plugins](/docs/reference/engine/classes/Plugin), as
it allows the developer to access and manipulate the current selection.

Currently selected [Instances](/docs/reference/engine/classes/Instance) can be obtained and set using
the [Selection:Get()](/docs/reference/engine/classes/Selection#Get) and [Selection:Set()](/docs/reference/engine/classes/Selection#Set) functions. The
[Selection.SelectionChanged](/docs/reference/engine/classes/Selection#SelectionChanged) event fires whenever the current selection
changes.

For more information on using [Selection](/docs/reference/engine/classes/Selection) and [Plugins](/docs/reference/engine/classes/Plugin),
see [Plugin](/docs/reference/engine/classes/Plugin).

Selection is also often used in the command bar, to set hidden properties or
run functions for selected [Instances](/docs/reference/engine/classes/Instance).

Note this class only applies to Roblox Studio and has no applicability to
games.

Code Samples

Selection

The following code sample, when used in a plugin or the command bar, will
rotate currently selected BaseParts.

```
local Selection = game:GetService("Selection")



for _, object in pairs(Selection:Get()) do



if object:IsA("BasePart") then



object.CFrame = object.CFrame * CFrame.Angles(0, math.pi / 2, 0)



end



end
```

---

API Reference

Properties

SelectionThickness

Read Only

Not Replicated

Read Parallel

Selection.SelectionThickness:[number](/docs/luau/numbers)

Provide feedback

---

Methods

Add

Plugin Security

Selection:Add(instancesToAdd:Instances):()

Parameters

|  |
| --- |
| instancesToAdd:Instances |

Returns

()

Provide feedback

---

Get

Plugin Security

Returns an array of currently selected [Instances](/docs/reference/engine/classes/Instance) in
Roblox Studio.

Selection:Get():Instances

Returns

Instances

An array of currently selected [Instances](/docs/reference/engine/classes/Instance).

Returns an array of currently selected [Instances](/docs/reference/engine/classes/Instance) in
Roblox Studio.

If no [Instances](/docs/reference/engine/classes/Instance) are selected, the array returned will be
empty. This function can be used in conjunction with the
[Selection.SelectionChanged](/docs/reference/engine/classes/Selection#SelectionChanged) event to get the selection whenever it
changes.

Note, this function can only be used in [Plugins](/docs/reference/engine/classes/Plugin) or the
command line.

For changing the current selection, please see [Selection:Set()](/docs/reference/engine/classes/Selection#Set).

Code Samples

Selection

The following code sample, when used in a plugin or the command bar, will
rotate currently selected BaseParts.

```
local Selection = game:GetService("Selection")



for _, object in pairs(Selection:Get()) do



if object:IsA("BasePart") then



object.CFrame = object.CFrame * CFrame.Angles(0, math.pi / 2, 0)



end



end
```

Selection.SelectionChanged

This example prints the number of selected items whenever SelectionChanged is
fired:

```
local selection = game:GetService("Selection")



selection.SelectionChanged:Connect(function()



print("Selection contains " .. #selection:Get() .. " items.")



end)
```

Provide feedback

---

Remove

Plugin Security

Selection:Remove(instancesToRemove:Instances):()

Parameters

|  |
| --- |
| instancesToRemove:Instances |

Returns

()

Provide feedback

---

Set

Plugin Security

Sets the currently selected objects in Roblox Studio to
[Instances](/docs/reference/engine/classes/Instance) in the given array.

Selection:Set(selection:Instances):()

Parameters

|  |
| --- |
| selection:Instances  An array of [Instances](/docs/reference/engine/classes/Instance) to set the current selection to. |

Returns

()

Sets the currently selected objects in Roblox Studio to
[Instances](/docs/reference/engine/classes/Instance) in the given array.

Calling this function will cause the [Selection.SelectionChanged](/docs/reference/engine/classes/Selection#SelectionChanged)
event to fire, unless the new selection set is identical to the previous
selection.

Note this function overwrites the existing selection. However, using
[Selection:Get()](/docs/reference/engine/classes/Selection#Get) an [Instance](/docs/reference/engine/classes/Instance) can be added to the existing
selection like so:

```
local selected = Selection:Get()



table.insert(selected, object)



Selection:Set(selected)
```

Code Samples

Selection Set

This code sample will select every BasePart in the workspace that is Bright
red.

```
local Selection = game:GetService("Selection")



local newSelection = {}



for _, object in pairs(workspace:GetDescendants()) do



if object:IsA("BasePart") and object.BrickColor == BrickColor.new("Bright red") then



table.insert(newSelection, object)



end



end



Selection:Set(newSelection)
```

Provide feedback

---

Events

SelectionChanged

Fires when the [Instances](/docs/reference/engine/classes/Instance) selected in Roblox Studio
changes.

Selection.SelectionChanged():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Fires when the [Instances](/docs/reference/engine/classes/Instance) selected in Roblox Studio
changes.

Note this event does not give the new selection. Developers will need to
use the [Selection:Get()](/docs/reference/engine/classes/Selection#Get) function to obtain the current selection.

Although this event can be used outside of plugins and the command bar, it
only applies to the selection in Roblox Studio and therefore has no
functionality outside of Studio.

To change the selection use the [Selection:Set()](/docs/reference/engine/classes/Selection#Set) function.

Code Samples

Selection.SelectionChanged

This example prints the number of selected items whenever SelectionChanged is
fired:

```
local selection = game:GetService("Selection")



selection.SelectionChanged:Connect(function()



print("Selection contains " .. #selection:Get() .. " items.")



end)
```

Provide feedback

---