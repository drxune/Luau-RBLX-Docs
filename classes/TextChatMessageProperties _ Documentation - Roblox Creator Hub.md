# TextChatMessageProperties | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TextChatMessageProperties
Scraped: 2026-01-11T02:40:54.987456Z

## Inherits
- Instance
- TextChatMessageProperties
- TextChatMessage
- TextChatService.OnIncomingMessage
- TextChannel.OnIncomingMessage
- Object
- BubbleChatMessageProperties
- ChatWindowMessageProperties
- TextChatService
- TextChatMessage.PrefixText
- TextChatMessage.Text
- TextChatMessage.Translation
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [TextChatMessageProperties](/docs/reference/engine/classes/TextChatMessageProperties)

English

Feedback

Engine Class

TextChatMessageProperties

Overrides [TextChatMessage](/docs/reference/engine/classes/TextChatMessage) properties when returned by callbacks
defined in [TextChatService.OnIncomingMessage](/docs/reference/engine/classes/TextChatService#OnIncomingMessage) or
[TextChannel.OnIncomingMessage](/docs/reference/engine/classes/TextChannel#OnIncomingMessage).

---

Summary

Properties

|  |
| --- |
| [PrefixText](#PrefixText):[string](/docs/luau/strings) |
| [Text](#Text):[string](/docs/luau/strings) |
| [Translation](#Translation):[string](/docs/luau/strings) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[BubbleChatMessageProperties](/docs/reference/engine/classes/BubbleChatMessageProperties), [ChatWindowMessageProperties](/docs/reference/engine/classes/ChatWindowMessageProperties)

Overrides [TextChatMessage](/docs/reference/engine/classes/TextChatMessage) properties like
[ChatWindowMessageProperties](/docs/reference/engine/classes/TextChatMessage#ChatWindowMessageProperties)
and
[BubbleChatMessageProperties](/docs/reference/engine/classes/TextChatMessage#BubbleChatMessageProperties)
when returned by callbacks defined in
[TextChatService.OnIncomingMessage](/docs/reference/engine/classes/TextChatService#OnIncomingMessage) or
[TextChannel.OnIncomingMessage](/docs/reference/engine/classes/TextChannel#OnIncomingMessage). These properties are useful for
customizing the appearance of a message with
[rich text](/docs/ui/rich-text) tags.

For sample code, see
[Assign chat tags](/docs/chat/examples/group-chat-tags).

If you return empty strings for any of these properties,
[TextChatService](/docs/reference/engine/classes/TextChatService) ignores them and doesn't override the original
values.

---

API Reference

Properties

PrefixText

Read Parallel

The [TextChatMessage.PrefixText](/docs/reference/engine/classes/TextChatMessage#PrefixText) to override.

TextChatMessageProperties.PrefixText:[string](/docs/luau/strings)

The [TextChatMessage.PrefixText](/docs/reference/engine/classes/TextChatMessage#PrefixText) to override.

Provide feedback

---

Text

Read Parallel

The [TextChatMessage.Text](/docs/reference/engine/classes/TextChatMessage#Text) to override.

TextChatMessageProperties.Text:[string](/docs/luau/strings)

The [TextChatMessage.Text](/docs/reference/engine/classes/TextChatMessage#Text) to override.

Provide feedback

---

Translation

Read Parallel

The [TextChatMessage.Translation](/docs/reference/engine/classes/TextChatMessage#Translation) to override.

TextChatMessageProperties.Translation:[string](/docs/luau/strings)

The [TextChatMessage.Translation](/docs/reference/engine/classes/TextChatMessage#Translation) to override; represents
[automatically translated](/docs/production/localization/automatic-translations)
and filtered text messages based on players' localization settings.

Provide feedback

---