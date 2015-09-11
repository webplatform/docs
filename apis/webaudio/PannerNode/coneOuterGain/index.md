---
title: coneOuterGain
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/PannerNode
    href: /apis/webaudio/PannerNode
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /apis/webaudio/PannerNode
standardization_status: 'W3C Editor''s Draft'
summary: 'A parameter for directional audio sources, this is the amount of volume reduction outside of the coneOuterAngle. The default value is 0.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/PannerNode/coneOuterGain

---
## <span>Summary</span>

A parameter for directional audio sources, this is the amount of volume reduction outside of the coneOuterAngle. The default value is 0.

Property of [apis/webaudio/PannerNode](/apis/webaudio/PannerNode)[apis/webaudio/PannerNode](/apis/webaudio/PannerNode)

## <span>Syntax</span>

``` js
var result = PannerNode.coneOuterGain;
PannerNode.coneOuterGain = value;
```

## <span>Return Value</span>

Returns an object of type NumberNumber

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var panner = audioCtx.createPanner();
panner.coneOuterGain = 0;
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
