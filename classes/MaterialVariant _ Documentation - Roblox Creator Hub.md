# MaterialVariant | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/MaterialVariant
Scraped: 2026-01-11T02:28:53.536207Z

## Inherits
- Object
- Instance
- MaterialVariant
- BasePart.MaterialVariant
- MaterialVariant.ColorMap
- MeshPart.Transparency
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
7. [MaterialVariant](/docs/reference/engine/classes/MaterialVariant)

English

Feedback

Engine Class

![MaterialVariant](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/MaterialVariant-Dark.webp)MaterialVariant

Represent a variant of a Material.

---

Summary

Properties

|  |
| --- |
| [AlphaMode](#AlphaMode):[Enum.AlphaMode](/docs/reference/engine/enums/AlphaMode) |
| [BaseMaterial](#BaseMaterial):[Enum.Material](/docs/reference/engine/enums/Material) |
| [ColorMap](#ColorMap):ContentId |
| [ColorMapContent](#ColorMapContent):[Content](/docs/reference/engine/datatypes/Content) |
| [CustomPhysicalProperties](#CustomPhysicalProperties):[PhysicalProperties](/docs/reference/engine/datatypes/PhysicalProperties) |
| [EmissiveMaskContent](#EmissiveMaskContent):[Content](/docs/reference/engine/datatypes/Content) |
| [EmissiveStrength](#EmissiveStrength):[number](/docs/luau/numbers) |
| [EmissiveTint](#EmissiveTint):[Color3](/docs/reference/engine/datatypes/Color3) |
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

Using MaterialVariant objects can expand the variety of materials in an
experience. MaterialVariant has properties that can define the appearance of a
material. Its name can be set in MaterialService to globally override a
built-in material, or set in the [BasePart.MaterialVariant](/docs/reference/engine/classes/BasePart#MaterialVariant) property to
change certain Parts. MaterialVariant objects only work as descendants of
MaterialService.

---

API Reference

Properties

AlphaMode

Not Browsable

Read Parallel

Determines how the alpha channel of the [MaterialVariant.ColorMap](/docs/reference/engine/classes/MaterialVariant#ColorMap)
is used.

MaterialVariant.AlphaMode:[Enum.AlphaMode](/docs/reference/engine/enums/AlphaMode)

This property determines how the alpha channel of the
[MaterialVariant.ColorMap](/docs/reference/engine/classes/MaterialVariant#ColorMap) is used.

When set to [Transparency](/docs/reference/engine/enums/AlphaMode) and the
[MeshPart.Transparency](/docs/reference/engine/classes/MeshPart#Transparency) is set to 0, opaque pixels in the
[ColorMap](/docs/reference/engine/classes/MaterialVariant#ColorMap) renders as completely opaque in
the 3D scene. This combination works better with depth-based effects and
occlusion.

When set to [Transparency](/docs/reference/engine/enums/AlphaMode) and the
[MeshPart.Transparency](/docs/reference/engine/classes/MeshPart#Transparency) is set to at least 0.02, a different
blending method is used that can better represent smooth transparency
gradients and soft edges. This combination does not support all effects
and occlusion may not be perfect.

For more information, see
[Alpha modes](/docs/art/modeling/surface-appearance#alpha-modes).

Provide feedback

---

BaseMaterial

Plugin Security

Read Parallel

Category Material this variant belongs to.

MaterialVariant.BaseMaterial:[Enum.Material](/docs/reference/engine/enums/Material)

Category Material this variant belongs to.

Provide feedback

---

ColorMap

Plugin Security

Read Parallel

Determines the color of the surface.

MaterialVariant.ColorMap:ContentId

This property determines the color of the surface. This texture is
sometimes called the albedo texture. The alpha channel is not used.

Provide feedback

---

ColorMapContent

Plugin Security

Read Parallel

Determines the color of the surface. Only supports asset URIs as textures.

MaterialVariant.ColorMapContent:[Content](/docs/reference/engine/datatypes/Content)

This property determines the color of the surface. This texture is
sometimes called the albedo texture. The alpha channel is not used.

Provide feedback

---

CustomPhysicalProperties

Read Parallel

MaterialVariant.CustomPhysicalProperties:[PhysicalProperties](/docs/reference/engine/datatypes/PhysicalProperties)

Provide feedback

---

EmissiveMaskContent

Plugin Security

Read Parallel

Determines the emissivity across the surface.

MaterialVariant.EmissiveMaskContent:[Content](/docs/reference/engine/datatypes/Content)

This property determines the apparent emissivity across the surface. An
emissive mask is a grayscale image where black pixels correspond to no
emissivity, and white pixels correspond to full emissivity.

The emissive contribution gets added to total lighting contribution across
the surface, and the sum gets multiplied by the albedo texture, which
would be sampled from [ColorMap](/docs/reference/engine/classes/MaterialVariant#ColorMap) if
provided.

Provide feedback

---

EmissiveStrength

Read Parallel

Determines the strength of emissive contribution.

MaterialVariant.EmissiveStrength:[number](/docs/luau/numbers)

This value is a multiplier to control how strong the emissive contribution
is across the surface. If the final contribution of emissives goes beyond
supported dynamic range, it will get clamped; this could result in
emissive contribution appearing all white when using large emissive
strength values. Since this value is a multiplier, the maximum value to
prevent clamping depends on all of the other contributing values,
including [EmissiveTint](/docs/reference/engine/classes/MaterialVariant#EmissiveTint),
[ColorMap](/docs/reference/engine/classes/MaterialVariant#ColorMap) and combined lighting
contribution.

Provide feedback

---

EmissiveTint

Read Parallel

Determines the tinting color for emissive contribution.

MaterialVariant.EmissiveTint:[Color3](/docs/reference/engine/datatypes/Color3)

This value is an RGB color for tinting emissive contribution.

Provide feedback

---

MaterialPattern

Read Parallel

Determines texture tiling method.

MaterialVariant.MaterialPattern:[Enum.MaterialPattern](/docs/reference/engine/enums/MaterialPattern)

Determines texture tiling method.

Provide feedback

---

MetalnessMap

Plugin Security

Read Parallel

Determines which parts of the surface are metal and are non-metal.

MaterialVariant.MetalnessMap:ContentId

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

MaterialVariant.MetalnessMapContent:[Content](/docs/reference/engine/datatypes/Content)

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

MaterialVariant.NormalMap:ContentId

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

MaterialVariant.NormalMapContent:[Content](/docs/reference/engine/datatypes/Content)

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

MaterialVariant.RoughnessMap:ContentId

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

MaterialVariant.RoughnessMapContent:[Content](/docs/reference/engine/datatypes/Content)

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

MaterialVariant.StudsPerTile:[number](/docs/luau/numbers)

Determines the scale of textures. Larger values for this property will
lead to the textures appearing larger, and repeating less frequently.

Provide feedback

---