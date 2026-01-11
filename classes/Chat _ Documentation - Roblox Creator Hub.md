# Chat | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Chat
Scraped: 2026-01-11T02:40:13.629668Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Object
- Instance
- Chat
- TextChatService
- Player
- StarterPlayerScripts
- Scripts
- ModuleScripts
- Player.Character
- LocalScript
- Script
- Player.UserId
- Chat.Chatted
- PlayerScripts
- TextService:FilterStringAsync()
- TextBox
- Chat:FilterStringAsync()
- LocalScripts
- RegisterChatCallback
- Chat:RegisterChatCallback()
- InvokeChatCallback
- Chat.BubbleChatEnabled
- Chat:Chat()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Chat](/docs/reference/engine/classes/Chat)

English

Feedback

Engine Class

![Chat](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Chat-Dark.webp)Chat

Deprecated

Houses the Luau code responsible for running the legacy chat system.

Not Creatable

Service

Not Replicated

This class is deprecated. Use [TextChatService](/docs/reference/engine/classes/TextChatService) instead.

---

Summary

Properties

|  |
| --- |
| [BubbleChatEnabled](#BubbleChatEnabled):[boolean](/docs/luau/booleans) |
| [LoadDefaultChat](#LoadDefaultChat):[boolean](/docs/luau/booleans) |

Methods

|  |
| --- |
| [CanUserChatAsync](#CanUserChatAsync)(userId: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans) |
| [CanUsersChatAsync](#CanUsersChatAsync)(userIdFrom: [number](/docs/luau/numbers),userIdTo: [number](/docs/luau/numbers)):[boolean](/docs/luau/booleans) |
| [Chat](#Chat)(partOrCharacter: [Instance](/docs/reference/engine/datatypes/Instance),message: [string](/docs/luau/strings),color: [Enum.ChatColor](/docs/reference/engine/enums/ChatColor)):() |
| [FilterStringAsync](#FilterStringAsync)(stringToFilter: [string](/docs/luau/strings),playerFrom: [Player](/docs/reference/engine/classes/Player),playerTo: [Player](/docs/reference/engine/classes/Player)):[string](/docs/luau/strings) |
| [FilterStringForBroadcast](#FilterStringForBroadcast)(stringToFilter: [string](/docs/luau/strings),playerFrom: [Player](/docs/reference/engine/classes/Player)):[string](/docs/luau/strings) |
| [FilterStringForPlayerAsync](#FilterStringForPlayerAsync)(stringToFilter: [string](/docs/luau/strings),playerToFilterFor: [Player](/docs/reference/engine/classes/Player)):[string](/docs/luau/strings)  Deprecated |
| [InvokeChatCallback](#InvokeChatCallback)(callbackType: [Enum.ChatCallbackType](/docs/reference/engine/enums/ChatCallbackType),callbackArguments: [Tuple](/docs/luau/tuples)):[Tuple](/docs/luau/tuples) |
| [RegisterChatCallback](#RegisterChatCallback)(callbackType: [Enum.ChatCallbackType](/docs/reference/engine/enums/ChatCallbackType),callbackFunction: [function](/docs/luau/functions)):() |
| [SetBubbleChatSettings](#SetBubbleChatSettings)(settings: Variant):() |

Events

|  |
| --- |
| [Chatted](#Chatted)(part: [Instance](/docs/reference/engine/datatypes/Instance),message: [string](/docs/luau/strings),color: [Enum.ChatColor](/docs/reference/engine/enums/ChatColor)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The Chat service houses the Luau code responsible for running the
[legacy chat system](/docs/chat/in-experience-text-chat#migrate-from-legacy-chat).
Similar to [StarterPlayerScripts](/docs/reference/engine/classes/StarterPlayerScripts), default objects like
[Scripts](/docs/reference/engine/classes/Script) and [ModuleScripts](/docs/reference/engine/classes/ModuleScript) are inserted
into the service.

---

API Reference

Properties

BubbleChatEnabled

Read Parallel

Determines whether player's chat messages will appear above their in-game
avatar.

Chat.BubbleChatEnabled:[boolean](/docs/luau/booleans)

If true, entering a message in the chat will result in a chat bubble
popping up above the player's [Player.Character](/docs/reference/engine/classes/Player#Character). This behavior can
either be enabled by directly ticking this checkbox in Studio, or by using
a [LocalScript](/docs/reference/engine/classes/LocalScript):

```
local ChatService = game:GetService("Chat")



ChatService.BubbleChatEnabled = true
```

This must be done on the client, toggling this value in a server-side
[Script](/docs/reference/engine/classes/Script) will have no effect.

Provide feedback

---

LoadDefaultChat

Not Accessible Security

Read Parallel

Toggles whether the default chat framework should be automatically loaded
when the game runs.

Chat.LoadDefaultChat:[boolean](/docs/luau/booleans)

Toggles whether the default chat framework should be automatically loaded
when the game runs.

Provide feedback

---

Methods

CanUserChatAsync

Yields

Will return false if the player with the specified [Player.UserId](/docs/reference/engine/classes/Player#UserId)
is not allowed to chat because of their account settings.

Chat:CanUserChatAsync(userId:[number](/docs/luau/numbers)):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| userId:[number](/docs/luau/numbers) |

Returns

[boolean](/docs/luau/booleans)

Will return false if the player with the specified [Player.UserId](/docs/reference/engine/classes/Player#UserId)
is not allowed to chat because of their account settings.

Provide feedback

---

CanUsersChatAsync

Yields

Will return false if the two users cannot communicate because their
account settings do not allow it.

Chat:CanUsersChatAsync(

userIdFrom:[number](/docs/luau/numbers), userIdTo:[number](/docs/luau/numbers)

):[boolean](/docs/luau/booleans)

Parameters

|  |
| --- |
| userIdFrom:[number](/docs/luau/numbers) |
| userIdTo:[number](/docs/luau/numbers) |

Returns

[boolean](/docs/luau/booleans)

Will return false if the two users cannot communicate because their
account settings do not allow it.

Provide feedback

---

Chat

Fires the [Chat.Chatted](/docs/reference/engine/classes/Chat#Chatted) event with the parameters specified in this
method.

Chat:Chat(

partOrCharacter:[Instance](/docs/reference/engine/datatypes/Instance), message:[string](/docs/luau/strings), color:[Enum.ChatColor](/docs/reference/engine/enums/ChatColor)

):()

Parameters

|  |
| --- |
| partOrCharacter:[Instance](/docs/reference/engine/datatypes/Instance)  An instance that is the part or character which the *BubbleChat* dialog should appear above. |
| message:[string](/docs/luau/strings)  The message string being chatted. |
| color:[Enum.ChatColor](/docs/reference/engine/enums/ChatColor) Default Value: "Blue" An [Enum.ChatColor](/docs/reference/engine/enums/ChatColor) specifying the color of the chatted message. |

Returns

()

The Chat function fires the [Chat.Chatted](/docs/reference/engine/classes/Chat#Chatted) event with the parameters
specified in this method.

By default, there is a [LocalScript](/docs/reference/engine/classes/LocalScript) inside of each player's
[PlayerScripts](/docs/reference/engine/classes/PlayerScripts) object named *BubbleChat*, which causes a
dialog-like billboard to appear above the *partOrCharacter* when the
chatted event is fired.

*Note:* Since dialogs are controlled by a LocalScript, you will not be
able to see any dialogs created from this method unless you are running in
*Play Solo* mode.

Code Samples

Chat:Chat

The below example would create a part in Workspace and cause it to exclaim
"Blame John!"

```
local ChatService = game:GetService("Chat")



local part = Instance.new("Part")



part.Anchored = true



part.Parent = workspace



ChatService:Chat(part, "Blame John!", "Red")
```

Provide feedback

---

FilterStringAsync

Yields

Filters a string sent from a player to another player using filtering that
is appropriate to the players' account settings.

Chat:FilterStringAsync(

stringToFilter:[string](/docs/luau/strings), playerFrom:[Player](/docs/reference/engine/classes/Player), playerTo:[Player](/docs/reference/engine/classes/Player)

):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| stringToFilter:[string](/docs/luau/strings)  The raw string to be filtered, exactly as entered by the player. |
| playerFrom:[Player](/docs/reference/engine/classes/Player)  The author of the text. |
| playerTo:[Player](/docs/reference/engine/classes/Player)  The intended recipient of the provided text; use the author if the text is persistent (see description). |

Returns

[string](/docs/luau/strings)

Partial Deprecation Warning: Calling this function from the client
using a [LocalScript](/docs/reference/engine/classes/LocalScript) is deprecated, and will be disabled in the
future. Text filtering should be done from a [Script](/docs/reference/engine/classes/Script) on the server
using the similarly-named [TextService:FilterStringAsync()](/docs/reference/engine/classes/TextService#FilterStringAsync), which
uses a different set of parameters and return type.

Games that do not properly filter player-generated text might be subject
to moderation action. Please be sure a game properly filters text before
publishing it.

FilterStringAsync filters a string using filtering that is appropriate
for the sending and receiving player. If the filtered string is to be used
for a persistent message, such as the name of a shop, writing on a plaque,
etc, then the function should be called with the author as both the sender
and receiver.

This function should be used every time a player can enter custom text
in any context, most commonly using a [TextBox](/docs/reference/engine/classes/TextBox). Some examples
of text to be filtered:

* Custom chat messages
* Custom character names
* Names for a shop in a tycoon-style game

Provide feedback

---

FilterStringForBroadcast

Yields

Filters a string sent from a player meant for broadcast to no particular
target. More restrictive than [Chat:FilterStringAsync()](/docs/reference/engine/classes/Chat#FilterStringAsync).

Chat:FilterStringForBroadcast(

stringToFilter:[string](/docs/luau/strings), playerFrom:[Player](/docs/reference/engine/classes/Player)

):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| stringToFilter:[string](/docs/luau/strings)  Message string being filtered. |
| playerFrom:[Player](/docs/reference/engine/classes/Player)  Instance of the player sending the message. |

Returns

[string](/docs/luau/strings)

Filtered message string.

Filters a string sent from *playerFrom* for broadcast to no particular
target. The filtered message has more restrictions than
[Chat:FilterStringAsync()](/docs/reference/engine/classes/Chat#FilterStringAsync).

Some examples of where this method could be used:

* Message walls
* Cross-server shouts
* User-created signs

Calling FilterString from [LocalScripts](/docs/reference/engine/classes/LocalScript) is deprecated
and will be disabled in the future. Text filtering should be done from
server-side [Scripts](/docs/reference/engine/classes/Script) using FilterStringAsync.

*Note:* A game not using this filter function for custom chat or other
user generated text may be subjected to moderation action.

Code Samples

Chat:FilterStringForBroadcast

The following example shows a simple way to use the FilterStringForBroadcast
function. The example uses the message variable as the *stringToFilter*
argument and the local player as the *playerFrom* argument.

The example then prints the result of the filtering function,
*FilteredString*.

```
local Players = game:GetService("Players")



local Chat = game:GetService("Chat")



local playerFrom = Players.LocalPlayer



local message = "Hello world!"



-- Filter the string and store the result in the 'FilteredString' variable



local filteredString = Chat:FilterStringForBroadcast(message, playerFrom)



print(filteredString)
```

Provide feedback

---

FilterStringForPlayerAsync

Deprecated

Show details

---

InvokeChatCallback

Invoke a chat callback function registered by
[RegisterChatCallback](/docs/reference/engine/classes/Chat#RegisterChatCallback). Used by the Luau
Chat System.

Chat:InvokeChatCallback(

callbackType:[Enum.ChatCallbackType](/docs/reference/engine/enums/ChatCallbackType), callbackArguments:[Tuple](/docs/luau/tuples)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| callbackType:[Enum.ChatCallbackType](/docs/reference/engine/enums/ChatCallbackType)  The type of callback to invoke. |
| callbackArguments:[Tuple](/docs/luau/tuples)  The arguments that will be sent to the registered callback function. |

Returns

[Tuple](/docs/luau/tuples)

The values returned by the function registered to the given
ChatCallbackType.

InvokeChatCallback will call a function registered by
[RegisterChatCallback](/docs/reference/engine/classes/Chat#RegisterChatCallback), given the
ChatCallbackType enum and the arguments to send the function. It will
return the result of the registered function, or raise an error if no
function has been registered.

This function is called by the Luau Chat System so that chat callbacks may
be registered to change the behavior of certain features. Unless you are
replacing the default Luau Chat System with your own, you should not need
to call this function. You can read about the different callback functions
at [Chat:RegisterChatCallback()](/docs/reference/engine/classes/Chat#RegisterChatCallback).

Provide feedback

---

RegisterChatCallback

Register a function to be called upon the invocation of some chat system
event ([InvokeChatCallback](/docs/reference/engine/classes/Chat#InvokeChatCallback)).

Chat:RegisterChatCallback(

callbackType:[Enum.ChatCallbackType](/docs/reference/engine/enums/ChatCallbackType), callbackFunction:[function](/docs/luau/functions)

):()

Parameters

|  |
| --- |
| callbackType:[Enum.ChatCallbackType](/docs/reference/engine/enums/ChatCallbackType)  The callback to which the function shall be registered (this determines in what way the function is called). |
| callbackFunction:[function](/docs/luau/functions)  The function to call when the callback is invoked using Chat:InvokeChatCallback. |

Returns

()

RegisterChatCallback binds a function to some chat system event in order
to affect the behavior of the Luau chat system. The first argument
determines the event (using the [Enum.ChatCallbackType](/docs/reference/engine/enums/ChatCallbackType) enum) to which the
second argument, the function, shall be bound. The default Luau chat
system uses [InvokeChatCallback](/docs/reference/engine/classes/Chat#InvokeChatCallback) to invoke
registered functions. Attempting to register a server- or client- only
callback on a peer that isn't a server or client respectively will raise
an error. The following sections describe in what ways registered
functions will be used.

#### OnCreatingChatWindow

Client-only. Invoked before the client constructs the chat window. Must
return a table of settings to be merged into the information returned by
the ChatSettings module.

#### OnClientFormattingMessage

Client-only. Invoked before the client displays a message (whether it is a
player chat message, system message, or /me command). This function is
invoked with the message object and may (or may not) return a table to be
merged into message.ExtraData.

#### OnClientSendingMessage

Not invoked at this time.

#### OnServerReceivingMessage

Server-only. Invoked when the server receives a message from a speaker
(note that speakers may not necessarily be a [Player](/docs/reference/engine/classes/Player) chatting).
This callback is called with the Message object. The function can make
changes to the Message object to change the manner in which the message is
processed. The Message object must be returned for this callback to do
anything. Setting this callback can allow the server to, for example:

* Set message.ShouldDeliver to false in order to cancel delivery of the
  message to players (useful for implementing a chat exclusion list)
* Get/set the speaker's name color (message.ExtraData.NameColor, a
  Color3) on a message-by-message basis

Provide feedback

---

SetBubbleChatSettings

Customizes various settings of the in-game bubble chat.

Chat:SetBubbleChatSettings(settings:Variant):()

Parameters

|  |
| --- |
| settings:Variant  A settings table. |

Returns

()

This function customizes various settings of the in-game bubble chat.

Before using this, make sure that bubble chat is enabled by setting
[Chat.BubbleChatEnabled](/docs/reference/engine/classes/Chat#BubbleChatEnabled) to true.

The settings argument is a table where the keys are the names of the
settings you want to edit and the values are what you want to change these
settings to. Note that you don't have to include all of them in the
settings argument, omitting some will result in them keeping their default
value.

This function is client-side only, attempting to call it on the server
will trigger an error.

Code Samples

Customize visual aspects

When run from a LocalScript, this snippet will make all the chat bubbles
appear with bigger text under a different font and a light blue background.
Note that all the other settings will keep their default value.

```
local ChatService = game:GetService("Chat")



ChatService:SetBubbleChatSettings({



BackgroundColor3 = Color3.fromRGB(180, 210, 228),



TextSize = 20,



Font = Enum.Font.Cartoon,



})
```

Restore default settings

If you want to reset the bubble chat to its default look, you can call this
function with an empty table, because any setting you omit from the argument
will result in it returning to its default value:

```
local ChatService = game:GetService("Chat")



ChatService:SetBubbleChatSettings({})
```

Provide feedback

---

Events

Chatted

Fires when [Chat:Chat()](/docs/reference/engine/classes/Chat#Chat) is called.

Chat.Chatted(

part:[Instance](/docs/reference/engine/datatypes/Instance), message:[string](/docs/luau/strings), color:[Enum.ChatColor](/docs/reference/engine/enums/ChatColor)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| part:[Instance](/docs/reference/engine/datatypes/Instance) |
| message:[string](/docs/luau/strings) |
| color:[Enum.ChatColor](/docs/reference/engine/enums/ChatColor) |

Fires when [Chat:Chat()](/docs/reference/engine/classes/Chat#Chat) is called.

Provide feedback

---