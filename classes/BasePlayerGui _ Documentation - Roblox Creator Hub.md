# BasePlayerGui | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/BasePlayerGui
Scraped: 2026-01-11T02:32:55.843459Z

## Tags
- Not Creatable

## Inherits
- Object
- Instance
- BasePlayerGui
- CoreGui
- PlayerGui
- StarterGui
- GuiObject
- GuiInset
- GuiObject.MouseEnter
- GuiObject.MouseLeave
- BasePlayerGui:GetGuiObjectsAtPosition()
- GuiBase2d.AbsoluteSize
- GuiBase2d.AbsolutePosition
- Instance:Destroy()
- ScreenGui.DisplayOrder
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [BasePlayerGui](/docs/reference/engine/classes/BasePlayerGui)

English

Feedback

Engine Class

BasePlayerGui

The BasePlayerGui is an abstract class which the GUI drawing storage classes
inherit from.

Not Creatable

---

Summary

Methods

|  |
| --- |
| [GetGuiObjectsAtPosition](#GetGuiObjectsAtPosition)(x: [number](/docs/luau/numbers),y: [number](/docs/luau/numbers)):Instances |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[CoreGui](/docs/reference/engine/classes/CoreGui), [PlayerGui](/docs/reference/engine/classes/PlayerGui), [StarterGui](/docs/reference/engine/classes/StarterGui)

The BasePlayerGui is an abstract class that all GUI drawing storage classes
inherit from.

---

API Reference

Methods

GetGuiObjectsAtPosition

Returns a list of all [GuiObject](/docs/reference/engine/classes/GuiObject) instances occupying the given
point on the screen.

BasePlayerGui:GetGuiObjectsAtPosition(

x:[number](/docs/luau/numbers), y:[number](/docs/luau/numbers)

):Instances

Parameters

|  |
| --- |
| x:[number](/docs/luau/numbers)  The x position on the screen relative to the top left corner after the [GuiInset](/docs/reference/engine/classes/GuiService#GetGuiInset) is applied. |
| y:[number](/docs/luau/numbers)  The y position on the screen relative to the top left corner after the [GuiInset](/docs/reference/engine/classes/GuiService#GetGuiInset) is applied. |

Returns

Instances

A table of the [GuiObject](/docs/reference/engine/classes/GuiObject) instances that occupy the given
screen space.

Takes a screen position and returns a list of all the [GuiObject](/docs/reference/engine/classes/GuiObject)
instances that are occupying that screen position, sorted in the order
they appear on-screen from top to bottom as the first and last index,
respectively.

The main use case is to get GUI objects under the player's mouse or touch
inputs to do things like allow selection or highlighting. These effects
can already be achieved using [GuiObject.MouseEnter](/docs/reference/engine/classes/GuiObject#MouseEnter) and
[GuiObject.MouseLeave](/docs/reference/engine/classes/GuiObject#MouseLeave) but this requires the developer to track
these events for their UI objects all the time even if they only need this
functionality in specific circumstances.

Since the child classes of [BasePlayerGui](/docs/reference/engine/classes/BasePlayerGui) inherit this function, it
can be fired by class objects such as the [PlayerGui](/docs/reference/engine/classes/PlayerGui) and
[StarterGui](/docs/reference/engine/classes/StarterGui) folders.

Code Samples

Selecting GUIs at a Position

All GUIs returned by [BasePlayerGui:GetGuiObjectsAtPosition()](/docs/reference/engine/classes/BasePlayerGui#GetGuiObjectsAtPosition) are
'cloned' by the highlightAsFrame() local function, which creates a Frame
GUI positioned on top of the specified GUI that is semi-transparent and the
same [GuiBase2d.AbsoluteSize](/docs/reference/engine/classes/GuiBase2d#AbsoluteSize) and [GuiBase2d.AbsolutePosition](/docs/reference/engine/classes/GuiBase2d#AbsolutePosition).

These highlights are added to the HighlightsContainer ScreenGui in the
Highlight folder of the player's PlayerGui folder. Both are created by the
code sample. All highlight GUIs are [Instance:Destroy()](/docs/reference/engine/classes/Instance#Destroy)ed every time
highlightGui() executes.

Note that HighlightContainer's [ScreenGui.DisplayOrder](/docs/reference/engine/classes/ScreenGui#DisplayOrder) is 99999, a
large number, so that it is unlikely any other GUI will render on top of the
highlight GUIs.

```
local UserInputService = game:GetService("UserInputService")



local Players = game:GetService("Players")



local player = Players.LocalPlayer



local playerGui = player:WaitForChild("PlayerGui")



-- Create a Folder and ScreenGui to contain the highlight Frames



local highlights = Instance.new("Folder")



highlights.Name = "Highlights"



highlights.Parent = playerGui



local highlightsContainer = Instance.new("ScreenGui")



highlightsContainer.Name = "Container"



highlightsContainer.Parent = highlights



highlightsContainer.DisplayOrder = 99999



-- Creates a semi-transparent yellow Frame on top of the gui with the same AbsoluteSize and AbsolutePosition



local function highlightAsFrame(gui)



local highlight = Instance.new("Frame")



highlight.Name = "Highlight"



highlight.Parent = highlightsContainer



highlight.Size = UDim2.new(0, gui.AbsoluteSize.X, 0, gui.AbsoluteSize.Y)



highlight.Position = UDim2.new(0, gui.AbsolutePosition.X, 0, gui.AbsolutePosition.Y)



highlight.BackgroundColor3 = Color3.fromRGB(255, 255, 10) -- Yellow



highlight.BackgroundTransparency = 0.75



highlight.BorderSizePixel = 0



highlight.LayoutOrder = gui.LayoutOrder - 1



end



-- Use GetGuiObjectsAtPosition to get and highlight all GuiObjects at the input's position



local function highlightGui(input, _gameProcessed)



local pos = input.Position



local guisAtPosition = playerGui:GetGuiObjectsAtPosition(pos.X, pos.Y)



highlightsContainer:ClearAllChildren()



for _, gui in ipairs(guisAtPosition) do



if gui:IsA("GuiObject") then



highlightAsFrame(gui)



end



end



end



-- Fire highlightGui on InputBegan if input is of type MouseButton1 of Touch



local function InputBegan(input, gameProcessed)



local inputType = input.UserInputType



local touch = Enum.UserInputType.Touch



local mouse1 = Enum.UserInputType.MouseButton1



if inputType == touch or inputType == mouse1 then



highlightGui(input, gameProcessed)



end



end



UserInputService.InputBegan:Connect(InputBegan)
```

Provide feedback

---