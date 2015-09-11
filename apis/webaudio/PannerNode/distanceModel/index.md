---
title: distanceModel
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/PannerNode
    href: /apis/webaudio/PannerNode
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned short'
    href: /apis/webaudio/PannerNode
standardization_status: 'W3C Editor''s Draft'
summary: 'Determines which algorithm will be used to reduce the volume of an audio source as it moves away from the listener. See below for the available choices. The default is INVERSE_DISTANCE.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/PannerNode/distanceModel

---
## <span>Summary</span>

Determines which algorithm will be used to reduce the volume of an audio source as it moves away from the listener. See below for the available choices. The default is INVERSE\_DISTANCE.

Property of [apis/webaudio/PannerNode](/apis/webaudio/PannerNode)[apis/webaudio/PannerNode](/apis/webaudio/PannerNode)

## <span>Syntax</span>

``` js
var result = PannerNode.distanceModel;
PannerNode.distanceModel = value;
```

## <span>Return Value</span>

Returns an object of type unsigned shortunsigned short

Uses one of the following constant values:

-   LINEAR (0), a linear distance model which calculates distanceGain as 1 - rolloffFactor \* (distance - refDistance) / (maxDistance - refDistance);
-   INVERSE (1) (default), an inverse distance model which calculates distanceGain as refDistance / (refDistance + rolloffFactor \* (distance - refDistance));
-   EXPONENTIAL (2), an exponential distance model which calculates distanceGain as pow(distance / refDistance, -rolloffFactor).

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var panner = audioCtx.createPanner();
panner.distanceModel = 'inverse';
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
