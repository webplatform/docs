---
title: 'RTCDataChannel'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Represents a bi-directional data channel between two peers.'
tags:
  0: API
  1: Objects
  3: WebRTC
uri: apis/webrtc/RTCDataChannel

---
## Summary

Represents a bi-directional data channel between two peers.

## Properties

API Name
:   Summary

[binaryType](/apis/webrtc/RTCDataChannel/binaryType)
:   Returns the value to which it was last set; on creation, must be initialized to the string "blob".

[bufferedAmount](/apis/webrtc/RTCDataChannel/bufferedAmount)
:   Returns the number of bytes of application data that have been queued using send() but that (as of the last time the event loop started executing a task) have not yet been transmitted to the network.

[label](/apis/webrtc/RTCDataChannel/label)
:   A unique identifier that can be used to distinguish this RTCDataChannel object from other RTCDataChannel objects.

[onclose](/apis/webrtc/RTCDataChannel/onclose)
:   An event listener to be called when an RTCDataChannel is closed.

[onerror](/apis/webrtc/RTCDataChannel/onerror)
:   An event listener to be called when an error occurs.

[onmessage](/apis/webrtc/RTCDataChannel/onmessage)
:   An event listener to be called when a message is received.

[onopen](/apis/webrtc/RTCDataChannel/onopen)
:   An event listener to be called when an RTCDataChannel is opened.

[readyState](/apis/webrtc/RTCDataChannel/readyState)
:   Represents the state of the RTCDataChannel object.

[reliable](/apis/webrtc/RTCDataChannel/reliable)
:   Returns true if the RTCDataChannel is reliable, and false otherwise.

## Methods

API Name
:   Summary

[close](/apis/webrtc/RTCDataChannel/close)
:   Closes the RTCDataChannel.

[send](/apis/webrtc/RTCDataChannel/send)
:   Sends a message (*data*) on the RTCDataChannel’s underlying data transport.

## Events

*No events.*

## Related specifications

[W3C Web RTC Specification](http://dev.w3.org/2011/webrtc/editor/webrtc.html)
:   W3C Editor's Draft
