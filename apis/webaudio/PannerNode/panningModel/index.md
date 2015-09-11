---
title: panningModel
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
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/PannerNode/panningModel

---
## <span>Summary</span>

Determines which spatialization algorithm will be used to position the audio in 3D space. See below for the available choices. The default is HRTF.

Property of [apis/webaudio/PannerNode](/apis/webaudio/PannerNode)[apis/webaudio/PannerNode](/apis/webaudio/PannerNode)

## <span>Syntax</span>

``` js
var result = PannerNode.panningModel;
PannerNode.panningModel = value;
```

## <span>Return Value</span>

Returns an object of type unsigned shortunsigned short

Uses one of the following constant values:

-   EQUALPOWER (0), a simple and efficient spatialization algorithm using equal-power panning;
-   HTRF (1) (default), a higher quality spatialization algorithm using a convolution with measured impulse responses from human subjects, which renders stereo output

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var panner = audioCtx.createPanner();
panner.panningModel = 'HRTF';
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
