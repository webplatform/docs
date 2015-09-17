---
title: 'refDistance'
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
summary: 'A reference distance for reducing volume as source moves further from the listener. The default value is 1.'
tags:
  - API_Object_Properties
  - API
  - WebAudio
uri: apis/webaudio/PannerNode/refDistance

---
## Summary

A reference distance for reducing volume as source moves further from the listener. The default value is 1.

Property of [apis/webaudio/PannerNode](/apis/webaudio/PannerNode)[apis/webaudio/PannerNode](/apis/webaudio/PannerNode)

## Syntax

``` js
var result = PannerNode.refDistance;
PannerNode.refDistance = value;
```

## Return Value

Returns an object of type NumberNumber

## Examples

``` js
var audioCtx = new AudioContext();
var panner = audioCtx.createPanner();
panner.refDistance = 1;
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
