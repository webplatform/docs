---
title: bufferedAmount
tags:
  0: API
  1: Object
  2: Properties
  4: WebRTC
readiness: 'Almost Ready'
standardization_status: 'W3C Editor''s Draft'
notes:
  - 'Needs example'
summary: 'Returns the number of bytes of application data that have been queued using send() but that (as of the last time the event loop started executing a task) have not yet been transmitted to the network.'
uri: apis/webrtc/RTCDataChannel/bufferedAmount

---
# bufferedAmount

## Summary

Returns the number of bytes of application data that have been queued using send() but that (as of the last time the event loop started executing a task) have not yet been transmitted to the network.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webrtc/RTCDataChannel](/apis/webrtc/RTCDataChannel)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = object.bufferedAmount;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[W3C Web RTC Specification](http://dev.w3.org/2011/webrtc/editor/webrtc.html)
:   W3C Editor's Draft

