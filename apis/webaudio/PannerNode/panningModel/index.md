---
title: 'panningModel'
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
summary: 'Determines which spatialization algorithm will be used to position the audio in 3D space. See below for the available choices. The default is HRTF.'
tags:
  - API_Object_Properties
  - API
  - WebAudio
uri: apis/webaudio/PannerNode/panningModel

---
## Summary

Determines which spatialization algorithm will be used to position the audio in 3D space. See below for the available choices. The default is HRTF.

Property of [apis/webaudio/PannerNode](/apis/webaudio/PannerNode)[apis/webaudio/PannerNode](/apis/webaudio/PannerNode)

## Syntax

``` js
var result = PannerNode.panningModel;
PannerNode.panningModel = value;
```

## Return Value

Returns an object of type unsigned shortunsigned short

Uses one of the following constant values:

-   EQUALPOWER (0), a simple and efficient spatialization algorithm using equal-power panning;
-   HTRF (1) (default), a higher quality spatialization algorithm using a convolution with measured impulse responses from human subjects, which renders stereo output

## Examples

``` js
var audioCtx = new AudioContext();
var panner = audioCtx.createPanner();
panner.panningModel = 'HRTF';
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
