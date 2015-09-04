---
title: numberOfOutputs
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The number of outputs coming out of an AudioNode. For destination nodes, this will be 0.'
uri: apis/webaudio/AudioNode/numberOfOutputs

---
# numberOfOutputs

## Summary

The number of outputs coming out of an AudioNode. For destination nodes, this will be 0.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioNode](/apis/webaudio/AudioNode)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = AudioNode.numberOfOutputs;
```

## Examples

``` {.js}
var oscillator = audioCtx.createOscillator();
var outputs = oscillator.numberOfOutputs;
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

