---
title: ScriptProcessorNode
tags:
  0: API
  1: Objects
  3: WebAudio
readiness: 'Out of Date'
standardization_status: 'W3C Editor''s Draft'
notes:
  - 'Deprecated; deletion candidate. See http://webaudio.github.io/web-audio-api/.'
summary: "This interface is an AudioNode which can generate, process, or analyse audio directly using JavaScript.\n"
uri: apis/webaudio/ScriptProcessorNode

---
# ScriptProcessorNode

## Summary

This interface is an AudioNode which can generate, process, or analyse audio directly using JavaScript.

**Deprecated; deletion candidate. See [http://webaudio.github.io/web-audio-api/](http://webaudio.github.io/web-audio-api/).**

## Properties

API Name
:   Summary
[bufferSize](/apis/webaudio/ScriptProcessorNode/bufferSize)
:   The size of the buffer (in sample-frames) which needs to be processed each time [**onaudioprocess**](/apis/webaudio/ScriptProcessorNode/onaudioprocess) is called. Legal values are 256, 512, 1024, 2048, 4096, 8192, and 16384.

    **Deprecated; deletion candidate. See [http://webaudio.github.io/web-audio-api/](http://webaudio.github.io/web-audio-api/).**

[onaudioprocess](/apis/webaudio/ScriptProcessorNode/onaudioprocess)
:   An event listener which is called periodically for audio processing. An event of type [**AudioProcessingEvent**](/apis/webaudio/AudioProcessingEvent) will be passed to the event handler.

    **Deprecated; deletion candidate. See [http://webaudio.github.io/web-audio-api/](http://webaudio.github.io/web-audio-api/).**

## Methods

*No methods.*

## Events

*No events.*

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

