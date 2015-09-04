---
title: webaudio
tags:
  0: API
  1: Listings
  3: WebAudio
readiness: 'Almost Ready'
standardization_status: 'W3C Editor''s Draft'
notes:
  - 'Fix broken link'
summary: 'Describes a high-level JavaScript API for processing and synthesizing audio in web applications.'
uri: apis/webaudio
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/xhr/objects/XMLHttpRequest

---
# Web Audio API

## Summary

Describes a high-level JavaScript API for processing and synthesizing audio in web applications.

API Name
:   Summary
[AnalyserNode](/apis/webaudio/AnalyserNode)
:   This interface represents a node which is able to provide real-time frequency and time-domain analysis information. The audio stream will be passed un-processed from input to output.
[AudioBuffer](/apis/webaudio/AudioBuffer)
:   This interface represents a memory-resident audio asset, primarily for one-shot sounds and other short audio clips. Its format is non-interleaved IEEE 32-bit linear PCM with a nominal range of -1 -\> +1. It can contain one or more channels.
[AudioBufferSourceNode](/apis/webaudio/AudioBufferSourceNode)
:   This interface represents an audio source from an in-memory audio asset in an [**AudioBuffer**](/apis/webaudio/AudioBuffer). It generally will be used for short audio assets which require a high degree of scheduling flexibility (can playback in rhythmically perfect ways).
[AudioContext](/apis/webaudio/AudioContext)
:   The [**AudioContext**](/apis/webaudio/AudioContext) represents a set of [**AudioNode**](/apis/webaudio/AudioNode) objects and their connections. It allows for arbitrary routing of signals to the [**AudioDestinationNode**](/apis/webaudio/AudioDestinationNode) (what the user ultimately hears). Nodes are created from the context and are then connected together. In most use cases, only a single [**AudioContext**](/apis/webaudio/AudioContext) is used per document.
[AudioDestinationNode](/apis/webaudio/AudioDestinationNode)
:   An [**AudioNode**](/apis/webaudio/AudioNode) representing the final audio destination and is what the user will ultimately hear. It can be considered as an audio output device which is connected to speakers. All rendered audio to be heard will be routed to this node, a *terminal* node in the [**AudioContext**](/apis/webaudio/AudioContext)'s routing graph. There is only a single [**AudioDestinationNode**](/apis/webaudio/AudioDestinationNode) per [**AudioContext**](/apis/webaudio/AudioContext), provided through the destination attribute of [**AudioContext**](/apis/webaudio/AudioContext).
[AudioListener](/apis/webaudio/AudioListener)
:   This interface represents the position and orientation of the person listening to the audio scene. All [**PannerNode**](/apis/webaudio/PannerNode) objects spatialize in relation to the [**AudioContext**](/apis/webaudio/AudioContext)'s listener.
[AudioNode](/apis/webaudio/AudioNode)
:   [**AudioNode**s](/apis/webaudio/AudioNode) are the building blocks of an [**AudioContext**](/apis/webaudio/AudioContext). An [**AudioNode**](/apis/webaudio/AudioNode) represents audio sources, the audio destination, and intermediate processing modules, connected together to form processing graphs for rendering audio to the audio hardware. In general, an AudioNode processes its inputs (if it has any), and generates audio for its outputs (if it has any).
[AudioParam](/apis/webaudio/AudioParam)
:   [**AudioParam**](/apis/webaudio/AudioParam) controls an individual aspect of an [**AudioNode**](/apis/webaudio/AudioNode)'s functioning, such as volume. The parameter can be set immediately to a particular value using the value attribute. Or, value changes can be scheduled to happen at very precise times (in the coordinate system of [**AudioContext.currentTime**](/apis/webaudio/AudioContext/currentTime)), for envelopes, volume fades, LFOs, filter sweeps, grain windows, etc. In this way, arbitrary timeline-based automation curves can be set on any [**AudioParam**](/apis/webaudio/AudioParam). Additionally, audio signals from the outputs of [**AudioNode**s](/apis/webaudio/AudioNode) can be connected to an [**AudioParam**](/apis/webaudio/AudioParam), summing with the intrinsic parameter value.
[AudioProcessingEvent](/apis/webaudio/AudioProcessingEvent)
:   This interface is a type of Event which is passed to the [**onaudioprocess**](/apis/webaudio/ScriptProcessorNode/onaudioprocess) event handler used by [**ScriptProcessorNode**](/apis/webaudio/ScriptProcessorNode). The event handler processes audio from the input (if any) by accessing the audio data from the [**inputBuffer**](/apis/webaudio/AudioProcessingEvent/inputBuffer) attribute. The audio data which is the result of the processing (or the synthesized data if there are no inputs) is then placed into the [**outputBuffer**](/apis/webaudio/AudioProcessingEvent/outputBuffer).

    **Deprecated; deletion candidate. See [http://webaudio.github.io/web-audio-api/](http://webaudio.github.io/web-audio-api/).**

[BiquadFilterNode](/apis/webaudio/BiquadFilterNode)
:   [**BiquadFilterNode**](/apis/webaudio/BiquadFilterNode) is an [**AudioNode**](/apis/webaudio/AudioNode) processor implementing common low-order filters, which are the building blocks of basic tone controls (bass, mid, treble), graphic equalizers, and more advanced filters. Multiple [**BiquadFilterNode**](/apis/webaudio/BiquadFilterNode) filters can be combined to form more complex filters. Each [**BiquadFilterNode**](/apis/webaudio/BiquadFilterNode) can be configured as one of a number of common filter types as listed in the type property page, linked below. The default filter type is LOWPASS.
[ChannelMergerNode](/apis/webaudio/ChannelMergerNode)
:   Represents an AudioNode for combining channels from multiple audio streams into a single audio stream. Often used in conjunction with [ChannelSplitterNode](/apis/webaudio/ChannelSplitterNode).
[ChannelSplitterNode](/apis/webaudio/ChannelSplitterNode)
:   Represents an AudioNode for accessing the individual channels of an audio stream in the routing graph. Often used in conjunction with [ChannelMergerNode](/apis/webaudio/ChannelMergerNode).
[ConvolverNode](/apis/webaudio/ConvolverNode)
:   This interface represents a processing node which applies a linear convolution effect given an impulse response.
[DelayNode](/apis/webaudio/DelayNode)
:   A delay-line is a fundamental building block in audio applications. This interface is an [**AudioNode**](/apis/webaudio/AudioNode) with a single input and single output, which delays the incoming audio signal by a certain amount. The default amount is 0 seconds (no delay).
[DynamicsCompressorNode](/apis/webaudio/DynamicsCompressorNode)
:   [**DynamicsCompressorNode**](/apis/webaudio/DynamicsCompressorNode) is an [**AudioNode**](/apis/webaudio/AudioNode) processor implementing a dynamics compression effect, which lowers the volume of the loudest parts of the signal and raises the volume of the softest parts. Compression is especially important in games and musical applications where large numbers of individual sounds are played simultaneously to control the overall signal level and help avoid clipping (distorting) the audio output to the speakers.
[GainNode](/apis/webaudio/GainNode)
:   Changing the gain of an audio signal is a fundamental operation in audio applications. The [**GainNode**](/apis/webaudio/GainNode) is one of the building blocks for creating mixers. This interface is an [**AudioNode**](/apis/webaudio/AudioNode) with a single input and single output, which multiplies the input audio signal by the (possibly time-varying) gain attribute, copying the result to the output.
[OscillatorNode](/apis/webaudio/OscillatorNode)
:   [**OscillatorNode**](/apis/webaudio/OscillatorNode) represents an audio source generating a periodic waveform. It can be set to a few commonly used waveforms. Additionally, it can be set to an arbitrary periodic waveform through the use of a [**WaveTable**](/apis/webaudio/WaveTable) object. Oscillators are common foundational building blocks in audio synthesis.
[PannerNode](/apis/webaudio/PannerNode)
:   This interface represents a processing node which positions / spatializes an incoming audio stream in three-dimensional space. The spatialization is in relation to the [**AudioContext**](/apis/webaudio/AudioContext)'s [**AudioListener**](/apis/webaudio/AudioListener) (listener attribute). The audio stream from the input will be either mono or stereo, depending on the connection(s) to the input. The output of this node is hard-coded to stereo (2 channels) and currently cannot be configured.
[ScriptProcessorNode](/apis/webaudio/ScriptProcessorNode)
:   This interface is an [**AudioNode**](/apis/webaudio/AudioNode) which can generate, process, or analyse audio directly using JavaScript.

    **Deprecated; deletion candidate. See [http://webaudio.github.io/web-audio-api/](http://webaudio.github.io/web-audio-api/).**

[WaveShaperNode](/apis/webaudio/WaveShaperNode)
:   [**WaveShaperNode**](/apis/webaudio/WaveShaperNode) is an [**AudioNode**](/apis/webaudio/AudioNode) processor implementing non-linear distortion effects. Non-linear waveshaping distortion is commonly used for both subtle non-linear warming, or for more obvious distortion effects.
[WaveTable](/apis/webaudio/WaveTable)
:   WaveTable represents an arbitrary periodic waveform to be used with an [**OscillatorNode**](/apis/webaudio/OscillatorNode).

## Usage

     This specification describes a high-level JavaScript API for processing and synthesizing audio in web applications. The primary paradigm is of an audio routing graph, where a number of AudioNode objects are connected together to define the overall audio rendering. The actual processing will primarily take place in the underlying implementation (typically optimized Assembly / C / C++ code), but direct JavaScript processing and synthesis is also supported.

This API is designed to be used in conjunction with other APIs and elements on the web platform, notably: [**XMLHttpRequest**](/w/index.php?title=apis/xhr/objects/XMLHttpRequest&action=edit&redlink=1) (using the **responseType** and **response** attributes). For games and interactive applications, it is anticipated to be used with the canvas 2D and WebGL 3D graphics APIs.

## See also

### Related articles

#### Audio

-   [audio-video](/apis/audio-video)

-   [enabled](/apis/audio-video/AudioTrack/enabled)

-   [language](/apis/audio-video/AudioTrack/language)

-   **Web Audio API**

-   [value](/apis/webaudio/AudioParam/value)

-   [WebRTC](/concepts/Internet_and_Web/webrtc)

-   [user-input](/css/properties/user-input)

-   [bgSound](/html/elements/bgSound)

-   [bgsound](/html/elements/bgSound/ja)

-   [implementing html5 audio](/tutorials/implementing_html5_audio)

-   [WebRTC Resources](/tutorials/webrtc_resources)

