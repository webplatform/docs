---
title: OscillatorNode
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'OscillatorNode represents an audio source generating a periodic waveform. It can be set to a few commonly used waveforms. Additionally, it can be set to an arbitrary periodic waveform through the use of a WaveTable object. Oscillators are common foundational building blocks in audio synthesis.'
tags:
  0: API
  1: Objects
  3: WebAudio
uri: apis/webaudio/OscillatorNode

---
## <span>Summary</span>

OscillatorNode represents an audio source generating a periodic waveform. It can be set to a few commonly used waveforms. Additionally, it can be set to an arbitrary periodic waveform through the use of a WaveTable object. Oscillators are common foundational building blocks in audio synthesis.

## <span>Properties</span>

API Name
:   Summary

[detune](/apis/webaudio/OscillatorNode/detune)
:   A detuning value (in cents) which will offset the frequency by the given amount. This parameter is a-rate.

[frequency](/apis/webaudio/OscillatorNode/frequency)
:   The frequency (in Hertz) of the periodic waveform. This parameter is a-rate.

[playbackState](/apis/webaudio/OscillatorNode/playbackState)
:   The playback state, initialized to UNSCHEDULED\_STATE, progressing through SCHEDULED\_STATE, PLAYING\_STATE, and FINISHED\_STATE.

    **Not in spec; deletion candidate. See <http://webaudio.github.io/web-audio-api/>.**

[type](/apis/webaudio/OscillatorNode/type)
:   The shape of the periodic waveform. It may directly be set to any of the type constant values except for CUSTOM. The [**setWaveTable()**](/apis/webaudio/OscillatorNode/setWaveTable) method can be used to set a custom waveform, which results in this attribute being set to CUSTOM.

## <span>Methods</span>

API Name
:   Summary

[setWaveTable](/apis/webaudio/OscillatorNode/setWaveTable)
:   Sets an arbitrary custom periodic waveform given a [**WaveTable**](/apis/webaudio/WaveTable).

    **Not in spec; deletion candidate. See <http://webaudio.github.io/web-audio-api/>.**

[start](/apis/webaudio/OscillatorNode/start)
:   Schedules a sound to playback at an exact time.

[stop](/apis/webaudio/OscillatorNode/stop)
:   Schedules a sound to stop playback at an exact time.

## <span>Events</span>

*No events.*

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
