---
title: playbackTime
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Out of Date'
standardization_status: 'W3C Editor''s Draft'
notes:
  - 'Deprecated; deletion candidate. See http://webaudio.github.io/web-audio-api/.'
summary: "The time when the audio will be played, in the same time coordinate system as AudioContext.currentTime. playbackTime allows for very tight synchronization between processing directly in JavaScript with the other events in the context's rendering graph.\n"
uri: apis/webaudio/AudioProcessingEvent/playbackTime

---
# playbackTime

## Summary

The time when the audio will be played, in the same time coordinate system as AudioContext.currentTime. playbackTime allows for very tight synchronization between processing directly in JavaScript with the other events in the context's rendering graph.

**Deprecated; deletion candidate. See [http://webaudio.github.io/web-audio-api/](http://webaudio.github.io/web-audio-api/).**

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioProcessingEvent](/apis/webaudio/AudioProcessingEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = AudioProcessingEvent.playbackTime;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

