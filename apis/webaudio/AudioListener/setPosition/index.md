---
title: setPosition
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/webaudio/AudioListener
    href: /apis/webaudio/AudioListener
  return_type:
    predicate: 'Returns an object of type  '
    value: Number
    href: /apis/webaudio/AudioListener
standardization_status: 'W3C Editor''s Draft'
summary: 'Sets the position of the listener in a 3D cartesian coordinate space. PannerNode objects use this position relative to individual audio sources for spatialization. The x, y, z parameters represent the coordinates in 3D space. The default value is (0,0,0).'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioListener/setPosition

---
## <span>Summary</span>

Sets the position of the listener in a 3D cartesian coordinate space. PannerNode objects use this position relative to individual audio sources for spatialization. The x, y, z parameters represent the coordinates in 3D space. The default value is (0,0,0).

Method of [apis/webaudio/AudioListener](/apis/webaudio/AudioListener)[apis/webaudio/AudioListener](/apis/webaudio/AudioListener)

## <span>Syntax</span>

``` js
var  = AudioListener.setPosition(x, y, z);
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
var myListener = audioCtx.listener;
myListener.setPosition(1,1,1);
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
