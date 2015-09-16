---
title: 'iceState'
notes:
  - 'Needs example, spec reference'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webrtc/RTCPeerConnection
    href: /apis/webrtc/RTCPeerConnection
  return:
    predicate: 'Returns an object of type '
    value: RTCIceState
    href: /apis/webrtc/RTCPeerConnection
standardization_status: 'W3C Working Draft'
summary: 'Returns the ICE state of the ICE agent.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebRTC
uri: apis/webrtc/RTCPeerConnection/iceState

---
## Summary

Returns the ICE state of the ICE agent.

Property of [apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.iceState;
```

## Return Value

Returns an object of type RTCIceStateRTCIceState

The RTCIceState enum has the following values:

-   starting - The ICE Agent is gathering addresses and/or waiting for remote candidates to be supplied.
-   checking - The ICE Agent has received remote candidates on at least one component, and is checking candidate pairs but has not yet found a connection. In addition to checking, it may also still be gathering.
-   connected - The ICE Agent has found a usable connection for all components but is still checking other candidate pairs to see if there is a better connection. It may also still be gathering.
-   completed - The ICE Agent has finished gathering and checking and found a connection for all components.
-   failed - The ICE Agent is finished checking all candidate pairs and failed to find a connection for at least one component.
-   disconnected - Liveness checks have failed for one or more components. This is more aggressive than failed, and may trigger intermittently (and resolve itself without action) on a flaky network.
-   closed - The ICE Agent has shut down and is no longer responding to STUN requests.

**Needs Examples**: This section should include examples.

## Usage

     An example transition might look like this:

-   new PeerConnection(): Starting
-   (Starting, remote candidates received): Checking
-   (Checking, found usable connection): Connected
-   (Checking, gave up): Failed
-   (Connected, finished all checks): Completed
-   (Completed, lost connectivity): Disconnected
-   (any state, ICE restart occurs): Starting
-   close(): Closed

## Notes

States take either the value of any component or all components, as outlined here:

-   `checking` occurs if ANY component has received a candidate and can start checking.
-   `connected` occurs if ALL components have established a working connection.
-   `completed` occurs if ALL components have finalized the running of their ICE processes.
-   `failed` occurs if ANY component has given up trying to connect.
-   `disconnected` occurs if ANY component has failed liveness checks.
-   `closed` occurs only if PeerConnection.close() has been called.
