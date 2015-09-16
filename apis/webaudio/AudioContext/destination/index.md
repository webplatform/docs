---
title: destination
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/AudioContext
    href: /apis/webaudio/AudioContext
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /apis/webaudio/AudioContext
standardization_status: 'W3C Editor''s Draft'
summary: 'An AudioDestinationNode with a single input representing the final destination for all audio (to be rendered to the audio hardware, i.e., speakers). All AudioNodes actively rendering audio will directly or indirectly connect to the destination node.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AudioContext/destination

---
## Summary

An AudioDestinationNode with a single input representing the final destination for all audio (to be rendered to the audio hardware, i.e., speakers). All AudioNodes actively rendering audio will directly or indirectly connect to the destination node.

Property of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## Syntax

**Note**: This property is read-only.

``` js
var result = AudioContext.destination;
```

## Return Value

Returns an object of type

AudioDestinationNode

## Examples

``` js
var audioCtx = new AudioContext();
gainNode.connect(audioCtx.destination);
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
