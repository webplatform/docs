---
title: 'coneInnerAngle'
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
summary: 'A parameter for directional audio sources, this is an angle inside of which there will be no volume reduction. The default value is 360.'
tags:
  - API_Object_Properties
  - API
  - WebAudio
uri: apis/webaudio/PannerNode/coneInnerAngle

---
## Summary

A parameter for directional audio sources, this is an angle inside of which there will be no volume reduction. The default value is 360.

Property of [apis/webaudio/PannerNode](/apis/webaudio/PannerNode)[apis/webaudio/PannerNode](/apis/webaudio/PannerNode)

## Syntax

``` js
var result = PannerNode.coneInnerAngle;
PannerNode.coneInnerAngle = value;
```

## Return Value

Returns an object of type NumberNumber

## Examples

``` js
var audioCtx = new AudioContext();
var panner = audioCtx.createPanner();
panner.coneInnerAngle = 360;
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
