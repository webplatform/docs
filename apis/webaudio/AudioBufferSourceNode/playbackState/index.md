---
title: 'playbackState'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/AudioBufferSourceNode
    href: /apis/webaudio/AudioBufferSourceNode
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned short'
    href: /apis/webaudio/AudioBufferSourceNode
standardization_status: 'W3C Editor''s Draft'
summary: 'The playback state, initialized to UNSCHEDULED_STATE, progressing through SCHEDULED_STATE, PLAYING_STATE, and FINISHED_STATE.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AudioBufferSourceNode/playbackState

---
## Summary

The playback state, initialized to UNSCHEDULED\_STATE, progressing through SCHEDULED\_STATE, PLAYING\_STATE, and FINISHED\_STATE.

Property of [apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)[apis/webaudio/AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)

## Syntax

**Note**: This property is read-only.

``` js
var result = AudioBufferSourceNode.playbackState;
```

## Return Value

Returns an object of type unsigned shortunsigned short

Returns one of the following constant values: UNSCHEDULED\_STATE (0), SCHEDULED\_STATE (1), PLAYING\_STATE (2), or FINISHED\_STATE (3).

## Examples

``` js
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

[W3C Web Audio API](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html)
:   W3C Editor's Draft
