---
title: setOrientation
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
notes:
  - Needsexample
summary: 'Describes which direction the audio source is pointing in the 3D cartesian coordinate space. Depending on how directional the sound is (controlled by the cone attributes), a sound pointing away from the listener can be very quiet or completely silent. The x, y, and z parameters represent a direction vector in 3D space. The default value is (1,0,0).'
uri: apis/webaudio/PannerNode/setOrientation

---
# setOrientation

## Summary

Describes which direction the audio source is pointing in the 3D cartesian coordinate space. Depending on how directional the sound is (controlled by the cone attributes), a sound pointing away from the listener can be very quiet or completely silent. The x, y, and z parameters represent a direction vector in 3D space. The default value is (1,0,0).

*Method of [apis/webaudio/PannerNode](/apis/webaudio/PannerNode)*

## Syntax

``` {.js}
var  = PannerNode.setOrientation(x, y, z);
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
panner.setOrientation(1,0,0);
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

