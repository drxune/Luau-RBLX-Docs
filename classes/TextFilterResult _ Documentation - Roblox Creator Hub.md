# TextFilterResult | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TextFilterResult
Scraped: 2026-01-11T02:41:20.489318Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- Instance
- TextFilterResult
- TextService:FilterStringAsync()
- Player.UserId
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [TextFilterResult](/docs/reference/engine/classes/TextFilterResult)

English

Feedback

Engine Class

TextFilterResult

Not Creatable

Not Replicated

---

Summary

Methods

|  |
| --- |
| [GetChatForUserAsync](#GetChatForUserAsync)(toUserId: [number](/docs/luau/numbers)):[string](/docs/luau/strings)  Deprecated |
| [GetNonChatStringForBroadcastAsync](#GetNonChatStringForBroadcastAsync)():[string](/docs/luau/strings) |
| [GetNonChatStringForUserAsync](#GetNonChatStringForUserAsync)(toUserId: [number](/docs/luau/numbers)):[string](/docs/luau/strings) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Represents the result of a call to [TextService:FilterStringAsync()](/docs/reference/engine/classes/TextService#FilterStringAsync).
Used to distribute a filtered string accordingly.

---

API Reference

Methods

GetChatForUserAsync

Deprecated

Show details

---

GetNonChatStringForBroadcastAsync

Yields

Returns the text in a properly filtered manner for all users.

TextFilterResult:GetNonChatStringForBroadcastAsync():[string](/docs/luau/strings)

Returns

[string](/docs/luau/strings)

Filtered text string.

Returns the text in a properly filtered manner for all users. This should
be used in the context of non-chat text that every user can see, such as
for a dialog that lets a user write a message on a sign, visible to all
users on the server even after the author has left.

Provide feedback

---

GetNonChatStringForUserAsync

Yields

Returns the text in a properly filtered manner for the specified
[Player.UserId](/docs/reference/engine/classes/Player#UserId) based on age and other details.

TextFilterResult:GetNonChatStringForUserAsync(toUserId:[number](/docs/luau/numbers)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| toUserId:[number](/docs/luau/numbers)  [Player.UserId](/docs/reference/engine/classes/Player#UserId) of the user intended to see/receive the text. |

Returns

[string](/docs/luau/strings)

Filtered text string.

Returns the text in a properly filtered manner for the specified
[Player.UserId](/docs/reference/engine/classes/Player#UserId) based on age and other details. This should be used
in the context of non-chat text that one specific user can see, such as
the name of a pet.

Provide feedback

---