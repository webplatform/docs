---
title: 'coneOuterGain'
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
  - API_Object_Properties
  - API
  - WebAudio
uri: apis/webaudio/PannerNode/coneOuterGain

---
## Summary

A parameter for directional audio sources, this is the amount of volume reduction outside of the coneOuterAngle. The default value is 0.

Property of [apis/webaudio/PannerNode](/apis/webaudio/PannerNode)[apis/webaudio/PannerNode](/apis/webaudio/PannerNode)

## Syntax

``` js
var result = PannerNode.coneOuterGain;
PannerNode.coneOuterGain = value;
```

## Return Value

Returns an object of type NumberNumber

## Examples

``` js
var audioCtx = new AudioContext();
var panner = audioCtx.createPanner();
panner.coneOuterGain = 0;
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
