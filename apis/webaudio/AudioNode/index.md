---
title: 'AudioNode'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'AudioNodes are the building blocks of an AudioContext. An AudioNode represents audio sources, the audio destination, and intermediate processing modules, connected together to form processing graphs for rendering audio to the audio hardware. In general, an AudioNode processes its inputs (if it has any), and generates audio for its outputs (if it has any).'
tags:
  - API_Objects
  - API
  - WebAudio
uri: apis/webaudio/AudioNode

---
## Summary

AudioNodes are the building blocks of an AudioContext. An AudioNode represents audio sources, the audio destination, and intermediate processing modules, connected together to form processing graphs for rendering audio to the audio hardware. In general, an AudioNode processes its inputs (if it has any), and generates audio for its outputs (if it has any).

## Properties

[context](/apis/webaudio/AudioNode/context)
:   The AudioContext that owns this AudioNode.

[numberOfInputs](/apis/webaudio/AudioNode/numberOfInputs)
:   The number of inputs feeding into the AudioNode. For source nodes, this value will be 0.

[numberOfOutputs](/apis/webaudio/AudioNode/numberOfOutputs)
:   The number of outputs coming out of an AudioNode. For destination nodes, this will be 0.

## Methods

[connect](/apis/webaudio/AudioNode/connect)
:   Connects one AudioNode to another AudioNode.

[disconnect](/apis/webaudio/AudioNode/disconnect)
:   Disconnects an AudioNode from another that it is already connected to.

## Events

*No events.*

## Related specifications

[W3C Web Audio API](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html)
:   W3C Editor's Draft
