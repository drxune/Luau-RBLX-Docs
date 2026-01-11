# TerrainDetail | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TerrainDetail
Scraped: 2026-01-11T02:33:45.838744Z

## Inherits
- Object
- Instance
- TerrainDetail
- MaterialVariant
- MaterialVariant.BaseMaterial
- ColorMap
- EmissiveTint
- Lighting.EnvironmentSpecularScale
- Lighting.EnvironmentDiffuseScale
- Lighting.Ambient
- Lighting.OutdoorAmbient
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [TerrainDetail](/docs/reference/engine/classes/TerrainDetail)

English

Feedback

Engine Class

![TerrainDetail](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/TerrainDetail-Dark.webp)TerrainDetail

Determines appearance of a certain terrain face direction.

---

Summary

Properties

|  |
| --- |
| [ColorMap](#ColorMap):ContentId |
| [ColorMapContent](#ColorMapContent):[Content](/docs/reference/engine/datatypes/Content) |
| [EmissiveMaskContent](#EmissiveMaskContent):[Content](/docs/reference/engine/datatypes/Content) |
| [EmissiveStrength](#EmissiveStrength):[number](/docs/luau/numbers) |
| [EmissiveTint](#EmissiveTint):[Color3](/docs/reference/engine/datatypes/Color3) |
| [Face](#Face):[Enum.TerrainFace](/docs/reference/engine/enums/TerrainFace) |
| [MaterialPattern](#MaterialPattern):[Enum.MaterialPattern](/docs/reference/engine/enums/MaterialPattern) |
| [MetalnessMap](#MetalnessMap):ContentId |
| [MetalnessMapContent](#MetalnessMapContent):[Content](/docs/reference/engine/datatypes/Content) |
| [NormalMap](#NormalMap):ContentId |
| [NormalMapContent](#NormalMapContent):[Content](/docs/reference/engine/datatypes/Content) |
| [RoughnessMap](#RoughnessMap):ContentId |
| [RoughnessMapContent](#RoughnessMapContent):[Content](/docs/reference/engine/datatypes/Content) |
| [StudsPerTile](#StudsPerTile):[number](/docs/luau/numbers) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

TerrainDetail has to be a child of a [MaterialVariant](/docs/reference/engine/classes/MaterialVariant) object. The
[MaterialVariant.BaseMaterial](/docs/reference/engine/classes/MaterialVariant#BaseMaterial) property of the parent MaterialVariant
object need to be one of the supported terrain Material, for example, it can
be Basalt but not Plastic.

Terrain renders with different textures for it's top(+y), bottom(-y), and
side(horizontal to y axis) faces. If a MaterialVariant has no TerrainDetail
children, all faces are rendered as MaterialVariant specified. At most 3
TerrainDetail objects can be added to MaterialVariant, one for each face.
TerrainDetail overrides the terrain appearance of a certain face.

For example, it can achieve this kind of effect: the top surface of Grass has
lots of grass. On side surfaces, there are less grass. On bottom surfaces
there are no grass.

---

API Reference

Properties

ColorMap

Plugin Security

Read Parallel

Determines the color of the surface.

TerrainDetail.ColorMap:ContentId

This property determines the color of the surface. This texture is
sometimes called the albedo texture. The alpha channel is not used.

Provide feedback

---

ColorMapContent

Plugin Security

Read Parallel

Determines the color of the surface. Only supports asset URIs as textures.

TerrainDetail.ColorMapContent:[Content](/docs/reference/engine/datatypes/Content)

This property determines the color of the surface. This texture is
sometimes called the albedo texture. The alpha channel is not used.

Provide feedback

---

EmissiveMaskContent

Plugin Security

Read Parallel

Determines the emissivity across the surface.

TerrainDetail.EmissiveMaskContent:[Content](/docs/reference/engine/datatypes/Content)

This property determines the apparent emissivity across the surface. An
emissive mask is a grayscale image where black pixels correspond to no
emissivity, and white pixels correspond to full emissivity.

The emissive contribution gets added to total lighting contribution across
the surface, and the sum gets multiplied by the albedo texture, which
would be sampled from [ColorMap](/docs/reference/engine/classes/TerrainDetail#ColorMap) if provided.

Provide feedback

---

EmissiveStrength

Read Parallel

Determines the strength of emissive contribution.

TerrainDetail.EmissiveStrength:[number](/docs/luau/numbers)

This value is a multiplier to control how strong the emissive contribution
is across the surface. If the final contribution of emissives goes beyond
supported dynamic range, it will get clamped; this could result in
emissive contribution appearing all white when using large emissive
strength values. Since this value is a multiplier, the maximum value to
prevent clamping depends on all of the other contributing values,
including [EmissiveTint](/docs/reference/engine/classes/TerrainDetail#EmissiveTint),
[ColorMap](/docs/reference/engine/classes/TerrainDetail#ColorMap) and combined lighting
contribution.

Provide feedback

---

EmissiveTint

Read Parallel

Determines the tinting color for emissive contribution.

TerrainDetail.EmissiveTint:[Color3](/docs/reference/engine/datatypes/Color3)

This value is an RGB color for tinting emissive contribution.

Provide feedback

---

Face

Read Parallel

The face this TerrainDetail overrides.

TerrainDetail.Face:[Enum.TerrainFace](/docs/reference/engine/enums/TerrainFace)

Face that this TerrainDetail overrides. When more than one TerrainDetail
objects with the same face exist under a MaterialVariant, only one of them
works.

Provide feedback

---

MaterialPattern

Read Parallel

Determines texture tiling method.

TerrainDetail.MaterialPattern:[Enum.MaterialPattern](/docs/reference/engine/enums/MaterialPattern)

Determines texture tiling method.

Provide feedback

---

MetalnessMap

Plugin Security

Read Parallel

Determines which parts of the surface are metal and are non-metal.

TerrainDetail.MetalnessMap:ContentId

This property determines which parts of the surface are metal and are
non-metal. A metalness map is a grayscale image where black pixels
correspond to non-metals and white pixels correspond to metals.

Metals only reflect light the same color as the metal, and they reflect
much more light than non-metals. Most materials in the real world can be
categorized either metals or non-metals. For this reason, most pixels in a
metalness map will be either pure black or pure white. Values in between
are typically used to simulate dirt or grunge on top of an underlying
metal area.

When [Lighting.EnvironmentSpecularScale](/docs/reference/engine/classes/Lighting#EnvironmentSpecularScale) is 0, metalness has no
effect. For the most realistic reflections, setting
EnvironmentSpecularScale and [Lighting.EnvironmentDiffuseScale](/docs/reference/engine/classes/Lighting#EnvironmentDiffuseScale) to
1, and [Lighting.Ambient](/docs/reference/engine/classes/Lighting#Ambient) and [Lighting.OutdoorAmbient](/docs/reference/engine/classes/Lighting#OutdoorAmbient) to
(0,0,0) is recommended.

Provide feedback

---

MetalnessMapContent

Plugin Security

Read Parallel

Determines which parts of the surface are metal and are non-metal. Only
supports asset URIs as textures.

TerrainDetail.MetalnessMapContent:[Content](/docs/reference/engine/datatypes/Content)

This property determines which parts of the surface are metal and are
non-metal. A metalness map is a grayscale image where black pixels
correspond to non-metals and white pixels correspond to metals.

Metals only reflect light the same color as the metal, and they reflect
much more light than non-metals. Most materials in the real world can be
categorized either metals or non-metals. For this reason, most pixels in a
metalness map will be either pure black or pure white. Values in between
are typically used to simulate dirt or grunge on top of an underlying
metal area.

When [Lighting.EnvironmentSpecularScale](/docs/reference/engine/classes/Lighting#EnvironmentSpecularScale) is 0, metalness has no
effect. For the most realistic reflections, setting
EnvironmentSpecularScale and [Lighting.EnvironmentDiffuseScale](/docs/reference/engine/classes/Lighting#EnvironmentDiffuseScale) to
1, and [Lighting.Ambient](/docs/reference/engine/classes/Lighting#Ambient) and [Lighting.OutdoorAmbient](/docs/reference/engine/classes/Lighting#OutdoorAmbient) to
(0,0,0) is recommended.

Provide feedback

---

NormalMap

Plugin Security

Read Parallel

Modifies the lighting of the surface by adding bumps, dents, cracks, and
curves without adding more polygons.

TerrainDetail.NormalMap:ContentId

This property modifies the lighting of the surface by adding bumps, dents,
cracks, and curves without adding more polygons.

Normal maps are RGB images that modify the surface's normal vector used
for lighting calculations. The R, G, and B channels of the NormalMap
correspond to the X, Y, and Z components of the local surface vector
respectively, and byte values of 0 and 255 for each channel correspond
linearly to normal vector components of -1 and 1.016 respectively. This
range is stretched slightly from -1 to 1 so that a byte value of 127 maps
to exactly 0. The normal vector's Z axis is always defined as the
direction of the underlying mesh's normal. A uniform (127,127,255) image
translates to a completely flat normal map where the normal is everywhere
perpendicular to the mesh surface. This format is called "tangent space"
normal maps. Roblox does not support world space or object space normal
maps.

Incorrectly flipped normal components can make bumps appear like indents.
If you import a normal map and notice the lighting looks off, you may need
to invert the G channel of the image. The X and Y axes of the tangent
space frame correspond to the X and Y directions in the image after it's
transformed by the mesh UVs. If you view your normal map in an image
editor as if it were displayed on a surface, normals pointing towards the
right side of the screen should appear more red, and normals pointing
towards the top side of your screen should appear more green.

The terms "DirectX format" and "OpenGL format" are sometimes used to
describe whether the G channel of the normal map is inverted or not.
Roblox expects the OpenGL format.

Roblox expects imported meshes to include tangents. Modeling software may
also refer to this as "tangent space" information. If you apply a normal
map and it does not seem to make any visual difference, you may need to
re-export your mesh along with its tangent information from modeling
software.

Provide feedback

---

NormalMapContent

Plugin Security

Read Parallel

Modifies the lighting of the surface by adding bumps, dents, cracks, and
curves without adding more polygons. Only supports asset URIs as textures.

TerrainDetail.NormalMapContent:[Content](/docs/reference/engine/datatypes/Content)

This property modifies the lighting of the surface by adding bumps, dents,
cracks, and curves without adding more polygons.

Normal maps are RGB images that modify the surface's normal vector used
for lighting calculations. The R, G, and B channels of the NormalMap
correspond to the X, Y, and Z components of the local surface vector
respectively, and byte values of 0 and 255 for each channel correspond
linearly to normal vector components of -1 and 1.016 respectively. This
range is stretched slightly from -1 to 1 so that a byte value of 127 maps
to exactly 0. The normal vector's Z axis is always defined as the
direction of the underlying mesh's normal. A uniform (127,127,255) image
translates to a completely flat normal map where the normal is everywhere
perpendicular to the mesh surface. This format is called "tangent space"
normal maps. Roblox does not support world space or object space normal
maps.

Incorrectly flipped normal components can make bumps appear like indents.
If you import a normal map and notice the lighting looks off, you may need
to invert the G channel of the image. The X and Y axes of the tangent
space frame correspond to the X and Y directions in the image after it's
transformed by the mesh UVs. If you view your normal map in an image
editor as if it were displayed on a surface, normals pointing towards the
right side of the screen should appear more red, and normals pointing
towards the top side of your screen should appear more green.

The terms "DirectX format" and "OpenGL format" are sometimes used to
describe whether the G channel of the normal map is inverted or not.
Roblox expects the OpenGL format.

Roblox expects imported meshes to include tangents. Modeling software may
also refer to this as "tangent space" information. If you apply a normal
map and it does not seem to make any visual difference, you may need to
re-export your mesh along with its tangent information from modeling
software.

Provide feedback

---

RoughnessMap

Plugin Security

Read Parallel

Determines the apparent roughness across the surface.

TerrainDetail.RoughnessMap:ContentId

This property determines the apparent roughness across the surface. A
roughness map is a grayscale image where black pixels correspond to a
maximally smooth surface, and white pixels correspond to a maximally rough
surface.

Roughness refers to how much variation the surface has on a very small
scale. Reflections on smooth surfaces are sharp and concentrated.
Reflections on rough surfaces are more blurry and dispersed.

Provide feedback

---

RoughnessMapContent

Plugin Security

Read Parallel

Determines the apparent roughness across the surface. Only supports asset
URIs as textures.

TerrainDetail.RoughnessMapContent:[Content](/docs/reference/engine/datatypes/Content)

This property determines the apparent roughness across the surface. A
roughness map is a grayscale image where black pixels correspond to a
maximally smooth surface, and white pixels correspond to a maximally rough
surface.

Roughness refers to how much variation the surface has on a very small
scale. Reflections on smooth surfaces are sharp and concentrated.
Reflections on rough surfaces are more blurry and dispersed.

Provide feedback

---

StudsPerTile

Read Parallel

Determines the scale of textures.

TerrainDetail.StudsPerTile:[number](/docs/luau/numbers)

Determines the scale of textures. Larger values for this property will
lead to the textures appearing larger, and repeating less frequently.

Provide feedback

---