---
title: type
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webrtc/RTCSessionDescription
    href: /apis/webrtc/RTCSessionDescription
  return:
    predicate: 'Returns an object of type '
    value: RTCSdpType
    href: /apis/webrtc/RTCSessionDescription
summary: 'The type of SDP object this RTCSessionDescription represents.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebRTC
uri: apis/webrtc/RTCSessionDescription/type

---
## <span>Summary</span>

The type of SDP object this RTCSessionDescription represents.

Property of [apis/webrtc/RTCSessionDescription](/apis/webrtc/RTCSessionDescription)[apis/webrtc/RTCSessionDescription](/apis/webrtc/RTCSessionDescription)

## <span>Syntax</span>

``` js
var result = element.type;
element.type = value;
```

## <span>Return Value</span>

Returns an object of type RTCSdpTypeRTCSdpType

The RTCSdpType enum has the following values:

-   answer - use the SDP object as the final answer.
-   offer - use the SDP object as an offer.
-   pranswer - use the SDP object as a provisional answer.

**Needs Examples**: This section should include examples.

