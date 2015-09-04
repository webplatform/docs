---
title: destination
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'An AudioDestinationNode with a single input representing the final destination for all audio (to be rendered to the audio hardware, i.e., speakers). All AudioNodes actively rendering audio will directly or indirectly connect to the destination node.'
uri: apis/webaudio/AudioContext/destination

---
# destination

## Summary

An AudioDestinationNode with a single input representing the final destination for all audio (to be rendered to the audio hardware, i.e., speakers). All AudioNodes actively rendering audio will directly or indirectly connect to the destination node.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = AudioContext.destination;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value"></span></span>

AudioDestinationNode

## Examples

``` {.js}
var audioCtx = new AudioContext();
gainNode.connect(audioCtx.destination);
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

