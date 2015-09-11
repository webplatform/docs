---
title: setVelocity
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
summary: 'Sets the velocity vector of the listener. This vector controls both the direction of travel and the speed in 3D space. This velocity relative an audio source''s velocity is used to determine how much doppler shift (pitch change) to apply. The x, y, z parameters describe a direction vector indicating direction of travel and intensity. The default value is (0,0,0).'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioListener/setVelocity

---
## <span>Summary</span>

Sets the velocity vector of the listener. This vector controls both the direction of travel and the speed in 3D space. This velocity relative an audio source's velocity is used to determine how much doppler shift (pitch change) to apply. The x, y, z parameters describe a direction vector indicating direction of travel and intensity. The default value is (0,0,0).

Method of [apis/webaudio/AudioListener](/apis/webaudio/AudioListener)[apis/webaudio/AudioListener](/apis/webaudio/AudioListener)

## <span>Syntax</span>

``` js
var  = AudioListener.setVelocity(x, y, z);
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
myListener.setVelocity(0,0,0);
```

## <span>Related specifications</span>

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's draft
