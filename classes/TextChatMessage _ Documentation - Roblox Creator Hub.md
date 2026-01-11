# TextChatMessage | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TextChatMessage
Scraped: 2026-01-11T02:32:12.127566Z

## Tags
- Not Creatable

## Inherits
- Instance
- TextChatMessage
- BubbleChatMessageProperties
- ChatWindowMessageProperties
- TextChannel
- TextSource
- Object
- TextChannel:SendAsync()
- TextChannel:DisplaySystemMessage()
- TextChatService.OnIncomingMessage
- TextChannel.OnIncomingMessage
- TextChatCommand
- Team
- TextChatMessage.PrefixText
- Player.DisplayName
- TextSource.UserId
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [TextChatMessage](/docs/reference/engine/classes/TextChatMessage)

English

Feedback

Engine Class

TextChatMessage

A data object representing a text chat message.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [BubbleChatMessageProperties](#BubbleChatMessageProperties):[BubbleChatMessageProperties](/docs/reference/engine/classes/BubbleChatMessageProperties) |
| [ChatWindowMessageProperties](#ChatWindowMessageProperties):[ChatWindowMessageProperties](/docs/reference/engine/classes/ChatWindowMessageProperties) |
| [MessageId](#MessageId):[string](/docs/luau/strings) |
| [Metadata](#Metadata):[string](/docs/luau/strings) |
| [PrefixText](#PrefixText):[string](/docs/luau/strings) |
| [Status](#Status):[Enum.TextChatMessageStatus](/docs/reference/engine/enums/TextChatMessageStatus) |
| [Text](#Text):[string](/docs/luau/strings) |
| [TextChannel](#TextChannel):[TextChannel](/docs/reference/engine/classes/TextChannel) |
| [TextSource](#TextSource):[TextSource](/docs/reference/engine/classes/TextSource) |
| [Timestamp](#Timestamp):[DateTime](/docs/reference/engine/datatypes/DateTime) |
| [Translation](#Translation):[string](/docs/luau/strings) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A data object representing a text chat message.

To learn more about using TextChatMessages, see
[In-Experience Text Chat](/docs/chat/in-experience-text-chat).

---

API Reference

Properties

BubbleChatMessageProperties

Read Parallel

TextChatMessage.BubbleChatMessageProperties:[BubbleChatMessageProperties](/docs/reference/engine/classes/BubbleChatMessageProperties)

Provide feedback

---

ChatWindowMessageProperties

Read Parallel

TextChatMessage.ChatWindowMessageProperties:[ChatWindowMessageProperties](/docs/reference/engine/classes/ChatWindowMessageProperties)

Provide feedback

---

MessageId

Read Parallel

A unique identifier for the [TextChatMessage](/docs/reference/engine/classes/TextChatMessage).

TextChatMessage.MessageId:[string](/docs/luau/strings)

A unique identifier for the [TextChatMessage](/docs/reference/engine/classes/TextChatMessage).

Provide feedback

---

Metadata

Read Parallel

A general purpose field for storing miscellaneous data about the
[TextChatMessage](/docs/reference/engine/classes/TextChatMessage).

TextChatMessage.Metadata:[string](/docs/luau/strings)

A general purpose field for storing miscellaneous data about the
TextChatMessage. The second argument of [TextChannel:SendAsync()](/docs/reference/engine/classes/TextChannel#SendAsync)
and [TextChannel:DisplaySystemMessage()](/docs/reference/engine/classes/TextChannel#DisplaySystemMessage) is used to populate this
field.

Use this field to apply additional formatting for special messages within
[TextChatService.OnIncomingMessage](/docs/reference/engine/classes/TextChatService#OnIncomingMessage) and
[TextChannel.OnIncomingMessage](/docs/reference/engine/classes/TextChannel#OnIncomingMessage) callbacks.

```
local TextChatService = game:GetService("TextChatService")



local generalChannel: TextChannel = TextChatService:WaitForChild("TextChannels").RBXGeneral



generalChannel:DisplaySystemMessage("This is an error!", "Game.Error.Generic")



generalChannel:DisplaySystemMessage("Could not find save data!", "Game.Error.SaveDataNotFound")



generalChannel:DisplaySystemMessage("You won the game!", "Game.Info.Win")



generalChannel:DisplaySystemMessage("You lost the game!", "Game.Info.Lose")



generalChannel.OnIncomingMessage = function(message: TextChatMessage)



if string.find(message.Metadata, "Error") then



local overrideProperties = Instance.new("TextChatMessageProperties")



overrideProperties.TextColor = Color3.fromRGB(255, 0, 0)



return overrideProperties



elseif string.find(message.Metadata, "Info") then



local overrideProperties = Instance.new("TextChatMessageProperties")



overrideProperties.TextColor = Color3.fromRGB(0, 255, 150)



return overrideProperties



end



return nil



end
```

As follows is a reference of the default system messages emitted by the
chat system:

| Metadata | Description |
| --- | --- |
| Roblox.ChatTranslation.ChatWindow.SystemMessage | Indicates that the system may translate chat messages for the player. |
| Roblox.Notification.Friend.Joined | Displayed when one of the player's connections join the experience. |
| Roblox.MessageStatus.Warning.Floodchecked | Displayed when the player's sent message was rate limited by the server. |
| Roblox.MessageStatus.Warning.TextFilterFailed | Displayed when the player's sent message could not be displayed due to a text filtering issue. |
| Roblox.MessageStatus.Warning.InvalidPrivacySettings | Displayed when the player's privacy settings prevent them from sending a message. |
| Roblox.MessageStatus.Warning.MessageTooLong | Displayed when the player sends a message with content that is too long. |
| Roblox.MessageStatus.Warning.Unknown | Displays when the system fails to send the player's message for an unknown reason. |
| Roblox.Help.Info | Displays the response from the RBXHelpCommand [TextChatCommand](/docs/reference/engine/classes/TextChatCommand). |
| Roblox.Version.Info | Displays the response from the RBXVersionCommand [TextChatCommand](/docs/reference/engine/classes/TextChatCommand). |
| Roblox.Team.Success.NowInTeam | Displayed when the player's team changes. |
| Roblox.Team.Error.CannotTeamChatIfNotInTeam | Displayed when the player triggers the RBXTeamCommand [TextChatCommand](/docs/reference/engine/classes/TextChatCommand) without being on a [Team](/docs/reference/engine/classes/Team). |
| Roblox.Whisper.Info.Success | Displayed when the player successfully starts a whisper conversation. |
| Roblox.Whisper.Welcome.Sent | Displayed when entering a whisper [TextChannel](/docs/reference/engine/classes/TextChannel). |
| Roblox.Whisper.Error.CannotWhisperToSelf | An error response from the RBXWhisperCommand [TextChatCommand](/docs/reference/engine/classes/TextChatCommand). |
| Roblox.Whisper.Error.TargetDoesNotExist | An error response from the RBXWhisperCommand [TextChatCommand](/docs/reference/engine/classes/TextChatCommand). |
| Roblox.Whisper.Error.TooManyMatches | An error response from the RBXWhisperCommand [TextChatCommand](/docs/reference/engine/classes/TextChatCommand). |
| Roblox.Whisper.Error.Unknown | An error response from the RBXWhisperCommand [TextChatCommand](/docs/reference/engine/classes/TextChatCommand). |
| Roblox.Emote.Error.DoesNotExist | An error response from the RBXEmoteCommand [TextChatCommand](/docs/reference/engine/classes/TextChatCommand). |
| Roblox.Emote.Error.UserEmotesNotEnabled | An error response from the RBXEmoteCommand [TextChatCommand](/docs/reference/engine/classes/TextChatCommand). |
| Roblox.Emote.Error.TemporarilyUnavailable | An error response from the RBXEmoteCommand [TextChatCommand](/docs/reference/engine/classes/TextChatCommand). |
| Roblox.Emote.Error.NotSupported | An error response from the RBXEmoteCommand [TextChatCommand](/docs/reference/engine/classes/TextChatCommand). |
| Roblox.Emote.Error.SwitchToR15 | An error response from the RBXEmoteCommand [TextChatCommand](/docs/reference/engine/classes/TextChatCommand). |
| Roblox.Emote.Error.AnimationPlaying | An error response from the RBXEmoteCommand [TextChatCommand](/docs/reference/engine/classes/TextChatCommand). |
| Roblox.Mute.Error.PlayerNotFound | An error response from the RBXMuteCommand [TextChatCommand](/docs/reference/engine/classes/TextChatCommand). |
| Roblox.Mute.Error.MultipleMatches | An error response from the RBXMuteCommand [TextChatCommand](/docs/reference/engine/classes/TextChatCommand). |
| Roblox.Mute.Error.CannotMuteSelf | An error response from the RBXMuteCommand [TextChatCommand](/docs/reference/engine/classes/TextChatCommand). |
| Roblox.Mute.Info.Success | An success response from the RBXMuteCommand [TextChatCommand](/docs/reference/engine/classes/TextChatCommand). |
| Roblox.Unmute.Error.PlayerNotFound | An error response from the RBXUnmuteCommand [TextChatCommand](/docs/reference/engine/classes/TextChatCommand). |
| Roblox.Unmute.Error.MultipleMatches | An error response from the RBXUnmuteCommand [TextChatCommand](/docs/reference/engine/classes/TextChatCommand). |
| Roblox.Unmute.Error.CannotMuteSelf | An error response from the RBXUnmuteCommand [TextChatCommand](/docs/reference/engine/classes/TextChatCommand). |
| Roblox.Unmute.Info.Success | An success response from the RBXUnmuteCommand [TextChatCommand](/docs/reference/engine/classes/TextChatCommand). |

Provide feedback

---

PrefixText

Read Parallel

A prefix to add to a user's message.

TextChatMessage.PrefixText:[string](/docs/luau/strings)

A prefix to add to a user's message. This supports Rich Text, so
developers can set custom properties for this text to support chat tags.

By default, [TextChatMessage.PrefixText](/docs/reference/engine/classes/TextChatMessage#PrefixText) is the name of the
[TextSource](/docs/reference/engine/classes/TextSource), which is the [Player.DisplayName](/docs/reference/engine/classes/Player#DisplayName) of the user
associated with the [TextSource](/docs/reference/engine/classes/TextSource) via [TextSource.UserId](/docs/reference/engine/classes/TextSource#UserId).

Provide feedback

---

Status

Read Parallel

Indicates the status of the [TextChatMessage](/docs/reference/engine/classes/TextChatMessage).

TextChatMessage.Status:[Enum.TextChatMessageStatus](/docs/reference/engine/enums/TextChatMessageStatus)

Indicates the status of the [TextChatMessage](/docs/reference/engine/classes/TextChatMessage).

Provide feedback

---

Text

Read Parallel

The filtered text message for the user.

TextChatMessage.Text:[string](/docs/luau/strings)

The filtered text message for the user. Different users may receive
different strings from this property based on filtering rules. It can be
an empty string.

Provide feedback

---

TextChannel

Read Parallel

A reference to the origin [TextChannel](/docs/reference/engine/classes/TextChannel).

TextChatMessage.TextChannel:[TextChannel](/docs/reference/engine/classes/TextChannel)

A reference to the origin [TextChannel](/docs/reference/engine/classes/TextChannel).

Provide feedback

---

TextSource

Read Parallel

A reference to the origin [TextSource](/docs/reference/engine/classes/TextSource).

TextChatMessage.TextSource:[TextSource](/docs/reference/engine/classes/TextSource)

A reference to the origin [TextSource](/docs/reference/engine/classes/TextSource).

Provide feedback

---

Timestamp

Read Parallel

A timestamp of when the message was originally sent.

TextChatMessage.Timestamp:[DateTime](/docs/reference/engine/datatypes/DateTime)

A timestamp of when the message was originally sent.

Provide feedback

---

Translation

Read Parallel

Translated and filtered text message.

TextChatMessage.Translation:[string](/docs/luau/strings)

Represents translated and filtered text messages based on users'
localization settings. The system doesn't translate messages between users
with the same localization settings or using languages without the text
filter support, so this property can be an empty string if no translation
happens. For customization, see
[Customizing Translated Messages](/docs/chat/chat-window).

Provide feedback

---