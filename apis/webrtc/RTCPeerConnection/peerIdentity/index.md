---
title: peerIdentity
tags:
  0: API
  1: Object
  2: Properties
  4: WebRTC
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs spec reference, standardization status'
summary: 'Contains the peer identity assertion information if an identity assertion was provided and verified.'
uri: apis/webrtc/RTCPeerConnection/peerIdentity

---
# peerIdentity

## Summary

Contains the peer identity assertion information if an identity assertion was provided and verified.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.peerIdentity;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">RTCIdentityAssertion</span></span>

The RTCIdentityAssertion object has two string members:

-   idp - the domain name representing the identity provider
-   name - the name of the verified peer identity

## Examples

This example shows how to consume identity assertions.

``` {.js}
pc.onidentityresult = function(result) {
  console.log("IdP= " + pc.peerIdentity.idp +
              " identity=" + pc.peerIdentity.name);
};
```

## Notes

The identity system is designed so that applications need not take any special action in order for users to generate and verify identity assertions; if a user has configured an IdP into their browser, then the browser will automatically request/generate assertions and the other side will automatically verify them and display the results.

