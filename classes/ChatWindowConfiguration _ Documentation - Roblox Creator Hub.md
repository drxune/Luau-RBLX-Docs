# ChatWindowConfiguration | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ChatWindowConfiguration
Scraped: 2026-01-11T02:40:13.240953Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- TextChatConfigurations
- ChatWindowConfiguration
- ChatWindowMessageProperties
- Instance
- Object
- TextChatService
- GuiBase2d.AbsolutePosition
- GuiBase2d.AbsoluteSize
- GuiService.PreferredTransparency
- UIGridStyleLayout.HorizontalAlignment
- UIGridStyleLayout.VerticalAlignment
- TextChatMessageProperties
- TextChatService.OnChatWindowAdded
- TextChannel
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [TextChatConfigurations](/docs/reference/engine/classes/TextChatConfigurations)
6. /
7. [ChatWindowConfiguration](/docs/reference/engine/classes/ChatWindowConfiguration)

English

Feedback

Engine Class

![ChatWindowConfiguration](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/ChatWindowConfiguration-Dark.webp)ChatWindowConfiguration

Configures properties of the default chat window.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [AbsolutePosition](#AbsolutePosition):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [AbsoluteSize](#AbsoluteSize):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [BackgroundColor3](#BackgroundColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [BackgroundTransparency](#BackgroundTransparency):[number](/docs/luau/numbers) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [FontFace](#FontFace):[Font](/docs/reference/engine/datatypes/Font) |
| [HeightScale](#HeightScale):[number](/docs/luau/numbers) |
| [HorizontalAlignment](#HorizontalAlignment):[Enum.HorizontalAlignment](/docs/reference/engine/enums/HorizontalAlignment) |
| [TextColor3](#TextColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [TextSize](#TextSize):[number](/docs/luau/numbers) |
| [TextStrokeColor3](#TextStrokeColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [TextStrokeTransparency](#TextStrokeTransparency):[number](/docs/luau/numbers) |
| [VerticalAlignment](#VerticalAlignment):[Enum.VerticalAlignment](/docs/reference/engine/enums/VerticalAlignment) |
| [WidthScale](#WidthScale):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [DeriveNewMessageProperties](#DeriveNewMessageProperties)():[ChatWindowMessageProperties](/docs/reference/engine/classes/ChatWindowMessageProperties) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Configures properties of the default text chat window. It is parented to
[TextChatService](/docs/reference/engine/classes/TextChatService).

---

API Reference

Properties

AbsolutePosition

Read Only

Not Replicated

Actual screen position of the default chat window, in pixels.

ChatWindowConfiguration.AbsolutePosition:[Vector2](/docs/reference/engine/datatypes/Vector2)

Read-only property that provides the screen position of the default chat
window in pixels. Behaves similarly to [GuiBase2d.AbsolutePosition](/docs/reference/engine/classes/GuiBase2d#AbsolutePosition).

Provide feedback

---

AbsoluteSize

Read Only

Not Replicated

Actual screen size of the default chat window, in pixels.

ChatWindowConfiguration.AbsoluteSize:[Vector2](/docs/reference/engine/datatypes/Vector2)

Read-only property that provides the screen size of the default chat
window in pixels. Behaves similarly to [GuiBase2d.AbsoluteSize](/docs/reference/engine/classes/GuiBase2d#AbsoluteSize).

Provide feedback

---

BackgroundColor3

Read Parallel

Background color of the default chat window.

ChatWindowConfiguration.BackgroundColor3:[Color3](/docs/reference/engine/datatypes/Color3)

Background color of the default chat window. If the background color is
not overridden, this value will respect the user's
[GuiService.PreferredTransparency](/docs/reference/engine/classes/GuiService#PreferredTransparency) by making the menu more gray as
the transparency of the menu decreases. Default value is
[Color3.new(25, 27, 29)](/docs/reference/engine/datatypes/Color3).

Provide feedback

---

BackgroundTransparency

Read Parallel

Background transparency of the default chat window.

ChatWindowConfiguration.BackgroundTransparency:[number](/docs/luau/numbers)

Background transparency of the default chat window as a number between 0
and 1. This value is multiplied with the user's
[GuiService.PreferredTransparency](/docs/reference/engine/classes/GuiService#PreferredTransparency) to create the effective
background transparency used by the chat window, which may be more opaque
than this value set here. Default value is 0.3.

Provide feedback

---

Enabled

Read Parallel

Whether to show the default chat window.

ChatWindowConfiguration.Enabled:[boolean](/docs/luau/booleans)

Whether to show the default chat window. Set to false to hide.

Provide feedback

---

FontFace

Read Parallel

Font used to render text in the default chat window.

ChatWindowConfiguration.FontFace:[Font](/docs/reference/engine/datatypes/Font)

Font used to render text in the default chat window. Default is
[Enum.Font.BuilderSansMedium](/docs/reference/engine/enums/Font#BuilderSansMedium).

Provide feedback

---

HeightScale

Read Parallel

Factor by which the height of the default chat window should be scaled.

ChatWindowConfiguration.HeightScale:[number](/docs/luau/numbers)

Factor by which the height of the default chat window should be scaled.
Must be a value between 0.5 and 2. Defining a value outside of range
clamps the actual value to the closest bound.

Provide feedback

---

HorizontalAlignment

Horizontal alignment of the chat window.

ChatWindowConfiguration.HorizontalAlignment:[Enum.HorizontalAlignment](/docs/reference/engine/enums/HorizontalAlignment)

Horizontal alignment of the chat window. Behaves similarly to
[UIGridStyleLayout.HorizontalAlignment](/docs/reference/engine/classes/UIGridStyleLayout#HorizontalAlignment). Setting to
[Left](/docs/reference/engine/enums/HorizontalAlignment) or [Right](/docs/reference/engine/enums/HorizontalAlignment) adding
a small padding away from touching the corresponding horizontal edge of
the screen. Setting to [Center](/docs/reference/engine/enums/HorizontalAlignment) aligns the window
in the horizontal middle of the screen. Default value is
[Left](/docs/reference/engine/enums/HorizontalAlignment).

Provide feedback

---

TextColor3

Read Parallel

Color of the text in default chat window.

ChatWindowConfiguration.TextColor3:[Color3](/docs/reference/engine/datatypes/Color3)

Color of the text in default chat window. Default value is
[Color3.new(255, 255, 255)](/docs/reference/engine/datatypes/Color3).

Provide feedback

---

TextSize

Read Parallel

Size of the text in default chat window.

ChatWindowConfiguration.TextSize:[number](/docs/luau/numbers)

Size of the text in default chat window. Default value is 14.

Provide feedback

---

TextStrokeColor3

Read Parallel

Color of the text stroke for text in default chat window.

ChatWindowConfiguration.TextStrokeColor3:[Color3](/docs/reference/engine/datatypes/Color3)

Color of the text stroke for text in default chat window. Default value is
[Color3.new(0, 0, 0)](/docs/reference/engine/datatypes/Color3).

Provide feedback

---

TextStrokeTransparency

Read Parallel

Transparency of the text stroke for text in default chat window.

ChatWindowConfiguration.TextStrokeTransparency:[number](/docs/luau/numbers)

Transparency of the text stroke for text in default chat window. Default
value is 0.5.

Provide feedback

---

VerticalAlignment

Vertical alignment of the chat window.

ChatWindowConfiguration.VerticalAlignment:[Enum.VerticalAlignment](/docs/reference/engine/enums/VerticalAlignment)

Vertical alignment of the chat window. Behaves similarly to
[UIGridStyleLayout.VerticalAlignment](/docs/reference/engine/classes/UIGridStyleLayout#VerticalAlignment). Setting to
[Top](/docs/reference/engine/enums/VerticalAlignment) or [Bottom](/docs/reference/engine/enums/VerticalAlignment) adds a
small padding away from touching the corresponding edge of the screen.
Setting to [Center](/docs/reference/engine/enums/VerticalAlignment) aligns the window in the
vertical middle of the screen. Default value is
[Top](/docs/reference/engine/enums/VerticalAlignment).

Provide feedback

---

WidthScale

Read Parallel

Factor by which the width of the default chat window should be scaled.

ChatWindowConfiguration.WidthScale:[number](/docs/luau/numbers)

Factor by which the width of the default chat window should be scaled.
Must be a value between 0.5 and 2. Defining a value outside of range
clamps the actual value to the closest bound.

Provide feedback

---

Methods

DeriveNewMessageProperties

Creates a new [ChatWindowMessageProperties](/docs/reference/engine/classes/ChatWindowMessageProperties) instance that can be
used to customize the appearance of messages in the chat window.

ChatWindowConfiguration:DeriveNewMessageProperties():[ChatWindowMessageProperties](/docs/reference/engine/classes/ChatWindowMessageProperties)

Returns

[ChatWindowMessageProperties](/docs/reference/engine/classes/ChatWindowMessageProperties)

Creates a new [ChatWindowMessageProperties](/docs/reference/engine/classes/ChatWindowMessageProperties) instance that can be
used to customize the appearance of messages in the chat window.
[ChatWindowMessageProperties](/docs/reference/engine/classes/ChatWindowMessageProperties) inherits from
[TextChatMessageProperties](/docs/reference/engine/classes/TextChatMessageProperties).

This is intended to be used during custom
[TextChatService.OnChatWindowAdded](/docs/reference/engine/classes/TextChatService#OnChatWindowAdded) callbacks.

```
local TextChatService = game:GetService("TextChatService")



local ChatWindowConfiguration = TextChatService.ChatWindowConfiguration



TextChatService.OnChatWindowAdded = function(textChatMessage)



local properties = ChatWindowConfiguration:DeriveNewMessageProperties()



if textChatMessage.Metadata == "Important" then



properties.TextColor3 = Color3.fromRGB(255, 0, 0)



end



return properties



end
```

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