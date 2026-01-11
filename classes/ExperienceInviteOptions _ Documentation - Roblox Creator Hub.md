# ExperienceInviteOptions | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ExperienceInviteOptions
Scraped: 2026-01-11T02:39:25.333146Z

## Tags
- Not Replicated

## Inherits
- Instance
- ExperienceInviteOptions
- Object
- UserId
- Player:GetJoinData()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [ExperienceInviteOptions](/docs/reference/engine/classes/ExperienceInviteOptions)

English

Feedback

Engine Class

ExperienceInviteOptions

Used to customize a player invite prompt.

Not Replicated

---

Summary

Properties

|  |
| --- |
| [InviteMessageId](#InviteMessageId):[string](/docs/luau/strings) |
| [InviteUser](#InviteUser):[number](/docs/luau/numbers) |
| [LaunchData](#LaunchData):[string](/docs/luau/strings) |
| [PromptMessage](#PromptMessage):[string](/docs/luau/strings) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Used to customize a
[player invite prompt](/docs/production/promotion/invite-prompts), such
as to customize the prompt message, target a specific connection, or include
launch data in the invite.

---

API Reference

Properties

InviteMessageId

Read Parallel

Asset ID that maps to a Notification asset type.

ExperienceInviteOptions.InviteMessageId:[string](/docs/luau/strings)

Asset ID that maps to a Notification asset type. This asset is used to
store/localize a custom string for the invite notification that
connections receive. See
[Setting Notification Options](/docs/production/promotion/invite-prompts#setting-notification-options)
for details.

Provide feedback

---

InviteUser

Read Parallel

Roblox [UserId](/docs/reference/engine/classes/Player#UserId) of the specific connection to invite.

ExperienceInviteOptions.InviteUser:[number](/docs/luau/numbers)

Roblox [UserId](/docs/reference/engine/classes/Player#UserId) of the specific connection to invite;
if not provided, the player will be prompted to pick from a list of
connections.

Provide feedback

---

LaunchData

Read Parallel

Used to set a parameter in [Player:GetJoinData()](/docs/reference/engine/classes/Player#GetJoinData) when a connection
joins from the invite notification.

ExperienceInviteOptions.LaunchData:[string](/docs/luau/strings)

Used to set a parameter in [Player:GetJoinData()](/docs/reference/engine/classes/Player#GetJoinData) when a connection
joins from the invite notification; maximum of 200 characters. See
[Include launch data](/docs/production/promotion/invite-prompts#include-launch-data)
for a usage example.

Provide feedback

---

PromptMessage

Read Parallel

Custom text shown on the invite prompt for the sending player.

ExperienceInviteOptions.PromptMessage:[string](/docs/luau/strings)

Custom text shown on the invite prompt for the sending player, for example
"Ask your connections to join the adventure!" for a multi-connection
invite prompt, or "Invite this connection to join the adventure!" for a
specific connection invite prompt.

Provide feedback

---