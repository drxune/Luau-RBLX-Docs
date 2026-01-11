# DataStoreRequestType | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/enums/DataStoreRequestType
Scraped: 2026-01-11T02:46:11.177713Z

## Inherits
- GetAsync()
- UpdateAsync()
- SetAsync()
- IncrementAsync()
- RemoveAsync()
- GetSortedAsync()
- OrderedDataStore
- OnUpdate()
- ListKeysAsync()
- ListVersionsAsync()
- GetVersionAsync()
- RemoveVersionAsync()
- GetRequestBudgetForRequestType()
- GetVersionAtTimeAsync()
- DataStore
- ListDataStoresAsync()
1. [Enums](/docs/reference/engine/enums)
2. /
3. [DataStoreRequestType](/docs/reference/engine/enums/DataStoreRequestType)

English

Feedback

Engine Enum

DataStoreRequestType

---

Indicates the type of data store request being made.

Items

| Name | Value | Summary |
| --- | --- | --- |
| GetAsync | 0 | Refers to [GetAsync()](/docs/reference/engine/classes/GlobalDataStore#GetAsync) and the read of [UpdateAsync()](/docs/reference/engine/classes/GlobalDataStore#UpdateAsync). |
| SetIncrementAsync | 1 | Refers to [SetAsync()](/docs/reference/engine/classes/DataStore#SetAsync), [IncrementAsync()](/docs/reference/engine/classes/DataStore#IncrementAsync), [RemoveAsync()](/docs/reference/engine/classes/DataStore#RemoveAsync), and the write of [UpdateAsync()](/docs/reference/engine/classes/DataStore#UpdateAsync) when it returns a non-nil value. |
| UpdateAsync | 2 | Refers to [UpdateAsync()](/docs/reference/engine/classes/GlobalDataStore#UpdateAsync). |
| GetSortedAsync | 3 | Refers to [GetSortedAsync()](/docs/reference/engine/classes/OrderedDataStore#GetSortedAsync). |
| SetIncrementSortedAsync | 4 | Refers to [SetAsync()](/docs/reference/engine/classes/OrderedDataStore#SetAsync) [IncrementAsync()](/docs/reference/engine/classes/OrderedDataStore#IncrementAsync), [RemoveAsync()](/docs/reference/engine/classes/OrderedDataStore#RemoveAsync), and the write of [UpdateAsync()](/docs/reference/engine/classes/OrderedDataStore#UpdateAsync) while using an [OrderedDataStore](/docs/reference/engine/classes/OrderedDataStore). |
| OnUpdate | 5 | Refers to [OnUpdate()](/docs/reference/engine/classes/GlobalDataStore#OnUpdate). |
| ListAsync | 6 | Refers to [ListKeysAsync()](/docs/reference/engine/classes/DataStore#ListKeysAsync) and [ListVersionsAsync()](/docs/reference/engine/classes/DataStore#ListVersionsAsync). |
| GetVersionAsync | 7 | Refers to [GetVersionAsync()](/docs/reference/engine/classes/DataStore#GetVersionAsync). |
| RemoveVersionAsync | 8 | Refers to [RemoveVersionAsync()](/docs/reference/engine/classes/DataStore#RemoveVersionAsync). |
| StandardRead | 9 | This request type is not yet active, [GetRequestBudgetForRequestType()](/docs/reference/engine/classes/DataStoreService#GetRequestBudgetForRequestType) with this enum will return 0.   Refers to [GetAsync()](/docs/reference/engine/classes/DataStore#GetAsync), [GetVersionAsync()](/docs/reference/engine/classes/DataStore#GetVersionAsync), [GetVersionAtTimeAsync()](/docs/reference/engine/classes/DataStore#GetVersionAtTimeAsync), and the read of [UpdateAsync()](/docs/reference/engine/classes/DataStore#UpdateAsync) for [DataStore](/docs/reference/engine/classes/DataStore). |
| StandardWrite | 10 | This request type is not yet active, [GetRequestBudgetForRequestType()](/docs/reference/engine/classes/DataStoreService#GetRequestBudgetForRequestType) with this enum will return 0.   Refers to [SetAsync()](/docs/reference/engine/classes/DataStore#SetAsync), [IncrementAsync()](/docs/reference/engine/classes/DataStore#IncrementAsync), and the write of [UpdateAsync()](/docs/reference/engine/classes/DataStore#UpdateAsync) for [DataStore](/docs/reference/engine/classes/DataStore). |
| StandardList | 11 | This request type is not yet active, [GetRequestBudgetForRequestType()](/docs/reference/engine/classes/DataStoreService#GetRequestBudgetForRequestType) with this enum will return 0.   Refers to [ListDataStoresAsync()](/docs/reference/engine/classes/DataStoreService#ListDataStoresAsync), and [ListKeysAsync()](/docs/reference/engine/classes/DataStore#ListKeysAsync) and [ListVersionsAsync()](/docs/reference/engine/classes/DataStore#ListVersionsAsync) for [DataStore](/docs/reference/engine/classes/DataStore). |
| StandardRemove | 12 | This request type is not yet active, [GetRequestBudgetForRequestType()](/docs/reference/engine/classes/DataStoreService#GetRequestBudgetForRequestType) with this enum will return 0.   Refers to [RemoveAsync()](/docs/reference/engine/classes/DataStore#RemoveAsync) for [DataStore](/docs/reference/engine/classes/DataStore). |
| OrderedRead | 13 | This request type is not yet active, [GetRequestBudgetForRequestType()](/docs/reference/engine/classes/DataStoreService#GetRequestBudgetForRequestType) with this enum will return 0.   Refers to [GetAsync()](/docs/reference/engine/classes/OrderedDataStore#GetAsync) and the read of [UpdateAsync()](/docs/reference/engine/classes/OrderedDataStore#UpdateAsync) for [OrderedDataStore](/docs/reference/engine/classes/OrderedDataStore). |
| OrderedWrite | 14 | This request type is not yet active, [GetRequestBudgetForRequestType()](/docs/reference/engine/classes/DataStoreService#GetRequestBudgetForRequestType) with this enum will return 0.   Refers to [SetAsync()](/docs/reference/engine/classes/OrderedDataStore#SetAsync), [IncrementAsync()](/docs/reference/engine/classes/OrderedDataStore#IncrementAsync), and the write of [UpdateAsync()](/docs/reference/engine/classes/OrderedDataStore#UpdateAsync) for [OrderedDataStore](/docs/reference/engine/classes/OrderedDataStore). |
| OrderedList | 15 | This request type is not yet active, [GetRequestBudgetForRequestType()](/docs/reference/engine/classes/DataStoreService#GetRequestBudgetForRequestType) with this enum will return 0.   Refers to [GetSortedAsync()](/docs/reference/engine/classes/OrderedDataStore#GetSortedAsync) for [OrderedDataStore](/docs/reference/engine/classes/OrderedDataStore). GetRequestBudgetForRequestType()with this enum will return0`. |
| OrderedRemove | 16 | This request type is not yet active, [GetRequestBudgetForRequestType()](/docs/reference/engine/classes/DataStoreService#GetRequestBudgetForRequestType) with this enum will return 0.   Refers to [RemoveAsync()](/docs/reference/engine/classes/OrderedDataStore#RemoveAsync) for [OrderedDataStore](/docs/reference/engine/classes/OrderedDataStore). |