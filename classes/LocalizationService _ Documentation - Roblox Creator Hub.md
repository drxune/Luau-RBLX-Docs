# LocalizationService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/LocalizationService
Scraped: 2026-01-11T02:31:54.565817Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Instance
- LocalizationService
- Object
- LocalizationTable
- GuiBase2d.RootLocalizationTable
- CoreGui
- Player.LocaleId
- PolicyService:GetPolicyInfoForPlayerAsync()
- LocalizationTable:GetEntries()
- LocalizationTables
- GuiBase2d
- GuiBase2d.AutoLocalize
- Translator
- LocalizationService:GetTableEntries(nil)
- LocalizationService:GetTranslatorForPlayer()
- LocalizationService:GetTranslatorForPlayerAsync()
- LocalizationService:GetTranslatorForLocaleAsync()
- Player
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [LocalizationService](/docs/reference/engine/classes/LocalizationService)

English

Feedback

Engine Class

![LocalizationService](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/LocalizationService-Dark.webp)LocalizationService

Handles automated translation.

Not Creatable

Service

Not Replicated

---

Summary

Properties

|  |
| --- |
| [RobloxLocaleId](#RobloxLocaleId):[string](/docs/luau/strings) |
| [SystemLocaleId](#SystemLocaleId):[string](/docs/luau/strings) |

Methods

|  |
| --- |
| [GetCorescriptLocalizations](#GetCorescriptLocalizations)():Instances |
| [GetCountryRegionForPlayerAsync](#GetCountryRegionForPlayerAsync)(player: [Instance](/docs/reference/engine/datatypes/Instance)):[string](/docs/luau/strings) |
| [GetTableEntries](#GetTableEntries)(instance: [Instance](/docs/reference/engine/datatypes/Instance)):[Array](/docs/luau/tables#arrays) |
| [GetTranslatorForLocaleAsync](#GetTranslatorForLocaleAsync)(locale: [string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance) |
| [GetTranslatorForPlayer](#GetTranslatorForPlayer)(player: [Instance](/docs/reference/engine/datatypes/Instance)):[Instance](/docs/reference/engine/datatypes/Instance)  Deprecated |
| [GetTranslatorForPlayerAsync](#GetTranslatorForPlayerAsync)(player: [Instance](/docs/reference/engine/datatypes/Instance)):[Instance](/docs/reference/engine/datatypes/Instance) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

LocalizationService is the service responsible for handling automated
translation.

It is used as a storage for [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) objects used by
automatic text replacement.

LocalizationService will only use its child LocalizationTables for automatic
text replacement unless [GuiBase2d.RootLocalizationTable](/docs/reference/engine/classes/GuiBase2d#RootLocalizationTable) is specified
on a GUI object or its ancestors.

---

API Reference

Properties

RobloxLocaleId

Read Only

Not Replicated

Read Parallel

The locale ID used for localizing core and internal features.

LocalizationService.RobloxLocaleId:[string](/docs/luau/strings)

This property shows the locale ID used for the localization of core and
internal features such as [CoreGui](/docs/reference/engine/classes/CoreGui). Returns a string with the two
letter code (for example, en-us) for the locale.

Provide feedback

---

SystemLocaleId

Read Only

Not Replicated

Read Parallel

The locale ID that the local player has set for their operating system.

LocalizationService.SystemLocaleId:[string](/docs/luau/strings)

This property shows the locale ID that the local player has set for their
operating system.

This will return a string with the two letter code (for example, "en-us")
for the locale.

See also [Player.LocaleId](/docs/reference/engine/classes/Player#LocaleId), the locale ID that a user has set for
their Roblox account which is used for localizing in-experience content.
This will be a different value when Roblox does not yet internally support
that player's locale.

Provide feedback

---

Methods

GetCorescriptLocalizations

Returns a list of [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) objects used for localizing
core scripts.

LocalizationService:GetCorescriptLocalizations():Instances

Returns

Instances

Returns a list of [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) objects used for localizing
core scripts.

Provide feedback

---

GetCountryRegionForPlayerAsync

Yields

Returns country/region code string according to player's client IP
geolocation.

LocalizationService:GetCountryRegionForPlayerAsync(player:[Instance](/docs/reference/engine/datatypes/Instance)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| player:[Instance](/docs/reference/engine/datatypes/Instance)  The player that you are getting country/region information for. |

Returns

[string](/docs/luau/strings)

A string indicating the country/region code of a player.

Returns a country/region code string according to player's client IP
geolocation. The supported country/region codes are as follows:

| Code | Country/Region |
| --- | --- |
| US | United States |
| GB | United Kingdom |
| CA | Canada |
| AF | Afghanistan |
| AX | Aland Islands |
| AL | Albania |
| DZ | Algeria |
| AS | American Samoa |
| AD | Andorra |
| AO | Angola |
| AI | Anguilla |
| AQ | Antarctica |
| AG | Antigua and Barbuda |
| AR | Argentina |
| AM | Armenia |
| AW | Aruba |
| AU | Australia |
| AT | Austria |
| AZ | Azerbaijan |
| BS | Bahamas |
| BH | Bahrain |
| BD | Bangladesh |
| BB | Barbados |
| BY | Belarus |
| BE | Belgium |
| BZ | Belize |
| BJ | Benin |
| BM | Bermuda |
| BT | Bhutan |
| BO | Bolivia |
| BQ | Bonaire, Saint Eustatius and Saba |
| BA | Bosnia and Herzegovina |
| BW | Botswana |
| BV | Bouvet Island |
| BR | Brazil |
| IO | British Indian Ocean Territory |
| BN | Brunei Darussalam |
| BG | Bulgaria |
| BF | Burkina Faso |
| BI | Burundi |
| KH | Cambodia |
| CM | Cameroon |
| CV | Cape Verde |
| KY | Cayman Islands |
| CF | Central African Republic |
| TD | Chad |
| CL | Chile |
| CN | China |
| CX | Christmas Island |
| CC | Cocos Islands |
| CO | Colombia |
| KM | Comoros |
| CG | Congo |
| CD | Congo (DRC) |
| CK | Cook Islands |
| CR | Costa Rica |
| CI | Ivory Coast |
| HR | Croatia |
| CW | Curaçao |
| CY | Cyprus |
| CZ | Czech Republic |
| DK | Denmark |
| DJ | Djibouti |
| DM | Dominica |
| DO | Dominican Republic |
| EC | Ecuador |
| EG | Egypt |
| SV | El Salvador |
| GQ | Equatorial Guinea |
| ER | Eritrea |
| EE | Estonia |
| ET | Ethiopia |
| FK | Falkland Islands (Malvinas) |
| FO | Faroe Islands |
| FJ | Fiji |
| FI | Finland |
| FR | France |
| GF | French Guiana |
| PF | French Polynesia |
| TF | French Southern Territories |
| GA | Gabon |
| GM | Gambia |
| GE | Georgia |
| DE | Germany |

| Code | Country/Region |
| --- | --- |
| GH | Ghana |
| GI | Gibraltar |
| GR | Greece |
| GL | Greenland |
| GD | Grenada |
| GP | Guadeloupe |
| GU | Guam |
| GT | Guatemala |
| GG | Guernsey |
| GN | Guinea |
| GW | Guinea-Bissau |
| GY | Guyana |
| HT | Haiti |
| HM | Heard Island and the McDonald Islands |
| VA | Holy See |
| HN | Honduras |
| HK | Hong Kong |
| HU | Hungary |
| IS | Iceland |
| IN | India |
| ID | Indonesia |
| IQ | Iraq |
| IE | Ireland |
| IM | Isle of Man |
| IL | Israel |
| IT | Italy |
| JM | Jamaica |
| JP | Japan |
| JE | Jersey |
| JO | Jordan |
| KZ | Kazakhstan |
| KE | Kenya |
| KI | Kiribati |
| KR | Korea |
| KW | Kuwait |
| KG | Kyrgyzstan |
| LA | Laos |
| LV | Latvia |
| LB | Lebanon |
| LS | Lesotho |
| LR | Liberia |
| LY | Libya |
| LI | Liechtenstein |
| LT | Lithuania |
| LU | Luxembourg |
| MO | Macao |
| MK | Macedonia |
| MG | Madagascar |
| MW | Malawi |
| MY | Malaysia |
| MV | Maldives |
| ML | Mali |
| MT | Malta |
| MH | Marshall Islands |
| MQ | Martinique |
| MR | Mauritania |
| MU | Mauritius |
| YT | Mayotte |
| MX | Mexico |
| FM | Micronesia |
| MD | Moldova |
| MC | Monaco |
| MN | Mongolia |
| ME | Montenegro |
| MS | Montserrat |
| MA | Morocco |
| MZ | Mozambique |
| MM | Myanmar |
| NA | Namibia |
| NR | Nauru |
| NP | Nepal |
| NL | Netherlands |
| AN | Netherlands Antilles |
| NC | New Caledonia |
| NZ | New Zealand |
| NI | Nicaragua |
| NE | Niger |
| NG | Nigeria |
| NU | Niue |
| NF | Norfolk Island |
| MP | Northern Mariana Islands |
| NO | Norway |
| OM | Oman |

| Code | Country/Region |
| --- | --- |
| PK | Pakistan |
| PW | Palau |
| PS | Palestine |
| PA | Panama |
| PG | Papua New Guinea |
| PY | Paraguay |
| PE | Peru |
| PH | Philippines |
| PN | Pitcairn Islands |
| PL | Poland |
| PT | Portugal |
| PR | Puerto Rico |
| QA | Qatar |
| RE | Reunion |
| RO | Romania |
| RU | Russian Federation |
| RW | Rwanda |
| BL | Saint Barthelemy |
| SH | Saint Helena, Ascension and Tristan da Cunha |
| KN | Saint Kitts and Nevis |
| LC | Saint Lucia |
| MF | Saint Martin |
| PM | Saint Pierre and Miquelon |
| VC | Saint Vincent and the Grenadines |
| WS | Samoa |
| SM | San Marino |
| ST | Sao Tome and Principe |
| SA | Saudi Arabia |
| SN | Senegal |
| RS | Serbia |
| SC | Seychelles |
| SL | Sierra Leone |
| SG | Singapore |
| SX | Sint Maarten |
| SK | Slovakia |
| SI | Slovenia |
| SB | Solomon Islands |
| SO | Somalia |
| ZA | South Africa |
| GS | South Georgia and the South Sandwich Islands |
| SS | South Sudan |
| ES | Spain |
| LK | Sri Lanka |
| SR | Suriname |
| SJ | Svalbard and Jan Mayen |
| SZ | Swaziland |
| SE | Sweden |
| CH | Switzerland |
| TW | Taiwan |
| TJ | Tajikistan |
| TZ | Tanzania |
| TH | Thailand |
| TL | Timor-Leste |
| TG | Togo |
| TK | Tokelau |
| TO | Tonga |
| TT | Trinidad and Tobago |
| TN | Tunisia |
| TR | Türkiye (Turkey) |
| TM | Turkmenistan |
| TC | Turks and Caicos Islands |
| TV | Tuvalu |
| UG | Uganda |
| UA | Ukraine |
| AE | United Arab Emirates |
| UM | United States Minor Outlying Islands |
| UY | Uruguay |
| UZ | Uzbekistan |
| VU | Vanuatu |
| VE | Venezuela |
| VN | Vietnam |
| VG | Virgin Islands (British) |
| VI | Virgin Islands (US) |
| WF | Wallis and Futuna |
| EH | Western Sahara |
| YE | Yemen |
| ZM | Zambia |
| ZW | Zimbabwe |
| CU | Cuba |
| IR | Iran |
| SY | Syria |
| KP | North Korea |

See also:

* [PolicyService:GetPolicyInfoForPlayerAsync()](/docs/reference/engine/classes/PolicyService#GetPolicyInfoForPlayerAsync), returns policy
  information about a player which is based on geolocation, age group and
  platform

Code Samples

Getting Country/Region Code for a Player

This code sample gets the country/region code for a local player and prints
"Hello, friend from Canada!" if the player's client IP geolocation is Canada.

```
local LocalizationService = game:GetService("LocalizationService")



local Players = game:GetService("Players")



local player = Players.LocalPlayer



local result, code = pcall(LocalizationService.GetCountryRegionForPlayerAsync, LocalizationService, player)



if result and code == "CA" then



print("Hello, friend from Canada!")



else



print("GetCountryRegionForPlayerAsync failed: " .. code)



end
```

Provide feedback

---

GetTableEntries

Gets all entries used for automated localization.

LocalizationService:GetTableEntries(instance:[Instance](/docs/reference/engine/datatypes/Instance)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| instance:[Instance](/docs/reference/engine/datatypes/Instance) Default Value: "nil" |

Returns

[Array](/docs/luau/tables#arrays)

An array of arrays, where each array is in the same format as
described in [LocalizationTable:GetEntries()](/docs/reference/engine/classes/LocalizationTable#GetEntries).

Returns an Array, where each element of the returned Array is itself
an Array of entries in the same format as described in
[LocalizationTable:GetEntries()](/docs/reference/engine/classes/LocalizationTable#GetEntries). The order of the elements in the
returned Array is the same order that the
[LocalizationTables](/docs/reference/engine/classes/LocalizationTable) will be searched through to
attempt automated localization for the provided [Instance](/docs/reference/engine/classes/Instance). The
entry elements within a particular [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) are returned
in an unspecified order.

This function returns entries regardless of whether the object is a
[GuiBase2d](/docs/reference/engine/classes/GuiBase2d) with [GuiBase2d.AutoLocalize](/docs/reference/engine/classes/GuiBase2d#AutoLocalize) enabled. An object
that is a [GuiBase2d](/docs/reference/engine/classes/GuiBase2d) will not actually be automatically localized
unless [GuiBase2d.AutoLocalize](/docs/reference/engine/classes/GuiBase2d#AutoLocalize) is enabled.

The ordering of the tables is as follows:

* First, it looks for the earliest [GuiBase2d](/docs/reference/engine/classes/GuiBase2d) ancestor of the
  object (including the provided object) that has a
  [GuiBase2d.RootLocalizationTable](/docs/reference/engine/classes/GuiBase2d#RootLocalizationTable). Tables then append in the same
  order as described in [GuiBase2d.RootLocalizationTable](/docs/reference/engine/classes/GuiBase2d#RootLocalizationTable) by going
  up through the [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) ancestors of that
  [GuiBase2d.RootLocalizationTable](/docs/reference/engine/classes/GuiBase2d#RootLocalizationTable). If no such
  [GuiBase2d.RootLocalizationTable](/docs/reference/engine/classes/GuiBase2d#RootLocalizationTable) is found, no tables append in
  this step. If instance is nil, no tables append in this step.
* Next, tables from the [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) hierarchy under
  [LocalizationService](/docs/reference/engine/classes/LocalizationService) append. For each child
  [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) of [LocalizationService](/docs/reference/engine/classes/LocalizationService), it appends
  tables going up from the lowest descendant [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) of
  the tables parented to the service, all the way up to the children of
  the service. If there are no children of [LocalizationService](/docs/reference/engine/classes/LocalizationService)
  that are [LocalizationTables](/docs/reference/engine/classes/LocalizationTable), then no tables
  append in this step.
* Finally, the cloud [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) appends to the array. If
  there is no cloud [LocalizationTable](/docs/reference/engine/classes/LocalizationTable), or the cloud
  [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) has not yet loaded, then no table appends in
  this step.

This function does not yield. It will not wait until the cloud
[LocalizationTable](/docs/reference/engine/classes/LocalizationTable) has loaded.

Provide feedback

---

GetTranslatorForLocaleAsync

Yields

Yields until the cloud [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) for the argument locale
has been loaded - if available. Returns a [Translator](/docs/reference/engine/classes/Translator) instance to
be used for translations for the provided locale.

LocalizationService:GetTranslatorForLocaleAsync(locale:[string](/docs/luau/strings)):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| locale:[string](/docs/luau/strings)  A Roblox supported language or locale code. |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

The [Translator](/docs/reference/engine/classes/Translator) instance for the specified locale.

This function takes a locale code as an argument and yields until the
cloud [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) for that locale has been loaded, if
available. It then returns a [Translator](/docs/reference/engine/classes/Translator) object which can be used
to perform translations for that locale if any are available. The entries
used for localization are the entries provided by the
[LocalizationTable](/docs/reference/engine/classes/LocalizationTable) hierarchy under [LocalizationService](/docs/reference/engine/classes/LocalizationService) as
well as the cloud table (if available). This will be the same set of
entries returned by [LocalizationService:GetTableEntries(nil)](/docs/reference/engine/classes/LocalizationService#GetTableEntries).

This function can error and thus should be wrapped in a pcall().

See also:

* [LocalizationService:GetTranslatorForPlayer()](/docs/reference/engine/classes/LocalizationService#GetTranslatorForPlayer) gets the translator
  corresponding to the locale of the provided player. This function is
  deprecated and should not be used in new work.
* [LocalizationService:GetTranslatorForPlayerAsync()](/docs/reference/engine/classes/LocalizationService#GetTranslatorForPlayerAsync) yields until
  the cloud [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) for the locale of the provided
  player has loaded and then gets the translator corresponding to the
  locale of the provided player.

Code Samples

Getting and Using a Translator for a Locale

This code sample attempts to retrieve a Translator object for the locale
"fr" (French).

[LocalizationService:GetTranslatorForLocaleAsync()](/docs/reference/engine/classes/LocalizationService#GetTranslatorForLocaleAsync) is wrapped in a
pcall because it may error. If it does not error and returns a Translator,
prints "Hello in French:" followed by the French translation of "Hello
World!". If the function errors, it prints "GetTranslatorForLocaleAsync
failed:" followed by the error message.

```
local LocalizationService = game:GetService("LocalizationService")



local textLabel = script.Parent



local success, translator = pcall(function()



return LocalizationService:GetTranslatorForLocaleAsync("fr")



end)



if success then



local result = translator:Translate(textLabel, "Hello World!")



print("Hello in French: " .. result)



else



print("GetTranslatorForLocaleAsync failed: " .. translator)



end
```

Provide feedback

---

GetTranslatorForPlayer

Deprecated

Show details

---

GetTranslatorForPlayerAsync

Yields

Yields until the cloud [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) for the player's locale
has been loaded - if available. Returns a [Translator](/docs/reference/engine/classes/Translator) instance to
be used for translations for the provided locale.

LocalizationService:GetTranslatorForPlayerAsync(player:[Instance](/docs/reference/engine/datatypes/Instance)):[Instance](/docs/reference/engine/datatypes/Instance)

Parameters

|  |
| --- |
| player:[Instance](/docs/reference/engine/datatypes/Instance)  The [Player](/docs/reference/engine/classes/Player) that you are getting the [Translator](/docs/reference/engine/classes/Translator) for. |

Returns

[Instance](/docs/reference/engine/datatypes/Instance)

The [Translator](/docs/reference/engine/classes/Translator) instance for the specified locale.

This function takes a player as an argument and yields until the cloud
[LocalizationTable](/docs/reference/engine/classes/LocalizationTable) for that player's locale has been loaded, if
available. It then returns a [Translator](/docs/reference/engine/classes/Translator) object which can be used
to perform translations for that locale if any are available. The entries
used for localization are the entries provided by the
[LocalizationTable](/docs/reference/engine/classes/LocalizationTable) hierarchy under [LocalizationService](/docs/reference/engine/classes/LocalizationService) as
well as the cloud table (if available). This will be the same set of
entries returned by [LocalizationService:GetTableEntries(nil)](/docs/reference/engine/classes/LocalizationService#GetTableEntries).

This function can error and thus should be wrapped in a pcall().

See also:

* [LocalizationService:GetTranslatorForPlayer()](/docs/reference/engine/classes/LocalizationService#GetTranslatorForPlayer), same functionality
  as this function except that it does not yield and does not wait until
  the cloud [LocalizationTable](/docs/reference/engine/classes/LocalizationTable) for the player's locale has been
  loaded. This function is deprecated and should not be used in new work.
* [LocalizationService:GetTranslatorForLocaleAsync()](/docs/reference/engine/classes/LocalizationService#GetTranslatorForLocaleAsync), returns a
  Translator to be used for translations using the provided locale.

Code Samples

Getting and Using a Translator for a Player

This code sample attempts to retrieve a Translator object for the local
player. [LocalizationService:GetTranslatorForPlayerAsync()](/docs/reference/engine/classes/LocalizationService#GetTranslatorForPlayerAsync) is wrapped
in a pcall because it may error. If it does not error and returns a
Translator, it translates and prints "Hello World!" in the player's language.
If the function errors, it prints "GetTranslatorForLocaleAsync failed:"
followed by the error message.

[LocalizationService:GetTranslatorForPlayer()](/docs/reference/engine/classes/LocalizationService#GetTranslatorForPlayer) can also be used if you'd
like to get the player's translator without yielding until the function
returns.

```
local LocalizationService = game:GetService("LocalizationService")



local Players = game:GetService("Players")



local textLabel = script.Parent



local success, translator = pcall(function()



return LocalizationService:GetTranslatorForPlayerAsync(Players.LocalPlayer)



end)



if success then



local result = translator:Translate(textLabel, "Hello World!")



print(result)



else



print("GetTranslatorForPlayerAsync failed: " .. translator)



end
```

Provide feedback

---