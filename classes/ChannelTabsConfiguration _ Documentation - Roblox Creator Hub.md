# ChannelTabsConfiguration | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ChannelTabsConfiguration
Scraped: 2026-01-11T02:40:49.268937Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- TextChatConfigurations
- ChannelTabsConfiguration
- Instance
- Object
- TextChatService
- GuiBase2d.AbsolutePosition
- GuiBase2d.AbsoluteSize
- GuiService.PreferredTransparency
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [TextChatConfigurations](/docs/reference/engine/classes/TextChatConfigurations)
6. /
7. [ChannelTabsConfiguration](/docs/reference/engine/classes/ChannelTabsConfiguration)

English

Feedback

Engine Class

![ChannelTabsConfiguration](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/ChannelTabsConfiguration-Dark.webp)ChannelTabsConfiguration

Configures properties of the optional channel tabs in the default chat window.

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
| [HoverBackgroundColor3](#HoverBackgroundColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [SelectedTabTextColor3](#SelectedTabTextColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [TextColor3](#TextColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [TextSize](#TextSize):[number](/docs/luau/numbers) |
| [TextStrokeColor3](#TextStrokeColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [TextStrokeTransparency](#TextStrokeTransparency):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Configures properties of the optional channel tabs in the default chat window.
It is parented to [TextChatService](/docs/reference/engine/classes/TextChatService).

To learn more, see
[Customizing the Chat Window](/docs/chat/chat-window).

---

API Reference

Properties

AbsolutePosition

Read Only

Not Replicated

Read Parallel

Actual screen position of the channel tab bar, in pixels.

ChannelTabsConfiguration.AbsolutePosition:[Vector2](/docs/reference/engine/datatypes/Vector2)

Read-only property that provides the screen position of the channel tab
bar in pixels. Behaves similarly to [GuiBase2d.AbsolutePosition](/docs/reference/engine/classes/GuiBase2d#AbsolutePosition).

Provide feedback

---

AbsoluteSize

Read Only

Not Replicated

Read Parallel

Actual screen size of the channel tab bar, in pixels.

ChannelTabsConfiguration.AbsoluteSize:[Vector2](/docs/reference/engine/datatypes/Vector2)

Read-only property that provides the screen size of the channel tab bar in
pixels. Behaves similarly to [GuiBase2d.AbsoluteSize](/docs/reference/engine/classes/GuiBase2d#AbsoluteSize).

Provide feedback

---

BackgroundColor3

Read Parallel

Background color of the channel tabs.

ChannelTabsConfiguration.BackgroundColor3:[Color3](/docs/reference/engine/datatypes/Color3)

Background color of the channel tabs. If the background color is not
overridden, this value will respect the user's
[GuiService.PreferredTransparency](/docs/reference/engine/classes/GuiService#PreferredTransparency) by making the menu more gray as
the transparency of the menu decreases. Default value is
[Color3.new(25, 27, 29)](/docs/reference/engine/datatypes/Color3).

Provide feedback

---

BackgroundTransparency

Read Parallel

Background transparency of the channel tabs.

ChannelTabsConfiguration.BackgroundTransparency:[number](/docs/luau/numbers)

Background transparency of the channel tabs as a number between 0 and
1. This value is multiplied with the user's
[GuiService.PreferredTransparency](/docs/reference/engine/classes/GuiService#PreferredTransparency) to create the effective
background transparency used by the channel tabs, which may be more opaque
than this value set here. Default value is 0.

Provide feedback

---

Enabled

Read Parallel

Whether to show the channel tabs.

ChannelTabsConfiguration.Enabled:[boolean](/docs/luau/booleans)

Whether to show the channel tabs. Set to false to hide.

Provide feedback

---

FontFace

Read Parallel

Font used to render text in the channel tabs.

ChannelTabsConfiguration.FontFace:[Font](/docs/reference/engine/datatypes/Font)

Font used to render text in the channel tabs. Default is
[Enum.Font.BuilderSansBold](/docs/reference/engine/enums/Font#BuilderSansBold).

Provide feedback

---

HoverBackgroundColor3

Read Parallel

Background color of a channel tab when hovering over it.

ChannelTabsConfiguration.HoverBackgroundColor3:[Color3](/docs/reference/engine/datatypes/Color3)

Background color of a channel tab when hovering over it. Default value is
[Color3.new(125, 125, 125)](/docs/reference/engine/datatypes/Color3).

Provide feedback

---

SelectedTabTextColor3

Read Parallel

Color of text in a selected tab.

ChannelTabsConfiguration.SelectedTabTextColor3:[Color3](/docs/reference/engine/datatypes/Color3)

Color of text in a selected tab. Default value is
[Color3.new(255, 255, 255)](/docs/reference/engine/datatypes/Color3).

Provide feedback

---

TextColor3

Read Parallel

Color of text in an unselected tab.

ChannelTabsConfiguration.TextColor3:[Color3](/docs/reference/engine/datatypes/Color3)

Color of text in an unselected tab. Default value is
[Color3.new(175, 175, 175)](/docs/reference/engine/datatypes/Color3).

Provide feedback

---

TextSize

Read Parallel

Size of the text in channel tabs.

ChannelTabsConfiguration.TextSize:[number](/docs/luau/numbers)

Size of the text in channel tabs. Default value is 14.

Provide feedback

---

TextStrokeColor3

Read Parallel

Color of the text stroke for text in channel tabs.

ChannelTabsConfiguration.TextStrokeColor3:[Color3](/docs/reference/engine/datatypes/Color3)

Color of the text stroke for text in channel tabs. Default value is
[Color3.new(0, 0, 0)](/docs/reference/engine/datatypes/Color3).

Provide feedback

---

TextStrokeTransparency

Read Parallel

Transparency of the text stroke for text in channel tabs.

ChannelTabsConfiguration.TextStrokeTransparency:[number](/docs/luau/numbers)

Transparency of the text stroke for text in channel tabs. Default value is
1.

Provide feedback

---