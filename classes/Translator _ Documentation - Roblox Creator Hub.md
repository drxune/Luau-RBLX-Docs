# Translator | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Translator
Scraped: 2026-01-11T02:35:24.215529Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- Instance
- Translator
- LocalizationTable
- Translator.LocaleId
- LocalizationTables
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Translator](/docs/reference/engine/classes/Translator)

English

Feedback

Engine Class

Translator

The role of a Translator is to manufacture/return strings localized for the
viewing player.

Not Creatable

Not Replicated

---

Summary

Properties

|  |
| --- |
| [LocaleId](#LocaleId):[string](/docs/luau/strings) |

Methods

|  |
| --- |
| [FormatByKey](#FormatByKey)(key: [string](/docs/luau/strings),args: Variant):[string](/docs/luau/strings) |
| [Translate](#Translate)(context: [Instance](/docs/reference/engine/datatypes/Instance),text: [string](/docs/luau/strings)):[string](/docs/luau/strings) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The role of a Translator is to manufacture/return strings localized for the
viewing player. It can be used to retrieve display-ready localized text from a
[LocalizationTable](/docs/reference/engine/classes/LocalizationTable). The source of the [Translator.LocaleId](/docs/reference/engine/classes/Translator#LocaleId)
property, the set of tables it will search, and the order it will search them
in depends on which method was used to create the Translator instance.

The input for a Translator is the original development language string and a
context, where all or part of the context can be used to find a more
precise/situational translation for the source string.

The Translator can also be used to manufacture translated strings with inserts
(data replacements) which may change order based on the target language.

---

API Reference

Properties

LocaleId

Read Only

Not Replicated

Read Parallel

The locale of translated strings.

Translator.LocaleId:[string](/docs/luau/strings)

The Roblox locale of the output translated strings from this table, for
example "en-us" or "es-es." Defaults to "en-us".

Provide feedback

---

Methods

FormatByKey

Returns the localized text string in a [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) based on
its [Translator](/docs/reference/engine/classes/Translator) locale, by key.

Translator:FormatByKey(

key:[string](/docs/luau/strings), args:Variant

):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings)  The Key value to look up and translate. |
| args:Variant  To be provided if the Source text and translations contain format strings. Will be a Luau table of values or key-value pairs, depending on whether the format strings are numbered or named. |

Returns

[string](/docs/luau/strings)

Returns the localized text string in a [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) based on
its [Translator](/docs/reference/engine/classes/Translator) locale, by key. The optional args table is used
for filling format parameters in the matching text entry.

Note that this method will throw an error in the following cases:

* If none of the [LocalizationTables](/docs/reference/engine/classes/LocalizationTable) available to
  this [Translator](/docs/reference/engine/classes/Translator) include a value for the given key.
* If the
  [format string](/docs/production/localization/translate-dynamic-content)
  for the key uses numbered parameters and args is not an array.
* If the
  [format string](/docs/production/localization/translate-dynamic-content)
  uses named parameters and args is not a table of key-value pairs.
* If args is missing values for parameters that are used in the
  matching
  [format string](/docs/production/localization/translate-dynamic-content).

See
[Localize with scripting](/docs/production/localization/localize-with-scripting)
for more details and usage examples of this function.

Provide feedback

---

Translate

Returns the localized text string in a [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) based on
its [Translator](/docs/reference/engine/classes/Translator) locale, by source lookup.

Translator:Translate(

context:[Instance](/docs/reference/engine/datatypes/Instance), text:[string](/docs/luau/strings)

):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| context:[Instance](/docs/reference/engine/datatypes/Instance)  A valid in-game [Instance](/docs/reference/engine/classes/Instance) to use for context override as outlined above. Note that this argument can be arbitrary, for example game, if you don't require a context override. |
| text:[string](/docs/luau/strings)  The Source text to look up and translate. |

Returns

[string](/docs/luau/strings)

The translated text.

Returns the localized text string in a [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) based on
its [Translator](/docs/reference/engine/classes/Translator) locale. This string will be in the context of the
provided object, given the provided Source text.

See
[Localize with scripting](/docs/production/localization/localize-with-scripting)
for more details and usage examples of this function.

#### Context Overrides

In some cases, duplicate Source strings may have completely different
translations in other languages. For example, the English noun "Screen"
can indicate both a computer screen and a window screen, but the Spanish
translations are completely different:

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| A | B | C | D | E |
| Key | Context | **Source** | Example | **es** |
|  |  | Screen |  | Pantalla |
|  |  | Screen |  | Mosquitero |
|  |  |  |  |  |

In these cases, the first argument to this function — a valid
in-game [Instance](/docs/reference/engine/classes/Instance) — can be used as a "tie breaker" when
multiple GUI objects use the same source string. To implement this,
specify the "path" to the [Instance](/docs/reference/engine/classes/Instance) you'd like to override as the
Context value of the translation data:

|  |  |  |  |  |
| --- | --- | --- | --- | --- |
| A | B | C | D | E |
| Key | **Context** | Source | Example | es |
|  | workspace.ComputerScreen.SurfaceGui.TextLabel | Screen |  | Pantalla |
|  |  | Screen |  | Mosquitero |
|  |  |  |  |  |

Then, when calling this function in a script, pass the same
[Instance](/docs/reference/engine/classes/Instance) as the first argument, followed by the Source lookup
text as the second argument:

```
local Players = game:GetService("Players")



local LocalizationService = game:GetService("LocalizationService")



local success, translator = pcall(function()



return LocalizationService:GetTranslatorForPlayerAsync(Players.LocalPlayer)



end)



if success then



local trans = translator:Translate(workspace.ComputerScreen.SurfaceGui.TextLabel, "Screen")



print(trans)



else



warn("Cannot load translator for player!")



end
```

Provide feedback

---