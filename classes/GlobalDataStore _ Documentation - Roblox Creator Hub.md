# GlobalDataStore | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/GlobalDataStore
Scraped: 2026-01-11T02:35:24.598981Z

## Tags
- Not Creatable
- Not Replicated

## Inherits
- Instance
- GlobalDataStore
- DataStoreGetOptions
- DataStoreIncrementOptions
- DataStoreSetOptions
- Object
- DataStore
- OrderedDataStore
- DataStoreService
- DataStoreKeyInfo
- DataStoreOptions.AllScopes
- DataStoreService:GetDataStore()
- UserIds
- GlobalDataStore:GetAsync()
- GlobalDataStore:SetAsync()
- GlobalDataStore:UpdateAsync()
- DataStore:GetVersionAsync()
- GlobalDataStores
- OrderedDataStores
- DataStore:ListVersionsAsync()
- RemoveAsync()
- GlobalDataStore:RemoveAsync()
- DataStore:RemoveVersionAsync()
- GetVersionAsync()
- RemoveVersionAsync()
- DataStoreKeyInfo:GetUserIds()
- DataStoreKeyInfo:GetMetadata()
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [GlobalDataStore](/docs/reference/engine/classes/GlobalDataStore)

English

Feedback

Engine Class

GlobalDataStore

An object that exposes methods to access a single data store.

Not Creatable

Not Replicated

---

Summary

Methods

