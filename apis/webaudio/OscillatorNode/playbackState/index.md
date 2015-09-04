---
title: playbackState
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Not Ready'
standardization_status: 'W3C Editor''s Draft'
notes:
  - 'Not in spec; deletion candidate. See http://webaudio.github.io/web-audio-api/.'
summary: "The playback state, initialized to UNSCHEDULED_STATE, progressing through SCHEDULED_STATE, PLAYING_STATE, and FINISHED_STATE.\n"
uri: apis/webaudio/OscillatorNode/playbackState

---
# playbackState

## Summary

The playback state, initialized to UNSCHEDULED\_STATE, progressing through SCHEDULED\_STATE, PLAYING\_STATE, and FINISHED\_STATE.

**Not in spec; deletion candidate. See [http://webaudio.github.io/web-audio-api/](http://webaudio.github.io/web-audio-api/).**

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/OscillatorNode](/apis/webaudio/OscillatorNode)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = OscillatorNode.playbackState;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned short</span></span>

Returns one of the following constant values: UNSCHEDULED\_STATE (0), SCHEDULED\_STATE (1), PLAYING\_STATE (2), or FINISHED\_STATE (3).

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

