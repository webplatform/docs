---
title: loop
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Indicates if the audio data should play in a loop. The default value is false.'
uri: apis/webaudio/AudioBufferSourceNode/loop

---
# loop

## Summary

Indicates if the audio data should play in a loop. The default value is false.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)</span></span>

## Syntax

``` {.js}
var result = AudioBufferSourceNode.loop;
AudioBufferSourceNode.loop = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

## Examples

``` {.js}
var source = audioCtx.createBufferSource();
source.loop = true;
```

## Related specifications

Specification
:   Status
[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

