# TextChatService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TextChatService
Scraped: 2026-01-11T02:30:49.048370Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Instance
- TextChatService
- TextChatMessage
- Object
- managing channels
- creating commands
- ChatWindowConfiguration
- ChatInputBarConfiguration
- BubbleChatConfiguration
- ChannelTabsConfiguration
- TextChatMessage.Translation
- TextChatCommands
- Folder
- Name
- DisplayName
- TextChannels
- Player
- CreateDefaultCommands
- TextChannel.OnIncomingMessage
- TextChannel
- PrefixText
- Player.Team
- Team.TeamColor
- TextChatMessage.Text
- TextChatMessage.Metadata
- TeamColor
- Team
- Teams
- TextSources
- Neutral
- UserIds
- TextChatMessage.PrefixText
- CreateDefaultTextChannels
- Script
- RunContext
- LocalScript
- UserId
- TextChannel:SetDirectChatRequester()
- TextChannel.DirectChatRequester
- BubbleDisplayed
- TextChatService:DisplayBubble()
- TextChannel:DisplaySystemMessage()
- TextChannel:SendAsync()
- TextChannel.MessageReceived
- TextChannel.ShouldDeliverCallback
- TextChatService.MessageReceived
- TextSource
- TextChatService.OnIncomingMessage
- BubbleChatMessageProperties
- UICorner
- UIGradient
- ImageLabel
- ChatWindowMessageProperties
- TextColor3
- TextChatMessageProperties
- TextChatMessages
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [TextChatService](/docs/reference/engine/classes/TextChatService)

English

Feedback

Engine Class

![TextChatService](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/TextChatService-Dark.webp)TextChatService

A service handling in-experience text chat.

Not Creatable

Service

---

Summary

Properties

