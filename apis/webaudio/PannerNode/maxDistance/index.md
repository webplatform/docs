---
title: maxDistance
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
summary: 'The maximum distance between source and listener, after which the volume will not be reduced any further. The default value is 10000.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/PannerNode/maxDistance

---
## <span>Summary</span>

The maximum distance between source and listener, after which the volume will not be reduced any further. The default value is 10000.

Property of [apis/webaudio/PannerNode](/apis/webaudio/PannerNode)[apis/webaudio/PannerNode](/apis/webaudio/PannerNode)

## <span>Syntax</span>

``` js
var result = PannerNode.maxDistance;
PannerNode.maxDistance = value;
```

## <span>Return Value</span>

Returns an object of type NumberNumber

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var panner = audioCtx.createPanner();
panner.maxDistance = 10000;
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
