# PhysicalProperties | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/PhysicalProperties
Scraped: 2026-01-11T02:42:35.280731Z

## Inherits
- BasePart
- BasePart.CustomPhysicalProperties
- AudioEmitters
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [PhysicalProperties](/docs/reference/engine/datatypes/PhysicalProperties)

English

Feedback

Engine Data Type

PhysicalProperties

Describes properties that affect the physical behavior of a [BasePart](/docs/reference/engine/classes/BasePart).

---

Summary

Constructors

|  |
| --- |
| [new](#new)(material: [Enum.Material](/docs/reference/engine/enums/Material)) |
| [new](#new-density-fr)(density: [number](/docs/luau/numbers),friction: [number](/docs/luau/numbers),elasticity: [number](/docs/luau/numbers)) |
| [new](#new-density-fr)(density: [number](/docs/luau/numbers),friction: [number](/docs/luau/numbers),elasticity: [number](/docs/luau/numbers),frictionWeight: [number](/docs/luau/numbers),elasticityWeight: [number](/docs/luau/numbers)) |

Properties

|  |
| --- |
| [AcousticAbsorption](#AcousticAbsorption):[number](/docs/luau/numbers) |
| [Density](#Density):[number](/docs/luau/numbers) |
| [Friction](#Friction):[number](/docs/luau/numbers) |
| [Elasticity](#Elasticity):[number](/docs/luau/numbers) |
| [FrictionWeight](#FrictionWeight):[number](/docs/luau/numbers) |
| [ElasticityWeight](#ElasticityWeight):[number](/docs/luau/numbers) |

The [PhysicalProperties](/docs/reference/engine/datatypes/PhysicalProperties) data type describes several physical
properties of a [BasePart](/docs/reference/engine/classes/BasePart):
[Density](/docs/reference/engine/datatypes/PhysicalProperties#Density),
[Elasticity](/docs/reference/engine/datatypes/PhysicalProperties#Elasticity), and
[Friction](/docs/reference/engine/datatypes/PhysicalProperties#Friction). It is used in the
similarly-named [BasePart.CustomPhysicalProperties](/docs/reference/engine/classes/BasePart#CustomPhysicalProperties) property.

#### Weighting Behavior

[PhysicalProperties](/docs/reference/engine/datatypes/PhysicalProperties) also provides weightings properties,
[ElasticityWeight](/docs/reference/engine/datatypes/PhysicalProperties#ElasticityWeight) and
[FrictionWeight](/docs/reference/engine/datatypes/PhysicalProperties#FrictionWeight). When two parts
interact, the friction and elasticity between them are determined in the same
way by the following pairwise weighted average function:

```
local function getActualFriction(partA, partB)



return (partA.Friction * partA.FrictionWeight + partB.Friction * partB.FrictionWeight) / (partA.FrictionWeight + partB.FrictionWeight)



end
```

Although the formula above refers to the
[Friction](/docs/reference/engine/datatypes/PhysicalProperties#Friction) and
[FrictionWeight](/docs/reference/engine/datatypes/PhysicalProperties#FrictionWeight) of two parts,
A and B, the formula is used in the same manner when determining
[Elasticity](/docs/reference/engine/datatypes/PhysicalProperties#Elasticity). Generally, when the
weight of A is much greater than that of B, the actual value will be
closer to A. If the weights are similar, the actual value will be close to
the midpoint between their individual values.

---

API Reference

Constructors

new

Returns a [PhysicalProperties](/docs/reference/engine/datatypes/PhysicalProperties) with the default properties for the given material.

PhysicalProperties.new(material:[Enum.Material](/docs/reference/engine/enums/Material))

Parameters

|  |
| --- |
| material:[Enum.Material](/docs/reference/engine/enums/Material) |

Returns a [PhysicalProperties](/docs/reference/engine/datatypes/PhysicalProperties) container, with the density, friction, and elasticity specified for this material.

Provide feedback

---

new

Returns a [PhysicalProperties](/docs/reference/engine/datatypes/PhysicalProperties) with the specified density, friction, and
elasticity.

PhysicalProperties.new(

density:[number](/docs/luau/numbers), friction:[number](/docs/luau/numbers), elasticity:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| density:[number](/docs/luau/numbers) |
| friction:[number](/docs/luau/numbers) |
| elasticity:[number](/docs/luau/numbers) |

Returns a [PhysicalProperties](/docs/reference/engine/datatypes/PhysicalProperties) container, with the specified density,
friction, and elasticity.

Provide feedback

---

new

Creates a [PhysicalProperties](/docs/reference/engine/datatypes/PhysicalProperties) container with the specified density,
friction, elasticity, weight of friction, and weight of elasticity.

PhysicalProperties.new(

density:[number](/docs/luau/numbers), friction:[number](/docs/luau/numbers), elasticity:[number](/docs/luau/numbers), frictionWeight:[number](/docs/luau/numbers), elasticityWeight:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| density:[number](/docs/luau/numbers) |
| friction:[number](/docs/luau/numbers) |
| elasticity:[number](/docs/luau/numbers) |
| frictionWeight:[number](/docs/luau/numbers) |
| elasticityWeight:[number](/docs/luau/numbers) |

Creates a [PhysicalProperties](/docs/reference/engine/datatypes/PhysicalProperties) container with the specified density,
friction, elasticity, weight of friction, and weight of elasticity.

Provide feedback

---

Properties

AcousticAbsorption

A value between 0 and 1 denoting how absorbent the material is to
[AudioEmitters](/docs/reference/engine/classes/AudioEmitter).

PhysicalProperties.AcousticAbsorption:[number](/docs/luau/numbers)

A value between 0 and 1 denoting how absorbent the material is to
[AudioEmitters](/docs/reference/engine/classes/AudioEmitter). When using acoustic simulation,
surfaces with higher absorption will result in less reverb than surfaces
with lower absorption.

Note that this does not affect the degree to which audio transmits
through surfaces; for that, see
[Density](/docs/reference/engine/datatypes/PhysicalProperties#Density).

Provide feedback

---

Density

The mass per unit volume of the part.

PhysicalProperties.Density:[number](/docs/luau/numbers)

Density is defined as the amount of mass per unit volume. The more dense a
part is, the more force it takes to accelerate it. Acceptable range is
0.0001 to 100.0 and values outside this range will be clamped.

When using acoustic simulation, parts with higher density will muffle
occluded [AudioEmitters](/docs/reference/engine/classes/AudioEmitter) more.

Provide feedback

---

Friction

The deceleration of the part when rubbing against another part.

PhysicalProperties.Friction:[number](/docs/luau/numbers)

Friction is defined as the force that opposes the relative lateral motion
of two solid surfaces in contact. The greater the friction on a part, the
quicker it will decelerate when it rubs against another part with
friction. Acceptable range is 0.0 to 2.0 and values outside this range
will be clamped.

Provide feedback

---

Elasticity

The amount of energy retained when colliding with another part.

PhysicalProperties.Elasticity:[number](/docs/luau/numbers)

Elasticity refers to a part's tendency to retain energy when colliding
with another part. An [Elasticity](/docs/reference/engine/datatypes/PhysicalProperties#Elasticity)
of 1 indicates that the part bounces with the same energy it had before a
collision. Acceptable range is 0.0 to 1.0 and values outside this
range will be clamped.

Provide feedback

---

FrictionWeight

The importance of the part's
[Friction](/docs/reference/engine/datatypes/PhysicalProperties#Friction) property when calculating
the friction with the colliding part.

PhysicalProperties.FrictionWeight:[number](/docs/luau/numbers)

The friction weight of two parts rubbing together creates a ratio used to
calculate the actual friction between the two parts. The higher a part's
[FrictionWeight](/docs/reference/engine/datatypes/PhysicalProperties#FrictionWeight), the more its
[Friction](/docs/reference/engine/datatypes/PhysicalProperties#Friction) is used. Acceptable range
is 0.0 to 100.0 and values outside this range will be clamped.

Provide feedback

---

ElasticityWeight

The importance of the part's
[Elasticity](/docs/reference/engine/datatypes/PhysicalProperties#Elasticity) property when
calculating the elasticity with the colliding part.

PhysicalProperties.ElasticityWeight:[number](/docs/luau/numbers)

The elasticity weight of two parts colliding creates a ratio used to
calculate the actual elasticity between the two parts. The higher a part's
[ElasticityWeight](/docs/reference/engine/datatypes/PhysicalProperties#ElasticityWeight), the more
its [Elasticity](/docs/reference/engine/datatypes/PhysicalProperties#Elasticity) is used.
Acceptable range is 0.0 to 100.0 and values outside this range will be
clamped.

Provide feedback

---