|  |
| --- |
| [ChatTranslationEnabled](#ChatTranslationEnabled):[boolean](/docs/luau/booleans) |
| [ChatVersion](#ChatVersion):[Enum.ChatVersion](/docs/reference/engine/enums/ChatVersion)  Deprecated |
| [CreateDefaultCommands](#CreateDefaultCommands):[boolean](/docs/luau/booleans) |
| [CreateDefaultTextChannels](#CreateDefaultTextChannels):[boolean](/docs/luau/booleans) |

Methods

|  |
| --- |
| [CanUserChatAsync](#CanUserChatAsync)(userId: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans) |
| [CanUsersChatAsync](#CanUsersChatAsync)(userIdFrom: [number](/docs/luau/numbers),userIdTo: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans) |
| [CanUsersDirectChatAsync](#CanUsersDirectChatAsync)(requesterUserId: [number](/docs/luau/numbers),userIds: [Array](/docs/luau/tables#arrays)):[Array](/docs/luau/tables#arrays) |
| [DisplayBubble](#DisplayBubble)(partOrCharacter: [Instance](/docs/reference/engine/datatypes/Instance),message: [string](/docs/luau/strings)):() |

Events

|  |
| --- |
| [BubbleDisplayed](#BubbleDisplayed)(partOrCharacter: [Instance](/docs/reference/engine/datatypes/Instance),textChatMessage: [TextChatMessage](/docs/reference/engine/classes/TextChatMessage)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MessageReceived](#MessageReceived)(textChatMessage: [TextChatMessage](/docs/reference/engine/classes/TextChatMessage)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [SendingMessage](#SendingMessage)(textChatMessage: [TextChatMessage](/docs/reference/engine/classes/TextChatMessage)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Callbacks

|  |
| --- |
| [OnBubbleAdded](#OnBubbleAdded)(message: [TextChatMessage](/docs/reference/engine/classes/TextChatMessage),adornee: [Instance](/docs/reference/engine/datatypes/Instance)):[Tuple](/docs/luau/tuples) |
| [OnChatWindowAdded](#OnChatWindowAdded)(message: [TextChatMessage](/docs/reference/engine/classes/TextChatMessage)):[Tuple](/docs/luau/tuples) |
| [OnIncomingMessage](#OnIncomingMessage)(message: [TextChatMessage](/docs/reference/engine/classes/TextChatMessage)):[Tuple](/docs/luau/tuples) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A service handling in-experience text chat, including
[managing channels](/docs/reference/engine/classes/TextChannel), decorating messages, filtering text,
[creating commands](/docs/reference/engine/classes/TextChatCommand), and
[developing custom chats interfaces](/docs/chat/examples/simple-custom-frontend-ui).

To learn more, see
[TextChatService Overview](/docs/chat/in-experience-text-chat).

For further customization, TextChatService has the following singleton
children:

* [ChatWindowConfiguration](/docs/reference/engine/classes/ChatWindowConfiguration)
* [ChatInputBarConfiguration](/docs/reference/engine/classes/ChatInputBarConfiguration)
* [BubbleChatConfiguration](/docs/reference/engine/classes/BubbleChatConfiguration)
* [ChannelTabsConfiguration](/docs/reference/engine/classes/ChannelTabsConfiguration)

---

API Reference

Properties

ChatTranslationEnabled

Not Replicated

Roblox Script Security

Read Parallel

Determines whether a user has chat translation enabled.

TextChatService.ChatTranslationEnabled:[boolean](/docs/luau/booleans)

Determines whether a user has chat translation enabled. If true, messages
the user receives will be translated into their preferred language. Use
[TextChatMessage.Translation](/docs/reference/engine/classes/TextChatMessage#Translation) to get the message
translation.

Provide feedback

---

ChatVersion

Deprecated

Show details

---

CreateDefaultCommands

Plugin Security

Read Parallel

Determines whether [TextChatService](/docs/reference/engine/classes/TextChatService) should create default
[TextChatCommands](/docs/reference/engine/classes/TextChatCommand).

TextChatService.CreateDefaultCommands:[boolean](/docs/luau/booleans)

Determines whether [TextChatService](/docs/reference/engine/classes/TextChatService) should create default
[TextChatCommands](/docs/reference/engine/classes/TextChatCommand).

If true, the following [TextChatCommands](/docs/reference/engine/classes/TextChatCommand) are
created and put in a [Folder](/docs/reference/engine/classes/Folder) named TextChatCommands inside
[TextChatService](/docs/reference/engine/classes/TextChatService):

| Name | Primary Alias | Secondary Alias | Description | Usage Example |
| --- | --- | --- | --- | --- |
| **RBXClearCommand** | clear | cls | Clears the chat log for the local user. | /cls |
| **RBXConsoleCommand** | console |  | Opens the Developer Console. | /console |
| **RBXEmoteCommand** | emote | e | Plays an avatar emote. | /e dance |
| **RBXHelpCommand** | help | ? | Shows a list of chat commands. | /help |
| **RBXMuteCommand** | mute | m | Mutes a user by their [Name](/docs/reference/engine/classes/Player#Name) or [DisplayName](/docs/reference/engine/classes/Player#DisplayName) in all [TextChannels](/docs/reference/engine/classes/TextChannel). | /m Username |
| **RBXTeamCommand** | team | t | Enters team chat mode where messages are only visible to teammates. | /t |
| **RBXUnmuteCommand** | unmute | um | Unmutes a user by their [Name](/docs/reference/engine/classes/Player#Name) or [DisplayName](/docs/reference/engine/classes/Player#DisplayName) in all [TextChannels](/docs/reference/engine/classes/TextChannel). | /um Username |
| **RBXVersionCommand** | version | v | Shows the chat version. | /version |
| **RBXWhisperCommand** | whisper | w | Enters whisper mode with another [Player](/docs/reference/engine/classes/Player). | /w DisplayName or /w @Username |

Note that you can edit, create, and remove
[TextChatCommands](/docs/reference/engine/classes/TextChatCommand) even if
[CreateDefaultCommands](/docs/reference/engine/classes/TextChatService#CreateDefaultCommands) is
true. Also note that mute and unmute commands apply to all
[TextChannels](/docs/reference/engine/classes/TextChannel).

Provide feedback

---

CreateDefaultTextChannels

Plugin Security

Read Parallel

Determines whether [TextChatService](/docs/reference/engine/classes/TextChatService) should create default
[TextChannels](/docs/reference/engine/classes/TextChannel).

TextChatService.CreateDefaultTextChannels:[boolean](/docs/luau/booleans)

Determines whether [TextChatService](/docs/reference/engine/classes/TextChatService) should create default
[TextChannels](/docs/reference/engine/classes/TextChannel). If true, a [Folder](/docs/reference/engine/classes/Folder) named
TextChannels is created inside [TextChatService](/docs/reference/engine/classes/TextChatService) at runtime to
contain the [TextChannels](/docs/reference/engine/classes/TextChannel) outlined in the table below.
Each of the default channels has the described special behavior applied to
messages using its internally bound [TextChannel.OnIncomingMessage](/docs/reference/engine/classes/TextChannel#OnIncomingMessage)
callback function, changing how messages appear when sent through the
channel. The callback is assigned automatically either at runtime (if the
[TextChannel](/docs/reference/engine/classes/TextChannel) exists) or when the [TextChannel](/docs/reference/engine/classes/TextChannel) is created.

| Channel | Description |
| --- | --- |
| **RBXGeneral** | [TextChannel](/docs/reference/engine/classes/TextChannel) for player messages. In the chat window, messages are modified such that [PrefixText](/docs/reference/engine/classes/TextChatMessage#PrefixText) receives a [rich text](/docs/ui/rich-text) font color tag to give chatting players their distinctive name color. If [Player.Team](/docs/reference/engine/classes/Player#Team) exists, that [Team.TeamColor](/docs/reference/engine/classes/Team#TeamColor) is used instead of the default name color. |
| **RBXSystem** | [TextChannel](/docs/reference/engine/classes/TextChannel) for system messages. In the chat window, messages are modified such that [TextChatMessage.Text](/docs/reference/engine/classes/TextChatMessage#Text) is given a light grey color tag by default, or a red color tag if [TextChatMessage.Metadata](/docs/reference/engine/classes/TextChatMessage#Metadata) contains the word "Error". |
| **RBXTeam[BrickColor]** | [TextChannel](/docs/reference/engine/classes/TextChannel) for team-specific player messages, created when a [TeamColor](/docs/reference/engine/classes/Team#TeamColor) is in use by any [Team](/docs/reference/engine/classes/Team) within the [Teams](/docs/reference/engine/classes/Teams) service. Name of the created channel is **RBXTeam** followed by the [TeamColor](/docs/reference/engine/classes/Team#TeamColor) name. For example, **RBXTeamCrimson** is a [TextChannel](/docs/reference/engine/classes/TextChannel) created when there is an active team whose [TeamColor](/docs/reference/engine/classes/Team#TeamColor) property is the "Crimson" [BrickColor](/docs/reference/engine/datatypes/BrickColor).  In the chat window, messages are modified such that [PrefixText](/docs/reference/engine/classes/TextChatMessage#PrefixText) is colored according to the [TeamColor](/docs/reference/engine/classes/Player#TeamColor) and is prepended with **[Team]**.  Team channels create [TextSources](/docs/reference/engine/classes/TextSource) for all non‑[Neutral](/docs/reference/engine/classes/Player#Neutral) players with the matching [TeamColor](/docs/reference/engine/classes/Team#TeamColor), allowing them to use team‑only chat. Channels are removed if there are no remaining teams with an associated [TeamColor](/docs/reference/engine/classes/Team#TeamColor). |
| **RBXWhisper:[UserId1]\_[UserId2]** | [TextChannel](/docs/reference/engine/classes/TextChannel) for whisper messages between two players, created when a player uses the /whisper command on another player. For example **RBXWhisper:2276836\_505306092** is a [TextChannel](/docs/reference/engine/classes/TextChannel) for players with [UserIds](/docs/reference/engine/classes/Player#UserId) **2276836** and **505306092**. Inside whisper channels are two [TextSources](/docs/reference/engine/classes/TextSource) associated with the respective [UserIds](/docs/reference/engine/classes/Player#UserId).  In the chat window, messages are colored the same as those in **RBXGeneral** and [TextChatMessage.PrefixText](/docs/reference/engine/classes/TextChatMessage#PrefixText) is modified to show whether a message was sent from or received by the local user.  Whisper channels are removed when either player leaves the experience. |

Note that the default [TextChannel.OnIncomingMessage](/docs/reference/engine/classes/TextChannel#OnIncomingMessage) callbacks can
be overwritten. Also note that you can edit, create, and remove
[TextChannels](/docs/reference/engine/classes/TextChannel) even if
[CreateDefaultTextChannels](/docs/reference/engine/classes/TextChatService#CreateDefaultTextChannels)
is true.

Messages from different TextChannels can be separated into different tabs
in the chat window using [ChannelTabsConfiguration](/docs/reference/engine/classes/ChannelTabsConfiguration).

Provide feedback

---

Methods

CanUserChatAsync

Yields

Determines whether a user has permission to chat in experiences.

TextChatService:CanUserChatAsync(userId:[number](/docs/luau/numbers)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| userId:[number](/docs/luau/numbers) |

Returns

[boolean](/docs/luau/booleans)

Determines whether a user has permission to chat in experiences. Factors
such as parental control settings may prevent the user from sending
messages. Errors if the userId is not in the current server. Note that
this method can be used with all current player
[UserIds](/docs/reference/engine/classes/Player#UserId) in a [Script](/docs/reference/engine/classes/Script) with
[RunContext](/docs/reference/engine/classes/Script#RunContext) of [Enum.RunContext.Server](/docs/reference/engine/enums/RunContext#Server) or
[Enum.RunContext.Legacy](/docs/reference/engine/enums/RunContext#Legacy). This method can also be used in a
[LocalScript](/docs/reference/engine/classes/LocalScript) but only with the [UserId](/docs/reference/engine/classes/Player#UserId) of the
local player.

Provide feedback

---

CanUsersChatAsync

Yields

Determines whether or not two users would receive messages between each
other.

TextChatService:CanUsersChatAsync(

userIdFrom:[number](/docs/luau/numbers), userIdTo:[number](/docs/luau/numbers)

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| userIdFrom:[number](/docs/luau/numbers) |
| userIdTo:[number](/docs/luau/numbers) |

Returns

[boolean](/docs/luau/booleans)

Determines whether or not two users would receive messages between each
other. Factors such as incompatible parental control settings or blocked
status may prevent the delivery of messages between users
[TextChannels](/docs/reference/engine/classes/TextChannel) internally use this result to determine
whether to deliver messages between users. Note that this method is only
available for use in a [Script](/docs/reference/engine/classes/Script) with
[RunContext](/docs/reference/engine/classes/Script#RunContext) of [Enum.RunContext.Server](/docs/reference/engine/enums/RunContext#Server) or
[Enum.RunContext.Legacy](/docs/reference/engine/enums/RunContext#Legacy).

Provide feedback

---

CanUsersDirectChatAsync

Yields

Determines whether a user has permission to chat directly with other users
in experiences based on factors such as their parental control settings.

TextChatService:CanUsersDirectChatAsync(

requesterUserId:[number](/docs/luau/numbers), userIds:[Array](/docs/luau/tables#arrays)

):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| requesterUserId:[number](/docs/luau/numbers)  The user who would have initiated the direct chat request. If the requesterUserId is not in the current server, this method will error. |
| userIds:[Array](/docs/luau/tables#arrays)  A list of users who the requesterUserId would like to chat with directly. Users not in the current server are ignored. |

Returns

[Array](/docs/luau/tables#arrays)

A list of users who could participate in the direct chat request. If
none of the users can direct chat with the requesterUserId, the result
is an empty array.

Determines whether a user has permission to chat directly with other users
in experiences based on their parental control settings. To be used when:

* The line of communication is user-initiated (not developer- or
  gameplay-initiated)
* Access to the communication is closed and limited

An example of a direct chat is a whisper channel between two users.

You may use this method to gate certain features in your experience
depending on the result.

When creating a [TextChannel](/docs/reference/engine/classes/TextChannel) for a direct chat, use
[TextChannel:SetDirectChatRequester()](/docs/reference/engine/classes/TextChannel#SetDirectChatRequester) to set the requesterUserId so
that the channel can determine whether to deliver messages between users.
When [TextChannel.DirectChatRequester](/docs/reference/engine/classes/TextChannel#DirectChatRequester) is non-nil,
[TextChannels](/docs/reference/engine/classes/TextChannel) internally use this result to determine
whether to deliver messages between users.

```
local whoCanDirectChat = TextChatService:CanUsersDirectChatAsync(requesterUserId, { userId1, userId2 })



if #whoCanDirectChat > 0 then



-- The requesterUserId can direct chat with either userId1, userId2, or both



else



-- The requesterUserId cannot direct chat with either userId1 or userId2



end
```

Note that this method is only available for use in a [Script](/docs/reference/engine/classes/Script) with
[RunContext](/docs/reference/engine/classes/Script#RunContext) of [Enum.RunContext.Server](/docs/reference/engine/enums/RunContext#Server) or
[Enum.RunContext.Legacy](/docs/reference/engine/enums/RunContext#Legacy).

Code Samples

CanUsersDirectChatAsync

This example checks if two users can chat, creates a new [TextChannel](/docs/reference/engine/classes/TextChannel),
and adds them to it.

```
local TextChatService = game:GetService("TextChatService")



local directChatParticipants = TextChatService:CanUsersDirectChatAsync(userId1, { userId2 })



-- Check for eligible participants



if #directChatParticipants > 0 then



local directChannel = Instance.new("TextChannel")



directChannel.Parent = TextChatService



for _, participant in directChatParticipants do



directChannel:AddUserAsync(participant)



end



return directChannel



end



warn("Could not create TextChannel. Not enough eligible users.")



return nil
```

Provide feedback

---

DisplayBubble

Displays a chat bubble above the provided part or player character.

TextChatService:DisplayBubble(

partOrCharacter:[Instance](/docs/reference/engine/datatypes/Instance), message:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| partOrCharacter:[Instance](/docs/reference/engine/datatypes/Instance)  The part or character that the bubble to be displayed above. |
| message:[string](/docs/luau/strings)  The text to be displayed in the chat bubble. |

Returns

()

Displays a chat bubble above the provided part or player character, and
fires the [BubbleDisplayed](/docs/reference/engine/classes/TextChatService#BubbleDisplayed) event
with the parameters specified in this method. Can display bubbles for
non-player characters (NPCs) if you specify a part within the character,
such as its head.

Note that this method is only available for use in [LocalScript](/docs/reference/engine/classes/LocalScript), or
in a [Script](/docs/reference/engine/classes/Script) with [RunContext](/docs/reference/engine/classes/Script#RunContext) of
[Enum.RunContext.Client](/docs/reference/engine/enums/RunContext#Client).

Provide feedback

---

Events

BubbleDisplayed

Fires when [TextChatService:DisplayBubble()](/docs/reference/engine/classes/TextChatService#DisplayBubble) is called.

TextChatService.BubbleDisplayed(

partOrCharacter:[Instance](/docs/reference/engine/datatypes/Instance), textChatMessage:[TextChatMessage](/docs/reference/engine/classes/TextChatMessage)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| partOrCharacter:[Instance](/docs/reference/engine/datatypes/Instance) |
| textChatMessage:[TextChatMessage](/docs/reference/engine/classes/TextChatMessage) |

Fires when [TextChatService:DisplayBubble()](/docs/reference/engine/classes/TextChatService#DisplayBubble) is called.

Provide feedback

---

MessageReceived

Fires when [TextChannel:DisplaySystemMessage()](/docs/reference/engine/classes/TextChannel#DisplaySystemMessage) is invoked on the
client, or when the client receives a valid
[TextChannel:SendAsync()](/docs/reference/engine/classes/TextChannel#SendAsync) response from the server.

TextChatService.MessageReceived(textChatMessage:[TextChatMessage](/docs/reference/engine/classes/TextChatMessage)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| textChatMessage:[TextChatMessage](/docs/reference/engine/classes/TextChatMessage)  The received [TextChatMessage](/docs/reference/engine/classes/TextChatMessage). |

Like [TextChannel.MessageReceived](/docs/reference/engine/classes/TextChannel#MessageReceived), fires when
[TextChannel:DisplaySystemMessage()](/docs/reference/engine/classes/TextChannel#DisplaySystemMessage) is invoked on the client, or
when the client receives a valid [TextChannel:SendAsync()](/docs/reference/engine/classes/TextChannel#SendAsync) response
from the server. This event is only fired on the client.

If the server's [TextChannel.ShouldDeliverCallback](/docs/reference/engine/classes/TextChannel#ShouldDeliverCallback) property is
bound and returns false, the client will not fire
[TextChatService.MessageReceived](/docs/reference/engine/classes/TextChatService#MessageReceived).

Use the [TextChatMessage](/docs/reference/engine/classes/TextChatMessage) parameter to get the [TextSource](/docs/reference/engine/classes/TextSource)
and the text of the message (with [TextChatMessage.Text](/docs/reference/engine/classes/TextChatMessage#Text)).

The [TextChatMessage](/docs/reference/engine/classes/TextChatMessage) parameter is the final result of any functions
bound to [TextChatService.OnIncomingMessage](/docs/reference/engine/classes/TextChatService#OnIncomingMessage) or
[TextChannel.OnIncomingMessage](/docs/reference/engine/classes/TextChannel#OnIncomingMessage).

Provide feedback

---

SendingMessage

Fires when [TextChannel:SendAsync()](/docs/reference/engine/classes/TextChannel#SendAsync) is called by the sending
client.

TextChatService.SendingMessage(textChatMessage:[TextChatMessage](/docs/reference/engine/classes/TextChatMessage)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| textChatMessage:[TextChatMessage](/docs/reference/engine/classes/TextChatMessage)  The [TextChatMessage](/docs/reference/engine/classes/TextChatMessage) from the [TextChannel:SendAsync()](/docs/reference/engine/classes/TextChannel#SendAsync) call. |

Fires when [TextChannel:SendAsync()](/docs/reference/engine/classes/TextChannel#SendAsync) is called by the sending
client. Use this to allow placeholder messages to be shown to the user
while waiting for server response to [TextChannel:SendAsync()](/docs/reference/engine/classes/TextChannel#SendAsync).

Provide feedback

---

Callbacks

OnBubbleAdded

Called when a bubble chat is about to be displayed.

TextChatService.OnBubbleAdded(

message:[TextChatMessage](/docs/reference/engine/classes/TextChatMessage), adornee:[Instance](/docs/reference/engine/datatypes/Instance)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| message:[TextChatMessage](/docs/reference/engine/classes/TextChatMessage)  The incoming [TextChatMessage](/docs/reference/engine/classes/TextChatMessage). |
| adornee:[Instance](/docs/reference/engine/datatypes/Instance)  The part or character the bubble chat message is attached to. |

Returns

[Tuple](/docs/luau/tuples)

If a [BubbleChatMessageProperties](/docs/reference/engine/classes/BubbleChatMessageProperties) is returned, its properties
override the [BubbleChatConfiguration](/docs/reference/engine/classes/BubbleChatConfiguration) properties.

Called when a bubble chat is about to be displayed. This can only be
implemented on the client.

Use this to customize individual bubble chat messages. If this callback
returns a [BubbleChatMessageProperties](/docs/reference/engine/classes/BubbleChatMessageProperties), those properties will be
applied to the associated bubble, overriding
[BubbleChatConfiguration](/docs/reference/engine/classes/BubbleChatConfiguration) properties. If a [UICorner](/docs/reference/engine/classes/UICorner),
[UIGradient](/docs/reference/engine/classes/UIGradient), or [ImageLabel](/docs/reference/engine/classes/ImageLabel) is parented under
[BubbleChatMessageProperties](/docs/reference/engine/classes/BubbleChatMessageProperties), they will also override their
respective counterparts defined in [BubbleChatConfiguration](/docs/reference/engine/classes/BubbleChatConfiguration).

If the chat message is sent by a player, message.TextSource will
correspond to that player, and adornee will be nil.

If the chat message is sent via [TextChatService:DisplayBubble()](/docs/reference/engine/classes/TextChatService#DisplayBubble),
adornee will be the partOrCharacter provided, and message.TextSource
will be nil.

When bound to the client sending a message, this callback is run twice:
first when the message is initially sent and received locally, then again
when the client receives the result of the filtered message from the
server.

Provide feedback

---

OnChatWindowAdded

Called when a new message is about to be displayed in the chat window.
This can only be implemented on the client.

TextChatService.OnChatWindowAdded(message:[TextChatMessage](/docs/reference/engine/classes/TextChatMessage)):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| message:[TextChatMessage](/docs/reference/engine/classes/TextChatMessage)  The incoming [TextChatMessage](/docs/reference/engine/classes/TextChatMessage). |

Returns

[Tuple](/docs/luau/tuples)

If a [ChatWindowMessageProperties](/docs/reference/engine/classes/ChatWindowMessageProperties) is returned, its properties
override the [ChatWindowConfiguration](/docs/reference/engine/classes/ChatWindowConfiguration) properties.

Called when a new message is about to be displayed in the chat window.
This can only be implemented on the client.

Use this to customize individual messages that appear in the chat window.
If this callback returns a [ChatWindowMessageProperties](/docs/reference/engine/classes/ChatWindowMessageProperties), those
properties will be applied to the associated message, overriding
[ChatWindowConfiguration](/docs/reference/engine/classes/ChatWindowConfiguration) properties. If a [UIGradient](/docs/reference/engine/classes/UIGradient) is
parented under [ChatWindowMessageProperties](/docs/reference/engine/classes/ChatWindowMessageProperties), it will also override
the [TextColor3](/docs/reference/engine/classes/ChatWindowConfiguration#TextColor3) property defined
in [ChatWindowConfiguration](/docs/reference/engine/classes/ChatWindowConfiguration).

When bound to the client sending a message, this callback is run twice:
first when the message is initially sent and received locally, then again
when the client receives the result of the filtered message from the
server.

Provide feedback

---

OnIncomingMessage

Called when [TextChatService](/docs/reference/engine/classes/TextChatService) is receiving an incoming message.

TextChatService.OnIncomingMessage(message:[TextChatMessage](/docs/reference/engine/classes/TextChatMessage)):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| message:[TextChatMessage](/docs/reference/engine/classes/TextChatMessage)  The incoming [TextChatMessage](/docs/reference/engine/classes/TextChatMessage). |

Returns

[Tuple](/docs/luau/tuples)

If a [TextChatMessageProperties](/docs/reference/engine/classes/TextChatMessageProperties) is returned, those properties
are merged with the [TextChatMessage](/docs/reference/engine/classes/TextChatMessage) parameter to create a new
[TextChatMessage](/docs/reference/engine/classes/TextChatMessage) with those properties, otherwise, if nil is
returned, then [TextChatMessage](/docs/reference/engine/classes/TextChatMessage) is not changed.

Called when [TextChatService](/docs/reference/engine/classes/TextChatService) is receiving an incoming message. Can
only be implemented on the client.

Use this to decorate [TextChatMessages](/docs/reference/engine/classes/TextChatMessage). If this
callback returns a [TextChatMessageProperties](/docs/reference/engine/classes/TextChatMessageProperties), those properties are
merged with the [TextChatMessage](/docs/reference/engine/classes/TextChatMessage) parameter to create a new
[TextChatMessage](/docs/reference/engine/classes/TextChatMessage).

When bound to the client sending a message, this callback is run twice;
first when the message is initially sent and received locally, and again
when the client receives the result of the filtered message from the
server.

Note that this [TextChatService.OnIncomingMessage](/docs/reference/engine/classes/TextChatService#OnIncomingMessage) callback runs
before any [TextChannel.OnIncomingMessage](/docs/reference/engine/classes/TextChannel#OnIncomingMessage) callbacks.

This should be defined only once in the source code. Multiple bindings
will override one another in a non‑deterministic manner.

Provide feedback

---