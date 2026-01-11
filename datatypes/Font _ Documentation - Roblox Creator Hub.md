# Font | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/Font
Scraped: 2026-01-11T02:42:56.469211Z

## Inherits
- TextLabel.FontFace
- TextButton.FontFace
- TextBox.FontFace
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [Font](/docs/reference/engine/datatypes/Font)

English

Feedback

Engine Data Type

Font

Describes the font used to render text.

---

Summary

Constructors

|  |
| --- |
| [new](#new)(family: [Content](/docs/reference/engine/datatypes/Content),weight: [Enum.FontWeight](/docs/reference/engine/enums/FontWeight),style: [Enum.FontStyle](/docs/reference/engine/enums/FontStyle)) |
| [fromEnum](#fromEnum)(font: [Enum.Font](/docs/reference/engine/enums/Font)) |
| [fromName](#fromName)(name: [string](/docs/luau/strings),weight: [Enum.FontWeight](/docs/reference/engine/enums/FontWeight),style: [Enum.FontStyle](/docs/reference/engine/enums/FontStyle)) |
| [fromId](#fromId)(id: [number](/docs/luau/numbers),weight: [Enum.FontWeight](/docs/reference/engine/enums/FontWeight),style: [Enum.FontStyle](/docs/reference/engine/enums/FontStyle)) |

Properties

|  |
| --- |
| [Family](#Family):[Content](/docs/reference/engine/datatypes/Content) |
| [Weight](#Weight):[Enum.FontWeight](/docs/reference/engine/enums/FontWeight) |
| [Style](#Style):[Enum.FontStyle](/docs/reference/engine/enums/FontStyle) |
| [Bold](#Bold):[boolean](/docs/luau/booleans) |

Describes the font used to render text. Every font consists of a font
family, a weight like [Enum.FontWeight.Bold](/docs/reference/engine/enums/FontWeight#Bold), and a style like
[Enum.FontStyle.Italic](/docs/reference/engine/enums/FontStyle#Italic).

Font families are a type of asset, like images or meshes. Each font family
contains a number of font faces, and each face has a different weight and
style.

[Font](/docs/reference/engine/datatypes/Font) is used by the [TextLabel.FontFace](/docs/reference/engine/classes/TextLabel#FontFace),
[TextButton.FontFace](/docs/reference/engine/classes/TextButton#FontFace), [TextBox.FontFace](/docs/reference/engine/classes/TextBox#FontFace), and similar properties.
See also [Enum.Font](/docs/reference/engine/enums/Font) as an older alternative to this datatype that is required
by some methods and properties.

| Name | Asset ID / Weights / Appearance |
| --- | --- |
| Accanthis ADF Std | rbxasset://fonts/families/AccanthisADFStd.json |
| Amatic SC | rbxasset://fonts/families/AmaticSC.json |
| Arimo | rbxasset://fonts/families/Arimo.json |
| Balthazar | rbxasset://fonts/families/Balthazar.json |
| Bangers | rbxasset://fonts/families/Bangers.json |
| Builder Sans | rbxasset://fonts/families/BuilderSans.json |
| Comic Neue Angular | rbxasset://fonts/families/ComicNeueAngular.json |
| Creepster | rbxasset://fonts/families/Creepster.json |
| Denk One | rbxasset://fonts/families/DenkOne.json |
| Fondamento | rbxasset://fonts/families/Fondamento.json |
| Fredoka One | rbxasset://fonts/families/FredokaOne.json |
| Grenze Gotisch | rbxasset://fonts/families/GrenzeGotisch.json |
| Guru | rbxasset://fonts/families/Guru.json |
| Highway Gothic | rbxasset://fonts/families/HighwayGothic.json |
| Inconsolata | rbxasset://fonts/families/Inconsolata.json |
| Indie Flower | rbxasset://fonts/families/IndieFlower.json |
| Josefin Sans | rbxasset://fonts/families/JosefinSans.json |
| Jura | rbxasset://fonts/families/Jura.json |
| Kalam | rbxasset://fonts/families/Kalam.json |
| Luckiest Guy | rbxasset://fonts/families/LuckiestGuy.json |
| Merriweather | rbxasset://fonts/families/Merriweather.json |
| Michroma | rbxasset://fonts/families/Michroma.json |
| Montserrat | rbxasset://fonts/families/Montserrat.json |
| Nunito | rbxasset://fonts/families/Nunito.json |
| Oswald | rbxasset://fonts/families/Oswald.json |
| Patrick Hand | rbxasset://fonts/families/PatrickHand.json |
| Permanent Marker | rbxasset://fonts/families/PermanentMarker.json |
| Press Start 2P | rbxasset://fonts/families/PressStart2P.json |
| Roboto | rbxasset://fonts/families/Roboto.json |
| Roboto Condensed | rbxasset://fonts/families/RobotoCondensed.json |
| Roboto Mono | rbxasset://fonts/families/RobotoMono.json |
| Roman Antique | rbxasset://fonts/families/RomanAntique.json |
| Sarpanch | rbxasset://fonts/families/Sarpanch.json |
| Source Sans Pro | rbxasset://fonts/families/SourceSansPro.json |
| Special Elite | rbxasset://fonts/families/SpecialElite.json |
| Titillium Web | rbxasset://fonts/families/TitilliumWeb.json |
| Ubuntu | rbxasset://fonts/families/Ubuntu.json |
| Zekton | rbxasset://fonts/families/Zekton.json |

---

API Reference

Constructors

new

Creates a new [Font](/docs/reference/engine/datatypes/Font).

Font.new(

family:[Content](/docs/reference/engine/datatypes/Content), weight:[Enum.FontWeight](/docs/reference/engine/enums/FontWeight), style:[Enum.FontStyle](/docs/reference/engine/enums/FontStyle) )

Parameters

|  |
| --- |
| family:[Content](/docs/reference/engine/datatypes/Content)  The asset ID for the font family, starting with rbxasset:// or rbxassetid://. |
| weight:[Enum.FontWeight](/docs/reference/engine/enums/FontWeight) Default Value: Enum.FontWeight.Regular How thick the text is. |
| style:[Enum.FontStyle](/docs/reference/engine/enums/FontStyle) Default Value: Enum.FontStyle.Normal Whether the text is normal or italic. |

Creates a new [Font](/docs/reference/engine/datatypes/Font).

Provide feedback

---

fromEnum

Creates a [Font](/docs/reference/engine/datatypes/Font) from an [Enum.Font](/docs/reference/engine/enums/Font) value.

Font.fromEnum(font:[Enum.Font](/docs/reference/engine/enums/Font))

Parameters

|  |
| --- |
| font:[Enum.Font](/docs/reference/engine/enums/Font)  The enum value of the font to use. |

Creates a [Font](/docs/reference/engine/datatypes/Font) from an [Enum.Font](/docs/reference/engine/enums/Font) value. Throws an error when called with [Enum.Font.Unknown](/docs/reference/engine/enums/Font#Unknown).

The following table indicates how each [Enum.Font](/docs/reference/engine/enums/Font) value maps to a font [Family](/docs/reference/engine/datatypes/Font#Family).

| Font Enums | Equivalent Family |
| --- | --- |
| [AmaticSC](/docs/reference/engine/enums/Font#AmaticSC) | rbxasset://fonts/families/AmaticSC.json |
| [Antique](/docs/reference/engine/enums/Font#Antique) | rbxasset://fonts/families/RomanAntique.json |
| [Arcade](/docs/reference/engine/enums/Font#Arcade) | rbxasset://fonts/families/PressStart2P.json |
| [Arimo](/docs/reference/engine/enums/Font#Arimo), [ArimoBold](/docs/reference/engine/enums/Font#ArimoBold) | rbxasset://fonts/families/Arimo.json |
| [Bangers](/docs/reference/engine/enums/Font#Bangers) | rbxasset://fonts/families/Bangers.json |
| [Bodoni](/docs/reference/engine/enums/Font#Bodoni) | rbxasset://fonts/families/AccanthisADFStd.json |
| [BuilderSans](/docs/reference/engine/enums/Font#BuilderSans), [BuilderSansMedium](/docs/reference/engine/enums/Font#BuilderSansMedium), [BuilderSansBold](/docs/reference/engine/enums/Font#BuilderSansBold), [BuilderSansExtraBold](/docs/reference/engine/enums/Font#BuilderSansExtraBold) | rbxasset://fonts/families/BuilderSans.json |
| [Cartoon](/docs/reference/engine/enums/Font#Cartoon) | rbxasset://fonts/families/ComicNeueAngular.json |
| [Code](/docs/reference/engine/enums/Font#Code) | rbxasset://fonts/families/Inconsolata.json |
| [Creepster](/docs/reference/engine/enums/Font#Creepster) | rbxasset://fonts/families/Creepster.json |
| [DenkOne](/docs/reference/engine/enums/Font#DenkOne) | rbxasset://fonts/families/DenkOne.json |
| [Fantasy](/docs/reference/engine/enums/Font#Fantasy) | rbxasset://fonts/families/Balthazar.json |
| [Fondamento](/docs/reference/engine/enums/Font#Fondamento) | rbxasset://fonts/families/Fondamento.json |
| [FredokaOne](/docs/reference/engine/enums/Font#FredokaOne) | rbxasset://fonts/families/FredokaOne.json |
| [Garamond](/docs/reference/engine/enums/Font#Garamond) | rbxasset://fonts/families/Guru.json |
| [GrenzeGotisch](/docs/reference/engine/enums/Font#GrenzeGotisch) | rbxasset://fonts/families/GrenzeGotisch.json |
| [Highway](/docs/reference/engine/enums/Font#Highway) | rbxasset://fonts/families/HighwayGothic.json |
| [IndieFlower](/docs/reference/engine/enums/Font#IndieFlower) | rbxasset://fonts/families/IndieFlower.json |
| [JosefinSans](/docs/reference/engine/enums/Font#JosefinSans) | rbxasset://fonts/families/JosefinSans.json |
| [Jura](/docs/reference/engine/enums/Font#Jura) | rbxasset://fonts/families/Jura.json |
| [Kalam](/docs/reference/engine/enums/Font#Kalam) | rbxasset://fonts/families/Kalam.json |
| [Legacy](/docs/reference/engine/enums/Font#Legacy) | rbxasset://fonts/families/LegacyArial.json |
| [LuckiestGuy](/docs/reference/engine/enums/Font#LuckiestGuy) | rbxasset://fonts/families/LuckiestGuy.json |
| [Merriweather](/docs/reference/engine/enums/Font#Merriweather) | rbxasset://fonts/families/Merriweather.json |
| [Michroma](/docs/reference/engine/enums/Font#Michroma) | rbxasset://fonts/families/Michroma.json |
| [Nunito](/docs/reference/engine/enums/Font#Nunito) | rbxasset://fonts/families/Nunito.json |
| [Oswald](/docs/reference/engine/enums/Font#Oswald) | rbxasset://fonts/families/Oswald.json |
| [PatrickHand](/docs/reference/engine/enums/Font#PatrickHand) | rbxasset://fonts/families/PatrickHand.json |
| [PermanentMarker](/docs/reference/engine/enums/Font#PermanentMarker) | rbxasset://fonts/families/PermanentMarker.json |
| [Roboto](/docs/reference/engine/enums/Font#Roboto) | rbxasset://fonts/families/Roboto.json |
| [RobotoCondensed](/docs/reference/engine/enums/Font#RobotoCondensed) | rbxasset://fonts/families/RobotoCondensed.json |
| [RobotoMono](/docs/reference/engine/enums/Font#RobotoMono) | rbxasset://fonts/families/RobotoMono.json |
| [Sarpanch](/docs/reference/engine/enums/Font#Sarpanch) | rbxasset://fonts/families/Sarpanch.json |
| [SciFi](/docs/reference/engine/enums/Font#SciFi) | rbxasset://fonts/families/Zekton.json |
| [SourceSans](/docs/reference/engine/enums/Font#SourceSans), [SourceSansBold](/docs/reference/engine/enums/Font#SourceSansBold), [SourceSansItalic](/docs/reference/engine/enums/Font#SourceSansItalic), [SourceSansLight](/docs/reference/engine/enums/Font#SourceSansLight), [SourceSansSemibold](/docs/reference/engine/enums/Font#SourceSansSemibold) | rbxasset://fonts/families/SourceSansPro.json |
| [SpecialElite](/docs/reference/engine/enums/Font#SpecialElite) | rbxasset://fonts/families/SpecialElite.json |
| [TitilliumWeb](/docs/reference/engine/enums/Font#TitilliumWeb) | rbxasset://fonts/families/TitilliumWeb.json |
| [Ubuntu](/docs/reference/engine/enums/Font#Ubuntu) | rbxasset://fonts/families/Ubuntu.json |

Provide feedback

---

fromName

Creates a [Font](/docs/reference/engine/datatypes/Font) from a name like FredokaOne.

Font.fromName(

name:[string](/docs/luau/strings), weight:[Enum.FontWeight](/docs/reference/engine/enums/FontWeight), style:[Enum.FontStyle](/docs/reference/engine/enums/FontStyle) )

Parameters

|  |
| --- |
| name:[string](/docs/luau/strings)  The name of the font. |
| weight:[Enum.FontWeight](/docs/reference/engine/enums/FontWeight) Default Value: Enum.FontWeight.Regular How thick the text is. |
| style:[Enum.FontStyle](/docs/reference/engine/enums/FontStyle) Default Value: Enum.FontStyle.Normal Whether the text is normal or italic. |

This is a convenience method for creating fonts from the content folder. The name you pass in will be converted into an asset ID like rbxasset://fonts/families/BuilderSans.json.

The name can only contain alphabetical characters, digits, \_ (underscore), and - (hyphen). It can't contain any spaces.

Provide feedback

---

fromId

Creates a [Font](/docs/reference/engine/datatypes/Font) from a numerical asset ID.

Font.fromId(

id:[number](/docs/luau/numbers), weight:[Enum.FontWeight](/docs/reference/engine/enums/FontWeight), style:[Enum.FontStyle](/docs/reference/engine/enums/FontStyle) )

Parameters

|  |
| --- |
| id:[number](/docs/luau/numbers)  The asset ID of the font as a number. |
| weight:[Enum.FontWeight](/docs/reference/engine/enums/FontWeight) Default Value: Enum.FontWeight.Regular How thick the text is. |
| style:[Enum.FontStyle](/docs/reference/engine/enums/FontStyle) Default Value: Enum.FontStyle.Normal Whether the text is normal or italic. |

This is a convenience method for creating fonts from an asset ID number.

Provide feedback

---

Properties

Family

The asset ID for the font family.

Font.Family:[Content](/docs/reference/engine/datatypes/Content)

The asset ID for the font family. These start with either rbxasset:// or
rbxassetid://.

Provide feedback

---

Weight

How thick the text is.

Font.Weight:[Enum.FontWeight](/docs/reference/engine/enums/FontWeight)

How thick the text is. The default value is [Enum.FontWeight.Regular](/docs/reference/engine/enums/FontWeight#Regular).

When set, [Font.Bold](/docs/reference/engine/datatypes/Font#Bold) is updated and becomes true if the weight
is [Enum.FontWeight.SemiBold](/docs/reference/engine/enums/FontWeight#SemiBold) or thicker.

Provide feedback

---

Style

Whether the font is italic.

Font.Style:[Enum.FontStyle](/docs/reference/engine/enums/FontStyle)

Whether the font is italic. The default value is [Enum.FontStyle.Normal](/docs/reference/engine/enums/FontStyle#Normal).

Provide feedback

---

Bold

Whether the font is bold.

Font.Bold:[boolean](/docs/luau/booleans)

Whether the font is bold. Sets [Font.Weight](/docs/reference/engine/datatypes/Font#Weight) to
[Enum.FontWeight.Bold](/docs/reference/engine/enums/FontWeight#Bold) when true, or to [Enum.FontWeight.Regular](/docs/reference/engine/enums/FontWeight#Regular)
otherwise.

Provide feedback

---