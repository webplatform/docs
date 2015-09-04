---
title: context
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The AudioContext that owns this AudioNode.'
uri: apis/webaudio/AudioNode/context

---
# context

## Summary

The AudioContext that owns this AudioNode.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioNode](/apis/webaudio/AudioNode)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = AudioNode.context;
```

## Examples

``` {.js}
var audioCtx = new AudioContext();
var oscillator = audioCtx.createOscillator();
var cont = oscillator.context; // "audioCtx"
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

