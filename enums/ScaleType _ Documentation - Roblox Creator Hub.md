# ScaleType | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/ScaleType
Scraped: 2026-01-11T02:46:25.720018Z

## Inherits
- ImageLabel
- ImageButton
- ImageLabel.SliceCenter
- ImageButton.SliceCenter
1. [Enums](/docs/reference/engine/enums)
2. /
3. [ScaleType](/docs/reference/engine/enums/ScaleType)

English

Feedback

Engine Enum

ScaleType

---

Determines how an image (of a [ImageLabel](/docs/reference/engine/classes/ImageLabel) or [ImageButton](/docs/reference/engine/classes/ImageButton)) is
scaled.

Items

| Name | Value | Summary |
| --- | --- | --- |
| Stretch | 0 | The image is stretched to fit within the element. |
| Slice | 1 | 9-Slice scaling: slice the image into 9 regions and apply different scaling rules to each region. The slice boundaries are determined by [ImageLabel.SliceCenter](/docs/reference/engine/classes/ImageLabel#SliceCenter) or [ImageButton.SliceCenter](/docs/reference/engine/classes/ImageButton#SliceCenter). See [UI 9-Slice Design](/docs/ui/9-slice) for more information. . |
| Tile | 2 | The image is tiled to fit within the element. For example, if the element is twice the X dimension of the image, the image will appear twice (2 tiles). |
| Fit | 3 | The image is scaled fit within the element X or Y dimension (whichever fits first). |
| Crop | 4 | The image is cropped to fit within the element. |