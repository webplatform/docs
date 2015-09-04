---
title: setPosition
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Sets the position of the audio source relative to the listener attribute. A 3D cartesian coordinate system is used. The x, y, and z parameters represent the coordinates in 3D space. The default value is (0,0,0).'
uri: apis/webaudio/PannerNode/setPosition

---
# setPosition

## Summary

Sets the position of the audio source relative to the listener attribute. A 3D cartesian coordinate system is used. The x, y, and z parameters represent the coordinates in 3D space. The default value is (0,0,0).

*Method of [apis/webaudio/PannerNode](/apis/webaudio/PannerNode)*

## Syntax

``` {.js}
var  = PannerNode.setPosition(x, y, z);
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
panner.setPosition(0,0,0);
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

