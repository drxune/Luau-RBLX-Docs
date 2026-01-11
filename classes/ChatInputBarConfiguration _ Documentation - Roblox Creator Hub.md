# ChatInputBarConfiguration | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ChatInputBarConfiguration
Scraped: 2026-01-11T02:31:47.130945Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- TextChatConfigurations
- ChatInputBarConfiguration
- TextChannel
- TextBox
- Instance
- Object
- TextChatService
- GuiBase2d.AbsolutePosition
- GuiBase2d.AbsoluteSize
- GuiService.PreferredTransparency
- ChatInputBarConfiguration.TargetTextChannel
- TextBox.Text
- ChatInputBarConfiguration.TextBox
- TextBox:CaptureFocus()
- TextBox:ReleaseFocus()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [TextChatConfigurations](/docs/reference/engine/classes/TextChatConfigurations)
6. /
7. [ChatInputBarConfiguration](/docs/reference/engine/classes/ChatInputBarConfiguration)

English

Feedback

Engine Class

![ChatInputBarConfiguration](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/ChatInputBarConfiguration-Dark.webp)ChatInputBarConfiguration

Configures properties of the default chat input bar.

Not Creatable

---

Summary

Properties

|  |
| --- |
| [AbsolutePosition](#AbsolutePosition):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [AbsoluteSize](#AbsoluteSize):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [AutocompleteEnabled](#AutocompleteEnabled):[boolean](/docs/luau/booleans) |
| [BackgroundColor3](#BackgroundColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [BackgroundTransparency](#BackgroundTransparency):[number](/docs/luau/numbers) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [FontFace](#FontFace):[Font](/docs/reference/engine/datatypes/Font) |
| [IsFocused](#IsFocused):[boolean](/docs/luau/booleans) |
| [KeyboardKeyCode](#KeyboardKeyCode):[Enum.KeyCode](/docs/reference/engine/enums/KeyCode) |
| [PlaceholderColor3](#PlaceholderColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [TargetTextChannel](#TargetTextChannel):[TextChannel](/docs/reference/engine/classes/TextChannel) |
| [TextBox](#TextBox):[TextBox](/docs/reference/engine/classes/TextBox) |
| [TextColor3](#TextColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [TextSize](#TextSize):[number](/docs/luau/numbers) |
| [TextStrokeColor3](#TextStrokeColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [TextStrokeTransparency](#TextStrokeTransparency):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Configures properties of the default text chat input bar. It is parented to
[TextChatService](/docs/reference/engine/classes/TextChatService).

---

API Reference

Properties

AbsolutePosition

Read Only

Not Replicated

Actual screen position of the default chat input bar in pixels.

ChatInputBarConfiguration.AbsolutePosition:[Vector2](/docs/reference/engine/datatypes/Vector2)

Read-only property that provides the screen position of the default chat
input bar in pixels. Behaves similarly to
[GuiBase2d.AbsolutePosition](/docs/reference/engine/classes/GuiBase2d#AbsolutePosition).

Provide feedback

---

AbsoluteSize

Read Only

Not Replicated

Actual screen size of the default chat input bar in pixels.

ChatInputBarConfiguration.AbsoluteSize:[Vector2](/docs/reference/engine/datatypes/Vector2)

Read-only property that provides the screen size of the default chat input
bar in pixels. Behaves similarly to [GuiBase2d.AbsoluteSize](/docs/reference/engine/classes/GuiBase2d#AbsoluteSize).

Provide feedback

---

AutocompleteEnabled

Read Parallel

Whether to enable autocomplete for the chat input bar.

ChatInputBarConfiguration.AutocompleteEnabled:[boolean](/docs/luau/booleans)

Whether to enable autocomplete for the chat input bar. Set to false to
disable autocomplete.

Provide feedback

---

BackgroundColor3

Read Parallel

Background color of the default chat input bar.

ChatInputBarConfiguration.BackgroundColor3:[Color3](/docs/reference/engine/datatypes/Color3)

Background color of the default chat input bar. Default value is
[Color3.new(25, 27, 29)](/docs/reference/engine/datatypes/Color3).

Provide feedback

---

BackgroundTransparency

Read Parallel

Background transparency of the default chat input bar.

ChatInputBarConfiguration.BackgroundTransparency:[number](/docs/luau/numbers)

Background transparency of the default chat input bar as a number between
0 and 1. This value is multiplied with the user's
[GuiService.PreferredTransparency](/docs/reference/engine/classes/GuiService#PreferredTransparency) to create the effective
background transparency used by the chat input bar, which may be more
opaque than this value set here. Default value is 0.2.

Provide feedback

---

Enabled

Read Parallel

Whether to show the default chat input bar.

ChatInputBarConfiguration.Enabled:[boolean](/docs/luau/booleans)

Whether to show the default chat input bar. Set to false to hide.

Provide feedback

---

FontFace

Read Parallel

Font used to render text in the default chat input bar.

ChatInputBarConfiguration.FontFace:[Font](/docs/reference/engine/datatypes/Font)

Font used to render text in the default chat input bar. Default is
[Enum.Font.BuilderSansMedium](/docs/reference/engine/enums/Font#BuilderSansMedium).

Provide feedback

---

IsFocused

Read Only

Not Replicated

Whether the default chat input bar is focused or not.

ChatInputBarConfiguration.IsFocused:[boolean](/docs/luau/booleans)

Indicates whether the default chat input bar is focused or not. Useful for
firing property changed events so you can implement callback functions
that respond to changes in the input bar's focus state.

Code Samples

Typing Indicator Bubble

The code below includes a simple way to create a typing indicator bubble above a user's avatar when the user is typing. Paste into a LocalScript.

```
local Players = game:GetService("Players")



local TextChatService = game:GetService("TextChatService")



local ChatInputBarConfiguration = TextChatService:FindFirstChildOfClass("ChatInputBarConfiguration")



local BubbleChatConfiguration = TextChatService:FindFirstChildOfClass("BubbleChatConfiguration")



local LocalPlayer = Players.LocalPlayer



local Character = LocalPlayer.Character or LocalPlayer.CharacterAdded:Wait()



-- Set up TextLabel



local textLabel = Instance.new("TextLabel")



textLabel.Size = UDim2.fromScale(1, 1)



textLabel.Text = ". . ."



textLabel.BackgroundColor3 = BubbleChatConfiguration.BackgroundColor3



textLabel.BorderColor3 = BubbleChatConfiguration.BackgroundColor3



textLabel.BackgroundTransparency = BubbleChatConfiguration.BackgroundTransparency



textLabel.TextColor3 = BubbleChatConfiguration.TextColor3



textLabel.FontFace = BubbleChatConfiguration.FontFace



textLabel.TextSize = BubbleChatConfiguration.TextSize



-- Parent a UICorner to the TextLabel to have rounded corners



local uiCorner = Instance.new("UICorner")



uiCorner.CornerRadius = UDim.new(0, 12)



uiCorner.Parent = textLabel



-- Set up Billboard



local typingIndicatorBillboard = Instance.new("BillboardGui")



typingIndicatorBillboard.Enabled = false



typingIndicatorBillboard.Size = UDim2.fromScale(1, 1)



typingIndicatorBillboard.StudsOffsetWorldSpace = Vector3.new(-0, 4, 0)



typingIndicatorBillboard.Adornee = Character



textLabel.Parent = typingIndicatorBillboard



typingIndicatorBillboard.Parent = LocalPlayer:FindFirstChildOfClass("PlayerGui")



ChatInputBarConfiguration:GetPropertyChangedSignal("IsFocused"):Connect(function()



-- Enable the typing indicator when the input bar is focused and disable otherwise



typingIndicatorBillboard.Enabled = ChatInputBarConfiguration.IsFocused



end)
```

Provide feedback

---

KeyboardKeyCode

Read Parallel

Additional key users can press to trigger focusing on the default chat
input bar.

ChatInputBarConfiguration.KeyboardKeyCode:[Enum.KeyCode](/docs/reference/engine/enums/KeyCode)

Additional key users can press to trigger focusing on the default chat
input bar. Useful when you want to have an extra hotkey for focusing in
addition to the / key.

Provide feedback

---

PlaceholderColor3

Read Parallel

Color of the text of the placeholder text in the default chat input bar.

ChatInputBarConfiguration.PlaceholderColor3:[Color3](/docs/reference/engine/datatypes/Color3)

Color of the text of the placeholder text in the default chat input bar.
Default value is [Color3.new(178, 178, 178)](/docs/reference/engine/datatypes/Color3).

Provide feedback

---

TargetTextChannel

Read Parallel

A reference to the target [TextChannel](/docs/reference/engine/classes/TextChannel).

ChatInputBarConfiguration.TargetTextChannel:[TextChannel](/docs/reference/engine/classes/TextChannel)

Determines which [TextChannel](/docs/reference/engine/classes/TextChannel) to use when the user sends a message
with the default chat input bar.

Provide feedback

---

TextBox

Read Parallel

Reference to a designated [TextBox](/docs/reference/engine/classes/TextBox) instance that sends messages on
behalf of the user.

ChatInputBarConfiguration.TextBox:[TextBox](/docs/reference/engine/classes/TextBox)

Reference to a designated [TextBox](/docs/reference/engine/classes/TextBox) instance that sends messages on
behalf of the user. You can use it to further integrate your custom chat
input bar UI into your experience by freely manipulating appearance,
location, and layout. When opting to set this property to a custom
[TextBox](/docs/reference/engine/classes/TextBox), you don't need to write any code for the following
behavior:

* When a user types a message and presses [Enum.KeyCode.Return](/docs/reference/engine/enums/KeyCode#Return), the
  message will be sent to
  [ChatInputBarConfiguration.TargetTextChannel](/docs/reference/engine/classes/ChatInputBarConfiguration#TargetTextChannel).
* When a message is sent, [TextBox.Text](/docs/reference/engine/classes/TextBox#Text) will automatically clear.

For security, some limitations are imposed on the [TextBox](/docs/reference/engine/classes/TextBox) when it
is promoted to [ChatInputBarConfiguration.TextBox](/docs/reference/engine/classes/ChatInputBarConfiguration#TextBox). Luau code will
not be able to:

* Change the [TextBox.Text](/docs/reference/engine/classes/TextBox#Text) property.
* Use the [TextBox:CaptureFocus()](/docs/reference/engine/classes/TextBox#CaptureFocus) or [TextBox:ReleaseFocus()](/docs/reference/engine/classes/TextBox#ReleaseFocus)
  methods.

Provide feedback

---

TextColor3

Read Parallel

Color of the text in default chat input bar.

ChatInputBarConfiguration.TextColor3:[Color3](/docs/reference/engine/datatypes/Color3)

Color of the text in default chat input bar. Default value is
[Color3.new(255, 255, 255)](/docs/reference/engine/datatypes/Color3).

Provide feedback

---

TextSize

Read Parallel

Size of the text in default chat input bar.

ChatInputBarConfiguration.TextSize:[number](/docs/luau/numbers)

Size of the text in default chat input bar. Default value is 14.

Provide feedback

---

TextStrokeColor3

Read Parallel

Color of the text stroke for text in default chat input bar.

ChatInputBarConfiguration.TextStrokeColor3:[Color3](/docs/reference/engine/datatypes/Color3)

Color of the text stroke for text in default chat input bar. Default value
is [Color3.new(0, 0, 0)](/docs/reference/engine/datatypes/Color3).

Provide feedback

---

TextStrokeTransparency

Read Parallel

Transparency of the text stroke for text in default chat input bar.

ChatInputBarConfiguration.TextStrokeTransparency:[number](/docs/luau/numbers)

Transparency of the text stroke for text in default chat input bar.
Default value is 0.5.

Provide feedback

---