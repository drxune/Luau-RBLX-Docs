# DockWidgetPluginGuiInfo | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/DockWidgetPluginGuiInfo
Scraped: 2026-01-11T02:42:39.028736Z

## Inherits
- DockWidgetPluginGui
- PluginGui
- Plugin:CreateDockWidgetPluginGui()
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [DockWidgetPluginGuiInfo](/docs/reference/engine/datatypes/DockWidgetPluginGuiInfo)

English

Feedback

Engine Data Type

DockWidgetPluginGuiInfo

Describes details for a [DockWidgetPluginGui](/docs/reference/engine/classes/DockWidgetPluginGui).

---

Summary

Constructors

|  |
| --- |
| [new](#new)(InitialDockState: [Enum.InitialDockState](/docs/reference/engine/enums/InitialDockState),InitialEnabled: [boolean](/docs/luau/booleans),InitialEnabledShouldOverrideRestore: [boolean](/docs/luau/booleans),FloatingXSize: [number](/docs/luau/numbers),FloatingYSize: [number](/docs/luau/numbers),MinWidth: [number](/docs/luau/numbers),MinHeight: [number](/docs/luau/numbers)) |

Properties

|  |
| --- |
| [InitialEnabled](#InitialEnabled):[boolean](/docs/luau/booleans) |
| [InitialEnabledShouldOverrideRestore](#InitialEnabledShouldOverrideRestore):[boolean](/docs/luau/booleans) |
| [FloatingXSize](#FloatingXSize):[number](/docs/luau/numbers) |
| [FloatingYSize](#FloatingYSize):[number](/docs/luau/numbers) |
| [MinWidth](#MinWidth):[number](/docs/luau/numbers) |
| [MinHeight](#MinHeight):[number](/docs/luau/numbers) |

The [DockWidgetPluginGuiInfo](/docs/reference/engine/datatypes/DockWidgetPluginGuiInfo) data type describes details for a
[DockWidgetPluginGui](/docs/reference/engine/classes/DockWidgetPluginGui). This data type is used when constructing a
[PluginGui](/docs/reference/engine/classes/PluginGui) via the plugin's [Plugin:CreateDockWidgetPluginGui()](/docs/reference/engine/classes/Plugin#CreateDockWidgetPluginGui)
method.

---

API Reference

Constructors

new

Returns a new DockWidgetPluginGuiInfo object.

DockWidgetPluginGuiInfo.new(

InitialDockState:[Enum.InitialDockState](/docs/reference/engine/enums/InitialDockState), InitialEnabled:[boolean](/docs/luau/booleans), InitialEnabledShouldOverrideRestore:[boolean](/docs/luau/booleans), FloatingXSize:[number](/docs/luau/numbers), FloatingYSize:[number](/docs/luau/numbers), MinWidth:[number](/docs/luau/numbers), MinHeight:[number](/docs/luau/numbers) )

Parameters

|  |
| --- |
| InitialDockState:[Enum.InitialDockState](/docs/reference/engine/enums/InitialDockState) Default Value: Enum.InitialDockState.Right |
| InitialEnabled:[boolean](/docs/luau/booleans) Default Value: false |
| InitialEnabledShouldOverrideRestore:[boolean](/docs/luau/booleans) Default Value: false |
| FloatingXSize:[number](/docs/luau/numbers) Default Value: 0 |
| FloatingYSize:[number](/docs/luau/numbers) Default Value: 0 |
| MinWidth:[number](/docs/luau/numbers) Default Value: 0 |
| MinHeight:[number](/docs/luau/numbers) Default Value: 0 |

The main constructor function for the [DockWidgetPluginGuiInfo](/docs/reference/engine/datatypes/DockWidgetPluginGuiInfo).

Provide feedback

---

Properties

InitialEnabled

The enabled state of the [PluginGui](/docs/reference/engine/classes/PluginGui) if it does not have a saved
state from a previous session.

DockWidgetPluginGuiInfo.InitialEnabled:[boolean](/docs/luau/booleans)

The initial enabled state of a [PluginGui](/docs/reference/engine/classes/PluginGui) created using this
[DockWidgetPluginGuiInfo](/docs/reference/engine/datatypes/DockWidgetPluginGuiInfo). If a [PluginGui](/docs/reference/engine/classes/PluginGui) with the same
''pluginGuiId'' has previously been created in an earlier session of
Roblox Studio, then it will reload that saved enabled state (unless
InitialEnabledShouldOverrideRestore is true).

Provide feedback

---

InitialEnabledShouldOverrideRestore

If true, will override any saved enabled state with the InitialEnabled
value.

DockWidgetPluginGuiInfo.InitialEnabledShouldOverrideRestore:[boolean](/docs/luau/booleans)

If true, the value of InitialEnabled will override the previously saved
enabled state of a [PluginGui](/docs/reference/engine/classes/PluginGui) being created with this
[DockWidgetPluginGuiInfo](/docs/reference/engine/datatypes/DockWidgetPluginGuiInfo). The previously saved enabled state is
loaded based on the pluginGuiId argument of
[Plugin:CreateDockWidgetPluginGui()](/docs/reference/engine/classes/Plugin#CreateDockWidgetPluginGui).

Provide feedback

---

FloatingXSize

The initial pixel width of the PluginGui when floating.

DockWidgetPluginGuiInfo.FloatingXSize:[number](/docs/luau/numbers)

The initial pixel width of a [PluginGui](/docs/reference/engine/classes/PluginGui) created using this
[DockWidgetPluginGuiInfo](/docs/reference/engine/datatypes/DockWidgetPluginGuiInfo), when the [Enum.InitialDockState](/docs/reference/engine/enums/InitialDockState) is
set to Float.

Provide feedback

---

FloatingYSize

The initial pixel height of the PluginGui when floating.

DockWidgetPluginGuiInfo.FloatingYSize:[number](/docs/luau/numbers)

The initial pixel height of a [PluginGui](/docs/reference/engine/classes/PluginGui) created using this
[DockWidgetPluginGuiInfo](/docs/reference/engine/datatypes/DockWidgetPluginGuiInfo), when the [Enum.InitialDockState](/docs/reference/engine/enums/InitialDockState) is
set to Float.

Provide feedback

---

MinWidth

The minimum pixel width of the PluginGui.

DockWidgetPluginGuiInfo.MinWidth:[number](/docs/luau/numbers)

The minimum width of a [PluginGui](/docs/reference/engine/classes/PluginGui) created using this
[DockWidgetPluginGuiInfo](/docs/reference/engine/datatypes/DockWidgetPluginGuiInfo), in pixels.

Each platform has its own absolute minimum that Roblox will enforce. These
variations exist to account for the contents of the title bar (which
varies by platform) when the widget is floating. For example, on a Mac,
the width can never be less than ~80 pixels to accommodate the
close/minimize/maximize buttons.

Provide feedback

---

MinHeight

The minimum pixel height of the PluginGui.

DockWidgetPluginGuiInfo.MinHeight:[number](/docs/luau/numbers)

The minimum height of a [PluginGui](/docs/reference/engine/classes/PluginGui) created using this
[DockWidgetPluginGuiInfo](/docs/reference/engine/datatypes/DockWidgetPluginGuiInfo), in pixels.

Provide feedback

---