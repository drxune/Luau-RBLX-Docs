# SurfaceAppearance | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/SurfaceAppearance
Scraped: 2026-01-11T02:33:36.036236Z

## Inherits
- Instance
- SurfaceAppearance
- Object
- MeshPart
- SurfaceAppearance.ColorMap
- MeshPart.Transparency
- ColorMap
- SurfaceAppearance.AlphaMode
- EmissiveTint
- Lighting.EnvironmentSpecularScale
- Lighting.EnvironmentDiffuseScale
- Lighting.Ambient
- Lighting.OutdoorAmbient
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [SurfaceAppearance](/docs/reference/engine/classes/SurfaceAppearance)

English

Feedback

Engine Class

![SurfaceAppearance](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/SurfaceAppearance-Dark.webp)SurfaceAppearance

An object that allows developers to override the appearance of a MeshPart with
advanced graphics options.

---

Summary

Properties

|  |
| --- |
| [AlphaMode](#AlphaMode):[Enum.AlphaMode](/docs/reference/engine/enums/AlphaMode) |
| [Color](#Color):[Color3](/docs/reference/engine/datatypes/Color3) |
| [ColorMap](#ColorMap):ContentId |
| [ColorMapContent](#ColorMapContent):[Content](/docs/reference/engine/datatypes/Content) |
| [EmissiveMaskContent](#EmissiveMaskContent):[Content](/docs/reference/engine/datatypes/Content) |
| [EmissiveStrength](#EmissiveStrength):[number](/docs/luau/numbers) |
| [EmissiveTint](#EmissiveTint):[Color3](/docs/reference/engine/datatypes/Color3) |
| [MetalnessMap](#MetalnessMap):ContentId |
| [MetalnessMapContent](#MetalnessMapContent):[Content](/docs/reference/engine/datatypes/Content) |
| [NormalMap](#NormalMap):ContentId |
| [NormalMapContent](#NormalMapContent):[Content](/docs/reference/engine/datatypes/Content) |
| [RoughnessMap](#RoughnessMap):ContentId |
| [RoughnessMapContent](#RoughnessMapContent):[Content](/docs/reference/engine/datatypes/Content) |
| [TexturePack](#TexturePack):ContentId |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

SurfaceAppearance objects let you override the appearance of a
[MeshPart](/docs/reference/engine/classes/MeshPart) with advanced graphics options. Most notably, it can apply a
set of Physically‑Based Rendering (PBR) texture images, or maps, on a
single object. Combining multiple texture maps can more accurately simulate
color, roughness, and reflectivity in any lighting environment and can enhance
the visual elements of your assets and environment; see
[PBR Textures](/docs/art/modeling/surface-appearance) for more details.

![A realistic leafy bush](https://prod.docsiteassets.roblox.com/assets/modeling/surface-appearance/SurfaceAppearance-Example-1.jpg)
![A realistic mossy rock](https://prod.docsiteassets.roblox.com/assets/modeling/surface-appearance/SurfaceAppearance-Example-3.jpg)

Appearance of this object on a [MeshPart](/docs/reference/engine/classes/MeshPart) depends on the user's device
and graphics quality level. For best results, you may want to preview your
content with different quality level settings.

Note that most [SurfaceAppearance](/docs/reference/engine/classes/SurfaceAppearance) properties cannot be modified by
scripts, as the necessary pre-processing is usually too expensive during
runtime.

---

API Reference

Properties

AlphaMode

Read Parallel

Determines how the alpha channel of the [SurfaceAppearance.ColorMap](/docs/reference/engine/classes/SurfaceAppearance#ColorMap)
is used.

SurfaceAppearance.AlphaMode:[Enum.AlphaMode](/docs/reference/engine/enums/AlphaMode)

This property determines how the alpha channel of the
[SurfaceAppearance.ColorMap](/docs/reference/engine/classes/SurfaceAppearance#ColorMap) is used.

When set to [Transparency](/docs/reference/engine/enums/AlphaMode) and the
[MeshPart.Transparency](/docs/reference/engine/classes/MeshPart#Transparency) is set to 0, opaque pixels in the
[ColorMap](/docs/reference/engine/classes/SurfaceAppearance#ColorMap) will render as completely
opaque in the 3D scene. This combination works better with depth-based
effects and occlusion.

When set to [Transparency](/docs/reference/engine/enums/AlphaMode) and the
[MeshPart.Transparency](/docs/reference/engine/classes/MeshPart#Transparency) is set to at least 0.02, a different
blending method is used that can better represent smooth transparency
gradients and soft edges. This combination does not support all effects
and occlusion may not be perfect.

See [here](/docs/art/modeling/surface-appearance#alpha-modes) for
more information.

Provide feedback

---

Color

Read Parallel

Applies a tint to your existing colormap. Set directly with color picker
or programmatically with [Color3](/docs/reference/engine/datatypes/Color3).

SurfaceAppearance.Color:[Color3](/docs/reference/engine/datatypes/Color3)

Applies a tint to your existing colormap. Set directly with color picker
or programmatically with [Color3](/docs/reference/engine/datatypes/Color3).

Provide feedback

---

ColorMap

Plugin Security

Read Parallel

Determines the color and opacity of the surface.

SurfaceAppearance.ColorMap:ContentId

This property determines the color and opacity of the surface. This
texture is sometimes called the albedo texture. The alpha channel of
this texture controls its opacity, which behaves differently based on the
[SurfaceAppearance.AlphaMode](/docs/reference/engine/classes/SurfaceAppearance#AlphaMode) setting.

See [here](/docs/art/modeling/surface-appearance#color-albedo) for
more information.

Provide feedback

---

ColorMapContent

Hidden

Plugin Security

Read Parallel

SurfaceAppearance.ColorMapContent:[Content](/docs/reference/engine/datatypes/Content)

Provide feedback

---

EmissiveMaskContent

Plugin Security

Read Parallel

Determines the emissivity across the surface.

SurfaceAppearance.EmissiveMaskContent:[Content](/docs/reference/engine/datatypes/Content)

This property determines the apparent emissivity across the surface. An
emissive mask is a grayscale image where black pixels correspond to no
emissivity, and white pixels correspond to full emissivity.

The emissive contribution gets added to total lighting contribution across
the surface, and the sum gets multiplied by the albedo texture, which
would be sampled from [ColorMap](/docs/reference/engine/classes/SurfaceAppearance#ColorMap) if
provided.

Provide feedback

---

EmissiveStrength

Read Parallel

Determines the strength of emissive contribution.

SurfaceAppearance.EmissiveStrength:[number](/docs/luau/numbers)

This value is a multiplier to control how strong the emissive contribution
is across the surface. If the final contribution of emissives goes beyond
supported dynamic range, it will get clamped; this could result in
emissive contribution appearing all white when using large emissive
strength values. Since this value is a multiplier, the maximum value to
prevent clamping depends on all of the other contributing values,
including [EmissiveTint](/docs/reference/engine/classes/SurfaceAppearance#EmissiveTint),
[ColorMap](/docs/reference/engine/classes/SurfaceAppearance#ColorMap) and combined lighting
contribution.

Provide feedback

---

EmissiveTint

Read Parallel

Determines the tinting color for emissive contribution.

SurfaceAppearance.EmissiveTint:[Color3](/docs/reference/engine/datatypes/Color3)

This value is an RGB color for tinting emissive contribution.

Provide feedback

---

MetalnessMap

Plugin Security

Read Parallel

Determines which parts of the surface are metal or non-metal.

SurfaceAppearance.MetalnessMap:ContentId

This property determines which parts of the surface are metal or
non-metal. The metalness map is a grayscale image where black pixels
correspond to non-metals and white pixels correspond to metals.

Metals only reflect light the same color as the metal, and they reflect
much more light than non-metals. Most pixels in a metalness map will be
either pure black or pure white, while values in between can be used to
simulate dirt or grunge on top of an underlying metal area.

When [Lighting.EnvironmentSpecularScale](/docs/reference/engine/classes/Lighting#EnvironmentSpecularScale) is 0, metalness has no
effect. For the most realistic reflections, it's recommended to set
[Lighting.EnvironmentSpecularScale](/docs/reference/engine/classes/Lighting#EnvironmentSpecularScale) and
[Lighting.EnvironmentDiffuseScale](/docs/reference/engine/classes/Lighting#EnvironmentDiffuseScale) to 1, as well as
[Lighting.Ambient](/docs/reference/engine/classes/Lighting#Ambient) and [Lighting.OutdoorAmbient](/docs/reference/engine/classes/Lighting#OutdoorAmbient) to
(0, 0, 0).

See [here](/docs/art/modeling/surface-appearance#metalness) for more
information.

Provide feedback

---

MetalnessMapContent

Hidden

Plugin Security

Read Parallel

SurfaceAppearance.MetalnessMapContent:[Content](/docs/reference/engine/datatypes/Content)

Provide feedback

---

NormalMap

Plugin Security

Read Parallel

Modifies the lighting of the surface by adding bumps, dents, cracks, and
curves.

SurfaceAppearance.NormalMap:ContentId

This property modifies the lighting of the surface by adding bumps, dents,
cracks, and curves, without adding more polygons. The normal map is an RGB
image that modifies the surface's normal vector used for lighting
calculations. Its R, G, and B channels correspond to the
X, Y, and Z components of the local surface vector
respectively, and byte values of 0 and 255 for each channel correspond
linearly to normal vector components of -1 and 1.016 respectively. This
range is stretched slightly from -1 to 1 so that a byte value of 127 maps
to exactly 0.

The normal vector's Z axis is always defined as the direction of the
underlying mesh's normal. A uniform (127, 127, 255) image translates to
a completely flat normal map where the normal is everywhere perpendicular
to the mesh surface; this format is referred to as a "tangent space"
normal map. Note that Roblox does not support world space or object space
normal maps.

Incorrectly flipped normal components can make bumps appear like indents.
If you import a normal map and notice the lighting looks off, you may need
to invert the G channel of the image. The X and Y axes of the
tangent space frame correspond to the X and Y directions in the
image after it's transformed by the mesh UVs. If you view your normal map
in an image editor as if it were displayed on a surface, normals pointing
towards the right side of the screen should appear more red, and normals
pointing towards the top side of your screen should appear more green. The
terms "DirectX format" and "OpenGL format" are sometimes used to describe
whether the G channel of the normal map is inverted or not (Roblox
expects the OpenGL format).

Roblox also expects imported meshes to include tangents. Modeling software
may also refer to this as "tangent space" information. If you apply a
normal map and it does not seem to make any visual difference, you may
need to re-export your mesh along with its tangent information from the
modeling software.

See [here](/docs/art/modeling/surface-appearance#normal) for more
information.

Provide feedback

---

NormalMapContent

Hidden

Plugin Security

Read Parallel

SurfaceAppearance.NormalMapContent:[Content](/docs/reference/engine/datatypes/Content)

Provide feedback

---

RoughnessMap

Plugin Security

Read Parallel

Determines the apparent roughness across the surface.

SurfaceAppearance.RoughnessMap:ContentId

This property determines the apparent roughness across the surface. The
roughness map is a grayscale image where black pixels correspond to a
maximally smooth surface, and white pixels correspond to a maximally rough
surface.

Note that surface roughness works on a very small scale. Reflections on
smooth surfaces are sharp and concentrated, while reflections on rough
surfaces are more blurry and dispersed.

See [here](/docs/art/modeling/surface-appearance#roughness) for more
information.

Provide feedback

---

RoughnessMapContent

Hidden

Plugin Security

Read Parallel

SurfaceAppearance.RoughnessMapContent:[Content](/docs/reference/engine/datatypes/Content)

Provide feedback

---

TexturePack

Roblox Security

Read Parallel

SurfaceAppearance.TexturePack:ContentId

Provide feedback

---