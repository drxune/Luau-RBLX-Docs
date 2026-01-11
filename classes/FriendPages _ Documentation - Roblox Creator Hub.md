# FriendPages | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/FriendPages
Scraped: 2026-01-11T02:29:39.928064Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Pages
- FriendPages
- Instance
- Object
- Players:GetFriendsAsync()
- Player.UserId
- Players:GetUserIdFromNameAsync()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Pages](/docs/reference/engine/classes/Pages)
6. /
7. [FriendPages](/docs/reference/engine/classes/FriendPages)

English

Feedback

Engine Class

FriendPages

A special version of [Pages](/docs/reference/engine/classes/Pages) that contains information about a player's
connections.

Not Creatable

Not Replicated

---

Summary

Inherited Members

3 inherited from [Pages](/docs/reference/engine/classes/Pages)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

FriendPages is a special version of [Pages](/docs/reference/engine/classes/Pages) returned by
[Players:GetFriendsAsync()](/docs/reference/engine/classes/Players#GetFriendsAsync). The items contained within include
information about a player's connections and have the following structure:

|  |  |  |
| --- | --- | --- |
| Name | Type | Description |
| DisplayName | string | The current display name of the connection. |
| Id | int64 | The user ID of the connection. |
| Username | string | The username of the connection. |

See the code samples for how to iterate over a player's connections.

Code Samples

Print Roblox Connections

This code sample loads the [Player.UserId](/docs/reference/engine/classes/Player#UserId) of the player whose username
is provided at the top of the script by using
[Players:GetUserIdFromNameAsync()](/docs/reference/engine/classes/Players#GetUserIdFromNameAsync). Then, it gets a FriendPages object
by calling [Players:GetFriendsAsync()](/docs/reference/engine/classes/Players#GetFriendsAsync) and iterates over each entry
using the iterPageItems function. The username of each connection is stored in a
table, then printed at the end.

```
local Players = game:GetService("Players")



local USERNAME = "Cozecant"



local function iterPageItems(pages)



return coroutine.wrap(function()



local pagenum = 1



while true do



for _, item in ipairs(pages:GetCurrentPage()) do



coroutine.yield(item, pagenum)



end



if pages.IsFinished then



break



end



pages:AdvanceToNextPageAsync()



pagenum = pagenum + 1



end



end)



end



-- First, get the user ID of the player



local userId = Players:GetUserIdFromNameAsync(USERNAME)



-- Then, get a FriendPages object for their connections



local friendPages = Players:GetFriendsAsync(userId)



-- Iterate over the items in the pages. For FriendPages, these



-- are tables of information about the connection, including Username.



-- Collect each username in a table



local usernames = {}



for item, _pageNo in iterPageItems(friendPages) do



table.insert(usernames, item.Username)



end



print("Connections of " .. USERNAME .. ": " .. table.concat(usernames, ", "))
```