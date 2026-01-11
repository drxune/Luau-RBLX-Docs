# BubbleChatConfiguration | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BubbleChatConfiguration
Scraped: 2026-01-11T02:38:37.205488Z

## Tags
- Not Creatable

## Inherits
- TextChatConfigurations
- BubbleChatConfiguration
- TextChatService
- Instance
- Object
- Attachment
- GuiService.PreferredTransparency
- BubbleChatConfiguration.Font
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [TextChatConfigurations](/docs/reference/engine/classes/TextChatConfigurations)
6. /
7. [BubbleChatConfiguration](/docs/reference/engine/classes/BubbleChatConfiguration)

English

Feedback

Engine Class

![BubbleChatConfiguration](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/BubbleChatConfiguration-Dark.webp)BubbleChatConfiguration

Allows for customization of text chat bubbles through [TextChatService](/docs/reference/engine/classes/TextChatService).

Not Creatable

---

Summary

Properties

|  |
| --- |
| [AdorneeName](#AdorneeName):[string](/docs/luau/strings) |
| [BackgroundColor3](#BackgroundColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [BackgroundTransparency](#BackgroundTransparency):[number](/docs/luau/numbers) |
| [BubbleDuration](#BubbleDuration):[number](/docs/luau/numbers) |
| [BubblesSpacing](#BubblesSpacing):[number](/docs/luau/numbers) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |
| [Font](#Font):[Enum.Font](/docs/reference/engine/enums/Font) |
| [FontFace](#FontFace):[Font](/docs/reference/engine/datatypes/Font) |
| [LocalPlayerStudsOffset](#LocalPlayerStudsOffset):[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [MaxBubbles](#MaxBubbles):[number](/docs/luau/numbers) |
| [MaxDistance](#MaxDistance):[number](/docs/luau/numbers) |
| [MinimizeDistance](#MinimizeDistance):[number](/docs/luau/numbers) |
| [TailVisible](#TailVisible):[boolean](/docs/luau/booleans) |
| [TextColor3](#TextColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [TextSize](#TextSize):[number](/docs/luau/numbers) |
| [VerticalStudsOffset](#VerticalStudsOffset):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Allows for customization of text chat bubbles through [TextChatService](/docs/reference/engine/classes/TextChatService).
See [Bubble Chat](/docs/chat/bubble-chat) for implementation details.

---

API Reference

Properties

AdorneeName

Read Parallel

Body part or [Attachment](/docs/reference/engine/classes/Attachment) that bubbles will attach to.

BubbleChatConfiguration.AdorneeName:[string](/docs/luau/strings)

String name of the body part or [Attachment](/docs/reference/engine/classes/Attachment) that bubbles attach to;
if multiple instances of the same name exist, the system attaches to the
first instance found. Default is "HumanoidRootPart".

Provide feedback

---

BackgroundColor3

Read Parallel

Background color of bubbles.

BubbleChatConfiguration.BackgroundColor3:[Color3](/docs/reference/engine/datatypes/Color3)

[Color3](/docs/reference/engine/datatypes/Color3) background color of bubbles. Default is
[Color3.fromRGB(250, 250, 250)](/docs/reference/engine/datatypes/Color3).

Provide feedback

---

BackgroundTransparency

Read Parallel

Determines the background transparency of the default bubble chat as a
number between 0 and 1.

BubbleChatConfiguration.BackgroundTransparency:[number](/docs/luau/numbers)

Determines the background transparency of the default bubble chat as a
number between 0 and 1. This value is multiplied with the user's
[GuiService.PreferredTransparency](/docs/reference/engine/classes/GuiService#PreferredTransparency) to create the effective
background transparency used by the bubble chat, which may be more opaque
than this value set here. Default value is 0.1.

Provide feedback

---

BubbleDuration

Read Parallel

Time before a bubble fades out, in seconds.

BubbleChatConfiguration.BubbleDuration:[number](/docs/luau/numbers)

Time before a bubble fades out, in seconds. Default is 30.

Provide feedback

---

BubblesSpacing

Read Parallel

Vertical space between stacked bubbles, in pixels.

BubbleChatConfiguration.BubblesSpacing:[number](/docs/luau/numbers)

Vertical space between stacked bubbles, in pixels. Default is 6.

Provide feedback

---

Enabled

Read Parallel

Whether text chat bubbles are enabled.

BubbleChatConfiguration.Enabled:[boolean](/docs/luau/booleans)

Whether text chat bubbles are enabled. Default is false.

Provide feedback

---

Font

Hidden

Read Parallel

[Font](/docs/reference/engine/datatypes/Font) of the bubble text.

BubbleChatConfiguration.Font:[Enum.Font](/docs/reference/engine/enums/Font)

[Font](/docs/reference/engine/datatypes/Font) of the bubble text. Default is [Enum.Font.GothamMedium](/docs/reference/engine/enums/Font#GothamMedium).

Provide feedback

---

FontFace

Read Parallel

[Font](/docs/reference/engine/datatypes/Font) of the bubble text.

BubbleChatConfiguration.FontFace:[Font](/docs/reference/engine/datatypes/Font)

[Font](/docs/reference/engine/datatypes/Font) of the bubble text. Similar to
[BubbleChatConfiguration.Font](/docs/reference/engine/classes/BubbleChatConfiguration#Font) but allows setting fonts that don't
exist in [Enum.Font](/docs/reference/engine/enums/Font).

Provide feedback

---

LocalPlayerStudsOffset

Read Parallel

Offset of bubbles from their adornee, in studs.

BubbleChatConfiguration.LocalPlayerStudsOffset:[Vector3](/docs/reference/engine/datatypes/Vector3)

If adorned to the local player, [Vector3](/docs/reference/engine/datatypes/Vector3) offset of bubbles from
their adornee, in studs, relative to the camera orientation.

Provide feedback

---

MaxBubbles

Read Parallel

Maximum number of text chat bubbles shown per user.

BubbleChatConfiguration.MaxBubbles:[number](/docs/luau/numbers)

Maximum number of text chat bubbles shown per user. If the number of
bubbles exceeds this maximum, the system removes bubbles from the oldest
one. Default is 3.

Provide feedback

---

MaxDistance

Read Parallel

Maximum distance from the camera that bubbles are shown.

BubbleChatConfiguration.MaxDistance:[number](/docs/luau/numbers)

Maximum distance from the camera that bubbles are shown. Default is 100.

Provide feedback

---

MinimizeDistance

Read Parallel

Distance from the camera when bubbles turn into a single bubble with an
ellipsis to indicate chatter.

BubbleChatConfiguration.MinimizeDistance:[number](/docs/luau/numbers)

Distance from the camera when bubbles turn into a single bubble with an
ellipsis (⋯) to indicate chatter.

Provide feedback

---

TailVisible

Read Parallel

Determines if the tail at the bottom of the text chat bubbles is visible.

BubbleChatConfiguration.TailVisible:[boolean](/docs/luau/booleans)

Determines if the tail at the bottom of the text chat bubbles is visible.
Default is True.

Provide feedback

---

TextColor3

Read Parallel

Color of bubble text.

BubbleChatConfiguration.TextColor3:[Color3](/docs/reference/engine/datatypes/Color3)

[Color3](/docs/reference/engine/datatypes/Color3) color of bubble text. Default is
[Color3.fromRGB(57, 59, 61)](/docs/reference/engine/datatypes/Color3).

Provide feedback

---

TextSize

Read Parallel

Size of bubble text.

BubbleChatConfiguration.TextSize:[number](/docs/luau/numbers)

Size of bubble text. Default is 16.

Provide feedback

---

VerticalStudsOffset

Read Parallel

Extra space between bubbles and their adornee, in studs.

BubbleChatConfiguration.VerticalStudsOffset:[number](/docs/luau/numbers)

Extra space between bubbles and their adornee, in studs. Default is 0.

Provide feedback

---