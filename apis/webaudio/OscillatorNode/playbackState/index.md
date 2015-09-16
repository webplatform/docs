---
title: playbackState
notes:
  - 'Not in spec; deletion candidate. See http://webaudio.github.io/web-audio-api/.'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/OscillatorNode
    href: /apis/webaudio/OscillatorNode
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned short'
    href: /apis/webaudio/OscillatorNode
standardization_status: 'W3C Editor''s Draft'
summary: "The playback state, initialized to UNSCHEDULED_STATE, progressing through SCHEDULED_STATE, PLAYING_STATE, and FINISHED_STATE.\n"
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/OscillatorNode/playbackState

---
## Summary

The playback state, initialized to UNSCHEDULED\_STATE, progressing through SCHEDULED\_STATE, PLAYING\_STATE, and FINISHED\_STATE.

**Not in spec; deletion candidate. See <http://webaudio.github.io/web-audio-api/>.**

Property of [apis/webaudio/OscillatorNode](/apis/webaudio/OscillatorNode)[apis/webaudio/OscillatorNode](/apis/webaudio/OscillatorNode)

## Syntax

**Note**: This property is read-only.

``` js
var result = OscillatorNode.playbackState;
```

## Return Value

Returns an object of type unsigned shortunsigned short

Returns one of the following constant values: UNSCHEDULED\_STATE (0), SCHEDULED\_STATE (1), PLAYING\_STATE (2), or FINISHED\_STATE (3).

**Needs Examples**: This section should include examples.

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
