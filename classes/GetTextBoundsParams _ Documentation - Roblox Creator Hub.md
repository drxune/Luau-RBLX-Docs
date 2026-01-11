# GetTextBoundsParams | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/GetTextBoundsParams
Scraped: 2026-01-11T02:41:37.255981Z

## Tags
- Not Replicated

## Inherits
- Instance
- GetTextBoundsParams
- TextService:GetTextBoundsAsync()
- Object
- TextLabel.FontFace
- TextLabel.TextSize
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [GetTextBoundsParams](/docs/reference/engine/classes/GetTextBoundsParams)

English

Feedback

Engine Class

GetTextBoundsParams

Use with [TextService:GetTextBoundsAsync()](/docs/reference/engine/classes/TextService#GetTextBoundsAsync) to measure the size of text.

Not Replicated

---

Summary

Properties

|  |
| --- |
| [Font](#Font):[Font](/docs/reference/engine/datatypes/Font) |
| [RichText](#RichText):[boolean](/docs/luau/booleans) |
| [Size](#Size):[number](/docs/luau/numbers) |
| [Text](#Text):[string](/docs/luau/strings) |
| [Width](#Width):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Pass this instance to [TextService:GetTextBoundsAsync()](/docs/reference/engine/classes/TextService#GetTextBoundsAsync) to measure the
size of text.

Code Samples

TextService: Measuring text size

This example shows how you can use [TextService:GetTextBoundsAsync()](/docs/reference/engine/classes/TextService#GetTextBoundsAsync).

It measures the size of some text in a specific font, then prints the result.

```
local TextService = game:GetService("TextService")



local params = Instance.new("GetTextBoundsParams")



params.Text = "hello world!"



params.Font = Font.new("rbxasset://fonts/families/GrenzeGotisch.json", Enum.FontWeight.Thin)



params.Size = 20



params.Width = 200



local size = TextService:GetTextBoundsAsync(params)



print("The size of the text is:", size)
```

---

API Reference

Properties

Font

Read Parallel

The [Font](/docs/reference/engine/datatypes/Font) of the text being measured.

GetTextBoundsParams.Font:[Font](/docs/reference/engine/datatypes/Font)

The [Font](/docs/reference/engine/datatypes/Font) of the text being measured. Corresponds to the
[TextLabel.FontFace](/docs/reference/engine/classes/TextLabel#FontFace) property on text objects.

Not to be confused with [Enum.Font](/docs/reference/engine/enums/Font). This is an object that you can create
using [Font.new()](/docs/reference/engine/datatypes/Font#new).

Provide feedback

---

RichText

Read Parallel

GetTextBoundsParams.RichText:[boolean](/docs/luau/booleans)

Provide feedback

---

Size

Read Parallel

The size of the text being measured.

GetTextBoundsParams.Size:[number](/docs/luau/numbers)

The size of the text that is being measured. Corresponds to the
[TextLabel.TextSize](/docs/reference/engine/classes/TextLabel#TextSize) property.

Provide feedback

---

Text

Read Parallel

The text being measured.

GetTextBoundsParams.Text:[string](/docs/luau/strings)

The text being measured.

Provide feedback

---

Width

Read Parallel

The width of the container for line breaking.

GetTextBoundsParams.Width:[number](/docs/luau/numbers)

The width of the container for line breaking. By default, the value is 0,
which means no line breaking will be performed. You can set it to the
width of the container that you'll be putting the text into.

Provide feedback

---