---
title: stop
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/webaudio/AudioBufferSourceNode
    href: /apis/webaudio/AudioBufferSourceNode
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/webaudio/AudioBufferSourceNode
standardization_status: 'W3C Editor''s Draft'
summary: 'Schedules a sound to stop playback at an exact time, with options.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioBufferSourceNode/stop

---
## <span>Summary</span>

Schedules a sound to stop playback at an exact time, with options.

Method of [apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)[apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)

## <span>Syntax</span>

``` js
var  = AudioBufferSourceNode.stop(when);
```

## <span>Parameters</span>

### <span>when</span>

 Data-type
:   Number

 Describes at what time (in seconds) the sound should stop playing. It is in the same time coordinate system as [**AudioContext.currentTime**](/apis/webaudio/AudioContext/currentTime). If 0 is passed in for this value or if the value is less than **currentTime**, then the sound will stop playing immediately. stop must only be called one time and only after a call to start or stop, or an exception will be thrown.

## <span>Return Value</span>

Returns an object of type<span></span>

## <span>Examples</span>

Stop playing the sound immediately.

``` js
var source = audioCtx.createBufferSource();
source.stop();
```

Stop playing the sound after 3 seconds.

``` js
var source = audioCtx.createBufferSource();
source.stop(3);
```

## <span>Related specifications</span>

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
