# UserService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/UserService
Scraped: 2026-01-11T02:29:19.033489Z

## Tags
- Not Creatable
- Service

## Inherits
- Object
- Instance
- UserService
- UserIds
- DataModel
- DisplayName
- UserId
- GetUserInfosByUserIdsAsync()
- HasVerifiedBadge
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [UserService](/docs/reference/engine/classes/UserService)

English

Feedback

Engine Class

![UserService](https://assets.create.roblox.com/docs/c42ae5b077702736b401df61580c08ca26d9600a/assets/engine-reference-icons/UserService-Dark.webp)UserService

A service that handles queries regarding users on the Roblox platform.

Not Creatable

Service

---

Summary

Methods

|  |
| --- |
| [GetUserInfosByUserIdsAsync](#GetUserInfosByUserIdsAsync)(userIds: [Array](/docs/luau/tables#arrays)):[Array](/docs/luau/tables#arrays) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A service that handles queries regarding users on the Roblox platform.

---

API Reference

Methods

GetUserInfosByUserIdsAsync

Yields

Returns an array of user information including user name and display name.

UserService:GetUserInfosByUserIdsAsync(userIds:[Array](/docs/luau/tables#arrays)):[Array](/docs/luau/tables#arrays)

Parameters

|  |
| --- |
| userIds:[Array](/docs/luau/tables#arrays)  An array of [UserIds](/docs/reference/engine/classes/Player#UserId) requested. |

Returns

[Array](/docs/luau/tables#arrays)

An array of dictionary objects that contain user information.

This function lets you request information about users outside of the
current [DataModel](/docs/reference/engine/classes/DataModel) in bulk. The input and output values are both
arrays.

* The order of the user info objects in the return value's array may not
  match the order of the [UserIds](/docs/reference/engine/classes/Player#UserId) sent in the input
  parameter's array. Use the Id field of the user info object to
  identify your input array with the output array.
* It's possible to receive fewer user info objects than requested if one
  or more of the [UserIds](/docs/reference/engine/classes/Player#UserId) in the request array are
  invalid, such as negative numbers or user IDs that don't have accounts
  associated with them. It's possible to receive a response with zero
  results if all [UserIds](/docs/reference/engine/classes/Player#UserId) are invalid.
* If a Roblox user does not have a [DisplayName](/docs/reference/engine/classes/Player#DisplayName)
  associated with their account, this function will instead return the
  same string as the user's username in their info object's DisplayName
  field. While a user's [UserId](/docs/reference/engine/classes/Player#UserId) will never change,
  they may change their username or display name, so the same input
  [UserIds](/docs/reference/engine/classes/Player#UserId) may return a different string for these
  fields from one day to another.
* Since
  [GetUserInfosByUserIdsAsync()](/docs/reference/engine/classes/UserService#GetUserInfosByUserIdsAsync)
  makes an external web request, it will yield and may fail if the backend
  service is experiencing interruptions. Ensure you can handle downtime
  appropriately by wrapping this method with a
  [pcall()](/docs/reference/engine/globals/LuaGlobals#pcall).
* Results are limited to 250 per minute, so if you receive an HTTP 429
  error, try again later, ideally after reducing the number of
  [UserIds](/docs/reference/engine/classes/Player#UserId) in your input array, reducing the number
  of method calls, or both.

The signature of a singular user info object is:

| Key | Type | Description |
| --- | --- | --- |
| Id | number | The [UserId](/docs/reference/engine/classes/Player#UserId) associated with the user. |
| Username | string | The username associated with the user. |
| DisplayName | string | The [DisplayName](/docs/reference/engine/classes/Player#DisplayName) associated with the user. |
| HasVerifiedBadge | boolean | The [HasVerifiedBadge](/docs/reference/engine/classes/Player#HasVerifiedBadge) value associated with the user. |

Code Samples

UserService:GetUserInfosByUserIdsAsync Example

```
local UserService = game:GetService("UserService")



local success, result = pcall(function()



return UserService:GetUserInfosByUserIdsAsync({ 156, 1, 735878936 })



end)



if success then



for _, userInfo in ipairs(result) do



print("Id:", userInfo.Id)



print("Username:", userInfo.Username)



print("DisplayName:", userInfo.DisplayName)



end



else



-- An error occurred



end
```

Provide feedback

---