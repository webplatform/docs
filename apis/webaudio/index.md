---
title: Web Audio API
notes:
  - 'Fix broken link'
readiness: 'Almost Ready'
standardization_status: 'W3C Editor''s Draft'
summary: 'Describes a high-level JavaScript API for processing and synthesizing audio in web applications.'
tags:
  0: API
  1: Listings
  3: WebAudio
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/xhr/objects/XMLHttpRequest
uri: apis/webaudio

---
## <span>Summary</span>

Describes a high-level JavaScript API for processing and synthesizing audio in web applications.

API Name
:   Summary

[AudioBuffer](/apis/webaudio/AudioBuffer)
:   This interface represents a memory-resident audio asset, primarily for one-shot sounds and other short audio clips. Its format is non-interleaved IEEE 32-bit linear PCM with a nominal range of -1 -\> +1. It can contain one or more channels.

[AudioListener](/apis/webaudio/AudioListener)
:   This interface represents the position and orientation of the person listening to the audio scene. All [**PannerNode**](/apis/webaudio/PannerNode) objects spatialize in relation to the [**AudioContext**](/apis/webaudio/AudioContext)'s listener.

[ChannelMergerNode](/apis/webaudio/ChannelMergerNode)
:   Represents an AudioNode for combining channels from multiple audio streams into a single audio stream. Often used in conjunction with [ChannelSplitterNode](/apis/webaudio/ChannelSplitterNode).

[ChannelSplitterNode](/apis/webaudio/ChannelSplitterNode)
:   Represents an AudioNode for accessing the individual channels of an audio stream in the routing graph. Often used in conjunction with [ChannelMergerNode](/apis/webaudio/ChannelMergerNode).

[ConvolverNode](/apis/webaudio/ConvolverNode)
:   This interface represents a processing node which applies a linear convolution effect given an impulse response.

[GainNode](/apis/webaudio/GainNode)
:   Changing the gain of an audio signal is a fundamental operation in audio applications. The [**GainNode**](/apis/webaudio/GainNode) is one of the building blocks for creating mixers. This interface is an [**AudioNode**](/apis/webaudio/AudioNode) with a single input and single output, which multiplies the input audio signal by the (possibly time-varying) gain attribute, copying the result to the output.

[OscillatorNode](/apis/webaudio/OscillatorNode)
:   [**OscillatorNode**](/apis/webaudio/OscillatorNode) represents an audio source generating a periodic waveform. It can be set to a few commonly used waveforms. Additionally, it can be set to an arbitrary periodic waveform through the use of a [**WaveTable**](/apis/webaudio/WaveTable) object. Oscillators are common foundational building blocks in audio synthesis.

[WaveTable](/apis/webaudio/WaveTable)
:   WaveTable represents an arbitrary periodic waveform to be used with an [**OscillatorNode**](/apis/webaudio/OscillatorNode).

## <span>Usage</span>

     This specification describes a high-level JavaScript API for processing and synthesizing audio in web applications. The primary paradigm is of an audio routing graph, where a number of AudioNode objects are connected together to define the overall audio rendering. The actual processing will primarily take place in the underlying implementation (typically optimized Assembly / C / C++ code), but direct JavaScript processing and synthesis is also supported.

This API is designed to be used in conjunction with other APIs and elements on the web platform, notably: [**XMLHttpRequest**](/w/index.php?title=apis/xhr/objects/XMLHttpRequest&action=edit&redlink=1) (using the **responseType** and **response** attributes). For games and interactive applications, it is anticipated to be used with the canvas 2D and WebGL 3D graphics APIs.

## <span>See also</span>

### <span>Related articles</span>

#### <span>Audio</span>

-   [audio-video](/apis/audio-video)

-   [enabled](/apis/audio-video/AudioTrack/enabled)

-   [language](/apis/audio-video/AudioTrack/language)

-   **Web Audio API**

-   [value](/apis/webaudio/AudioParam/value)

-   [WebRTC](/concepts/Internet_and_Web/webrtc)

-   [bgSound](/html/elements/bgSound)

-   [bgsound](/html/elements/bgSound/ja)

-   [implementing html5 audio](/tutorials/implementing_html5_audio)

-   [WebRTC Resources](/tutorials/webrtc_resources)
