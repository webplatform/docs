---
title: playbackTime
notes:
  - 'Deprecated; deletion candidate. See http://webaudio.github.io/web-audio-api/.'
readiness: 'Out of Date'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/AudioProcessingEvent
    href: /apis/webaudio/AudioProcessingEvent
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /apis/webaudio/AudioProcessingEvent
standardization_status: 'W3C Editor''s Draft'
summary: "The time when the audio will be played, in the same time coordinate system as AudioContext.currentTime. playbackTime allows for very tight synchronization between processing directly in JavaScript with the other events in the context's rendering graph.\n"
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AudioProcessingEvent/playbackTime

---
## <span>Summary</span>

The time when the audio will be played, in the same time coordinate system as AudioContext.currentTime. playbackTime allows for very tight synchronization between processing directly in JavaScript with the other events in the context's rendering graph.

**Deprecated; deletion candidate. See <http://webaudio.github.io/web-audio-api/>.**

Property of [apis/webaudio/AudioProcessingEvent](/apis/webaudio/AudioProcessingEvent)[apis/webaudio/AudioProcessingEvent](/apis/webaudio/AudioProcessingEvent)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = AudioProcessingEvent.playbackTime;
```

## <span>Return Value</span>

Returns an object of type NumberNumber

**Needs Examples**: This section should include examples.

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
