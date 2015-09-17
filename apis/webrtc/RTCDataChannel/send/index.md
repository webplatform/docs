---
title: 'send'
notes:
  - 'Needs example'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/webrtc/RTCDataChannel
    href: /apis/webrtc/RTCDataChannel
standardization_status: 'W3C Editor''s Draft'
summary: 'Sends a message (data) on the RTCDataChannel’s underlying data transport.'
tags:
  - API_Object_Methods
  - API
  - WebRTC
  - Needs_Examples
uri: apis/webrtc/RTCDataChannel/send

---
## Summary

Sends a message (data) on the RTCDataChannel’s underlying data transport.

Method of [apis/webrtc/RTCDataChannel](/apis/webrtc/RTCDataChannel)[apis/webrtc/RTCDataChannel](/apis/webrtc/RTCDataChannel)

## Syntax

``` js
 object.send(data);
```

## Parameters

### data

 Data-type
:   any

 The send() method is overloaded to handle different data argument types. This parameter may be any of the following objects:

-   string -- a series of Unicode characters
-   Blob -- raw data represented by a Blob object
-   ArrayBuffer -- data directly stored in an ArrayBuffer object
-   ArrayBufferView -- data stored in a section of an ArrayBuffer object that the ArrayBufferview object references

## Return Value

No return value

## Related specifications

[W3C Web RTC Specification](http://dev.w3.org/2011/webrtc/editor/webrtc.html)
:   W3C Editor's Draft
