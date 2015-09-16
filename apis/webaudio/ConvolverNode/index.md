---
title: 'ConvolverNode'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'This interface represents a processing node which applies a linear convolution effect given an impulse response.'
tags:
  0: API
  1: Objects
  3: WebAudio
uri: apis/webaudio/ConvolverNode

---
## Summary

This interface represents a processing node which applies a linear convolution effect given an impulse response.

## Properties

API Name
:   Summary

[buffer](/apis/webaudio/ConvolverNode/buffer)
:   A mono, stereo, or 4-channel [**AudioBuffer**](/apis/webaudio/AudioBuffer) containing the (possibly multi-channel) impulse response used by the ****ConvolverNode****. At the time when this attribute is set, the buffer and the state of the normalize attribute will be used to configure the ****ConvolverNode**** with this impulse response having the given normalization.

[normalize](/apis/webaudio/ConvolverNode/normalize)
:   Controls whether the impulse response from the buffer will be scaled by an equal-power normalization when the buffer atttribute is set. Its default value is true in order to achieve a more uniform output level from the convolver when loaded with diverse impulse responses. If normalize is set to false, then the convolution will be rendered with no pre-processing/scaling of the impulse response. Changes to this value do not take effect until the next time the buffer attribute is set. If the normalize attribute is false when the buffer attribute is set then the ****ConvolverNode**** will perform a linear convolution given the exact impulse response contained within the buffer.

## Methods

*No methods.*

## Events

*No events.*

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
