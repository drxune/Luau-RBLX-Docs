# Color3 | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/Color3
Scraped: 2026-01-11T02:43:16.844711Z

## Inherits
- BasePart.Color
- GuiObject.BackgroundColor3
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [Color3](/docs/reference/engine/datatypes/Color3)

English

Feedback

Engine Data Type

Color3

A color value comprised of red, green, and blue components.

---

Summary

Constructors

|  |
| --- |
| [new](#new)(red: [number](/docs/luau/numbers),green: [number](/docs/luau/numbers),blue: [number](/docs/luau/numbers)) |
| [fromRGB](#fromRGB)(red: [number](/docs/luau/numbers),green: [number](/docs/luau/numbers),blue: [number](/docs/luau/numbers)) |
| [fromHSV](#fromHSV)(hue: [number](/docs/luau/numbers),saturation: [number](/docs/luau/numbers),value: [number](/docs/luau/numbers)) |
| [fromHex](#fromHex)(hex: [string](/docs/luau/strings)) |

Properties

|  |
| --- |
| [R](#R):[number](/docs/luau/numbers) |
| [G](#G):[number](/docs/luau/numbers) |
| [B](#B):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [Lerp](#Lerp)(color: [Color3](/docs/reference/engine/datatypes/Color3),alpha: [number](/docs/luau/numbers)):[Color3](/docs/reference/engine/datatypes/Color3) |
| [ToHSV](#ToHSV)():[number](/docs/luau/numbers),[number](/docs/luau/numbers),[number](/docs/luau/numbers) |
| [ToHex](#ToHex)():[string](/docs/luau/strings) |

Functions

|  |
| --- |
| [toHSV](#toHSV)(color: [Color3](/docs/reference/engine/datatypes/Color3)):[number](/docs/luau/numbers),[number](/docs/luau/numbers),[number](/docs/luau/numbers)  Deprecated |

The [Color3](/docs/reference/engine/datatypes/Color3) data type describes a color using red, green, and blue
components in the range of 0 to 1. Unlike the [BrickColor](/docs/reference/engine/datatypes/BrickColor) data type
which describes named colors, [Color3](/docs/reference/engine/datatypes/Color3) is used for precise coloring
of objects on screen through properties like [BasePart.Color](/docs/reference/engine/classes/BasePart#Color) and
[GuiObject.BackgroundColor3](/docs/reference/engine/classes/GuiObject#BackgroundColor3).

---

API Reference

Constructors

new

Returns a [Color3](/docs/reference/engine/datatypes/Color3) with the given red, green, and blue values.

Color3.new(

red:[number](/docs/luau/numbers), green:[number](/docs/luau/numbers), blue:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| red:[number](/docs/luau/numbers) Default Value: 0 |
| green:[number](/docs/luau/numbers) Default Value: 0 |
| blue:[number](/docs/luau/numbers) Default Value: 0 |

Returns a [Color3](/docs/reference/engine/datatypes/Color3) with the given red, green, and blue values.
The parameters should be within the range of 0 to 1.

```
local red = Color3.new(1, 0, 0)



local green = Color3.new(0, 1, 0)



local blue = Color3.new(0, 0, 1)
```

Provide feedback

---

fromRGB

Returns a [Color3](/docs/reference/engine/datatypes/Color3) from given components within the range of 0 to
255.

Color3.fromRGB(

red:[number](/docs/luau/numbers), green:[number](/docs/luau/numbers), blue:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| red:[number](/docs/luau/numbers) Default Value: 0 |
| green:[number](/docs/luau/numbers) Default Value: 0 |
| blue:[number](/docs/luau/numbers) Default Value: 0 |

Creates a [Color3](/docs/reference/engine/datatypes/Color3) with the given red, green, and blue
components. Unlike most other [Color3](/docs/reference/engine/datatypes/Color3) functions, the parameters
for this function should be within the range of 0 to 255.

```
local red = Color3.fromRGB(255, 0, 0)



local green = Color3.fromRGB(0, 255, 0)



local blue = Color3.fromRGB(0, 0, 255)
```

Provide feedback

---

fromHSV

Returns a [Color3](/docs/reference/engine/datatypes/Color3) from the given hue, saturation, and value
components.

Color3.fromHSV(

hue:[number](/docs/luau/numbers), saturation:[number](/docs/luau/numbers), value:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| hue:[number](/docs/luau/numbers) |
| saturation:[number](/docs/luau/numbers) |
| value:[number](/docs/luau/numbers) |

Creates a [Color3](/docs/reference/engine/datatypes/Color3) with the given hue, saturation, and value. The
parameters should be within the range of 0 to 1.

```
local red = Color3.fromHSV(1, 1, 1)



local green = Color3.fromHSV(0.3333333, 1, 1)



local white = Color3.fromHSV(0, 0, 1)
```

Provide feedback

---

fromHex

Returns a [Color3](/docs/reference/engine/datatypes/Color3) from a given hex value.

Color3.fromHex(hex:[string](/docs/luau/strings))

Parameters

|  |
| --- |
| hex:[string](/docs/luau/strings) |

Returns a new [Color3](/docs/reference/engine/datatypes/Color3) from a six- or three-character hexadecimal
format, case insensitive. A preceding hashtag (#) is ignored, if
present. This function interprets the given string as a typical web hex
color in the format RRGGBB or RGB (shorthand for RRGGBB). For
example, #FFAA00 produces an orange color and is the same as #FA0.

```
local red = Color3.fromHex("FF0000")



local magenta = Color3.fromHex("ec008c")



local black = Color3.fromHex("000")



local white = Color3.fromHex("#FFF")
```

Provide feedback

---

Properties

R

The red value of the color.

Color3.R:[number](/docs/luau/numbers)

The red value of the color.

Provide feedback

---

G

The green value of the color.

Color3.G:[number](/docs/luau/numbers)

The green value of the color.

Provide feedback

---

B

The blue value of the color.

Color3.B:[number](/docs/luau/numbers)

The blue value of the color.

Provide feedback

---

Methods

Lerp

Returns a [Color3](/docs/reference/engine/datatypes/Color3) interpolated between two colors.

Color3:Lerp(

color:[Color3](/docs/reference/engine/datatypes/Color3), alpha:[number](/docs/luau/numbers)

):[Color3](/docs/reference/engine/datatypes/Color3)

Parameters

|  |
| --- |
| color:[Color3](/docs/reference/engine/datatypes/Color3) |
| alpha:[number](/docs/luau/numbers) |

Returns

[Color3](/docs/reference/engine/datatypes/Color3)

Returns a [Color3](/docs/reference/engine/datatypes/Color3) interpolated between two colors. The alpha
value should be within the range of 0 to 1.

```
local white = Color3.new(1, 1, 1)



local black = Color3.new(0, 0, 0)



local gray10 = white:Lerp(black, 0.1)



print(gray10)  --> 0.9, 0.9, 0.9



local gray50 = white:Lerp(black, 0.5)



print(gray50)  --> 0.5, 0.5, 0.5



local gray85 = white:Lerp(black, 0.85)



print(gray85)  --> 0.15, 0.15, 0.15
```

Provide feedback

---

ToHSV

Returns the hue, saturation, and value of a [Color3](/docs/reference/engine/datatypes/Color3).

Color3:ToHSV():[number](/docs/luau/numbers),[number](/docs/luau/numbers),[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers), [number](/docs/luau/numbers), [number](/docs/luau/numbers)

Returns the hue, saturation, and value of a [Color3](/docs/reference/engine/datatypes/Color3). This
function is the inverse operation of the [Color3.fromHSV()](/docs/reference/engine/datatypes/Color3#fromHSV)
constructor.

```
local red = Color3.fromRGB(255, 0, 0)



local green = Color3.fromRGB(0, 255, 0)



local redH, redS, redV = red:ToHSV()



print(redH, redS, redV)  --> 1 1 1



local greenH, greenS, greenV = green:ToHSV()



print(greenH, greenS, greenV)  --> 0.3333333 1 1
```

Provide feedback

---

ToHex

Returns the hex code of a [Color3](/docs/reference/engine/datatypes/Color3).

Color3:ToHex():[string](/docs/luau/strings)

Returns

[string](/docs/luau/strings)

Converts the color to a six-character hexadecimal string representing the
color in the format RRGGBB. It is not prefixed with an octothorpe (#).

The returned string can be provided to [Color3.fromHex()](/docs/reference/engine/datatypes/Color3#fromHex) to
produce the original color.

```
local red = Color3.fromRGB(255, 0, 0)



local magenta = Color3.fromRGB(236, 0, 140)



local redHex = red:ToHex()



print(redHex)  --> ff0000



local magentaHex = magenta:ToHex()



print(magentaHex)  --> ec008c
```

Provide feedback

---

Functions

toHSV

Deprecated

Show details

---