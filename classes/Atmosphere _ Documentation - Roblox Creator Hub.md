# Atmosphere | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Atmosphere
Scraped: 2026-01-11T02:28:06.971265Z

## Inherits
- Object
- Instance
- Atmosphere
- Atmosphere.Haze
- Atmosphere.Glare
- Atmosphere.Color
- Atmosphere.Density
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Atmosphere](/docs/reference/engine/classes/Atmosphere)

English

Feedback

Engine Class

![Atmosphere](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Atmosphere-Dark.webp)Atmosphere

The [Atmosphere](/docs/reference/engine/classes/Atmosphere) object pushes Roblox closer toward realistic
environments where sunlight scatters in different ways depending on density
and other air particle properties.

---

Summary

Properties

|  |
| --- |
| [Color](#Color):[Color3](/docs/reference/engine/datatypes/Color3) |
| [Decay](#Decay):[Color3](/docs/reference/engine/datatypes/Color3) |
| [Density](#Density):[number](/docs/luau/numbers) |
| [Glare](#Glare):[number](/docs/luau/numbers) |
| [Haze](#Haze):[number](/docs/luau/numbers) |
| [Offset](#Offset):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Fog properties are hidden when Lighting contains an Atmosphere object.

The Atmosphere object pushes Roblox closer toward realistic environments
where sunlight scatters in different ways depending on density and other air
particle properties. It simulates real-world "aerial perspective" and lets you
control light transmission from the background sky through distant objects.
Furthermore, it controls haze and glare conditions, letting you tune a perfect
sunset, foggy afternoon, and more.

See also:

* [Atmospheric Effects](/docs/environment/atmosphere) for property
  comparisons and example environments.
* [Skybox](/docs/environment/skybox) for how to change the default
  skybox for games and customize the lighting.
* [Post-Processing Effects](/docs/environment/post-processing-effects)
  for how post-processing effects can quickly improve a game's visuals with a
  variety of customizable filters.

---

API Reference

Properties

Color

Read Parallel

Changes the [Atmosphere](/docs/reference/engine/classes/Atmosphere) hue for subtle environmental moods.

Atmosphere.Color:[Color3](/docs/reference/engine/datatypes/Color3)

A [Color3](/docs/reference/engine/datatypes/Color3) value which changes the [Atmosphere](/docs/reference/engine/classes/Atmosphere) hue for
subtle environmental moods. This is best combined with increased
[Atmosphere.Haze](/docs/reference/engine/classes/Atmosphere#Haze) to expand the visible effect.

Provide feedback

---

Decay

Read Parallel

When used with increased [Atmosphere.Haze](/docs/reference/engine/classes/Atmosphere#Haze) and
[Atmosphere.Glare](/docs/reference/engine/classes/Atmosphere#Glare), defines the hue of the [Atmosphere](/docs/reference/engine/classes/Atmosphere) away
from the sun, gradually falling off from [Atmosphere.Color](/docs/reference/engine/classes/Atmosphere#Color) towards
this value.

Atmosphere.Decay:[Color3](/docs/reference/engine/datatypes/Color3)

Defines the hue of the [Atmosphere](/docs/reference/engine/classes/Atmosphere) away from the sun, gradually
falling off from [Atmosphere.Color](/docs/reference/engine/classes/Atmosphere#Color) towards this value. Must be used
with [Atmosphere.Haze](/docs/reference/engine/classes/Atmosphere#Haze) and [Atmosphere.Glare](/docs/reference/engine/classes/Atmosphere#Glare) levels higher
than 0 to see any effect.

Provide feedback

---

Density

Read Parallel

Defines the amount of particles in the [Atmosphere](/docs/reference/engine/classes/Atmosphere) and essentially
controls how much in-game objects/terrain will be obscured by them.

Atmosphere.Density:[number](/docs/luau/numbers)

Defines the amount of particles in the air. The higher the density, the
more particles and the more in-game objects/terrain will be obscured by
them. Note that density does not directly affect the skybox — it
merely affects in-game objects/terrain and visibility of the skybox
through them.

Provide feedback

---

Glare

Read Parallel

When used with increased [Atmosphere.Haze](/docs/reference/engine/classes/Atmosphere#Haze), specifies the glow/glare
of the [Atmosphere](/docs/reference/engine/classes/Atmosphere) around the sun. More glare results in an
increased effect of sunlight cast onto the sky and world.

Atmosphere.Glare:[number](/docs/luau/numbers)

Specifies the glow/glare of the [Atmosphere](/docs/reference/engine/classes/Atmosphere) around the sun. More
glare results in an increased effect of sunlight cast onto the sky and
world. Must be used with a [Atmosphere.Haze](/docs/reference/engine/classes/Atmosphere#Haze) level higher than 0 to
see any effect.

Provide feedback

---

Haze

Read Parallel

Defines the haziness of the [Atmosphere](/docs/reference/engine/classes/Atmosphere) with a visible effect both
above the horizon and into the distance.

Atmosphere.Haze:[number](/docs/luau/numbers)

Defines the haziness of the [Atmosphere](/docs/reference/engine/classes/Atmosphere) with a visible effect both
above the horizon and into the distance. This can be combined with
[Atmosphere.Color](/docs/reference/engine/classes/Atmosphere#Color) to create environmental moods, like a grey tint
for a polluted alien planet.

Provide feedback

---

Offset

Read Parallel

Controls how light transmits between the camera and the sky background.

Atmosphere.Offset:[number](/docs/luau/numbers)

Controls how light transmits between the camera and the sky background.
Increase this value to create a horizon silhouette against the sky or
reduce it to blend distant objects into the sky for an endless and
seamless open world.

Offset should be balanced against [Atmosphere.Density](/docs/reference/engine/classes/Atmosphere#Density) and carefully
tested in your place. A low offset may cause "ghosting" where the skybox
can be seen through objects/terrain. This can be corrected by increasing
the offset, which more clearly silhouettes distant objects/terrain against
the sky, but too much offset may reveal level-of-detail "popping" for far
distant terrain and meshes.

Provide feedback

---