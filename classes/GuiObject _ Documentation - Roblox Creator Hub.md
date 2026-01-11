# GuiObject | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/GuiObject
Scraped: 2026-01-11T02:42:25.224676Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- GuiBase2d
- GuiObject
- InputObject
- Instance
- Object
- CanvasGroup
- Frame
- GuiButton
- GuiLabel
- ScrollingFrame
- BasePart
- Size
- Position
- AbsolutePosition
- AbsoluteSize
- AbsoluteRotation
- InputBegan
- InputEnded
- ImageButton
- TextButton
- Activated
- ClickDetector
- DragDetector
- AutoButtonColor
- InputChanged
- GuiObject.Position
- GuiObject.Size
- AutomaticSize
- TextBox
- TextLabel
- GuiObject.BackgroundTransparency
- BorderColor3
- TextBox.TextTransparency
- TextButton.TextTransparency
- TextLabel.TextTransparency
- GuiObject.BackgroundColor3
- GuiObject.BorderSizePixel
- UIStroke
- GuiObjects
- Rotation
- GuiState
- Interactable
- UIGridStyleLayout
- UIListLayout
- UIPageLayout
- SortOrder
- ZIndex
- GuiService.SelectedObject
- Selectable
- NextSelectionUp
- NextSelectionLeft
- NextSelectionRight
- GuiObject.NextSelectionUp
- GuiObject.NextSelectionDown
- GuiObject.NextSelectionLeft
- name
- gets the children
- NextSelectionDown
- GuiObject.AnchorPoint
- GuiBase2d.AbsolutePosition
- AnchorPoint
- ClipsDescendants
- GuiObject.SelectionGained
- GuiObject.SelectionLost
- GuiObject.Selectable
- SelectionImageObject
- PlayerGui.SelectionImageObject
- GuiService:Select()
- GuiBase2d.AbsoluteSize
- SizeConstraint
- ImageLabel.ImageTransparency
- UIGridLayout
- UITableLayout
- ScreenGui
- SurfaceGui
- BillboardGui
- ZIndexBehavior
- LayoutOrder
- screen coordinates of the input
- UserInputService
- UserInputService.InputBegan
- GuiObject.InputEnded
- GuiObject.InputChanged
- UserInputService.InputChanged
- GuiObject.InputBegan
- InputObject.Position
- UserInputService.InputEnded
- GuiObject.MouseLeave
- GuiObject.MouseMoved
- GuiObject.MouseWheelForward
- GuiObject.MouseWheelBackward
- GuiObject.MouseEnter
- Mouse.Move
- Mouse.WheelBackward
- Mouse.WheelForward
- SelectedObject
- SelectionObject
- GuiObject.TouchSwipe
- GuiObject.TouchTap
- GuiObject.TouchPan
- GuiObject.TouchPinch
- GuiObject.TouchRotate
- GuiObject.TouchLongPress
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)
6. /
7. [GuiObject](/docs/reference/engine/classes/GuiObject)

English

Feedback

Engine Class

GuiObject

An abstract class for all 2D user interface objects.

Not Creatable

Not Browsable

---

Summary

Properties

