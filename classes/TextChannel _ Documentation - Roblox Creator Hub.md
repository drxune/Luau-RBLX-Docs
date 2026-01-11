# TextChannel | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TextChannel
Scraped: 2026-01-11T02:38:07.234441Z

## Tags
- Not Replicated

## Inherits
- Object
- Instance
- TextChannel
- Player
- TextChatMessage
- TextSource
- TextSources
- TextChannel:SendAsync()
- LocalScript
- ChannelTabsConfiguration
- SetDirectChatRequester()
- Player.UserId
- Script
- TextChatMessage.Status
- RunContext
- TextChatMessage.Metadata
- TextChatMessage.Text
- DirectChatRequester
- TextChatService
- TextChannel:DisplaySystemMessage()
- TextChatService.MessageReceived
- TextChannel.ShouldDeliverCallback
- TextChannel.MessageReceived
- TextChatService.OnIncomingMessage
- TextChannel.OnIncomingMessage
- TextChatMessageProperties
- TextChatMessages
- TextChatService:CreateDefaultTextChannels()
- TextChannels
- TextChatMessage.TextSource
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [TextChannel](/docs/reference/engine/classes/TextChannel)

English

Feedback

Engine Class

![TextChannel](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/TextChannel-Dark.webp)TextChannel

Represents a text chat channel.

---

Summary

Properties

