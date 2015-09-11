---
title: bufferedAmount
notes:
  - 'Needs example'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webrtc/RTCDataChannel
    href: /apis/webrtc/RTCDataChannel
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned long'
    href: /apis/webrtc/RTCDataChannel
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the number of bytes of application data that have been queued using send() but that (as of the last time the event loop started executing a task) have not yet been transmitted to the network.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebRTC
uri: apis/webrtc/RTCDataChannel/bufferedAmount

---
## <span>Summary</span>

Returns the number of bytes of application data that have been queued using send() but that (as of the last time the event loop started executing a task) have not yet been transmitted to the network.

Property of [apis/webrtc/RTCDataChannel](/apis/webrtc/RTCDataChannel)[apis/webrtc/RTCDataChannel](/apis/webrtc/RTCDataChannel)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = object.bufferedAmount;
```

## <span>Return Value</span>

Returns an object of type unsigned longunsigned long

**Needs Examples**: This section should include examples.

## <span>Related specifications</span>

[W3C Web RTC Specification](http://dev.w3.org/2011/webrtc/editor/webrtc.html)
:   W3C Editor's Draft
