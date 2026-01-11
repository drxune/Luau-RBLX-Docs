# ChatWindowMessageProperties | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ChatWindowMessageProperties
Scraped: 2026-01-11T02:27:23.985180Z

## Tags
- Not Creatable

## Inherits
- TextChatMessageProperties
- ChatWindowMessageProperties
- Instance
- Object
- ChatWindowConfiguration:DeriveNewMessageProperties()
- ChatWindowConfiguration
- PrefixText
- TextChatMessage.PrefixText
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [TextChatMessageProperties](/docs/reference/engine/classes/TextChatMessageProperties)
6. /
7. [ChatWindowMessageProperties](/docs/reference/engine/classes/ChatWindowMessageProperties)

English

Feedback

Engine Class

ChatWindowMessageProperties

Not Creatable

---

Summary

Properties

|  |
| --- |
| [FontFace](#FontFace):[Font](/docs/reference/engine/datatypes/Font) |
| [PrefixTextProperties](#PrefixTextProperties):[ChatWindowMessageProperties](/docs/reference/engine/classes/ChatWindowMessageProperties) |
| [TextColor3](#TextColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [TextSize](#TextSize):[number](/docs/luau/numbers) |
| [TextStrokeColor3](#TextStrokeColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [TextStrokeTransparency](#TextStrokeTransparency):[number](/docs/luau/numbers) |

Inherited Members

3 inherited from [TextChatMessageProperties](/docs/reference/engine/classes/TextChatMessageProperties)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Can be used to customize the appearance of text chat messages sent to the
ChatWindow. Inherits from Class.TextChatMessageProperies. To create a new
ChatWindowMessageProperties instance, use
[ChatWindowConfiguration:DeriveNewMessageProperties()](/docs/reference/engine/classes/ChatWindowConfiguration#DeriveNewMessageProperties) which will have
the current properties from [ChatWindowConfiguration](/docs/reference/engine/classes/ChatWindowConfiguration).

```
local TextChatService = game:GetService("TextChatService")



local ChatWindowConfiguration = TextChatService:FindFirstChildOfClass("ChatWindowConfiguration")



TextChatService.OnChatWindowAdded = function(message: TextChatMessage)



-- Derive chat message properties



local properties = ChatWindowConfiguration:DeriveNewMessageProperties()



-- Change color of message within the chat window



properties.TextColor3 = Color3.fromRGB(255, 121, 121)



return properties



end
```

---

API Reference

Properties

FontFace

Read Parallel

Font used to render text in the chat window.

ChatWindowMessageProperties.FontFace:[Font](/docs/reference/engine/datatypes/Font)

Determines the font used to render text in the chat window. Default is
[Enum.Font.BuilderSansMedium](/docs/reference/engine/enums/Font#BuilderSansMedium).

Provide feedback

---

PrefixTextProperties

Read Parallel

Determines the properties of the
[PrefixText](/docs/reference/engine/classes/TextChatMessage#PrefixText) preceding the chat message.

ChatWindowMessageProperties.PrefixTextProperties:[ChatWindowMessageProperties](/docs/reference/engine/classes/ChatWindowMessageProperties)

Determines the properties of the [TextChatMessage.PrefixText](/docs/reference/engine/classes/TextChatMessage#PrefixText)
preceding the chat message.

Provide feedback

---

TextColor3

Read Parallel

Color of the text in the chat window.

ChatWindowMessageProperties.TextColor3:[Color3](/docs/reference/engine/datatypes/Color3)

Determines the color of the text in the chat window. Default value is
[Color3.fromRGB(255, 255, 255)](/docs/reference/engine/datatypes/Color3#fromRGB) (white).

Provide feedback

---

TextSize

Read Parallel

Size of the text in the chat window.

ChatWindowMessageProperties.TextSize:[number](/docs/luau/numbers)

Determines the size of the text in the chat window.

Provide feedback

---

TextStrokeColor3

Read Parallel

Stroke color applied to text in the chat window.

ChatWindowMessageProperties.TextStrokeColor3:[Color3](/docs/reference/engine/datatypes/Color3)

Determines the stroke color applied to text in the chat window. Default
value is [Color3.fromRGB(0, 0, 0)](/docs/reference/engine/datatypes/Color3#fromRGB) (black).

Provide feedback

---

TextStrokeTransparency

Read Parallel

Transparency of the stroke applied to text in the chat window.

ChatWindowMessageProperties.TextStrokeTransparency:[number](/docs/luau/numbers)

Determines the transparency of the stroke applied to text in the chat
window. Default value is 0.5.

Provide feedback

---