---
title: stop
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/webaudio/OscillatorNode
    href: /apis/webaudio/OscillatorNode
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/webaudio/OscillatorNode
standardization_status: 'W3C Editor''s Draft'
summary: 'Schedules a sound to stop playback at an exact time.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/OscillatorNode/stop

---
## <span>Summary</span>

Schedules a sound to stop playback at an exact time.

Method of [apis/webaudio/OscillatorNode](/apis/webaudio/OscillatorNode)[apis/webaudio/OscillatorNode](/apis/webaudio/OscillatorNode)

## <span>Syntax</span>

``` js
var  = OscillatorNode.stop(when);
```

## <span>Parameters</span>

### <span>when</span>

 Data-type
:   Number

 Describes at what time (in seconds) the sound should stop playing. It is in the same time coordinate system as [**AudioContext.currentTime**](/apis/webaudio/AudioContext/currentTime). If 0 is passed in for this value or if the value is less than **currentTime**, then the sound will stop playing immediately. stop must only be called one time and only after a call to start or stop, or an exception will be thrown.

## <span>Return Value</span>

Returns an object of type<span></span>

## <span>Examples</span>

``` js
var oscillator = audioCtx.createOscillator();
oscillator.type = 'square';
oscillator.frequency.value = 3000; // value in hertz
oscillator.start();
oscillator.stop(2); // stop after 2 seconds
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
