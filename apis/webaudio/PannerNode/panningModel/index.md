---
title: panningModel
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Determines which spatialization algorithm will be used to position the audio in 3D space. See below for the available choices. The default is HRTF.'
uri: apis/webaudio/PannerNode/panningModel

---
# panningModel

## Summary

Determines which spatialization algorithm will be used to position the audio in 3D space. See below for the available choices. The default is HRTF.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/PannerNode](/apis/webaudio/PannerNode)</span></span>

## Syntax

``` {.js}
var result = PannerNode.panningModel;
PannerNode.panningModel = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned short</span></span>

Uses one of the following constant values:

-   EQUALPOWER (0), a simple and efficient spatialization algorithm using equal-power panning;
-   HTRF (1) (default), a higher quality spatialization algorithm using a convolution with measured impulse responses from human subjects, which renders stereo output

## Examples

``` {.js}
var audioCtx = new AudioContext();
var panner = audioCtx.createPanner();
panner.panningModel = 'HRTF';
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

