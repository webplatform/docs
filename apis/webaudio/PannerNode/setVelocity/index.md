---
title: setVelocity
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
summary: 'Sets the velocity vector of the audio source. This vector controls both the direction of travel and the speed in 3D space. This velocity relative to the listener''s velocity is used to determine how much doppler shift (pitch change) to apply. The x, y, and z parameters describe a direction vector indicating direction of travel and intensity. The default value is (0,0,0).'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/PannerNode/setVelocity

---
## <span>Summary</span>

Sets the velocity vector of the audio source. This vector controls both the direction of travel and the speed in 3D space. This velocity relative to the listener's velocity is used to determine how much doppler shift (pitch change) to apply. The x, y, and z parameters describe a direction vector indicating direction of travel and intensity. The default value is (0,0,0).

Method of [apis/webaudio/PannerNode](/apis/webaudio/PannerNode)[apis/webaudio/PannerNode](/apis/webaudio/PannerNode)

## <span>Syntax</span>

``` js
var  = PannerNode.setVelocity(x, y, z);
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
panner.setVelocity(0,0,17);
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
