---
title: 'stop'
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
  - API_Object_Methods
  - API
  - WebAudio
uri: apis/webaudio/AudioBufferSourceNode/stop

---
## Summary

Schedules a sound to stop playback at an exact time, with options.

Method of [apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)[apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)

## Syntax

``` js
var  = AudioBufferSourceNode.stop(when);
```

## Parameters

### when

 Data-type
:   Number

 Describes at what time (in seconds) the sound should stop playing. It is in the same time coordinate system as [**AudioContext.currentTime**](/apis/webaudio/AudioContext/currentTime). If 0 is passed in for this value or if the value is less than **currentTime**, then the sound will stop playing immediately. stop must only be called one time and only after a call to start or stop, or an exception will be thrown.

## Return Value

Returns an object of type

## Examples

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

## Related specifications

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
