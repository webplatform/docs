---
title: 'getIdentityAssertion'
notes:
  - 'Needs example, spec reference, return value'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/webrtc/RTCPeerConnection
    href: /apis/webrtc/RTCPeerConnection
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/webrtc/RTCPeerConnection
summary: 'Provides an identity assertion.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebRTC
uri: apis/webrtc/RTCPeerConnection/getIdentityAssertion

---
## Summary

Provides an identity assertion.

Method of [apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)

## Syntax

``` js
var result = element.getIdentityAssertion();
```

## Return Value

Returns an object of type

**Needs Examples**: This section should include examples.

## Notes

Applications need not make this call. It is merely intended to allow them to start the process of obtaining identity assertions before a call is initiated. If an identity is needed, either because the browser has been configured with a default identity provider or because the [setIdentityProvider()](/apis/webrtc/RTCPeerConnection/setIdentityProvider) method was called, then an identity will be automatically requested when an offer or answer is created.
