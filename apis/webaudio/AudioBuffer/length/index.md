---
title: length
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Length, in sample-frames, of the PCM audio data.'
uri: apis/webaudio/AudioBuffer/length

---
# length

## Summary

Length, in sample-frames, of the PCM audio data.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioBuffer](/apis/webaudio/AudioBuffer)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = AudioBuffer.length;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

## Examples

``` {.js}
var myArrayBuffer = audioCtx.createBuffer(2, frameCount, audioCtx.sampleRate);
var len = myArrayBuffer.length;
```

## Related specifications

Specification
:   Status
[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

