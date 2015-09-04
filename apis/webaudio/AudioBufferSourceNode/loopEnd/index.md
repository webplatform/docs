---
title: loopEnd
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'An optional value in seconds where looping should end if the loop attribute is true. Its default value is 0, and it may usefully be set to any value between 0 and the duration of the buffer.'
uri: apis/webaudio/AudioBufferSourceNode/loopEnd

---
# loopEnd

## Summary

An optional value in seconds where looping should end if the loop attribute is true. Its default value is 0, and it may usefully be set to any value between 0 and the duration of the buffer.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)</span></span>

## Syntax

``` {.js}
var result = AudioBufferSourceNode.loopEnd;
AudioBufferSourceNode.loopEnd = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.js}
var source = audioCtx.createBufferSource();
source.loopEnd = 3;
```

## Related specifications

Specification
:   Status
[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

