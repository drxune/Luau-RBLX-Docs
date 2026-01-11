# Clouds | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/Clouds
Scraped: 2026-01-11T02:28:49.153337Z

## Inherits
- Object
- Instance
- Clouds
- Lighting
- Atmosphere
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [Clouds](/docs/reference/engine/classes/Clouds)

English

Feedback

Engine Class

![Clouds](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/Clouds-Dark.webp)Clouds

Renders realistic clouds that drift slowly across the sky.

---

Summary

Properties

|  |
| --- |
| [Color](#Color):[Color3](/docs/reference/engine/datatypes/Color3) |
| [Cover](#Cover):[number](/docs/luau/numbers) |
| [Density](#Density):[number](/docs/luau/numbers) |
| [Enabled](#Enabled):[boolean](/docs/luau/booleans) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

The Clouds object renders realistic clouds that drift slowly across the
sky. Both cloud cover and density can be adjusted, as well as cloud color to
achieve atmospheres like stormy skies, moody sunsets, alien worlds, etc.

See the [Dynamic Clouds](/docs/environment/clouds) article
for a summary of properties and expected results.

---

API Reference

Properties

Color

Read Parallel

Controls the material color of cloud particles.

Clouds.Color:[Color3](/docs/reference/engine/datatypes/Color3)

This property controls the material color of cloud particles. However,
cloud color is influenced by several [Lighting](/docs/reference/engine/classes/Lighting) and
[Atmosphere](/docs/reference/engine/classes/Atmosphere) properties, so it is not intended as a dedicated
property to simulate colored sunsets, sunrises, etc.

See the [Dynamic Clouds](/docs/environment/clouds)
article for a summary of properties and expected results.

Provide feedback

---

Cover

Read Parallel

Defines the cloud cover within the overall skyscape layer.

Clouds.Cover:[number](/docs/luau/numbers)

This property defines the cloud cover within the overall skyscape layer.
Valid range is from 0 to 1 (sparse cloud cover to full cloud cover).

See the [Dynamic Clouds](/docs/environment/clouds)
article for a summary of properties and expected results.

Provide feedback

---

Density

Read Parallel

Controls the particulate density of clouds.

Clouds.Density:[number](/docs/luau/numbers)

This property controls the particulate density of clouds (the proportion
of airborne water vapor particles at full cloud cover).

See the [Dynamic Clouds](/docs/environment/clouds)
article for a summary of properties and expected results.

Provide feedback

---

Enabled

Read Parallel

Toggles rendering of the [Clouds](/docs/reference/engine/classes/Clouds) object.

Clouds.Enabled:[boolean](/docs/luau/booleans)

This property toggles rendering of the [Clouds](/docs/reference/engine/classes/Clouds) object. Useful for
toggling on/off different [Clouds](/docs/reference/engine/classes/Clouds) objects that exist in the same
place.

Provide feedback

---