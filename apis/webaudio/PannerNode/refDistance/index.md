---
title: refDistance
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'A reference distance for reducing volume as source moves further from the listener. The default value is 1.'
uri: apis/webaudio/PannerNode/refDistance

---
# refDistance

## Summary

A reference distance for reducing volume as source moves further from the listener. The default value is 1.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/PannerNode](/apis/webaudio/PannerNode)</span></span>

## Syntax

``` {.js}
var result = PannerNode.refDistance;
PannerNode.refDistance = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.js}
var audioCtx = new AudioContext();
var panner = audioCtx.createPanner();
panner.refDistance = 1;
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

