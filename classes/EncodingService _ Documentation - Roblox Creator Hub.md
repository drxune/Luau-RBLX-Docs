# EncodingService | Documentation - Roblox Creator Hub

Source: https://create.roblox.com/docs/reference/engine/classes/EncodingService
Scraped: 2026-01-11T02:28:04.189139Z

## Tags
- Not Creatable
- Service
- Not Replicated

## Inherits
- Instance
- EncodingService
- Object
- EncodingService.GetDecompressedBufferSize
- EncodingService.DecompressBuffer
1. [Classes](/docs/reference/engine/classes)
2. /
4. /
5. [Instance](/docs/reference/engine/classes/Instance)
6. /
7. [EncodingService](/docs/reference/engine/classes/EncodingService)

English

Feedback

Engine Class

EncodingService

Service providing common encoding, hashing, and compression methods.

Not Creatable

Service

Not Replicated

---

Summary

Methods

|  |
| --- |
| [Base64Decode](#Base64Decode)(input: [buffer](/docs/reference/engine/libraries/buffer)):[buffer](/docs/reference/engine/libraries/buffer) |
| [Base64Encode](#Base64Encode)(input: [buffer](/docs/reference/engine/libraries/buffer)):[buffer](/docs/reference/engine/libraries/buffer) |
| [CompressBuffer](#CompressBuffer)(input: [buffer](/docs/reference/engine/libraries/buffer),algorithm: [Enum.CompressionAlgorithm](/docs/reference/engine/enums/CompressionAlgorithm),compressionLevel: [number](/docs/luau/numbers)):[buffer](/docs/reference/engine/libraries/buffer) |
| [ComputeBufferHash](#ComputeBufferHash)(input: [buffer](/docs/reference/engine/libraries/buffer),algorithm: [Enum.HashAlgorithm](/docs/reference/engine/enums/HashAlgorithm)):[buffer](/docs/reference/engine/libraries/buffer) |
| [ComputeStringHash](#ComputeStringHash)(input: [string](/docs/luau/strings),algorithm: [Enum.HashAlgorithm](/docs/reference/engine/enums/HashAlgorithm)):[string](/docs/luau/strings) |
| [DecompressBuffer](#DecompressBuffer)(input: [buffer](/docs/reference/engine/libraries/buffer),algorithm: [Enum.CompressionAlgorithm](/docs/reference/engine/enums/CompressionAlgorithm)):[buffer](/docs/reference/engine/libraries/buffer) |
| [GetDecompressedBufferSize](#GetDecompressedBufferSize)(input: [buffer](/docs/reference/engine/libraries/buffer),algorithm: [Enum.CompressionAlgorithm](/docs/reference/engine/enums/CompressionAlgorithm)):[number](/docs/luau/numbers)? |

Inherited Members

57 inherited from [Instance](/docs/reference/engine/classes/Instance)

6 inherited from [Object](/docs/reference/engine/classes/Object)

Service providing common encoding, hashing, and compression methods.

---

API Reference

Methods

Base64Decode

Write Parallel

EncodingService:Base64Decode(input:[buffer](/docs/reference/engine/libraries/buffer)):[buffer](/docs/reference/engine/libraries/buffer)

Parameters

|  |
| --- |
| input:[buffer](/docs/reference/engine/libraries/buffer)  [buffer](/docs/reference/engine/libraries/buffer) containing Base64 data to decode |

Returns

[buffer](/docs/reference/engine/libraries/buffer)

[buffer](/docs/reference/engine/libraries/buffer) with the decoded result

Method takes a [buffer](/docs/reference/engine/libraries/buffer) with data encoded in Base64 format and
decodes it into a new [buffer](/docs/reference/engine/libraries/buffer).

If the input is not valid Base64 data, this method throws an error.

Base64 data is most often used for binary data encoding, so these
functions are designed to work on [buffer](/docs/reference/engine/libraries/buffer) values.

If the data is stored in a string, [buffer.fromstring](/docs/reference/engine/libraries/buffer#fromstring) can be used
to quickly convert it into a buffer.

Provide feedback

---

Base64Encode

Write Parallel

EncodingService:Base64Encode(input:[buffer](/docs/reference/engine/libraries/buffer)):[buffer](/docs/reference/engine/libraries/buffer)

Parameters

|  |
| --- |
| input:[buffer](/docs/reference/engine/libraries/buffer)  [buffer](/docs/reference/engine/libraries/buffer) containing binary data to encode |

Returns

[buffer](/docs/reference/engine/libraries/buffer)

[buffer](/docs/reference/engine/libraries/buffer) with the encoded result

Method takes a [buffer](/docs/reference/engine/libraries/buffer) with binary data and encodes it using
Base64.

Encoded result is returned as a new [buffer](/docs/reference/engine/libraries/buffer).

Provide feedback

---

CompressBuffer

Write Parallel

EncodingService:CompressBuffer(

input:[buffer](/docs/reference/engine/libraries/buffer), algorithm:[Enum.CompressionAlgorithm](/docs/reference/engine/enums/CompressionAlgorithm), compressionLevel:[number](/docs/luau/numbers)

):[buffer](/docs/reference/engine/libraries/buffer)

Parameters

|  |
| --- |
| input:[buffer](/docs/reference/engine/libraries/buffer)  [buffer](/docs/reference/engine/libraries/buffer) with binary data to compress |
| algorithm:[Enum.CompressionAlgorithm](/docs/reference/engine/enums/CompressionAlgorithm)  [Enum.CompressionAlgorithm](/docs/reference/engine/enums/CompressionAlgorithm) to use for compression |
| compressionLevel:[number](/docs/luau/numbers) Default Value: 1 optional integer compression level to use |

Returns

[buffer](/docs/reference/engine/libraries/buffer)

[buffer](/docs/reference/engine/libraries/buffer) with compressed binary data

Compresses the binary data stored in a [buffer](/docs/reference/engine/libraries/buffer) using the
specified compression algorithm and compression level. The higher the
compression level, the longer it takes to compress, but the resulting
compression ratio might increase.

For [Enum.CompressionAlgorithm.Zstd](/docs/reference/engine/enums/CompressionAlgorithm#Zstd), the allowed compression values are
from -7 to 22 inclusive.

Provide feedback

---

ComputeBufferHash

Write Parallel

EncodingService:ComputeBufferHash(

input:[buffer](/docs/reference/engine/libraries/buffer), algorithm:[Enum.HashAlgorithm](/docs/reference/engine/enums/HashAlgorithm)

):[buffer](/docs/reference/engine/libraries/buffer)

Parameters

|  |
| --- |
| input:[buffer](/docs/reference/engine/libraries/buffer)  [buffer](/docs/reference/engine/libraries/buffer) with binary data to compute hash for |
| algorithm:[Enum.HashAlgorithm](/docs/reference/engine/enums/HashAlgorithm)  [Enum.HashAlgorithm](/docs/reference/engine/enums/HashAlgorithm) cryptographic hash function |

Returns

[buffer](/docs/reference/engine/libraries/buffer)

[buffer](/docs/reference/engine/libraries/buffer) with the binary data of the hash

Uses a
[cryptographic hash function](https://en.wikipedia.org/wiki/Cryptographic_hash_function)
to compute a hash of the input [buffer](/docs/reference/engine/libraries/buffer). Returns a new
[buffer](/docs/reference/engine/libraries/buffer) with the binary data.

See descriptions of [Enum.HashAlgorithm](/docs/reference/engine/enums/HashAlgorithm) to learn of the supported digest
size for each hash.

#### Do not use this for passwords

None of these hashes are password hashing algorithms. They were designed
to be fast to execute, whereas password hashing should never be fast. You
shouldn't use this function for computing password hashes that will be
stored, or for deriving keys from passwords.

Provide feedback

---

ComputeStringHash

Write Parallel

EncodingService:ComputeStringHash(

input:[string](/docs/luau/strings), algorithm:[Enum.HashAlgorithm](/docs/reference/engine/enums/HashAlgorithm)

):[string](/docs/luau/strings)

Parameters

|  |
| --- |
| input:[string](/docs/luau/strings)  string to compute the hash for |
| algorithm:[Enum.HashAlgorithm](/docs/reference/engine/enums/HashAlgorithm)  [Enum.HashAlgorithm](/docs/reference/engine/enums/HashAlgorithm) cryptographic hash function |

Returns

[string](/docs/luau/strings)

String with the binary data of the hash

Uses a
[cryptographic hash function](https://en.wikipedia.org/wiki/Cryptographic_hash_function)
to compute a hash of the input string. Returns a new string with the
binary data.

See descriptions of [Enum.HashAlgorithm](/docs/reference/engine/enums/HashAlgorithm) to learn of the supported digest
size for each hash.

#### Do not use this for passwords

None of these hashes are password hashing algorithms. They were designed
to be fast to execute, whereas password hashing should never be fast. You
shouldn't use this function for computing password hashes that will be
stored, or for deriving keys from passwords.

Provide feedback

---

DecompressBuffer

Write Parallel

EncodingService:DecompressBuffer(

input:[buffer](/docs/reference/engine/libraries/buffer), algorithm:[Enum.CompressionAlgorithm](/docs/reference/engine/enums/CompressionAlgorithm)

):[buffer](/docs/reference/engine/libraries/buffer)

Parameters

|  |
| --- |
| input:[buffer](/docs/reference/engine/libraries/buffer)  [buffer](/docs/reference/engine/libraries/buffer) with compressed binary data |
| algorithm:[Enum.CompressionAlgorithm](/docs/reference/engine/enums/CompressionAlgorithm)  [Enum.CompressionAlgorithm](/docs/reference/engine/enums/CompressionAlgorithm) to use for decompression |

Returns

[buffer](/docs/reference/engine/libraries/buffer)

[buffer](/docs/reference/engine/libraries/buffer) with the decompressed binary data

Decompresses the binary data stored in a [buffer](/docs/reference/engine/libraries/buffer) using the
specified compression algorithm.

Decompression might throw an error if the compressed data doesn't contain
expected decompressed size, if it is larger than 1GB or if it is invalid.

It is recommended to use [EncodingService.GetDecompressedBufferSize](/docs/reference/engine/classes/EncodingService#GetDecompressedBufferSize)
to find out the decompressed data size before attempting to decompress.
This is very important if the input buffer contents are outside of your
control (for example, from a client Class.RemoveEvent)

Provide feedback

---

GetDecompressedBufferSize

Write Parallel

EncodingService:GetDecompressedBufferSize(

input:[buffer](/docs/reference/engine/libraries/buffer), algorithm:[Enum.CompressionAlgorithm](/docs/reference/engine/enums/CompressionAlgorithm)

):[number](/docs/luau/numbers)?

Parameters

|  |
| --- |
| input:[buffer](/docs/reference/engine/libraries/buffer)  [buffer](/docs/reference/engine/libraries/buffer) with compressed binary data |
| algorithm:[Enum.CompressionAlgorithm](/docs/reference/engine/enums/CompressionAlgorithm)  [Enum.CompressionAlgorithm](/docs/reference/engine/enums/CompressionAlgorithm) used to compress it |

Returns

[number](/docs/luau/numbers)?

Integer size of the decompressed data or 'nil'

Reports the size of the decompressed data stored in a compressed
[buffer](/docs/reference/engine/libraries/buffer). If the compressed data doesn't have a size or the size
is corrupted or invalid (larger than 1GB), function returns nil. When a
nil is returned, attempting to use
[EncodingService.DecompressBuffer](/docs/reference/engine/classes/EncodingService#DecompressBuffer) on this [buffer](/docs/reference/engine/libraries/buffer) will
throw an error.

Provide feedback

---