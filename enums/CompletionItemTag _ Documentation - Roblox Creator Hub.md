# CompletionItemTag | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/CompletionItemTag
Scraped: 2026-01-11T02:44:32.962130Z

## Inherits
- ScriptEditorService:RegisterAutocompleteCallback()
1. [Enums](/docs/reference/engine/enums)
2. /
3. [CompletionItemTag](/docs/reference/engine/enums/CompletionItemTag)

English

Feedback

Engine Enum

CompletionItemTag

---

Determines the tags for completion items in
[ScriptEditorService:RegisterAutocompleteCallback()](/docs/reference/engine/classes/ScriptEditorService#RegisterAutocompleteCallback).

Items

| Name | Value | Summary |
| --- | --- | --- |
| Deprecated | 1 | Indicates that the completion is deprecated, applying a penalty towards its score and crossing it out in the completion list. |
| IncorrectIndexType | 2 | Indicates that the completion is a member and being accessed with the wrong index type (e.g. using : to access a property), hiding it from the completion list. |
| PluginPermissions | 3 | Indicates that the completion requires Plugin security level to access, hiding it if the client lacks this level. |
| CommandLinePermissions | 4 | Indicates that the completion requires Command line security level to access, hiding it if the client lacks this level. |
| RobloxPermissions | 5 | Indicates that the completion requires core script security level to access, hiding it if the client lacks this level. |
| AddParens | 6 | Instructs the editor to add parentheses before the cursor after inserting the given completion, if accepted. |
| PutCursorInParens | 7 | Instructs the editor to add parentheses before the cursor and move the cursor into the parentheses after inserting the given completion, if accepted. |
| TypeCorrect | 8 | Indicates that the completion is type correct in the current context, granting a bonus to its score. |
| ClientServerBoundaryViolation | 9 | Indicates that the completion is being accessed from the wrong side of the client/server boundary (e.g. Players.LocalPlayer in a server script), hiding it from the completion list. |
| Invalidated | 10 |  |
| PutCursorBeforeEnd | 11 |  |