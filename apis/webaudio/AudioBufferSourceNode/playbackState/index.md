---
title: playbackState
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The playback state, initialized to UNSCHEDULED_STATE, progressing through SCHEDULED_STATE, PLAYING_STATE, and FINISHED_STATE.'
uri: apis/webaudio/AudioBufferSourceNode/playbackState

---
# playbackState

## Summary

The playback state, initialized to UNSCHEDULED\_STATE, progressing through SCHEDULED\_STATE, PLAYING\_STATE, and FINISHED\_STATE.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = AudioBufferSourceNode.playbackState;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned short</span></span>

Returns one of the following constant values: UNSCHEDULED\_STATE (0), SCHEDULED\_STATE (1), PLAYING\_STATE (2), or FINISHED\_STATE (3).

## Examples

``` {.js}
// 1. Create an AudioBufferSourceNode and load data into it
var soundSource = …

// 2. Check to see if the sound has finished playing, once per second
var timer = setInterval(function() {
  if (soundSource.playbackState == soundSource.FINISHED_STATE) {
    console.log("The sound has finished playing.");
    clearInterval(timer);
  }
}, 1000);

// 3. Play the sound
soundSource.start(…);
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html)
:   W3C Editor's Draft

