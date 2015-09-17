---
title: 'ScriptProcessorNode'
notes:
  - 'Deprecated; deletion candidate. See http://webaudio.github.io/web-audio-api/.'
readiness: 'Out of Date'
standardization_status: 'W3C Editor''s Draft'
summary: "This interface is an AudioNode which can generate, process, or analyse audio directly using JavaScript.\n"
tags:
  - API_Objects
  - API
  - WebAudio
uri: apis/webaudio/ScriptProcessorNode

---
## Summary

This interface is an AudioNode which can generate, process, or analyse audio directly using JavaScript.

**Deprecated; deletion candidate. See <http://webaudio.github.io/web-audio-api/>.**

## Properties

[bufferSize](/apis/webaudio/ScriptProcessorNode/bufferSize)
:   The size of the buffer (in sample-frames) which needs to be processed each time [**onaudioprocess**](/apis/webaudio/ScriptProcessorNode/onaudioprocess) is called. Legal values are 256, 512, 1024, 2048, 4096, 8192, and 16384.

    **Deprecated; deletion candidate. See <http://webaudio.github.io/web-audio-api/>.**

[onaudioprocess](/apis/webaudio/ScriptProcessorNode/onaudioprocess)
:   An event listener which is called periodically for audio processing. An event of type [**AudioProcessingEvent**](/apis/webaudio/AudioProcessingEvent) will be passed to the event handler.

    **Deprecated; deletion candidate. See <http://webaudio.github.io/web-audio-api/>.**

## Methods

*No methods.*

## Events

*No events.*

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
