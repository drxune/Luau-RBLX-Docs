# ConfigSnapshot | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/ConfigSnapshot
Scraped: 2026-01-11T02:29:59.427557Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Object
- ConfigSnapshot
- ConfigService:GetConfigAsync()
- ConfigService:GetConfigForPlayerAsync()
- ConfigSnapshot:Refresh()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [ConfigSnapshot](/docs/reference/engine/classes/ConfigSnapshot)

English

Feedback

Engine Class

ConfigSnapshot

A snapshot of configuration values at a given version. Can be player-specific.

Not Creatable

Not Replicated

---

Summary

Properties

|  |
| --- |
| [Error](#Error):[Enum.ConfigSnapshotErrorState](/docs/reference/engine/enums/ConfigSnapshotErrorState) |
| [Outdated](#Outdated):[boolean](/docs/luau/booleans) |

Methods

|  |
| --- |
| [GetValue](#GetValue)(key: [string](/docs/luau/strings)):Variant |
| [GetValueChangedSignal](#GetValueChangedSignal)(key: [string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |
| [Refresh](#Refresh)():() |

Events

|  |
| --- |
| [UpdateAvailable](#UpdateAvailable)():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal) |

Inherited Members

6 inherited from [Object](/docs/reference/engine/classes/Object)

An object with the configuration values at a specific version. A snapshot can
be targeted to a single player to apply experimentation values. This is
returned by [ConfigService:GetConfigAsync()](/docs/reference/engine/classes/ConfigService#GetConfigAsync) and
[ConfigService:GetConfigForPlayerAsync()](/docs/reference/engine/classes/ConfigService#GetConfigForPlayerAsync).

For more information, see
[Experience configs](/docs/production/configs).

---

API Reference

Properties

Error

Read Only

Not Replicated

Read Parallel

Populated if snapshot was in an error state.

ConfigSnapshot.Error:[Enum.ConfigSnapshotErrorState](/docs/reference/engine/enums/ConfigSnapshotErrorState)

Populated if snapshot was in an error state.

Provide feedback

---

Outdated

Read Only

Not Replicated

Read Parallel

If true, indicates the snapshot is outdated and can be refreshed to newer
values.

ConfigSnapshot.Outdated:[boolean](/docs/luau/booleans)

If true, indicates the snapshot is outdated and can be refreshed to newer
values.

Provide feedback

---

Methods

GetValue

Returns the value for the given key.

ConfigSnapshot:GetValue(key:[string](/docs/luau/strings)):Variant

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings)  Key of the configuration to get the value for. |

Returns

Variant

The value of the configuration for the given key.

Returns the value for the provided key in the snapshot.

Provide feedback

---

GetValueChangedSignal

Returns a signal that fires when the value for the given key changes due
to a refresh.

ConfigSnapshot:GetValueChangedSignal(key:[string](/docs/luau/strings)):[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings)  Key of the configuration to get the change signal for. |

Returns

[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

A DataType.RBXScriptSignal that fires when the value for the given
key changes upon refresh.

Returns a signal that fires when the value for the provided key changes
after calling [ConfigSnapshot:Refresh()](/docs/reference/engine/classes/ConfigSnapshot#Refresh).

Provide feedback

---

Refresh

Refreshes the snapshot to the latest configuration values.

ConfigSnapshot:Refresh():()

Returns

()

Refreshes the snapshot to the latest configuration values from the
service. If not called, the snapshot will continue to reflect the values
at the time it was created or last refreshed.

Provide feedback

---

Events

UpdateAvailable

Fires when a newer version of the configuration is available.

ConfigSnapshot.UpdateAvailable():[RBXScriptSignal](/docs/reference/engine/datatypes/RBXScriptSignal)

Fires when a newer version of the configuration is available than the
current snapshot. You can perform validation and/or call
[ConfigSnapshot:Refresh()](/docs/reference/engine/classes/ConfigSnapshot#Refresh) to update to the latest values.

Provide feedback

---