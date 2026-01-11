# TextSource | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TextSource
Scraped: 2026-01-11T02:28:49.040525Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- Instance
- TextSource
- TextChannel
- TextSources
- TextChannels
- TextChannel:AddUserAsync()
- TextSource.Destroy
- Player.DisplayName
- TextSource.UserId
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [TextSource](/docs/reference/engine/classes/TextSource)

English

Feedback

Engine Class

TextSource

Represents a speaker in a [TextChannel](/docs/reference/engine/classes/TextChannel).

Not Creatable

---

Summary

Properties

|  |
| --- |
| [CanSend](#CanSend):[boolean](/docs/luau/booleans) |
| [UserId](#UserId):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Represents a speaker in a [TextChannel](/docs/reference/engine/classes/TextChannel).

[TextSources](/docs/reference/engine/classes/TextSource) provide details on permissions users have in
[TextChannels](/docs/reference/engine/classes/TextChannel). There may be multiple
[TextSources](/docs/reference/engine/classes/TextSource) for a user if that user belongs in multiple
[TextChannels](/docs/reference/engine/classes/TextChannel).

Create [TextSources](/docs/reference/engine/classes/TextSource) with [TextChannel:AddUserAsync()](/docs/reference/engine/classes/TextChannel#AddUserAsync),
which adds a [TextSource](/docs/reference/engine/classes/TextSource) to the [TextChannel](/docs/reference/engine/classes/TextChannel) as a descendant.

Remove [TextSources](/docs/reference/engine/classes/TextSource) by calling [TextSource.Destroy](/docs/reference/engine/classes/TextSource#Destroy).

Name of a [TextSource](/docs/reference/engine/classes/TextSource) is the [Player.DisplayName](/docs/reference/engine/classes/Player#DisplayName) of the user
associated with the [TextSource](/docs/reference/engine/classes/TextSource) via [TextSource.UserId](/docs/reference/engine/classes/TextSource#UserId).

To learn more about using TextSources, see
[In-Experience Text Chat](/docs/chat/in-experience-text-chat).

---

API Reference

Properties

CanSend

Read Parallel

Determines whether the user can send messages to the [TextChannel](/docs/reference/engine/classes/TextChannel).

TextSource.CanSend:[boolean](/docs/luau/booleans)

Determines whether the user can send messages to the [TextChannel](/docs/reference/engine/classes/TextChannel).

If false, user can only read messages in the [TextChannel](/docs/reference/engine/classes/TextChannel).

Provide feedback

---

UserId

Read Only

Not Replicated

Read Parallel

UserId of the user represented by the [TextSource](/docs/reference/engine/classes/TextSource).

TextSource.UserId:[number](/docs/luau/numbers)

UserId of the user represented by the [TextSource](/docs/reference/engine/classes/TextSource).

Support for non-user entities may be added in the future via passing in
negative numbers for this property.

Provide feedback

---