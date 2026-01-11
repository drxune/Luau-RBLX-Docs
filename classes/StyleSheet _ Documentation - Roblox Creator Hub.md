# StyleSheet | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/StyleSheet
Scraped: 2026-01-11T02:37:50.354865Z

## Inherits
- StyleBase
- StyleSheet
- StyleRules
- DataModel
- Instance
- Object
- StyleDerive
- ReplicatedStorage
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [StyleBase](/docs/reference/engine/classes/StyleBase)
6. /
7. [StyleSheet](/docs/reference/engine/classes/StyleSheet)

English

Feedback

Engine Class

![StyleSheet](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/StyleSheet-Dark.webp)StyleSheet

Aggregates [StyleRules](/docs/reference/engine/classes/StyleRule) and can be linked to [DataModel](/docs/reference/engine/classes/DataModel)
trees to apply style properties to instances.

---

Summary

Methods

|  |
| --- |
| [GetDerives](#GetDerives)():Instances |
| [SetDerives](#SetDerives)(derives: Instances):() |

Inherited Members

4 inherited from [StyleBase](/docs/reference/engine/classes/StyleBase)

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Aggregates [StyleRules](/docs/reference/engine/classes/StyleRule) and can be linked to [DataModel](/docs/reference/engine/classes/DataModel)
trees to apply style properties to instances. Note that a StyleSheet may
exist outside the [DataModel](/docs/reference/engine/classes/DataModel), but it cannot be derived or linked to a
[DataModel](/docs/reference/engine/classes/DataModel) tree in such a case.

---

API Reference

Methods

GetDerives

Returns an array of other StyleSheets from which the StyleSheet is
deriving [StyleRules](/docs/reference/engine/classes/StyleRule) and token definitions.

StyleSheet:GetDerives():Instances

Returns

Instances

Array of other StyleSheets.

Returns an array of other StyleSheets from which the StyleSheet is
deriving [StyleRules](/docs/reference/engine/classes/StyleRule) and token definitions.

Provide feedback

---

SetDerives

Sets the StyleSheet to derive [StyleRules](/docs/reference/engine/classes/StyleRule) and token
definitions from one or more other StyleSheets.

StyleSheet:SetDerives(derives:Instances):()

Parameters

|  |
| --- |
| derives:Instances  Array of other StyleSheets to derive [StyleRules](/docs/reference/engine/classes/StyleRule) and token definitions from. |

Returns

()

Sets the StyleSheet to derive [StyleRules](/docs/reference/engine/classes/StyleRule) and token
definitions from one or more other StyleSheets in the order they are
listed. This method spawns the appropriate [StyleDerive](/docs/reference/engine/classes/StyleDerive) instances
and sets their priorities to establish the specified derivations.

```
local ReplicatedStorage = game:GetService("ReplicatedStorage")



local coreSheet = ReplicatedStorage:FindFirstChild("CoreSheet")



-- Create a tokens style sheet



local tokensSheet = Instance.new("StyleSheet")



tokensSheet.Name = "Tokens"



tokensSheet.Parent = ReplicatedStorage



-- Set tokens (attributes) on tokens sheet



tokensSheet:SetAttribute("LightGray", Color3.new(0.9, 0.9, 0.9))



tokensSheet:SetAttribute("DarkGray", Color3.new(0.2, 0.2, 0.2))



-- Create theme style sheets



local lightThemeSheet = Instance.new("StyleSheet")



lightThemeSheet.Name = "LightTheme"



lightThemeSheet:SetAttribute("Background", "$LightGray")



lightThemeSheet.Parent = ReplicatedStorage



local darkThemeSheet = Instance.new("StyleSheet")



darkThemeSheet.Name = "DarkTheme"



darkThemeSheet:SetAttribute("Background", "$DarkGray")



darkThemeSheet.Parent = ReplicatedStorage



-- Set theme sheets to derive from tokens sheet



lightThemeSheet:SetDerives({ tokensSheet })



darkThemeSheet:SetDerives({ tokensSheet })



local themeDerive = Instance.new("StyleDerive")



themeDerive.Parent = coreSheet



themeDerive.StyleSheet = lightThemeSheet



-- Function to dynamically change the derived theme for the core sheet



local function changeTheme()



if themeDerive.StyleSheet == lightThemeSheet then



themeDerive.StyleSheet = darkThemeSheet



elseif themeDerive.StyleSheet == darkThemeSheet then



themeDerive.StyleSheet = lightThemeSheet



end



end
```

Note that if you've created a design using the
[Style Editor](/docs/ui/styling/editor), the StyleSheet sheet in
the Design folder of [ReplicatedStorage](/docs/reference/engine/classes/ReplicatedStorage) will contain a
[StyleDerive](/docs/reference/engine/classes/StyleDerive) to the BaseStyleSheet also in the Design
folder. When setting derives with SetDerives(), be sure to include the
base style sheet in the spot of least priority in relation to other
StyleSheets in the derives array.

Provide feedback

---