# ScriptDocument | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ScriptDocument
Scraped: 2026-01-11T02:42:45.452261Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Instance
- ScriptDocument
- LuaSourceContainer
- Object
- DataModel
- ScriptEditorService
- TextBox.CursorPosition
- ScriptDocument:RequestSetSelectionAsync()
- ScriptDocument.GetViewport
- ScriptDocument.ViewportChanged
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ScriptDocument](/docs/reference/engine/classes/ScriptDocument)

English

Feedback

Engine Class

ScriptDocument

Not Creatable

Not Replicated

---

Summary

Methods

|  |
| --- |
| [CloseAsync](#CloseAsync)():[Tuple](/docs/luau/tuples) |
| [EditTextAsync](#EditTextAsync)(newText: [string](/docs/luau/strings),startLine: [number](/docs/luau/numbers),startCharacter: [number](/docs/luau/numbers),endLine: [number](/docs/luau/numbers),endCharacter: [number](/docs/luau/numbers)):[Tuple](/docs/luau/tuples) |
| [ForceSetSelectionAsync](#ForceSetSelectionAsync)(cursorLine: [number](/docs/luau/numbers),cursorCharacter: [number](/docs/luau/numbers),anchorLine: [number](/docs/luau/numbers)?,anchorCharacter: [number](/docs/luau/numbers)?):[Tuple](/docs/luau/tuples) |
| [GetLine](#GetLine)(lineIndex: [number](/docs/luau/numbers)?):[string](/docs/luau/strings) |
| [GetLineCount](#GetLineCount)():[number](/docs/luau/numbers) |
| [GetScript](#GetScript)():[LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer) |
| [GetSelectedText](#GetSelectedText)():[string](/docs/luau/strings) |
| [GetSelection](#GetSelection)():[Tuple](/docs/luau/tuples) |
| [GetSelectionEnd](#GetSelectionEnd)():[Tuple](/docs/luau/tuples) |
| [GetSelectionStart](#GetSelectionStart)():[Tuple](/docs/luau/tuples) |
| [GetText](#GetText)(startLine: [number](/docs/luau/numbers)?,startCharacter: [number](/docs/luau/numbers)?,endLine: [number](/docs/luau/numbers)?,endCharacter: [number](/docs/luau/numbers)?):[string](/docs/luau/strings) |
| [GetViewport](#GetViewport)():[Tuple](/docs/luau/tuples) |
| [HasSelectedText](#HasSelectedText)():[boolean](/docs/luau/booleans) |
| [IsCommandBar](#IsCommandBar)():[boolean](/docs/luau/booleans) |
| [MultiEditTextAsync](#MultiEditTextAsync)(edits: [Array](/docs/luau/tables#arrays)):[Tuple](/docs/luau/tuples) |
| [RequestSetSelectionAsync](#RequestSetSelectionAsync)(cursorLine: [number](/docs/luau/numbers),cursorCharacter: [number](/docs/luau/numbers),anchorLine: [number](/docs/luau/numbers)?,anchorCharacter: [number](/docs/luau/numbers)?):[Tuple](/docs/luau/tuples) |

Events

|  |
| --- |
| [SelectionChanged](#SelectionChanged)(positionLine: [number](/docs/luau/numbers),positionCharacter: [number](/docs/luau/numbers),anchorLine: [number](/docs/luau/numbers),anchorCharacter: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [ViewportChanged](#ViewportChanged)(startLine: [number](/docs/luau/numbers),endLine: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A [ScriptDocument](/docs/reference/engine/classes/ScriptDocument) instance is a proxy of the document of a Studio
Script Editor. It's different from the [LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer) open in the
editor in that it represents the ephemeral state of an open document, and its
representation is in a format that's more suited for reading and editing code
than executing it. In particular, [ScriptDocument](/docs/reference/engine/classes/ScriptDocument) reflects any changes
that have been made to the open script in Drafts Mode, which the source
property doesn't.

The Script Editor itself exists and changes on a different thread than any
[DataModel](/docs/reference/engine/classes/DataModel), so the [ScriptDocument](/docs/reference/engine/classes/ScriptDocument) replicates the open Script
Editor, but it isn't the open editor. Because of the replication, there's
sometimes a slight delay between changing the text in the editor and updating
the [ScriptDocument](/docs/reference/engine/classes/ScriptDocument). The delay usually occurs because the
[DataModel](/docs/reference/engine/classes/DataModel) is busy, and it's almost always extremely small, but it
still exists.

The existence of a [ScriptDocument](/docs/reference/engine/classes/ScriptDocument) indicates that a document is open in
the Script Editor. All [ScriptDocument](/docs/reference/engine/classes/ScriptDocument) instances have
[ScriptEditorService](/docs/reference/engine/classes/ScriptEditorService) as its parent. Each instance adheres to the
following encoding conventions:

* All text in [ScriptDocument](/docs/reference/engine/classes/ScriptDocument) is UTF-8 encoded.
* All line indices are 1-indexed.
* All character indices are 1-indexed and count UTF-8 bytes, not graphemes, so
  the same warning from [TextBox.CursorPosition](/docs/reference/engine/classes/TextBox#CursorPosition) applies: many Unicode
  characters take more than one byte.
* All ranges are inclusive of their start position and exclusive of their end
  position, so start == end implies an empty range.

All APIs for [ScriptDocument](/docs/reference/engine/classes/ScriptDocument) are at Plugin level security.

---

API Reference

Methods

CloseAsync

Yields

Plugin Security

Requests that the editor associated with this document close. Yields the
current thread until the editor responds to the request.

ScriptDocument:CloseAsync():[Tuple](/docs/luau/tuples)

Returns

[Tuple](/docs/luau/tuples)

Requests that the editor associated with this document close. Yields the
current thread until the editor responds to the request. If the function
succeeds, it returns (true, nil). If the function fails, it returns
(false, string) as a description of the problem.

This function can't close the command bar.

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

Provide feedback

---

EditTextAsync

Yields

Plugin Security

Replaces the text in the specified range from (startLine, startColumn)
to (endLine, endColumn) with newText.

ScriptDocument:EditTextAsync(

newText:[string](/docs/luau/strings), startLine:[number](/docs/luau/numbers), startCharacter:[number](/docs/luau/numbers), endLine:[number](/docs/luau/numbers), endCharacter:[number](/docs/luau/numbers)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| newText:[string](/docs/luau/strings) |
| startLine:[number](/docs/luau/numbers) |
| startCharacter:[number](/docs/luau/numbers) |
| endLine:[number](/docs/luau/numbers) |
| endCharacter:[number](/docs/luau/numbers) |

Returns

[Tuple](/docs/luau/tuples)

Replaces the text in the specified range from (startLine, startColumn)
to (endLine, endColumn) with newText. If the range is empty, then
the function inserts the text at (startLine, startColumn). If the text
cursor is within the specified range, the cursor moves to the end position
of the edit. Otherwise, the text cursor doesn't move. This function yields
the current thread until it receives a reply from the editor about the
edit.

If the function succeeds, it returns (true, nil).

The function throws an error if:

* The range is invalid.
* The range would slice a unicode character, for example replace only some
  of the bytes of the unicode character.
* The newText itself contains invalid UTF-8.

If the function fails, it returns (false, string). The string is a
description of the problem. The most common failure type is a version
mismatch. This occurs when you try to call EditTextAsync during the time
when the [ScriptDocument](/docs/reference/engine/classes/ScriptDocument) is out of sync with the contents of the
editor. If this happens, you can retry the edit.

Provide feedback

---

ForceSetSelectionAsync

Yields

Plugin Security

Asks the editor to set its cursor selection to the argument values.

ScriptDocument:ForceSetSelectionAsync(

cursorLine:[number](/docs/luau/numbers), cursorCharacter:[number](/docs/luau/numbers), anchorLine:[number](/docs/luau/numbers)?, anchorCharacter:[number](/docs/luau/numbers)?

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| cursorLine:[number](/docs/luau/numbers) |
| cursorCharacter:[number](/docs/luau/numbers) |
| anchorLine:[number](/docs/luau/numbers)? Default Value: "nil" |
| anchorCharacter:[number](/docs/luau/numbers)? Default Value: "nil" |

Returns

[Tuple](/docs/luau/tuples)

Asks the editor to set its cursor selection to the argument values. Both
anchor arguments must be passed, or neither. If neither is passed, then
they each default to being the same as the corresponding cursor argument.
The editor might decline to update its cursor if the text content of the
document has changed. Unlike
[ScriptDocument:RequestSetSelectionAsync()](/docs/reference/engine/classes/ScriptDocument#RequestSetSelectionAsync), the editor will not
decline to move its cursor if the cursor has moved since the request was
made. Returns (true, nil) if the cursor was updated, and (false, string)
with an explanation string if it was not. Yields the current thread until
the editor replies.

Code Samples

ScriptDocument:ForceSetSelectionAsync()

ScriptDocument:ForceSetSelectionAsync()

```
--!nocheck



-- Run the following code in the Command Bar while a script is open



local ScriptEditorService = game:GetService("ScriptEditorService")



local function getFirstOpenDocument()



local documents = ScriptEditorService:GetScriptDocuments()



for _, document in documents do



if not document:IsCommandBar() then



return document



end



end



return nil



end



local scriptDocument = getFirstOpenDocument()



if scriptDocument then



-- Get the text on the cursor's current line



local cursorLine = scriptDocument:GetSelection()



local lineText = scriptDocument:GetLine(cursorLine)



-- Force select the entire line of text



local success, err = scriptDocument:ForceSetSelectionAsync(cursorLine, 1, cursorLine, #lineText + 1)



if success then



print("Set selection!")



else



print(`Failed to set selection because: {err}`)



end



else



print("No scripts open")



end
```

Provide feedback

---

GetLine

Plugin Security

Returns the text of the specified line. When no argument is provided,
returns the line of the current cursor position.

ScriptDocument:GetLine(lineIndex:[number](/docs/luau/numbers)?):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| lineIndex:[number](/docs/luau/numbers)? Default Value: "nil" |

Returns

[string](/docs/luau/strings)

Returns the text of the specified line. When no argument is provided,
returns the line of the current cursor position.

Code Samples

ScriptDocument.SelectionChanged and ScriptDocument:GetLine()

ScriptDocument.SelectionChanged and ScriptDocument:GetLine()

```
--!nocheck



-- Run the following code in the Command Bar while a script is open



local ScriptEditorService = game:GetService("ScriptEditorService")



local function getFirstOpenDocument()



local documents = ScriptEditorService:GetScriptDocuments()



for _, document in documents do



if not document:IsCommandBar() then



return document



end



end



return nil



end



local scriptDocument = getFirstOpenDocument()



if scriptDocument then



scriptDocument.SelectionChanged:Connect(function(positionLine, positionCharacter, anchorLine, anchorCharacter)



print(`Selected: Line {positionLine}, Char {positionCharacter}`)



print(`Anchor: Line {anchorLine}, Char {anchorCharacter}`)



local lineText = scriptDocument:GetLine(positionLine)



print(`Selected line text: {lineText}`)



end)



else



print("No scripts open")



end
```

Provide feedback

---

GetLineCount

Plugin Security

Returns the number of lines in the document.

ScriptDocument:GetLineCount():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

Returns the number of lines in the active document.

Code Samples

ScriptDocument:GetLineCount()

ScriptDocument:GetLineCount()

```
--!nocheck



-- Run the following code in the Command Bar while a script is open



local ScriptEditorService = game:GetService("ScriptEditorService")



local function getFirstOpenDocument()



local documents = ScriptEditorService:GetScriptDocuments()



for _, document in documents do



if not document:IsCommandBar() then



return document



end



end



return nil



end



local scriptDocument = getFirstOpenDocument()



if scriptDocument then



local lineCount = scriptDocument:GetLineCount()



print(`The script has {lineCount} lines!`)



else



print("No scripts open")



end
```

Provide feedback

---

GetScript

Plugin Security

Returns the underlying [LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer) instance, if one exists,
otherwise nil.

ScriptDocument:GetScript():[LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer)

Returns

[LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer)

Returns the underlying [LuaSourceContainer](/docs/reference/engine/classes/LuaSourceContainer) instance, if one exists,
otherwise nil.

Code Samples

ScriptDocument:GetScript()

ScriptDocument:GetScript()

```
--!nocheck



-- Run the following code in the Command Bar while a script is open



local ScriptEditorService = game:GetService("ScriptEditorService")



local function getFirstOpenDocument()



local documents = ScriptEditorService:GetScriptDocuments()



for _, document in documents do



if not document:IsCommandBar() then



return document



end



end



return nil



end



local scriptDocument = getFirstOpenDocument()



if scriptDocument then



local openScript = scriptDocument:GetScript()



print(`Currently open script: {openScript:GetFullName()}`)



else



print("No scripts open")



end
```

Provide feedback

---

GetSelectedText

Plugin Security

Gets the text selected in the editor, or an empty string if there is no
selection.

ScriptDocument:GetSelectedText():[string](/docs/luau/strings)

Returns

[string](/docs/luau/strings)

Gets the text selected in the editor, or an empty string if there is no
selection.

Code Samples

ScriptDocument:HasSelectedText() and :GetSelectedText()

ScriptDocument:HasSelectedText() and :GetSelectedText()

```
--!nocheck



-- Run the following code in the Command Bar while a script is open



local ScriptEditorService = game:GetService("ScriptEditorService")



local function getFirstOpenDocument()



local documents = ScriptEditorService:GetScriptDocuments()



for _, document in documents do



if not document:IsCommandBar() then



return document



end



end



return nil



end



local scriptDocument = getFirstOpenDocument()



if scriptDocument then



scriptDocument.SelectionChanged:Connect(function()



if scriptDocument:HasSelectedText() then



local selectedText = scriptDocument:GetSelectedText()



print(`Currently selected text: {selectedText}`)



else



print("No text currently selected")



end



end)



else



print("No scripts open")



end
```

Provide feedback

---

GetSelection

Plugin Security

Returns the last known selection of the Script Editor in the format:
CursorLine, CursorChar, AnchorLine, AnchorChar. If the Script Editor has
no selection, CursorLine == AnchorLine and CursorChar == AnchorChar.

ScriptDocument:GetSelection():[Tuple](/docs/luau/tuples)

Returns

[Tuple](/docs/luau/tuples)

CursorLine, CursorChar, AnchorLine, AnchorChar.

Returns the last known selection of the Script Editor in the format:
CursorLine, CursorChar, AnchorLine, AnchorChar. If the Script Editor has
no selection, CursorLine == AnchorLine and CursorChar == AnchorChar.

Provide feedback

---

GetSelectionEnd

Plugin Security

Gets the larger of the cursor position and anchor. If the editor has no
selection, they are the same value.

ScriptDocument:GetSelectionEnd():[Tuple](/docs/luau/tuples)

Returns

[Tuple](/docs/luau/tuples)

Gets the larger of the cursor position and anchor. If the editor has no
selection, they are the same value.

Code Samples

ScriptDocument:GetSelectionStart() and :GetSelectionEnd()

ScriptDocument:GetSelectionStart() and :GetSelectionEnd()

```
--!nocheck



-- Run the following code in the Command Bar while a script is open



local ScriptEditorService = game:GetService("ScriptEditorService")



local function getFirstOpenDocument()



local documents = ScriptEditorService:GetScriptDocuments()



for _, document in documents do



if not document:IsCommandBar() then



return document



end



end



return nil



end



local scriptDocument = getFirstOpenDocument()



if scriptDocument then



local startLine, startCharacter = scriptDocument:GetSelectionStart()



local endLine, endCharacter = scriptDocument:GetSelectionEnd()



print(`Selection start: Line {startLine}, Char {startCharacter}`)



print(`Selection end: Line {endLine}, Char {endCharacter}`)



else



print("No scripts open")



end
```

Provide feedback

---

GetSelectionStart

Plugin Security

Gets the smaller of the cursor position and anchor. If the editor has no
selection, they are the same value.

ScriptDocument:GetSelectionStart():[Tuple](/docs/luau/tuples)

Returns

[Tuple](/docs/luau/tuples)

Gets the smaller of the cursor position and anchor. If the editor has no
selection, they are the same value.

Code Samples

ScriptDocument:GetSelectionStart() and :GetSelectionEnd()

ScriptDocument:GetSelectionStart() and :GetSelectionEnd()

```
--!nocheck



-- Run the following code in the Command Bar while a script is open



local ScriptEditorService = game:GetService("ScriptEditorService")



local function getFirstOpenDocument()



local documents = ScriptEditorService:GetScriptDocuments()



for _, document in documents do



if not document:IsCommandBar() then



return document



end



end



return nil



end



local scriptDocument = getFirstOpenDocument()



if scriptDocument then



local startLine, startCharacter = scriptDocument:GetSelectionStart()



local endLine, endCharacter = scriptDocument:GetSelectionEnd()



print(`Selection start: Line {startLine}, Char {startCharacter}`)



print(`Selection end: Line {endLine}, Char {endCharacter}`)



else



print("No scripts open")



end
```

Provide feedback

---

GetText

Plugin Security

Returns text from the open editor.

ScriptDocument:GetText(

startLine:[number](/docs/luau/numbers)?, startCharacter:[number](/docs/luau/numbers)?, endLine:[number](/docs/luau/numbers)?, endCharacter:[number](/docs/luau/numbers)?

):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| startLine:[number](/docs/luau/numbers)? Default Value: "nil" |
| startCharacter:[number](/docs/luau/numbers)? Default Value: "nil" |
| endLine:[number](/docs/luau/numbers)? Default Value: "nil" |
| endCharacter:[number](/docs/luau/numbers)? Default Value: "nil" |

Returns

[string](/docs/luau/strings)

Returns text from the open editor. Must be called with 0, 2 or 4
arguments:

* If called with 0 arguments, gets the entire contents of the open editor.
* If called with 2 arguments, gets the text of the document starting at
  (startLine, startColumn).
* If called with 4 arguments, gets the text of the document starting at
  (startLine, startColumn) and ending at (endLine, endColumn).

Code Samples

ScriptDocument:GetText()

ScriptDocument:GetText()

```
--!nocheck



-- Run the following code in the Command Bar while a script is open



local ScriptEditorService = game:GetService("ScriptEditorService")



local function getFirstOpenDocument()



local documents = ScriptEditorService:GetScriptDocuments()



for _, document in documents do



if not document:IsCommandBar() then



return document



end



end



return nil



end



local scriptDocument = getFirstOpenDocument()



if scriptDocument then



local text = scriptDocument:GetText()



print(`Script contents: {text}`)



else



print("No scripts open")



end
```

Provide feedback

---

GetViewport

Plugin Security

Returns the currently displayed line numbers in the editor change.

ScriptDocument:GetViewport():[Tuple](/docs/luau/tuples)

Returns

[Tuple](/docs/luau/tuples)

Returns the currently displayed line numbers in the editor change. The
editor displays the lines between startLine and endLine, inclusive. The
first and last line might only display partially. For example, only the
topmost pixel of the last line might be on screen. Furthermore, code
folding might hide lines between startLine and endLine.

Code Samples

ScriptDocument:GetViewport

ScriptDocument:GetViewport

```
--!nocheck



-- Run the following code in the Command Bar while a script is open



local ScriptEditorService = game:GetService("ScriptEditorService")



local function getFirstOpenDocument()



local documents = ScriptEditorService:GetScriptDocuments()



for _, document in documents do



if not document:IsCommandBar() then



return document



end



end



return nil



end



local scriptDocument = getFirstOpenDocument()



if scriptDocument then



local firstLine, lastLine = scriptDocument:GetViewport()



print(`Currently viewing lines {firstLine} to {lastLine}`)



else



print("No scripts open")



end
```

Provide feedback

---

HasSelectedText

Plugin Security

Returns whether or not the editor has any text selected.

ScriptDocument:HasSelectedText():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

Returns whether or not the editor has any text selected.

Code Samples

ScriptDocument:HasSelectedText() and :GetSelectedText()

ScriptDocument:HasSelectedText() and :GetSelectedText()

```
--!nocheck



-- Run the following code in the Command Bar while a script is open



local ScriptEditorService = game:GetService("ScriptEditorService")



local function getFirstOpenDocument()



local documents = ScriptEditorService:GetScriptDocuments()



for _, document in documents do



if not document:IsCommandBar() then



return document



end



end



return nil



end



local scriptDocument = getFirstOpenDocument()



if scriptDocument then



scriptDocument.SelectionChanged:Connect(function()



if scriptDocument:HasSelectedText() then



local selectedText = scriptDocument:GetSelectedText()



print(`Currently selected text: {selectedText}`)



else



print("No text currently selected")



end



end)



else



print("No scripts open")



end
```

Provide feedback

---

IsCommandBar

Plugin Security

Returns true if the [ScriptDocument](/docs/reference/engine/classes/ScriptDocument) represents the Command bar.

ScriptDocument:IsCommandBar():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

Returns true if the [ScriptDocument](/docs/reference/engine/classes/ScriptDocument) represents the Command bar. The
command bar has special rules and limitations in this API:

* Studio creates the Command bar before running plugins, so it doesn't
  always fire the opened event, although it does close and reopen as
  Studio transitions between DataModels.
* You can't edit the Command bar with EditTextAsync for security
  reasons.

Code Samples

ScriptDocument:IsCommandBar()

ScriptDocument:IsCommandBar()

```
--!nocheck



-- Run the following code in the Command Bar



local ScriptEditorService = game:GetService("ScriptEditorService")



local documents = ScriptEditorService:GetScriptDocuments()



for _, document in documents do



if document:IsCommandBar() then



print("Command bar document:", document)



end



end
```

Provide feedback

---

MultiEditTextAsync

Yields

Plugin Security

ScriptDocument:MultiEditTextAsync(edits:[Array](/docs/luau/tables#arrays)):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| edits:[Array](/docs/luau/tables#arrays) |

Returns

[Tuple](/docs/luau/tuples)

Provide feedback

---

RequestSetSelectionAsync

Yields

Plugin Security

Asks the editor to set its cursor selection to the argument values.

ScriptDocument:RequestSetSelectionAsync(

cursorLine:[number](/docs/luau/numbers), cursorCharacter:[number](/docs/luau/numbers), anchorLine:[number](/docs/luau/numbers)?, anchorCharacter:[number](/docs/luau/numbers)?

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| cursorLine:[number](/docs/luau/numbers) |
| cursorCharacter:[number](/docs/luau/numbers) |
| anchorLine:[number](/docs/luau/numbers)? Default Value: "nil" |
| anchorCharacter:[number](/docs/luau/numbers)? Default Value: "nil" |

Returns

[Tuple](/docs/luau/tuples)

Asks the editor to set its cursor selection to the argument values. Both
anchor arguments must be passed, or neither. If neither is passed, then
they each default to being the same as the corresponding cursor argument.
The editor might decline to update its cursor if the text content of the
document has changed, or the cursor has moved since the request was made.
Returns (true, nil) if the cursor was updated, and (false, string) with an
explanation string if it was not. Yields the current thread until the
editor replies.

Code Samples

ScriptDocument:RequestSetSelectionAsync()

ScriptDocument:RequestSetSelectionAsync()

```
--!nocheck



-- Run the following code in the Command Bar while a script is open



local ScriptEditorService = game:GetService("ScriptEditorService")



local function getFirstOpenDocument()



local documents = ScriptEditorService:GetScriptDocuments()



for _, document in documents do



if not document:IsCommandBar() then



return document



end



end



return nil



end



local scriptDocument = getFirstOpenDocument()



if scriptDocument then



-- Get the text on the cursor's current line



local cursorLine = scriptDocument:GetSelection()



local lineText = scriptDocument:GetLine(cursorLine)



-- Force select the entire line of text



local success, err = scriptDocument:RequestSetSelectionAsync(cursorLine, 1, cursorLine, #lineText + 1)



if success then



print("Set selection!")



else



print(`Failed to set selection because: {err}`)



end



else



print("No scripts open")



end
```

Provide feedback

---

Events

SelectionChanged

Plugin Security

Fires when the ScriptDocument changes, including immediately after a text
change.

ScriptDocument.SelectionChanged(

positionLine:[number](/docs/luau/numbers), positionCharacter:[number](/docs/luau/numbers), anchorLine:[number](/docs/luau/numbers), anchorCharacter:[number](/docs/luau/numbers)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| positionLine:[number](/docs/luau/numbers) |
| positionCharacter:[number](/docs/luau/numbers) |
| anchorLine:[number](/docs/luau/numbers) |
| anchorCharacter:[number](/docs/luau/numbers) |

Fires when the ScriptDocument changes, including immediately after a text
change.

Code Samples

ScriptDocument.SelectionChanged and ScriptDocument:GetLine()

ScriptDocument.SelectionChanged and ScriptDocument:GetLine()

```
--!nocheck



-- Run the following code in the Command Bar while a script is open



local ScriptEditorService = game:GetService("ScriptEditorService")



local function getFirstOpenDocument()



local documents = ScriptEditorService:GetScriptDocuments()



for _, document in documents do



if not document:IsCommandBar() then



return document



end



end



return nil



end



local scriptDocument = getFirstOpenDocument()



if scriptDocument then



scriptDocument.SelectionChanged:Connect(function(positionLine, positionCharacter, anchorLine, anchorCharacter)



print(`Selected: Line {positionLine}, Char {positionCharacter}`)



print(`Anchor: Line {anchorLine}, Char {anchorCharacter}`)



local lineText = scriptDocument:GetLine(positionLine)



print(`Selected line text: {lineText}`)



end)



else



print("No scripts open")



end
```

Provide feedback

---

ViewportChanged

Plugin Security

Fires when the displayed line numbers in the editor change.

ScriptDocument.ViewportChanged(

startLine:[number](/docs/luau/numbers), endLine:[number](/docs/luau/numbers)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| startLine:[number](/docs/luau/numbers) |
| endLine:[number](/docs/luau/numbers) |

Fires when the displayed line numbers in the editor change. See
[ScriptDocument.GetViewport](/docs/reference/engine/classes/ScriptDocument#GetViewport) for details.

Code Samples

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