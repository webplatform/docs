---
title: coneInnerAngle
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'A parameter for directional audio sources, this is an angle inside of which there will be no volume reduction. The default value is 360.'
uri: apis/webaudio/PannerNode/coneInnerAngle

---
# coneInnerAngle

## Summary

A parameter for directional audio sources, this is an angle inside of which there will be no volume reduction. The default value is 360.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/PannerNode](/apis/webaudio/PannerNode)</span></span>

## Syntax

``` {.js}
var result = PannerNode.coneInnerAngle;
PannerNode.coneInnerAngle = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.js}
var audioCtx = new AudioContext();
var panner = audioCtx.createPanner();
panner.coneInnerAngle = 360;
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

