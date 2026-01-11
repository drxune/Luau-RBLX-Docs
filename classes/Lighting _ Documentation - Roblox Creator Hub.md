# Lighting | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Lighting
Scraped: 2026-01-11T02:39:46.288826Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Object
- Instance
- Lighting
- Atmosphere
- Workspace.CurrentCamera
- SunRaysEffect
- BlurEffect
- OutdoorAmbient
- GlobalShadows
- Ambient
- TimeOfDay
- SetMinutesAfterMidnight()
- BasePart
- Brightness
- ColorShift_Top
- ColorShift_Bottom
- GetSunDirection()
- GetMoonDirection()
- BaseParts
- Technology
- ClockTime
- Script
- Sky
- FogColor
- FogStart
- FogEnd
- Object.Changed
- Object:GetPropertyChangedSignal()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Lighting](/docs/reference/engine/classes/Lighting)

English

Feedback

Engine Class

![Lighting](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Lighting-Dark.webp)Lighting

The Lighting service controls global lighting in an experience. It includes
a range of adjustable properties that you can use to change how lighting
appears and interacts with other objects.

Not Creatable

Service

---

Summary

Properties

|  |
| --- |
| [Ambient](#Ambient):[Color3](/docs/reference/engine/datatypes/Color3) |
| [Brightness](#Brightness):[number](/docs/luau/numbers) |
| [ClockTime](#ClockTime):[number](/docs/luau/numbers) |
| [ColorShift\_Bottom](#ColorShift_Bottom):[Color3](/docs/reference/engine/datatypes/Color3) |
| [ColorShift\_Top](#ColorShift_Top):[Color3](/docs/reference/engine/datatypes/Color3) |
| [EnvironmentDiffuseScale](#EnvironmentDiffuseScale):[number](/docs/luau/numbers) |
| [EnvironmentSpecularScale](#EnvironmentSpecularScale):[number](/docs/luau/numbers) |
| [ExposureCompensation](#ExposureCompensation):[number](/docs/luau/numbers) |
| [ExtendLightRangeTo120](#ExtendLightRangeTo120):[Enum.RolloutState](/docs/reference/engine/enums/RolloutState) |
| [FogColor](#FogColor):[Color3](/docs/reference/engine/datatypes/Color3) |
| [FogEnd](#FogEnd):[number](/docs/luau/numbers) |
| [FogStart](#FogStart):[number](/docs/luau/numbers) |
| [GeographicLatitude](#GeographicLatitude):[number](/docs/luau/numbers) |
| [GlobalShadows](#GlobalShadows):[boolean](/docs/luau/booleans) |
| [LightingStyle](#LightingStyle):[Enum.LightingStyle](/docs/reference/engine/enums/LightingStyle) |
| [OutdoorAmbient](#OutdoorAmbient):[Color3](/docs/reference/engine/datatypes/Color3) |
| [Outlines](#Outlines):[boolean](/docs/luau/booleans)  Deprecated |
| [PrioritizeLightingQuality](#PrioritizeLightingQuality):[boolean](/docs/luau/booleans) |
| [ShadowColor](#ShadowColor):[Color3](/docs/reference/engine/datatypes/Color3)  Deprecated |
| [ShadowSoftness](#ShadowSoftness):[number](/docs/luau/numbers) |
| [Technology](#Technology):[Enum.Technology](/docs/reference/engine/enums/Technology)  Deprecated |
| [TimeOfDay](#TimeOfDay):[string](/docs/luau/strings) |

Methods

|  |
| --- |
| [GetMinutesAfterMidnight](#GetMinutesAfterMidnight)():[number](/docs/luau/numbers) |
| [getMinutesAfterMidnight](#getMinutesAfterMidnight)():[number](/docs/luau/numbers)  Deprecated |
| [GetMoonDirection](#GetMoonDirection)():[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [GetMoonPhase](#GetMoonPhase)():[number](/docs/luau/numbers)  Deprecated |
| [GetSunDirection](#GetSunDirection)():[Vector3](/docs/reference/engine/datatypes/Vector3) |
| [SetMinutesAfterMidnight](#SetMinutesAfterMidnight)(minutes: [number](/docs/luau/numbers)):() |
| [setMinutesAfterMidnight](#setMinutesAfterMidnight)(minutes: [number](/docs/luau/numbers)):()  Deprecated |

Events

|  |
| --- |
| [LightingChanged](#LightingChanged)(skyChanged: [boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The Lighting service controls global lighting in an experience. It includes
a range of adjustable properties that you can use to change how lighting
appears and interacts with other objects, as summarized in
[Lighting Properties](/docs/environment/lighting).

![](https://prod.docsiteassets.roblox.com/assets/lighting-and-effects/lighting-properties/TimeOfDay-17.jpg)

Lighting may also contain an [Atmosphere](/docs/reference/engine/classes/Atmosphere) object to render realistic
atmospheric effects, including particle density, haze, glare, and color. See
[Atmospheric Effects](/docs/environment/atmosphere) for details.

![](https://prod.docsiteassets.roblox.com/assets/lighting-and-effects/atmosphere/Offset-A.jpg)

In addition, Lighting (along with [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera)) may
contain
[post‑processing effects](/docs/environment/post-processing-effects)
such as [SunRaysEffect](/docs/reference/engine/classes/SunRaysEffect) and [BlurEffect](/docs/reference/engine/classes/BlurEffect).

---

API Reference

Properties

Ambient

Read Parallel

The lighting hue applied to areas that are occluded from the sky, such as
indoor areas.

Lighting.Ambient:[Color3](/docs/reference/engine/datatypes/Color3)

Ambient is the lighting hue applied to areas that are occluded from the
sky, such as indoor areas.

Ambient defaults to [0, 0, 0] (black). As long as the red, green, and
blue channels of this property do not exceed the corresponding channels in
[OutdoorAmbient](/docs/reference/engine/classes/Lighting#OutdoorAmbient), the change in hue will be
reserved for areas occluded from the sun/moon.

Note that when [GlobalShadows](/docs/reference/engine/classes/Lighting#GlobalShadows) is disabled,
there is no distinction between areas occluded from the sky and
non‑occluded areas. In this case,
[OutdoorAmbient](/docs/reference/engine/classes/Lighting#OutdoorAmbient) will be ignored and the hue
from the Ambient property will be applied everywhere.

Provide feedback

---

Brightness

Read Parallel

The intensity of illumination in the place.

Lighting.Brightness:[number](/docs/luau/numbers)

The intensity of illumination in the place.

Changing this value will influence the impact of the light source (sun or
moon) on the place's lighting. Note that [Ambient](/docs/reference/engine/classes/Lighting#Ambient)
and [OutdoorAmbient](/docs/reference/engine/classes/Lighting#OutdoorAmbient) can also be used to
influence how bright a place appears. For example, setting
[OutdoorAmbient](/docs/reference/engine/classes/Lighting#OutdoorAmbient) to [255, 255, 255] will make the place appear brighter
than its default value of 127, 127, 127
(as it is more white).

Provide feedback

---

ClockTime

Not Replicated

Read Parallel

A numerical representation (in hours) of the current time of day used by
Lighting.

Lighting.ClockTime:[number](/docs/luau/numbers)

A numerical representation (in hours) of the current time of day used by
Lighting. Note that this property does not correspond with the actual
time of day and will not change during gameplay unless it has been changed
by a script.

For a measure of Lighting time formatted as a 24-hour string, use
[TimeOfDay](/docs/reference/engine/classes/Lighting#TimeOfDay). Changing
[TimeOfDay](/docs/reference/engine/classes/Lighting#TimeOfDay) or using
[SetMinutesAfterMidnight()](/docs/reference/engine/classes/Lighting#SetMinutesAfterMidnight) will
also change this property.

Provide feedback

---

ColorShift\_Bottom

Read Parallel

The hue represented in light reflected in the opposite surfaces to those
facing the sun or moon.

Lighting.ColorShift\_Bottom:[Color3](/docs/reference/engine/datatypes/Color3)

The hue represented in light reflected in the opposite surfaces to those
facing the sun or moon.

The surfaces of a [BasePart](/docs/reference/engine/classes/BasePart) influenced by ColorShift\_Bottom
depends on the position and orientation of the [BasePart](/docs/reference/engine/classes/BasePart) relative
to the sun or moon's position. Where the sun is directly overhead a
[BasePart](/docs/reference/engine/classes/BasePart), the shift in color will only apply to the bottom
surface.

This effect can be increased or reduced by altering
[Brightness](/docs/reference/engine/classes/Lighting#Brightness).

Note that [ColorShift\_Top](/docs/reference/engine/classes/Lighting#ColorShift_Top) and
ColorShift\_Bottom will interact with the
[Ambient](/docs/reference/engine/classes/Lighting#Ambient) and
[OutdoorAmbient](/docs/reference/engine/classes/Lighting#OutdoorAmbient) properties if they are
greater than [0, 0, 0]. Also note that
the influence of ColorShift\_Bottom can be very hard to identify when
[GlobalShadows](/docs/reference/engine/classes/Lighting#GlobalShadows) is enabled (default).

Provide feedback

---

ColorShift\_Top

Read Parallel

The hue represented in light reflected from surfaces facing the sun or
moon.

Lighting.ColorShift\_Top:[Color3](/docs/reference/engine/datatypes/Color3)

The hue represented in light reflected from surfaces facing the sun or
moon.

The surfaces of a [BasePart](/docs/reference/engine/classes/BasePart) influenced by ColorShift\_Top depends
on the position and orientation of the [BasePart](/docs/reference/engine/classes/BasePart) relative to the
sun or moon's position. Where the sun is directly overhead a
[BasePart](/docs/reference/engine/classes/BasePart), the shift in color will only apply to the top surface.

This effect can be increased or reduced by altering
[Brightness](/docs/reference/engine/classes/Lighting#Brightness).

Note that ColorShift\_Top and
[ColorShift\_Bottom](/docs/reference/engine/classes/Lighting#ColorShift_Bottom) will interact with
the [Ambient](/docs/reference/engine/classes/Lighting#Ambient) and
[OutdoorAmbient](/docs/reference/engine/classes/Lighting#OutdoorAmbient) properties if they are
greater than [0, 0, 0].

Provide feedback

---

EnvironmentDiffuseScale

Read Parallel

Ambient light that is derived from the environment.

Lighting.EnvironmentDiffuseScale:[number](/docs/luau/numbers)

Ambient light that is derived from the environment with a default of 0.
This property is similar to [Ambient](/docs/reference/engine/classes/Lighting#Ambient) and
[OutdoorAmbient](/docs/reference/engine/classes/Lighting#OutdoorAmbient) but it's dynamic and can
change according to the sky and time of day. When this property is
increased, it's recommended to decrease [Ambient](/docs/reference/engine/classes/Lighting#Ambient)
and [OutdoorAmbient](/docs/reference/engine/classes/Lighting#OutdoorAmbient) accordingly.

Provide feedback

---

EnvironmentSpecularScale

Read Parallel

Specular light derived from environment.

Lighting.EnvironmentSpecularScale:[number](/docs/luau/numbers)

Specular light derived from environment with a default of 0. This
property will make smooth objects reflect the environment and it is
especially important to make metal look more realistic.

Provide feedback

---

ExposureCompensation

Read Parallel

The exposure compensation value.

Lighting.ExposureCompensation:[number](/docs/luau/numbers)

This property determines the exposure compensation amount which applies a
bias to the exposure level of the scene prior to the tonemap step.
Defaults to 0 (no exposure compensation) and has a range from -5 to
5. A value of 1 indicates twice as much exposure and -1 means half
as much exposure.

Provide feedback

---

ExtendLightRangeTo120

Not Scriptable

Read Parallel

Lighting.ExtendLightRangeTo120:[Enum.RolloutState](/docs/reference/engine/enums/RolloutState)

Provide feedback

---

FogColor

Read Parallel

A [Color3](/docs/reference/engine/datatypes/Color3) value giving the hue of Lighting fog.

Lighting.FogColor:[Color3](/docs/reference/engine/datatypes/Color3)

A [Color3](/docs/reference/engine/datatypes/Color3) value giving the hue of Lighting fog. Note that fog
properties are hidden when Lighting contains an [Atmosphere](/docs/reference/engine/classes/Atmosphere)
object.

Provide feedback

---

FogEnd

Read Parallel

The depth from the [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera), in studs, at which fog
will be completely opaque.

Lighting.FogEnd:[number](/docs/luau/numbers)

The depth from the [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera), in studs, at which fog
will be completely opaque. Note that fog properties are hidden when
Lighting contains an [Atmosphere](/docs/reference/engine/classes/Atmosphere) object.

Provide feedback

---

FogStart

Read Parallel

The depth from the [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera), in studs, at which fog
begins to show.

Lighting.FogStart:[number](/docs/luau/numbers)

The depth from the [Workspace.CurrentCamera](/docs/reference/engine/classes/Workspace#CurrentCamera), in studs, at which fog
begins to show. Note that fog properties are hidden when Lighting
contains an [Atmosphere](/docs/reference/engine/classes/Atmosphere) object.

Provide feedback

---

GeographicLatitude

Read Parallel

The geographic latitude, in degrees, of the scene, influencing the result
of Lighting time on the position of the sun and moon.

Lighting.GeographicLatitude:[number](/docs/luau/numbers)

The geographic latitude, in degrees, of the scene, influencing the result
of Lighting time on the position of the sun and moon. When calculating
the position of the sun, the earth's tilt is also taken into account.

Changing GeographicLatitude will alter the position of the sun at every
[TimeOfDay](/docs/reference/engine/classes/Lighting#TimeOfDay). If you're looking to obtain the sun
or moon's position, use
[GetSunDirection()](/docs/reference/engine/classes/Lighting#GetSunDirection) or
[GetMoonDirection()](/docs/reference/engine/classes/Lighting#GetMoonDirection).

Provide feedback

---

GlobalShadows

Read Parallel

Toggles voxel-based dynamic lighting for the place.

Lighting.GlobalShadows:[boolean](/docs/luau/booleans)

Toggles voxel-based dynamic lighting in the place. When set to true,
shadows are rendered in sheltered areas depending on the position of the
sun and moon. The lighting hue applied to these sheltered areas is
determined by the [Ambient](/docs/reference/engine/classes/Lighting#Ambient) property while the
lighting hue in all other areas is determined by the
[OutdoorAmbient](/docs/reference/engine/classes/Lighting#OutdoorAmbient) property.

When false, shadows are not drawn and no distinction is made between
indoor and outdoor areas. As a result, the
[Ambient](/docs/reference/engine/classes/Lighting#Ambient) property determines the lighting hue and
[OutdoorAmbient](/docs/reference/engine/classes/Lighting#OutdoorAmbient) will do nothing.

Shadows are calculated using a voxel system and each lighting voxel is
4×4×4 studs. This means objects need to be larger than
4×4×4 studs to display a realistic shadow. Shadows are also
recalculated when [BaseParts](/docs/reference/engine/classes/BasePart) are moving.

Provide feedback

---

LightingStyle

Roblox Script Security

Read Parallel

The artistic intent behind lighting in the experience.

Lighting.LightingStyle:[Enum.LightingStyle](/docs/reference/engine/enums/LightingStyle)

LightingStyle indicates the artistic intent behind lighting in the
experience, as an [Enum.LightingStyle](/docs/reference/engine/enums/LightingStyle) option.

Provide feedback

---

OutdoorAmbient

Read Parallel

The lighting hue applied to outdoor areas.

Lighting.OutdoorAmbient:[Color3](/docs/reference/engine/datatypes/Color3)

OutdoorAmbient is the lighting hue applied to outdoor areas.

OutdoorAmbient defaults to [127, 127, 127]. As long as the red, green,
and blue channels of [Ambient](/docs/reference/engine/classes/Lighting#Ambient) do not exceed the
corresponding channels in OutdoorAmbient, the hue of the lighting in
outdoor areas will be determined by this property.

The effective OutdoorAmbient value is clamped to be greater than or
equal to [Ambient](/docs/reference/engine/classes/Lighting#Ambient) in all channels, meaning that if
a channel of [Ambient](/docs/reference/engine/classes/Lighting#Ambient) exceeds its corresponding
OutdoorAmbient channel, the hue of [Ambient](/docs/reference/engine/classes/Lighting#Ambient) will
begin to apply to outdoor areas.

Note that when [GlobalShadows](/docs/reference/engine/classes/Lighting#GlobalShadows) is disabled,
there is no distinction between areas occluded from the sky and
non‑occluded areas. In this case, OutdoorAmbient will be ignored and the
hue from the [Ambient](/docs/reference/engine/classes/Lighting#Ambient) property will be applied
everywhere.

Provide feedback

---

Outlines

Deprecated

Show details

---

PrioritizeLightingQuality

Roblox Script Security

Read Parallel

Indicates whether you prefer lighting/shading quality or view distance to
scale down first.

Lighting.PrioritizeLightingQuality:[boolean](/docs/luau/booleans)

This property indicates whether you prefer lighting/shading quality or
view distance to scale down first. As the rendering quality level reduces,
a setting of true prioritizes features such as advanced shadows and
high‑quality shaders at closer distances, while a setting of false
prioritizes view distance.

Provide feedback

---

ShadowColor

Deprecated

Show details

---

ShadowSoftness

Read Parallel

Controls how blurry the shadows are.

Lighting.ShadowSoftness:[number](/docs/luau/numbers)

Controls how blurry the shadows are with a default of 0.2. This property
only works when [Technology](/docs/reference/engine/classes/Lighting#Technology) mode is
[ShadowMap](/docs/reference/engine/enums/Technology) or [Future](/docs/reference/engine/enums/Technology) and the device is
capable of rendering shadow maps.

Provide feedback

---

Technology

Deprecated

Show details

---

TimeOfDay

Read Parallel

A 24-hour string representation of the current time of day used by
Lighting.

Lighting.TimeOfDay:[string](/docs/luau/strings)

A 24-hour string representation of the current time of day used by
Lighting. Note that this property does not correspond with the actual
time of day and will not change during gameplay unless it has been changed
by a script.

For a numeric measure of Lighting time, use
[ClockTime](/docs/reference/engine/classes/Lighting#ClockTime). Changing
[ClockTime](/docs/reference/engine/classes/Lighting#ClockTime) or using
[SetMinutesAfterMidnight()](/docs/reference/engine/classes/Lighting#SetMinutesAfterMidnight) will
also change this property.

Provide feedback

---

Methods

GetMinutesAfterMidnight

Write Parallel

Returns the number of minutes that have passed after midnight for the
purposes of lighting.

Lighting:GetMinutesAfterMidnight():[number](/docs/luau/numbers)

Returns

[number](/docs/luau/numbers)

The number of minutes after midnight.

Returns the number of minutes that have passed after midnight for the
purposes of lighting. This number will be nearly identical to
[ClockTime](/docs/reference/engine/classes/Lighting#ClockTime) multiplied by 60.

Note that this number will not always be equal to the value given in
[SetMinutesAfterMidnight()](/docs/reference/engine/classes/Lighting#SetMinutesAfterMidnight) as it
returns minutes after midnight in the current day.

Provide feedback

---

getMinutesAfterMidnight

Deprecated

Show details

---

GetMoonDirection

Write Parallel

Returns a [Vector3](/docs/reference/engine/datatypes/Vector3) representing the direction of the moon.

Lighting:GetMoonDirection():[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

[Vector3](/docs/reference/engine/datatypes/Vector3) representing the direction of the moon.

Returns a [Vector3](/docs/reference/engine/datatypes/Vector3) representing the direction of the moon from
the position (0, 0, 0). Note that when
the moon has "set" and is no longer visible, the [Vector3](/docs/reference/engine/datatypes/Vector3)
returned by this method will continue to point towards the moon below the
horizon.

[GetSunDirection()](/docs/reference/engine/classes/Lighting#GetSunDirection) is a variant of this
method for obtaining the direction of the sun.

Provide feedback

---

GetMoonPhase

Deprecated

Show details

---

GetSunDirection

Write Parallel

Returns a [Vector3](/docs/reference/engine/datatypes/Vector3) representing the direction of the sun.

Lighting:GetSunDirection():[Vector3](/docs/reference/engine/datatypes/Vector3)

Returns

[Vector3](/docs/reference/engine/datatypes/Vector3)

[Vector3](/docs/reference/engine/datatypes/Vector3) representing the direction of the sun.

Returns a [Vector3](/docs/reference/engine/datatypes/Vector3) representing the direction of the sun from
the position (0, 0, 0). Note that when
the sun has "set" and is no longer visible, the [Vector3](/docs/reference/engine/datatypes/Vector3)
returned by this method will continue to point towards the sun below the
horizon.

[GetMoonDirection()](/docs/reference/engine/classes/Lighting#GetMoonDirection) is a variant of
this method for obtaining the direction of the moon.

Provide feedback

---

SetMinutesAfterMidnight

Sets [TimeOfDay](/docs/reference/engine/classes/Lighting#TimeOfDay) and
[ClockTime](/docs/reference/engine/classes/Lighting#ClockTime) to the given number of minutes after
midnight.

Lighting:SetMinutesAfterMidnight(minutes:[number](/docs/luau/numbers)):()

Parameters

|  |
| --- |
| minutes:[number](/docs/luau/numbers)  The number of minutes after midnight. |

Returns

()

Sets [TimeOfDay](/docs/reference/engine/classes/Lighting#TimeOfDay) and
[ClockTime](/docs/reference/engine/classes/Lighting#ClockTime) to the given number of minutes after
midnight.

This method allows a numerical value to be used, for example in a
day/night cycle [Script](/docs/reference/engine/classes/Script), without the need to convert to a string in
the format required by [TimeOfDay](/docs/reference/engine/classes/Lighting#TimeOfDay). It also
allows values greater than 24 hours to be given that correspond to times
in the next day.

The following code sample includes a simple day/night cycle script. The
speed of time and the initial time can be changed using the TIME\_SPEED
and START\_TIME parameters.

```
local Lighting = game:GetService("Lighting")



local TIME_SPEED = 60  -- 1 min = 1 hour



local START_TIME = 9  -- 9 AM



local minutesAfterMidnight = START_TIME * 60



local waitTime = 60 / TIME_SPEED



while true do



minutesAfterMidnight = minutesAfterMidnight + 1



Lighting:SetMinutesAfterMidnight(minutesAfterMidnight)



task.wait(waitTime)



end
```

Provide feedback

---

setMinutesAfterMidnight

Deprecated

Show details

---

Events

LightingChanged

This event fires when a Lighting property is changed or a [Sky](/docs/reference/engine/classes/Sky) is
added or removed from Lighting.

Lighting.LightingChanged(skyChanged:[boolean](/docs/luau/booleans)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| skyChanged:[boolean](/docs/luau/booleans) |

This event fires when a Lighting property is changed or a [Sky](/docs/reference/engine/classes/Sky) is
added or removed from Lighting, with some exceptions:

* Changing [GlobalShadows](/docs/reference/engine/classes/Lighting#GlobalShadows) will not fire this
  event.
* Changing fog properties [FogColor](/docs/reference/engine/classes/Lighting#FogColor),
  [FogStart](/docs/reference/engine/classes/Lighting#FogStart), or [FogEnd](/docs/reference/engine/classes/Lighting#FogEnd)
  will not fire this event.

In cases where this behavior is not desired, the [Object.Changed](/docs/reference/engine/classes/Object#Changed)
event or [Object:GetPropertyChangedSignal()](/docs/reference/engine/classes/Object#GetPropertyChangedSignal) method can be used.

Provide feedback

---