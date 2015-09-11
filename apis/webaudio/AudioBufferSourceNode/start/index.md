---
title: start
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
summary: 'Schedules a sound to playback at an exact time, with options.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioBufferSourceNode/start

---
## <span>Summary</span>

Schedules a sound to playback at an exact time, with options.

Method of [apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)[apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)

## <span>Syntax</span>

``` js
var  = AudioBufferSourceNode.start(when, offset, duration);
```

## <span>Parameters</span>

### <span>when</span>

 Data-type
:   Number

 Describes at what time (in seconds) the sound should start playing. It is in the same time coordinate system as [**AudioContext.currentTime**](/apis/webaudio/AudioContext/currentTime). If 0 is passed in for this value or if the value is less than **currentTime**, then the sound will start playing immediately. start may only be called one time and must be called before stop is called or an exception will be thrown.

### <span>offset</span>

 Data-type
:   Number

(Optional)

Describes the offset time in the buffer (in seconds) where playback will begin. This parameter is optional with a default value of 0 (playing back from the beginning of the buffer).

### <span>duration</span>

 Data-type
:   Number

(Optional)

Describes the duration of the portion (in seconds) to be played. This parameter is optional, with the default value equal to the total duration of the [**AudioBuffer**](/apis/webaudio/AudioBuffer) minus the offset parameter. Thus if neither offset nor duration are specified then the implied duration is the total duration of the [**AudioBuffer**](/apis/webaudio/AudioBuffer).

## <span>Return Value</span>

Returns an object of type<span></span>

## <span>Examples</span>

Play the entire sound from the beginning.

``` js
var source = audioCtx.createBufferSource();
source.start();
```

Play, after a 1 second delay, starting at second 3, the next 10 seconds of the sound (seconds 3 through 12).

``` js
var source = audioCtx.createBufferSource();
source.start(1,3,10);
```

## <span>Related specifications</span>

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
