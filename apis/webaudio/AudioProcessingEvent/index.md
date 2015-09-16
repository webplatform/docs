---
title: AudioProcessingEvent
notes:
  - 'Deprecated; deletion candidate. See http://webaudio.github.io/web-audio-api/.'
readiness: 'Out of Date'
standardization_status: 'W3C Editor''s Draft'
summary: "This interface is a type of Event which is passed to the onaudioprocess event handler used by ScriptProcessorNode. The event handler processes audio from the input (if any) by accessing the audio data from the inputBuffer attribute. The audio data which is the result of the processing (or the synthesized data if there are no inputs) is then placed into the outputBuffer.\n"
tags:
  0: API
  1: Objects
  3: WebAudio
uri: apis/webaudio/AudioProcessingEvent

---
## Summary

This interface is a type of Event which is passed to the onaudioprocess event handler used by ScriptProcessorNode. The event handler processes audio from the input (if any) by accessing the audio data from the inputBuffer attribute. The audio data which is the result of the processing (or the synthesized data if there are no inputs) is then placed into the outputBuffer.

**Deprecated; deletion candidate. See <http://webaudio.github.io/web-audio-api/>.**

## Properties

API Name
:   Summary

[inputBuffer](/apis/webaudio/AudioProcessingEvent/inputBuffer)
:   An [**AudioBuffer**](/apis/webaudio/AudioBuffer) containing the input audio data. It will have a number of channels equal to the **numberOfInputChannels** parameter of the [**createScriptProcessor()**](/apis/webaudio/AudioContext/createScriptProcessor) method. This [**AudioBuffer**](/apis/webaudio/AudioBuffer) is only valid while in the scope of the [**onaudioprocess**](/apis/webaudio/ScriptProcessorNode/onaudioprocess) function. Its values will be meaningless outside of this scope.

    **Deprecated; deletion candidate. See <http://webaudio.github.io/web-audio-api/>.**

[node](/apis/webaudio/AudioProcessingEvent/node)
:   The [**ScriptProcessorNode**](/apis/webaudio/ScriptProcessorNode) associated with this processing event.

    **Deprecated; deletion candidate. See <http://webaudio.github.io/web-audio-api/>.**

[outputBuffer](/apis/webaudio/AudioProcessingEvent/outputBuffer)
:   An [**AudioBuffer**](/apis/webaudio/AudioBuffer) where the output audio data should be written. It will have a number of channels equal to the **numberOfOutputChannels** parameter of the [**createScriptProcessor()**](/apis/webaudio/AudioContext/createScriptProcessor) method. Script code within the scope of the [**onaudioprocess**](/apis/webaudio/ScriptProcessorNode/onaudioprocess) function is expected to modify the **Float32Array** arrays representing channel data in this [**AudioBuffer**](/apis/webaudio/AudioBuffer). Any script modifications to this [**AudioBuffer**](/apis/webaudio/AudioBuffer) outside of this scope will not produce any audible effects.

    **Deprecated; deletion candidate. See <http://webaudio.github.io/web-audio-api/>.**

[playbackTime](/apis/webaudio/AudioProcessingEvent/playbackTime)
:   The time when the audio will be played, in the same time coordinate system as [**AudioContext.currentTime**](/apis/webaudio/AudioContext/currentTime). [**playbackTime**](/apis/webaudio/AudioProcessingEvent/playbackTime) allows for very tight synchronization between processing directly in JavaScript with the other events in the context's rendering graph.

    **Deprecated; deletion candidate. See <http://webaudio.github.io/web-audio-api/>.**

## Methods

*No methods.*

## Events

*No events.*

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
