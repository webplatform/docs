---
title: createDataChannel
tags:
  0: API
  1: Object
  2: Methods
  4: WebRTC
readiness: 'In Progress'
standardization_status: Experimental
notes:
  - 'Needs example, spec reference, return value'
summary: 'Creates an RTCDataChannel object with the given label.'
uri: apis/webrtc/RTCPeerConnection/createDataChannel

---
# createDataChannel

## Summary

Creates an RTCDataChannel object with the given label.

*Method of [apis/webrtc/RTCPeerConnection](/apis/webrtc/RTCPeerConnection)*

## Syntax

``` {.js}
var result = peerConnection.createDataChannel(label, options);
```

## Parameters

### label

 Data-typeÂ
:   String

 The label of the data channel.

### options

 Data-typeÂ
:   Object

*(Optional)*

Currently the only available option is a Boolean property named "reliable" (e.g. {reliable: false})

## Return Value

Returns an object of type .