|  |
| --- |
| [GetAsync](#GetAsync)(key: [string](/docs/luau/strings),options: [DataStoreGetOptions](/docs/reference/engine/classes/DataStoreGetOptions)):[Tuple](/docs/luau/tuples) |
| [IncrementAsync](#IncrementAsync)(key: [string](/docs/luau/strings),delta: [number](/docs/luau/numbers),userIds: [Array](/docs/luau/tables#arrays),options: [DataStoreIncrementOptions](/docs/reference/engine/classes/DataStoreIncrementOptions)):Variant |
| [OnUpdate](#OnUpdate)(key: [string](/docs/luau/strings),callback: [function](/docs/luau/functions)):[RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection)  Deprecated |
| [RemoveAsync](#RemoveAsync)(key: [string](/docs/luau/strings)):[Tuple](/docs/luau/tuples) |
| [SetAsync](#SetAsync)(key: [string](/docs/luau/strings),value: Variant,userIds: [Array](/docs/luau/tables#arrays),options: [DataStoreSetOptions](/docs/reference/engine/classes/DataStoreSetOptions)):Variant |
| [UpdateAsync](#UpdateAsync)(key: [string](/docs/luau/strings),transformFunction: [function](/docs/luau/functions)):[Tuple](/docs/luau/tuples) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Inherited by

[DataStore](/docs/reference/engine/classes/DataStore), [OrderedDataStore](/docs/reference/engine/classes/OrderedDataStore)

A GlobalDataStore exposes functions for saving and loading data for the
[DataStoreService](/docs/reference/engine/classes/DataStoreService).

See [Data stores](/docs/cloud-services/data-stores) for an
in-depth guide on data structure, management, error handling, limits, and
more.

Ordered data stores do not support versioning and metadata, so
[DataStoreKeyInfo](/docs/reference/engine/classes/DataStoreKeyInfo) is always nil for keys in an
[OrderedDataStore](/docs/reference/engine/classes/OrderedDataStore). If you need versioning and metadata support, use a
[DataStore](/docs/reference/engine/classes/DataStore).

---

API Reference

Methods

GetAsync

Yields

Returns the value of a key in a specified data store and a
[DataStoreKeyInfo](/docs/reference/engine/classes/DataStoreKeyInfo) instance.

GlobalDataStore:GetAsync(

key:[string](/docs/luau/strings), options:[DataStoreGetOptions](/docs/reference/engine/classes/DataStoreGetOptions)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings)  The key name for which the value is requested. If [DataStoreOptions.AllScopes](/docs/reference/engine/classes/DataStoreOptions#AllScopes) was set to true when accessing the data store through [DataStoreService:GetDataStore()](/docs/reference/engine/classes/DataStoreService#GetDataStore), this key name must be prepended with the original scope as in "scope/key". |
| options:[DataStoreGetOptions](/docs/reference/engine/classes/DataStoreGetOptions) Default Value: "nil" |

Returns

[Tuple](/docs/luau/tuples)

The value of the entry in the data store with the given key and a
[DataStoreKeyInfo](/docs/reference/engine/classes/DataStoreKeyInfo) instance that includes the version number,
date and time the version was created, and functions to retrieve
[UserIds](/docs/reference/engine/classes/Player#UserId) and metadata.

This function returns the latest value of the provided key and a
[DataStoreKeyInfo](/docs/reference/engine/classes/DataStoreKeyInfo) instance. If the key does not exist or if the
latest version has been marked as deleted, both return values will be
nil.

Keys are cached locally for 4 seconds after the first read. A
[GlobalDataStore:GetAsync()](/docs/reference/engine/classes/GlobalDataStore#GetAsync) call within these 4 seconds returns a
value from the cache. Modifications to the key by
[GlobalDataStore:SetAsync()](/docs/reference/engine/classes/GlobalDataStore#SetAsync) or
[GlobalDataStore:UpdateAsync()](/docs/reference/engine/classes/GlobalDataStore#UpdateAsync) apply to the cache immediately and
restart the 4 second timer.

To get a specific version, such as a version before the latest, use
[DataStore:GetVersionAsync()](/docs/reference/engine/classes/DataStore#GetVersionAsync).

Provide feedback

---

IncrementAsync

Yields

Increments the value of a key by the provided amount (both must be
integers).

GlobalDataStore:IncrementAsync(

key:[string](/docs/luau/strings), delta:[number](/docs/luau/numbers), userIds:[Array](/docs/luau/tables#arrays), options:[DataStoreIncrementOptions](/docs/reference/engine/classes/DataStoreIncrementOptions)

):Variant

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings)  Key name for which the value should be updated. If [DataStoreOptions.AllScopes](/docs/reference/engine/classes/DataStoreOptions#AllScopes) was set to true when accessing the data store through [DataStoreService:GetDataStore()](/docs/reference/engine/classes/DataStoreService#GetDataStore), this key name must be prepended with the original scope as in "scope/key". |
| delta:[number](/docs/luau/numbers) Default Value: 1 Amount to increment the current value by. |
| userIds:[Array](/docs/luau/tables#arrays) Default Value: "{}" (Optional) A table of [UserIds](/docs/reference/engine/classes/Player#UserId) to associate with the key. |
| options:[DataStoreIncrementOptions](/docs/reference/engine/classes/DataStoreIncrementOptions) Default Value: "nil" (Optional) [DataStoreIncrementOptions](/docs/reference/engine/classes/DataStoreIncrementOptions) instance that combines multiple additional parameters as custom metadata and allows for future extensibility. |

Returns

Variant

The updated value of the entry in the data store with the given key.

This function increments the value of a key by the provided amount (both
must be integers).

Values in [GlobalDataStores](/docs/reference/engine/classes/GlobalDataStore) are versioned as
outlined in
[versioning](/docs/cloud-services/data-stores/versioning-listing-and-caching#versioning).
[OrderedDataStores](/docs/reference/engine/classes/OrderedDataStore) do not support versioning, so
calling this method on an ordered data store key will overwrite the
current value with the incremented value and make previous versions
inaccessible.

Provide feedback

---

OnUpdate

Deprecated

Show details

---

RemoveAsync

Yields

Removes the specified key while also retaining an accessible version.

GlobalDataStore:RemoveAsync(key:[string](/docs/luau/strings)):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings)  Key name to be removed. If [DataStoreOptions.AllScopes](/docs/reference/engine/classes/DataStoreOptions#AllScopes) was set to true when accessing the data store through [DataStoreService:GetDataStore()](/docs/reference/engine/classes/DataStoreService#GetDataStore), this key name must be prepended with the original scope as in "scope/key". |

Returns

[Tuple](/docs/luau/tuples)

The value of the data store prior to deletion and a
[DataStoreKeyInfo](/docs/reference/engine/classes/DataStoreKeyInfo) instance that includes the version number,
date and time the version was created, and functions to retrieve
[UserIds](/docs/reference/engine/classes/Player#UserId) and metadata.

This function marks the specified key as deleted by creating a new
"tombstone" version of the key. Prior to this, it returns the latest
version prior to the remove call.

After a key is removed via this function,
[GlobalDataStore:GetAsync()](/docs/reference/engine/classes/GlobalDataStore#GetAsync) calls for the key will return nil.
Older versions of the key remain accessible through
[DataStore:ListVersionsAsync()](/docs/reference/engine/classes/DataStore#ListVersionsAsync) and
[DataStore:GetVersionAsync()](/docs/reference/engine/classes/DataStore#GetVersionAsync), assuming they have not expired.

[OrderedDataStore](/docs/reference/engine/classes/OrderedDataStore) does not support versioning, so calling
[RemoveAsync()](/docs/reference/engine/classes/GlobalDataStore#RemoveAsync) on an
[OrderedDataStore](/docs/reference/engine/classes/OrderedDataStore) key will permanently delete it.

Removed objects will be deleted permanently after 30 days.

If the previous values were already deleted via
[GlobalDataStore:RemoveAsync()](/docs/reference/engine/classes/GlobalDataStore#RemoveAsync) or
[DataStore:RemoveVersionAsync()](/docs/reference/engine/classes/DataStore#RemoveVersionAsync), the function will return nil,
nil for value and [DataStoreKeyInfo](/docs/reference/engine/classes/DataStoreKeyInfo) respectively.

Provide feedback

---

SetAsync

Yields

Sets the value of the data store for the given key.

GlobalDataStore:SetAsync(

key:[string](/docs/luau/strings), value:Variant, userIds:[Array](/docs/luau/tables#arrays), options:[DataStoreSetOptions](/docs/reference/engine/classes/DataStoreSetOptions)

):Variant

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings)  Key name for which the value should be set. If [DataStoreOptions.AllScopes](/docs/reference/engine/classes/DataStoreOptions#AllScopes) was set to true when accessing the data store through [DataStoreService:GetDataStore()](/docs/reference/engine/classes/DataStoreService#GetDataStore), this key name must be prepended with the original scope as in "scope/key". |
| value:Variant  The value that the data store key will be set to. |
| userIds:[Array](/docs/luau/tables#arrays) Default Value: "{}" Table of [UserIds](/docs/reference/engine/classes/Player#UserId), highly recommended to assist with GDPR tracking/removal. |
| options:[DataStoreSetOptions](/docs/reference/engine/classes/DataStoreSetOptions) Default Value: "nil" (Optional) [DataStoreSetOptions](/docs/reference/engine/classes/DataStoreSetOptions) instance that allows for metadata specification on the key. |

Returns

Variant

The version identifier of the newly created version. It can be used to
retrieve key info using
[GetVersionAsync()](/docs/reference/engine/classes/DataStore#GetVersionAsync) or to remove it
using [RemoveVersionAsync()](/docs/reference/engine/classes/DataStore#RemoveVersionAsync).

This function sets the latest value, [UserIds](/docs/reference/engine/classes/Player#UserId), and
metadata for the given key.

Values in [GlobalDataStores](/docs/reference/engine/classes/GlobalDataStore) are versioned as
outlined in
[versioning](/docs/cloud-services/data-stores/versioning-listing-and-caching#versioning).
[OrderedDataStores](/docs/reference/engine/classes/OrderedDataStore) do not support versioning, so
calling this method on an ordered data store key will overwrite the
current value and make previous versions inaccessible.

Metadata definitions must always be updated with a value, even if there
are no changes to the current value; otherwise the current value will be
lost.

Any string being stored in a data store must be valid
[UTF-8](/docs/reference/engine/libraries/utf8). In UTF-8, values greater than 127 are used
exclusively for encoding multi-byte codepoints, so a single byte greater
than 127 will not be valid UTF-8 and the
[GlobalDataStore:SetAsync()](/docs/reference/engine/classes/GlobalDataStore#SetAsync) attempt will fail.

#### Set vs. Update

[GlobalDataStore:SetAsync()](/docs/reference/engine/classes/GlobalDataStore#SetAsync) is best for a quick update of a
specific key, and it only counts against the write limit. However, it may
cause data inconsistency if two servers attempt to set the same key at the
same time. [GlobalDataStore:UpdateAsync()](/docs/reference/engine/classes/GlobalDataStore#UpdateAsync) is safer for handling
multi-server attempts because it reads the current key value (from
whatever server last updated it) before making any changes. However, it's
somewhat slower because it reads before it writes, and it also counts
against both the read and write limit.

Provide feedback

---

UpdateAsync

Yields

Updates a key's value with a new value from the specified callback
function.

GlobalDataStore:UpdateAsync(

key:[string](/docs/luau/strings), transformFunction:[function](/docs/luau/functions)

):[Tuple](/docs/luau/tuples)

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings)  Key name for which the value should be updated. If [DataStoreOptions.AllScopes](/docs/reference/engine/classes/DataStoreOptions#AllScopes) was set to true when accessing the data store through [DataStoreService:GetDataStore()](/docs/reference/engine/classes/DataStoreService#GetDataStore), this key name must be prepended with the original scope as in "scope/key". |
| transformFunction:[function](/docs/luau/functions)  Transform function that takes the current value and [DataStoreKeyInfo](/docs/reference/engine/classes/DataStoreKeyInfo) as parameters and returns the new value along with optional [UserIds](/docs/reference/engine/classes/Player#UserId) and metadata. |

Returns

[Tuple](/docs/luau/tuples)

The updated value of the entry in the data store with the given key
and a [DataStoreKeyInfo](/docs/reference/engine/classes/DataStoreKeyInfo) instance that includes the version
number, date and time the version was created, and functions to
retrieve [UserIds](/docs/reference/engine/classes/Player#UserId) and metadata.

This function retrieves the value and metadata of a key from the data
store and updates it with a new value determined by the callback function
specified through the second parameter. If the callback returns nil, the
write operation is cancelled and the value remains unchanged.

Values in [GlobalDataStores](/docs/reference/engine/classes/GlobalDataStore) are versioned as
outlined in
[versioning](/docs/cloud-services/data-stores/versioning-listing-and-caching#versioning).
[OrderedDataStores](/docs/reference/engine/classes/OrderedDataStore) do not support versioning, so
calling this method on an ordered data store key will overwrite the
current value and make previous versions inaccessible.

In cases where another game server updated the key in the short timespan
between retrieving the key's current value and setting the key's value,
[GlobalDataStore:UpdateAsync()](/docs/reference/engine/classes/GlobalDataStore#UpdateAsync) will call the function again,
discarding the result of the previous call. The function will be called as
many times as needed until the data is saved or until the callback
function returns nil. This can be used to ensure that no data is
overwritten.

Any string being stored in a data store must be valid
[UTF-8](/docs/reference/engine/libraries/utf8). In UTF-8, values greater than 127 are used
exclusively for encoding multi-byte codepoints, so a single byte greater
than 127 will not be valid UTF-8 and the
[GlobalDataStore:UpdateAsync()](/docs/reference/engine/classes/GlobalDataStore#UpdateAsync) attempt will fail.

#### Set vs. Update

[GlobalDataStore:SetAsync()](/docs/reference/engine/classes/GlobalDataStore#SetAsync) is best for a quick update of a
specific key, and it only counts against the write limit. However, it may
cause data inconsistency if two servers attempt to set the same key at the
same time. [GlobalDataStore:UpdateAsync()](/docs/reference/engine/classes/GlobalDataStore#UpdateAsync) is safer for handling
multi-server attempts because it reads the current key value (from
whatever server last updated it) before making any changes. However, it's
somewhat slower because it reads before it writes, and it also counts
against both the read and write limit.

#### Callback Function

The callback function accepts two arguments:

* Current value of the key prior to the update.
* [DataStoreKeyInfo](/docs/reference/engine/classes/DataStoreKeyInfo) instance that contains the latest version
  information (this argument can be ignored if metadata is not being
  used).

In turn, the callback function returns up to three values:

* The new value to set for the key.
* An array of [UserIds](/docs/reference/engine/classes/Player#UserId) to associate with the key.
  [DataStoreKeyInfo:GetUserIds()](/docs/reference/engine/classes/DataStoreKeyInfo#GetUserIds) should be returned unless the
  existing IDs are being changed; otherwise all existing IDs will be
  cleared.
* A Luau table containing metadata to associate with the key.
  [DataStoreKeyInfo:GetMetadata()](/docs/reference/engine/classes/DataStoreKeyInfo#GetMetadata) should be returned unless the
  existing metadata is being changed; otherwise all existing metadata will
  be cleared.

If the callback returns nil instead, the current server will stop
attempting to update the key.

The callback function cannot yield, so do not include calls like
[task.wait()](/docs/reference/engine/libraries/task#wait).

Provide feedback

---