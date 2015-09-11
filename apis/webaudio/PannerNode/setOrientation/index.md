---
title: setOrientation
notes:
  - Needsexample
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/webaudio/PannerNode
    href: /apis/webaudio/PannerNode
  return_type:
    predicate: 'Returns an object of type  '
    value: Number
    href: /apis/webaudio/PannerNode
standardization_status: 'W3C Editor''s Draft'
summary: 'Describes which direction the audio source is pointing in the 3D cartesian coordinate space. Depending on how directional the sound is (controlled by the cone attributes), a sound pointing away from the listener can be very quiet or completely silent. The x, y, and z parameters represent a direction vector in 3D space. The default value is (1,0,0).'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/PannerNode/setOrientation

---
## <span>Summary</span>

Describes which direction the audio source is pointing in the 3D cartesian coordinate space. Depending on how directional the sound is (controlled by the cone attributes), a sound pointing away from the listener can be very quiet or completely silent. The x, y, and z parameters represent a direction vector in 3D space. The default value is (1,0,0).

Method of [apis/webaudio/PannerNode](/apis/webaudio/PannerNode)[apis/webaudio/PannerNode](/apis/webaudio/PannerNode)

## <span>Syntax</span>

``` js
var  = PannerNode.setOrientation(x, y, z);
```

## <span>Parameters</span>

### <span>x</span>

 Data-type
:   Number

### <span>y</span>

 Data-type
:   Number

### <span>z</span>

 Data-type
:   Number

## <span>Return Value</span>

Returns an object of type NumberNumber

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var panner = audioCtx.createPanner();
panner.setOrientation(1,0,0);
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
