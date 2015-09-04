---
title: setPosition
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Sets the position of the listener in a 3D cartesian coordinate space. PannerNode objects use this position relative to individual audio sources for spatialization. The x, y, z parameters represent the coordinates in 3D space. The default value is (0,0,0).'
uri: apis/webaudio/AudioListener/setPosition

---
# setPosition

## Summary

Sets the position of the listener in a 3D cartesian coordinate space. PannerNode objects use this position relative to individual audio sources for spatialization. The x, y, z parameters represent the coordinates in 3D space. The default value is (0,0,0).

*Method of [apis/webaudio/AudioListener](/apis/webaudio/AudioListener)*

## Syntax

``` {.js}
var  = AudioListener.setPosition(x, y, z);
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
var myListener = audioCtx.listener;
myListener.setPosition(1,1,1);
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

