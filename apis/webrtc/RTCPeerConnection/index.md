---
title: 'RTCPeerConnection'
notes:
  - 'Needs example, spec reference'
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
summary: 'Provides for the connection between remote peers, the transmission of locally generated MediaStream data and arbitrary data between peers.'
tags:
  0: API
  1: Objects
  3: WebRTC
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/webrtc/RTCPeerConnection/addstream
uri: apis/webrtc/RTCPeerConnection

---
## Summary

Provides for the connection between remote peers, the transmission of locally generated MediaStream data and arbitrary data between peers.

## Properties

API Name
:   Summary

[iceGatheringState](/apis/webrtc/RTCPeerConnection/iceGatheringState)
:   Returns the gathering state of the ICE agent.

[iceState](/apis/webrtc/RTCPeerConnection/iceState)
:   Returns the ICE state of the ICE agent.

[localDescription](/apis/webrtc/RTCPeerConnection/localDescription)
:   Returns the [RTCSessionDescription](/apis/webrtc/RTCSessionDescription) most recently passed to the [setLocalDescription()](/apis/webrtc/RTCPeerConnection/setLocalDescription) method along with any local candidate descriptions generated since the method was called.

[localStreams](/apis/webrtc/RTCPeerConnection/localStreams)
:   Returns an array of [MediaStream](/apis/webrtc/MediaStream) objects added to the connection with [addStream()](/apis/webrtc/RTCPeerConnection/addStream).

[onaddstream](/apis/webrtc/RTCPeerConnection/onaddstream)
:   Handles the [addstream](/w/index.php?title=apis/webrtc/RTCPeerConnection/addstream&action=edit&redlink=1) event fired when [setRemoteDescription()](/apis/webrtc/RTCPeerConnection/setRemoteDescription) is called.

[ondatachannel](/apis/webrtc/RTCPeerConnection/ondatachannel)
:   Handles the **datachannel** event.

[ongatheringchange](/apis/webrtc/RTCPeerConnection/ongatheringchange)
:   Handles the **gatheringchange** event for a change to the [iceGatheringState](/apis/webrtc/RTCPeerConnection/iceGatheringState) property.

[onicecandidate](/apis/webrtc/RTCPeerConnection/onicecandidate)
:   Handles the [icechange](/apis/webrtc/RTCPeerConnection/icechange) event for a change to the [apis/webrtc/RTCPeerConnection/iceState](/apis/webrtc/RTCPeerConnection/iceState) property. It is called any time there is a new ICE candidate added to a previous offer or answer.

[onicechange](/apis/webrtc/RTCPeerConnection/onicechange)
:   Handles the [icechange](/apis/webrtc/RTCPeerConnection/icechange) event. It is called any time the [iceState](/apis/webrtc/RTCPeerConnection/iceState) changes.

[onidentityresult](/apis/webrtc/RTCPeerConnection/onidentityresult)
:   Handles the [identityresult](/apis/webrtc/RTCPeerConnection/identityresult) event for the success or failure of an identity verification.

[onnegotiationneeded](/apis/webrtc/RTCPeerConnection/onnegotiationneeded)
:   Handles the [negotiationneeded](/apis/webrtc/RTCPeerConnection/negotiationneeded) event.

[onopen](/apis/webrtc/RTCPeerConnection/onopen)
:   Handles the [open](/apis/webrtc/RTCPeerConnection/open) event.

    Testing.

[onremovestream](/apis/webrtc/RTCPeerConnection/onremovestream)
:   Handles the [removeStream](/apis/webrtc/RTCPeerConnection/removeStream) event for when [setRemoteDescription()](/apis/webrtc/RTCPeerConnection/setRemoteDescription) is called to remove a [MediaStream](/apis/webrtc/MediaStream) object on the remote peer.

[onstatechange](/apis/webrtc/RTCPeerConnection/onstatechange)
:   Handles the [statechange](/apis/webrtc/RTCPeerConnection/statechange) event for when the [readyState](/apis/webrtc/RTCPeerConnection/readyState) property is changed, i.e. with a call to [setLocalDescription()](/apis/webrtc/RTCPeerConnection/setLocalDescription) or [setRemoteDescription()](/apis/webrtc/RTCPeerConnection/setRemoteDescription). The event does not fire when a new RTCPeerConnection object is created.

