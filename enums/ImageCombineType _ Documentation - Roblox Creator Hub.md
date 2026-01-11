# ImageCombineType | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/ImageCombineType
Scraped: 2026-01-11T02:42:47.660794Z
1. [Enums](/docs/reference/engine/enums)
2. /
3. [ImageCombineType](/docs/reference/engine/enums/ImageCombineType)

English

Feedback

Engine Enum

ImageCombineType

---

Enum for determining how two images are combined together.

Items

| Name | Value | Summary |
| --- | --- | --- |
| BlendSourceOver | 1 | Blends pixels from the source with pixels from the destination using source over alpha blending. |
| Overwrite | 2 | Overwrites all pixels in the destination image with pixels from the source image. |
| Add | 3 | Adds pixels from the source and pixels from the destination together. |
| Multiply | 4 | Multiplies pixels from the source and pixels from the destination together. RGBA values are multiplied as values between 0 and 1. Values lower than 1 have a darkening effect on the image. |
| AlphaBlend | 5 | Blends pixels from the source with pixels from the destination based on the alpha of the source pixels. Unlike BlendSourceOver, the destination color in AlphaBlend affects the resulting color of the image, regardless of the destination color's alpha. |