---
title: distanceModel
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Determines which algorithm will be used to reduce the volume of an audio source as it moves away from the listener. See below for the available choices. The default is INVERSE_DISTANCE.'
uri: apis/webaudio/PannerNode/distanceModel

---
# distanceModel

## Summary

Determines which algorithm will be used to reduce the volume of an audio source as it moves away from the listener. See below for the available choices. The default is INVERSE\_DISTANCE.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/PannerNode](/apis/webaudio/PannerNode)</span></span>

## Syntax

``` {.js}
var result = PannerNode.distanceModel;
PannerNode.distanceModel = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned short</span></span>

Uses one of the following constant values:

-   LINEAR (0), a linear distance model which calculates distanceGain as 1 - rolloffFactor \* (distance - refDistance) / (maxDistance - refDistance);
-   INVERSE (1) (default), an inverse distance model which calculates distanceGain as refDistance / (refDistance + rolloffFactor \* (distance - refDistance));
-   EXPONENTIAL (2), an exponential distance model which calculates distanceGain as pow(distance / refDistance, -rolloffFactor).

## Examples

``` {.js}
var audioCtx = new AudioContext();
var panner = audioCtx.createPanner();
panner.distanceModel = 'inverse';
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

