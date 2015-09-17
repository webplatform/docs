---
title: 'onremovetrack'
notes:
  - 'Needs example, usage, spec reference'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/media_capture_and_streams/MediaStream
    href: /apis/media_capture_and_streams/MediaStream
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /apis/media_capture_and_streams/MediaStream
standardization_status: 'W3C Working Draft'
summary: 'Handles the removetrack event when fired on the MediaStream object.'
tags:
  - API_Object_Properties
  - API
  - Media_Capture_and_Streams
  - Needs_Examples
uri: 'apis/media capture and streams/MediaStream/onremovetrack'

---
## Summary

Handles the removetrack event when fired on the MediaStream object.

Property of [apis/media\_capture\_and\_streams/MediaStream](/apis/media_capture_and_streams/MediaStream)[apis/media\_capture\_and\_streams/MediaStream](/apis/media_capture_and_streams/MediaStream)

## Syntax

``` js
var result = stream.onremovetrack;
stream.onremovetrack = value;
```

## Return Value

Returns an object of type

EventHandler

