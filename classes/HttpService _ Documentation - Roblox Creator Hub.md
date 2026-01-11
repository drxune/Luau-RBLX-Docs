# HttpService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/HttpService
Scraped: 2026-01-11T02:30:23.492298Z

## Tags
- Not Creatable
- Service

## Inherits
- Object
- Instance
- HttpService
- WebStreamClient
- RequestAsync
- GetAsync
- PostAsync
- JSONEncode
- JSONDecode
- GenerateGUID
- CreateWebStreamClient()
- HttpService:GetSecret("API KEY SECRET NAME")
- HttpService:GetAsync()
- HttpService:PostAsync()
- HttpService:RequestAsync()
- WebStreamClient:Close()
- RequestAsync()
- HttpService:JSONEncode()
- HttpService:JSONDecode()
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [HttpService](/docs/reference/engine/classes/HttpService)

English

Feedback

Engine Class

HttpService

Allows sending HTTP requests and provides various web-related and JSON
methods.

Not Creatable

Service

---

Summary

Properties

|  |
| --- |
| [HttpEnabled](#HttpEnabled):[boolean](/docs/luau/booleans) |

Methods

|  |
| --- |
| [CreateWebStreamClient](#CreateWebStreamClient)(streamClientType: [Enum.WebStreamClientType](/docs/reference/engine/enums/WebStreamClientType),requestOptions: [Dictionary](/docs/luau/tables#dictionaries)):[WebStreamClient](/docs/reference/engine/classes/WebStreamClient) |
| [GenerateGUID](#GenerateGUID)(wrapInCurlyBraces: [boolean](/docs/luau/booleans)):[string](/docs/luau/strings) |
| [GetAsync](#GetAsync)(url: Variant,nocache: [boolean](/docs/luau/booleans),headers: Variant):[string](/docs/luau/strings) |
| [GetSecret](#GetSecret)(key: [string](/docs/luau/strings)):[Secret](/docs/reference/engine/datatypes/Secret) |
| [JSONDecode](#JSONDecode)(input: [string](/docs/luau/strings)):Variant |
| [JSONEncode](#JSONEncode)(input: Variant):[string](/docs/luau/strings) |
| [PostAsync](#PostAsync)(url: Variant,data: [string](/docs/luau/strings),content\_type: [Enum.HttpContentType](/docs/reference/engine/enums/HttpContentType),compress: [boolean](/docs/luau/booleans),headers: Variant):[string](/docs/luau/strings) |
| [RequestAsync](#RequestAsync)(requestOptions: [Dictionary](/docs/luau/tables#dictionaries)):[Dictionary](/docs/luau/tables#dictionaries) |
| [UrlEncode](#UrlEncode)(input: [string](/docs/luau/strings)):[string](/docs/luau/strings) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

HttpService allows HTTP requests to be sent from game servers using
[RequestAsync](/docs/reference/engine/classes/HttpService#RequestAsync),
[GetAsync](/docs/reference/engine/classes/HttpService#GetAsync) and
[PostAsync](/docs/reference/engine/classes/HttpService#PostAsync). This service allows games to be
integrated with third-party web services such as analytics, data storage,
remote server configuration, error reporting, advanced calculations, or
real-time communication. Additionally, it can call a subset of the Open Cloud
APIs.

For more information about these use cases, see
[In-experience HTTP requests](/docs/cloud-services/http-service).

HttpService also houses the [JSONEncode](/docs/reference/engine/classes/HttpService#JSONEncode) and
[JSONDecode](/docs/reference/engine/classes/HttpService#JSONDecode) methods, which are useful for
communicating with services that use the [JSON](https://json.org) format. In
addition, the [GenerateGUID](/docs/reference/engine/classes/HttpService#GenerateGUID) method provides
random 128‑bit labels which can be treated as probabilistically unique in a
variety of scenarios.

Within Studio, use
[CreateWebStreamClient()](/docs/reference/engine/classes/HttpService#CreateWebStreamClient) to process
data in real time from servers that support streaming protocols such as
[SSE](https://en.wikipedia.org/wiki/Server-sent_events),
[chunked transfer encoding](https://en.wikipedia.org/wiki/Chunked_transfer_encoding),
and [WebSockets](https://en.wikipedia.org/wiki/WebSocket). You can connect
callback functions to stream events, allowing you to process data immediately
as it arrives instead of waiting for the entire response to complete.

Only send HTTP requests to trusted third-party platforms to avoid introducing
unnecessary security risks to your experience.

Code Samples

Astronauts in Space

This code sample uses HttpService's GetAsync to make a request to
[Open Notify](http://open-notify.org), a web service that provides data from
NASA. The request is made to an endpoint that provides information on how many
astronauts are currently in space. The response is provided in JSON format, so
it is parsed using JSONDecode. Finally, the response data is then processed
and printed to the Output.

Test this script by pasting the source code into a Script (HttpService cannot
be used by LocalScripts). Also, be sure to enable HTTP Requests in your Game
Settings (Home > Game Settings).

```
local HttpService = game:GetService("HttpService")



local URL_ASTROS = "http://api.open-notify.org/astros.json"



-- Make the request to our endpoint URL



local response = HttpService:GetAsync(URL_ASTROS)



-- Parse the JSON response



local data = HttpService:JSONDecode(response)



-- Information in the data table is dependent on the response JSON



if data.message == "success" then



print("There are currently " .. data.number .. " astronauts in space:")



for i, person in pairs(data.people) do



print(i .. ": " .. person.name .. " is on " .. person.craft)



end



end
```

Where is the International Space Station?

This code sample uses HttpService's GetAsync to make a request to an endpoint
at [Open Notify](http://open-notify.org/Open-Notify-API/ISS-Location-Now/), a
website that provides information from NASA. The endpoint provides information
on the current location of the International Space Station. This example uses
a defensive coding technique that you should use when making web requests.
It wraps the call to GetAsync and JSONDecode in pcall, which protects our
script from raising an error if either of these fail. Then, it checks the raw
response for all proper data before using it. All of this is put inside a
function that returns true or false depending of the request's success.

Whenever you're working with web requests, you should prepare for anything to
go wrong. Perhaps your web endpoint changes or goes down - you don't want your
game scripts raising errors and breaking your game. You want to handle both
success and failure gracefully - have a plan in case your data is not
available. Use pcall and make plenty of validity checks (if statements) on
your data to make sure you're getting exactly what you expect.

```
local HttpService = game:GetService("HttpService")



-- Where is the International Space Station right now?



local URL_ISS = "http://api.open-notify.org/iss-now.json"



local function printISS()



local response



local data



-- Use pcall in case something goes wrong



pcall(function()



response = HttpService:GetAsync(URL_ISS)



data = HttpService:JSONDecode(response)



end)



-- Did our request fail or our JSON fail to parse?



if not data then



return false



end



-- Fully check our data for validity. This is dependent on what endpoint you're



-- to which you're sending your requests. For this example, this endpoint is



-- described here:  http://open-notify.org/Open-Notify-API/ISS-Location-Now/



if data.message == "success" and data.iss_position then



if data.iss_position.latitude and data.iss_position.longitude then



print("The International Space Station is currently at:")



print(data.iss_position.latitude .. ", " .. data.iss_position.longitude)



return true



end



end



return false



end



if printISS() then



print("Success")



else



print("Something went wrong")



end
```

New Pastebin Post

Pastebin.com is a website that allows users to paste text (usually source
code) for others to view publicly. This code sample uses HttpService PostAsync
and the pastebin web API to automatically create a new public paste on the
website. Since pastebin's API is designed to take data in as a URL encoded
string, the code uses a for-loop to turn the dataFields table into a URL
encoded string, such as hello=world&foo=bar. This is used as the HTTP POST
data.

Test this code by first going to
[pastebin.com/api#1](https://pastebin.com/api#1) and getting an API key
(you'll need a pastebin account to do this). Then, paste your unique developer
API key into the field api\_dev\_key in the code sample's dataFields table.
Fill in any other information about the post you want to make, then run this
code in a Script (not a LocalScript). If all goes well, you'll get a URL to
your new paste in the Output window (or some error string from pastebin).

```
local HttpService = game:GetService("HttpService")



local URL_PASTEBIN_NEW_PASTE = "https://pastebin.com/api/api_post.php"



local dataFields = {



-- Pastebin API developer key from



-- https://pastebin.com/api#1



["api_dev_key"] = "FILL THIS WITH YOUR API DEVELOPER KEY",



["api_option"] = "paste", -- keep as "paste"



["api_paste_name"] = "HttpService:PostAsync", -- paste name



["api_paste_code"] = "Hello, world", -- paste content



["api_paste_format"] = "text", -- paste format



["api_paste_expire_date"] = "10M", -- expire date



["api_paste_private"] = "0", -- 0=public, 1=unlisted, 2=private



["api_user_key"] = "", -- user key, if blank post as guest



}



-- The pastebin API uses a URL encoded string for post data



-- Other APIs might use JSON, XML or some other format



local data = ""



for k, v in pairs(dataFields) do



data = data .. ("&%s=%s"):format(HttpService:UrlEncode(k), HttpService:UrlEncode(v))



end



data = data:sub(2) -- Remove the first &



-- Here's the data we're sending



print(data)



-- Make the request



local response = HttpService:PostAsync(URL_PASTEBIN_NEW_PASTE, data, Enum.HttpContentType.ApplicationUrlEncoded, false)



-- The response will be the URL to the new paste (or an error string if something was wrong)



print(response)
```

Open Cloud via HttpService

This code sample demonstrates sending a single HTTP PATCH request with JSON
data to the [Open Cloud Update Group Membership](/docs/cloud/reference/GroupMembership#Cloud_UpdateGroupMembership) endpoint.
Every Open Cloud endpoint requires adding your [API key](/docs/cloud/auth/api-keys#create-api-keys)
to the x-api-key header to receive a successful response. The generated API
key must be stored as a [Secret](/docs/reference/engine/datatypes/Secret) that can later be retrieved with
[HttpService:GetSecret("API KEY SECRET NAME")](/docs/reference/engine/classes/HttpService#GetSecret).

```
-- Remember to set enable HTTP Requests in game settings!



local HttpService = game:GetService("HttpService")



local groupId = "your_group_id"



local membershipId = "your_membership_id"



local roleId = "your_role_id"



local function request()



local response = HttpService:RequestAsync({



Url = `https://apis.roblox.com/cloud/v2/groups/{groupId}/memberships/{membershipId}`, -- Updates a user's group membership



Method = "PATCH",



Headers = {



["Content-Type"] = "application/json", -- When sending JSON, set this!



["x-api-key"] = HttpService:GetSecret("APIKey"), -- Set in Creator Hub



},



Body = HttpService:JSONEncode({ role = `groups/{groupId}/roles/{roleId}` }),



})



if response.Success then



print("The response was successful:", response.StatusCode, response.StatusMessage)



else



print("The response returned an error:", response.StatusCode, response.StatusMessage)



end



print("Response body:\n", response.Body)



print("Response headers:\n", HttpService:JSONEncode(response.Headers))



end



-- Remember to wrap the function in a 'pcall' to prevent the script from breaking if the request fails



local success, message = pcall(request)



if not success then



print("The Http request failed to send:", message)



end
```

---

API Reference

Properties

HttpEnabled

Local User Security

Read Parallel

Indicates whether HTTP requests can be sent to external websites.

HttpService.HttpEnabled:[boolean](/docs/luau/booleans)

When set to true, allows scripts to send requests to websites using
[HttpService:GetAsync()](/docs/reference/engine/classes/HttpService#GetAsync), [HttpService:PostAsync()](/docs/reference/engine/classes/HttpService#PostAsync), and
[HttpService:RequestAsync()](/docs/reference/engine/classes/HttpService#RequestAsync).

This property must be toggled on through the
[Game Settings](/docs/studio/game-settings) interface in Studio, or
for unpublished experiences by setting this property to true using
the [Command Bar](/docs/studio/ui-overview#command-bar):

game:GetService("HttpService").HttpEnabled = true

Provide feedback

---

Methods

CreateWebStreamClient

Creates a client that opens a persistent connection to stream data.

HttpService:CreateWebStreamClient(

streamClientType:[Enum.WebStreamClientType](/docs/reference/engine/enums/WebStreamClientType), requestOptions:[Dictionary](/docs/luau/tables#dictionaries)

):[WebStreamClient](/docs/reference/engine/classes/WebStreamClient)

Parameters

|  |
| --- |
| streamClientType:[Enum.WebStreamClientType](/docs/reference/engine/enums/WebStreamClientType)  The type of streaming connection to intiialize the client with. |
| requestOptions:[Dictionary](/docs/luau/tables#dictionaries)  A dictionary containing information to be requested from the server. It is identical to requestOptions in [HttpService:RequestAsync()](/docs/reference/engine/classes/HttpService#RequestAsync). |

Returns

[WebStreamClient](/docs/reference/engine/classes/WebStreamClient)

A stateful client that emits events in the stream lifecycle.

This method creates a client that establishes a long-lived connection to
servers utilizing various streaming technologies, such as
[Server-Sent Events (SSE)](https://developer.mozilla.org/en-US/docs/Web/API/Server-sent_events/Using_server-sent_events).
After the connection is established, the client fires signals that you can
connect callback functions to with [RBXScriptConnection](/docs/reference/engine/datatypes/RBXScriptConnection). Use
these callbacks to process messages as soon as they arrive, as well as
respond to open, close, and error events.

There is a limit of six total clients allowed at one time. Close streams
that you no longer need with [WebStreamClient:Close()](/docs/reference/engine/classes/WebStreamClient#Close). When the
stream is no longer needed, you should disconnect any associated
[RBXScriptConnections](/docs/reference/engine/datatypes/RBXScriptConnection) to avoid memory leaks.

This method is available in Studio only. If you use it inside scripts,
make sure to remove any references before publishing the experience. We
encourage you to create plugins with this feature for reusability and ease
of use.

Code Samples

HttpService CreateWebStreamClient SSE

This code sample uses CreateWebStreamClient to create a SSE client
and connects a function to each event that the client fires, allowing the client to process
messages from the Google Gemini API as they arrive.

```
local HttpService = game:GetService("HttpService")



local URL_GEMINI_SSE = "https://generativelanguage.googleapis.com/v1beta/models/gemini-2.0-flash:streamGenerateContent?alt=sse&key="



local geminiSecret = HttpService:GetSecret("gemini_secret") -- Assumes you have already uploaded your Gemini API key as a local secret



local url_with_secret = geminiSecret:AddPrefix(URL_GEMINI_SSE) -- Remember that plugins can't access local secrets!



local function handleOpen(responseStatusCode, headers)



print("Stream opened with response code:", responseStatusCode)



end



local function handleMessage(message)



-- Parse events depending on the stream type



print("Stream message received:", message)



end



local function request()



local sse_client = HttpService:CreateWebStreamClient(Enum.WebStreamClientType.RawStream, {



Url = url_with_secret,



Method = "POST",



Headers = {



["Content-Type"] = "application/json", -- When sending JSON, set this!



},



Body = HttpService:JSONEncode({ contents = { parts = { text ="How does the SSE protocol work?" }}}),



})



local openConnection = sse_client.Opened:Connect(handleOpen)



local messageConnection = sse_client.MessageReceived:Connect(handleMessage)



sse_client.Closed:Wait()



openConnection:Disconnect()



messageConnection:Disconnect()



end



-- Remember to wrap the function in a 'pcall' to prevent the script from breaking if the request fails



local success, message = pcall(request)



if not success then



print("WebStreamClient failed:", message)



end
```

HttpService CreateWebStreamClient RawStream

This code sample uses CreateWebStreamClient() to create a RawStream client
and connects a function to each event that the client fires, allowing the client to process
messages from the locally running Llama 3.3 LLM server as they arrive.

```
local HttpService = game:GetService("HttpService")



local LOCAL_LLM_PORT = "http://localhost:11434/api/generate?stream=true"



local function handleMessage(message)



-- Parse events depending on the stream type



-- If response Content-Type header is JSON, you can decode it like this:



local json = HttpService:JSONDecode(message)



end



local function handleError(responseStatusCode, errorMessage)



print("Stream error with response code:", responseStatusCode)



end



local function request()



local sse_client = HttpService:CreateWebStreamClient(Enum.WebStreamClientType.RawStream, {



-- Llama3.2 LLM server running locally using Ollama



Url = LOCAL_LLM_PORT,



Method = "POST",



Headers = {



["Content-Type"] = "application/json", -- When sending JSON, set this!



},



Body = HttpService:JSONEncode({ model="llama3.2", prompt ="Tell me a funny joke"}),



})



local messageConnection = sse_client.MessageReceived:Connect(handleMessage)



local errorConnection = sse_client.Error:Connect(handleError)



sse_client.Closed:Wait()



messageConnection:Disconnect()



errorConnection:Disconnect()



sse_client:close()



end



-- Remember to wrap the function in a 'pcall' to prevent the script from breaking if the request fails



local success, message = pcall(request)



if not success then



print("WebStreamClient failed:", message)



end
```

Provide feedback

---

GenerateGUID

Write Parallel

Generates a UUID/GUID random string, optionally with curly braces.

HttpService:GenerateGUID(wrapInCurlyBraces:[boolean](/docs/luau/booleans)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| wrapInCurlyBraces:[boolean](/docs/luau/booleans) Default Value: true Whether the returned string should be wrapped in curly braces ({}). |

Returns

[string](/docs/luau/strings)

The randomly generated UUID.

This method generates a random universally unique identifier
([UUID](https://en.wikipedia.org/wiki/Universally_unique_identifier))
string. The sixteen octets of a UUID are represented as 32 hexadecimal
(base 16) digits, displayed in five groups separated by hyphens in
the form 8-4-4-4-12 for a total of 36 characters, for example
123e4567-e89b-12d3-a456-426655440000.

The UUID specification used is
[Version 4 (random)](https://en.wikipedia.org/wiki/Universally_unique_identifier#Version_4_(random)),
variant 1 (DCE 1.1, ISO/IEC 11578:1996). UUIDs of this version are the
most commonly used due to their simplicity, as they are entirely randomly
generated. Note that this version does not have certain features that
other UUID versions have, such as encoded timestamps, MAC addresses, or
time-based sorting like [UUIDv7](https://uuid7.com/) or
[ULID](https://github.com/ulid/spec).

There are over 5.3×1036 unique v4 UUIDs, in which the
probability of finding a duplicate within 103 trillion UUIDs is one in a
billion.

The wrapInCurlyBraces argument determines whether the returned string is
wrapped in curly braces ({}). For instance:

* true: {94b717b2-d54f-4340-a504-bd809ef5bf5c}
* false: db454790-7563-44ed-ab4b-397ff5df737b

Code Samples

HttpService GenerateGUID

This example uses HttpService's GenerateGUID method to generate and print a
universally unique identifier.

```
local HttpService = game:GetService("HttpService")



local result = HttpService:GenerateGUID(true)



print(result) --> Example output: {4c50eba2-d2ed-4d79-bec1-02a967f49c58}
```

Provide feedback

---

GetAsync

Yields

Sends an HTTP GET request.

HttpService:GetAsync(

url:Variant, nocache:[boolean](/docs/luau/booleans), headers:Variant

):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| url:Variant  The web address you are requesting data from. |
| nocache:[boolean](/docs/luau/booleans) Default Value: false Whether the request stores (caches) the response. |
| headers:Variant  Used to specify some HTTP request headers. |

Returns

[string](/docs/luau/strings)

The GET request's response body.

This method sends an HTTP GET request. It functions similarly to
[RequestAsync()](/docs/reference/engine/classes/HttpService#RequestAsync) except that it accepts
HTTP request parameters as method parameters instead of a single
dictionary and returns only the body of the HTTP response. Generally, this
method is useful only as a shorthand and
[RequestAsync()](/docs/reference/engine/classes/HttpService#RequestAsync) should be used in most
cases.

When true, the nocache parameter prevents this method from caching
results from previous calls with the same url.

Code Samples

Astronauts in Space

This code sample uses HttpService's GetAsync to make a request to
[Open Notify](http://open-notify.org), a web service that provides data from
NASA. The request is made to an endpoint that provides information on how many
astronauts are currently in space. The response is provided in JSON format, so
it is parsed using JSONDecode. Finally, the response data is then processed
and printed to the Output.

Test this script by pasting the source code into a Script (HttpService cannot
be used by LocalScripts). Also, be sure to enable HTTP Requests in your Game
Settings (Home > Game Settings).

```
local HttpService = game:GetService("HttpService")



local URL_ASTROS = "http://api.open-notify.org/astros.json"



-- Make the request to our endpoint URL



local response = HttpService:GetAsync(URL_ASTROS)



-- Parse the JSON response



local data = HttpService:JSONDecode(response)



-- Information in the data table is dependent on the response JSON



if data.message == "success" then



print("There are currently " .. data.number .. " astronauts in space:")



for i, person in pairs(data.people) do



print(i .. ": " .. person.name .. " is on " .. person.craft)



end



end
```

Where is the International Space Station?

This code sample uses HttpService's GetAsync to make a request to an endpoint
at [Open Notify](http://open-notify.org/Open-Notify-API/ISS-Location-Now/), a
website that provides information from NASA. The endpoint provides information
on the current location of the International Space Station. This example uses
a defensive coding technique that you should use when making web requests.
It wraps the call to GetAsync and JSONDecode in pcall, which protects our
script from raising an error if either of these fail. Then, it checks the raw
response for all proper data before using it. All of this is put inside a
function that returns true or false depending of the request's success.

Whenever you're working with web requests, you should prepare for anything to
go wrong. Perhaps your web endpoint changes or goes down - you don't want your
game scripts raising errors and breaking your game. You want to handle both
success and failure gracefully - have a plan in case your data is not
available. Use pcall and make plenty of validity checks (if statements) on
your data to make sure you're getting exactly what you expect.

```
local HttpService = game:GetService("HttpService")



-- Where is the International Space Station right now?



local URL_ISS = "http://api.open-notify.org/iss-now.json"



local function printISS()



local response



local data



-- Use pcall in case something goes wrong



pcall(function()



response = HttpService:GetAsync(URL_ISS)



data = HttpService:JSONDecode(response)



end)



-- Did our request fail or our JSON fail to parse?



if not data then



return false



end



-- Fully check our data for validity. This is dependent on what endpoint you're



-- to which you're sending your requests. For this example, this endpoint is



-- described here:  http://open-notify.org/Open-Notify-API/ISS-Location-Now/



if data.message == "success" and data.iss_position then



if data.iss_position.latitude and data.iss_position.longitude then



print("The International Space Station is currently at:")



print(data.iss_position.latitude .. ", " .. data.iss_position.longitude)



return true



end



end



return false



end



if printISS() then



print("Success")



else



print("Something went wrong")



end
```

Provide feedback

---

GetSecret

Write Parallel

Returns a [Secret](/docs/reference/engine/datatypes/Secret) from the secrets store.

HttpService:GetSecret(key:[string](/docs/luau/strings)):[Secret](/docs/reference/engine/datatypes/Secret)

Parameters

|  |
| --- |
| key:[string](/docs/luau/strings) |

Returns

[Secret](/docs/reference/engine/datatypes/Secret)

This method returns a value previously added to the secrets store for the
experience. The secret content is not printable and not available when the
experience runs locally.

The returned [Secret](/docs/reference/engine/datatypes/Secret) can be transformed using built-in methods
such as [Secret:AddPrefix()](/docs/reference/engine/datatypes/Secret#AddPrefix). It is expected to be sent as a part
of an HTTP request.

For more information, see the
[usage guide](/docs/cloud-services/secrets).

Provide feedback

---

JSONDecode

Write Parallel

Decodes a JSON string into a Luau table.

HttpService:JSONDecode(input:[string](/docs/luau/strings)):Variant

Parameters

|  |
| --- |
| input:[string](/docs/luau/strings)  The JSON object being decoded. |

Returns

Variant

The decoded JSON object as a Luau table.

This method transforms a JSON object or array into a Luau
[table](/docs/luau/tables) with the following characteristics:

* Keys of the table are strings or numbers but not both. If a JSON object
  contains both, string keys are ignored.
* An empty JSON object generates an empty Luau table ({}).
* If the input string is not a valid JSON object, this method will throw
  an error.

To encode a Luau table into a JSON object, use the
[HttpService:JSONEncode()](/docs/reference/engine/classes/HttpService#JSONEncode) method.

This method can be used regardless of whether HTTP requests are enabled.

Code Samples

HttpService JSONDecode

This code sample gives an example [JSON](https://www.json.org/) format string
and parses it using HttpService's JSONDecode. It then verifies that the JSON
was parsed correctly, and prints out some of the information within the
object.

Try editing the JSON string to experiment with the format. Also experiment
with inspecting the data in Lua to get comfortable with the Lua representation
of the data (tables and other values).

```
local HttpService = game:GetService("HttpService")



local jsonString = [[



{



"message": "success",



"info": {



"points": 120,



"isLeader": true,



"user": {



"id": 12345,



"name": "JohnDoe"



},



"past_scores": [50, 42, 95],



"best_friend": null



}



}



]]



local data = HttpService:JSONDecode(jsonString)



if data.message == "success" then



-- Since tab["hello"] and tab.hello are equivalent,



-- you could also use data["info"]["points"] here:



print("I have " .. data.info.points .. " points")



if data.info.isLeader then



print("I am the leader")



end



print("I have " .. #data.info.past_scores .. " past scores")



print("All the information:")



for key, value in pairs(data.info) do



print(key, typeof(value), value)



end



end
```

Provide feedback

---

JSONEncode

Write Parallel

Generate a JSON string from a Luau table.

HttpService:JSONEncode(input:Variant):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| input:Variant  The input Luau table. |

Returns

[string](/docs/luau/strings)

The returned JSON string.

This method transforms a Luau [table](/docs/luau/tables) into a JSON
object or array based on the following guidelines:

* Keys of the table must be either strings or numbers. If a table contains
  both, an array takes priority (string keys are ignored).
* An empty Luau table ({}) generates an empty JSON array (e.g. []).
* The value nil is never generated.
* Cyclic table references cause an error.

This method allows values such as inf and nan which are not valid
JSON. This may cause problems if you want to use the outputted JSON
elsewhere.

This method also accepts [buffers](/docs/reference/engine/libraries/buffer), which it encodes to
base64 (and often compresses) before converting to a JSON object.

To reverse the encoding process and decode a JSON object, use the
[HttpService:JSONDecode()](/docs/reference/engine/classes/HttpService#JSONDecode) method.

This method can be used regardless of whether HTTP requests are enabled.

Code Samples

HttpService JSONEncode

This code sample turns a Lua table tab into a
[JSON string](https://www.json.org/) using HttpService's JSONEncode. Then, it
prints out the string.

Try editing the Lua table to see how the JSON output changes.

```
local HttpService = game:GetService("HttpService")



local tab = {



-- Remember: these lines are equivalent



--["message"] = "success",



message = "success",



info = {



points = 123,



isLeader = true,



user = {



id = 12345,



name = "JohnDoe",



},



past_scores = { 50, 42, 95 },



best_friend = nil,



},



}



local json = HttpService:JSONEncode(tab)



print(json)
```

Provide feedback

---

PostAsync

Yields

Sends an HTTP POST request.

HttpService:PostAsync(

url:Variant, data:[string](/docs/luau/strings), content\_type:[Enum.HttpContentType](/docs/reference/engine/enums/HttpContentType), compress:[boolean](/docs/luau/booleans), headers:Variant

):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| url:Variant  The destination address for the data. |
| data:[string](/docs/luau/strings)  The data being sent. |
| content\_type:[Enum.HttpContentType](/docs/reference/engine/enums/HttpContentType) Default Value: "ApplicationJson" Modifies the value in the Content-Type header sent with the request. |
| compress:[boolean](/docs/luau/booleans) Default Value: false Determines whether the data is compressed (gzipped) when sent. |
| headers:Variant  Used to specify some HTTP request headers. |

Returns

[string](/docs/luau/strings)

The HTTP response sent back indicating the request result.

This method sends an HTTP POST request. It functions similarly to
[RequestAsync()](/docs/reference/engine/classes/HttpService#RequestAsync) except that it accepts
HTTP request parameters as method parameters instead of a single
dictionary and returns only the body of the HTTP response. Generally, this
method is useful only as a shorthand and
[RequestAsync()](/docs/reference/engine/classes/HttpService#RequestAsync) should be used in most
cases.

When true, the compress parameter controls whether large request
bodies will be compressed using gzip.

Code Samples

New Pastebin Post

Pastebin.com is a website that allows users to paste text (usually source
code) for others to view publicly. This code sample uses HttpService PostAsync
and the pastebin web API to automatically create a new public paste on the
website. Since pastebin's API is designed to take data in as a URL encoded
string, the code uses a for-loop to turn the dataFields table into a URL
encoded string, such as hello=world&foo=bar. This is used as the HTTP POST
data.

Test this code by first going to
[pastebin.com/api#1](https://pastebin.com/api#1) and getting an API key
(you'll need a pastebin account to do this). Then, paste your unique developer
API key into the field api\_dev\_key in the code sample's dataFields table.
Fill in any other information about the post you want to make, then run this
code in a Script (not a LocalScript). If all goes well, you'll get a URL to
your new paste in the Output window (or some error string from pastebin).

```
local HttpService = game:GetService("HttpService")



local URL_PASTEBIN_NEW_PASTE = "https://pastebin.com/api/api_post.php"



local dataFields = {



-- Pastebin API developer key from



-- https://pastebin.com/api#1



["api_dev_key"] = "FILL THIS WITH YOUR API DEVELOPER KEY",



["api_option"] = "paste", -- keep as "paste"



["api_paste_name"] = "HttpService:PostAsync", -- paste name



["api_paste_code"] = "Hello, world", -- paste content



["api_paste_format"] = "text", -- paste format



["api_paste_expire_date"] = "10M", -- expire date



["api_paste_private"] = "0", -- 0=public, 1=unlisted, 2=private



["api_user_key"] = "", -- user key, if blank post as guest



}



-- The pastebin API uses a URL encoded string for post data



-- Other APIs might use JSON, XML or some other format



local data = ""



for k, v in pairs(dataFields) do



data = data .. ("&%s=%s"):format(HttpService:UrlEncode(k), HttpService:UrlEncode(v))



end



data = data:sub(2) -- Remove the first &



-- Here's the data we're sending



print(data)



-- Make the request



local response = HttpService:PostAsync(URL_PASTEBIN_NEW_PASTE, data, Enum.HttpContentType.ApplicationUrlEncoded, false)



-- The response will be the URL to the new paste (or an error string if something was wrong)



print(response)
```

Provide feedback

---

RequestAsync

Yields

Sends an HTTP request using any HTTP method given a dictionary of
information.

HttpService:RequestAsync(requestOptions:[Dictionary](/docs/luau/tables#dictionaries)):[Dictionary](/docs/luau/tables#dictionaries)

Parameters

|  |
| --- |
| requestOptions:[Dictionary](/docs/luau/tables#dictionaries)  A dictionary containing information to be requested from the server specified. |

Returns

[Dictionary](/docs/luau/tables#dictionaries)

A dictionary containing response information from the server
specified.

This method sends an HTTP request using a dictionary to specify the
request data, such as the target URL, method, headers, and request body
data. It returns a dictionary that describes the response data received.
Optionally, the request can be compressed using [Enum.HttpCompression](/docs/reference/engine/enums/HttpCompression).

##### Request dictionary fields

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| Url | String | yes | The target URL for this request. Must use http or https protocols. |
| Method | String | no | The HTTP method being used by this request, most often GET or POST. |
| Headers | Dictionary | no | A dictionary of headers to be used with this request. Most HTTP headers are accepted here, but not all. |
| Body | String | no | The request body. Can be any string, including binary data. Must be excluded when using the GET or HEAD HTTP methods. It might be necessary to specify the Content-Type header when sending JSON or other formats. |
| Compress | [Enum.HttpCompression](/docs/reference/engine/enums/HttpCompression) | no | An optional compression field that will compress the data in the request. The value can either be [Enum.HttpCompression.None](/docs/reference/engine/enums/HttpCompression#None) or [Enum.HttpCompression.Gzip](/docs/reference/engine/enums/HttpCompression#Gzip). |

##### Supported HTTP methods

The HTTP request methods specify the purpose of the request being made and
what is expected if the request is successful. For instance, the GET
request method tells the server at the requested address that a resource
is being requested and, if it succeeds, the resource at that address will
be returned. Similarly, the HEAD request method does the same except the
server knows to return a response without a Body element.

| Method | Description | Safe |
| --- | --- | --- |
| GET  [ⓘ](https://developer.mozilla.org/docs/Web/HTTP/Methods/GET) | The GET method requests the resource at the specified address. Does not support use of the Body parameter. | Yes |
| HEAD  [ⓘ](https://developer.mozilla.org/docs/Web/HTTP/Methods/HEAD) | The HEAD method requests a response identical to a GET request, but with no response body. Does not support use of the Body parameter. | Yes |
| POST  [ⓘ](https://developer.mozilla.org/docs/Web/HTTP/Methods/POST) | The POST method submits the supplied Body data to the requested address. | No |
| PUT  [ⓘ](https://developer.mozilla.org/docs/Web/HTTP/Methods/PUT) | The PUT method replaces all current iterations of the resource specified within the supplied Body data. | No |
| DELETE  [ⓘ](https://developer.mozilla.org/docs/Web/HTTP/Methods/DELETE) | The DELETE method deletes the resource specified in the supplied Body data at the requested address. | No |
| OPTIONS  [ⓘ](https://developer.mozilla.org/docs/Web/HTTP/Methods/OPTIONS) | The OPTIONS method requests the permitted communication options for the supplied address. | Yes |
| TRACE  [ⓘ](https://developer.mozilla.org/docs/Web/HTTP/Methods/TRACE) | The TRACE method performs a message loop-back test along the path to the resource specified in the supplied Body data. | Yes |
| PATCH  [ⓘ](https://developer.mozilla.org/docs/Web/HTTP/Methods/PATCH) | The PATCH method applies partial changes to the resource specified in the supplied Body data at the requested address. | No |

##### HTTP headers

In the request dictionary, you can specify custom HTTP headers to use in
the request. However, some headers cannot be specified. For example,
Content-Length is determined from the request body. User-Agent and
Roblox-Id are locked by Roblox. Other headers like Accept or
Cache-Control use default values but can be overridden. More commonly,
some REST APIs may require API keys or other service authentication to be
specified in request headers.

The RequestAsync() method does not detect the format of body content.
Many web servers require the Content-Type header be set appropriately
when sending certain formats. Other methods of [HttpService](/docs/reference/engine/classes/HttpService) use the
[Enum.HttpContentType](/docs/reference/engine/enums/HttpContentType) enum; for this method set the Content-Type header
appropriately: text/plain, text/xml, application/xml,
application/json or application/x-www-form-urlencoded are replacement
Content-Type header values for the respective enum values.

##### Response dictionary fields

RequestAsync() returns a dictionary containing the following fields:

| Name | Type | Description |
| --- | --- | --- |
| Success | Boolean | The success status of the request. This is true if and only if the StatusCode lies within the range 200-299. |
| StatusCode | Integer | The HTTP response code identifying the status of the response. |
| StatusMessage | String | The status message that was sent back. |
| Headers | Dictionary | A dictionary of headers that were set in this response. |
| Body |  | The request body (content) received in the response. |

##### Error Cases

RequestAsync() raises an error if the response times out or if the
target server rejects the request. If a web service goes down for some
reason, it can cause scripts that use this method to stop functioning
altogether. It is often a good idea to wrap calls to this method in
[pcall()](/docs/reference/engine/globals/LuaGlobals#pcall) and gracefully handle failure cases if the
required information isn't available.

##### Limitations

The current limitation for sending and receiving external HTTP
requests is 500 requests per minute. There is also a separate limit of
2500 requests per minute for
[Open Cloud requests](/docs/cloud-services/http-service#use-with-open-cloud).
Requests over these thresholds will fail.

Code Samples

Sending an HTTP Request

This code sample demonstrates sending a single HTTP POST request with JSON
data to the website httpbin.org, a website that helps debug HTTP requests.
Here, we send some JSON data by using [HttpService:JSONEncode()](/docs/reference/engine/classes/HttpService#JSONEncode) and
also setting the Content-Type header.

```
-- Remember to set enable HTTP Requests in game settings!



local HttpService = game:GetService("HttpService")



local function request()



local response = HttpService:RequestAsync({



Url = "http://httpbin.org/post", -- This website helps debug HTTP requests



Method = "POST",



Headers = {



["Content-Type"] = "application/json", -- When sending JSON, set this!



},



Body = HttpService:JSONEncode({ hello = "world" }),



})



if response.Success then



print("Status code:", response.StatusCode, response.StatusMessage)



print("Response body:\n", response.Body)



else



print("The request failed:", response.StatusCode, response.StatusMessage)



end



end



-- Remember to wrap the function in a 'pcall' to prevent the script from breaking if the request fails



local success, message = pcall(request)



if not success then



print("Http Request failed:", message)



end
```

Open Cloud via HttpService

This code sample demonstrates sending a single HTTP PATCH request with JSON
data to the [Open Cloud Update Group Membership](/docs/cloud/reference/GroupMembership#Cloud_UpdateGroupMembership) endpoint.
Every Open Cloud endpoint requires adding your [API key](/docs/cloud/auth/api-keys#create-api-keys)
to the x-api-key header to receive a successful response. The generated API
key must be stored as a [Secret](/docs/reference/engine/datatypes/Secret) that can later be retrieved with
[HttpService:GetSecret("API KEY SECRET NAME")](/docs/reference/engine/classes/HttpService#GetSecret).

```
-- Remember to set enable HTTP Requests in game settings!



local HttpService = game:GetService("HttpService")



local groupId = "your_group_id"



local membershipId = "your_membership_id"



local roleId = "your_role_id"



local function request()



local response = HttpService:RequestAsync({



Url = `https://apis.roblox.com/cloud/v2/groups/{groupId}/memberships/{membershipId}`, -- Updates a user's group membership



Method = "PATCH",



Headers = {



["Content-Type"] = "application/json", -- When sending JSON, set this!



["x-api-key"] = HttpService:GetSecret("APIKey"), -- Set in Creator Hub



},



Body = HttpService:JSONEncode({ role = `groups/{groupId}/roles/{roleId}` }),



})



if response.Success then



print("The response was successful:", response.StatusCode, response.StatusMessage)



else



print("The response returned an error:", response.StatusCode, response.StatusMessage)



end



print("Response body:\n", response.Body)



print("Response headers:\n", HttpService:JSONEncode(response.Headers))



end



-- Remember to wrap the function in a 'pcall' to prevent the script from breaking if the request fails



local success, message = pcall(request)



if not success then



print("The Http request failed to send:", message)



end
```

Provide feedback

---

UrlEncode

Write Parallel

Replaces URL-unsafe characters with '%' and two hexadecimal characters.

HttpService:UrlEncode(input:[string](/docs/luau/strings)):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| input:[string](/docs/luau/strings)  The string (URL) to encode. |

Returns

[string](/docs/luau/strings)

The encoded string.

This method
[percent-encodes](https://en.wikipedia.org/wiki/Percent-encoding) a given
string so that reserved characters properly encoded with % and two
hexadecimal characters.

This is useful when formatting URLs for use with
[HttpService:GetAsync()](/docs/reference/engine/classes/HttpService#GetAsync)/[HttpService:PostAsync()](/docs/reference/engine/classes/HttpService#PostAsync), or POST
data of the media type application/x-www-form-urlencoded
([Enum.HttpContentType.ApplicationUrlEncoded](/docs/reference/engine/enums/HttpContentType)).

For instance, when you encode the URL https://www.roblox.com/discover#/,
this method returns https%3A%2F%2Fwww%2Eroblox%2Ecom%2Fdiscover%23%2F.

Code Samples

HttpService UrlEncode

This code sample uses UrlEncode to turn a string into a safe,
[percent-encoded](https://en.wikipedia.org/wiki/Percent-encoding) string that can be used in a URL as an argument. Notice
how only unreserved characters (letters, numbers and -\_.~) are not
transformed into percent-encoded equivalents. Characters with accents are also
transformed (for example é is transformed into %C3).

```
local HttpService = game:GetService("HttpService")



local content = "Je suis allé au cinéma." -- French for "I went to the movies"



local result = HttpService:UrlEncode(content)



print(result) --> Je%20suis%20all%C3%A9%20au%20cinema%2E
```

New Pastebin Post

Pastebin.com is a website that allows users to paste text (usually source
code) for others to view publicly. This code sample uses HttpService PostAsync
and the pastebin web API to automatically create a new public paste on the
website. Since pastebin's API is designed to take data in as a URL encoded
string, the code uses a for-loop to turn the dataFields table into a URL
encoded string, such as hello=world&foo=bar. This is used as the HTTP POST
data.

Test this code by first going to
[pastebin.com/api#1](https://pastebin.com/api#1) and getting an API key
(you'll need a pastebin account to do this). Then, paste your unique developer
API key into the field api\_dev\_key in the code sample's dataFields table.
Fill in any other information about the post you want to make, then run this
code in a Script (not a LocalScript). If all goes well, you'll get a URL to
your new paste in the Output window (or some error string from pastebin).

```
local HttpService = game:GetService("HttpService")



local URL_PASTEBIN_NEW_PASTE = "https://pastebin.com/api/api_post.php"



local dataFields = {



-- Pastebin API developer key from



-- https://pastebin.com/api#1



["api_dev_key"] = "FILL THIS WITH YOUR API DEVELOPER KEY",



["api_option"] = "paste", -- keep as "paste"



["api_paste_name"] = "HttpService:PostAsync", -- paste name



["api_paste_code"] = "Hello, world", -- paste content



["api_paste_format"] = "text", -- paste format



["api_paste_expire_date"] = "10M", -- expire date



["api_paste_private"] = "0", -- 0=public, 1=unlisted, 2=private



["api_user_key"] = "", -- user key, if blank post as guest



}



-- The pastebin API uses a URL encoded string for post data



-- Other APIs might use JSON, XML or some other format



local data = ""



for k, v in pairs(dataFields) do



data = data .. ("&%s=%s"):format(HttpService:UrlEncode(k), HttpService:UrlEncode(v))



end



data = data:sub(2) -- Remove the first &



-- Here's the data we're sending



print(data)



-- Make the request



local response = HttpService:PostAsync(URL_PASTEBIN_NEW_PASTE, data, Enum.HttpContentType.ApplicationUrlEncoded, false)



-- The response will be the URL to the new paste (or an error string if something was wrong)



print(response)
```

Provide feedback

---