|  |
| --- |
| [Active](#Active):[boolean](/docs/luau/booleans) |
| [AnchorPoint](#AnchorPoint):[Vector2](/docs/reference/engine/datatypes/Vector2) |
| [AutomaticSize](#AutomaticSize):[Enum.AutomaticSize](/docs/reference/engine/enums/AutomaticSize) |
| [BackgroundColor](#BackgroundColor):[BrickColor](/docs/reference/engine/datatypes/BrickColor)  Deprecated |
| [BackgroundColor3](#BackgroundColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [BackgroundTransparency](#BackgroundTransparency):[number](/docs/luau/numbers) |
| [BorderColor](#BorderColor):[BrickColor](/docs/reference/engine/datatypes/BrickColor)  Deprecated |
| [BorderColor3](#BorderColor3):[Color3](/docs/reference/engine/datatypes/Color3) |
| [BorderMode](#BorderMode):[Enum.BorderMode](/docs/reference/engine/enums/BorderMode) |
| [BorderSizePixel](#BorderSizePixel):[number](/docs/luau/numbers) |
| [ClipsDescendants](#ClipsDescendants):[boolean](/docs/luau/booleans) |
| [Draggable](#Draggable):[boolean](/docs/luau/booleans)  Deprecated |
| [GuiState](#GuiState):[Enum.GuiState](/docs/reference/engine/enums/GuiState) |
| [Interactable](#Interactable):[boolean](/docs/luau/booleans) |
| [LayoutOrder](#LayoutOrder):[number](/docs/luau/numbers) |
| [NextSelectionDown](#NextSelectionDown):[GuiObject](/docs/reference/engine/classes/GuiObject) |
| [NextSelectionLeft](#NextSelectionLeft):[GuiObject](/docs/reference/engine/classes/GuiObject) |
| [NextSelectionRight](#NextSelectionRight):[GuiObject](/docs/reference/engine/classes/GuiObject) |
| [NextSelectionUp](#NextSelectionUp):[GuiObject](/docs/reference/engine/classes/GuiObject) |
| [Position](#Position):[UDim2](/docs/reference/engine/datatypes/UDim2) |
| [Rotation](#Rotation):[number](/docs/luau/numbers) |
| [Selectable](#Selectable):[boolean](/docs/luau/booleans) |
| [SelectionImageObject](#SelectionImageObject):[GuiObject](/docs/reference/engine/classes/GuiObject) |
| [SelectionOrder](#SelectionOrder):[number](/docs/luau/numbers) |
| [Size](#Size):[UDim2](/docs/reference/engine/datatypes/UDim2) |
| [SizeConstraint](#SizeConstraint):[Enum.SizeConstraint](/docs/reference/engine/enums/SizeConstraint) |
| [Transparency](#Transparency):[number](/docs/luau/numbers)  Deprecated |
| [Visible](#Visible):[boolean](/docs/luau/booleans) |
| [ZIndex](#ZIndex):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [TweenPosition](#TweenPosition)(endPosition: [UDim2](/docs/reference/engine/datatypes/UDim2),easingDirection: [Enum.EasingDirection](/docs/reference/engine/enums/EasingDirection),easingStyle: [Enum.EasingStyle](/docs/reference/engine/enums/EasingStyle),time: [number](/docs/luau/numbers),override: [boolean](/docs/luau/booleans),callback: [function](/docs/luau/functions)):[boolean](/docs/luau/booleans)  Deprecated |
| [TweenSize](#TweenSize)(endSize: [UDim2](/docs/reference/engine/datatypes/UDim2),easingDirection: [Enum.EasingDirection](/docs/reference/engine/enums/EasingDirection),easingStyle: [Enum.EasingStyle](/docs/reference/engine/enums/EasingStyle),time: [number](/docs/luau/numbers),override: [boolean](/docs/luau/booleans),callback: [function](/docs/luau/functions)):[boolean](/docs/luau/booleans)  Deprecated |
| [TweenSizeAndPosition](#TweenSizeAndPosition)(endSize: [UDim2](/docs/reference/engine/datatypes/UDim2),endPosition: [UDim2](/docs/reference/engine/datatypes/UDim2),easingDirection: [Enum.EasingDirection](/docs/reference/engine/enums/EasingDirection),easingStyle: [Enum.EasingStyle](/docs/reference/engine/enums/EasingStyle),time: [number](/docs/luau/numbers),override: [boolean](/docs/luau/booleans),callback: [function](/docs/luau/functions)):[boolean](/docs/luau/booleans)  Deprecated |

Events

|  |
| --- |
| [DragBegin](#DragBegin)(initialPosition: [UDim2](/docs/reference/engine/datatypes/UDim2)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |
| [DragStopped](#DragStopped)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)  Deprecated |
| [InputBegan](#InputBegan)(input: [InputObject](/docs/reference/engine/classes/InputObject)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [InputChanged](#InputChanged)(input: [InputObject](/docs/reference/engine/classes/InputObject)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [InputEnded](#InputEnded)(input: [InputObject](/docs/reference/engine/classes/InputObject)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MouseEnter](#MouseEnter)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MouseLeave](#MouseLeave)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MouseMoved](#MouseMoved)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MouseWheelBackward](#MouseWheelBackward)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [MouseWheelForward](#MouseWheelForward)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [SelectionGained](#SelectionGained)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [SelectionLost](#SelectionLost)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TouchLongPress](#TouchLongPress)(touchPositions: [Array](/docs/luau/tables#arrays),state: [Enum.UserInputState](/docs/reference/engine/enums/UserInputState)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TouchPan](#TouchPan)(touchPositions: [Array](/docs/luau/tables#arrays),totalTranslation: [Vector2](/docs/reference/engine/datatypes/Vector2),velocity: [Vector2](/docs/reference/engine/datatypes/Vector2),state: [Enum.UserInputState](/docs/reference/engine/enums/UserInputState)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TouchPinch](#TouchPinch)(touchPositions: [Array](/docs/luau/tables#arrays),scale: [number](/docs/luau/numbers),velocity: [number](/docs/luau/numbers),state: [Enum.UserInputState](/docs/reference/engine/enums/UserInputState)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TouchRotate](#TouchRotate)(touchPositions: [Array](/docs/luau/tables#arrays),rotation: [number](/docs/luau/numbers),velocity: [number](/docs/luau/numbers),state: [Enum.UserInputState](/docs/reference/engine/enums/UserInputState)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TouchSwipe](#TouchSwipe)(swipeDirection: [Enum.SwipeDirection](/docs/reference/engine/enums/SwipeDirection),numberOfTouches: [number](/docs/luau/numbers)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [TouchTap](#TouchTap)(touchPositions: [Array](/docs/luau/tables#arrays)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

12 inherited from [GuiBase2d](/docs/reference/engine/classes/GuiBase2d)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[CanvasGroup](/docs/reference/engine/classes/CanvasGroup), [Frame](/docs/reference/engine/classes/Frame), [GuiButton](/docs/reference/engine/classes/GuiButton), [GuiLabel](/docs/reference/engine/classes/GuiLabel), [ScrollingFrame](/docs/reference/engine/classes/ScrollingFrame), Show more...

[GuiObject](/docs/reference/engine/classes/GuiObject) is an abstract class (much like [BasePart](/docs/reference/engine/classes/BasePart)) for a 2D
user interface object. It defines all the properties relating to the display
of a graphical user interface (GUI) object such as [Size](/docs/reference/engine/classes/GuiObject#Size)
and [Position](/docs/reference/engine/classes/GuiObject#Position). It also has some useful read‑only
properties like [AbsolutePosition](/docs/reference/engine/classes/GuiObject#AbsolutePosition),
[AbsoluteSize](/docs/reference/engine/classes/GuiObject#AbsoluteSize), and
[AbsoluteRotation](/docs/reference/engine/classes/GuiObject#AbsoluteRotation).

To manipulate the layout of GUI objects in special ways, you can use a layout
structure such as [list/flex](/docs/ui/list-flex-layouts) or
[grid](/docs/ui/grid-table-layouts), and you can style them beyond their
core properties through
[appearance modifiers](/docs/ui/appearance-modifiers).

Although it's possible to detect mouse button events on any GUI object using
[InputBegan](/docs/reference/engine/classes/GuiObject#InputBegan) and
[InputEnded](/docs/reference/engine/classes/GuiObject#InputEnded), only [ImageButton](/docs/reference/engine/classes/ImageButton) and
[TextButton](/docs/reference/engine/classes/TextButton) have convenient dedicated events such as
[Activated](/docs/reference/engine/classes/TextButton#Activated) to detect click/press.

---

API Reference

Properties

Active

Read Parallel

Determines whether this UI element sinks input.

GuiObject.Active:[boolean](/docs/luau/booleans)

This property determines whether the [GuiObject](/docs/reference/engine/classes/GuiObject) will sink input to
3D space, such as underlying models with a [ClickDetector](/docs/reference/engine/classes/ClickDetector) class
like [DragDetector](/docs/reference/engine/classes/DragDetector).

For [GuiButton](/docs/reference/engine/classes/GuiButton) objects ([ImageButton](/docs/reference/engine/classes/ImageButton) and
[TextButton](/docs/reference/engine/classes/TextButton)), this property determines whether
[Activated](/docs/reference/engine/classes/GuiButton#Activated) fires
([AutoButtonColor](/docs/reference/engine/classes/GuiButton#AutoButtonColor) will still work for
those as well). The events [InputBegan](/docs/reference/engine/classes/GuiObject#InputBegan),
[InputChanged](/docs/reference/engine/classes/GuiObject#InputChanged), and
[InputEnded](/docs/reference/engine/classes/GuiObject#InputEnded) work as normal no matter the value
of this property.

Code Samples

TextButton Active Debounce

This code sample demonstrates the usage of the Active property as a debounce
for the Activated event.

```
-- Place this LocalScript within a TextButton (or ImageButton)



local textButton = script.Parent



textButton.Text = "Click me"



textButton.Active = true



local function onActivated()



-- This acts like a debounce



textButton.Active = false



-- Count backwards from 5



for i = 5, 1, -1 do



textButton.Text = "Time: " .. i



task.wait(1)



end



textButton.Text = "Click me"



textButton.Active = true



end



textButton.Activated:Connect(onActivated)
```

Provide feedback

---

AnchorPoint

Read Parallel

Determines the origin point of a [GuiObject](/docs/reference/engine/classes/GuiObject), relative to its
absolute size.

GuiObject.AnchorPoint:[Vector2](/docs/reference/engine/datatypes/Vector2)

This property determines the origin point of a [GuiObject](/docs/reference/engine/classes/GuiObject), relative
to its absolute size. The origin point determines from where the element
is positioned (through [GuiObject.Position](/docs/reference/engine/classes/GuiObject#Position)) and from which the
rendered [GuiObject.Size](/docs/reference/engine/classes/GuiObject#Size) expands.

See [here](/docs/ui/position-and-size#anchorpoint) for illustrated
diagrams and details.

Code Samples

AnchorPoint Demo

This code sample moves a UI element to different sides of the parent element.
It starts at the top-left and ends at the bottom-right. Paste into a
LocalScript in a Frame, within a ScreenGui.

```
local guiObject = script.Parent



while true do



-- Top-left



guiObject.AnchorPoint = Vector2.new(0, 0)



guiObject.Position = UDim2.new(0, 0, 0, 0)



task.wait(1)



-- Top



guiObject.AnchorPoint = Vector2.new(0.5, 0)



guiObject.Position = UDim2.new(0.5, 0, 0, 0)



task.wait(1)



-- Top-right



guiObject.AnchorPoint = Vector2.new(1, 0)



guiObject.Position = UDim2.new(1, 0, 0, 0)



task.wait(1)



-- Left



guiObject.AnchorPoint = Vector2.new(0, 0.5)



guiObject.Position = UDim2.new(0, 0, 0.5, 0)



task.wait(1)



-- Dead center



guiObject.AnchorPoint = Vector2.new(0.5, 0.5)



guiObject.Position = UDim2.new(0.5, 0, 0.5, 0)



task.wait(1)



-- Right



guiObject.AnchorPoint = Vector2.new(1, 0.5)



guiObject.Position = UDim2.new(1, 0, 0.5, 0)



task.wait(1)



-- Bottom-left



guiObject.AnchorPoint = Vector2.new(0, 1)



guiObject.Position = UDim2.new(0, 0, 1, 0)



task.wait(1)



-- Bottom



guiObject.AnchorPoint = Vector2.new(0.5, 1)



guiObject.Position = UDim2.new(0.5, 0, 1, 0)



task.wait(1)



-- Bottom-right



guiObject.AnchorPoint = Vector2.new(1, 1)



guiObject.Position = UDim2.new(1, 0, 1, 0)



task.wait(1)



end
```

Provide feedback

---

AutomaticSize

Read Parallel

Determines whether resizing occurs based on child content.

GuiObject.AutomaticSize:[Enum.AutomaticSize](/docs/reference/engine/enums/AutomaticSize)

This property is used to automatically size parent UI objects based on the
size of its descendants. You can use this property to dynamically add text
and other content to a UI object at edit or run time, and the size will
adjust to fit that content.

When [AutomaticSize](/docs/reference/engine/classes/GuiObject#AutomaticSize) is set to an
[Enum.AutomaticSize](/docs/reference/engine/enums/AutomaticSize) value to anything other than
[None](/docs/reference/engine/enums/AutomaticSize), this UI object may resize depending on its
child content.

For more information on how to use this property and how it works, please
see [here](/docs/ui/size-modifiers#automatic-sizing).

Code Samples

LocalScript in a ScreenGui

The following script creates an automatically-sized parent frame with
aUIListLayout, then it inserts several automatically-sized TextLabel
objects. Note how the parent UIListLayout automatically resizes to fit its
child content and the labels automatically resize to fit their text content.
This script can be parented to a ScreenGui.

```
-- Array of text labels/fonts/sizes to output



local labelArray = {



{ text = "Lorem", font = Enum.Font.Creepster, size = 50 },



{ text = "ipsum", font = Enum.Font.IndieFlower, size = 35 },



{ text = "dolor", font = Enum.Font.Antique, size = 55 },



{ text = "sit", font = Enum.Font.SpecialElite, size = 65 },



{ text = "amet", font = Enum.Font.FredokaOne, size = 40 },



}



-- Create an automatically-sized parent frame



local parentFrame = Instance.new("Frame")



parentFrame.AutomaticSize = Enum.AutomaticSize.XY



parentFrame.BackgroundColor3 = Color3.fromRGB(90, 90, 90)



parentFrame.Size = UDim2.fromOffset(25, 100)



parentFrame.Position = UDim2.fromScale(0.1, 0.1)



parentFrame.Parent = script.Parent



-- Add a list layout



local listLayout = Instance.new("UIListLayout")



listLayout.Padding = UDim.new(0, 5)



listLayout.Parent = parentFrame



-- Set rounded corners and padding for visual aesthetics



local roundedCornerParent = Instance.new("UICorner")



roundedCornerParent.Parent = parentFrame



local uiPaddingParent = Instance.new("UIPadding")



uiPaddingParent.PaddingTop = UDim.new(0, 5)



uiPaddingParent.PaddingLeft = UDim.new(0, 5)



uiPaddingParent.PaddingRight = UDim.new(0, 5)



uiPaddingParent.PaddingBottom = UDim.new(0, 5)



uiPaddingParent.Parent = parentFrame



for i = 1, #labelArray do



-- Create an automatically-sized text label from array



local childLabel = Instance.new("TextLabel")



childLabel.AutomaticSize = Enum.AutomaticSize.XY



childLabel.Size = UDim2.fromOffset(75, 15)



childLabel.Text = labelArray[i]["text"]



childLabel.Font = labelArray[i]["font"]



childLabel.TextSize = labelArray[i]["size"]



childLabel.TextColor3 = Color3.new(1, 1, 1)



childLabel.Parent = parentFrame



-- Visual aesthetics



local roundedCorner = Instance.new("UICorner")



roundedCorner.Parent = childLabel



local uiPadding = Instance.new("UIPadding")



uiPadding.PaddingTop = UDim.new(0, 5)



uiPadding.PaddingLeft = UDim.new(0, 5)



uiPadding.PaddingRight = UDim.new(0, 5)



uiPadding.PaddingBottom = UDim.new(0, 5)



uiPadding.Parent = childLabel



task.wait(2)



end
```

Provide feedback

---

BackgroundColor

Deprecated

Show details

---

BackgroundColor3

Read Parallel

Determines the [GuiObject](/docs/reference/engine/classes/GuiObject) background color.

GuiObject.BackgroundColor3:[Color3](/docs/reference/engine/datatypes/Color3)

This property determines the color of a [GuiObject](/docs/reference/engine/classes/GuiObject) background (the
fill color). If your element contains text, such as a [TextBox](/docs/reference/engine/classes/TextBox),
[TextButton](/docs/reference/engine/classes/TextButton), or [TextLabel](/docs/reference/engine/classes/TextLabel), make sure the color of your
background contrasts the text's color.

Another property that determines the visual properties of the background
is [GuiObject.BackgroundTransparency](/docs/reference/engine/classes/GuiObject#BackgroundTransparency); if this is set to 1,
neither the background nor the border will render.

See also [BorderColor3](/docs/reference/engine/classes/GuiObject#BorderColor3).

Code Samples

Rainbow Frame

This code sample causes a parent Frame to loop through all colors of the
rainbow using Color3.fromHSV.

```
-- Put this code in a LocalScript in a Frame



local frame = script.Parent



while true do



for hue = 0, 255, 4 do



-- HSV = hue, saturation, value



-- If we loop from 0 to 1 repeatedly, we get a rainbow!



frame.BorderColor3 = Color3.fromHSV(hue / 256, 1, 1)



frame.BackgroundColor3 = Color3.fromHSV(hue / 256, 0.5, 0.8)



task.wait()



end



end
```

Provide feedback

---

BackgroundTransparency

Read Parallel

Determines the transparency of the [GuiObject](/docs/reference/engine/classes/GuiObject) background and
border.

GuiObject.BackgroundTransparency:[number](/docs/luau/numbers)

This property determines the transparency of the [GuiObject](/docs/reference/engine/classes/GuiObject)
background and border. It does not, however, determine the transparency of
text if the GUI is a [TextBox](/docs/reference/engine/classes/TextBox), [TextButton](/docs/reference/engine/classes/TextButton), or
[TextLabel](/docs/reference/engine/classes/TextLabel); text transparency is determined
[TextBox.TextTransparency](/docs/reference/engine/classes/TextBox#TextTransparency), [TextButton.TextTransparency](/docs/reference/engine/classes/TextButton#TextTransparency), and
[TextLabel.TextTransparency](/docs/reference/engine/classes/TextLabel#TextTransparency) respectively.

If this property is set to 1, neither the background nor the border will
render and the GUI background will be completely transparent.

Provide feedback

---

BorderColor

Deprecated

Show details

---

BorderColor3

Read Parallel

Determines the color of the [GuiObject](/docs/reference/engine/classes/GuiObject) border.

GuiObject.BorderColor3:[Color3](/docs/reference/engine/datatypes/Color3)

Determines the color of the [GuiObject](/docs/reference/engine/classes/GuiObject) rectangular border (also
known as the stroke color). This is separate from the object's
[GuiObject.BackgroundColor3](/docs/reference/engine/classes/GuiObject#BackgroundColor3). You will not be able to see the
object's border if its [GuiObject.BorderSizePixel](/docs/reference/engine/classes/GuiObject#BorderSizePixel) property is set
to 0.

Note that the [UIStroke](/docs/reference/engine/classes/UIStroke) component allows for more advanced border
effects.

Code Samples

Button Highlight

This code sample causes the border of a parent GuiObject to highlight when the
user hovers their mouse over the element.

```
-- Put me inside some GuiObject, preferrably an ImageButton/TextButton



local button = script.Parent



local function onEnter()



button.BorderSizePixel = 2



button.BorderColor3 = Color3.new(1, 1, 0) -- Yellow



end



local function onLeave()



button.BorderSizePixel = 1



button.BorderColor3 = Color3.new(0, 0, 0) -- Black



end



-- Connect events



button.MouseEnter:Connect(onEnter)



button.MouseLeave:Connect(onLeave)



-- Our default state is "not hovered"



onLeave()
```

Provide feedback

---

BorderMode

Read Parallel

Determines in what manner the [GuiObject](/docs/reference/engine/classes/GuiObject) border is laid out
relative to its dimensions.

GuiObject.BorderMode:[Enum.BorderMode](/docs/reference/engine/enums/BorderMode)

This property determines in what manner the [GuiObject](/docs/reference/engine/classes/GuiObject) border is
laid out relative to its dimensions using the enum of the same name,
[Enum.BorderMode](/docs/reference/engine/enums/BorderMode).

Note that [UIStroke](/docs/reference/engine/classes/UIStroke) can override this property and allow for more
advanced border effects.

Provide feedback

---

BorderSizePixel

Read Parallel

Determines the pixel width of the [GuiObject](/docs/reference/engine/classes/GuiObject) border.

GuiObject.BorderSizePixel:[number](/docs/luau/numbers)

This property determines how wide the [GuiObject](/docs/reference/engine/classes/GuiObject) border renders, in
pixels. Setting this to 0 disables the border altogether.

Note that [UIStroke](/docs/reference/engine/classes/UIStroke) can override this property and allow for more
advanced border effects.

Code Samples

Button Highlight

This code sample causes the border of a parent GuiObject to highlight when the
user hovers their mouse over the element.

```
-- Put me inside some GuiObject, preferrably an ImageButton/TextButton



local button = script.Parent



local function onEnter()



button.BorderSizePixel = 2



button.BorderColor3 = Color3.new(1, 1, 0) -- Yellow



end



local function onLeave()



button.BorderSizePixel = 1



button.BorderColor3 = Color3.new(0, 0, 0) -- Black



end



-- Connect events



button.MouseEnter:Connect(onEnter)



button.MouseLeave:Connect(onLeave)



-- Our default state is "not hovered"



onLeave()
```

Provide feedback

---

ClipsDescendants

Read Parallel

Determines if descendant [GuiObjects](/docs/reference/engine/classes/GuiObject) outside of the
bounds of a parent GUI element should render.

GuiObject.ClipsDescendants:[boolean](/docs/luau/booleans)

This property determines if the [GuiObject](/docs/reference/engine/classes/GuiObject) will clip (make
invisible) any portion of descendant GUI elements that would otherwise
render outside the bounds of the rectangle.

Note that [Rotation](/docs/reference/engine/classes/GuiObject#Rotation) isn't supported by this
property. If this or any ancestor GUI has a non‑zero
[Rotation](/docs/reference/engine/classes/GuiObject#Rotation), this property is ignored and
descendant GUI elements will be rendered regardless of this property's
value.

Provide feedback

---

Draggable

Deprecated

Show details

---

GuiState

Read Only

Not Replicated

Read Parallel

Determines whether the player's mouse is being actively pressed on the
[GuiObject](/docs/reference/engine/classes/GuiObject) or not.

GuiObject.GuiState:[Enum.GuiState](/docs/reference/engine/enums/GuiState)

When the player's finger is being tapped and held on the
[GuiObject](/docs/reference/engine/classes/GuiObject), the [GuiState](/docs/reference/engine/classes/GuiObject#GuiState) of the
[GuiObject](/docs/reference/engine/classes/GuiObject) will be set to [Press](/docs/reference/engine/enums/GuiState#Press). Similarly,
When the player's finger is being released from the [GuiObject](/docs/reference/engine/classes/GuiObject), the
[GuiState](/docs/reference/engine/classes/GuiObject#GuiState) of the [GuiObject](/docs/reference/engine/classes/GuiObject) will be set
to [Idle](/docs/reference/engine/enums/GuiState#Idle), and when
[Interactable](/docs/reference/engine/classes/GuiObject#Interactable) is turned off on the
[GuiObject](/docs/reference/engine/classes/GuiObject), the Class.GuiState of the [GuiObject](/docs/reference/engine/classes/GuiObject) will be
set to [NonInteractable](/docs/reference/engine/enums/GuiState#NonInteractable).

Provide feedback

---

Interactable

Read Parallel

Determines whether the [GuiButton](/docs/reference/engine/classes/GuiButton) can be interacted with or not, or
if the [GuiState](/docs/reference/engine/enums/GuiState) of the [GuiObject](/docs/reference/engine/classes/GuiObject) is changing or
not.

GuiObject.Interactable:[boolean](/docs/luau/booleans)

Determines whether the [GuiButton](/docs/reference/engine/classes/GuiButton) can be interacted with or not, or
if the [GuiState](/docs/reference/engine/enums/GuiState) of the [GuiObject](/docs/reference/engine/classes/GuiObject) is changing or
not.

On a [GuiButton](/docs/reference/engine/classes/GuiButton):

* When the [Interactable](/docs/reference/engine/classes/GuiObject#Interactable) setting on the
  [GuiButton](/docs/reference/engine/classes/GuiButton) is set to false, the [GuiButton](/docs/reference/engine/classes/GuiButton) will no
  longer be able to be pressed or clicked, and the
  [GuiState](/docs/reference/engine/classes/GuiObject#GuiState) will be constantly set to
  [NonInteractable](/docs/reference/engine/enums/GuiState#NonInteractable).
* When the [Interactable](/docs/reference/engine/classes/GuiObject#Interactable) setting on the
  [GuiButton](/docs/reference/engine/classes/GuiButton) is set to true, the [GuiButton](/docs/reference/engine/classes/GuiButton) will behave
  normally again and the [GuiState](/docs/reference/engine/classes/GuiObject#GuiState) will behave
  normally.

On a [GuiObject](/docs/reference/engine/classes/GuiObject):

* When the [Interactable](/docs/reference/engine/classes/GuiObject#Interactable) setting on the
  [GuiButton](/docs/reference/engine/classes/GuiButton) is set to false, the
  [GuiState](/docs/reference/engine/classes/GuiObject#GuiState) will be constantly set to
  [NonInteractable](/docs/reference/engine/enums/GuiState#NonInteractable).
* When the [Interactable](/docs/reference/engine/classes/GuiObject#Interactable) setting on the
  [GuiButton](/docs/reference/engine/classes/GuiButton) is set to true, the
  [GuiState](/docs/reference/engine/classes/GuiObject#GuiState) will behave normally again.

Provide feedback

---

LayoutOrder

Read Parallel

Controls the sort order of the [GuiObject](/docs/reference/engine/classes/GuiObject) when used with a
[UIGridStyleLayout](/docs/reference/engine/classes/UIGridStyleLayout).

GuiObject.LayoutOrder:[number](/docs/luau/numbers)

This property controls the sorting order of the [GuiObject](/docs/reference/engine/classes/GuiObject) when
using a [UIGridStyleLayout](/docs/reference/engine/classes/UIGridStyleLayout) (such as [UIListLayout](/docs/reference/engine/classes/UIListLayout) or
[UIPageLayout](/docs/reference/engine/classes/UIPageLayout)) with [SortOrder](/docs/reference/engine/classes/UIGridStyleLayout#SortOrder)
set to [Enum.SortOrder.LayoutOrder](/docs/reference/engine/enums/SortOrder#LayoutOrder). It has no functionality if the object
does not have a sibling UI layout structure.

[GuiObjects](/docs/reference/engine/classes/GuiObject) are sorted in ascending order where lower
values take priority over higher values. Objects with equal values fall
back to the order they were added in.

If you are unsure if you'll need to add an element between two existing
elements in the future, it's a good practice to use multiples of 100
(0, 100, 200, etc.). This ensures a large gap of layout order values
which you can use for elements ordered in-between other elements.

See also [ZIndex](/docs/reference/engine/classes/GuiObject#ZIndex) which determines the object's
rendering order instead of sorting order.

Provide feedback

---

NextSelectionDown

Read Parallel

Sets the [GuiObject](/docs/reference/engine/classes/GuiObject) which will be selected when the gamepad
selector is moved downward.

GuiObject.NextSelectionDown:[GuiObject](/docs/reference/engine/classes/GuiObject)

This property sets the [GuiObject](/docs/reference/engine/classes/GuiObject) selected when the user moves the
[gamepad](/docs/input/gamepad) selector downward. If this property
is empty, moving the gamepad downward will not change the selected GUI.

Moving the gamepad selector downward sets the
[GuiService.SelectedObject](/docs/reference/engine/classes/GuiService#SelectedObject) to this object unless the GUI is not
[Selectable](/docs/reference/engine/classes/GuiObject#Selectable). Note that this property can be
set to a GUI element even if it is not
[Selectable](/docs/reference/engine/classes/GuiObject#Selectable), so you should ensure that the
value of a GUI's selectable property matches your expected behavior.

See also [NextSelectionUp](/docs/reference/engine/classes/GuiObject#NextSelectionUp),
[NextSelectionLeft](/docs/reference/engine/classes/GuiObject#NextSelectionLeft), and
[NextSelectionRight](/docs/reference/engine/classes/GuiObject#NextSelectionRight).

Code Samples

Creating a Gamepad Selection Grid

This example demonstrates how to enable Gamepad navigation through a grid of
GuiObject|GUI elements without manually having to connect the
[GuiObject.NextSelectionUp](/docs/reference/engine/classes/GuiObject#NextSelectionUp), [GuiObject.NextSelectionDown](/docs/reference/engine/classes/GuiObject#NextSelectionDown), and
GuiObject|NextSelectionRight, and [GuiObject.NextSelectionLeft](/docs/reference/engine/classes/GuiObject#NextSelectionLeft)
properties for every element in the grid.

Note that this code sample assumes your UIGridLayout is sorted by
[name](/docs/reference/engine/classes/UIGridLayout#SortOrder), where elements are named in successive
numerical order.

The code relies on this to set the NextSelection properties for all
GuiObjects in the same level as the UIGridLayout. In our example, the
UIGridLayoutObject and GUI elements within the grid are all children of a
Frame named *"Container"*. The code
[gets the children](/docs/reference/engine/classes/Instance#GetChildren) of *"Container"* and loops
through each child. Children that are not GuiObjects are ignored. For each GUI
element, the code attempts to assigned the NextSelection properties using the
following logic:

1. Starting with 1, the name of all GUI elements match their position in the
   grid
2. Left: The item to the left will always be numbered 1 less than the current
   element
3. Right: The item to the left will always be numbered 1 more than the current
   element
4. Up: The item above (up) will always be number of GUIs in a row 1 less than
   the current element
5. Down: The item below (down) will always be the number of GUIs in a row more
   than the current element This logic also allows for the GUI elements at the
   begging and end of rows (excluding the first and last element) to wrap
   around to the next and previous rows. If an element doesn't exist to the
   left, right, up, or down, the NextSelection will remain nil and moving the
   Gamepad selector in the direction will not change the selected GUI.

This example also contains code to test the grid using the arrow keys (Up,
Down, Left, Right) of your keyboard instead of a gamepad, just in case you
don't have a gamepad to test with. This portion of code initially selects the
element named *"1"* by assigning it to the [GuiService.SelectedObject](/docs/reference/engine/classes/GuiService#SelectedObject)
property.

```
-- Setup the Gamepad selection grid using the code below



local container = script.Parent:FindFirstChild("Container")



local grid = container:GetChildren()



local rowSize = container:FindFirstChild("UIGridLayout").FillDirectionMaxCells



for _, gui in pairs(grid) do



if gui:IsA("GuiObject") then



local pos = gui.Name



-- Left edge



gui.NextSelectionLeft = container:FindFirstChild(pos - 1)



-- Right edge



gui.NextSelectionRight = container:FindFirstChild(pos + 1)



-- Above



gui.NextSelectionUp = container:FindFirstChild(pos - rowSize)



-- Below



gui.NextSelectionDown = container:FindFirstChild(pos + rowSize)



end



end



-- Test the Gamepad selection grid using the code below



local GuiService = game:GetService("GuiService")



local UserInputService = game:GetService("UserInputService")



GuiService.SelectedObject = container:FindFirstChild("1")



function updateSelection(input)



if input.UserInputType == Enum.UserInputType.Keyboard then



local key = input.KeyCode



local selectedObject = GuiService.SelectedObject



if not selectedObject then



return



end



if key == Enum.KeyCode.Up then



if not selectedObject.NextSelectionUp then



GuiService.SelectedObject = selectedObject



end



elseif key == Enum.KeyCode.Down then



if not selectedObject.NextSelectionDown then



GuiService.SelectedObject = selectedObject



end



elseif key == Enum.KeyCode.Left then



if not selectedObject.NextSelectionLeft then



GuiService.SelectedObject = selectedObject



end



elseif key == Enum.KeyCode.Right then



if not selectedObject.NextSelectionRight then



GuiService.SelectedObject = selectedObject



end



end



end



end



UserInputService.InputBegan:Connect(updateSelection)
```

Provide feedback

---

NextSelectionLeft

Read Parallel

Sets the [GuiObject](/docs/reference/engine/classes/GuiObject) which will be selected when the gamepad
selector is moved to the left.

GuiObject.NextSelectionLeft:[GuiObject](/docs/reference/engine/classes/GuiObject)

This property sets the [GuiObject](/docs/reference/engine/classes/GuiObject) selected when the user moves the
[gamepad](/docs/input/gamepad) selector to the left. If this
property is empty, moving the gamepad to the left will not change the
selected GUI.

Moving the gamepad selector to the left sets the
[GuiService.SelectedObject](/docs/reference/engine/classes/GuiService#SelectedObject) to this object unless the GUI is not
[Selectable](/docs/reference/engine/classes/GuiObject#Selectable). Note that this property can be
set to a GUI element even if it is not
[Selectable](/docs/reference/engine/classes/GuiObject#Selectable), so you should ensure that the
value of a GUI's selectable property matches your expected behavior.

See also [NextSelectionUp](/docs/reference/engine/classes/GuiObject#NextSelectionUp),
[NextSelectionDown](/docs/reference/engine/classes/GuiObject#NextSelectionDown), and
[NextSelectionRight](/docs/reference/engine/classes/GuiObject#NextSelectionRight).

Code Samples

Creating a Gamepad Selection Grid

This example demonstrates how to enable Gamepad navigation through a grid of
GuiObject|GUI elements without manually having to connect the
[GuiObject.NextSelectionUp](/docs/reference/engine/classes/GuiObject#NextSelectionUp), [GuiObject.NextSelectionDown](/docs/reference/engine/classes/GuiObject#NextSelectionDown), and
GuiObject|NextSelectionRight, and [GuiObject.NextSelectionLeft](/docs/reference/engine/classes/GuiObject#NextSelectionLeft)
properties for every element in the grid.

Note that this code sample assumes your UIGridLayout is sorted by
[name](/docs/reference/engine/classes/UIGridLayout#SortOrder), where elements are named in successive
numerical order.

The code relies on this to set the NextSelection properties for all
GuiObjects in the same level as the UIGridLayout. In our example, the
UIGridLayoutObject and GUI elements within the grid are all children of a
Frame named *"Container"*. The code
[gets the children](/docs/reference/engine/classes/Instance#GetChildren) of *"Container"* and loops
through each child. Children that are not GuiObjects are ignored. For each GUI
element, the code attempts to assigned the NextSelection properties using the
following logic:

1. Starting with 1, the name of all GUI elements match their position in the
   grid
2. Left: The item to the left will always be numbered 1 less than the current
   element
3. Right: The item to the left will always be numbered 1 more than the current
   element
4. Up: The item above (up) will always be number of GUIs in a row 1 less than
   the current element
5. Down: The item below (down) will always be the number of GUIs in a row more
   than the current element This logic also allows for the GUI elements at the
   begging and end of rows (excluding the first and last element) to wrap
   around to the next and previous rows. If an element doesn't exist to the
   left, right, up, or down, the NextSelection will remain nil and moving the
   Gamepad selector in the direction will not change the selected GUI.

This example also contains code to test the grid using the arrow keys (Up,
Down, Left, Right) of your keyboard instead of a gamepad, just in case you
don't have a gamepad to test with. This portion of code initially selects the
element named *"1"* by assigning it to the [GuiService.SelectedObject](/docs/reference/engine/classes/GuiService#SelectedObject)
property.

```
-- Setup the Gamepad selection grid using the code below



local container = script.Parent:FindFirstChild("Container")



local grid = container:GetChildren()



local rowSize = container:FindFirstChild("UIGridLayout").FillDirectionMaxCells



for _, gui in pairs(grid) do



if gui:IsA("GuiObject") then



local pos = gui.Name



-- Left edge



gui.NextSelectionLeft = container:FindFirstChild(pos - 1)



-- Right edge



gui.NextSelectionRight = container:FindFirstChild(pos + 1)



-- Above



gui.NextSelectionUp = container:FindFirstChild(pos - rowSize)



-- Below



gui.NextSelectionDown = container:FindFirstChild(pos + rowSize)



end



end



-- Test the Gamepad selection grid using the code below



local GuiService = game:GetService("GuiService")



local UserInputService = game:GetService("UserInputService")



GuiService.SelectedObject = container:FindFirstChild("1")



function updateSelection(input)



if input.UserInputType == Enum.UserInputType.Keyboard then



local key = input.KeyCode



local selectedObject = GuiService.SelectedObject



if not selectedObject then



return



end



if key == Enum.KeyCode.Up then



if not selectedObject.NextSelectionUp then



GuiService.SelectedObject = selectedObject



end



elseif key == Enum.KeyCode.Down then



if not selectedObject.NextSelectionDown then



GuiService.SelectedObject = selectedObject



end



elseif key == Enum.KeyCode.Left then



if not selectedObject.NextSelectionLeft then



GuiService.SelectedObject = selectedObject



end



elseif key == Enum.KeyCode.Right then



if not selectedObject.NextSelectionRight then



GuiService.SelectedObject = selectedObject



end



end



end



end



UserInputService.InputBegan:Connect(updateSelection)
```

Provide feedback

---

NextSelectionRight

Read Parallel

Sets the [GuiObject](/docs/reference/engine/classes/GuiObject) which will be selected when the gamepad
selector is moved to the right.

GuiObject.NextSelectionRight:[GuiObject](/docs/reference/engine/classes/GuiObject)

This property sets the [GuiObject](/docs/reference/engine/classes/GuiObject) selected when the user moves the
[gamepad](/docs/input/gamepad) selector to the right. If this
property is empty, moving the gamepad to the right will not change the
selected GUI.

Moving the gamepad selector to the right sets the
[GuiService.SelectedObject](/docs/reference/engine/classes/GuiService#SelectedObject) to this object unless the GUI is not
[Selectable](/docs/reference/engine/classes/GuiObject#Selectable). Note that this property can be
set to a GUI element even if it is not
[Selectable](/docs/reference/engine/classes/GuiObject#Selectable), so you should ensure that the
value of a GUI's selectable property matches your expected behavior.

See also [NextSelectionUp](/docs/reference/engine/classes/GuiObject#NextSelectionUp),
[NextSelectionDown](/docs/reference/engine/classes/GuiObject#NextSelectionDown), and
[NextSelectionLeft](/docs/reference/engine/classes/GuiObject#NextSelectionLeft).

Code Samples

Creating a Gamepad Selection Grid

This example demonstrates how to enable Gamepad navigation through a grid of
GuiObject|GUI elements without manually having to connect the
[GuiObject.NextSelectionUp](/docs/reference/engine/classes/GuiObject#NextSelectionUp), [GuiObject.NextSelectionDown](/docs/reference/engine/classes/GuiObject#NextSelectionDown), and
GuiObject|NextSelectionRight, and [GuiObject.NextSelectionLeft](/docs/reference/engine/classes/GuiObject#NextSelectionLeft)
properties for every element in the grid.

Note that this code sample assumes your UIGridLayout is sorted by
[name](/docs/reference/engine/classes/UIGridLayout#SortOrder), where elements are named in successive
numerical order.

The code relies on this to set the NextSelection properties for all
GuiObjects in the same level as the UIGridLayout. In our example, the
UIGridLayoutObject and GUI elements within the grid are all children of a
Frame named *"Container"*. The code
[gets the children](/docs/reference/engine/classes/Instance#GetChildren) of *"Container"* and loops
through each child. Children that are not GuiObjects are ignored. For each GUI
element, the code attempts to assigned the NextSelection properties using the
following logic:

1. Starting with 1, the name of all GUI elements match their position in the
   grid
2. Left: The item to the left will always be numbered 1 less than the current
   element
3. Right: The item to the left will always be numbered 1 more than the current
   element
4. Up: The item above (up) will always be number of GUIs in a row 1 less than
   the current element
5. Down: The item below (down) will always be the number of GUIs in a row more
   than the current element This logic also allows for the GUI elements at the
   begging and end of rows (excluding the first and last element) to wrap
   around to the next and previous rows. If an element doesn't exist to the
   left, right, up, or down, the NextSelection will remain nil and moving the
   Gamepad selector in the direction will not change the selected GUI.

This example also contains code to test the grid using the arrow keys (Up,
Down, Left, Right) of your keyboard instead of a gamepad, just in case you
don't have a gamepad to test with. This portion of code initially selects the
element named *"1"* by assigning it to the [GuiService.SelectedObject](/docs/reference/engine/classes/GuiService#SelectedObject)
property.

```
-- Setup the Gamepad selection grid using the code below



local container = script.Parent:FindFirstChild("Container")



local grid = container:GetChildren()



local rowSize = container:FindFirstChild("UIGridLayout").FillDirectionMaxCells



for _, gui in pairs(grid) do



if gui:IsA("GuiObject") then



local pos = gui.Name



-- Left edge



gui.NextSelectionLeft = container:FindFirstChild(pos - 1)



-- Right edge



gui.NextSelectionRight = container:FindFirstChild(pos + 1)



-- Above



gui.NextSelectionUp = container:FindFirstChild(pos - rowSize)



-- Below



gui.NextSelectionDown = container:FindFirstChild(pos + rowSize)



end



end



-- Test the Gamepad selection grid using the code below



local GuiService = game:GetService("GuiService")



local UserInputService = game:GetService("UserInputService")



GuiService.SelectedObject = container:FindFirstChild("1")



function updateSelection(input)



if input.UserInputType == Enum.UserInputType.Keyboard then



local key = input.KeyCode



local selectedObject = GuiService.SelectedObject



if not selectedObject then



return



end



if key == Enum.KeyCode.Up then



if not selectedObject.NextSelectionUp then



GuiService.SelectedObject = selectedObject



end



elseif key == Enum.KeyCode.Down then



if not selectedObject.NextSelectionDown then



GuiService.SelectedObject = selectedObject



end



elseif key == Enum.KeyCode.Left then



if not selectedObject.NextSelectionLeft then



GuiService.SelectedObject = selectedObject



end



elseif key == Enum.KeyCode.Right then



if not selectedObject.NextSelectionRight then



GuiService.SelectedObject = selectedObject



end



end



end



end



UserInputService.InputBegan:Connect(updateSelection)
```

Provide feedback

---

NextSelectionUp

Read Parallel

Sets the [GuiObject](/docs/reference/engine/classes/GuiObject) which will be selected when the gamepad
selector is moved upward.

GuiObject.NextSelectionUp:[GuiObject](/docs/reference/engine/classes/GuiObject)

This property sets the [GuiObject](/docs/reference/engine/classes/GuiObject) selected when the user moves the
[gamepad](/docs/input/gamepad) selector upward. If this property is
empty, moving the gamepad upward will not change the selected GUI.

Moving the gamepad selector upward sets the
[GuiService.SelectedObject](/docs/reference/engine/classes/GuiService#SelectedObject) to this object unless the GUI is not
[Selectable](/docs/reference/engine/classes/GuiObject#Selectable). Note that this property can be
set to a GUI element even if it is not
[Selectable](/docs/reference/engine/classes/GuiObject#Selectable), so you should ensure that the
value of a GUI's selectable property matches your expected behavior.

See also [NextSelectionDown](/docs/reference/engine/classes/GuiObject#NextSelectionDown),
[NextSelectionLeft](/docs/reference/engine/classes/GuiObject#NextSelectionLeft),
[NextSelectionRight](/docs/reference/engine/classes/GuiObject#NextSelectionRight).

Code Samples

Creating a Gamepad Selection Grid

This example demonstrates how to enable Gamepad navigation through a grid of
GuiObject|GUI elements without manually having to connect the
[GuiObject.NextSelectionUp](/docs/reference/engine/classes/GuiObject#NextSelectionUp), [GuiObject.NextSelectionDown](/docs/reference/engine/classes/GuiObject#NextSelectionDown), and
GuiObject|NextSelectionRight, and [GuiObject.NextSelectionLeft](/docs/reference/engine/classes/GuiObject#NextSelectionLeft)
properties for every element in the grid.

Note that this code sample assumes your UIGridLayout is sorted by
[name](/docs/reference/engine/classes/UIGridLayout#SortOrder), where elements are named in successive
numerical order.

The code relies on this to set the NextSelection properties for all
GuiObjects in the same level as the UIGridLayout. In our example, the
UIGridLayoutObject and GUI elements within the grid are all children of a
Frame named *"Container"*. The code
[gets the children](/docs/reference/engine/classes/Instance#GetChildren) of *"Container"* and loops
through each child. Children that are not GuiObjects are ignored. For each GUI
element, the code attempts to assigned the NextSelection properties using the
following logic:

1. Starting with 1, the name of all GUI elements match their position in the
   grid
2. Left: The item to the left will always be numbered 1 less than the current
   element
3. Right: The item to the left will always be numbered 1 more than the current
   element
4. Up: The item above (up) will always be number of GUIs in a row 1 less than
   the current element
5. Down: The item below (down) will always be the number of GUIs in a row more
   than the current element This logic also allows for the GUI elements at the
   begging and end of rows (excluding the first and last element) to wrap
   around to the next and previous rows. If an element doesn't exist to the
   left, right, up, or down, the NextSelection will remain nil and moving the
   Gamepad selector in the direction will not change the selected GUI.

This example also contains code to test the grid using the arrow keys (Up,
Down, Left, Right) of your keyboard instead of a gamepad, just in case you
don't have a gamepad to test with. This portion of code initially selects the
element named *"1"* by assigning it to the [GuiService.SelectedObject](/docs/reference/engine/classes/GuiService#SelectedObject)
property.

```
-- Setup the Gamepad selection grid using the code below



local container = script.Parent:FindFirstChild("Container")



local grid = container:GetChildren()



local rowSize = container:FindFirstChild("UIGridLayout").FillDirectionMaxCells



for _, gui in pairs(grid) do



if gui:IsA("GuiObject") then



local pos = gui.Name



-- Left edge



gui.NextSelectionLeft = container:FindFirstChild(pos - 1)



-- Right edge



gui.NextSelectionRight = container:FindFirstChild(pos + 1)



-- Above



gui.NextSelectionUp = container:FindFirstChild(pos - rowSize)



-- Below



gui.NextSelectionDown = container:FindFirstChild(pos + rowSize)



end



end



-- Test the Gamepad selection grid using the code below



local GuiService = game:GetService("GuiService")



local UserInputService = game:GetService("UserInputService")



GuiService.SelectedObject = container:FindFirstChild("1")



function updateSelection(input)



if input.UserInputType == Enum.UserInputType.Keyboard then



local key = input.KeyCode



local selectedObject = GuiService.SelectedObject



if not selectedObject then



return



end



if key == Enum.KeyCode.Up then



if not selectedObject.NextSelectionUp then



GuiService.SelectedObject = selectedObject



end



elseif key == Enum.KeyCode.Down then



if not selectedObject.NextSelectionDown then



GuiService.SelectedObject = selectedObject



end



elseif key == Enum.KeyCode.Left then



if not selectedObject.NextSelectionLeft then



GuiService.SelectedObject = selectedObject



end



elseif key == Enum.KeyCode.Right then



if not selectedObject.NextSelectionRight then



GuiService.SelectedObject = selectedObject



end



end



end



end



UserInputService.InputBegan:Connect(updateSelection)
```

Provide feedback

---

Position

Read Parallel

Determines the pixel and scalar position of the [GuiObject](/docs/reference/engine/classes/GuiObject).

GuiObject.Position:[UDim2](/docs/reference/engine/datatypes/UDim2)

This property determines the [GuiObject](/docs/reference/engine/classes/GuiObject) pixel and scalar position
using a [UDim2](/docs/reference/engine/datatypes/UDim2). Position is centered around the object's
[GuiObject.AnchorPoint](/docs/reference/engine/classes/GuiObject#AnchorPoint).

The scalar position is relative to the size of the parent GUI element, if
any.

The pixel portions of the [UDim2](/docs/reference/engine/datatypes/UDim2) value are the same regardless
of the parent GUI's size. The values represent the position of the object
in pixels. An object's actual pixel position can be read from the
[GuiBase2d.AbsolutePosition](/docs/reference/engine/classes/GuiBase2d#AbsolutePosition) property.

Provide feedback

---

Rotation

Read Parallel

Determines the number of degrees by which the [GuiObject](/docs/reference/engine/classes/GuiObject) is
rotated.

GuiObject.Rotation:[number](/docs/luau/numbers)

This property determines the number of degrees by which the
[GuiObject](/docs/reference/engine/classes/GuiObject) is rotated. Rotation is relative to the center of
the object, not the [AnchorPoint](/docs/reference/engine/classes/GuiObject#AnchorPoint), meaning
you cannot change the point of rotation. Additionally, this property is
not compatible with [ClipsDescendants](/docs/reference/engine/classes/GuiObject#ClipsDescendants).

Provide feedback

---

Selectable

Read Parallel

Determine whether the [GuiObject](/docs/reference/engine/classes/GuiObject) can be selected by a gamepad.

GuiObject.Selectable:[boolean](/docs/luau/booleans)

This property determines whether the [GuiObject](/docs/reference/engine/classes/GuiObject) can be selected
when navigating GUIs using a gamepad.

If this property is true, a GUI can be selected. Selecting a GUI also
sets the [GuiService.SelectedObject](/docs/reference/engine/classes/GuiService#SelectedObject) property to that object.

When this is false, the GUI cannot be selected. However, setting this to
false when a GUI is selected will not deselect it nor change the value
of the [GuiService.SelectedObject](/docs/reference/engine/classes/GuiService#SelectedObject) property.

Add [GuiObject.SelectionGained](/docs/reference/engine/classes/GuiObject#SelectionGained) and [GuiObject.SelectionLost](/docs/reference/engine/classes/GuiObject#SelectionLost)
will not fire for the element. To deselect a GuiObject, you must change
the [GuiService.SelectedObject](/docs/reference/engine/classes/GuiService#SelectedObject) property.

This property is useful if a GUI is connected to several GUIs via
properties such as this [GuiObject.NextSelectionUp](/docs/reference/engine/classes/GuiObject#NextSelectionUp),
[GuiObject.NextSelectionDown](/docs/reference/engine/classes/GuiObject#NextSelectionDown), [NextSelectionRight](/docs/reference/engine/classes/GuiObject),
or [NextSelectionLeft](/docs/reference/engine/classes/GuiObject). Rather than change all of the
properties so that the Gamepad cannot select the GUI, you can disable its
Selectable property to temporarily prevent it from being selected. Then,
when you want the gamepad selector to be able to select the GUI, simply
re-enable its selectable property.

Code Samples

Limiting TextBox Selection

The example below offers a simple demonstration on how to use the
[GuiObject.Selectable](/docs/reference/engine/classes/GuiObject#Selectable) property to limit when a GUI element can be
selected by the Gamepad navigator.

When a TextBox has gains focus, it can be selected. However, when a TextBox
loses focus it can no longer be selected.

Although this is a simple demonstration, the property can also be used to
prevent the navigator from selecting UI elements that exist for cosmetic
rather than functional purposes. For instance, while the buttons on a menu
screen should be selectable, the title image should not be.

```
local GuiService = game:GetService("GuiService")



local textBox = script.Parent



local function gainFocus()



textBox.Selectable = true



GuiService.SelectedObject = textBox



end



local function loseFocus(_enterPressed, _inputObject)



GuiService.SelectedObject = nil



textBox.Selectable = false



end



-- The FocusLost and FocusGained event will fire because the textBox



-- is of type TextBox



textBox.Focused:Connect(gainFocus)



textBox.FocusLost:Connect(loseFocus)
```

Provide feedback

---

SelectionImageObject

Read Parallel

Overrides the default selection adornment used for gamepads.

GuiObject.SelectionImageObject:[GuiObject](/docs/reference/engine/classes/GuiObject)

This property overrides the default selection adornment used for gamepads.

Note that the chosen
[SelectionImageObject](/docs/reference/engine/classes/GuiObject#SelectionImageObject) overlays the
selected [GuiObject](/docs/reference/engine/classes/GuiObject) with the [Size](/docs/reference/engine/classes/GuiObject#Size) of the
image. For best results, you should size the custom SelectionImageObject
via the scale [UDim2](/docs/reference/engine/datatypes/UDim2) values to help ensure that the object
scales properly over the selected element.

Changing the [SelectionImageObject](/docs/reference/engine/classes/GuiObject#SelectionImageObject)
for a [GuiObject](/docs/reference/engine/classes/GuiObject) element only affects that element. To affect all
of a user's GUI elements, set the [PlayerGui.SelectionImageObject](/docs/reference/engine/classes/PlayerGui#SelectionImageObject)
property.

To determine or set which GUI element is selected by the user, you can use
the [GuiService.SelectedObject](/docs/reference/engine/classes/GuiService#SelectedObject) property. The player uses the
gamepad to select different GUI elements, invoking the
[NextSelectionUp](/docs/reference/engine/classes/GuiObject#NextSelectionUp),
[NextSelectionDown](/docs/reference/engine/classes/GuiObject#NextSelectionDown),
[NextSelectionLeft](/docs/reference/engine/classes/GuiObject#NextSelectionLeft), and
[NextSelectionRight](/docs/reference/engine/classes/GuiObject#NextSelectionRight) events.

Provide feedback

---

SelectionOrder

Read Parallel

The order of [GuiObjects](/docs/reference/engine/classes/GuiObject) selected by the gamepad UI
selection.

GuiObject.SelectionOrder:[number](/docs/luau/numbers)

GuiObjects with a lower SelectionOrder are selected earlier than
GuiObjects with a higher SelectionOrder when starting the gamepad
selection or calling [GuiService:Select()](/docs/reference/engine/classes/GuiService#Select) on an ancestor. This
property does not affect directional navigation. Default value is 0.

Provide feedback

---

Size

Read Parallel

Determines the pixel and scalar size of the [GuiObject](/docs/reference/engine/classes/GuiObject).

GuiObject.Size:[UDim2](/docs/reference/engine/datatypes/UDim2)

This property determines the [GuiObject](/docs/reference/engine/classes/GuiObject) scalar and pixel size using
a [UDim2](/docs/reference/engine/datatypes/UDim2).

The scalar size is relative to the size of the parent GUI element, if any.

The pixel portions of the [UDim2](/docs/reference/engine/datatypes/UDim2) value are the same regardless
of the parent GUI's size. The values represent the size of the object in
pixels. An object's actual pixel size can be read from the
[GuiBase2d.AbsoluteSize](/docs/reference/engine/classes/GuiBase2d#AbsoluteSize) property.

If the [GuiObject](/docs/reference/engine/classes/GuiObject) has a parent, its size along each axis is also
influenced by the parent's
[SizeConstraint](/docs/reference/engine/classes/GuiObject#SizeConstraint).

Code Samples

Health Bar

This code sample allows you to create a simple color-changing health bar using
two nested Frames. Paste this into a LocalScript on the inner frame.

```
local Players = game:GetService("Players")



local player = Players.LocalPlayer



-- Paste script into a LocalScript that is



-- parented to a Frame within a Frame



local frame = script.Parent



local container = frame.Parent



container.BackgroundColor3 = Color3.new(0, 0, 0) -- black



-- This function is called when the humanoid's health changes



local function onHealthChanged()



local human = player.Character.Humanoid



local percent = human.Health / human.MaxHealth



-- Change the size of the inner bar



frame.Size = UDim2.new(percent, 0, 1, 0)



-- Change the color of the health bar



if percent < 0.1 then



frame.BackgroundColor3 = Color3.new(1, 0, 0) -- black



elseif percent < 0.4 then



frame.BackgroundColor3 = Color3.new(1, 1, 0) -- yellow



else



frame.BackgroundColor3 = Color3.new(0, 1, 0) -- green



end



end



-- This function runs is called the player spawns in



local function onCharacterAdded(character)



local human = character:WaitForChild("Humanoid")



-- Pattern: update once now, then any time the health changes



human.HealthChanged:Connect(onHealthChanged)



onHealthChanged()



end



-- Connect our spawn listener; call it if already spawned



player.CharacterAdded:Connect(onCharacterAdded)



if player.Character then



onCharacterAdded(player.Character)



end
```

Provide feedback

---

SizeConstraint

Read Parallel

Sets the [Size](/docs/reference/engine/classes/GuiObject#Size) axes that the [GuiObject](/docs/reference/engine/classes/GuiObject) will
be based on, relative to the size of its parent.

GuiObject.SizeConstraint:[Enum.SizeConstraint](/docs/reference/engine/enums/SizeConstraint)

This property sets the [Size](/docs/reference/engine/classes/GuiObject#Size) axes that the
[GuiObject](/docs/reference/engine/classes/GuiObject) will be based on, relative to the size of its parent.

This property is useful for creating GUI objects that are meant to scale
with either the width or height of a parent object, but not both,
effectively preserving the aspect ratio of the object.

Provide feedback

---

Transparency

Deprecated

Show details

---

Visible

Read Parallel

Determines whether the [GuiObject](/docs/reference/engine/classes/GuiObject) and its descendants will be
rendered.

GuiObject.Visible:[boolean](/docs/luau/booleans)

This property whether the [GuiObject](/docs/reference/engine/classes/GuiObject) and its descendants will be
rendered.

The rendering of individual components of a [GuiObject](/docs/reference/engine/classes/GuiObject) can be
controlled individually through transparency properties such as
[GuiObject.BackgroundTransparency](/docs/reference/engine/classes/GuiObject#BackgroundTransparency),
[TextLabel.TextTransparency](/docs/reference/engine/classes/TextLabel#TextTransparency) and
[ImageLabel.ImageTransparency](/docs/reference/engine/classes/ImageLabel#ImageTransparency).

When this property is false, the [GuiObject](/docs/reference/engine/classes/GuiObject) will be ignored by
layout structures such as [UIListLayout](/docs/reference/engine/classes/UIListLayout), [UIGridLayout](/docs/reference/engine/classes/UIGridLayout), and
[UITableLayout](/docs/reference/engine/classes/UITableLayout). In other words, the space that the element would
otherwise occupy in the layout is used by other elements instead.

Code Samples

UI Window

This code sample adds open/close functionality to a Window UI. Paste as a
LocalScript that is a sibling of a Frame named Window, a
TextButton/ImageButton named Window, and a TextButton/ImageButton within the
Window called Close.

```
local gui = script.Parent



local window = gui:WaitForChild("Window")



local toggleButton = gui:WaitForChild("ToggleWindow")



local closeButton = window:WaitForChild("Close")



local function toggleWindowVisbility()



-- Flip a boolean using the `not` keyword



window.Visible = not window.Visible



end



toggleButton.Activated:Connect(toggleWindowVisbility)



closeButton.Activated:Connect(toggleWindowVisbility)
```

Provide feedback

---

ZIndex

Read Parallel

Determines the order in which a [GuiObject](/docs/reference/engine/classes/GuiObject) renders relative to
others.

GuiObject.ZIndex:[number](/docs/luau/numbers)

This property determines the order in which a [GuiObject](/docs/reference/engine/classes/GuiObject) renders
relative to others.

By default, [GuiObjects](/docs/reference/engine/classes/GuiObject) render in ascending priority
order where those with lower [ZIndex](/docs/reference/engine/classes/GuiObject#ZIndex) values are
rendered under those with higher values. You can change the render order
within a [ScreenGui](/docs/reference/engine/classes/ScreenGui), [SurfaceGui](/docs/reference/engine/classes/SurfaceGui), or [BillboardGui](/docs/reference/engine/classes/BillboardGui) by
changing the value of its
[ZIndexBehavior](/docs/reference/engine/classes/LayerCollector#ZIndexBehavior).

If you are unsure if you'll need to add an element between two existing
elements in the future, it's a good practice to use multiples of 100
(0, 100, 200, etc.). This ensures a large gap of render order values
which you can use for elements layered in-between other elements.

See also [LayoutOrder](/docs/reference/engine/classes/GuiObject#LayoutOrder) which controls the
sorting order of a [GuiObject](/docs/reference/engine/classes/GuiObject) when used with a layout structure
such as [UIListLayout](/docs/reference/engine/classes/UIListLayout) or [UIGridLayout](/docs/reference/engine/classes/UIGridLayout).

Provide feedback

---

Methods

TweenPosition

Deprecated

Show details

---

TweenSize

Deprecated

Show details

---

TweenSizeAndPosition

Deprecated

Show details

---

Events

DragBegin

Deprecated

Show details

---

DragStopped

Deprecated

Show details

---

InputBegan

Fired when a user begins interacting via a Human-Computer Interface device
(Mouse button down, touch begin, keyboard button down, etc).

GuiObject.InputBegan(input:[InputObject](/docs/reference/engine/classes/InputObject)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| input:[InputObject](/docs/reference/engine/classes/InputObject)  An [InputObject](/docs/reference/engine/classes/InputObject), which contains useful data for querying user input such as the[type of input](/docs/reference/engine/enums/UserInputType), [state of input](/docs/reference/engine/enums/UserInputState), and [screen coordinates of the input](/docs/reference/engine/classes/InputObject#Position). |

This event fires when a user begins interacting with the [GuiObject](/docs/reference/engine/classes/GuiObject)
via a Human-Computer Interface device (Mouse button down, touch begin,
keyboard button down, etc).

The [UserInputService](/docs/reference/engine/classes/UserInputService) has a similarly named event that is not
restricted to a specific UI element: [UserInputService.InputBegan](/docs/reference/engine/classes/UserInputService#InputBegan).

This event will always fire regardless of game state.

See also [GuiObject.InputEnded](/docs/reference/engine/classes/GuiObject#InputEnded) and [GuiObject.InputChanged](/docs/reference/engine/classes/GuiObject#InputChanged).

Code Samples

Tracking the Beginning of Input on a GuiObject

The following example demonstrates one of many usage examples of handling user
input from InputBegan depending on its type.

In order for this to work as expected, it must be placed in a LocalScript
and a child of *gui*.

```
-- In order to use the InputBegan event, you must specify the GuiObject



local gui = script.Parent



-- A sample function providing multiple usage cases for various types of user input



local function inputBegan(input)



if input.UserInputType == Enum.UserInputType.Keyboard then



print("A key is being pushed down! Key:", input.KeyCode)



elseif input.UserInputType == Enum.UserInputType.MouseButton1 then



print("The left mouse button has been pressed down at", input.Position)



elseif input.UserInputType == Enum.UserInputType.MouseButton2 then



print("The right mouse button has been pressed down at", input.Position)



elseif input.UserInputType == Enum.UserInputType.Touch then



print("A touchscreen input has started at", input.Position)



elseif input.UserInputType == Enum.UserInputType.Gamepad1 then



print("A button is being pressed on a gamepad! Button:", input.KeyCode)



end



end



gui.InputBegan:Connect(inputBegan)
```

Provide feedback

---

InputChanged

Fired when a user changes how they're interacting via a Human-Computer
Interface device (Mouse button down, touch begin, keyboard button down,
etc).

GuiObject.InputChanged(input:[InputObject](/docs/reference/engine/classes/InputObject)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| input:[InputObject](/docs/reference/engine/classes/InputObject)  An [InputObject](/docs/reference/engine/classes/InputObject), which contains useful data for querying user input such as the[type of input](/docs/reference/engine/enums/UserInputType), [state of input](/docs/reference/engine/enums/UserInputState), and [screen coordinates of the input](/docs/reference/engine/classes/InputObject#Position). |

This event fires when a user changes how they're interacting via a
Human-Computer Interface device (Mouse button down, touch begin, keyboard
button down, etc).

The [UserInputService](/docs/reference/engine/classes/UserInputService) has a similarly named event that is not
restricted to a specific UI element:
[UserInputService.InputChanged](/docs/reference/engine/classes/UserInputService#InputChanged).

This event will always fire regardless of game state.

See also [GuiObject.InputBegan](/docs/reference/engine/classes/GuiObject#InputBegan) and [GuiObject.InputEnded](/docs/reference/engine/classes/GuiObject#InputEnded).

Code Samples

GuiObject InputChanged Demo

The following example demonstrates one of many usage examples of handling user
input from InputChanged depending on its type.

In order for this to work as expected, it must be placed in a LocalScript
and a child of *gui*.

```
local UserInputService = game:GetService("UserInputService")



local gui = script.Parent



local function printMovement(input)



print("Position:", input.Position)



print("Movement Delta:", input.Delta)



end



local function inputChanged(input)



if input.UserInputType == Enum.UserInputType.MouseMovement then



print("The mouse has been moved!")



printMovement(input)



elseif input.UserInputType == Enum.UserInputType.MouseWheel then



print("The mouse wheel has been scrolled!")



print("Wheel Movement:", input.Position.Z)



elseif input.UserInputType == Enum.UserInputType.Gamepad1 then



if input.KeyCode == Enum.KeyCode.Thumbstick1 then



print("The left thumbstick has been moved!")



printMovement(input)



elseif input.KeyCode == Enum.KeyCode.Thumbstick2 then



print("The right thumbstick has been moved!")



printMovement(input)



elseif input.KeyCode == Enum.KeyCode.ButtonL2 then



print("The pressure being applied to the left trigger has changed!")



print("Pressure:", input.Position.Z)



elseif input.KeyCode == Enum.KeyCode.ButtonR2 then



print("The pressure being applied to the right trigger has changed!")



print("Pressure:", input.Position.Z)



end



elseif input.UserInputType == Enum.UserInputType.Touch then



print("The user's finger is moving on the screen!")



printMovement(input)



elseif input.UserInputType == Enum.UserInputType.Gyro then



local _rotInput, rotCFrame = UserInputService:GetDeviceRotation()



local rotX, rotY, rotZ = rotCFrame:toEulerAnglesXYZ()



local rot = Vector3.new(math.deg(rotX), math.deg(rotY), math.deg(rotZ))



print("The rotation of the user's mobile device has been changed!")



print("Position", rotCFrame.p)



print("Rotation:", rot)



elseif input.UserInputType == Enum.UserInputType.Accelerometer then



print("The acceleration of the user's mobile device has been changed!")



printMovement(input)



end



end



gui.InputChanged:Connect(inputChanged)
```

Provide feedback

---

InputEnded

Fired when a user stops interacting via a Human-Computer Interface device
(Mouse button down, touch begin, keyboard button down, etc).

GuiObject.InputEnded(input:[InputObject](/docs/reference/engine/classes/InputObject)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| input:[InputObject](/docs/reference/engine/classes/InputObject)  An [InputObject](/docs/reference/engine/classes/InputObject), which contains useful data for querying user input such as the[Enum.UserInputType](/docs/reference/engine/enums/UserInputType), [Enum.UserInputState](/docs/reference/engine/enums/UserInputState), and [InputObject.Position](/docs/reference/engine/classes/InputObject#Position). |

The InputEnded event fires when a user stops interacting via a
Human-Computer Interface device (Mouse button down, touch begin, keyboard
button down, etc).

The [UserInputService](/docs/reference/engine/classes/UserInputService) has a similarly named event that is not
restricted to a specific UI element: [UserInputService.InputEnded](/docs/reference/engine/classes/UserInputService#InputEnded).

This event will always fire regardless of game state.

See also [GuiObject.InputBegan](/docs/reference/engine/classes/GuiObject#InputBegan) and [GuiObject.InputChanged](/docs/reference/engine/classes/GuiObject#InputChanged).

Code Samples

Tracking the End of Input on a GuiObject

The following example demonstrates one of many usage examples of handling user
input from InputEnded depending on its type.

In order for this to work as expected, it must be placed in a LocalScript
and a child of *gui*.

```
-- In order to use the InputChanged event, you must specify a GuiObject



local gui = script.Parent



-- A sample function providing multiple usage cases for various types of user input



local function inputEnded(input)



if input.UserInputType == Enum.UserInputType.Keyboard then



print("A key has been released! Key:", input.KeyCode)



elseif input.UserInputType == Enum.UserInputType.MouseButton1 then



print("The left mouse button has been released at", input.Position)



elseif input.UserInputType == Enum.UserInputType.MouseButton2 then



print("The right mouse button has been released at", input.Position)



elseif input.UserInputType == Enum.UserInputType.Touch then



print("A touchscreen input has been released at", input.Position)



elseif input.UserInputType == Enum.UserInputType.Gamepad1 then



print("A button has been released on a gamepad! Button:", input.KeyCode)



end



end



gui.InputEnded:Connect(inputEnded)
```

Provide feedback

---

MouseEnter

Fires when a user moves their mouse into a GUI element.

GuiObject.MouseEnter(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers)  The mouse's X screen coordinate in pixels, relative to the top left corner of the screen. |
| y:[number](/docs/luau/numbers)  The mouse's Y screen coordinate in pixels, relative to the top left corner of the screen. |

The MouseEnter event fires when a user moves their mouse into a
[GuiObject](/docs/reference/engine/classes/GuiObject) element.

Please do not rely on the x and y arguments passed by this event as a
fool-proof way to determine where the user's mouse is when it enters a
GUI. These coordinates may vary even when the mouse enters the GUI via the
same edge - particularly when the mouse enters the element quickly. This
is due to the fact the coordinates indicate the position of the mouse when
the event fires rather than the exact moment the mouse enters the GUI.

This event fires even when the GUI element renders beneath another
element.

If you would like to track when a user's mouse leaves a GUI element, you
can use the [GuiObject.MouseLeave](/docs/reference/engine/classes/GuiObject#MouseLeave) event.

##### See Also

* [GuiObject.MouseLeave](/docs/reference/engine/classes/GuiObject#MouseLeave)
* [GuiObject.MouseMoved](/docs/reference/engine/classes/GuiObject#MouseMoved)
* [GuiObject.MouseWheelForward](/docs/reference/engine/classes/GuiObject#MouseWheelForward)
* [GuiObject.MouseWheelBackward](/docs/reference/engine/classes/GuiObject#MouseWheelBackward)

Code Samples

Printing where a Mouse Enters a GuiObject

The following example prints the mouse location, in pixels, when it enters GUI
element.

```
local guiObject = script.Parent



guiObject.MouseEnter:Connect(function(x, y)



print("The user's mouse cursor has entered the GuiObject at position", x, ",", y)



end)
```

Provide feedback

---

MouseLeave

Fires when a user moves their mouse out of a GUI element.

GuiObject.MouseLeave(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers)  The mouse's X screen coordinate in pixels, relative to the top left corner of the screen. |
| y:[number](/docs/luau/numbers)  The mouse's Y screen coordinate in pixels, relative to the top left corner of the screen. |

The MouseLeave event fires when a user moves their mouse out of a
[GuiObject](/docs/reference/engine/classes/GuiObject) element.

Please do not rely on the x and y arguments passed by this event as a
fool-proof way to determine where the user's mouse is when it leaves a
GUI. These coordinates may vary even when the mouse leaves the GUI via the
same edge - particularly when the mouse leaves the element quickly. This
is due to the fact the coordinates indicate the position of the mouse when
the event fires rather than the exact moment the mouse leaves the GUI.

This event fires even when the GUI element renders beneath another
element.

##### See Also

* [GuiObject.MouseEnter](/docs/reference/engine/classes/GuiObject#MouseEnter)
* [GuiObject.MouseMoved](/docs/reference/engine/classes/GuiObject#MouseMoved)
* [GuiObject.MouseWheelForward](/docs/reference/engine/classes/GuiObject#MouseWheelForward)
* [GuiObject.MouseWheelBackward](/docs/reference/engine/classes/GuiObject#MouseWheelBackward)

Provide feedback

---

MouseMoved

Fires whenever a user moves their mouse while it is inside a GUI element.

GuiObject.MouseMoved(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers)  The mouse's X screen coordinate in pixels, relative to the top left corner of the screen. |
| y:[number](/docs/luau/numbers)  The mouse's Y screen coordinate in pixels, relative to the top left corner of the screen. |

Fires whenever a user moves their mouse while it is inside a
[GuiObject](/docs/reference/engine/classes/GuiObject) element. It is similar to [Mouse.Move](/docs/reference/engine/classes/Mouse#Move), which
fires regardless whether the user's mouse is over a GUI element.

Note, this event fires when the mouse's position is updated, therefore it
will fire repeatedly while being moved.

The x and y arguments indicate the updated screen coordinates of the
user's mouse in pixels. These can be useful to determine the mouse's
location on the GUI, screen, and delta since the mouse's previous position
if it is being tracked in a global variable.

The code below demonstrates how to determine the [Vector2](/docs/reference/engine/datatypes/Vector2) offset
of the user's mouse relative to a GUI element:

```
local Players = game:GetService("Players")



local CustomScrollingFrame = script.Parent



local SubFrame = CustomScrollingFrame:FindFirstChild("SubFrame")



local mouse = Players.LocalPlayer:GetMouse()



local function getPosition(X, Y)



local gui_X = CustomScrollingFrame.AbsolutePosition.X



local gui_Y = CustomScrollingFrame.AbsolutePosition.Y



local pos = Vector2.new(math.abs(X - gui_X), math.abs(Y - gui_Y - 36))



print(pos)



end



CustomScrollingFrame.MouseMoved:Connect(getPosition)
```

Note that this event may not fire exactly when the user's mouse enters or
exits a GUI element. Therefore, the x and y arguments may not match up
perfectly to the coordinates of the GUI's edges.

##### See Also

* [GuiObject.MouseEnter](/docs/reference/engine/classes/GuiObject#MouseEnter)
* [GuiObject.MouseLeave](/docs/reference/engine/classes/GuiObject#MouseLeave)
* [GuiObject.MouseWheelForward](/docs/reference/engine/classes/GuiObject#MouseWheelForward)
* [GuiObject.MouseWheelBackward](/docs/reference/engine/classes/GuiObject#MouseWheelBackward)

Provide feedback

---

MouseWheelBackward

Fires when a user scrolls their mouse wheel back when the mouse is over a
GUI element.

GuiObject.MouseWheelBackward(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers)  The mouse's X screen coordinate in pixels, relative to the top left corner of the screen. |
| y:[number](/docs/luau/numbers)  The mouse's Y screen coordinate in pixels, relative to the top left corner of the screen. |

The WheelBackward event fires when a user scrolls their mouse wheel back
when the mouse is over a [GuiObject](/docs/reference/engine/classes/GuiObject) element. It is similar to
[Mouse.WheelBackward](/docs/reference/engine/classes/Mouse#WheelBackward), which fires regardless whether the user's
mouse is over a GUI element.

This event fires merely as an indicator of the wheel's backward movement.
This means that the x and y mouse coordinate arguments don't change as
a result of this event. These coordinates only change when the mouse
moves, which can be tracked by the [GuiObject.MouseMoved](/docs/reference/engine/classes/GuiObject#MouseMoved) event.

##### See Also

* [GuiObject.MouseEnter](/docs/reference/engine/classes/GuiObject#MouseEnter)
* [GuiObject.MouseLeave](/docs/reference/engine/classes/GuiObject#MouseLeave)
* [GuiObject.MouseMoved](/docs/reference/engine/classes/GuiObject#MouseMoved)
* [GuiObject.MouseWheelForward](/docs/reference/engine/classes/GuiObject#MouseWheelForward)

Provide feedback

---

MouseWheelForward

Fires when a user scrolls their mouse wheel forward when the mouse is over
a GUI element.

GuiObject.MouseWheelForward(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers)  The mouse's X screen coordinate in pixels, relative to the top left corner of the screen. |
| y:[number](/docs/luau/numbers)  The Y coordinate of the user's mouse. |

The WheelForward event fires when a user scrolls their mouse wheel forward
when the mouse is over a [GuiObject](/docs/reference/engine/classes/GuiObject) element. It is similar to
[Mouse.WheelForward](/docs/reference/engine/classes/Mouse#WheelForward), which fires regardless whether the user's
mouse is over a GUI element.

This event fires merely as an indicator of the wheel's forward movement.
This means that the X and Y mouse coordinate arguments do not
change as a result of this event. These coordinates only change when the
mouse moves, which can be tracked by the [GuiObject.MouseMoved](/docs/reference/engine/classes/GuiObject#MouseMoved)
event.

##### See Also

* [GuiObject.MouseEnter](/docs/reference/engine/classes/GuiObject#MouseEnter)
* [GuiObject.MouseLeave](/docs/reference/engine/classes/GuiObject#MouseLeave)
* [GuiObject.MouseMoved](/docs/reference/engine/classes/GuiObject#MouseMoved)
* [GuiObject.MouseWheelBackward](/docs/reference/engine/classes/GuiObject#MouseWheelBackward)

Provide feedback

---

SelectionGained

Fired when the GuiObject is being focused on with the Gamepad selector.

GuiObject.SelectionGained():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires when the Gamepad selector starts focusing on the
[GuiObject](/docs/reference/engine/classes/GuiObject).

If you want to check from the Gamepad select stops focusing on the GUI
element, you can use the [GuiObject.SelectionLost](/docs/reference/engine/classes/GuiObject#SelectionLost) event.

When a GUI gains selection focus, the value of the
[SelectedObject](/docs/reference/engine/classes/GuiService#SelectedObject) property also changes to
the that gains selection. To determine which GUI gained selection, check
the value of this property.

Code Samples

Handling GUI Selection Gained

The following example prints a message when the user selects the object with a
gamepad.

In order for this to work as expected, it must be placed in a LocalScript
and a child of *gui*.

```
local guiObject = script.Parent



local function selectionGained()



print("The user has selected this button with a gamepad.")



end



guiObject.SelectionGained:Connect(selectionGained)
```

Provide feedback

---

SelectionLost

Fired when the Gamepad selector stops focusing on the GuiObject.

GuiObject.SelectionLost():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

This event fires when the Gamepad selector stops focusing on the
[GuiObject](/docs/reference/engine/classes/GuiObject).

If you want to check from the Gamepad select starts focusing on the GUI
element, you can use the [GuiObject.SelectionGained](/docs/reference/engine/classes/GuiObject#SelectionGained) event.

When a GUI loses selection focus, the value of the
[SelectionObject](/docs/reference/engine/classes/GuiService#SelectionObject) property changes either
to nil or to the GUI element that gains selection focus. To determine
which GUI gained selection, or if no GUI is selected, check the value of
this property.

Code Samples

Handling GUI Selection Lost

The following example prints a message when the element has its focus lost on
a gamepad.

In order for this to work as expected, it must be placed in a LocalScript
and a child of *gui*.

```
local guiObject = script.Parent



local function selectionLost()



print("The user no longer has this selected with their gamepad.")



end



guiObject.SelectionLost:Connect(selectionLost)
```

Provide feedback

---

TouchLongPress

Fires when the player starts, continues and stops long-pressing the UI
element.

GuiObject.TouchLongPress(

touchPositions:[Array](/docs/luau/tables#arrays), state:[Enum.UserInputState](/docs/reference/engine/enums/UserInputState)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| touchPositions:[Array](/docs/luau/tables#arrays)  An array of [Vector2](/docs/reference/engine/datatypes/Vector2) that describe the relative positions of the fingers involved in the gesture. |
| state:[Enum.UserInputState](/docs/reference/engine/enums/UserInputState)  A [Enum.UserInputState](/docs/reference/engine/enums/UserInputState) that describes the state of the gesture:   * Begin fires once at the beginning of the gesture (after the brief   delay) * Change fires if the player moves their finger while pressing down * End fires once at the end of the gesture when they release their   finger. |

This event fires after a brief moment when the player holds their finger
on the UI element using a touch-enabled device. It fires with a table of
[Vector2](/docs/reference/engine/datatypes/Vector2) that describe the relative screen positions of the
fingers involved in the gesture. In addition, it fires multiple times:
[Enum.UserInputState.Begin](/docs/reference/engine/enums/UserInputState#Begin) after a brief delay,
[Enum.UserInputState.Change](/docs/reference/engine/enums/UserInputState#Change) if the player moves their finger during the
gesture, and finally [Enum.UserInputState.End](/docs/reference/engine/enums/UserInputState#End). The delay is platform
dependent; in Studio it is a little longer than one second.

Since this event only requires one finger, this event can be simulated in
Studio using the emulator and a mouse.

Code Samples

Move UI Element with TouchLongPress

This code sample allows the player to manipulate the screen position of some
UI element, like a Frame, by holding down on the UI element for a brief
moment. Then, the player moves their finger and releases. During the gesture
the Frame is colored blue with a white outline.

```
local frame = script.Parent



frame.Active = true



local dragging = false



local basePosition



local startTouchPosition



local borderColor3



local backgroundColor3



local function onTouchLongPress(touchPositions, state)



if state == Enum.UserInputState.Begin and not dragging then



-- Start a drag



dragging = true



basePosition = frame.Position



startTouchPosition = touchPositions[1]



-- Color the frame to indicate the drag is happening



borderColor3 = frame.BorderColor3



backgroundColor3 = frame.BackgroundColor3



frame.BorderColor3 = Color3.new(1, 1, 1) -- White



frame.BackgroundColor3 = Color3.new(0, 0, 1) -- Blue



elseif state == Enum.UserInputState.Change then



local touchPosition = touchPositions[1]



local deltaPosition =



UDim2.new(0, touchPosition.X - startTouchPosition.X, 0, touchPosition.Y - startTouchPosition.Y)



frame.Position = basePosition + deltaPosition



elseif state == Enum.UserInputState.End and dragging then



-- Stop the drag



dragging = false



frame.BorderColor3 = borderColor3



frame.BackgroundColor3 = backgroundColor3



end



end



frame.TouchLongPress:Connect(onTouchLongPress)
```

Provide feedback

---

TouchPan

Fires when the player moves their finger on the UI element.

GuiObject.TouchPan(

touchPositions:[Array](/docs/luau/tables#arrays), totalTranslation:[Vector2](/docs/reference/engine/datatypes/Vector2), velocity:[Vector2](/docs/reference/engine/datatypes/Vector2), state:[Enum.UserInputState](/docs/reference/engine/enums/UserInputState)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| touchPositions:[Array](/docs/luau/tables#arrays)  A Luau array of [Vector2](/docs/reference/engine/datatypes/Vector2) objects, each indicating the position of all the fingers involved in the gesture. |
| totalTranslation:[Vector2](/docs/reference/engine/datatypes/Vector2)  Indicates how far the pan gesture has gone from its starting point. |
| velocity:[Vector2](/docs/reference/engine/datatypes/Vector2)  Indicates how quickly the gesture is being performed in each dimension. |
| state:[Enum.UserInputState](/docs/reference/engine/enums/UserInputState)  Indicates the [Enum.UserInputState](/docs/reference/engine/enums/UserInputState) of the gesture. |

This event fires when the player moves their finger on the UI element
using a touch-enabled device. It fires shortly before
[GuiObject.TouchSwipe](/docs/reference/engine/classes/GuiObject#TouchSwipe) would, and does not fire with
[GuiObject.TouchTap](/docs/reference/engine/classes/GuiObject#TouchTap). This event is useful for allowing the player
to manipulate the position of UI elements on the screen.

This event fires with a table of [Vector2](/docs/reference/engine/datatypes/Vector2) that describe the
relative screen positions of the fingers involved in the gesture. In
addition, it fires multiple times: [Enum.UserInputState.Begin](/docs/reference/engine/enums/UserInputState#Begin) after a
brief delay, [Enum.UserInputState.Change](/docs/reference/engine/enums/UserInputState#Change) when the player moves their
finger during the gesture, and finally with [Enum.UserInputState.End](/docs/reference/engine/enums/UserInputState#End).

This event cannot be simulated in Studio using the emulator and a mouse;
you must have a real touch-enabled device to fire it.

Code Samples

Panning UI Element

This code sample is meant to be placed in a LocalScript within an inner
Frame that is inside an outer Frame, or other GuiObject. It allows the
player to manipulate the position of the inner frame by moving their finger on
the outer frame.

```
local innerFrame = script.Parent



local outerFrame = innerFrame.Parent



outerFrame.BackgroundTransparency = 0.75



outerFrame.Active = true



outerFrame.Size = UDim2.new(1, 0, 1, 0)



outerFrame.Position = UDim2.new(0, 0, 0, 0)



outerFrame.AnchorPoint = Vector2.new(0, 0)



outerFrame.ClipsDescendants = true



local dragging = false



local basePosition



local function onTouchPan(_touchPositions, totalTranslation, _velocity, state)



if state == Enum.UserInputState.Begin and not dragging then



dragging = true



basePosition = innerFrame.Position



outerFrame.BackgroundTransparency = 0.25



elseif state == Enum.UserInputState.Change then



innerFrame.Position = basePosition + UDim2.new(0, totalTranslation.X, 0, totalTranslation.Y)



elseif state == Enum.UserInputState.End and dragging then



dragging = false



outerFrame.BackgroundTransparency = 0.75



end



end



outerFrame.TouchPan:Connect(onTouchPan)
```

Provide feedback

---

TouchPinch

Fires when the player performs a pinch or pull gesture using two fingers
on the UI element.

GuiObject.TouchPinch(

touchPositions:[Array](/docs/luau/tables#arrays), scale:[number](/docs/luau/numbers), velocity:[number](/docs/luau/numbers), state:[Enum.UserInputState](/docs/reference/engine/enums/UserInputState)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| touchPositions:[Array](/docs/luau/tables#arrays)  A Luau array of [Vector2](/docs/reference/engine/datatypes/Vector2) objects, each indicating the position of all the fingers involved in the pinch gesture. |
| scale:[number](/docs/luau/numbers)  A float that indicates the difference from the beginning of the pinch gesture. |
| velocity:[number](/docs/luau/numbers)  A float indicating how quickly the pinch gesture is happening. |
| state:[Enum.UserInputState](/docs/reference/engine/enums/UserInputState)  Indicates the [Enum.UserInputState](/docs/reference/engine/enums/UserInputState) of the gesture. |

This event fires when the player uses two fingers to make a pinch or pull
gesture on the UI element using a touch-enabled device. A pinch
happens when two or more fingers move closer together, and a pull
happens when they move apart. This event fires in conjunction with
[GuiObject.TouchPan](/docs/reference/engine/classes/GuiObject#TouchPan). This event is useful for allowing the player
to manipulate the scale (size) of UI elements on the screen, and is most
often used for zooming features.

This event fires with a table of [Vector2](/docs/reference/engine/datatypes/Vector2) that describe the
relative screen positions of the fingers involved in the gesture. In
addition, it fires multiple times: [Enum.UserInputState.Begin](/docs/reference/engine/enums/UserInputState#Begin) after a
brief delay, [Enum.UserInputState.Change](/docs/reference/engine/enums/UserInputState#Change) when the player moves a finger
during the gesture, and finally with [Enum.UserInputState.End](/docs/reference/engine/enums/UserInputState#End). It should
be noted that the scale should be used multiplicatively.

Since this event requires at least two fingers, it is not possible to
simulate it in Studio using the emulator and a mouse; you must have a real
touch-enabled device.

Code Samples

Pinch/Pull Scaling

This code sample is meant for a LocalScript within an inner Frame that is
inside an outer Frame, or other GuiObject. It allows the player to scale
the inner frame by performing a [GuiObject.TouchPinch](/docs/reference/engine/classes/GuiObject#TouchPinch) gesture on the
outer frame.

```
local innerFrame = script.Parent



local outerFrame = innerFrame.Parent



outerFrame.BackgroundTransparency = 0.75



outerFrame.Active = true



outerFrame.Size = UDim2.new(1, 0, 1, 0)



outerFrame.Position = UDim2.new(0, 0, 0, 0)



outerFrame.AnchorPoint = Vector2.new(0, 0)



outerFrame.ClipsDescendants = true



local dragging = false



local uiScale = Instance.new("UIScale")



uiScale.Parent = innerFrame



local baseScale



local function onTouchPinch(_touchPositions, scale, _velocity, state)



if state == Enum.UserInputState.Begin and not dragging then



dragging = true



baseScale = uiScale.Scale



outerFrame.BackgroundTransparency = 0.25



elseif state == Enum.UserInputState.Change then



uiScale.Scale = baseScale * scale -- Notice the multiplication here



elseif state == Enum.UserInputState.End and dragging then



dragging = false



outerFrame.BackgroundTransparency = 0.75



end



end



outerFrame.TouchPinch:Connect(onTouchPinch)
```

Provide feedback

---

TouchRotate

Fires when the player performs a rotation gesture using two fingers on the
UI element.

GuiObject.TouchRotate(

touchPositions:[Array](/docs/luau/tables#arrays), rotation:[number](/docs/luau/numbers), velocity:[number](/docs/luau/numbers), state:[Enum.UserInputState](/docs/reference/engine/enums/UserInputState)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| touchPositions:[Array](/docs/luau/tables#arrays)  A Luau array of [Vector2](/docs/reference/engine/datatypes/Vector2) objects, each indicating the position of all the fingers involved in the gesture. |
| rotation:[number](/docs/luau/numbers)  A float indicating how much the rotation has gone from the start of the gesture. |
| velocity:[number](/docs/luau/numbers)  A float that indicates how quickly the gesture is being performed. |
| state:[Enum.UserInputState](/docs/reference/engine/enums/UserInputState)  Indicates the [Enum.UserInputState](/docs/reference/engine/enums/UserInputState) of the gesture. |

This event fires when the player uses two fingers to make a pinch or pull
gesture on the UI element using a touch-enabled device. Rotation occurs
when the angle of the line between two fingers changes. This event fires
in conjunction with [GuiObject.TouchPan](/docs/reference/engine/classes/GuiObject#TouchPan). This event is useful for
allowing the player to manipulate the rotation of UI elements on the
screen.

This event fires with a table of [Vector2](/docs/reference/engine/datatypes/Vector2) that describe the
relative screen positions of the fingers involved in the gesture. In
addition, it fires multiple times: [Enum.UserInputState.Begin](/docs/reference/engine/enums/UserInputState#Begin) after a
brief delay, [Enum.UserInputState.Change](/docs/reference/engine/enums/UserInputState#Change) when the player moves a finger
during the gesture, and finally with [Enum.UserInputState.End](/docs/reference/engine/enums/UserInputState#End).

Since this event requires at least two fingers, it is not possible to be
simulated in Studio using the emulator and a mouse; you must have a real
touch-enabled device.

Code Samples

Touch Rotation

This code sample is meant for a LocalScript within an inner Frame that is
inside an outer Frame, or other GuiObject. It allows the player to rotate
the inner frame by performing a [GuiObject.TouchRotate](/docs/reference/engine/classes/GuiObject#TouchRotate) gesture on the
outer frame.

```
local innerFrame = script.Parent



local outerFrame = innerFrame.Parent



outerFrame.BackgroundTransparency = 0.75



outerFrame.Active = true



outerFrame.Size = UDim2.new(1, 0, 1, 0)



outerFrame.Position = UDim2.new(0, 0, 0, 0)



outerFrame.AnchorPoint = Vector2.new(0, 0)



outerFrame.ClipsDescendants = true



local dragging = false



local baseRotation = innerFrame.Rotation



local function onTouchRotate(_touchPositions, rotation, _velocity, state)



if state == Enum.UserInputState.Begin and not dragging then



dragging = true



baseRotation = innerFrame.Rotation



outerFrame.BackgroundTransparency = 0.25



elseif state == Enum.UserInputState.Change then



innerFrame.Rotation = baseRotation + rotation



elseif state == Enum.UserInputState.End and dragging then



dragging = false



outerFrame.BackgroundTransparency = 0.75



end



end



outerFrame.TouchRotate:Connect(onTouchRotate)
```

Provide feedback

---

TouchSwipe

Fires when the player performs a swipe gesture on the UI element.

GuiObject.TouchSwipe(

swipeDirection:[Enum.SwipeDirection](/docs/reference/engine/enums/SwipeDirection), numberOfTouches:[number](/docs/luau/numbers)

):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| swipeDirection:[Enum.SwipeDirection](/docs/reference/engine/enums/SwipeDirection)  A [Enum.SwipeDirection](/docs/reference/engine/enums/SwipeDirection) indicating the direction of the swipe gesture (Up, Down, Left or Right). |
| numberOfTouches:[number](/docs/luau/numbers)  The number of touch points involved in the gesture (usually 1). |

This event fires when the player performs a swipe gesture on the UI
element using a touch-enabled device. It fires with the direction of the
gesture (Up, Down, Left or Right) and the number of touch points involved
in the gesture. Swipe gestures are often used to change tabs in mobile
UIs.

Since this event only requires one finger, it can be simulated in Studio
using the emulator and a mouse.

Code Samples

Bouncing Color Picker

This code sample will cause a Frame (or other GuiObject) to bounce when a
swipe gesture is performed on a touch-enabled device (or Studio's emulator).
Horizontal swipes will change the hue of the
[GuiObject.BackgroundColor3](/docs/reference/engine/classes/GuiObject#BackgroundColor3), while vertical swipes will change the
saturation.

```
local frame = script.Parent



frame.Active = true



-- How far the frame should bounce on a successful swipe



local BOUNCE_DISTANCE = 50



-- Current state of the frame



local basePosition = frame.Position



local hue = 0



local saturation = 128



local function updateColor()



frame.BackgroundColor3 = Color3.fromHSV(hue / 256, saturation / 256, 1)



end



local function onTouchSwipe(swipeDir, _touchCount)



-- Change the BackgroundColor3 based on the swipe direction



local deltaPos



if swipeDir == Enum.SwipeDirection.Right then



deltaPos = UDim2.new(0, BOUNCE_DISTANCE, 0, 0)



hue = (hue + 16) % 255



elseif swipeDir == Enum.SwipeDirection.Left then



deltaPos = UDim2.new(0, -BOUNCE_DISTANCE, 0, 0)



hue = (hue - 16) % 255



elseif swipeDir == Enum.SwipeDirection.Up then



deltaPos = UDim2.new(0, 0, 0, -BOUNCE_DISTANCE)



saturation = (saturation + 16) % 255



elseif swipeDir == Enum.SwipeDirection.Down then



deltaPos = UDim2.new(0, 0, 0, BOUNCE_DISTANCE)



saturation = (saturation - 16) % 255



else



deltaPos = UDim2.new()



end



-- Update the color and bounce the frame a little



updateColor()



frame.Position = basePosition + deltaPos



frame:TweenPosition(basePosition, Enum.EasingDirection.Out, Enum.EasingStyle.Bounce, 0.7, true)



end



frame.TouchSwipe:Connect(onTouchSwipe)



updateColor()
```

Provide feedback

---

TouchTap

Fires when the player performs a tap gesture on the UI element.

GuiObject.TouchTap(touchPositions:[Array](/docs/luau/tables#arrays)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| touchPositions:[Array](/docs/luau/tables#arrays)  An array of [Vector2](/docs/reference/engine/datatypes/Vector2) that describe the relative positions of the fingers involved in the gesture. |

This event fires when the player performs a tap gesture on the UI element
using a touch-enabled device. A tap is a quick single touch without any
movement involved (a longer press would fire
[GuiObject.TouchLongPress](/docs/reference/engine/classes/GuiObject#TouchLongPress), and moving during the touch would fire
[GuiObject.TouchPan](/docs/reference/engine/classes/GuiObject#TouchPan) and/or [GuiObject.TouchSwipe](/docs/reference/engine/classes/GuiObject#TouchSwipe)). It fires
with a table of [Vector2](/docs/reference/engine/datatypes/Vector2) objects that describe the relative
positions of the fingers involved in the gesture.

Since this event only requires one finger, it can be simulated in Studio
using the emulator and a mouse.

Code Samples

Tap Transparency Toggle

This code sample will toggle the [GuiObject.BackgroundTransparency](/docs/reference/engine/classes/GuiObject#BackgroundTransparency) of a
UI element, like a Frame, when it is tapped on a touch-enabled device.

```
local frame = script.Parent



frame.Active = true



local function onTouchTap()



-- Toggle background transparency



if frame.BackgroundTransparency > 0 then



frame.BackgroundTransparency = 0



else



frame.BackgroundTransparency = 0.75



end



end



frame.TouchTap:Connect(onTouchTap)
```

Provide feedback

---