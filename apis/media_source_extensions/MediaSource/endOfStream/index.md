---
title: 'endOfStream'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/media_source_extensions/MediaSource
    href: /apis/media_source_extensions/MediaSource
summary: 'Used to indicate that the end of the stream has been reached.'
tags:
  - API_Object_Methods
  - Needs_Examples
uri: 'apis/media source extensions/MediaSource/endOfStream'

---
## Summary

Used to indicate that the end of the stream has been reached.

Method of [apis/media\_source\_extensions/MediaSource](/apis/media_source_extensions/MediaSource)[apis/media\_source\_extensions/MediaSource](/apis/media_source_extensions/MediaSource)

## Syntax

``` js
 MediaSource.endOfStream(error);
```

## Parameters

### error

 Data-type
:   enum

(Optional)

Type: EndOfStreamError

If an error has occurred, this optional parameter can be used to send error information.

EndOfStreamError error values

network
:   A network error occurred.
decode
:   A decode error occurred.

## Return Value

No return value

## Usage

     This method throws an INVALID_STATE_ERR exception under the following conditions:

-   If the readyState attribute is not open.
-   If the updating attribute is true on any SourceBuffer in sourceBuffers.

