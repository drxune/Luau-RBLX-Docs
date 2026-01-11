# TextLabel | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TextLabel
Scraped: 2026-01-11T02:38:52.562578Z

## Tags
- Not Replicated

## Inherits
- GuiLabel
- TextLabel
- GuiObject
- GuiBase2d
- Instance
- Object
- Frame
- TextScaled
- TextWrapped
- TextXAlignment
- TextYAlignment
- Font
- TextColor3
- BackgroundTransparency
- UITextSizeConstraint
- TextLabel.Text
- Text
- RichText
- ContentText
- TextSize
- FontFace
- GuiBase2d.Localize
- TextTransparency
- Script
- LocalScript
- TextService:GetTextSize()
- TextBounds
- BillboardGuis
- AutomaticSize
- TextStrokeTransparency
- UIStroke
- TextStrokeColor3
- GuiBase2d.AbsoluteSize
- TextFits
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [GuiLabel](/docs/reference/engine/classes/GuiLabel)
6. /
7. [TextLabel](/docs/reference/engine/classes/TextLabel)

English

Feedback

Engine Class

![TextLabel](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/TextLabel-Dark.webp)TextLabel

A 2D user interface element that displays non-interactive text.

---

Summary

Properties

|  |
| --- |
| [ContentText](#ContentText):[string](/docs/luau/strings) |
| [Font](#Font):[Enum.Font](/docs/reference/engine/enums/Font) |
| [FontFace](#FontFace):[Font](/docs/reference/engine/datatypes/Font) |
| [FontSize](#FontSize):[Enum.FontSize](/docs/reference/engine/enums/FontSize)  Deprecated |
| [LineHeight](#LineHeight):[number](/docs/luau/numbers) |
| [LocalizedText](#LocalizedText):[string](/docs/luau/strings) |
| [MaxVisibleGraphemes](#MaxVisibleGraphemes):[number](/docs/luau/numbers) |
| [OpenTypeFeatures](#OpenTypeFeatures):[string](/docs/luau/strings) |
| [OpenTypeFeaturesError](#OpenTypeFeaturesError):[string](/docs/luau/strings) |
| [RichText](#RichText):[boolean](/docs/luau/booleans) |
| [Text](#Text):[string](/docs/luau/strings) |
| [TextBounds](#TextBounds):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [TextColor](#TextColor):[BrickColor](/docs/reference/engine/datatypes/BrickColor)  Deprecated |
| [TextColor3](#TextColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [TextDirection](#TextDirection):[Enum.TextDirection](/docs/reference/engine/enums/TextDirection) |
| [TextFits](#TextFits):[boolean](/docs/luau/booleans) |
| [TextScaled](#TextScaled):[boolean](/docs/luau/booleans) |
| [TextSize](#TextSize):[number](/docs/luau/numbers) |
| [TextStrokeColor3](#TextStrokeColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [TextStrokeTransparency](#TextStrokeTransparency):[number](/docs/luau/numbers) |
| [TextTransparency](#TextTransparency):[number](/docs/luau/numbers) |
| [TextTruncate](#TextTruncate):[Enum.TextTruncate](/docs/reference/engine/enums/TextTruncate) |
| [TextWrap](#TextWrap):[boolean](/docs/luau/booleans)  Deprecated |
| [TextWrapped](#TextWrapped):[boolean](/docs/luau/booleans) |
| [TextXAlignment](#TextXAlignment):[Enum.TextXAlignment](/docs/reference/engine/enums/TextXAlignment) |
| [TextYAlignment](#TextYAlignment):[Enum.TextYAlignment](/docs/reference/engine/enums/TextYAlignment) |

Inherited Members

50 inherited from [GuiObject](/docs/reference/engine/classes/GuiObject)

12 inherited from [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A [TextLabel](/docs/reference/engine/classes/TextLabel) renders a rectangle, like a [Frame](/docs/reference/engine/classes/Frame), with styled
text. The rectangle can be used to define text boundaries, text scaling
([TextScaled](/docs/reference/engine/classes/TextLabel#TextScaled)), wrapping
([TextWrapped](/docs/reference/engine/classes/TextLabel#TextWrapped)), and alignment
([TextXAlignment](/docs/reference/engine/classes/TextLabel#TextXAlignment) and/or
[TextYAlignment](/docs/reference/engine/classes/TextLabel#TextYAlignment)).

This class contains properties that control the display of the text, such as
[Font](/docs/reference/engine/classes/TextLabel#Font) and [TextColor3](/docs/reference/engine/classes/TextLabel#TextColor3). To
display only text and hide the background rectangle, set
[BackgroundTransparency](/docs/reference/engine/classes/TextLabel#BackgroundTransparency) to 1.

A [UITextSizeConstraint](/docs/reference/engine/classes/UITextSizeConstraint) object can be used to constrain the size of
text with [TextScaled](/docs/reference/engine/classes/TextLabel#TextScaled) enabled. It is recommended
that the size of text is no lower than 9, otherwise it may not be visible to
many users.

---

API Reference

Properties

ContentText

Read Only

Not Replicated

Read Parallel

A copy of [TextLabel.Text](/docs/reference/engine/classes/TextLabel#Text) that contains exactly what is being
rendered by the [TextLabel](/docs/reference/engine/classes/TextLabel).

TextLabel.ContentText:[string](/docs/luau/strings)

This property provides a copy of [Text](/docs/reference/engine/classes/TextLabel#Text) that contains
exactly what is being rendered by the [TextLabel](/docs/reference/engine/classes/TextLabel). This is useful
for eliminating style tags used for [rich text](/docs/ui/rich-text)
markup; for example, when [RichText](/docs/reference/engine/classes/TextLabel#RichText) is enabled,
the [ContentText](/docs/reference/engine/classes/TextLabel#ContentText) property shows the text as
it appears to the user.

| RichText | Text | ContentText |
| --- | --- | --- |
| false | <b>Hello,<br/> world!</b> | <b>Hello,<br/> world!</b> |
| true | <b>Hello,<br/> world!</b> | Hello,  world! |

Provide feedback

---

Font

Hidden

Not Replicated

Read Parallel

Determines the font used to render text.

TextLabel.Font:[Enum.Font](/docs/reference/engine/enums/Font)

This property selects one of several pre-defined fonts with which the
[TextLabel](/docs/reference/engine/classes/TextLabel) will render its text. Some fonts have bold, italic
and/or light variants.

With the exception of the [Enum.Font.Legacy](/docs/reference/engine/enums/Font#Legacy) font, each font will render
text with the line height equal to the [TextSize](/docs/reference/engine/classes/TextLabel#TextSize)
property.

The [Enum.Font.Code](/docs/reference/engine/enums/Font#Code) font is the only monospace font. It has the unique
property that each character has the exact same width and height ratio of
1:2, where the width of each character is approximately half the
[TextSize](/docs/reference/engine/classes/TextLabel#TextSize) property.

This property is kept in sync with the [FontFace](/docs/reference/engine/classes/TextLabel#FontFace)
property.

Code Samples

Show All Fonts

This code sample renders a list of all the available fonts.

```
local frame = script.Parent



-- Create a TextLabel displaying each font



for _, font in pairs(Enum.Font:GetEnumItems()) do



local textLabel = Instance.new("TextLabel")



textLabel.Name = font.Name



-- Set the text properties



textLabel.Text = font.Name



textLabel.Font = font



-- Some rendering properties



textLabel.TextSize = 24



textLabel.TextXAlignment = Enum.TextXAlignment.Left



-- Size the frame equal to the height of the text



textLabel.Size = UDim2.new(1, 0, 0, textLabel.TextSize)



-- Add to the parent frame



textLabel.Parent = frame



end



-- Layout the frames in a list (if they aren't already)



if not frame:FindFirstChildOfClass("UIListLayout") then



local uiListLayout = Instance.new("UIListLayout")



uiListLayout.Parent = frame



end
```

Provide feedback

---

FontFace

Read Parallel

Determines the font used to render text.

TextLabel.FontFace:[Font](/docs/reference/engine/datatypes/Font)

This property is similar to the [Font](/docs/reference/engine/classes/TextLabel#Font) property but
allows setting fonts that don't exist in [Enum.Font](/docs/reference/engine/enums/Font).

This property is kept in sync with the [Font](/docs/reference/engine/classes/TextLabel#Font)
property, such that when setting [FontFace](/docs/reference/engine/classes/TextLabel#FontFace), the
font is set to the corresponding [Enum.Font](/docs/reference/engine/enums/Font) value or to
[Enum.Font.Unknown](/docs/reference/engine/enums/Font#Unknown) if there are no matches.

Provide feedback

---

FontSize

Deprecated

Show details

---

LineHeight

Read Parallel

Scales the spacing between lines of text in the [TextLabel](/docs/reference/engine/classes/TextLabel).

TextLabel.LineHeight:[number](/docs/luau/numbers)

Controls the height of lines as a multiple of the font's em square size
by scaling the spacing between lines of text in the [TextLabel](/docs/reference/engine/classes/TextLabel).
Valid values range from 1.0 to 3.0, defaulting to 1.0.

Provide feedback

---

LocalizedText

Hidden

Read Only

Not Replicated

Read Parallel

Sets whether a [TextLabel](/docs/reference/engine/classes/TextLabel) should be [GuiBase2d.Localize](/docs/reference/engine/classes/GuiBase2d#Localize) or
not.

TextLabel.LocalizedText:[string](/docs/luau/strings)

This property sets whether a [TextLabel](/docs/reference/engine/classes/TextLabel) should regard
[GuiBase2d.Localize](/docs/reference/engine/classes/GuiBase2d#Localize) or not.

Provide feedback

---

MaxVisibleGraphemes

Read Parallel

The maximum number of graphemes the [TextLabel](/docs/reference/engine/classes/TextLabel) can show.

TextLabel.MaxVisibleGraphemes:[number](/docs/luau/numbers)

This property controls the maximum number of graphemes (or units of text)
that are shown on the [TextLabel](/docs/reference/engine/classes/TextLabel). It is primarily provided as an
easy way to create a
[typewriter effect](/docs/ui/animation#typewriter-effect) where the
characters appear one at a time.

Changing the property does not change the position or size of the visible
graphemes; the layout will be calculated as if all graphemes are visible.

Setting the property to -1 disables the limit and shows the entirety of
the [Text](/docs/reference/engine/classes/TextLabel#Text).

Provide feedback

---

OpenTypeFeatures

Read Parallel

TextLabel.OpenTypeFeatures:[string](/docs/luau/strings)

Provide feedback

---

OpenTypeFeaturesError

Read Only

Not Replicated

Read Parallel

TextLabel.OpenTypeFeaturesError:[string](/docs/luau/strings)

Provide feedback

---

RichText

Read Parallel

Determines whether the [TextLabel](/docs/reference/engine/classes/TextLabel) renders its text using rich text
formatting.

TextLabel.RichText:[boolean](/docs/luau/booleans)

This property determines whether the [TextLabel](/docs/reference/engine/classes/TextLabel) renders its text
using [rich text](/docs/ui/rich-text) markup to style sections of
the string in bold, italics, specific colors, and more.

To use rich text, simply include rich text formatting tags in the
[Text](/docs/reference/engine/classes/TextLabel#Text) string.

Provide feedback

---

Text

Read Parallel

Determines the string rendered by the [TextLabel](/docs/reference/engine/classes/TextLabel).

TextLabel.Text:[string](/docs/luau/strings)

This property determines the text content rendered by the
[TextLabel](/docs/reference/engine/classes/TextLabel). The visual properties of the string rendered to the
screen is determined by [TextColor3](/docs/reference/engine/classes/TextLabel#TextColor3),
[TextTransparency](/docs/reference/engine/classes/TextLabel#TextTransparency),
[TextSize](/docs/reference/engine/classes/TextLabel#TextSize), [Font](/docs/reference/engine/classes/TextLabel#Font),
[TextScaled](/docs/reference/engine/classes/TextLabel#TextScaled),
[TextWrapped](/docs/reference/engine/classes/TextLabel#TextWrapped),
[TextXAlignment](/docs/reference/engine/classes/TextLabel#TextXAlignment) and
[TextYAlignment](/docs/reference/engine/classes/TextLabel#TextYAlignment).

It is possible to render emoji such as 🔒 and other symbols which aren't
affected by the [TextColor3](/docs/reference/engine/classes/TextLabel#TextColor3) property. These
can be pasted into [Script](/docs/reference/engine/classes/Script) and [LocalScript](/docs/reference/engine/classes/LocalScript) objects, as well
as the field within the [Properties](/docs/studio/properties)
window.

This property may contain newline characters. Similarly, this property may
contain a tab character, but it will render as a space instead.

Code Samples

Fading Banner

This code sample creates a fading banner for a TextLabel. It fades text out,
chooses a random string (avoiding repetition), and fades back in.

```
local TweenService = game:GetService("TweenService")



local textLabel = script.Parent



local content = {



"Welcome to my game!",



"Be sure to have fun!",



"Please give suggestions!",



"Be nice to other players!",



"Don't grief other players!",



"Check out the shop!",



"Tip: Don't die!",



}



local tweenInfo = TweenInfo.new(1, Enum.EasingStyle.Sine, Enum.EasingDirection.InOut)



local RNG = Random.new()



local fadeIn = TweenService:Create(textLabel, tweenInfo, {



TextTransparency = 0,



})



local fadeOut = TweenService:Create(textLabel, tweenInfo, {



TextTransparency = 1,



})



local lastIndex



while true do



-- Step 0: Fade out before doing anything



fadeOut:Play()



task.wait(tweenInfo.Time)



-- Step 1: pick content that wasn't the last displayed



local index



repeat



index = RNG:NextInteger(1, #content)



until lastIndex ~= index



-- Make sure we don't show the same thing next time



lastIndex = index



-- Step 2: show the content



textLabel.Text = content[index]



fadeIn:Play()



task.wait(tweenInfo.Time + 1)



end
```

Emoji in Text

This code sample demonstrates emoji rendering using the Text property.

```
local textLabel = script.Parent



local moods = {



["happy"] = "😃",



["sad"] = "😢",



["neutral"] = "😐",



["tired"] = "😫",



}



while true do



for mood, face in pairs(moods) do



textLabel.Text = "I am feeling " .. mood .. "! " .. face



task.wait(1)



end



end
```

Provide feedback

---

TextBounds

Read Only

Not Replicated

Read Parallel

Read-only property which reflects the absolute size of rendered text in
offsets.

TextLabel.TextBounds:[Vector2](/docs/reference/engine/datatypes/Vector2)

This read-only property reflects the absolute size of rendered text in
offsets, meaning that if you try to fit text into a rectangle, this
property would reflect the minimum dimensions of the rectangle you'd need
in order to fit the text.

Using [TextService:GetTextSize()](/docs/reference/engine/classes/TextService#GetTextSize), you can predict what
[TextBounds](/docs/reference/engine/classes/TextLabel#TextBounds) will be given a string,
[Font](/docs/reference/engine/classes/TextLabel#Font), [TextSize](/docs/reference/engine/classes/TextLabel#TextSize), and
frame size.

Provide feedback

---

TextColor

Deprecated

Show details

---

TextColor3

Read Parallel

Determines the color of rendered text.

TextLabel.TextColor3:[Color3](/docs/reference/engine/datatypes/Color3)

This property determines the color of all the text rendered by the
[TextLabel](/docs/reference/engine/classes/TextLabel) element.

Code Samples

Countdown Text

This code sample makes a TextLabel or TextButton count backwards from 10,
setting the text color as it does so.

```
-- Place this code in a LocalScript within a TextLabel/TextButton



local textLabel = script.Parent



-- Some colors we'll use with TextColor3



local colorNormal = Color3.new(0, 0, 0) -- black



local colorSoon = Color3.new(1, 0.5, 0.5) -- red



local colorDone = Color3.new(0.5, 1, 0.5) -- green



-- Loop infinitely



while true do



-- Count backwards from 10 to 1



for i = 10, 1, -1 do



-- Set the text



textLabel.Text = "Time: " .. i



-- Set the color based on how much time is left



if i > 3 then



textLabel.TextColor3 = colorNormal



else



textLabel.TextColor3 = colorSoon



end



task.wait(1)



end



textLabel.Text = "GO!"



textLabel.TextColor3 = colorDone



task.wait(2)



end
```

Provide feedback

---

TextDirection

Read Parallel

Direction in which the text is rendered.

TextLabel.TextDirection:[Enum.TextDirection](/docs/reference/engine/enums/TextDirection)

[Enum.TextDirection](/docs/reference/engine/enums/TextDirection) in which the text is rendered.

Provide feedback

---

TextFits

Read Only

Not Replicated

Read Parallel

A boolean representation of whether the label's text fits within the size
of it.

TextLabel.TextFits:[boolean](/docs/luau/booleans)

A boolean representation of whether the label's text fits within the size
of it.

Provide feedback

---

TextScaled

Read Parallel

Changes whether text is resized to fit within the [TextLabel](/docs/reference/engine/classes/TextLabel).

TextLabel.TextScaled:[boolean](/docs/luau/booleans)

This property determines whether text is scaled so that it fills the
label's entire space. When enabled, [TextSize](/docs/reference/engine/classes/TextLabel#TextSize) is
ignored and [TextWrapped](/docs/reference/engine/classes/TextLabel#TextWrapped) is automatically
enabled. This property is useful for rendering text elements within
[BillboardGuis](/docs/reference/engine/classes/BillboardGui). When this property is used for
[on-screen UI](/docs/ui/on-screen-containers), it may be helpful to
use a [UITextSizeConstraint](/docs/reference/engine/classes/UITextSizeConstraint) to restrict the range of possible text
sizes.

##### Automatic Sizing

It's recommended that you avoid usage of
[TextScaled](/docs/reference/engine/classes/TextLabel#TextScaled) and adjust UI to take advantage of
the [AutomaticSize](/docs/reference/engine/classes/GuiObject#AutomaticSize) property instead. Here
are the core differences between the two properties:

* [TextScaled](/docs/reference/engine/classes/TextLabel#TextScaled) scales the content (text) to
  accommodate the UI. Without careful consideration, some text may become
  unreadable if scaled too small.
* [AutomaticSize](/docs/reference/engine/classes/GuiObject#AutomaticSize) resizes the UI to
  accommodate content while maintaining a consistent font size. For more
  information, see [here](/docs/ui/size-modifiers#automatic-sizing).

Additionally, it's recommended that you avoid applying both
[AutomaticSize](/docs/reference/engine/classes/GuiObject#AutomaticSize) and
[TextScaled](/docs/reference/engine/classes/TextLabel#TextScaled) and to the same [TextLabel](/docs/reference/engine/classes/TextLabel).
[AutomaticSize](/docs/reference/engine/classes/GuiObject#AutomaticSize) determines the maximum
amount of available space that a [GuiObject](/docs/reference/engine/classes/GuiObject) can use (in this case,
text), while [TextScaled](/docs/reference/engine/classes/TextLabel#TextScaled) uses the available
space determined by [AutomaticSize](/docs/reference/engine/classes/GuiObject#AutomaticSize) to scale
the font size up to the maximum font size (100) if there are no size
constraints.

Provide feedback

---

TextSize

Read Parallel

Determines the line height of text in offsets.

TextLabel.TextSize:[number](/docs/luau/numbers)

This property determines the height of one line of rendered text. The unit
is in offsets, not points (which is used in most document editing
programs). The [Enum.Font.Legacy](/docs/reference/engine/enums/Font#Legacy) font does not hold this property.

Provide feedback

---

TextStrokeColor3

Read Parallel

Determines the color of the text stroke (outline).

TextLabel.TextStrokeColor3:[Color3](/docs/reference/engine/datatypes/Color3)

This property sets the color of the stroke, or outline, of rendered text.
Along with
[TextStrokeTransparency](/docs/reference/engine/classes/TextLabel#TextStrokeTransparency), it
determines the final visual appearance of the text stroke.

As a powerful alternative which supports color gradients, see
[UIStroke](/docs/reference/engine/classes/UIStroke).

Provide feedback

---

TextStrokeTransparency

Read Parallel

Determines the transparency of the text stroke (outline).

TextLabel.TextStrokeTransparency:[number](/docs/luau/numbers)

This property sets the transparency of the stroke, or outline, of rendered
text. Along with [TextStrokeColor3](/docs/reference/engine/classes/TextLabel#TextStrokeColor3), it
determines the final visual appearance of the text stroke.

Note that text stroke is multiple renderings of the same transparency, so
this property is essentially multiplicative on itself four times over.
Therefore, it's recommended to set
[TextStrokeTransparency](/docs/reference/engine/classes/TextLabel#TextStrokeTransparency) to a value
in the range of 0.75 to 1 for more a more subtle effect.

As a powerful alternative which supports color gradients, see
[UIStroke](/docs/reference/engine/classes/UIStroke).

Provide feedback

---

TextTransparency

Read Parallel

Determines the transparency of rendered text.

TextLabel.TextTransparency:[number](/docs/luau/numbers)

This property determines the transparency of all the text rendered by the
[TextLabel](/docs/reference/engine/classes/TextLabel).

Provide feedback

---

TextTruncate

Read Parallel

Controls the truncation of the text displayed in the [TextLabel](/docs/reference/engine/classes/TextLabel).

TextLabel.TextTruncate:[Enum.TextTruncate](/docs/reference/engine/enums/TextTruncate)

Controls the truncation of the text displayed in the [TextLabel](/docs/reference/engine/classes/TextLabel).

Provide feedback

---

TextWrap

Deprecated

Show details

---

TextWrapped

Read Parallel

Determines if text wraps to multiple lines within the [TextLabel](/docs/reference/engine/classes/TextLabel)
element's space, truncating excess text.

TextLabel.TextWrapped:[boolean](/docs/luau/booleans)

When enabled, this property will render text on multiple lines within a
[TextLabel](/docs/reference/engine/classes/TextLabel) element's space so that
[TextBounds](/docs/reference/engine/classes/TextLabel#TextBounds) will never exceed the
[GuiBase2d.AbsoluteSize](/docs/reference/engine/classes/GuiBase2d#AbsoluteSize) of the element. This is achieved by
breaking long lines of text into multiple lines.

Line breaks will prefer whitespace; should a long unbroken word exceed the
width of the element, that word will be broken into multiple lines.

If further line breaks would cause the vertical height of the text (the
Y component of [TextBounds](/docs/reference/engine/classes/TextLabel#TextBounds)) to exceed the
vertical height of the element (the Y component of
[GuiBase2d.AbsoluteSize](/docs/reference/engine/classes/GuiBase2d#AbsoluteSize)), then that line will not be rendered at
all.

Provide feedback

---

TextXAlignment

Read Parallel

Determines the horizontal alignment of rendered text.

TextLabel.TextXAlignment:[Enum.TextXAlignment](/docs/reference/engine/enums/TextXAlignment)

This property determines the horizontal alignment of text rendered within
the object's space. It is used in conjunction with
[TextYAlignment](/docs/reference/engine/classes/TextLabel#TextYAlignment) to fully determine text
alignment on both axes.

Note that this property won't affect the read-only properties
[TextBounds](/docs/reference/engine/classes/TextLabel#TextBounds) and
[TextFits](/docs/reference/engine/classes/TextLabel#TextFits).

Provide feedback

---

TextYAlignment

Read Parallel

Determines the vertical alignment of rendered text.

TextLabel.TextYAlignment:[Enum.TextYAlignment](/docs/reference/engine/enums/TextYAlignment)

This property determines the vertical alignment of text rendered within
the object's space. It is used in conjunction with
[TextXAlignment](/docs/reference/engine/classes/TextLabel#TextXAlignment) to fully determine text
alignment on both axes.

Note that this property won't affect the read-only properties
[TextBounds](/docs/reference/engine/classes/TextLabel#TextBounds) and
[TextFits](/docs/reference/engine/classes/TextLabel#TextFits).

Provide feedback

---