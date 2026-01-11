# RenderFidelity | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/RenderFidelity
Scraped: 2026-01-11T02:42:38.565143Z
1. [Enums](/docs/reference/engine/enums)
2. /
3. [RenderFidelity](/docs/reference/engine/enums/RenderFidelity)

English

Feedback

Engine Enum

RenderFidelity

---

This enum determines the level of detail that
[meshes](/docs/parts/meshes) and
[solid modeled](/docs/parts/solid-modeling) parts will be shown in. The
default is Automatic, meaning the object's detail is based on its distance
from the camera as outlined in the following table.

| Distance From Camera | Render Fidelity |
| --- | --- |
| Less than 250 studs | Highest |
| 250 to 500 studs | Medium |
| 500 or more studs | Lowest |

Items

| Name | Value | Summary |
| --- | --- | --- |
| Automatic | 0 | Object's level of detail is dynamically controlled by its distance from the camera (see table above). |
| Precise | 1 | Object is rendered in the highest fidelity regardless of its distance from the camera. |
| Performance | 2 | Push performance as much as possible, trying to maintain quality if possible, and discarding appearance if that's necessary to reach performance. This means that the performance will always be excellent, but mesh visuals may be affected negatively. |