---
title: AudioContext
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The AudioContext represents a set of AudioNode objects and their connections. It allows for arbitrary routing of signals to the AudioDestinationNode (what the user ultimately hears). Nodes are created from the context and are then connected together. In most use cases, only a single AudioContext is used per document.'
tags:
  0: API
  1: Objects
  3: WebAudio
uri: apis/webaudio/AudioContext

---
## Summary

The AudioContext represents a set of AudioNode objects and their connections. It allows for arbitrary routing of signals to the AudioDestinationNode (what the user ultimately hears). Nodes are created from the context and are then connected together. In most use cases, only a single AudioContext is used per document.

## Properties

API Name
:   Summary

[activeSourceCount](/apis/webaudio/AudioContext/activeSourceCount)
:   The number of [**AudioBufferSourceNode**s](/apis/webaudio/AudioBufferSourceNode) that are currently playing.

    **Out of date; removed from spec. See <http://webaudio.github.io/web-audio-api/>.**

[currentTime](/apis/webaudio/AudioContext/currentTime)
:   This is a time in seconds which starts at zero when the context is created and increases in real-time. All scheduled times are relative to it. This is not a *transport* time which can be started, paused, and re-positioned. It is always moving forward. A GarageBand-like timeline transport system can be very easily built on top of this (in JavaScript). This time corresponds to an ever-increasing hardware timestamp.

[destination](/apis/webaudio/AudioContext/destination)
:   An [AudioDestinationNode](/apis/webaudio/AudioDestinationNode) with a single input representing the final destination for all audio (to be rendered to the audio hardware, i.e., speakers). All [AudioNodes](/apis/webaudio/AudioNode) actively rendering audio will directly or indirectly connect to the destination node.

[listener](/apis/webaudio/AudioContext/listener)
:   An [AudioListener](/apis/webaudio/AudioListener), used for 3D spatialization.

[sampleRate](/apis/webaudio/AudioContext/sampleRate)
:   The sample rate, in sample-frames per second, at which the AudioContext handles audio. It is assumed that all [AudioNodes](/apis/webaudio/AudioNode) in the context run at this rate. In making this assumption, sample-rate converters or *varispeed* processors are not supported in real-time processing.

## Methods

API Name
:   Summary

[createAnalyser](/apis/webaudio/AudioContext/createAnalyser)
:   Creates an [**AnalyserNode**](/apis/webaudio/AnalyserNode).

[createBiquadFilter](/apis/webaudio/AudioContext/createBiquadFilter)
:   Creates a [BiquadFilterNode](/apis/webaudio/BiquadFilterNode) representing a second order filter which can be configured as one of several common filter types.

[createBuffer](/apis/webaudio/AudioContext/createBuffer)
:   Creates an [AudioBuffer](/apis/webaudio/AudioBuffer) of the given size. The audio data in the buffer will be zero-initialized (silent). An exception will be thrown if the [numberOfChannels](/apis/webaudio/AudioBuffer/numberOfChannels) or [sampleRate](/apis/webaudio/AudioContext/sampleRate) are out-of-bounds.

[createBufferSource](/apis/webaudio/AudioContext/createBufferSource)
:   Creates an [AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode) that can be used to play audio data contained within an AudioBuffer object..

[createChannelMerger](/apis/webaudio/AudioContext/createChannelMerger)
:   Creates a [ChannelMergerNode](/apis/webaudio/ChannelMergerNode) representing a channel merger. An exception will be thrown for invalid parameter values.

[createChannelSplitter](/apis/webaudio/AudioContext/createChannelSplitter)
:   Creates a [ChannelSplitterNode](/apis/webaudio/ChannelSplitterNode) representing a channel splitter. An exception will be thrown for invalid parameter values.

[createConvolver](/apis/webaudio/AudioContext/createConvolver)
:   Creates a [ConvolverNode](/apis/webaudio/ConvolverNode), commonly used to add reverb to audio.

