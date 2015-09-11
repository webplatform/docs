---
title: peerIdentity
notes:
  - 'Needs spec reference, standardization status'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webrtc/RTCPeerConnection
    href: /apis/webrtc/RTCPeerConnection
  return:
    predicate: 'Returns an object of type '
    value: RTCIdentityAssertion
    href: /apis/webrtc/RTCPeerConnection
standardization_status: 'W3C Working Draft'
summary: 'Contains the peer identity assertion information if an identity assertion was provided and verified.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebRTC
uri: apis/webrtc/RTCPeerConnection/peerIdentity

---
## <span>Summary</span>

Contains the peer identity assertion information if an identity assertion was provided and verified.

Property of [apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.peerIdentity;
```

## <span>Return Value</span>

Returns an object of type RTCIdentityAssertionRTCIdentityAssertion

The RTCIdentityAssertion object has two string members:

-   idp - the domain name representing the identity provider
-   name - the name of the verified peer identity

## <span>Examples</span>

This example shows how to consume identity assertions.

``` js
pc.onidentityresult = function(result) {
  console.log("IdP= " + pc.peerIdentity.idp +
              " identity=" + pc.peerIdentity.name);
};
```

## <span>Notes</span>

The identity system is designed so that applications need not take any special action in order for users to generate and verify identity assertions; if a user has configured an IdP into their browser, then the browser will automatically request/generate assertions and the other side will automatically verify them and display the results.