# HttpRbxApiService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/HttpRbxApiService
Scraped: 2026-01-11T02:32:09.320914Z

## Tags
- Not Creatable
- Service

## Inherits
- Instance
- HttpRbxApiService
- Object
- HttpService
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [HttpRbxApiService](/docs/reference/engine/classes/HttpRbxApiService)

English

Feedback

Engine Class

HttpRbxApiService

An internal service whose functionality is not available to developers.

Not Creatable

Service

---

Summary

Methods

|  |
| --- |
| [RequestLimitedAsync](#RequestLimitedAsync)(requestOptions: [Dictionary](/docs/luau/tables#dictionaries),priority: [Enum.ThrottlingPriority](/docs/reference/engine/enums/ThrottlingPriority),content\_type: [Enum.HttpContentType](/docs/reference/engine/enums/HttpContentType),httpRequestType: [Enum.HttpRequestType](/docs/reference/engine/enums/HttpRequestType)):[string](/docs/luau/strings) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A version of the [HttpService](/docs/reference/engine/classes/HttpService) used by the admins. Unlike the regular
service, this one can send GET/POST requests to roblox.com

---

API Reference

Methods

RequestLimitedAsync

Yields

HttpRbxApiService:RequestLimitedAsync(

requestOptions:[Dictionary](/docs/luau/tables#dictionaries), priority:[Enum.ThrottlingPriority](/docs/reference/engine/enums/ThrottlingPriority), content\_type:[Enum.HttpContentType](/docs/reference/engine/enums/HttpContentType), httpRequestType:[Enum.HttpRequestType](/docs/reference/engine/enums/HttpRequestType)

):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| requestOptions:[Dictionary](/docs/luau/tables#dictionaries) |
| priority:[Enum.ThrottlingPriority](/docs/reference/engine/enums/ThrottlingPriority) Default Value: "Default" |
| content\_type:[Enum.HttpContentType](/docs/reference/engine/enums/HttpContentType) Default Value: "ApplicationJson" |
| httpRequestType:[Enum.HttpRequestType](/docs/reference/engine/enums/HttpRequestType) Default Value: "Default" |

Returns

[string](/docs/luau/strings)

Provide feedback

---