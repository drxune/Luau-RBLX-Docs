# TextureMode | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/TextureMode
Scraped: 2026-01-11T02:43:17.633934Z

## Inherits
- Trail
- Beam
- TextureLength
1. [Enums](/docs/reference/engine/enums)
2. /
3. [TextureMode](/docs/reference/engine/enums/TextureMode)

English

Feedback

Engine Enum

TextureMode

---

Describes how the texture of a [Trail](/docs/reference/engine/classes/Trail) or [Beam](/docs/reference/engine/classes/Beam) behaves.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Stretch | 0 | For a [Trail](/docs/reference/engine/classes/Trail), the texture will stretch out based on the lifetime of the trail, and shrink inwards if the trail's attachments stop moving.  For a [Beam](/docs/reference/engine/classes/Beam), the texture will repeat [TextureLength](/docs/reference/engine/classes/Beam#TextureLength) times across the beam's overall length. See [here](/docs/effects/beams#texture-lengthmode) for details. |
| Wrap | 1 | For a [Trail](/docs/reference/engine/classes/Trail), the texture will be tiled as the length of the trail changes, but the textures will remain stationary relative to their attachments.  For a [Beam](/docs/reference/engine/classes/Beam), the texture repetitions will equal the beam's overall length (in studs) divided by its [TextureLength](/docs/reference/engine/classes/Beam#TextureLength). See [here](/docs/effects/beams#texture-lengthmode) for details. |
| Static | 2 | For a [Trail](/docs/reference/engine/classes/Trail), the texture will be rolled out as the attachments move, and they will remain in place until their lifetime is met. This setting is ideal for trail textures that should appear "stamped" where rendered, such as paw prints or tire tracks.  This value is not supported for [Beam](/docs/reference/engine/classes/Beam) and therefore behaves identically to Wrap. |