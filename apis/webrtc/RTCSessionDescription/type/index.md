---
title: type
tags:
  0: API
  1: Object
  2: Properties
  4: WebRTC
readiness: 'In Progress'
notes:
  - 'Needs example, spec reference, standardization status'
summary: 'The type of SDP object this RTCSessionDescription represents.'
uri: apis/webrtc/RTCSessionDescription/type

---
# type

## Summary

The type of SDP object this RTCSessionDescription represents.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webrtc/RTCSessionDescription](/apis/webrtc/RTCSessionDescription)</span></span>

## Syntax

``` {.js}
var result = element.type;
element.type = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">RTCSdpType</span></span>

The RTCSdpType enum has the following values:

-   answer - use the SDP object as the final answer.
-   offer - use the SDP object as an offer.
-   pranswer - use the SDP object as a provisional answer.

**Needs Examples**: This section should include examples.

