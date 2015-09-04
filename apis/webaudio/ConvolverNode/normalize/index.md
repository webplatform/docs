---
title: normalize
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Controls whether the impulse response from the buffer will be scaled by an equal-power normalization when the buffer atttribute is set. Its default value is true in order to achieve a more uniform output level from the convolver when loaded with diverse impulse responses. If normalize is set to false, then the convolution will be rendered with no pre-processing/scaling of the impulse response. Changes to this value do not take effect until the next time the buffer attribute is set. If the normalize attribute is false when the buffer attribute is set then the ConvolverNode will perform a linear convolution given the exact impulse response contained within the buffer.'
uri: apis/webaudio/ConvolverNode/normalize

---
# normalize

## Summary

Controls whether the impulse response from the buffer will be scaled by an equal-power normalization when the buffer atttribute is set. Its default value is true in order to achieve a more uniform output level from the convolver when loaded with diverse impulse responses. If normalize is set to false, then the convolution will be rendered with no pre-processing/scaling of the impulse response. Changes to this value do not take effect until the next time the buffer attribute is set. If the normalize attribute is false when the buffer attribute is set then the ConvolverNode will perform a linear convolution given the exact impulse response contained within the buffer.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/webaudio/ConvolverNode](/apis/webaudio/ConvolverNode)</span></span>

## Syntax

``` {.js}
var result = ConvolverNode.normalize;
ConvolverNode.normalize = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

## Examples

``` {.js}
var audioCtx = new AudioContext();
var convolver = audioCtx.createConvolver();
convolver.normalize = false;
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

