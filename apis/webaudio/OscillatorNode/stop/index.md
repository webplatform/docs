---
title: stop
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Schedules a sound to stop playback at an exact time.'
uri: apis/webaudio/OscillatorNode/stop

---
# stop

## Summary

Schedules a sound to stop playback at an exact time.

*Method of [apis/webaudio/OscillatorNode](/apis/webaudio/OscillatorNode)*

## Syntax

``` {.js}
var  = OscillatorNode.stop(when);
```

## Parameters

### when

 Data-typeÂ
:   Number

 Describes at what time (in seconds) the sound should stop playing. It is in the same time coordinate system as [**AudioContext.currentTime**](/apis/webaudio/AudioContext/currentTime). If 0 is passed in for this value or if the value is less than **currentTime**, then the sound will stop playing immediately. stop must only be called one time and only after a call to start or stop, or an exception will be thrown.

## Return Value

Returns an object of type .

## Examples

``` {.js}
var oscillator = audioCtx.createOscillator();
oscillator.type = 'square';
oscillator.frequency.value = 3000; // value in hertz
oscillator.start();
oscillator.stop(2); // stop after 2 seconds
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

