# ChangeHistoryService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ChangeHistoryService
Scraped: 2026-01-11T02:30:38.131646Z

## Tags
- Not Creatable
- Service

## Inherits
- Instance
- ChangeHistoryService
- Object
- ChangeHistoryService:TryBeginRecording()
- ChangeHistoryService:FinishRecording()
- ChangeHistoryService:Undo()
- ChangeHistoryService:Redo()
- TryBeginRecording()
- OnFinishRecording
- FinishRecording()
- SetWaypoint()
- IsRecordingInProgress()
- FinishOperation()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ChangeHistoryService](/docs/reference/engine/classes/ChangeHistoryService)

English

Feedback

Engine Class

ChangeHistoryService

Must be used by plugins to communicate to Studio how to undo and redo the
changes which they make to the experience.

Not Creatable

Service

---

Summary

Methods

|  |
| --- |
| [FinishRecording](#FinishRecording)(identifier: [string](/docs/luau/strings),operation: [Enum.FinishRecordingOperation](/docs/reference/engine/enums/FinishRecordingOperation),finalOptions: [Dictionary](/docs/luau/tables#dictionaries)?):() |
| [GetCanRedo](#GetCanRedo)():[Tuple](/docs/luau/tuples) |
| [GetCanUndo](#GetCanUndo)():[Tuple](/docs/luau/tuples) |
| [IsRecordingInProgress](#IsRecordingInProgress)(identifier: [string](/docs/luau/strings)?):[boolean](/docs/luau/booleans) |
| [Redo](#Redo)():() |
| [ResetWaypoints](#ResetWaypoints)():() |
| [SetEnabled](#SetEnabled)(state: [boolean](/docs/luau/booleans)):() |
| [SetWaypoint](#SetWaypoint)(name: [string](/docs/luau/strings)):() |
| [TryBeginRecording](#TryBeginRecording)(name: [string](/docs/luau/strings),displayName: [string](/docs/luau/strings)?):[string](/docs/luau/strings)? |
| [Undo](#Undo)():() |

Events

|  |
| --- |
| [OnRecordingFinished](#OnRecordingFinished)(name: [string](/docs/luau/strings),displayName: [string](/docs/luau/strings)?,identifier: [string](/docs/luau/strings)?,operation: [Enum.FinishRecordingOperation](/docs/reference/engine/enums/FinishRecordingOperation),finalOptions: [Dictionary](/docs/luau/tables#dictionaries)?):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [OnRecordingStarted](#OnRecordingStarted)(name: [string](/docs/luau/strings),displayName: [string](/docs/luau/strings)?):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [OnRedo](#OnRedo)(waypoint: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [OnUndo](#OnUndo)(waypoint: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Plugin developers must use [ChangeHistoryService](/docs/reference/engine/classes/ChangeHistoryService) to tell Studio how
to undo and redo changes that their plugins make to experiences by recording.
Before making changes, a plugin calls
[ChangeHistoryService:TryBeginRecording()](/docs/reference/engine/classes/ChangeHistoryService#TryBeginRecording), remembering the identifier
it assigns, then after making changes, the Plugin calls
[ChangeHistoryService:FinishRecording()](/docs/reference/engine/classes/ChangeHistoryService#FinishRecording) to complete the recording.

Plugins may also programmatically invoke an undo or redo through
[ChangeHistoryService:Undo()](/docs/reference/engine/classes/ChangeHistoryService#Undo) or [ChangeHistoryService:Redo()](/docs/reference/engine/classes/ChangeHistoryService#Redo).

[ChangeHistoryService](/docs/reference/engine/classes/ChangeHistoryService) is not enabled at runtime, so calling its methods
in a running experience has no effect.

---

API Reference

Methods

FinishRecording

Plugin Security

Communicates to Studio that the identified recording is finished and to
take the final operation to complete the recording.

ChangeHistoryService:FinishRecording(

identifier:[string](/docs/luau/strings), operation:[Enum.FinishRecordingOperation](/docs/reference/engine/enums/FinishRecordingOperation), finalOptions:[Dictionary](/docs/luau/tables#dictionaries)?

):()

Parameters

|  |
| --- |
| identifier:[string](/docs/luau/strings)  Identifies the recording from the previous call to [TryBeginRecording()](/docs/reference/engine/classes/ChangeHistoryService#TryBeginRecording). If the operation is Enum.ChangeHistoryService.FinishRecordingOperation.Cancel, this value is ignored, and the recording is determined by context. |
| operation:[Enum.FinishRecordingOperation](/docs/reference/engine/enums/FinishRecordingOperation)  Specifies the operation to take. |
| finalOptions:[Dictionary](/docs/luau/tables#dictionaries)?  Optional table of values to pass to [OnFinishRecording](/docs/reference/engine/classes/ChangeHistoryService#OnFinishRecording). |

Returns

()

Code Samples

ChangeHistoryService:TryBeginRecording

To commit an undo/redo record, you need to first call
[TryBeginRecording()](/docs/reference/engine/classes/ChangeHistoryService#TryBeginRecording)
followed by calling
[FinishRecording()](/docs/reference/engine/classes/ChangeHistoryService#FinishRecording).

```
local ChangeHistoryService = game:GetService("ChangeHistoryService")



local Selection = game:GetService("Selection")



local toolbar = plugin:CreateToolbar("Example Plugin")



local button = toolbar:CreateButton("Neon it up", "", "")



button.Click:Connect(function()



local parts = {}



for _, part in pairs(Selection:Get()) do



if part:IsA("BasePart") then



parts[#parts + 1] = part



end



end



if #parts < 1 then



-- Nothing to do.



return



end



local recording = ChangeHistoryService:TryBeginRecording("Set selection to neon")



if not recording then



-- Handle error here. This indidcates that your plugin began a previous



-- recording and never completed it. You may only have one recording



-- per plugin active at a time.



return



end



for _, part in pairs(parts) do



part.Material = Enum.Material.Neon



end



ChangeHistoryService:FinishRecording(recording, Enum.FinishRecordingOperation.Commit)



end)
```

Provide feedback

---

GetCanRedo

Plugin Security

Returns whether there are actions that can be redone, and, if there are,
returns the last of them.

ChangeHistoryService:GetCanRedo():[Tuple](/docs/luau/tuples)

Returns

[Tuple](/docs/luau/tuples)

Returns whether there are actions that can be redone, and, if there are,
returns the last of them.

Provide feedback

---

GetCanUndo

Plugin Security

Returns whether there are actions that can be undone, and, if there are,
returns the last of them.

ChangeHistoryService:GetCanUndo():[Tuple](/docs/luau/tuples)

Returns

[Tuple](/docs/luau/tuples)

Returns whether there are actions that can be undone, and, if there are,
returns the last of them.

Provide feedback

---

IsRecordingInProgress

Plugin Security

ChangeHistoryService:IsRecordingInProgress(identifier:[string](/docs/luau/strings)?):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| identifier:[string](/docs/luau/strings)? |

Returns

[boolean](/docs/luau/booleans)

Provide feedback

---

Redo

Plugin Security

Executes the last action that was undone.

ChangeHistoryService:Redo():()

Returns

()

Executes the last action that was undone.

Provide feedback

---

ResetWaypoints

Plugin Security

Clears the history, causing all undo/redo waypoints to be removed.

ChangeHistoryService:ResetWaypoints():()

Returns

()

Clears the history, causing all undo/redo waypoints to be removed.

Provide feedback

---

SetEnabled

Plugin Security

Sets whether or not the ChangeHistoryService is enabled.

ChangeHistoryService:SetEnabled(state:[boolean](/docs/luau/booleans)):()

Parameters

|  |
| --- |
| state:[boolean](/docs/luau/booleans) |

Returns

()

Sets whether or not the ChangeHistoryService is enabled. When set to
false, the undo/redo list is cleared, and does not repopulate. When set to
true again, the original list is not restored, but further operations
append to the list once more

Provide feedback

---

SetWaypoint

Plugin Security

Sets a new waypoint which can be used as an undo or redo point.

ChangeHistoryService:SetWaypoint(name:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings) |

Returns

()

This method will be deprecated soon in favor of
[TryBeginRecording()](/docs/reference/engine/classes/ChangeHistoryService#TryBeginRecording).

[ChangeHistoryService](/docs/reference/engine/classes/ChangeHistoryService) tracks plugin history as a stream of property
changes. [SetWaypoint()](/docs/reference/engine/classes/ChangeHistoryService#SetWaypoint) creates
a cut in that stream of property changes so that the undo and redo actions
know where to stop.

By convention, user-invoked actions in Studio must call
[SetWaypoint()](/docs/reference/engine/classes/ChangeHistoryService#SetWaypoint) *after*
completing their set of changes to the experience. Calling it before a
set of changes may clean up another misbehaving plugin which failed to set
a waypoint, but it's a poor reason to justify such usage in your own
plugin.

Code Samples

ChangeHistoryService:SetWaypoint

In order for the waypoints to work correctly, you need to set one both before
AND after you perform the action that should be able to be undone.

```
local ChangeHistoryService = game:GetService("ChangeHistoryService")



local Selection = game:GetService("Selection")



local toolbar = plugin:CreateToolbar("Example Plugin")



local button = toolbar:CreateButton("Neon it up", "", "")



button.Click:Connect(function()



local parts = {}



for _, part in pairs(Selection:Get()) do



if part:IsA("BasePart") then



parts[#parts + 1] = part



end



end



if #parts > 0 then



-- Calling SetWaypoint before the work will not cause any issues, however



-- it is redundant, only the call AFTER the work is needed.



--ChangeHistoryService:SetWaypoint("Setting selection to neon")



for _, part in pairs(parts) do



part.Material = Enum.Material.Neon



end



-- Call SetWaypoint AFTER completing the work



ChangeHistoryService:SetWaypoint("Set selection to neon")



else



-- Nothing to do. You do not need to call SetWaypoint in the case where



-- the action did not end up making any changes to the experience.



end



end)
```

Provide feedback

---

TryBeginRecording

Plugin Security

Begins tracking changes made to the data model into a recording.

ChangeHistoryService:TryBeginRecording(

name:[string](/docs/luau/strings), displayName:[string](/docs/luau/strings)?

):[string](/docs/luau/strings)?

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  Name of the action being performed suitable for logging and coding purposes. |
| displayName:[string](/docs/luau/strings)?  Name of the action being performed to display to the user. |

Returns

[string](/docs/luau/strings)?

This method begins a recording to track changes to the data model. You
must call it prior to making changes to avoid future warnings or
errors.

When the recording is completed, you call
[FinishRecording()](/docs/reference/engine/classes/ChangeHistoryService#FinishRecording) with the
returned recording identifier to complete the recording and update the
undo/redo stack.

This method will return nil if it fails to begin a recording. Recordings
fail if the plugin already has a recording in progress, or if the user is
in a solo playtest.

You may use
[IsRecordingInProgress()](/docs/reference/engine/classes/ChangeHistoryService#IsRecordingInProgress)
to check the recording status of the plugin.

Code Samples

ChangeHistoryService:TryBeginRecording

To commit an undo/redo record, you need to first call
[TryBeginRecording()](/docs/reference/engine/classes/ChangeHistoryService#TryBeginRecording)
followed by calling
[FinishRecording()](/docs/reference/engine/classes/ChangeHistoryService#FinishRecording).

```
local ChangeHistoryService = game:GetService("ChangeHistoryService")



local Selection = game:GetService("Selection")



local toolbar = plugin:CreateToolbar("Example Plugin")



local button = toolbar:CreateButton("Neon it up", "", "")



button.Click:Connect(function()



local parts = {}



for _, part in pairs(Selection:Get()) do



if part:IsA("BasePart") then



parts[#parts + 1] = part



end



end



if #parts < 1 then



-- Nothing to do.



return



end



local recording = ChangeHistoryService:TryBeginRecording("Set selection to neon")



if not recording then



-- Handle error here. This indidcates that your plugin began a previous



-- recording and never completed it. You may only have one recording



-- per plugin active at a time.



return



end



for _, part in pairs(parts) do



part.Material = Enum.Material.Neon



end



ChangeHistoryService:FinishRecording(recording, Enum.FinishRecordingOperation.Commit)



end)
```

Provide feedback

---

Undo

Plugin Security

Undos the last action taken, for which there exists a waypoint.

ChangeHistoryService:Undo():()

Returns

()

Undos the last action taken, for which there exists a waypoint.

Provide feedback

---

Events

OnRecordingFinished

Plugin Security

Fired when the user completes an action. Parameters come from
[TryBeginRecording()](/docs/reference/engine/classes/ChangeHistoryService#TryBeginRecording) and
[FinishRecording()](/docs/reference/engine/classes/ChangeHistoryService#FinishRecording).

ChangeHistoryService.OnRecordingFinished(

name:[string](/docs/luau/strings), displayName:[string](/docs/luau/strings)?, identifier:[string](/docs/luau/strings)?, operation:[Enum.FinishRecordingOperation](/docs/reference/engine/enums/FinishRecordingOperation), finalOptions:[Dictionary](/docs/luau/tables#dictionaries)?

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  Name of the action being performed suitable for logging and coding purposes. |
| displayName:[string](/docs/luau/strings)?  Name of the action being performed to display to the user. |
| identifier:[string](/docs/luau/strings)?  The identifier for the recording. |
| operation:[Enum.FinishRecordingOperation](/docs/reference/engine/enums/FinishRecordingOperation) |
| finalOptions:[Dictionary](/docs/luau/tables#dictionaries)?  Optional table from  [FinishOperation()](/docs/reference/engine/classes/ChangeHistoryService#FinishOperation). |

Provide feedback

---

OnRecordingStarted

Plugin Security

Fired when the user begins an action. Parameters come from
[TryBeginRecording()](/docs/reference/engine/classes/ChangeHistoryService#TryBeginRecording).

ChangeHistoryService.OnRecordingStarted(

name:[string](/docs/luau/strings), displayName:[string](/docs/luau/strings)?

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  Name of the action being performed suitable for logging and coding purposes. |
| displayName:[string](/docs/luau/strings)?  Name of the action being performed to display to the user. |

Provide feedback

---

OnRedo

Plugin Security

Fired when the user reverses the undo command. Waypoint describes the type
action that has been redone.

ChangeHistoryService.OnRedo(waypoint:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| waypoint:[string](/docs/luau/strings) |

Fired when the user reverses the undo command. Waypoint describes the type
action that has been redone.

Provide feedback

---

OnUndo

Plugin Security

Fired when the user undoes an action in studio. Waypoint describes the
type action that has been undone.

ChangeHistoryService.OnUndo(waypoint:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| waypoint:[string](/docs/luau/strings) |

Fired when the user undoes an action in studio. Waypoint describes the
type action that has been undone.

Provide feedback

---