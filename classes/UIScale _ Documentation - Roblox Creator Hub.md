# UIScale | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/UIScale
Scraped: 2026-01-11T02:33:18.224128Z

## Inherits
- UIComponent
- UIScale
- Instance
- Object
- GuiBase2d.AbsoluteSize
- UIScale.Scale
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [UIComponent](/docs/reference/engine/classes/UIComponent)
6. /
7. [UIScale](/docs/reference/engine/classes/UIScale)

English

Feedback

Engine Class

![UIScale](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/UIScale-Dark.webp)UIScale

An object that acts as a multiplier for the size of the parent UI element's
scale.

---

Summary

Properties

|  |
| --- |
| [Scale](#Scale):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A UIScale object simply contains a number that is used to multiply the
[GuiBase2d.AbsoluteSize](/docs/reference/engine/classes/GuiBase2d#AbsoluteSize) of the parent UI element. This number is stored
in [UIScale.Scale](/docs/reference/engine/classes/UIScale#Scale).

Code Samples

UI Scale Demo

This code sample creates some images of a lock and scales them using UIScale.
It lays them out using a UIListLayout.

```
-- Lay out the images in a list



Instance.new("UIListLayout", script.Parent).SortOrder = Enum.SortOrder.LayoutOrder



-- Create some images of varying sizes using UIScale objects



for size = 0.2, 1.5, 0.2 do



local image = Instance.new("ImageLabel")



image.Image = "rbxassetid://284402752" -- an image of a Lock



image.Parent = script.Parent



image.Size = UDim2.new(0, 100, 0, 100)



-- Scale the image by adding a UIScale with the size



--  Note: this is a shorthand since we don't need a reference to the UIScale



Instance.new("UIScale", image).Scale = size



end
```

---

API Reference

Properties

Scale

Read Parallel

Determines the multiplier to apply to the parent UI element's size.

UIScale.Scale:[number](/docs/luau/numbers)

The Scale property determines the multiplier used on the parent UI
element's [GuiBase2d.AbsoluteSize](/docs/reference/engine/classes/GuiBase2d#AbsoluteSize). When set to 0.5, an AbsoluteSize
of {0, 200}, {0, 50} becomes {0, 100}, {0, 25}. Similarly, when set to 2,
such an AbsoluteSize would become {0, 400}, {0, 100}.

Code Samples

UI Scale Demo

This code sample creates some images of a lock and scales them using UIScale.
It lays them out using a UIListLayout.

```
-- Lay out the images in a list



Instance.new("UIListLayout", script.Parent).SortOrder = Enum.SortOrder.LayoutOrder



-- Create some images of varying sizes using UIScale objects



for size = 0.2, 1.5, 0.2 do



local image = Instance.new("ImageLabel")



image.Image = "rbxassetid://284402752" -- an image of a Lock



image.Parent = script.Parent



image.Size = UDim2.new(0, 100, 0, 100)



-- Scale the image by adding a UIScale with the size



--  Note: this is a shorthand since we don't need a reference to the UIScale



Instance.new("UIScale", image).Scale = size



end
```

Provide feedback

---