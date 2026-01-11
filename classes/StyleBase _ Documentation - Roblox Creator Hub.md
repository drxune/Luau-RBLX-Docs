# StyleBase | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/StyleBase
Scraped: 2026-01-11T02:30:00.834687Z

## Tags
- Not Creatable

## Inherits
- Object
- Instance
- StyleBase
- StyleSheet
- StyleRule
- StyleRules
- Priority
- InsertStyleRule()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [StyleBase](/docs/reference/engine/classes/StyleBase)

English

Feedback

Engine Class

StyleBase

The base class for [StyleSheet](/docs/reference/engine/classes/StyleSheet) and [StyleRule](/docs/reference/engine/classes/StyleRule).

Not Creatable

---

Summary

Methods

|  |
| --- |
| [GetStyleRules](#GetStyleRules)():Instances |
| [InsertStyleRule](#InsertStyleRule)(rule: [StyleRule](/docs/reference/engine/classes/StyleRule),priority: [number](/docs/luau/numbers)?):() |
| [SetStyleRules](#SetStyleRules)(rules: Instances):() |

Events

|  |
| --- |
| [StyleRulesChanged](#StyleRulesChanged)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[StyleRule](/docs/reference/engine/classes/StyleRule), [StyleSheet](/docs/reference/engine/classes/StyleSheet)

The base class for [StyleSheet](/docs/reference/engine/classes/StyleSheet) and [StyleRule](/docs/reference/engine/classes/StyleRule). Holds a list of
child [StyleRules](/docs/reference/engine/classes/StyleRule), as well as token definitions which are
stored as [attributes](/docs/studio/properties#instance-attributes).

---

API Reference

Methods

GetStyleRules

Returns an array of associated [StyleRules](/docs/reference/engine/classes/StyleRule).

StyleBase:GetStyleRules():Instances

Returns

Instances

Array of [StyleRules](/docs/reference/engine/classes/StyleRule).

Returns an array of associated [StyleRules](/docs/reference/engine/classes/StyleRule).

Provide feedback

---

InsertStyleRule

Inserts a new [StyleRule](/docs/reference/engine/classes/StyleRule) into the array of rules.

StyleBase:InsertStyleRule(

rule:[StyleRule](/docs/reference/engine/classes/StyleRule), priority:[number](/docs/luau/numbers)?

):()

Parameters

|  |
| --- |
| rule:[StyleRule](/docs/reference/engine/classes/StyleRule)  The [StyleRule](/docs/reference/engine/classes/StyleRule) to insert. |
| priority:[number](/docs/luau/numbers)?  The number to set the rule's [Priority](/docs/reference/engine/classes/StyleRule#Priority) to. |

Returns

()

Inserts a new [StyleRule](/docs/reference/engine/classes/StyleRule) into the array of rules so that its
[Priority](/docs/reference/engine/classes/StyleRule#Priority) is greater than all previous
[StyleRules](/docs/reference/engine/classes/StyleRule). If priority is specified, sets the new
rule's [Priority](/docs/reference/engine/classes/StyleRule#Priority) to the specified value.

Provide feedback

---

SetStyleRules

Similar to [InsertStyleRule()](/docs/reference/engine/classes/StyleBase#InsertStyleRule) but lets
you declare and set multiple [StyleRules](/docs/reference/engine/classes/StyleRule) at once.

StyleBase:SetStyleRules(rules:Instances):()

Parameters

|  |
| --- |
| rules:Instances  Array of [StyleRules](/docs/reference/engine/classes/StyleRule) to set. |

Returns

()

Similar to [InsertStyleRule()](/docs/reference/engine/classes/StyleBase#InsertStyleRule) but lets
you declare and set multiple [StyleRules](/docs/reference/engine/classes/StyleRule) at once.

```
local ReplicatedStorage = game:GetService("ReplicatedStorage")



local coreSheet = Instance.new("StyleSheet")



coreSheet.Name = "CoreSheet"



coreSheet.Parent = ReplicatedStorage



local styleRuleA = Instance.new("StyleRule")



styleRuleA.Selector = "Frame"



styleRuleA:SetProperty("BackgroundColor3", Color3.new(1, 0, 0))



local styleRuleB = Instance.new("StyleRule")



styleRuleB.Selector = "Frame"



styleRuleB:SetProperty("BackgroundColor3", Color3.new(0, 1, 0))



coreSheet:SetStyleRules({ styleRuleA, styleRuleB })
```

Provide feedback

---

Events

StyleRulesChanged

Fires when one or more [StyleRules](/docs/reference/engine/classes/StyleRule) is explicitly changed
on the connected [StyleSheet](/docs/reference/engine/classes/StyleSheet) or [StyleRule](/docs/reference/engine/classes/StyleRule).

StyleBase.StyleRulesChanged():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Fires when one or more [StyleRules](/docs/reference/engine/classes/StyleRule) is explicitly changed
on the connected [StyleSheet](/docs/reference/engine/classes/StyleSheet) or [StyleRule](/docs/reference/engine/classes/StyleRule), for example when
[InsertStyleRule()](/docs/reference/engine/classes/StyleBase#InsertStyleRule) is called.

Provide feedback

---