# PluginManager | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/PluginManager
Scraped: 2026-01-11T02:27:22.656411Z

## Tags
- Not Creatable

## Inherits
- Object
- Instance
- PluginManager
- Plugin
- Selection
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [PluginManager](/docs/reference/engine/classes/PluginManager)

English

Feedback

Engine Class

PluginManager

Not Creatable

---

Summary

Methods

|  |
| --- |
| [CreatePlugin](#CreatePlugin)():[Instance](/docs/reference/engine/datatypes/Instance)  Deprecated |
| [ExportPlace](#ExportPlace)(filePath: [string](/docs/luau/strings)):() |
| [ExportSelection](#ExportSelection)(filePath: [string](/docs/luau/strings)):() |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

PluginManager is a deprecated singleton that was previously required to
create plugins. It still has some applicable uses, such as if you need to
create a [Plugin](/docs/reference/engine/classes/Plugin) object from Studio's
[Command Bar](/docs/studio/ui-overview#command-bar).

---

API Reference

Methods

CreatePlugin

Deprecated

Show details

---

ExportPlace

Plugin Security

Exports the place to an .obj file that is saved to the path chosen by
the user in a file save dialogue.

PluginManager:ExportPlace(filePath:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| filePath:[string](/docs/luau/strings) |

Returns

()

This method exports all geometry in the place to an .obj file. The file
is saved to the path chosen by the user in a file save dialogue (the
filePath argument is ignored).

Provide feedback

---

ExportSelection

Plugin Security

Exports the current [Selection](/docs/reference/engine/classes/Selection) to an .obj file that is saved to
the path chosen by the user in a file save dialogue.

PluginManager:ExportSelection(filePath:[string](/docs/luau/strings)):()

Parameters

|  |
| --- |
| filePath:[string](/docs/luau/strings) |

Returns

()

This method exports all geometry in the current [Selection](/docs/reference/engine/classes/Selection) to an
.obj file. The file is saved to the path chosen by the user in a file
save dialogue (the filePath argument is ignored).

Provide feedback

---