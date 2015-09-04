---
title: numberOfInputs
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The number of inputs feeding into the AudioNode. For source nodes, this value will be 0.'
uri: apis/webaudio/AudioNode/numberOfInputs

---
# numberOfInputs

## Summary

The number of inputs feeding into the AudioNode. For source nodes, this value will be 0.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioNode](/apis/webaudio/AudioNode)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = AudioNode.numberOfInputs;
```

## Examples

``` {.js}
var oscillator = audioCtx.createOscillator();
var inputs = oscillator.numberOfInputs;
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

