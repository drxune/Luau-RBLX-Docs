# LocalizationTable | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/LocalizationTable
Scraped: 2026-01-11T02:33:34.900359Z

## Inherits
- Instance
- LocalizationTable
- Object
- Translator
- LocalizationService
- LocalizationTable.SourceLocaleId
- GuiBase2d.RootLocalizationTable
- LocalizationTable:SetEntries()
- Instance:GetFullName()
- LocalizationTable:GetEntries()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [LocalizationTable](/docs/reference/engine/classes/LocalizationTable)

English

Feedback

Engine Class

![LocalizationTable](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/LocalizationTable-Dark.webp)LocalizationTable

A LocalizationTable is a database of translations. It contains source strings
and translations for various languages.

---

Summary

Properties

|  |
| --- |
| [DevelopmentLanguage](#DevelopmentLanguage):[string](/docs/luau/strings)  Deprecated |
| [Root](#Root):[Instance](/docs/reference/engine/datatypes/Instance)  Deprecated |
| [SourceLocaleId](#SourceLocaleId):[string](/docs/luau/strings) |

Methods

|  |
| --- |
| [GetContents](#GetContents)():[string](/docs/luau/strings)  Deprecated |
| [GetEntries](#GetEntries)():[Array](/docs/luau/tables#arrays) |
| [GetString](#GetString)(targetLocaleId: [string](/docs/luau/strings),key: [string](/docs/luau/strings)):[string](/docs/luau/strings)  Deprecated |
| [GetTranslator](#GetTranslator)(localeId: [string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [RemoveEntry](#RemoveEntry)(key: [string](/docs/luau/strings),source: [string](/docs/luau/strings),context: [string](/docs/luau/strings)):() |
| [RemoveEntryValue](#RemoveEntryValue)(key: [string](/docs/luau/strings),source: [string](/docs/luau/strings),context: [string](/docs/luau/strings),localeId: [string](/docs/luau/strings)):() |
| [RemoveKey](#RemoveKey)(key: [string](/docs/luau/strings)):()  Deprecated |
| [RemoveTargetLocale](#RemoveTargetLocale)(localeId: [string](/docs/luau/strings)):() |
| [SetContents](#SetContents)(contents: [string](/docs/luau/strings)):()  Deprecated |
| [SetEntries](#SetEntries)(entries: Variant):() |
| [SetEntry](#SetEntry)(key: [string](/docs/luau/strings),targetLocaleId: [string](/docs/luau/strings),text: [string](/docs/luau/strings)):()  Deprecated |
| [SetEntryContext](#SetEntryContext)(key: [string](/docs/luau/strings),source: [string](/docs/luau/strings),context: [string](/docs/luau/strings),newContext: [string](/docs/luau/strings)):() |
| [SetEntryExample](#SetEntryExample)(key: [string](/docs/luau/strings),source: [string](/docs/luau/strings),context: [string](/docs/luau/strings),example: [string](/docs/luau/strings)):() |
| [SetEntryKey](#SetEntryKey)(key: [string](/docs/luau/strings),source: [string](/docs/luau/strings),context: [string](/docs/luau/strings),newKey: [string](/docs/luau/strings)):() |
| [SetEntrySource](#SetEntrySource)(key: [string](/docs/luau/strings),source: [string](/docs/luau/strings),context: [string](/docs/luau/strings),newSource: [string](/docs/luau/strings)):() |
| [SetEntryValue](#SetEntryValue)(key: [string](/docs/luau/strings),source: [string](/docs/luau/strings),context: [string](/docs/luau/strings),localeId: [string](/docs/luau/strings),text: [string](/docs/luau/strings)):() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A LocalizationTable is a database of translations. It contains source strings
and translations for various languages. It is used with the [Translator](/docs/reference/engine/classes/Translator)
and [LocalizationService](/docs/reference/engine/classes/LocalizationService) auto-translator system to control text
translations in the game. LocalizationTables are designed to be treated as
resources, like a texture or a script. They are not optimized to be modified
at runtime. Changing the contents of a table will cause the entire contents of
the table to be replicated to all players.

LocalizationTable Entries
-------------------------

Each LocalizationTable contains a set of entries. Each entry contains the
translations of the text, along with some special fields:

* Key is an optional unique key for fast hash lookups in code. If it is
  non-empty it must be unique in the table.
* Source is the original text in the source language that will be used by
  the [LocalizationService](/docs/reference/engine/classes/LocalizationService) automatic text replacement system to match
  GUI text and render a translation instead. The Source field can be filled by
  the text capture tools, or can be set manually. For key-based lookups the
  Source value can be used as a translation for
  [LocalizationTable.SourceLocaleId](/docs/reference/engine/classes/LocalizationTable#SourceLocaleId) if the entry doesn't have a
  translation for that locale. If Source is empty then the entry will not be
  used by the automatic replacement system.
* Context is the full Instance name for the object that the text appeared
  on. Context is used for disambiguation by the automatic text replacement
  system. When multiple matches for the Source are found, the system will pick
  the best match by matching backwards from the end of the Context string.
  There are other more robust ways to handle disambiguation available as well,
  like using multiple tables with [GuiBase2d.RootLocalizationTable](/docs/reference/engine/classes/GuiBase2d#RootLocalizationTable).
* Example is whatever you want it to be. If the text capture tool guessed
  some parameters for a string the Example field will contain an example of
  them used in context.

All of these fields are optional, but at least either Key or Source must be
non-empty. No two entries can have the same Key, Source, and Context.

See
[Translating Dynamic Content](/docs/production/localization/translate-dynamic-content)
for more information.

Code Samples

LocalizationTable

```
local LocalizationService = game:GetService("LocalizationService")



local function createLocalizationTable(entries)



local localTable = Instance.new("LocalizationTable")



localTable.DevelopmentLanguage = LocalizationService.SystemLocaleId



localTable:SetEntries(entries)



return localTable



end



local entries = {



{



Key = "Hello_World", -- The 'expressionKey' to be used with GetString



Values = { -- A dictionary of keys corresponding to IETF language tags, and their translations.



["ru"] = " !", -- Russian



["fr"] = "Bonjour le monde!", -- French



["de"] = "Hallo Welt!", -- German



["en-US"] = "Hello world!", -- English



["it"] = "Ciao mondo!", -- Italian



["pt-BR"] = "Ol Mundo!", -- Portuguese



["ja"] = "", -- Japanese



["es"] = "Hola Mundo!", -- Spanish



},



},



}



local helloWorldTable = createLocalizationTable(entries)



print(helloWorldTable:GetString("en-US", "Hello_World"))
```

---

API Reference

Properties

DevelopmentLanguage

Deprecated

Show details

---

Root

Deprecated

Show details

---

SourceLocaleId

Read Parallel

The locale of source strings.

LocalizationTable.SourceLocaleId:[string](/docs/luau/strings)

The Roblox locale of the input key strings for this table, for example
"en-us" or "es-es." This is typically the "development language" of the
game. For a Translator that merges multiple LocalizationTable objects,
it's the LocaleId of the Default LocalizationTable. Defaults to "en-us".

Provide feedback

---

Methods

GetContents

Deprecated

Show details

---

GetEntries

Returns an array of dictionaries, where each dictionary represents an
entry of localization data.

LocalizationTable:GetEntries():[Array](/docs/luau/tables#arrays)

Returns

[Array](/docs/luau/tables#arrays)

An array of dictionaries, where each dictionary represents an entry of
localization data.

The GetEntries function returns an array of dictionaries contained in a
given [LocalizationTable](/docs/reference/engine/classes/LocalizationTable), where each dictionary represents an entry
of localization data.

To set the entries of a LocalizationTable, you can use
[LocalizationTable:SetEntries()](/docs/reference/engine/classes/LocalizationTable#SetEntries).

Each dictionary in the array contains the following fields:

| Index | Type | Description |
| --- | --- | --- |
| **Key** | [string](/docs/reference/engine/libraries/string) | A lookup key for this specific entry in the LocalizationTable. |
| **Source** | [string](/docs/reference/engine/libraries/string) | The string used to format the localized string. Used as a lookup if a key is not provided. |
| **Context** | [string](/docs/reference/engine/libraries/string) | An [Instance:GetFullName()](/docs/reference/engine/classes/Instance#GetFullName) path to the object that was used to generate the LocalizationTable. Used as a lookup if a key is not provided. |
| **Example** | [string](/docs/reference/engine/libraries/string) | The string used to format the localization. Optional. |
| **Values** | Dictionary | A dictionary of language translations for this localization entry. The keys of this dictionary are locale ids, and the values are strings that are used to apply localization for the language corresponding to the locale id. |

Code Samples

Using a LocalizationTable

The following code sample creates a LocalizationTable, sets its entries,
then gets and displays its entries. In order for this example to work, a
LocalizationTable instance must be located inside the LocalizationService
service.

The *entries* variable is a table of dictionaries, each with the format
required to create a LocalizationTable with
[LocalizationTable:SetEntries()](/docs/reference/engine/classes/LocalizationTable#SetEntries).

The *get\_results* variable is a table of dictionaries - the same table that we
created with the *entries* variable. We then loop through each of the tables
in this dictionary to display its *Values*/strings.

```
local LocalizationService = game:GetService("LocalizationService")



local localizationTable = LocalizationService:FindFirstChild("LocalizationTable")



local entries = {



{



["Key"] = "0001",



["Source"] = "en-us",



["Values"] = {



["0001"] = "Hello Muddah, hello Fadduh.",



["0002"] = "Here I am at Camp Granada.",



["0003"] = "Camp is very entertaining.",



["0004"] = "And they say we'll have some fun if it stops raining.",



},



},



}



localizationTable:SetEntries(entries)



local get_results = localizationTable:GetEntries()



for _index, dict in pairs(get_results) do



for _key, value in pairs(dict["Values"]) do -- Loop through every key, value pair in the dictionary to print our strings



print(value)



end



end
```

Provide feedback

---

GetString

Deprecated

Show details

---

GetTranslator

Returns a [Translator](/docs/reference/engine/classes/Translator) for entries in this LocalizationTable, in the
specified language.

LocalizationTable:GetTranslator(localeId:[string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| localeId:[string](/docs/luau/strings) |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

Returns a [Translator](/docs/reference/engine/classes/Translator) for entries in this LocalizationTable, in the
specified language. The translator will first search in this table and
then look in ancestor tables.

Provide feedback

---

RemoveEntry

Removes an entry from the LocalizationTable, using the specified key,
source, and context to narrow down the specific entry to be removed.

LocalizationTable:RemoveEntry(

key:[string](/docs/luau/strings), source:[string](/docs/luau/strings), context:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings) |
| source:[string](/docs/luau/strings) |
| context:[string](/docs/luau/strings) |

Returns

()

Removes an entry from the LocalizationTable, using the specified key,
source, and context to narrow down the specific entry to be removed.

Provide feedback

---

RemoveEntryValue

Removes a single language translation from the LocalizationTable, using
the provided key, source, context, and localeId to narrow down the
specific entry to be removed.

LocalizationTable:RemoveEntryValue(

key:[string](/docs/luau/strings), source:[string](/docs/luau/strings), context:[string](/docs/luau/strings), localeId:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings) |
| source:[string](/docs/luau/strings) |
| context:[string](/docs/luau/strings) |
| localeId:[string](/docs/luau/strings) |

Returns

()

Removes a single language translation from the LocalizationTable, using
the provided key, source, context, and localeId to narrow down the
specific entry to be removed.

Provide feedback

---

RemoveKey

Deprecated

Show details

---

RemoveTargetLocale

Removes all translations from the LocalizationTable with the specified
localeId.

LocalizationTable:RemoveTargetLocale(localeId:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| localeId:[string](/docs/luau/strings) |

Returns

()

Removes all translations from the LocalizationTable with the specified
localeId.

Provide feedback

---

SetContents

Deprecated

Show details

---

SetEntries

Sets the contents of the LocalizationTable.

LocalizationTable:SetEntries(entries:Variant):()

Parameters

|  |
| --- |
| entries:Variant |

Returns

()

Sets the contents of the LocalizationTable.

The entries parameter should be an array of dictionaries in the same
format as the one returned from the [LocalizationTable:GetEntries()](/docs/reference/engine/classes/LocalizationTable#GetEntries)
function.

Provide feedback

---

SetEntry

Deprecated

Show details

---

SetEntryContext

Sets the Context field of a LocalizationTable entry to newContext,
using the specified key, source, and context to narrow down the
entry that will have this change applied.

LocalizationTable:SetEntryContext(

key:[string](/docs/luau/strings), source:[string](/docs/luau/strings), context:[string](/docs/luau/strings), newContext:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings) |
| source:[string](/docs/luau/strings) |
| context:[string](/docs/luau/strings) |
| newContext:[string](/docs/luau/strings) |

Returns

()

Sets the Context field of a LocalizationTable entry to newContext,
using the specified key, source, and context to narrow down the
entry that will have this change applied.

Provide feedback

---

SetEntryExample

Sets the Example field of a LocalizationTable entry to example,
using the specified key, source, and context to narrow down the
entry that will have this change applied.

LocalizationTable:SetEntryExample(

key:[string](/docs/luau/strings), source:[string](/docs/luau/strings), context:[string](/docs/luau/strings), example:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings) |
| source:[string](/docs/luau/strings) |
| context:[string](/docs/luau/strings) |
| example:[string](/docs/luau/strings) |

Returns

()

Sets the Example field of a LocalizationTable entry to example,
using the specified key, source, and context to narrow down the
entry that will have this change applied.

Provide feedback

---

SetEntryKey

Sets the Key field of a LocalizationTable entry to newKey, using the
specified key, source, and context to narrow down the entry that
will have this change applied.

LocalizationTable:SetEntryKey(

key:[string](/docs/luau/strings), source:[string](/docs/luau/strings), context:[string](/docs/luau/strings), newKey:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings) |
| source:[string](/docs/luau/strings) |
| context:[string](/docs/luau/strings) |
| newKey:[string](/docs/luau/strings) |

Returns

()

Sets the Key field of a LocalizationTable entry to newKey, using the
specified key, source, and context to narrow down the entry that
will have this change applied.

Provide feedback

---

SetEntrySource

Sets the Source field of a LocalizationTable entry to newSource,
using the specified key, source, and context to narrow down the
entry that will have this change applied.

LocalizationTable:SetEntrySource(

key:[string](/docs/luau/strings), source:[string](/docs/luau/strings), context:[string](/docs/luau/strings), newSource:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings) |
| source:[string](/docs/luau/strings) |
| context:[string](/docs/luau/strings) |
| newSource:[string](/docs/luau/strings) |

Returns

()

Sets the Source field of a LocalizationTable entry to newSource,
using the specified key, source, and context to narrow down the
entry that will have this change applied.

Provide feedback

---

SetEntryValue

Sets the text of the specified localeId in a LocalizationTable entry,
using the specified key, source, and context to narrow down the
entry that will have this change applied.

LocalizationTable:SetEntryValue(

key:[string](/docs/luau/strings), source:[string](/docs/luau/strings), context:[string](/docs/luau/strings), localeId:[string](/docs/luau/strings), text:[string](/docs/luau/strings)

):()

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings) |
| source:[string](/docs/luau/strings) |
| context:[string](/docs/luau/strings) |
| localeId:[string](/docs/luau/strings) |
| text:[string](/docs/luau/strings) |

Returns

()

Sets the text of the specified localeId in a LocalizationTable entry,
using the specified key, source, and context to narrow down the
entry that will have this change applied.

Provide feedback

---