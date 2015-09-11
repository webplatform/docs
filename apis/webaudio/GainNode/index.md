---
title: GainNode
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Changing the gain of an audio signal is a fundamental operation in audio applications. The GainNode is one of the building blocks for creating mixers. This interface is an AudioNode with a single input and single output, which multiplies the input audio signal by the (possibly time-varying) gain attribute, copying the result to the output.'
tags:
  0: API
  1: Objects
  3: WebAudio
uri: apis/webaudio/GainNode

---
## <span>Summary</span>

Changing the gain of an audio signal is a fundamental operation in audio applications. The GainNode is one of the building blocks for creating mixers. This interface is an AudioNode with a single input and single output, which multiplies the input audio signal by the (possibly time-varying) gain attribute, copying the result to the output.

## <span>Properties</span>

API Name
:   Summary

[gain](/apis/webaudio/GainNode/gain)
:   Represents the amount of gain to apply. Its default value is 1 (no gain change). The nominal minValue is 0, but may be set negative for phase inversion. The nominal maxValue is 1, but higher values are allowed (no exception thrown). This parameter is a-rate.

## <span>Methods</span>

*No methods.*

## <span>Events</span>

*No events.*

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
