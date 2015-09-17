---
title: 'AudioDestinationNode'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'An AudioNode representing the final audio destination and is what the user will ultimately hear. It can be considered as an audio output device which is connected to speakers. All rendered audio to be heard will be routed to this node, a terminal node in the AudioContext''s routing graph. There is only a single AudioDestinationNode per AudioContext, provided through the destination attribute of AudioContext.'
tags:
  - API_Objects
  - API
  - WebAudio
uri: apis/webaudio/AudioDestinationNode

---
## Summary

An AudioNode representing the final audio destination and is what the user will ultimately hear. It can be considered as an audio output device which is connected to speakers. All rendered audio to be heard will be routed to this node, a terminal node in the AudioContext's routing graph. There is only a single AudioDestinationNode per AudioContext, provided through the destination attribute of AudioContext.

## Properties

[maxChannelCount](/apis/webaudio/AudioDestinationNode/maxChannelCount)
:   The maximum number of channels that the physical hardware is capable of supporting. The AudioNode *channelCount* property can be set between 0 and this value, inclusive. A value of 0 indicates that the channel count may not be changed. Default is 2.

[numberOfChannels](/apis/webaudio/AudioDestinationNode/numberOfChannels)
:   The number of channels of the destination's input. This value will default to 2, and may be set to any non-zero value less than or equal to [**maxChannelCount**](/apis/webaudio/AudioDestinationNode/maxChannelCount). An exception will be thrown if this value is not within the valid range.

    **Not in spec; deletion candidate. Possibly confused with AudioBuffer/numberOfChannels. See <http://webaudio.github.io/web-audio-api/>.**

## Methods

*No methods.*

## Events

*No events.*

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
