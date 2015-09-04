---
title: setVelocity
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Sets the velocity vector of the audio source. This vector controls both the direction of travel and the speed in 3D space. This velocity relative to the listener''s velocity is used to determine how much doppler shift (pitch change) to apply. The x, y, and z parameters describe a direction vector indicating direction of travel and intensity. The default value is (0,0,0).'
uri: apis/webaudio/PannerNode/setVelocity

---
# setVelocity

## Summary

Sets the velocity vector of the audio source. This vector controls both the direction of travel and the speed in 3D space. This velocity relative to the listener's velocity is used to determine how much doppler shift (pitch change) to apply. The x, y, and z parameters describe a direction vector indicating direction of travel and intensity. The default value is (0,0,0).

*Method of [apis/webaudio/PannerNode](/apis/webaudio/PannerNode)*

## Syntax

``` {.js}
var  = PannerNode.setVelocity(x, y, z);
```

## Parameters

### x

 Data-typeÂ
:   Number

### y

 Data-typeÂ
:   Number

### z

 Data-typeÂ
:   Number

## Return Value

Returns an object of type Number.

## Examples

``` {.js}
var audioCtx = new AudioContext();
var panner = audioCtx.createPanner();
panner.setVelocity(0,0,17);
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

