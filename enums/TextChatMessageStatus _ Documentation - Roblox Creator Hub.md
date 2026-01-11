# TextChatMessageStatus | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/TextChatMessageStatus
Scraped: 2026-01-11T02:43:03.894057Z

## Inherits
- TextChatMessage
- TextChannel:SendAsync()
- TextSource
- TextChannel
- TextSource.CanSend
1. [Enums](/docs/reference/engine/enums)
2. /
3. [TextChatMessageStatus](/docs/reference/engine/enums/TextChatMessageStatus)

English

Feedback

Engine Enum

TextChatMessageStatus

---

Indicates the status of a [TextChatMessage](/docs/reference/engine/classes/TextChatMessage).

Items

| Name | Value | Summary |
| --- | --- | --- |
| Unknown | 1 | Generic failed status for any other [TextChannel:SendAsync()](/docs/reference/engine/classes/TextChannel#SendAsync) failures. |
| Success | 2 | Message has no issues. |
| Sending | 3 | Message is sending. |
| TextFilterFailed | 4 | Text filter failed to process the message. |
| Floodchecked | 5 | Message is from a user sending messages too frequently. |
| InvalidPrivacySettings | 6 | Message can't be sent because of the user's chat privacy settings. |
| InvalidTextChannelPermissions | 7 | Message's [TextSource](/docs/reference/engine/classes/TextSource) is either not in the intended [TextChannel](/docs/reference/engine/classes/TextChannel) or [TextSource.CanSend](/docs/reference/engine/classes/TextSource#CanSend) is false. |
| MessageTooLong | 8 | Message is too long. |
| ModerationTimeout | 9 |  |