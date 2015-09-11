---
title: AudioBuffer
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'This interface represents a memory-resident audio asset, primarily for one-shot sounds and other short audio clips. Its format is non-interleaved IEEE 32-bit linear PCM with a nominal range of -1 -&gt; +1. It can contain one or more channels.'
tags:
  0: API
  1: Objects
  3: WebAudio
uri: apis/webaudio/AudioBuffer

---
## <span>Summary</span>

This interface represents a memory-resident audio asset, primarily for one-shot sounds and other short audio clips. Its format is non-interleaved IEEE 32-bit linear PCM with a nominal range of -1 -&gt; +1. It can contain one or more channels.

## <span>Properties</span>

API Name
:   Summary

[duration](/apis/webaudio/AudioBuffer/duration)
:   Duration, in seconds, of the PCM audio data in the buffer.

[length](/apis/webaudio/AudioBuffer/length)
:   Length, in sample-frames, of the PCM audio data.

[numberOfChannels](/apis/webaudio/AudioBuffer/numberOfChannels)
:   The number of discrete audio channels described by the PCM audio data.

[sampleRate](/apis/webaudio/AudioBuffer/sampleRate)
:   The sample rate, in samples per second, for the PCM audio data.

## <span>Methods</span>

API Name
:   Summary

[getChannelData](/apis/webaudio/AudioBuffer/getChannelData)
:   Returns the **Float32Array** representing the PCM audio data for the specific channel.

## <span>Events</span>

*No events.*

## <span>Related specifications</span>

[W3C Web Audio API](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html)
:   W3C Editor's Draft
