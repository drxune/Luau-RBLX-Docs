# Secret | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/datatypes/Secret
Scraped: 2026-01-11T02:41:45.070455Z

## Inherits
- HttpService:GetSecret()
1. [Data types](/docs/reference/engine/datatypes)
2. /
3. [Secret](/docs/reference/engine/datatypes/Secret)

English

Feedback

Engine Data Type

Secret

Stores secret non-printable content.

---

Summary

Methods

|  |
| --- |
| [AddPrefix](#AddPrefix)(prefix: [string](/docs/luau/strings)):[Secret](/docs/reference/engine/datatypes/Secret) |
| [AddSuffix](#AddSuffix)(suffix: [string](/docs/luau/strings)):[Secret](/docs/reference/engine/datatypes/Secret) |

The [Secret](/docs/reference/engine/datatypes/Secret) data type stores the secret content returned by
[HttpService:GetSecret()](/docs/reference/engine/classes/HttpService#GetSecret). It cannot be printed or logged, but can be
modified using built-in functions:

```
local HttpService = game:GetService("HttpService")



local mySiteApiKey = HttpService:GetSecret("my_site")



local url = "https://apis.mysite.com?apiKey="



local urlWithKey = mySiteApiKey:AddPrefix(url)



local params = "&request=join&user=myname"



local resultingUrl = urlWithKey:AddSuffix(params)
```

---

API Reference

Methods

AddPrefix

Prepends a string to the secret content.

Secret:AddPrefix(prefix:[string](/docs/luau/strings)):[Secret](/docs/reference/engine/datatypes/Secret)

Parameters

|  |
| --- |
| prefix:[string](/docs/luau/strings) |

Returns

[Secret](/docs/reference/engine/datatypes/Secret)

Returns a secret formed by concatenating the supplied string to the secret
content, for example prepending "Bearer" to the API key.

```
local HttpService = game:GetService("HttpService")



local secret = HttpService:GetSecret("yelp")



local authHeader = secret:AddPrefix("Bearer ")
```

Provide feedback

---

AddSuffix

Appends a string to the secret content.

Secret:AddSuffix(suffix:[string](/docs/luau/strings)):[Secret](/docs/reference/engine/datatypes/Secret)

Parameters

|  |
| --- |
| suffix:[string](/docs/luau/strings) |

Returns

[Secret](/docs/reference/engine/datatypes/Secret)

Returns a secret formed by concatenating the original secret and the
supplied string parameter. Useful when creating a URL containing a key and
query parameters.

```
local HttpService = game:GetService("HttpService")



local googleMapsApiKey = HttpService:GetSecret("google_map")



local baseUrl = "https://maps.googleapis.com/maps/api/distancematrix/json?key="



local queryParams = "&destinations=" .. destination .. "&origins=" .. origin .. "&departure_time=now&units=imperial"



local authedUrl = googleMapsApiKey:AddPrefix(baseUrl)



local queryUrl = authedUrl:AddSuffix(queryParams)
```

Provide feedback

---