[createDelay](/apis/webaudio/AudioContext/createDelay)
:   Creates a [DelayNode](/apis/webaudio/DelayNode) representing a variable delay line. Default delay is 0 seconds.

[createDynamicsCompressor](/apis/webaudio/AudioContext/createDynamicsCompressor)
:   Creates a [DynamicsCompressorNode](/apis/webaudio/DynamicsCompressorNode), used to apply compression to audio.

[createGain](/apis/webaudio/AudioContext/createGain)
:   Creates a [GainNode](/apis/webaudio/GainNode), used to control the volume of audio.

[createMediaElementSource](/apis/webaudio/AudioContext/createMediaElementSource)
:   Creates a MediaElementAudioSourceNode, given an [HTMLMediaElement](/dom/HTMLMediaElement). As a consequence of calling this method, audio playback from the [HTMLMediaElement](/dom/HTMLMediaElement) will be re-routed into the processing graph of the **AudioContext**.

[createMediaStreamSource](/apis/webaudio/AudioContext/createMediaStreamSource)
:   Creates a MediaStreamAudioSourceNode, given a [MediaStream](/apis/webrtc/MediaStream). As a consequence of calling this method, audio playback from the [MediaStream](/apis/webrtc/MediaStream) will be re-routed into the processing graph of the **AudioContext**.

[createOscillator](/apis/webaudio/AudioContext/createOscillator)
:   Creates an [OscillatorNode](/apis/webaudio/OscillatorNode), a source representing a periodic waveform. It basically generates a constant tone..

[createPanner](/apis/webaudio/AudioContext/createPanner)
:   Creates a [PannerNode](/apis/webaudio/PannerNode), used to spatialize an incoming audio stream in 3D space..

[createScriptProcessor](/apis/webaudio/AudioContext/createScriptProcessor)
:   Creates a [ScriptProcessorNode](/apis/webaudio/ScriptProcessorNode) for direct audio processing using JavaScript. An exception will be thrown if [bufferSize](/apis/webaudio/ScriptProcessorNode/bufferSize) or numberOfInputChannels or numberOfOutputChannels are outside the valid range.

[createWaveShaper](/apis/webaudio/AudioContext/createWaveShaper)
:   Creates a [WaveShaperNode](/apis/webaudio/WaveShaperNode), used to apply a distortion effect to audio.

[createWaveTable](/apis/webaudio/AudioContext/createWaveTable)
:   Creates a [**WaveTable**](/apis/webaudio/WaveTable) representing a waveform containing arbitrary harmonic content. The real and imag parameters must be of type **Float32Array** of equal lengths greater than zero and less than or equal to 4096 or an exception will be thrown. These parameters specify the Fourier coefficients of a Fourier series representing the partials of a periodic waveform. The created [**WaveTable**](/apis/webaudio/WaveTable) will be used with an [**OscillatorNode**](/apis/webaudio/OscillatorNode) and will represent a normalized time-domain waveform having maximum absolute peak value of 1. Another way of saying this is that the generated waveform of an [**OscillatorNode**](/apis/webaudio/OscillatorNode) will have maximum peak value at 0dBFS. Conveniently, this corresponds to the full-range of the signal values used by the Web Audio API. Because the [**WaveTable**](/apis/webaudio/WaveTable) will be normalized on creation, the real and imag parameters represent relative values.

    **Out of date; removed from spec. See <http://webaudio.github.io/web-audio-api/>.**

[decodeAudioData](/apis/webaudio/AudioContext/decodeAudioData)
:   Asynchronously decodes the audio file data contained in the ArrayBuffer. The ArrayBuffer can, for example, be loaded from an XMLHttpRequest with the new *responseType* and *response* attributes. Audio file data can be in any of the formats supported by the audio element.

    The decodeAudioData() method is preferred over the [createBuffer()](/apis/webaudio/AudioContext/createBuffer) from ArrayBuffer method because it is asynchronous and does not block the main JavaScript thread.

## Events

*No events.*

## Related specifications

[W3C Web Audio API](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html)
:   W3C Editor's Draft
