---
title: createDataChannel
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
standardization_status: Experimental
summary: 'Creates an RTCDataChannel object with the given label.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebRTC
uri: apis/webrtc/RTCPeerConnection/createDataChannel

---
## Summary

Creates an RTCDataChannel object with the given label.

Method of [apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)[apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)

## Syntax

``` js
var result = peerConnection.createDataChannel(label, options);
```

## Parameters

### label

 Data-type
:   String

 The label of the data channel.

### options

 Data-type
:   Object

(Optional)

Currently the only available option is a Boolean property named "reliable" (e.g. {reliable: false})

## Return Value

Returns an object of type