[peerIdentity](/apis/webrtc/RTCPeerConnection/peerIdentity)
:   Contains the peer identity assertion information if an identity assertion was provided and verified.

[readyState](/apis/webrtc/RTCPeerConnection/readyState)
:   Returns the ready state of the peer connection.

[remoteDescription](/apis/webrtc/RTCPeerConnection/remoteDescription)
:   Returns the [RTCSessionDescription](/apis/webrtc/RTCSessionDescription) most recently passed to the [setRemoteDescription()](/apis/webrtc/RTCPeerConnection/setRemoteDescription) method along with any remote candidate descriptions supplied with [addIceCandidate()](/apis/webrtc/RTCPeerConnection/addIceCandidate). Returns null if the remote description has not been set.

[remoteStreams](/apis/webrtc/RTCPeerConnection/remoteStreams)
:   Returns an array of [MediaStream](/apis/webrtc/MediaStream) objects added to the connection by the remote peer. This array is updated when the [addstream](/apis/webrtc/RTCPeerConnection/onaddstream) and [removestream](/apis/webrtc/RTCPeerConnection/removeStream) events are fired.

## Methods

API Name
:   Summary

[addIceCandidate](/apis/webrtc/RTCPeerConnection/addIceCandidate)
:   Provides a remote candidate to the ICE agent.

[addStream](/apis/webrtc/RTCPeerConnection/addStream)
:   Adds a new stream to the RTCPeerConnection.

[close](/apis/webrtc/RTCPeerConnection/close)
:   Closes a peer connection, stops all active ICE processing and any active streaming, and releases any relevant resources such as TURN permissions.

[createAnswer](/apis/webrtc/RTCPeerConnection/createAnswer)
:   Creates a session description compatible with the remote configuration.

[createDataChannel](/apis/webrtc/RTCPeerConnection/createDataChannel)
:   Creates an [RTCDataChannel](/apis/webrtc/RTCDataChannel) object with the given label.

[createOffer](/apis/webrtc/RTCPeerConnection/createOffer)
:   Creates a session description compatible with the local configuration.

[getIdentityAssertion](/apis/webrtc/RTCPeerConnection/getIdentityAssertion)
:   Provides an identity assertion.

[getStats](/apis/webrtc/RTCPeerConnection/getStats)
:   Retrieves status information for a given [MediaStreamTrack](/apis/webrtc/MediaStreamTrack).

[removeStream](/apis/webrtc/RTCPeerConnection/removeStream)
:   Removes the given stream from the [localStreams](/apis/webrtc/RTCPeerConnection/localStreams) array in the RTCPeerConnection and fires the [negotiationneeded](/apis/webrtc/RTCPeerConnection/negotiationneeded) event.

[setIdentityProvider](/apis/webrtc/RTCPeerConnection/setIdentityProvider)
:   Sets the identity provider. Not required if the browser is already configured for an identity provider.

[setLocalDescription](/apis/webrtc/RTCPeerConnection/setLocalDescription)
:   Applies the supplied [RTCSessionDescription](/apis/webrtc/RTCSessionDescription) to the local description.

[setRemoteDescription](/apis/webrtc/RTCPeerConnection/setRemoteDescription)
:   Applies the supplied [RTCSessionDescription](/apis/webrtc/RTCSessionDescription) to the remote description.

[updateIce](/apis/webrtc/RTCPeerConnection/updateIce)
:   Updates the ICE agent process that gathers local candidates and remote candidates.

## Events

API Name
:   Summary

[icecandidate](/apis/webrtc/RTCPeerConnection/icecandidate)
:

[icechange](/apis/webrtc/RTCPeerConnection/icechange)
:

[identityresult](/apis/webrtc/RTCPeerConnection/identityresult)
:

[negotiationneeded](/apis/webrtc/RTCPeerConnection/negotiationneeded)
:   The browser anticipates a session negotiation is required.

    It is triggered whenever [addStream](/apis/webrtc/RTCPeerConnection/addStream), [removeStream](/apis/webrtc/RTCPeerConnection/removeStream) or [setIdentityProvider](/apis/webrtc/RTCPeerConnection/setIdentityProvider) methods were called successfully and **RTCPeerConnection** signalingState is `stable` .

[open](/apis/webrtc/RTCPeerConnection/open)
:

[statechange](/apis/webrtc/RTCPeerConnection/statechange)
:

**Needs Examples**: This section should include examples.

