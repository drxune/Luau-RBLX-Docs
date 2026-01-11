# ScriptEditorService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ScriptEditorService
Scraped: 2026-01-11T02:40:09.414385Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Instance
- ScriptEditorService
- ScriptDocument
- LuaSourceContainer
- Object
- ScriptDocument.ViewportChanged
- Script.Source
- ScriptEditorService:GetScriptDocuments()
- Script
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ScriptEditorService](/docs/reference/engine/classes/ScriptEditorService)

English

Feedback

Engine Class

ScriptEditorService

This service is used for interacting with [ScriptDocument](/docs/reference/engine/classes/ScriptDocument) instances.

Not Creatable

Service

Not Replicated

---

Summary

Methods

|  |
| --- |
| [DeregisterAutocompleteCallback](#DeregisterAutocompleteCallback)(name: [string](/docs/luau/strings)):() |
| [DeregisterScriptAnalysisCallback](#DeregisterScriptAnalysisCallback)(name: [string](/docs/luau/strings)):() |
| [FindScriptDocument](#FindScriptDocument)(script: [LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer)):[ScriptDocument](/docs/reference/engine/classes/ScriptDocument) |
| [GetEditorSource](#GetEditorSource)(script: [LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer)):[string](/docs/luau/strings) |
| [GetScriptDocuments](#GetScriptDocuments)():Instances |
| [OpenScriptDocumentAsync](#OpenScriptDocumentAsync)(script: [LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer),options: [Dictionary](/docs/luau/tables#dictionaries)):[Tuple](/docs/luau/tuples) |
| [RegisterAutocompleteCallback](#RegisterAutocompleteCallback)(name: [string](/docs/luau/strings),priority: [number](/docs/luau/numbers),callbackFunction: [function](/docs/luau/functions)):() |
| [RegisterScriptAnalysisCallback](#RegisterScriptAnalysisCallback)(name: [string](/docs/luau/strings),priority: [number](/docs/luau/numbers),callbackFunction: [function](/docs/luau/functions)):() |
| [UpdateSourceAsync](#UpdateSourceAsync)(script: [LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer),callback: [function](/docs/luau/functions)):() |

Events

|  |
| --- |
| [TextDocumentDidChange](#TextDocumentDidChange)(document: [ScriptDocument](/docs/reference/engine/classes/ScriptDocument),changesArray: Variant):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TextDocumentDidClose](#TextDocumentDidClose)(oldDocument: [ScriptDocument](/docs/reference/engine/classes/ScriptDocument)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TextDocumentDidOpen](#TextDocumentDidOpen)(newDocument: [ScriptDocument](/docs/reference/engine/classes/ScriptDocument)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

This service is used for interacting with [ScriptDocument](/docs/reference/engine/classes/ScriptDocument) instances.

---

API Reference

Methods

DeregisterAutocompleteCallback

Plugin Security

Removes a previously registered callback with the name name.

ScriptEditorService:DeregisterAutocompleteCallback(name:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings) |

Returns

()

Removes a previously registered callback with the name name.

Code Samples

ScriptEditorService:DeregisterAutocompleteCallback

```
game.ScriptEditorService:DeregisterAutocompleteCallback("foo")
```

Provide feedback

---

DeregisterScriptAnalysisCallback

Plugin Security

Removes a previously registered callback with the name name.

ScriptEditorService:DeregisterScriptAnalysisCallback(name:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings) |

Returns

()

Removes a previously registered callback with the name name.

Code Samples

ScriptEditorService:DeregisterScriptAnalysisCallback

```
local ScriptEditorService = game:GetService("ScriptEditorService")



ScriptEditorService:DeregisterScriptAnalysisCallback("foo")
```

Provide feedback

---

FindScriptDocument

Plugin Security

Returns the open [ScriptDocument](/docs/reference/engine/classes/ScriptDocument) corresponding to the given
[LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer), or nil if the given script is not open.

ScriptEditorService:FindScriptDocument(script:[LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer)):[ScriptDocument](/docs/reference/engine/classes/ScriptDocument)

Parameters

|  |
| --- |
| script:[LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer) |

Returns

[ScriptDocument](/docs/reference/engine/classes/ScriptDocument)

Returns the open [ScriptDocument](/docs/reference/engine/classes/ScriptDocument) corresponding to the given
[LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer), or nil if the given script is not open.

Code Samples

ScriptDocument:CloseAsync

ScriptDocument:CloseAsync

```
--!nocheck



-- Run the following code in the Command Bar



local ScriptEditorService = game:GetService("ScriptEditorService")



local documents = ScriptEditorService:GetScriptDocuments()



local scriptDocument



-- Find the first open script document



for _, document in documents do



-- The Command Bar can't be closed, so don't select it



if not document:IsCommandBar() then



scriptDocument = document



break



end



end



if scriptDocument then



local success, err = scriptDocument:CloseAsync()



if success then



print(`Closed {scriptDocument.Name}`)



else



warn(`Failed to close {scriptDocument.Name} because: {err}`)



end



else



print("No open scripts")



end
```

Connecting to ScriptDocument.ViewportChanged

Demonstrates using [ScriptDocument.ViewportChanged](/docs/reference/engine/classes/ScriptDocument#ViewportChanged) to print the start and end line of the script's viewport when it changes.

To run:

1. Ensure Output view is open
2. Run the below code in the Command Bar
3. Scroll up and down in the opened Script window

```
--!nocheck



--[[



To run:



1. Ensure Output view is open



2. Run the below code in the Command Bar



3. Scroll up and down in the opened Script window



Print statements from the ViewportChanged event will appear in the Output



]]



local Workspace = game:GetService("Workspace")



local ScriptEditorService = game:GetService("ScriptEditorService")



-- Create text that spans many lines



local dummyText = string.rep("-- Dummy Text\n", 60)



-- Create a script containing the dummy text and open it



local otherScript = Instance.new("Script")



otherScript.Source = dummyText



otherScript.Parent = Workspace



local success, err = ScriptEditorService:OpenScriptDocumentAsync(otherScript)



if not success then



warn(`Failed to open script because: {err}`)



return



end



-- Get a reference to the opened script



local scriptDocument = ScriptEditorService:FindScriptDocument(otherScript)



local function onViewportChanged(startLine: number, endLine: number)



print(`Script Viewport Changed - startLine: {startLine}, endLine: {endLine}`)



end



-- Connect the ViewportChanged event to the function above that prints the start and end line of the updated viewport



scriptDocument.ViewportChanged:Connect(onViewportChanged)
```

Provide feedback

---

GetEditorSource

Plugin Security

Returns the edit-time source for the given script.

ScriptEditorService:GetEditorSource(script:[LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| script:[LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer) |

Returns

[string](/docs/luau/strings)

Returns the edit-time source for the given script.

If the script is open in the
[Script Editor](/docs/studio/script-editor), this method returns the
text currently being displayed in the editor. If the script is not open in
the editor, the method returns the text that the editor would display if
it's opened. The edit-time source is not always be consistent with the
[Script.Source](/docs/reference/engine/classes/Script#Source) property.

Provide feedback

---

GetScriptDocuments

Plugin Security

Returns an array of the currently open script documents, including the
command bar.

ScriptEditorService:GetScriptDocuments():Instances

Returns

Instances

Returns an array of the currently open script documents, including the
command bar.

Code Samples

Print the name of every script

Gets all script documents in the place with [ScriptEditorService:GetScriptDocuments()](/docs/reference/engine/classes/ScriptEditorService#GetScriptDocuments) and prints their names.

```
--!nocheck



-- Run the following code in the Command Bar



local ScriptEditorService = game:GetService("ScriptEditorService")



local scriptDocuments = ScriptEditorService:GetScriptDocuments()



for _, scriptDocument in scriptDocuments do



-- Prints the name of each script



if not scriptDocument:IsCommandBar() then



print(scriptDocument.Name)



end



end
```

Provide feedback

---

OpenScriptDocumentAsync

Yields

Plugin Security

Requests that a Script Editor open the specified script. Returns (true,
nil) if the request succeeds. Returns (false, string) if the request
fails, with a string that describes the problem.

ScriptEditorService:OpenScriptDocumentAsync(

script:[LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer), options:[Dictionary](/docs/luau/tables#dictionaries)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| script:[LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer) |
| options:[Dictionary](/docs/luau/tables#dictionaries) Default Value: "nil" |

Returns

[Tuple](/docs/luau/tuples)

Requests that a Script Editor open the specified script. Returns (true,
nil) if the request succeeds. Returns (false, string) if the request
fails, with a string that describes the problem.

If the script is already open, this function succeeds and switches tabs to
the associated editor.

Code Samples

ScriptEditorService:OpenScriptDocumentAsync

ScriptEditorService:OpenScriptDocumentAsync

```
--!nocheck



-- Run the following code in the Command Bar



local ScriptEditorService = game:GetService("ScriptEditorService")



local Workspace = game:GetService("Workspace")



local newScript = Instance.new("Script")



newScript.Parent = Workspace



local success, err = ScriptEditorService:OpenScriptDocumentAsync(newScript)



if success then



print("Opened script document")



else



print(`Failed to open script document: {err}`)



end
```

Provide feedback

---

RegisterAutocompleteCallback

Plugin Security

Registers an autocomplete callback callbackFunction named name with
priority priority.

ScriptEditorService:RegisterAutocompleteCallback(

name:[string](/docs/luau/strings), priority:[number](/docs/luau/numbers), callbackFunction:[function](/docs/luau/functions)

):()

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings) |
| priority:[number](/docs/luau/numbers) |
| callbackFunction:[function](/docs/luau/functions) |

Returns

()

Registers an autocomplete callback callbackFunction named name with
priority priority.

When the Script Editor invokes autocomplete, all registered autocomplete
callbacks call in order of ascending priority with the autocomplete
request and response. Multiple callbacks may share a priority, but then
their calling order is unpredictable. Each callback is intended to return
a response table with the same format as the response input table.
Callbacks shouldn't yield. The first callback invoked receives the
internal autocomplete's response as its response table, and subsequent
callbacks receive the previous callback's output as their response table.
Callbacks may either modify the passed table or return a new table of the
same format.

The callbackFunction must have the following type:
(Request: table, Response: table) -> table

The Request table has the following format:

```
type Request = {



position: {



line: number,



character: number



},



textDocument: {



document: ScriptDocument?,



script: LuaSourceContainer?



}



}
```

* position is the one-indexed cursor position where you are
  autocompleting.
* textDocument.document is the open [ScriptDocument](/docs/reference/engine/classes/ScriptDocument) you are
  completing in, if it exists.
* textDocument.script is the [LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer) you are
  completing in, if it exists.

If both textDocument.document and textDocument.script are present,
then they correspond to each other:
req.textDocument.document:GetScript() == req.textDocument.script

The Response table has the following format:

```
type Response = {



items: {



{



label: string, -- The label



kind: Enum.CompletionItemKind?,



tags: {Enum.CompletionItemTag}?,



detail: string?,



documentation: {



value: string,



}?,



overloads: number?,



learnMoreLink: string?,



codeSample: string?,



preselect: boolean?,



textEdit: {



newText: string,



insert: { start: { line: number, character: number }, ["end"]: { line: number, character: number } },



replace: { start: { line: number, character: number }, ["end"]: { line: number, character: number } },



}?



}



}



}
```

* Response.items is an array of the completion items. The order of this
  array is insignificant, and it resorts in the editor as the user types.
* Response.items[n].label is the label of the item which display in the
  autocomplete menu.
* Response.items[n].kind specifies what type of autocomplete item this
  is. Primarily this controls the icon given to the item in the editor.
  Not all kinds have a unique icon. If not specified, the editor uses the
  "Text" icon. Unsupported kinds default to displaying the "Property"
  icon.
* Response.items[n].tags specifies an array of tags describing this
  completion item. See the [Enum.CompletionItemTag](/docs/reference/engine/enums/CompletionItemTag) for details on their
  function.
* Response.items[n].details specifies a string describing details about
  the completion item. For default items, this is a string representation
  of their type. Note that, in order for the documentation widget to
  display, documentation must be present, but documentation.value may
  be empty.
* Response.items[n].documentation specifies the main body of the
  documentation in its value field. documentation is present, even if
  value is empty, so the documentation window displays if either details
  or overloads are specified.
* Response.items[n].overloads specifies the number of overloads of a
  function autocompletion.
* Response.items[n].learnMoreLink links to a relevant page on the
  creator docs. This URL must be a https request to create.roblox.com;
  no other URLs display in the editor.
* Response.items[n].codeSample specifies a sample use of the completion
  item. documentation must be non-empty to display this field.
* Response.items[n].preselect If true, the editor sorts this completion
  item ahead of all others and selects it for the user by default. No
  effect if false or missing.
* Response.items[n].textEdit If present, accepting the completion
  applies this text edit - inserting or replacing the span between the
  positions start and end with newText.

If a callback returns a malformed result or encounters an error, the
editor discards the modified Response table and uses the built-in
autocomplete result list.

Code Samples

ScriptEditorService:RegisterAutocompleteCallback
ScriptEditorService:DeregisterAutocompleteCallback

ScriptEditorService:RegisterAutocompleteCallback
ScriptEditorService:DeregisterAutocompleteCallback

```
--!nocheck



-- Run the following code in the Command Bar



local ScriptEditorService = game:GetService("ScriptEditorService")



type Request = {



position: {



line: number,



character: number,



},



textDocument: {



document: ScriptDocument?,



script: LuaSourceContainer?,



},



}



type Response = {



items: {



{



label: string,



kind: Enum.CompletionItemKind?,



tags: { Enum.CompletionItemTag }?,



detail: string?,



documentation: {



value: string,



}?,



overloads: number?,



learnMoreLink: string?,



codeSample: string?,



preselect: boolean?,



textEdit: {



newText: string,



replace: {



start: { line: number, character: number },



["end"]: { line: number, character: number },



},



}?,



}



},



}



local autocompleteCallback = function(request: Request, response: Response): Response



local item = {



label = "foo",



preselect = true,



}



table.insert(response.items, item)



return response



end



ScriptEditorService:RegisterAutocompleteCallback("foo", 1, autocompleteCallback)



-- To deregister the callback, run the following code in the Command Bar



ScriptEditorService:DeregisterAutocompleteCallback("foo")
```

Provide feedback

---

RegisterScriptAnalysisCallback

Plugin Security

Registers a Script Analysis callback callbackFunction named name with
priority.

ScriptEditorService:RegisterScriptAnalysisCallback(

name:[string](/docs/luau/strings), priority:[number](/docs/luau/numbers), callbackFunction:[function](/docs/luau/functions)

):()

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings) |
| priority:[number](/docs/luau/numbers) |
| callbackFunction:[function](/docs/luau/functions) |

Returns

()

Registers a Script Analysis callback callbackFunction named name with
priority. When Script Analysis in Studio runs, all registered callbacks
call in order of ascending priority. Each callback is intended to return a
response table matching the format specified below. Callbacks should not
yield.

The request table has the following format, where script is the
LuaSourceContainer that is going to be analyzed.

```
type Request = {



script: LuaSourceContainer?



}
```

The response table has the following format, where diagnostics is an
array of diagnostic tables. Each diagnostic table has the entries listed
below.

```
type Response = {



diagnostics: {



{



range: {



start: {



line: number,



character: number,



},



["end"]: {



line: number,



character: number,



}



},



code: string?,



message: string,



severity: Enum.Severity?,



codeDescription: { href: string }?



}



}



}
```

* range represents a text range that should be highlighted by the
  linter, providing what line/character to start highlighting and what
  line/character to stop highlighting.
* code is a label for the message.
* message is a warning message to be displayed for the line. This will
  also appear on a tooltip when the user hovers their cursor over the line
  in the Script Editor.
* severity is a [Enum.Severity](/docs/reference/engine/enums/Severity) value for the diagnostics. This
  determines how the diagnostic is categorized in the Script Analysis tool
  in Studio, as well as how text is highlighted in the Script Editor.
* codeDescription links to a relevant page on the creator docs. This URL
  must be an https request to create.roblox.com; no other URLs display
  in the editor.

Code Samples

ScriptEditorService:RegisterScriptAnalysisCallback

```
type Request = {



["script"]: LuaSourceContainer,



}



type Response = {



diagnostics: {



{



range: {



start: {



line: number,



character: number,



},



["end"]: {



line: number,



character: number,



},



},



code: string?,



message: string,



severity: Enum.Severity?,



codeDescription: { href: string }?,



}



},



}



local ScriptEditorService = game:GetService("ScriptEditorService")



ScriptEditorService:RegisterScriptAnalysisCallback("foo", 1, function(Req: Request): Response



local response = {



diagnostics = {},



}



local lineNo = 1



-- Iterate line by line



for text, newline in Req.script.Source:gmatch("([^\r\n]*)([\r\n]*)") do



local startIndex, endIndex = string.find(text, "Foo")



if startIndex and endIndex then



table.insert(response.diagnostics, {



range = {



["start"] = {



line = lineNo,



character = startIndex,



},



["end"] = {



line = lineNo,



character = endIndex,



},



},



code = "FooFinder",



message = "Foo found here!",



severity = Enum.Severity.Warning,



})



end



lineNo = lineNo + #newline:gsub("\n+", "\0%0\0"):gsub(".%z.", "."):gsub("%z", "")



end



return response



end)
```

Provide feedback

---

UpdateSourceAsync

Yields

Plugin Security

Generates new content from the old script and updates the script editor if
it's open, or the [Script](/docs/reference/engine/classes/Script) instance if the script editor is closed.

ScriptEditorService:UpdateSourceAsync(

script:[LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer), callback:[function](/docs/luau/functions)

):()

Parameters

|  |
| --- |
| script:[LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer)  Script instance to be updated. |
| callback:[function](/docs/luau/functions)  The function to return new script content. |

Returns

()

Returns the edit-time [Script.Source](/docs/reference/engine/classes/Script#Source) for the given script.

This function calls the passed callback using the old contents of the
script to calculate the new contents of the script.

If the script is open in the
[Script Editor](/docs/studio/script-editor), then it issues a
request to the editor to update its source. The editor may reject this
update if the [Script.Source](/docs/reference/engine/classes/Script#Source) property was out of date with the
user's version of the script when this function was called, in which case
the callback will be re-invoked and the attempt will be repeated.

The callback may not yield. If the callback returns nil, the operation
is cancelled. This function yields until the operation is cancelled or
succeeds.

If the script is not open in the editor, the new content updates to the
script source, which is the text the editor would display if it is opened.

```
local ses = game:GetService('ScriptEditorService')



ses:UpdateSourceAsync(Workspace.Script, function(oldContent)



return oldContent .. " World!"



end)
```

Provide feedback

---

Events

TextDocumentDidChange

Plugin Security

Fires just after a [ScriptDocument](/docs/reference/engine/classes/ScriptDocument) changes.

ScriptEditorService.TextDocumentDidChange(

document:[ScriptDocument](/docs/reference/engine/classes/ScriptDocument), changesArray:Variant

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| document:[ScriptDocument](/docs/reference/engine/classes/ScriptDocument) |
| changesArray:Variant |

Fires just after a [ScriptDocument](/docs/reference/engine/classes/ScriptDocument) changes. The textChanged is an
array of change structures of the format:

{ range : { start : { line : number, character : number }, end : { line : number, character : number } }, text: string }

Code Samples

ScriptEditorService.TextDocumentDidChange

ScriptEditorService.TextDocumentDidChange

```
--!nocheck



-- Run the following code in the Command Bar



local ScriptEditorService = game:GetService("ScriptEditorService")



ScriptEditorService.TextDocumentDidChange:Connect(function(scriptDocument, changes)



print("Changed", scriptDocument, changes)



end)
```

Provide feedback

---

TextDocumentDidClose

Plugin Security

Fires just before a [ScriptDocument](/docs/reference/engine/classes/ScriptDocument) object is destroyed, which
happens right after the script editor closes.

ScriptEditorService.TextDocumentDidClose(oldDocument:[ScriptDocument](/docs/reference/engine/classes/ScriptDocument)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| oldDocument:[ScriptDocument](/docs/reference/engine/classes/ScriptDocument) |

Fires just before a [ScriptDocument](/docs/reference/engine/classes/ScriptDocument) object is destroyed, which
happens right after the script editor closes. After this event fires, the
[ScriptDocument](/docs/reference/engine/classes/ScriptDocument) enters a "Closed" state, and trying to call its
methods throws an error. [ScriptDocument](/docs/reference/engine/classes/ScriptDocument) objects aren't reusable,
even if the script editor reopens the same script.

Code Samples

ScriptEditorService.TextDocumentDidClose

ScriptEditorService.TextDocumentDidClose

```
--!nocheck



-- Run the following code in the Command Bar



local ScriptEditorService = game:GetService("ScriptEditorService")



ScriptEditorService.TextDocumentDidClose:Connect(function(scriptDocument)



print("Closed", scriptDocument)



end)
```

Provide feedback

---

TextDocumentDidOpen

Plugin Security

Fires just after a [ScriptDocument](/docs/reference/engine/classes/ScriptDocument) object is created and parented
to the service, which happens right after the script editor opens.

ScriptEditorService.TextDocumentDidOpen(newDocument:[ScriptDocument](/docs/reference/engine/classes/ScriptDocument)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| newDocument:[ScriptDocument](/docs/reference/engine/classes/ScriptDocument) |

Fires just after a [ScriptDocument](/docs/reference/engine/classes/ScriptDocument) object is created and parented
to the service, which happens right after the script editor opens.

Code Samples

ScriptEditorService.TextDocumentDidOpen

ScriptEditorService.TextDocumentDidOpen

```
--!nocheck



-- Run the following code in the Command Bar



local ScriptEditorService = game:GetService("ScriptEditorService")



ScriptEditorService.TextDocumentDidOpen:Connect(function(scriptDocument)



print("Opened", scriptDocument)



end)
```

Provide feedback

---