---
title: endOfStream
tags:
  - API
  - Object
  - Methods
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'Used to indicate that the end of the stream has been reached.'
uri: 'apis/media source extensions/MediaSource/endOfStream'

---
# endOfStream

## Summary

Used to indicate that the end of the stream has been reached.

*Method of [apis/media\_source\_extensions/MediaSource](/apis/media_source_extensions/MediaSource)*

## Syntax

``` {.js}
 MediaSource.endOfStream(error);
```

## Parameters

### error

 Data-typeÂ
:   enum

*(Optional)*

Type: EndOfStreamError

If an error has occurred, this optional parameter can be used to send error information.

EndOfStreamError error values

network
:   A network error occurred.
decode
:   A decode error occurred.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Usage

     This method throws an INVALID_STATE_ERR exception under the following conditions:

-   If the readyState attribute is not open.
-   If the updating attribute is true on any SourceBuffer in sourceBuffers.

