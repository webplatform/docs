---
title: duration
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Duration, in seconds, of the PCM audio data in the buffer.'
uri: apis/webaudio/AudioBuffer/duration

---
# duration

## Summary

Duration, in seconds, of the PCM audio data in the buffer.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioBuffer](/apis/webaudio/AudioBuffer)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = AudioBuffer.duration;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.js}
var myArrayBuffer = audioCtx.createBuffer(2, frameCount, audioCtx.sampleRate);
var dur = myArrayBuffer.duration;
```

## Related specifications

Specification
:   Status
[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

