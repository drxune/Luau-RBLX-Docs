# TextBox | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TextBox
Scraped: 2026-01-11T02:42:28.547375Z

## Tags
- Not Replicated

## Inherits
- GuiObject
- TextBox
- InputObject
- GuiBase2d
- Instance
- Object
- TextButton
- Text
- PlaceholderText
- ClearTextOnFocus
- MultiLine
- CaptureFocus
- ContextActionService:BindAction()
- Focused
- IsFocused
- UserInputService:GetFocusedTextBox()
- FocusLost
- ReturnPressedFromOnScreenKeyboard
- ReleaseFocus
- CursorPosition
- SelectionStart
- GetPropertyChangedSignal
- TextService:FilterStringAsync()
- Chat:FilterStringAsync()
- TextBox.Text
- CursorPosition()
- SelectionStart()
- TextBox.TextSize
- TextBox.FontFace
- TextBox.Font
- TextBox.PlaceholderText
- TextBox.TextColor3
- TextBox.TextTransparency
- TextBox.TextScaled
- TextBox.TextWrapped
- TextBox.TextXAlignment
- TextBox.TextYAlignment
- Script
- LocalScript
- TextService:GetTextSize()
- TextBox.TextStrokeColor3
- TextBox.BackgroundColor3
- AutomaticSize
- BillboardGuis
- UITextSizeConstraint
- TextBox.TextStrokeTransparency
- TextBox.TextBounds
- GuiBase2d.AbsoluteSize
- TextBox.TextFits
- TextBox.FocusLost
- UserInputService.TextBoxFocused
- UserInputService.TextBoxFocusReleased
- TextBox.Focused
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [GuiObject](/docs/reference/engine/classes/GuiObject)
6. /
7. [TextBox](/docs/reference/engine/classes/TextBox)

English

Feedback

Engine Class

![TextBox](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/TextBox-Dark.webp)TextBox

A 2D user interface element that displays player-editable text.

---

Summary

Properties