|  |
| --- |
| [DirectChatRequester](#DirectChatRequester):[Player](/docs/reference/engine/classes/Player) |

Methods

|  |
| --- |
| [AddUserAsync](#AddUserAsync)(userId: [number](/docs/luau/numbers)):[Tuple](/docs/luau/tuples) |
| [DisplaySystemMessage](#DisplaySystemMessage)(systemMessage: [string](/docs/luau/strings),metadata: [string](/docs/luau/strings)):[TextChatMessage](/docs/reference/engine/classes/TextChatMessage) |
| [SendAsync](#SendAsync)(message: [string](/docs/luau/strings),metadata: [string](/docs/luau/strings)):[TextChatMessage](/docs/reference/engine/classes/TextChatMessage) |
| [SetDirectChatRequester](#SetDirectChatRequester)(requester: [Player](/docs/reference/engine/classes/Player)):() |

Events

|  |
| --- |
| [MessageReceived](#MessageReceived)(incomingMessage: [TextChatMessage](/docs/reference/engine/classes/TextChatMessage)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Callbacks

|  |
| --- |
| [OnIncomingMessage](#OnIncomingMessage)(message: [TextChatMessage](/docs/reference/engine/classes/TextChatMessage)):[Tuple](/docs/luau/tuples) |
| [ShouldDeliverCallback](#ShouldDeliverCallback)(message: [TextChatMessage](/docs/reference/engine/classes/TextChatMessage),textSource: [TextSource](/docs/reference/engine/classes/TextSource)):[Tuple](/docs/luau/tuples) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Represents a text chat channel. Contains [TextSources](/docs/reference/engine/classes/TextSource) as
descendants.

To send a chat message to the [TextChannel](/docs/reference/engine/classes/TextChannel), call
[TextChannel:SendAsync()](/docs/reference/engine/classes/TextChannel#SendAsync) from a [LocalScript](/docs/reference/engine/classes/LocalScript). The corresponding
[TextSource](/docs/reference/engine/classes/TextSource) of the user with TextSource.CanSend = true must be in
that channel.

Messages from different TextChannels can be separated into different tabs in
the chat window using [ChannelTabsConfiguration](/docs/reference/engine/classes/ChannelTabsConfiguration).

To learn more, see
[In-Experience Text Chat](/docs/chat/in-experience-text-chat).

---

API Reference

Properties

DirectChatRequester

Read Only

Not Replicated

Read Parallel

The TextChannel will only deliver messages to users that can send direct
messages to the DirectChatRequester.

TextChannel.DirectChatRequester:[Player](/docs/reference/engine/classes/Player)

The TextChannel will only deliver messages to users that can send direct
messages to the DirectChatRequester. This property can only be set using
[SetDirectChatRequester()](/docs/reference/engine/classes/TextChannel#SetDirectChatRequester).

Provide feedback

---

Methods

AddUserAsync

Yields

Adds a [TextSource](/docs/reference/engine/classes/TextSource) to the [TextChannel](/docs/reference/engine/classes/TextChannel) given userId of a
[Player](/docs/reference/engine/classes/Player).

TextChannel:AddUserAsync(userId:[number](/docs/luau/numbers)):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| userId:[number](/docs/luau/numbers)  The userId of the [Player](/docs/reference/engine/classes/Player). |

Returns

[Tuple](/docs/luau/tuples)

Returns [TextSource](/docs/reference/engine/classes/TextSource) and true if a new [TextSource](/docs/reference/engine/classes/TextSource) is
created for the user, [TextSource](/docs/reference/engine/classes/TextSource) and false if there is an
existing [TextSource](/docs/reference/engine/classes/TextSource), or nil and false if the user has chat
off or is not in this server.

Adds a [TextSource](/docs/reference/engine/classes/TextSource) to the [TextChannel](/docs/reference/engine/classes/TextChannel) given userId of the
user (with [Player.UserId](/docs/reference/engine/classes/Player#UserId)). Can only be used in a [Script](/docs/reference/engine/classes/Script).

If a [TextSource](/docs/reference/engine/classes/TextSource) representing the user does not exist, this adds a
[TextSource](/docs/reference/engine/classes/TextSource).

If a [TextSource](/docs/reference/engine/classes/TextSource) representing the user does exist, this returns the
[TextSource](/docs/reference/engine/classes/TextSource).

If the user has chat off or isn't in the server, this returns a tuple
nil, false.

Provide feedback

---

DisplaySystemMessage

Displays a system message to the user.

TextChannel:DisplaySystemMessage(

systemMessage:[string](/docs/luau/strings), metadata:[string](/docs/luau/strings)

):[TextChatMessage](/docs/reference/engine/classes/TextChatMessage)

Parameters

|  |
| --- |
| systemMessage:[string](/docs/luau/strings)  The system message sent to the [TextChannel](/docs/reference/engine/classes/TextChannel). |
| metadata:[string](/docs/luau/strings)  Use to identify system message types, such as the default system messages. |

Returns

[TextChatMessage](/docs/reference/engine/classes/TextChatMessage)

A [TextChatMessage](/docs/reference/engine/classes/TextChatMessage) with [TextChatMessage.Status](/docs/reference/engine/classes/TextChatMessage#Status) property
that indicates the condition of the message.

Displays a system message to user. Can only be used in a
[LocalScript](/docs/reference/engine/classes/LocalScript), or in a [Script](/docs/reference/engine/classes/Script) with
[RunContext](/docs/reference/engine/classes/Script#RunContext) of [Enum.RunContext.Client](/docs/reference/engine/enums/RunContext#Client). Messages
are only visible to that user and aren't automatically filtered or
localized.

Provide feedback

---

SendAsync

Yields

Sends a [TextChatMessage](/docs/reference/engine/classes/TextChatMessage) to the server.

TextChannel:SendAsync(

message:[string](/docs/luau/strings), metadata:[string](/docs/luau/strings)

):[TextChatMessage](/docs/reference/engine/classes/TextChatMessage)

Parameters

|  |
| --- |
| message:[string](/docs/luau/strings)  The message to send to the [TextChannel](/docs/reference/engine/classes/TextChannel). |
| metadata:[string](/docs/luau/strings)  Custom metadata to attach to the message. |

Returns

[TextChatMessage](/docs/reference/engine/classes/TextChatMessage)

A [TextChatMessage](/docs/reference/engine/classes/TextChatMessage) with [TextChatMessage.Status](/docs/reference/engine/classes/TextChatMessage#Status) property
that indicates the condition of the message.

Sends a [TextChatMessage](/docs/reference/engine/classes/TextChatMessage) to the server. Can only be used in a
[LocalScript](/docs/reference/engine/classes/LocalScript), or in a [Script](/docs/reference/engine/classes/Script) with
[RunContext](/docs/reference/engine/classes/Script#RunContext) of [Enum.RunContext.Client](/docs/reference/engine/enums/RunContext#Client).

The metadata argument has a limit of 200 characters. If this is called
with a metadata argument that has more than 200 characters, the message
will not be sent to other users. Instead, the sender will receive a
[TextChatMessage](/docs/reference/engine/classes/TextChatMessage) with the [TextChatMessage.Metadata](/docs/reference/engine/classes/TextChatMessage#Metadata) and
[TextChatMessage.Text](/docs/reference/engine/classes/TextChatMessage#Text) properties set to empty strings.

Provide feedback

---

SetDirectChatRequester

Sets the [DirectChatRequester](/docs/reference/engine/classes/TextChannel#DirectChatRequester) for
the TextChannel. The TextChannel will only deliver messages to users
that can send direct messages to the DirectChatRequester.

TextChannel:SetDirectChatRequester(requester:[Player](/docs/reference/engine/classes/Player)):()

Parameters

|  |
| --- |
| requester:[Player](/docs/reference/engine/classes/Player) |

Returns

()

Sets the [DirectChatRequester](/docs/reference/engine/classes/TextChannel#DirectChatRequester) for
the TextChannel. This method is only available for use in server
scripts.

Use this API if you are working with [TextChatService](/docs/reference/engine/classes/TextChatService) and have a
custom implementation of direct chat outside of the default text channels.

When called on a TextChannel that is parented to TextChatService and
has no existing TextSources, SetDirectChatRequester adds the requested
users as a TextSource and set the DirectChatRequester property for the
channel.

When DirectChatRequester is set, only messages between users that can
direct chat with the DirectChatRequester are delivered.

```
local function createWhisperChannel(fromPlayer, toPlayer)



local whisperChannel = Instance.new("TextChannel")



whisperChannel:SetDirectChatRequester(fromPlayer)



whisperChannel:AddUserAsync(toPlayer.UserId)



-- The TextChannel instance now has two TextSource instances.



return whisperChannel



end
```

Provide feedback

---

Events

MessageReceived

Fires when [TextChannel:DisplaySystemMessage()](/docs/reference/engine/classes/TextChannel#DisplaySystemMessage) is invoked on the
client, or when the client receives a valid
[TextChannel:SendAsync()](/docs/reference/engine/classes/TextChannel#SendAsync) response from the server.

TextChannel.MessageReceived(incomingMessage:[TextChatMessage](/docs/reference/engine/classes/TextChatMessage)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| incomingMessage:[TextChatMessage](/docs/reference/engine/classes/TextChatMessage)  The received [TextChatMessage](/docs/reference/engine/classes/TextChatMessage). |

Like [TextChatService.MessageReceived](/docs/reference/engine/classes/TextChatService#MessageReceived), fires when
[TextChannel:DisplaySystemMessage()](/docs/reference/engine/classes/TextChannel#DisplaySystemMessage) is invoked on the client, or
when the client receives a valid [TextChannel:SendAsync()](/docs/reference/engine/classes/TextChannel#SendAsync) response
from the server. This event is only fired on the client.

If the server's [TextChannel.ShouldDeliverCallback](/docs/reference/engine/classes/TextChannel#ShouldDeliverCallback) property is
bound and returns false, the client will not fire
[TextChannel.MessageReceived](/docs/reference/engine/classes/TextChannel#MessageReceived).

Use the [TextChatMessage](/docs/reference/engine/classes/TextChatMessage) parameter to get the [TextSource](/docs/reference/engine/classes/TextSource)
and the text of the message (with [TextChatMessage.Text](/docs/reference/engine/classes/TextChatMessage#Text)).

The [TextChatMessage](/docs/reference/engine/classes/TextChatMessage) parameter is the final result of any functions
bound to [TextChatService.OnIncomingMessage](/docs/reference/engine/classes/TextChatService#OnIncomingMessage) or
[TextChannel.OnIncomingMessage](/docs/reference/engine/classes/TextChannel#OnIncomingMessage).

Provide feedback

---

Callbacks

OnIncomingMessage

Called when [TextChannel](/docs/reference/engine/classes/TextChannel) is receiving an incoming message.

TextChannel.OnIncomingMessage(message:[TextChatMessage](/docs/reference/engine/classes/TextChatMessage)):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| message:[TextChatMessage](/docs/reference/engine/classes/TextChatMessage)  The incoming [TextChatMessage](/docs/reference/engine/classes/TextChatMessage). |

Returns

[Tuple](/docs/luau/tuples)

If a [TextChatMessageProperties](/docs/reference/engine/classes/TextChatMessageProperties) is returned, those properties
are merged with the [TextChatMessage](/docs/reference/engine/classes/TextChatMessage) parameter to create a new
[TextChatMessage](/docs/reference/engine/classes/TextChatMessage) with those properties.

Called when [TextChannel](/docs/reference/engine/classes/TextChannel) is receiving an incoming message. Can only
be implemented on the client.

Use this to decorate [TextChatMessages](/docs/reference/engine/classes/TextChatMessage). If this
callback returns a [TextChatMessageProperties](/docs/reference/engine/classes/TextChatMessageProperties), those properties are
merged with the [TextChatMessage](/docs/reference/engine/classes/TextChatMessage) parameter to create a new
[TextChatMessage](/docs/reference/engine/classes/TextChatMessage).

When bound to the client sending a message, this callback is run twice;
first when the message is initially sent and received locally, and again
when the client receives the result of the filtered message from the
server.

[TextChannel.OnIncomingMessage](/docs/reference/engine/classes/TextChannel#OnIncomingMessage) callbacks always run after the
[TextChatService.OnIncomingMessage](/docs/reference/engine/classes/TextChatService#OnIncomingMessage) callback.

This should be defined only once per [TextChannel](/docs/reference/engine/classes/TextChannel) in the source
code. Multiple bindings to the same channel will override one another in a
nondeterministic manner.

When [TextChatService:CreateDefaultTextChannels()](/docs/reference/engine/classes/TextChatService#CreateDefaultTextChannels) is true, those
default [TextChannels](/docs/reference/engine/classes/TextChannel) have their
[TextChannel.OnIncomingMessage](/docs/reference/engine/classes/TextChannel#OnIncomingMessage) callbacks assigned internally in
order to exhibit special default behavior.

Provide feedback

---

ShouldDeliverCallback

Called for each client when [TextChannel](/docs/reference/engine/classes/TextChannel) is receiving an incoming
message to determine whether or not it should be delivered to that client.

TextChannel.ShouldDeliverCallback(

message:[TextChatMessage](/docs/reference/engine/classes/TextChatMessage), textSource:[TextSource](/docs/reference/engine/classes/TextSource)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| message:[TextChatMessage](/docs/reference/engine/classes/TextChatMessage)  The message being sent, which also contains the sender of the message. |
| textSource:[TextSource](/docs/reference/engine/classes/TextSource)  The [TextSource](/docs/reference/engine/classes/TextSource) of the user who will be receiving the message. |

Returns

[Tuple](/docs/luau/tuples)

Called for each client when [TextChannel](/docs/reference/engine/classes/TextChannel) is receiving an incoming
message to determine whether or not it should be delivered to that client.
Can only be defined on the server.

Once defined, this callback needs to return a truthy value such as true,
1, or "hello" to deliver the message to said client. If the callback
returns anything else (including nil), the message won't be delivered to
that client, although the sender will see the message regardless.

The sender can be referenced by [TextChatMessage.TextSource](/docs/reference/engine/classes/TextChatMessage#TextSource), while
the receiver is the textSource argument. Note that the sender and
receiver can be the same, as the callback iterates through all possible
receivers.

Provide feedback

---