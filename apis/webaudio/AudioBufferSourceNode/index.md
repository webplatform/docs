---
title: 'AudioBufferSourceNode'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'This interface represents an audio source from an in-memory audio asset in an AudioBuffer. It generally will be used for short audio assets which require a high degree of scheduling flexibility (can playback in rhythmically perfect ways).'
tags:
  - API_Objects
  - API
  - WebAudio
uri: apis/webaudio/AudioBufferSourceNode

---
## Summary

This interface represents an audio source from an in-memory audio asset in an AudioBuffer. It generally will be used for short audio assets which require a high degree of scheduling flexibility (can playback in rhythmically perfect ways).

## Properties

[buffer](/apis/webaudio/AudioBufferSourceNode/buffer)
:   Represents the audio asset to be played.

[loop](/apis/webaudio/AudioBufferSourceNode/loop)
:   Indicates if the audio data should play in a loop. The default value is false.

[loopEnd](/apis/webaudio/AudioBufferSourceNode/loopEnd)
:   An optional value in seconds where looping should end if the loop attribute is true. Its default value is 0, and it may usefully be set to any value between 0 and the duration of the buffer.

[loopStart](/apis/webaudio/AudioBufferSourceNode/loopStart)
:   An optional value in seconds where looping should begin if the loop attribute is true. Its default value is 0, and it may usefully be set to any value between 0 and the duration of the buffer.

[playbackRate](/apis/webaudio/AudioBufferSourceNode/playbackRate)
:   The speed at which to render the audio stream. The default [playbackRate](/apis/webaudio/AudioBufferSourceNode/playbackRate) value is 1. This parameter is a-rate.

[playbackState](/apis/webaudio/AudioBufferSourceNode/playbackState)
:   The playback state, initialized to UNSCHEDULED\_STATE, progressing through SCHEDULED\_STATE, PLAYING\_STATE, and FINISHED\_STATE.

## Methods

[start](/apis/webaudio/AudioBufferSourceNode/start)
:   Schedules a sound to playback at an exact time, with options.

[stop](/apis/webaudio/AudioBufferSourceNode/stop)
:   Schedules a sound to stop playback at an exact time, with options.

## Events

*No events.*

## Related specifications

[W3C Web Audio API](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html)
:   W3C Editor's Draft
