# TextChatCommand | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TextChatCommand
Scraped: 2026-01-11T02:27:25.324791Z

## Inherits
- Instance
- TextChatCommand
- TextSource
- Object
- TextChatService
- PrimaryAlias
- SecondaryAlias
- TextChannel:SendAsync()
- TextChatCommand.Triggered
- TextChatCommand.PrimaryAlias
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [TextChatCommand](/docs/reference/engine/classes/TextChatCommand)

English

Feedback

Engine Class

![TextChatCommand](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/TextChatCommand-Dark.webp)TextChatCommand

Represents a text chat command.

---

Summary

Properties

|  |
| --- |
| [AutocompleteVisible](#AutocompleteVisible):[boolean](/docs/luau/booleans) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [PrimaryAlias](#PrimaryAlias):[string](/docs/luau/strings) |
| [SecondaryAlias](#SecondaryAlias):[string](/docs/luau/strings) |

Events

|  |
| --- |
| [Triggered](#Triggered)(originTextSource: [TextSource](/docs/reference/engine/classes/TextSource),unfilteredText: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Represents a text chat command. Can be used to create custom text chat
commands when parented to [TextChatService](/docs/reference/engine/classes/TextChatService).

Custom commands can have up to two aliases, and the Triggered event fires when
a user's message matches the value of either the
[PrimaryAlias](/docs/reference/engine/classes/TextChatCommand#PrimaryAlias) or
[SecondaryAlias](/docs/reference/engine/classes/TextChatCommand#SecondaryAlias). For an example of
custom commands, see
[Custom text chat commands](/docs/chat/examples/custom-text-chat-commands).

To learn more about using [TextChatService](/docs/reference/engine/classes/TextChatService), see
[In-experience text chat](/docs/chat/in-experience-text-chat).

---

API Reference

Properties

AutocompleteVisible

Read Parallel

TextChatCommand.AutocompleteVisible:[boolean](/docs/luau/booleans)

Provide feedback

---

Enabled

Read Parallel

Determines whether the [TextChatCommand](/docs/reference/engine/classes/TextChatCommand) is enabled.

TextChatCommand.Enabled:[boolean](/docs/luau/booleans)

Determines whether the [TextChatCommand](/docs/reference/engine/classes/TextChatCommand) is enabled.

When disabled, messages that match the value of
[PrimaryAlias](/docs/reference/engine/classes/TextChatCommand#PrimaryAlias) or
[SecondaryAlias](/docs/reference/engine/classes/TextChatCommand#SecondaryAlias) are not sunk and is
sent to other users.

Use this to disable default commands on a case-by-case basis.

Provide feedback

---

PrimaryAlias

Read Parallel

A primary alias used to trigger the [TextChatCommand](/docs/reference/engine/classes/TextChatCommand).

TextChatCommand.PrimaryAlias:[string](/docs/luau/strings)

A primary alias used to trigger the [TextChatCommand](/docs/reference/engine/classes/TextChatCommand).

If a user sends a message with [TextChannel:SendAsync()](/docs/reference/engine/classes/TextChannel#SendAsync) that
matches the [PrimaryAlias](/docs/reference/engine/classes/TextChatCommand#PrimaryAlias), the message
is not sent and instead [TextChatCommand.Triggered](/docs/reference/engine/classes/TextChatCommand#Triggered) is fired.

Provide feedback

---

SecondaryAlias

Read Parallel

A secondary alias used to trigger the [TextChatCommand](/docs/reference/engine/classes/TextChatCommand).

TextChatCommand.SecondaryAlias:[string](/docs/luau/strings)

A secondary alias used to trigger the [TextChatCommand](/docs/reference/engine/classes/TextChatCommand).

Provide feedback

---

Events

Triggered

An event that developers can bind to execute commands.

TextChatCommand.Triggered(

originTextSource:[TextSource](/docs/reference/engine/classes/TextSource), unfilteredText:[string](/docs/luau/strings)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| originTextSource:[TextSource](/docs/reference/engine/classes/TextSource)  A reference to the [TextSource](/docs/reference/engine/classes/TextSource) responsible for triggering the command via [TextChannel:SendAsync()](/docs/reference/engine/classes/TextChannel#SendAsync). |
| unfilteredText:[string](/docs/luau/strings)  The full, unfiltered text used to trigger the command that can be used to dissect parameters from the command message. |

An event that developers can bind to execute commands.

When a user sends a message to the server via
[TextChannel:SendAsync()](/docs/reference/engine/classes/TextChannel#SendAsync), the message is intercepted by the
[TextChatCommand](/docs/reference/engine/classes/TextChatCommand) and not replicated to other users if the content
of the message matches the
[PrimaryAlias](/docs/reference/engine/classes/TextChatCommand#PrimaryAlias) or
[SecondaryAlias](/docs/reference/engine/classes/TextChatCommand#SecondaryAlias).

For example, for a [TextChatCommand](/docs/reference/engine/classes/TextChatCommand) with
[TextChatCommand.PrimaryAlias](/docs/reference/engine/classes/TextChatCommand#PrimaryAlias) as "mute", if a user sends "/mute
SomeUserName", then the relevant [TextChatCommand](/docs/reference/engine/classes/TextChatCommand) for mute will
fire its [TextChatCommand.Triggered](/docs/reference/engine/classes/TextChatCommand#Triggered). The message "/mute
SomeUserName" is not replicated to other users.

Provide feedback

---