|  |
| --- |
| [ClearTextOnFocus](#ClearTextOnFocus):[boolean](/docs/luau/booleans) |
| [ContentText](#ContentText):[string](/docs/luau/strings) |
| [CursorPosition](#CursorPosition):[number](/docs/luau/numbers) |
| [Font](#Font):[Enum.Font](/docs/reference/engine/enums/Font) |
| [FontFace](#FontFace):[Font](/docs/reference/engine/datatypes/Font) |
| [FontSize](#FontSize):[Enum.FontSize](/docs/reference/engine/enums/FontSize)  Deprecated |
| [LineHeight](#LineHeight):[number](/docs/luau/numbers) |
| [MaxVisibleGraphemes](#MaxVisibleGraphemes):[number](/docs/luau/numbers) |
| [MultiLine](#MultiLine):[boolean](/docs/luau/booleans) |
| [OpenTypeFeatures](#OpenTypeFeatures):[string](/docs/luau/strings) |
| [OpenTypeFeaturesError](#OpenTypeFeaturesError):[string](/docs/luau/strings) |
| [PlaceholderColor3](#PlaceholderColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [PlaceholderText](#PlaceholderText):[string](/docs/luau/strings) |
| [RichText](#RichText):[boolean](/docs/luau/booleans) |
| [SelectionStart](#SelectionStart):[number](/docs/luau/numbers) |
| [ShowNativeInput](#ShowNativeInput):[boolean](/docs/luau/booleans) |
| [Text](#Text):[string](/docs/luau/strings) |
| [TextBounds](#TextBounds):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [TextColor](#TextColor):[BrickColor](/docs/reference/engine/datatypes/BrickColor)  Deprecated |
| [TextColor3](#TextColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [TextDirection](#TextDirection):[Enum.TextDirection](/docs/reference/engine/enums/TextDirection) |
| [TextEditable](#TextEditable):[boolean](/docs/luau/booleans) |
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

Methods

|  |
| --- |
| [CaptureFocus](#CaptureFocus)():() |
| [IsFocused](#IsFocused)():[boolean](/docs/luau/booleans) |
| [ReleaseFocus](#ReleaseFocus)(submitted: [boolean](/docs/luau/booleans)):() |

Events

|  |
| --- |
| [Focused](#Focused)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [FocusLost](#FocusLost)(enterPressed: [boolean](/docs/luau/booleans),inputThatCausedFocusLoss: [InputObject](/docs/reference/engine/classes/InputObject)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [ReturnPressedFromOnScreenKeyboard](#ReturnPressedFromOnScreenKeyboard)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

50 inherited from [GuiObject](/docs/reference/engine/classes/GuiObject)

12 inherited from [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A TextBox allows the player to provide text input. It behaves similarly to a
[TextButton](/docs/reference/engine/classes/TextButton), except that a single TextBox can be put in focus by
clicking, tapping, or gamepad selection. While in focus, the player can use a
keyboard to change the [Text](/docs/reference/engine/classes/TextBox#Text) property.

* If there is no text, the [PlaceholderText](/docs/reference/engine/classes/TextBox#PlaceholderText)
  will be visible. This is useful prompting players of the kind or format of
  data they should input.
* By default, the [ClearTextOnFocus](/docs/reference/engine/classes/TextBox#ClearTextOnFocus) property
  is enabled and ensures there is no existing text when a TextBox is
  focused. This may not be desirable for text that should be editable by the
  player.
* The [MultiLine](/docs/reference/engine/classes/TextBox#MultiLine) property allows players to enter
  multiple lines of text with newline characters (\n).

#### Focus State

It is possible to detect and change the focus state of a TextBox:

* You can use [CaptureFocus](/docs/reference/engine/classes/TextBox#CaptureFocus) when a dialogue
  appears so that the player doesn't have to click on a TextBox when it
  becomes available; you can use [ContextActionService:BindAction()](/docs/reference/engine/classes/ContextActionService#BindAction) to
  bind a certain key to focus a TextBox using this function. When a
  TextBox comes into focus, the [Focused](/docs/reference/engine/classes/TextBox#Focused) event fires.
* You can detect if a certain TextBox is in focus by using
  [IsFocused](/docs/reference/engine/classes/TextBox#IsFocused). Alternatively,
  [UserInputService:GetFocusedTextBox()](/docs/reference/engine/classes/UserInputService#GetFocusedTextBox) can be used to check if any
  TextBox is in focus.
* When the player is done inputting text, the
  [FocusLost](/docs/reference/engine/classes/TextBox#FocusLost) event fires, indicating if the user
  pressed Enter to submit text along with the [InputObject](/docs/reference/engine/classes/InputObject)
  that caused the loss of focus. When using on screen keyboards on mobile and
  console,
  [ReturnPressedFromOnScreenKeyboard](/docs/reference/engine/classes/TextBox#ReturnPressedFromOnScreenKeyboard)
  may also fire.
* If some more important matter comes up during gameplay, you can
  [ReleaseFocus](/docs/reference/engine/classes/TextBox#ReleaseFocus) of the TextBox so that a
  player's keyboard input returns to your game.

#### Text Editing

A TextBox supports text selection through its
[CursorPosition](/docs/reference/engine/classes/TextBox#CursorPosition) and
[SelectionStart](/docs/reference/engine/classes/TextBox#SelectionStart) properties. Using
[GetPropertyChangedSignal](/docs/reference/engine/classes/Object#GetPropertyChangedSignal), you can
detect when a selection changes. Additionally, it is possible for players to
copy and paste text within a TextBox, enabling basic clipboard support.

Text Filtering Notice Games that facilitate player-to-player communication
using text, such as custom chat or nametags, must properly filter such text
using [TextService:FilterStringAsync()](/docs/reference/engine/classes/TextService#FilterStringAsync) or
[Chat:FilterStringAsync()](/docs/reference/engine/classes/Chat#FilterStringAsync). If this is not properly done, your game may
receive moderation action.

Code Samples

TextBox Secret Word

This code sample creates a password-like interface for a TextBox, giving
visual feedback on the player's input.

```
-- Place this code in a LocalScript inside a TextBox



local textBox = script.Parent



local secretWord = "roblox"



local colorNormal = Color3.new(1, 1, 1) -- white



local colorWrong = Color3.new(1, 0, 0) -- red



local colorCorrect = Color3.new(0, 1, 0) -- green



-- Initialize the state of the textBox



textBox.ClearTextOnFocus = true



textBox.Text = ""



textBox.Font = Enum.Font.Code



textBox.PlaceholderText = "What is the secret word?"



textBox.BackgroundColor3 = colorNormal



local function onFocused()



textBox.BackgroundColor3 = colorNormal



end



local function onFocusLost(enterPressed, _inputObject)



if enterPressed then



local guess = textBox.Text



if guess == secretWord then



textBox.Text = "ACCESS GRANTED"



textBox.BackgroundColor3 = colorCorrect



else



textBox.Text = "ACCESS DENIED"



textBox.BackgroundColor3 = colorWrong



end



else



-- The player stopped editing without pressing Enter



textBox.Text = ""



textBox.BackgroundColor3 = colorNormal



end



end



textBox.FocusLost:Connect(onFocusLost)



textBox.Focused:Connect(onFocused)
```

---

API Reference

Properties

ClearTextOnFocus

Read Parallel

Determines whether clicking on the TextBox will clear its
[TextBox.Text](/docs/reference/engine/classes/TextBox#Text) property.

TextBox.ClearTextOnFocus:[boolean](/docs/luau/booleans)

Determines whether clicking on the TextBox will clear its
[TextBox.Text](/docs/reference/engine/classes/TextBox#Text) property

Provide feedback

---

ContentText

Read Only

Not Replicated

Read Parallel

TextBox.ContentText:[string](/docs/luau/strings)

Provide feedback

---

CursorPosition

Read Parallel

Determines the offset of the text cursor in bytes, or -1 if there is no
cursor.

TextBox.CursorPosition:[number](/docs/luau/numbers)

This property determines the offset of the text cursor in bytes, or -1
if the [TextBox](/docs/reference/engine/classes/TextBox) is not currently being edited. A value of 1
represents the position before the first byte in the
[Text](/docs/reference/engine/classes/TextBox#Text) property. When used in conjunction with the
[SelectionStart](/docs/reference/engine/classes/TextBox#SelectionStart) property, it is possible to
both get and set selected text within a [TextBox](/docs/reference/engine/classes/TextBox).

Note that the units of this property are bytes and that many unicode
characters such as emoji are longer than 1 byte. For instance, if a player
types in "Hello👋" ("Hello" immediately followed by the waving hand sign),
the cursor position would be 10, not 7, since the emoji uses 4 bytes.

Code Samples

TextBox Selections

This code sample demonstrates reading the current selection of a TextBox
using [CursorPosition()](/docs/reference/engine/classes/TextBox#CursorPosition) and
[SelectionStart()](/docs/reference/engine/classes/TextBox#SelectionStart).

```
local textBox = script.Parent



local function showSelection()



if textBox.CursorPosition == -1 or textBox.SelectionStart == -1 then



print("No selection")



else



local selectedText = string.sub(



textBox.Text,



math.min(textBox.CursorPosition, textBox.SelectionStart),



math.max(textBox.CursorPosition, textBox.SelectionStart)



)



print('The selection is:"', selectedText, '"')



end



end



textBox:GetPropertyChangedSignal("CursorPosition"):Connect(showSelection)



textBox:GetPropertyChangedSignal("SelectionStart"):Connect(showSelection)
```

Provide feedback

---

Font

Hidden

Not Replicated

Read Parallel

Determines the font used to render text.

TextBox.Font:[Enum.Font](/docs/reference/engine/enums/Font)

The Font property selects one of several pre-defined [fonts](/docs/reference/engine/enums/Font)
with which the UI element will render its text. Some fonts have bold,
italic and/or light variants (as there is no font-weight or font-style
properties).

With the exception of the "Legacy" font, each font will render text with
the line height equal to the [TextBox.TextSize](/docs/reference/engine/classes/TextBox#TextSize) property. The "Code"
font is the only monospace font. It has the unique property that each
character has the exact same width and height ratio of 1:2. The width of
each character is approximately half the [TextBox.TextSize](/docs/reference/engine/classes/TextBox#TextSize)
property.

This property is kept in sync with the [TextBox.FontFace](/docs/reference/engine/classes/TextBox#FontFace) property.
When setting Font, the FontFace will be set to
[Font.fromEnum(value)](/docs/reference/engine/datatypes/Font#fromEnum).

Code Samples

Cycle Font

This code sample sets a parent TextLabel's Font and Text properties to all the
different fonts available.

```
local textLabel = script.Parent



while true do



-- Iterate over all the different fonts



for _, font in pairs(Enum.Font:GetEnumItems()) do



textLabel.Font = font



textLabel.Text = font.Name



task.wait(1)



end



end
```

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

TextBox.FontFace:[Font](/docs/reference/engine/datatypes/Font)

The FontFace property is similar to the Font property, but allows setting
fonts that don't exist in the Font enum.

This property is kept in sync with the [TextBox.Font](/docs/reference/engine/classes/TextBox#Font) property. When
setting FontFace, the Font is set to the corresponding enum value, or to
[Enum.Font.Unknown](/docs/reference/engine/enums/Font#Unknown) if there are no matches.

Provide feedback

---

FontSize

Deprecated

Show details

---

LineHeight

Read Parallel

Scales the spacing between lines of text in the [TextBox](/docs/reference/engine/classes/TextBox).

TextBox.LineHeight:[number](/docs/luau/numbers)

Controls the height of lines, as a multiple of the font's em square size,
by scaling the spacing between lines of text in the [TextBox](/docs/reference/engine/classes/TextBox). Valid
values range from 1.0 to 3.0, defaulting to 1.0.

Provide feedback

---

MaxVisibleGraphemes

Read Parallel

The maximum number of graphemes the [TextBox](/docs/reference/engine/classes/TextBox) can show.

TextBox.MaxVisibleGraphemes:[number](/docs/luau/numbers)

This property controls the maximum number of graphemes (or units of text)
that are shown on the [TextBox](/docs/reference/engine/classes/TextBox), regardless of whether it's showing
the [TextBox.PlaceholderText](/docs/reference/engine/classes/TextBox#PlaceholderText) or [TextBox.Text](/docs/reference/engine/classes/TextBox#Text).

Changing the property does not change the position or size of the visible
graphemes - the layout will be calculated as if all graphemes are visible.

Setting the property to -1 disables the limit and shows the entirety of
the [TextBox.Text](/docs/reference/engine/classes/TextBox#Text).

Provide feedback

---

MultiLine

Read Parallel

When set to true, text inside a TextBox is able to move onto multiple
lines. This also enables players to use the enter key to move onto a new
line.

TextBox.MultiLine:[boolean](/docs/luau/booleans)

When set to true, text inside a TextBox is able to move onto multiple
lines. This also enables players to use the enter key to move onto a new
line.

Provide feedback

---

OpenTypeFeatures

Read Parallel

TextBox.OpenTypeFeatures:[string](/docs/luau/strings)

Provide feedback

---

OpenTypeFeaturesError

Read Only

Not Replicated

Read Parallel

TextBox.OpenTypeFeaturesError:[string](/docs/luau/strings)

Provide feedback

---

PlaceholderColor3

Read Parallel

Sets the text color that gets used when no text has been entered into the
TextBox yet.

TextBox.PlaceholderColor3:[Color3](/docs/reference/engine/datatypes/Color3)

Sets the text color that gets used when no text has been entered into the
TextBox yet.

Provide feedback

---

PlaceholderText

Read Parallel

Sets the text that gets displayed when no text has been entered into the
TextBox yet.

TextBox.PlaceholderText:[string](/docs/luau/strings)

Sets the text that gets displayed when no text has been entered into the
TextBox yet.

Provide feedback

---

RichText

Read Parallel

Determines whether the TextBox renders the [TextBox.Text](/docs/reference/engine/classes/TextBox#Text) string
using rich text formatting.

TextBox.RichText:[boolean](/docs/luau/booleans)

This property determines whether the [TextBox](/docs/reference/engine/classes/TextBox) renders the
[TextBox.Text](/docs/reference/engine/classes/TextBox#Text) string using rich text formatting. Rich text uses
simple markup tags to style sections of the string in bold, italics,
specific colors, and more.

To use rich text, simply include formatting tags in the
[TextBox.Text](/docs/reference/engine/classes/TextBox#Text) string.

Note that when the [TextBox](/docs/reference/engine/classes/TextBox) has this property enabled and the box
gains focus, the user will be able to edit and interact with the complete
XML string, including all of the formatting tags. When focus is lost, the
text will automatically parse and render the tags as rich text.

Provide feedback

---

SelectionStart

Read Parallel

Determines the starting position of a text selection, or -1 if no text is
selected.

TextBox.SelectionStart:[number](/docs/luau/numbers)

Determines the starting position of a text selection, or -1 if the TextBox
has no range of selected text. If the value is -1 or equivalent to
[CursorPosition](/docs/reference/engine/classes/TextBox#CursorPosition), there is no range of text
selected. This property uses the same positioning logic as CursorPosition.
SelectionStart will be greater than CursorPosition if the cursor is at the
beginning of a selection, and less than CursorPosition if the cursor is at
the end.

Code Samples

TextBox Selections

This code sample demonstrates reading the current selection of a TextBox
using [CursorPosition()](/docs/reference/engine/classes/TextBox#CursorPosition) and
[SelectionStart()](/docs/reference/engine/classes/TextBox#SelectionStart).

```
local textBox = script.Parent



local function showSelection()



if textBox.CursorPosition == -1 or textBox.SelectionStart == -1 then



print("No selection")



else



local selectedText = string.sub(



textBox.Text,



math.min(textBox.CursorPosition, textBox.SelectionStart),



math.max(textBox.CursorPosition, textBox.SelectionStart)



)



print('The selection is:"', selectedText, '"')



end



end



textBox:GetPropertyChangedSignal("CursorPosition"):Connect(showSelection)



textBox:GetPropertyChangedSignal("SelectionStart"):Connect(showSelection)
```

Provide feedback

---

ShowNativeInput

Read Parallel

If set to true, input native to the platform is used instead of Roblox's
built-in keyboard.

TextBox.ShowNativeInput:[boolean](/docs/luau/booleans)

If set to true, input native to the platform is used instead of Roblox's
built-in keyboard.

Provide feedback

---

Text

Read Parallel

Determines the string rendered by the UI element.

TextBox.Text:[string](/docs/luau/strings)

The Text property determines the content rendered by the UI element. The
visual properties of the string rendered to the screen is determined by
[TextBox.TextColor3](/docs/reference/engine/classes/TextBox#TextColor3), [TextBox.TextTransparency](/docs/reference/engine/classes/TextBox#TextTransparency),
[TextBox.TextSize](/docs/reference/engine/classes/TextBox#TextSize), [TextBox.Font](/docs/reference/engine/classes/TextBox#Font),
[TextBox.TextScaled](/docs/reference/engine/classes/TextBox#TextScaled), [TextBox.TextWrapped](/docs/reference/engine/classes/TextBox#TextWrapped),
[TextBox.TextXAlignment](/docs/reference/engine/classes/TextBox#TextXAlignment) and [TextBox.TextYAlignment](/docs/reference/engine/classes/TextBox#TextYAlignment).

It is possible to render emoji (for example, 😃) and other symbols. These
special symbols aren't affected by the [TextBox.TextColor3](/docs/reference/engine/classes/TextBox#TextColor3)
property. These can be pasted into [Script](/docs/reference/engine/classes/Script) and [LocalScript](/docs/reference/engine/classes/LocalScript)
objects, as well as the field within the Properties window.

This property may contain newline characters, however, it is not possible
to type newline characters within the Properties window. Similarly, this
property may contain a tab character, but it will render as a space
instead.

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

"Kaboom!" Text

This code sample repeatedly tweens a TextLabel's TextSize from 5 to 100 and
fades out the text as it grows in size.

```
local textLabel = script.Parent



textLabel.Text = "Kaboom!"



while true do



for size = 5, 100, 5 do



textLabel.TextSize = size



textLabel.TextTransparency = size / 100



task.wait()



end



task.wait(1)



end
```

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

Long Text Wrapping

This code sample demonstrates TextWrap by spelling out a long chunk of text
progressively. If the text doesn't fit, it turns a different color.

```
local textLabel = script.Parent



-- This text wrapping demo is best shown on a 200x50 px rectangle



textLabel.Size = UDim2.new(0, 200, 0, 50)



-- Some content to spell out



local content = "Here's a long string of words that will "



.. "eventually exceed the UI element's width "



.. "and form line breaks. Useful for paragraphs "



.. "that are really long."



-- A function that will spell text out two characters at a time



local function spellTheText()



-- Iterate from 1 to the length of our content



for i = 1, content:len() do



-- Get a substring of our content: 1 to i



textLabel.Text = content:sub(1, i)



-- Color the text if it doesn't fit in our box



if textLabel.TextFits then



textLabel.TextColor3 = Color3.new(0, 0, 0) -- Black



else



textLabel.TextColor3 = Color3.new(1, 0, 0) -- Red



end



-- Wait a brief moment on even lengths



if i % 2 == 0 then



task.wait()



end



end



end



while true do



-- Spell the text with scale/wrap off



textLabel.TextWrapped = false



textLabel.TextScaled = false



spellTheText()



task.wait(1)



-- Spell the text with wrap on



textLabel.TextWrapped = true



textLabel.TextScaled = false



spellTheText()



task.wait(1)



-- Spell the text with text scaling on



-- Note: Text turns red (TextFits = false) once text has to be



-- scaled down in order to fit within the UI element.



textLabel.TextScaled = true



-- Note: TextWrapped is enabled implicitly when TextScaled = true



--textLabel.TextWrapped = true



spellTheText()



task.wait(1)



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

The size of a UI element's text in offsets.

TextBox.TextBounds:[Vector2](/docs/reference/engine/datatypes/Vector2)

The read-only property TextBounds reflects the absolute size of rendered
text in offsets. In other words, if you were to try to fit text into a
rectangle, this property would reflect the minimum dimensions of the
rectangle you would need in order to fit the text.

Using [TextService:GetTextSize()](/docs/reference/engine/classes/TextService#GetTextSize), you can predict what TextBounds
will be on a TextLabel given a string, [TextBox.Font](/docs/reference/engine/classes/TextBox#Font),
[TextBox.TextSize](/docs/reference/engine/classes/TextBox#TextSize) and frame size.

Code Samples

Dynamic TextBox Size

This code sample dynamically resizes a TextLabel, TextButton or TextBox to
match the size of its TextBounds. Try changing the minimum width/height and
pasting into a LocalScript in a TextBox.

```
local textBox = script.Parent



-- The smallest the TextBox will go



local minWidth, minHeight = 10, 10



-- Set alignment so our text doesn't wobble a bit while we type



textBox.TextXAlignment = Enum.TextXAlignment.Left



textBox.TextYAlignment = Enum.TextYAlignment.Top



local function updateSize()



textBox.Size = UDim2.new(0, math.max(minWidth, textBox.TextBounds.X), 0, math.max(minHeight, textBox.TextBounds.Y))



end



textBox:GetPropertyChangedSignal("TextBounds"):Connect(updateSize)
```

Provide feedback

---

TextColor

Deprecated

Show details

---

TextColor3

Read Parallel

Determines the color of rendered text.

TextBox.TextColor3:[Color3](/docs/reference/engine/datatypes/Color3)

This property determines the color of all the text rendered by a
[GuiObject](/docs/reference/engine/classes/GuiObject) element. This property along with [TextBox.Font](/docs/reference/engine/classes/TextBox#Font),
[TextBox.TextSize](/docs/reference/engine/classes/TextBox#TextSize) and [TextBox.TextTransparency](/docs/reference/engine/classes/TextBox#TextTransparency) will
determine the visual properties of text. Text is rendered after the text
stroke ([TextBox.TextStrokeColor3](/docs/reference/engine/classes/TextBox#TextStrokeColor3)).

It's important that text is easily read by players! Be sure to choose
colors with little-to-no saturation, like white, grey, or black. Make sure
the color of your text is contrasted by the
[TextBox.BackgroundColor3](/docs/reference/engine/classes/TextBox#BackgroundColor3) of the UI element. If the element has a
transparent background, try applying a black
[TextBox.TextStrokeColor3](/docs/reference/engine/classes/TextBox#TextStrokeColor3) to help contrast the text with the 3D
world behind it.

Code Samples

Vowel Detector

This code sample, when placed within a TextBox, will turn the text color red
if the typed string contains no vowels (A, E, I, O or U).

```
local textBox = script.Parent



local function hasVowels(str)



return str:lower():find("[aeiou]")



end



local function onTextChanged()



local text = textBox.Text



-- Check for vowels



if hasVowels(text) then



textBox.TextColor3 = Color3.new(0, 0, 0) -- Black



else



textBox.TextColor3 = Color3.new(1, 0, 0) -- Red



end



end



textBox:GetPropertyChangedSignal("Text"):Connect(onTextChanged)
```

TextBox Secret Word

This code sample creates a password-like interface for a TextBox, giving
visual feedback on the player's input.

```
-- Place this code in a LocalScript inside a TextBox



local textBox = script.Parent



local secretWord = "roblox"



local colorNormal = Color3.new(1, 1, 1) -- white



local colorWrong = Color3.new(1, 0, 0) -- red



local colorCorrect = Color3.new(0, 1, 0) -- green



-- Initialize the state of the textBox



textBox.ClearTextOnFocus = true



textBox.Text = ""



textBox.Font = Enum.Font.Code



textBox.PlaceholderText = "What is the secret word?"



textBox.BackgroundColor3 = colorNormal



local function onFocused()



textBox.BackgroundColor3 = colorNormal



end



local function onFocusLost(enterPressed, _inputObject)



if enterPressed then



local guess = textBox.Text



if guess == secretWord then



textBox.Text = "ACCESS GRANTED"



textBox.BackgroundColor3 = colorCorrect



else



textBox.Text = "ACCESS DENIED"



textBox.BackgroundColor3 = colorWrong



end



else



-- The player stopped editing without pressing Enter



textBox.Text = ""



textBox.BackgroundColor3 = colorNormal



end



end



textBox.FocusLost:Connect(onFocusLost)



textBox.Focused:Connect(onFocused)
```

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

Game State Text

This code sample mirrors the contents of a StringValue into a TextLabel,
updating and setting the color of the text as it changes.

```
local ReplicatedStorage = game:GetService("ReplicatedStorage")



-- Place a StringValue called "GameState" in the ReplicatedStorage



local vGameState = ReplicatedStorage:WaitForChild("GameState")



-- Place this code in a TextLabel



local textLabel = script.Parent



-- Some colors we'll use with TextColor3



local colorNormal = Color3.new(0, 0, 0) -- black



local colorCountdown = Color3.new(1, 0.5, 0) -- orange



local colorRound = Color3.new(0.25, 0.25, 1) -- blue



-- We'll run this function to update the TextLabel as the state of the



-- game changes.



local function update()



-- Update the text



textLabel.Text = "State: " .. vGameState.Value



-- Set the color of the text based on the current game state



if vGameState.Value == "Countdown" then



textLabel.TextColor3 = colorCountdown



elseif vGameState.Value == "Round" then



textLabel.TextColor3 = colorRound



else



textLabel.TextColor3 = colorNormal



end



end



-- Pattern: update once when we start and also when vGameState changes



-- We should always see the most updated GameState.



update()



vGameState.Changed:Connect(update)
```

Provide feedback

---

TextDirection

Read Parallel

TextBox.TextDirection:[Enum.TextDirection](/docs/reference/engine/enums/TextDirection)

Provide feedback

---

TextEditable

Read Parallel

Determines whether the user can change the [Text](/docs/reference/engine/classes/TextBox#Text).

TextBox.TextEditable:[boolean](/docs/luau/booleans)

TextEditable determines whether the user can change the
[Text](/docs/reference/engine/classes/TextBox#Text) through input. It is recommended to disable
[ClearTextOnFocus](/docs/reference/engine/classes/TextBox#ClearTextOnFocus) when this property is
disabled, otherwise the Text could be cleared on-focus. This property is
useful to make read-only TextBoxes from which content can be copied
in-game.

Provide feedback

---

TextFits

Read Only

Not Replicated

Read Parallel

Whether the text fits within the constraints of the TextBox.

TextBox.TextFits:[boolean](/docs/luau/booleans)

Whether the text fits within the constraints of the TextBox.

Provide feedback

---

TextScaled

Read Parallel

Changes whether text is resized to fit the GUI object that renders it.

TextBox.TextScaled:[boolean](/docs/luau/booleans)

Rather than using TextScaled, we recommend you consider using
[AutomaticSize](/docs/reference/engine/classes/GuiObject#AutomaticSize), a new method to dynamically
size UI that will give you the best visual result possible.

The TextScaled property determines whether text is scaled so that it fills
the entire UI element's space. When this is enabled,
[TextBox.TextSize](/docs/reference/engine/classes/TextBox#TextSize) is ignored and [TextBox.TextWrapped](/docs/reference/engine/classes/TextBox#TextWrapped) is
automatically enabled. This property is useful for text-rendering UI
elements within [BillboardGuis](/docs/reference/engine/classes/BillboardGui).

When this property is used for screen-space UI, it may be desirable to use
a [UITextSizeConstraint](/docs/reference/engine/classes/UITextSizeConstraint) to restrict the range of possible text
sizes.

#### TextScaled and AutomaticSize

It's recommended that developers avoid usage of TextScaled and adjust UI
to take advantage of the AutomaticSize property instead. Here are the core
differences between the two properties:

* TextScaled scales the content (text) to accommodate the UI. Without
  careful consideration, some text may become unreadable if scaled too
  small.
* AutomaticSize resizes the UI to accommodate content.

With AutomaticSize, you're able to adjust your UI to accommodate the
content (text) while maintaining a consistent font size. For more
information on how to use automatic sizing, see the UI Automatic Size
article.

We suggest that you don't apply both TextScaled and AutomaticSize on the
same UI object. If you apply both properties:

* AutomaticSize determines the maximum amount of available space that a
  [GuiObject](/docs/reference/engine/classes/GuiObject) can use (in this case, text)
* TextScaled uses the available space determined by AutomaticSize, to
  scale the font size to fit the available space, which will expand up to
  the maximum font size (100), if there are no size constraints
* The end result will be: text goes to 100 font size and the UI object
  will expand to fit that text

Using both AutomaticSize and TextScaled at the same time can result in
significant scaling differences than when AutomaticSize is off.

Code Samples

Long Text Wrapping

This code sample demonstrates TextWrap by spelling out a long chunk of text
progressively. If the text doesn't fit, it turns a different color.

```
local textLabel = script.Parent



-- This text wrapping demo is best shown on a 200x50 px rectangle



textLabel.Size = UDim2.new(0, 200, 0, 50)



-- Some content to spell out



local content = "Here's a long string of words that will "



.. "eventually exceed the UI element's width "



.. "and form line breaks. Useful for paragraphs "



.. "that are really long."



-- A function that will spell text out two characters at a time



local function spellTheText()



-- Iterate from 1 to the length of our content



for i = 1, content:len() do



-- Get a substring of our content: 1 to i



textLabel.Text = content:sub(1, i)



-- Color the text if it doesn't fit in our box



if textLabel.TextFits then



textLabel.TextColor3 = Color3.new(0, 0, 0) -- Black



else



textLabel.TextColor3 = Color3.new(1, 0, 0) -- Red



end



-- Wait a brief moment on even lengths



if i % 2 == 0 then



task.wait()



end



end



end



while true do



-- Spell the text with scale/wrap off



textLabel.TextWrapped = false



textLabel.TextScaled = false



spellTheText()



task.wait(1)



-- Spell the text with wrap on



textLabel.TextWrapped = true



textLabel.TextScaled = false



spellTheText()



task.wait(1)



-- Spell the text with text scaling on



-- Note: Text turns red (TextFits = false) once text has to be



-- scaled down in order to fit within the UI element.



textLabel.TextScaled = true



-- Note: TextWrapped is enabled implicitly when TextScaled = true



--textLabel.TextWrapped = true



spellTheText()



task.wait(1)



end
```

Provide feedback

---

TextSize

Read Parallel

Determine the line height of text in offsets.

TextBox.TextSize:[number](/docs/luau/numbers)

The TextSize property determines the height in offsets of one line of
rendered text. The unit is in offsets, not points (which is used in most
document editing programs). The "Legacy" font does not hold this property.

Code Samples

"Kaboom!" Text

This code sample repeatedly tweens a TextLabel's TextSize from 5 to 100 and
fades out the text as it grows in size.

```
local textLabel = script.Parent



textLabel.Text = "Kaboom!"



while true do



for size = 5, 100, 5 do



textLabel.TextSize = size



textLabel.TextTransparency = size / 100



task.wait()



end



task.wait(1)



end
```

Provide feedback

---

TextStrokeColor3

Read Parallel

Determines the color of the text stroke (outline).

TextBox.TextStrokeColor3:[Color3](/docs/reference/engine/datatypes/Color3)

The TextStrokeColor3 property sets the color of the stroke, or outline, of
rendered text. This property and [TextBox.TextStrokeTransparency](/docs/reference/engine/classes/TextBox#TextStrokeTransparency)
determine the visual properties of the text stroke.

Text stroke is rendered before normal text and is simply 4 renderings of
the same text in +/- 1 pixel offsets in each direction. Text stroke
rendering works independently and identically to
[TextBox.TextColor3](/docs/reference/engine/classes/TextBox#TextColor3) and [TextBox.TextTransparency](/docs/reference/engine/classes/TextBox#TextTransparency).

Code Samples

Text Highlight Oscillation

This code sample oscillates a TextLabel's TextStrokeTransparency so that it
blinks the highlight of a text.

```
local textLabel = script.Parent



-- How fast the highlight ought to blink



local freq = 2



-- Set to yellow highlight color



textLabel.TextStrokeColor3 = Color3.new(1, 1, 0)



while true do



-- math.sin oscillates from -1 to 1, so we change the range to 0 to 1:



local transparency = math.sin(workspace.DistributedGameTime * math.pi * freq) * 0.5 + 0.5



textLabel.TextStrokeTransparency = transparency



task.wait()



end
```

Provide feedback

---

TextStrokeTransparency

Read Parallel

Determines the transparency of the text stroke (outline).

TextBox.TextStrokeTransparency:[number](/docs/luau/numbers)

The TextStrokeTransparency property sets the transparency of the stroke,
or outline, of rendered text. This property and
[TextBox.TextStrokeColor3](/docs/reference/engine/classes/TextBox#TextStrokeColor3) determine the visual properties of the
text stroke.

Text stroke is rendered before normal text and is simply 4 renderings of
the same text in +/- 1 pixel offsets in each direction. Text stroke
rendering works independently and identically to
[TextBox.TextColor3](/docs/reference/engine/classes/TextBox#TextColor3) and [TextBox.TextTransparency](/docs/reference/engine/classes/TextBox#TextTransparency). Since
text stroke is simply multiple renderings of the same transparency, this
property is essentially multiplicative on itself four times over (e.g. a
TextStrokeTransparency of 0.5 appears about the same as TextTransparency
of 0.0625, or 0.5^4). Therefore, it's recommended to set
TextStrokeTransparency to a value in the range of 0.75 to 1 for more a
more subtle effect.

Code Samples

Text Highlight Oscillation

This code sample oscillates a TextLabel's TextStrokeTransparency so that it
blinks the highlight of a text.

```
local textLabel = script.Parent



-- How fast the highlight ought to blink



local freq = 2



-- Set to yellow highlight color



textLabel.TextStrokeColor3 = Color3.new(1, 1, 0)



while true do



-- math.sin oscillates from -1 to 1, so we change the range to 0 to 1:



local transparency = math.sin(workspace.DistributedGameTime * math.pi * freq) * 0.5 + 0.5



textLabel.TextStrokeTransparency = transparency



task.wait()



end
```

Provide feedback

---

TextTransparency

Read Parallel

Determines the transparency of rendered text.

TextBox.TextTransparency:[number](/docs/luau/numbers)

The TextColor3 property determines the transparency of all the text
rendered by a UI element. This property along with [TextBox.Font](/docs/reference/engine/classes/TextBox#Font),
[TextBox.TextSize](/docs/reference/engine/classes/TextBox#TextSize) and [TextBox.TextColor3](/docs/reference/engine/classes/TextBox#TextColor3) will determine the
visual properties of text. Text is rendered after the text stroke
([TextBox.TextStrokeTransparency](/docs/reference/engine/classes/TextBox#TextStrokeTransparency)).

Fading text in using a numeric for-loop is a fantastic way to draw a
player's attention to text appearing on screen.

```
-- Count backwards from 1 to 0, decrementing by 0.1



for i = 1, 0, -0.1 do



textLabel.TextTransparency = i



task.wait(0.1)



end
```

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

"Kaboom!" Text

This code sample repeatedly tweens a TextLabel's TextSize from 5 to 100 and
fades out the text as it grows in size.

```
local textLabel = script.Parent



textLabel.Text = "Kaboom!"



while true do



for size = 5, 100, 5 do



textLabel.TextSize = size



textLabel.TextTransparency = size / 100



task.wait()



end



task.wait(1)



end
```

Provide feedback

---

TextTruncate

Read Parallel

Controls the truncation of the text displayed in this TextBox.

TextBox.TextTruncate:[Enum.TextTruncate](/docs/reference/engine/enums/TextTruncate)

Controls the truncation of the text displayed in this TextBox.

Provide feedback

---

TextWrap

Deprecated

Show details

---

TextWrapped

Read Parallel

Determines if text wraps to multiple lines within the [GuiObject](/docs/reference/engine/classes/GuiObject)
element space, truncating excess text.

TextBox.TextWrapped:[boolean](/docs/luau/booleans)

When enabled, this property will render text on multiple lines within a
[TextBox](/docs/reference/engine/classes/TextBox) element's space so that [TextBox.TextBounds](/docs/reference/engine/classes/TextBox#TextBounds) will
never exceed the [GuiBase2d.AbsoluteSize](/docs/reference/engine/classes/GuiBase2d#AbsoluteSize) of the GUI element.

This is achieved by breaking long lines of text into multiple lines. Line
breaks will prefer whitespace; should a long unbroken word exceed the
width of the element, that word will be broken into multiple lines.

If further line breaks would cause the vertical height of the text (the Y
component of [TextBox.TextBounds](/docs/reference/engine/classes/TextBox#TextBounds)) to exceed the vertical height of
the element (the Y component of [GuiBase2d.AbsoluteSize](/docs/reference/engine/classes/GuiBase2d#AbsoluteSize)), then that
line will not be rendered at all.

Code Samples

Long Text Wrapping

This code sample demonstrates TextWrap by spelling out a long chunk of text
progressively. If the text doesn't fit, it turns a different color.

```
local textLabel = script.Parent



-- This text wrapping demo is best shown on a 200x50 px rectangle



textLabel.Size = UDim2.new(0, 200, 0, 50)



-- Some content to spell out



local content = "Here's a long string of words that will "



.. "eventually exceed the UI element's width "



.. "and form line breaks. Useful for paragraphs "



.. "that are really long."



-- A function that will spell text out two characters at a time



local function spellTheText()



-- Iterate from 1 to the length of our content



for i = 1, content:len() do



-- Get a substring of our content: 1 to i



textLabel.Text = content:sub(1, i)



-- Color the text if it doesn't fit in our box



if textLabel.TextFits then



textLabel.TextColor3 = Color3.new(0, 0, 0) -- Black



else



textLabel.TextColor3 = Color3.new(1, 0, 0) -- Red



end



-- Wait a brief moment on even lengths



if i % 2 == 0 then



task.wait()



end



end



end



while true do



-- Spell the text with scale/wrap off



textLabel.TextWrapped = false



textLabel.TextScaled = false



spellTheText()



task.wait(1)



-- Spell the text with wrap on



textLabel.TextWrapped = true



textLabel.TextScaled = false



spellTheText()



task.wait(1)



-- Spell the text with text scaling on



-- Note: Text turns red (TextFits = false) once text has to be



-- scaled down in order to fit within the UI element.



textLabel.TextScaled = true



-- Note: TextWrapped is enabled implicitly when TextScaled = true



--textLabel.TextWrapped = true



spellTheText()



task.wait(1)



end
```

Provide feedback

---

TextXAlignment

Read Parallel

Determines the horizontal alignment of rendered text.

TextBox.TextXAlignment:[Enum.TextXAlignment](/docs/reference/engine/enums/TextXAlignment)

TextXAlignment determines the horizontal alignment (X-axis) of text
rendered within a UI element's space. It functions similarly to the CSS
text-align property, with left, right and center values (there is no
justify option). For Left and Right, text is rendered such that the
left/right text bounds just touch the edge of the UI element rectangle.
For Center, each line of text is centered on the very center of the UI
element rectangle.

This property is used in conjunction with [TextBox.TextYAlignment](/docs/reference/engine/classes/TextBox#TextYAlignment)
to fully determine text alignment on both axes. This property won't affect
the read-only properties [TextBox.TextBounds](/docs/reference/engine/classes/TextBox#TextBounds) and
[TextBox.TextFits](/docs/reference/engine/classes/TextBox#TextFits).

Code Samples

Text Alignment

This code sample shows all the different text alignment combinations by
iterating over each enum item. It is meant to be placed within a TextLabel,
TextButton or TextBox.

```
-- Paste this in a LocalScript within a TextLabel/TextButton/TextBox



local textLabel = script.Parent



local function setAlignment(xAlign, yAlign)



textLabel.TextXAlignment = xAlign



textLabel.TextYAlignment = yAlign



textLabel.Text = xAlign.Name .. " + " .. yAlign.Name



end



while true do



-- Iterate over both TextXAlignment and TextYAlignment enum items



for _, yAlign in pairs(Enum.TextYAlignment:GetEnumItems()) do



for _, xAlign in pairs(Enum.TextXAlignment:GetEnumItems()) do



setAlignment(xAlign, yAlign)



task.wait(1)



end



end



end
```

Provide feedback

---

TextYAlignment

Read Parallel

Determines the vertical alignment of rendered text.

TextBox.TextYAlignment:[Enum.TextYAlignment](/docs/reference/engine/enums/TextYAlignment)

TextYAlignment determines the vertical alignment (Y-axis) of text rendered
within a UI element's space. For Top and Bottom, text is rendered such
that the top/bottom text bounds just touch the edge of the UI element
rectangle. For Center, text is rendered such that there is an equal space
from the top bounds of the text to the top of the element and the bottom
bounds of the text to the bottom of the element.

This property is used in conjunction with [TextBox.TextXAlignment](/docs/reference/engine/classes/TextBox#TextXAlignment)
to fully determine text alignment on both axes. This property won't affect
the read-only properties [TextBox.TextBounds](/docs/reference/engine/classes/TextBox#TextBounds) and
[TextBox.TextFits](/docs/reference/engine/classes/TextBox#TextFits).

Code Samples

Text Alignment

This code sample shows all the different text alignment combinations by
iterating over each enum item. It is meant to be placed within a TextLabel,
TextButton or TextBox.

```
-- Paste this in a LocalScript within a TextLabel/TextButton/TextBox



local textLabel = script.Parent



local function setAlignment(xAlign, yAlign)



textLabel.TextXAlignment = xAlign



textLabel.TextYAlignment = yAlign



textLabel.Text = xAlign.Name .. " + " .. yAlign.Name



end



while true do



-- Iterate over both TextXAlignment and TextYAlignment enum items



for _, yAlign in pairs(Enum.TextYAlignment:GetEnumItems()) do



for _, xAlign in pairs(Enum.TextXAlignment:GetEnumItems()) do



setAlignment(xAlign, yAlign)



task.wait(1)



end



end



end
```

Provide feedback

---

Methods

CaptureFocus

Forces the client to focus on the TextBox.

TextBox:CaptureFocus():()

Returns

()

Forces the client to focus on the TextBox.

Code Samples

TextBox:CaptureFocus

This code sample causes the client to focus on the parent TextBox when the
Q key is pressed by the player.

```
local ContextActionService = game:GetService("ContextActionService")



local ACTION_NAME = "FocusTheTextBox"



local textBox = script.Parent



local function handleAction(actionName, inputState, _inputObject)



if actionName == ACTION_NAME and inputState == Enum.UserInputState.End then



textBox:CaptureFocus()



end



end



ContextActionService:BindAction(ACTION_NAME, handleAction, false, Enum.KeyCode.Q)
```

Provide feedback

---

IsFocused

Returns true if the TextBox is focused or false if it is not.

TextBox:IsFocused():[boolean](/docs/luau/booleans)

Returns

[boolean](/docs/luau/booleans)

Returns true if the TextBox is focused or false if it is not.

Provide feedback

---

ReleaseFocus

Forces the client to unfocus the TextBox.

TextBox:ReleaseFocus(submitted:[boolean](/docs/luau/booleans)):()

Parameters

|  |
| --- |
| submitted:[boolean](/docs/luau/booleans) Default Value: false |

Returns

()

Forces the client to unfocus the TextBox. The submitted parameter allows
you to over-ride the enterPressed parameter in the
[TextBox.FocusLost](/docs/reference/engine/classes/TextBox#FocusLost) event.

This item should be used with a [LocalScript](/docs/reference/engine/classes/LocalScript) in order to work as
expected in online mode.

The code shown below will force the client to unfocus the 'TextBox' 5
seconds after it's selected:

```
local TextBox = script.Parent



TextBox.Focused:Connect(function()



wait(5)



TextBox:ReleaseFocus()



end)
```

Please be aware that the above example assumes that it's in a LocalScript,
as a child of a TextBox.

Code Samples

TextBox:ReleaseFocus

The code shown below will force the client to unfocus the 'TextBox' 5 seconds
after it's selected:

```
local textBox = script.Parent



local function onFocused()



task.wait(5)



textBox:ReleaseFocus()



end



textBox.Focused:Connect(onFocused)
```

Provide feedback

---

Events

Focused

Fires when the [TextBox](/docs/reference/engine/classes/TextBox) gains focus.

TextBox.Focused():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Fires when the [TextBox](/docs/reference/engine/classes/TextBox) gains focus - typically when a client
clicks/taps on a TextBox to begin text entry. This also fires if a
TextBox forces focus on the user.

It can be used alongside [TextBox.FocusLost](/docs/reference/engine/classes/TextBox#FocusLost) to track when a TextBox
gains and loses focus.

See also the [UserInputService.TextBoxFocused](/docs/reference/engine/classes/UserInputService#TextBoxFocused) and
[UserInputService.TextBoxFocusReleased](/docs/reference/engine/classes/UserInputService#TextBoxFocusReleased) for similar functions that
rely on the UserInputService service.

This event will only fire when used in a [LocalScript](/docs/reference/engine/classes/LocalScript).

Code Samples

Focus

This example works when placed in a [LocalScript](/docs/reference/engine/classes/LocalScript) that is the child of a
TextBox. When the TextBox gains focus, the example prints "Focus".

```
local textBox = script.Parent



local function onFocused()



print("Focused")



end



textBox.Focused:Connect(onFocused)
```

Provide feedback

---

FocusLost

Fires when the client lets their focus leave the [TextBox](/docs/reference/engine/classes/TextBox).

TextBox.FocusLost(

enterPressed:[boolean](/docs/luau/booleans), inputThatCausedFocusLoss:[InputObject](/docs/reference/engine/classes/InputObject)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| enterPressed:[boolean](/docs/luau/booleans)  A boolean indicating whether the client pressed Enter to lose focus (true) or not (false). |
| inputThatCausedFocusLoss:[InputObject](/docs/reference/engine/classes/InputObject)  An [InputObject](/docs/reference/engine/classes/InputObject) instance indicating the type of input that caused the TextBox to lose focus. |

Fires when the client lets their focus leave the TextBox, typically when
a client clicks/taps outside of it. This also fires if a TextBox forces
focus on the user.

It can be used alongside [TextBox.Focused](/docs/reference/engine/classes/TextBox#Focused) to track when a TextBox
gains and loses focus.

See also the [UserInputService.TextBoxFocused](/docs/reference/engine/classes/UserInputService#TextBoxFocused) and
[UserInputService.TextBoxFocusReleased](/docs/reference/engine/classes/UserInputService#TextBoxFocusReleased) for similar functions that
rely on the UserInputService service.

This event will only fire when used in a [LocalScript](/docs/reference/engine/classes/LocalScript).

Code Samples

TextBox.FocusLost1

The example shown below will print "Focus was lost because enter was pressed!"
whenever the TextBox loses focus as a result of the enter key being pressed.

```
local gui = script.Parent



local textBox = gui.TextBox



local function focusLost(enterPressed)



if enterPressed then



print("Focus was lost because enter was pressed!")



else



print("Focus was lost without enter being pressed")



end



end



textBox.FocusLost:Connect(focusLost)
```

FocusLost

This example works when placed in a [LocalScript](/docs/reference/engine/classes/LocalScript) that is the child of a
TextBox. When the TextBox loses focus, the example prints either:

1. "Player pressed Enter" - if the TextBox lost focus because the player
   pressed the Enter key. *or*
2. "Player pressed InputObject.*KeyCode*" - where "*KeyCode*" is the
   [InputObject](/docs/reference/engine/classes/InputObject) KeyCode property of the input that caused the TextBox
   to lose focus. For example, pressing the Escape (esc) key to exit TextBox
   focus returns an InputObject instance with the KeyCode
   'InputObject.Escape'.

```
local textBox = script.Parent



local function onFocusLost(enterPressed, inputThatCausedFocusLost)



if enterPressed then



print("Player pressed Enter")



else



print("Player pressed", inputThatCausedFocusLost.KeyCode)



end



end



textBox.FocusLost:Connect(onFocusLost)
```

Provide feedback

---

ReturnPressedFromOnScreenKeyboard

TextBox.ReturnPressedFromOnScreenKeyboard():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Provide feedback

---