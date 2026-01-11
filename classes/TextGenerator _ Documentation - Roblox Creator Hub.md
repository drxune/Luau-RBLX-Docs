# TextGenerator | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/TextGenerator
Scraped: 2026-01-11T02:37:15.942516Z

## Inherits
- Object
- Instance
- TextGenerator
1. [Classes](/docs/reference/engine/classes)
2. /
3. [Object](/docs/reference/engine/classes/Object)
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [TextGenerator](/docs/reference/engine/classes/TextGenerator)

English

Feedback

Engine Class

TextGenerator

Gives access to a large language model for text generation.

---

Summary

Properties

|  |
| --- |
| [Seed](#Seed):[number](/docs/luau/numbers) |
| [SystemPrompt](#SystemPrompt):[string](/docs/luau/strings) |
| [Temperature](#Temperature):[number](/docs/luau/numbers) |
| [TopP](#TopP):[number](/docs/luau/numbers) |

Methods

|  |
| --- |
| [GenerateTextAsync](#GenerateTextAsync)(request: [Dictionary](/docs/luau/tables#dictionaries)):[Dictionary](/docs/luau/tables#dictionaries) |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

A TextGenerator instance lets you use a large language model (LLM) to
generate text based on a system prompt from you and a user prompt from the
player. The most common use of the API is for creating interactive non-player
characters (NPCs).

For example, in a survival experience, your system prompt for a talking animal
might be
"You are a very busy beaver. You end all statements by mentioning how you need to get back to work on your dam.".
Users could ask the beaver about water in the area, the size of a nearby
forest, predators, etc.

The novelty of LLM responses can help create unique, delightful moments for
players, but using the API effectively requires a bit of creativity and
tuning. System prompts can be very extensive, so don't hesitate to include a
long string with lots of detail.

#### Rate limits

Requests are initially limited to 100 per minute, which scales up based on the
number of concurrent users.

Code Samples

```
local Workspace = game:GetService("Workspace")



local textGenerator = Instance.new("TextGenerator")



textGenerator.Parent = Workspace



textGenerator.SystemPrompt = "You are a helpful NPC in a virtual world."



textGenerator.Temperature = 0.8



textGenerator.TopP = 0.6



textGenerator.Seed = 7



local function getResponse(userInput)



local request = {



UserPrompt = userInput,



MaxTokens = 50



}



local success, response = pcall(function()



return textGenerator:GenerateTextAsync(request)



end)



if success then



if response then



print("Generated Text: " .. response.GeneratedText)



print("Context Token: " .. response.ContextToken)



print("Model: " .. response.Model)



return response



end



else



warn("Text generation failed: " .. tostring(response))



end



return nil



end



getResponse("Tell me something cool.")
```

---

API Reference

Properties

Seed

Read Parallel

Sets a fixed seed for the random number generator, allowing reproducible
responses in cases where the same input parameters are used across
multiple requests.

TextGenerator.Seed:[number](/docs/luau/numbers)

Sets a fixed seed for the random number generator, allowing reproducible
responses in cases where the same input parameters are used across
multiple requests. By setting the same seed value, you can obtain
identical results for debugging, testing, or evaluation purposes. The
value of Seed should be an integer. Non-integral values will be
truncated. Default is 0.

Provide feedback

---

SystemPrompt

Read Parallel

Provides context to the model about its role, tone, or behavior during
conversation.

TextGenerator.SystemPrompt:[string](/docs/luau/strings)

Provides context to the model about its role, tone, or behavior during the
conversation. This parameter can guide the model on how to respond,
setting expectations like "You are an assistant" or
"Use a formal tone".

Provide feedback

---

Temperature

Read Parallel

Controls the "creativity" or randomness of the model's responses.

TextGenerator.Temperature:[number](/docs/luau/numbers)

Controls the "creativity" or randomness of the model's responses. Values
closer to 1 increase randomness, while values closer to 0 make the
responses more focused and deterministic. Values outside the accepted
range are clamped to the range of [0.4, 1.0]. Default is 0.7.

Provide feedback

---

TopP

Read Parallel

Helps the AI model narrow or expand the range of possible words to sample
from while generating the next token.

TextGenerator.TopP:[number](/docs/luau/numbers)

Helps the model narrow or expand the range of possible words to sample
from while generating the next token. This setting narrows the token
choices to only contain words that together make up a certain percentage
of total likelihood (for example, 90%). A lower TopP means the model
sticks to closer and more predictable choices, while a higher TopP opens
the door to more diverse and creative responses. Values outside the
accepted range are clamped to the range of [0.5, 1.0]. Default is 0.9.

Provide feedback

---

Methods

GenerateTextAsync

Yields

Returns text generated by an LLM based on the provided system and user
prompts.

TextGenerator:GenerateTextAsync(request:[Dictionary](/docs/luau/tables#dictionaries)):[Dictionary](/docs/luau/tables#dictionaries)

Parameters

|  |
| --- |
| request:[Dictionary](/docs/luau/tables#dictionaries)  A dictionary containing optional parameters for the text generation request. The currently supported parameters are UserPrompt, ContextToken, and MaxTokens. |

Returns

[Dictionary](/docs/luau/tables#dictionaries)

A dictionary containing the generated response.

This method returns text generated by an LLM based on the provided system
and user prompts, as well as any other optional paramaters that have been
set.

The request argument for this method should be a dictionary with the
following structure:

| Key Name | Data Type | Description | Required |
| --- | --- | --- | --- |
| UserPrompt | string | Optional prompt from the user that initiates the chat. This could be a question, statement, or command that the user wants the model to respond to. | No |
| ContextToken | string | Prompt history context token containing a summarization of the previous prompt requests and responses in a conversation up to the current request. If no token is provided, a new token is generated and returned in the response. Providing a previously generated context token restores the conversation state into the current request. | No |
| MaxTokens | number | The maximum number of tokens in the response generated by the model. Expected to be an integer of at least 1. This limits the length of the response, preventing overly long or incomplete answers. Non-integral numbers are rounded to the nearest integer. | No |
| JsonSchema | string | A JSON Schema formatted string that follows the specification at [json-schema.org](https://json-schema.org). When JsonSchema is provided, the model response will conform to the requested format, providing a structured output that can be parsed. | No |

This method returns a dictionary with the following structure:

| Key Name | Data Type | Description |
| --- | --- | --- |
| GeneratedText | string | The generated response. |
| ContextToken | string | A token containing the summarization of a previously passed context token and the current generated response. This token can be passed into subsequent requests to maintain the state of the current conversation. Subsequent requests generate new tokens with updated conversation state. Extracting the token and providing it maintains the ongoing conversation context. |
| Model | string | The model and version that generated the response. |

Provide feedback

---