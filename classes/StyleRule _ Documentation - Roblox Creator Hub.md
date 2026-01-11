# StyleRule | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/StyleRule
Scraped: 2026-01-11T02:37:24.572651Z

## Tags
- Not Replicated

## Inherits
- StyleBase
- StyleRule
- Selector
- Instance
- Object
- StyleRules
- ImageLabel
- GuiObject
- UIComponent
- CollectionService
- Instance.Name
- TextButton
- LocalScript
- ScreenGui
- StarterGui
- UICorner
- Frame
- SetProperty()
- UIGradient
- AnchorPoint
- BackgroundColor3
- SetProperties()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [StyleBase](/docs/reference/engine/classes/StyleBase)
6. /
7. [StyleRule](/docs/reference/engine/classes/StyleRule)

English

Feedback

Engine Class

![StyleRule](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/StyleRule-Dark.webp)StyleRule

Defines style properties which override properties on the instances affected
by the [Selector](/docs/reference/engine/classes/StyleRule#Selector) property.

---

Summary

Properties

|  |
| --- |
| [Priority](#Priority):[number](/docs/luau/numbers) |
| [Selector](#Selector):[string](/docs/luau/strings) |
| [SelectorError](#SelectorError):[string](/docs/luau/strings) |

Methods

|  |
| --- |
| [GetProperties](#GetProperties)():[Dictionary](/docs/luau/tables#dictionaries) |
| [GetProperty](#GetProperty)(name: [string](/docs/luau/strings)):Variant |
| [SetProperties](#SetProperties)(styleProperties: [Dictionary](/docs/luau/tables#dictionaries)):() |
| [SetProperty](#SetProperty)(name: [string](/docs/luau/strings),value: Variant):() |

Inherited Members

4 inherited from [StyleBase](/docs/reference/engine/classes/StyleBase)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Defines style properties which override properties on the instances affected
by the [Selector](/docs/reference/engine/classes/StyleRule#Selector) property.

---

API Reference

Properties

Priority

Read Parallel

A number that determines how properties of the StyleRule apply relative
to the same properties in other StyleRules. Higher priority values take
precedence over lower.

StyleRule.Priority:[number](/docs/luau/numbers)

A number that determines how properties of the StyleRule apply relative
to the same properties in other [StyleRules](/docs/reference/engine/classes/StyleRule). Higher
priority values take precedence over lower. For example, if a StyleRule
with a priority of 10 has an AnchorPoint property of 1, 0, it will take precedence over lower-priority
[StyleRules](/docs/reference/engine/classes/StyleRule) with AnchorPoint properties.

Provide feedback

---

Selector

Read Parallel

A string specifying which instances the StyleRule should affect.

StyleRule.Selector:[string](/docs/luau/strings)

A string specifying which instances the StyleRule should affect. This
can be a mix of selectors and combinators to match characteristics such as
the class name, instance name, and hierarchy relationships.

For example, ".Container > ImageLabel.BlueOnHover:Hover" effectively
means the style rule overrides every [ImageLabel](/docs/reference/engine/classes/ImageLabel) that's a child of
an instance tagged with Container (.Container > ImageLabel) and is
tagged with BlueOnHover (.BlueOnHover) and is in the
[Enum.GuiState.Hover](/docs/reference/engine/enums/GuiState#Hover) state (:Hover).

##### Selectors

| Selector | Description | Examples |
| --- | --- | --- |
| [class] | Matches instances of a [GuiObject](/docs/reference/engine/classes/GuiObject) or [UIComponent](/docs/reference/engine/classes/UIComponent) class. | "Frame" "ImageButton" "UICorner" |
| .[tag] | Matches instances [tagged](/docs/studio/properties#instance-tags) with a [CollectionService](/docs/reference/engine/classes/CollectionService) tag. | ".Container" ".BlueOnHover" |
| #[name] | Matches instances of a specific [Instance.Name](/docs/reference/engine/classes/Instance#Name). | "#ModalFrame" "#CloseButton" |
| :[state] | Matches instances currently in a [Enum.GuiState](/docs/reference/engine/enums/GuiState). | ":Hover" |

##### Combinators

| Combinator | Description | Examples |
| --- | --- | --- |
| > | Matches instances that are **direct children** of the previous filter matches. | "Frame > .Inventory" |
| >> | Matches instances that are **descendants** of the previous filter matches. | "ImageButton >> .BlueOnHover" |
| , | Specifies a list of multiple independent selectors for the style rule. | "Frame.TagA, TextLabel.TagA" |
| :: | Creates a phantom [UIComponent](/docs/reference/engine/classes/UIComponent) instance under the previous filter matches and applies the style rule's properties to it. | "Frame::UICorner" |

Code Samples

UI Class Selector

The following example shows how to define a class selector which targets
all [TextButton](/docs/reference/engine/classes/TextButton) instances and styles them with blue background and
light grey text. To test, paste the code into a [LocalScript](/docs/reference/engine/classes/LocalScript) which is a
child of a [ScreenGui](/docs/reference/engine/classes/ScreenGui) located inside the [StarterGui](/docs/reference/engine/classes/StarterGui) container.

```
local ReplicatedStorage = game:GetService("ReplicatedStorage")



local screenGui = script.Parent



local coreSheet = Instance.new("StyleSheet")



coreSheet.Parent = ReplicatedStorage



local styleLink = Instance.new("StyleLink")



styleLink.StyleSheet = coreSheet



styleLink.Parent = screenGui



local rule = Instance.new("StyleRule")



rule.Parent = coreSheet



-- Class selector



rule.Selector = "TextButton"



-- Set rule properties



rule:SetProperties({



["BackgroundColor3"] = Color3.fromHex("335FFF"),



["TextColor3"] = Color3.fromHex("E1E1E1"),



["Size"] = UDim2.new(0.15, 0, 0, 40),



["BorderSizePixel"] = 0,



})



local button = Instance.new("TextButton")



button.Text = "Main Menu"



button.Parent = screenGui
```

UI Tag Selector

The following example shows how to define a tag selector which utilizes
[tags](/docs/studio/properties#instance-tags) applied through
[CollectionService](/docs/reference/engine/classes/CollectionService) to target a [TextButton](/docs/reference/engine/classes/TextButton) tagged with
ButtonPrimary. To test, paste the code into a [LocalScript](/docs/reference/engine/classes/LocalScript) which is a
child of a [ScreenGui](/docs/reference/engine/classes/ScreenGui) located inside the [StarterGui](/docs/reference/engine/classes/StarterGui) container.

```
local CollectionService = game:GetService("CollectionService")



local ReplicatedStorage = game:GetService("ReplicatedStorage")



local screenGui = script.Parent



local coreSheet = Instance.new("StyleSheet")



coreSheet.Parent = ReplicatedStorage



local styleLink = Instance.new("StyleLink")



styleLink.StyleSheet = coreSheet



styleLink.Parent = screenGui



local rule = Instance.new("StyleRule")



rule.Parent = coreSheet



-- Tag selector



rule.Selector = ".ButtonPrimary"



-- Set rule properties



rule:SetProperties({



["BackgroundColor3"] = Color3.fromHex("FF0099"),



["TextColor3"] = Color3.fromHex("E1E1E1"),



["Size"] = UDim2.new(0.15, 0, 0, 40),



["BorderSizePixel"] = 0,



})



local button = Instance.new("TextButton")



button.Text = "Main Menu"



button.Parent = screenGui



-- Apply tag to button



CollectionService:AddTag(button, "ButtonPrimary")
```

UI Modifier Selector

The following example shows how to define a UI modifier selector which
applies a phantom [UICorner](/docs/reference/engine/classes/UICorner) instance to a [Frame](/docs/reference/engine/classes/Frame) tagged with
RoundedCorner20. To test, paste the code into a [LocalScript](/docs/reference/engine/classes/LocalScript) which is
a child of a [ScreenGui](/docs/reference/engine/classes/ScreenGui) located inside the [StarterGui](/docs/reference/engine/classes/StarterGui)
container.

```
local CollectionService = game:GetService("CollectionService")



local ReplicatedStorage = game:GetService("ReplicatedStorage")



local screenGui = script.Parent



local coreSheet = Instance.new("StyleSheet")



coreSheet.Parent = ReplicatedStorage



local styleLink = Instance.new("StyleLink")



styleLink.StyleSheet = coreSheet



styleLink.Parent = screenGui



local rule = Instance.new("StyleRule")



rule.Parent = coreSheet



-- UI component selector



rule.Selector = "Frame.RoundedCorner20::UICorner"



-- Set rule property



rule:SetProperty("CornerRadius", UDim.new(0, 20))



-- Create frame



local frame = Instance.new("Frame")



frame.Size = UDim2.new(0.4, 0, 0.2, 0)



frame.Parent = screenGui



-- Apply tag to frame



CollectionService:AddTag(frame, "RoundedCorner20")
```

Provide feedback

---

SelectorError

Read Only

Not Replicated

Read Parallel

A read-only string that displays errors from the
[Selector](/docs/reference/engine/classes/StyleRule#Selector) property.

StyleRule.SelectorError:[string](/docs/luau/strings)

A read-only string that displays errors from the
[Selector](/docs/reference/engine/classes/StyleRule#Selector) property such as syntax errors,
unsupported class types, etc.

Provide feedback

---

Methods

GetProperties

Returns a dictionary of key-value pairs describing the properties of the
StyleRule.

StyleRule:GetProperties():[Dictionary](/docs/luau/tables#dictionaries)

Returns

[Dictionary](/docs/luau/tables#dictionaries)

Dictionary of key-value pairs describing the properties of the
StyleRule.

Returns a dictionary of key-value pairs describing the properties of the
StyleRule, for example:

```
local ReplicatedStorage = game:GetService("ReplicatedStorage")



local coreSheet = ReplicatedStorage:FindFirstChild("CoreSheet")



-- Get reference to style rule



local frameRule = coreSheet.Frame



local props = frameRule:GetProperties()



print(props)



--[[



{



["AnchorPoint"] = 0.5, 0,



["BackgroundColor3"] = 1, 0, 0.25



}



]]
```

Provide feedback

---

GetProperty

Returns the value of a specific property in the StyleRule.

StyleRule:GetProperty(name:[string](/docs/luau/strings)):Variant

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  String name of the property, for example "AnchorPoint" or "BackgroundColor3". |

Returns

Variant

Value of the property.

Returns the value of a specific property in the StyleRule.

```
local ReplicatedStorage = game:GetService("ReplicatedStorage")



local coreSheet = ReplicatedStorage:FindFirstChild("CoreSheet")



-- Get reference to style rule



local frameRule = coreSheet.Frame



local prop = frameRule:GetProperty("AnchorPoint")



print(prop) --> 0.5, 0
```

Provide feedback

---

SetProperties

Lets you declare and set multiple properties of the StyleRule at once.

StyleRule:SetProperties(styleProperties:[Dictionary](/docs/luau/tables#dictionaries)):()

Parameters

|  |
| --- |
| styleProperties:[Dictionary](/docs/luau/tables#dictionaries)  Dictionary of key-value pairs defining the properties to set. |

Returns

()

Similar to [SetProperty()](/docs/reference/engine/classes/StyleRule#SetProperty) but lets you
declare and set multiple properties of the StyleRule at once. Each
assignment should be a valid property of the affected [GuiObject](/docs/reference/engine/classes/GuiObject) or
[UIComponent](/docs/reference/engine/classes/UIComponent) ([UICorner](/docs/reference/engine/classes/UICorner), [UIGradient](/docs/reference/engine/classes/UIGradient), etc.), and each
assigned value should match its property's value type, for example
[Vector2](/docs/reference/engine/datatypes/Vector2) for [AnchorPoint](/docs/reference/engine/classes/GuiObject#AnchorPoint) or
[Color3](/docs/reference/engine/datatypes/Color3) for [BackgroundColor3](/docs/reference/engine/classes/GuiObject#BackgroundColor3).

Attempts to assign invalid property names such as "AnchorPt" or
"BkColor" will silently fail. Type mismatches such as [CFrame](/docs/reference/engine/datatypes/CFrame)
for [AnchorPoint](/docs/reference/engine/classes/GuiObject#AnchorPoint) or [UDim2](/docs/reference/engine/datatypes/UDim2) for
[BackgroundColor3](/docs/reference/engine/classes/GuiObject#BackgroundColor3) will also fail and an
error will appear in the [Output](/docs/studio/output) window.

To set/update just one property of a StyleRule, see
[SetProperty()](/docs/reference/engine/classes/StyleRule#SetProperty).

```
local ReplicatedStorage = game:GetService("ReplicatedStorage")



local coreSheet = ReplicatedStorage:FindFirstChild("CoreSheet")



-- Get reference to style rule



local frameRule = coreSheet.Frame



-- Set rule properties



frameRule:SetProperties({



["AnchorPoint"] = Vector2.new(0.5, 0),



["BackgroundColor3"] = Color3.new(1, 0, 0.25)



})
```

Note that you can assign tokens as property values through the $
prefix:

```
local ReplicatedStorage = game:GetService("ReplicatedStorage")



local coreSheet = ReplicatedStorage:FindFirstChild("CoreSheet")



local tokensSheet = ReplicatedStorage:FindFirstChild("Tokens")



-- Set tokens (attributes) on tokens sheet



tokensSheet:SetAttribute("TopCenterAnchor", Vector2.new(0.5, 0))



tokensSheet:SetAttribute("MainBackgroundColor", Color3.new(0.2, 0.2, 0.3))



-- Get reference to style rule



local frameRule = coreSheet.Frame



-- Set rule properties



frameRule:SetProperties({



["AnchorPoint"] = "$TopCenterAnchor",



["BackgroundColor3"] = "$MainBackgroundColor"



})
```

Provide feedback

---

SetProperty

StyleRule:SetProperty(

name:[string](/docs/luau/strings), value:Variant

):()

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  Property name to set, for example "BackgroundColor3". |
| value:Variant  Property value to set, for example [Color3.new(1, 0, 0.25)](/docs/reference/engine/datatypes/Color3#new). |

Returns

()

Sets a new property (or modifies an existing property) for the
StyleRule. The name parameter should be a valid property of the
affected [GuiObject](/docs/reference/engine/classes/GuiObject) or [UIComponent](/docs/reference/engine/classes/UIComponent) ([UICorner](/docs/reference/engine/classes/UICorner),
[UIGradient](/docs/reference/engine/classes/UIGradient), etc.), and the assigned value should match the
property's value type, for example [Vector2](/docs/reference/engine/datatypes/Vector2) for
[AnchorPoint](/docs/reference/engine/classes/GuiObject#AnchorPoint) or [Color3](/docs/reference/engine/datatypes/Color3) for
[BackgroundColor3](/docs/reference/engine/classes/GuiObject#BackgroundColor3).

Attempts to assign invalid property names such as "AnchorPt" or
"BkColor" will silently fail. Type mismatches such as [CFrame](/docs/reference/engine/datatypes/CFrame)
for [AnchorPoint](/docs/reference/engine/classes/GuiObject#AnchorPoint) or [UDim2](/docs/reference/engine/datatypes/UDim2) for
[BackgroundColor3](/docs/reference/engine/classes/GuiObject#BackgroundColor3) will also fail and an
error will appear in the [Output](/docs/studio/output) window.

To set multiple properties for a StyleRule at once, see
[SetProperties()](/docs/reference/engine/classes/StyleRule#SetProperties).

```
local ReplicatedStorage = game:GetService("ReplicatedStorage")



local coreSheet = ReplicatedStorage:FindFirstChild("CoreSheet")



-- Get reference to style rule



local frameRule = coreSheet.Frame



-- Set rule property



frameRule:SetProperty("BackgroundColor3", Color3.new(1, 0, 0.25))
```

Note that you can assign tokens as property values through the $
prefix:

```
local ReplicatedStorage = game:GetService("ReplicatedStorage")



local coreSheet = ReplicatedStorage:FindFirstChild("CoreSheet")



local tokensSheet = ReplicatedStorage:FindFirstChild("Tokens")



-- Set new token (attribute) on tokens sheet



tokensSheet:SetAttribute("MainBackgroundColor", Color3.new(0.2, 0.2, 0.3))



-- Get reference to style rule



local frameRule = coreSheet.Frame



-- Set rule property to use the token as its value



frameRule:SetProperty("BackgroundColor3, "$MainBackgroundColor")
```

Provide feedback

---