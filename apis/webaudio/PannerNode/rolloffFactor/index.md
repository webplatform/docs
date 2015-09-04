---
title: rolloffFactor
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Describes how quickly the volume is reduced as source moves away from listener. The default value is 1.'
uri: apis/webaudio/PannerNode/rolloffFactor

---
# rolloffFactor

## Summary

Describes how quickly the volume is reduced as source moves away from listener. The default value is 1.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/PannerNode](/apis/webaudio/PannerNode)</span></span>

## Syntax

``` {.js}
var result = PannerNode.rolloffFactor;
PannerNode.rolloffFactor = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.js}
var audioCtx = new AudioContext();
var panner = audioCtx.createPanner();
panner.rolloffFactor = 1;
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

