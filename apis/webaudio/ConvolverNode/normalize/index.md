---
title: normalize
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/ConvolverNode
    href: /apis/webaudio/ConvolverNode
  return:
    predicate: 'Returns an object of type '
    value: Boolean
    href: /apis/webaudio/ConvolverNode
standardization_status: 'W3C Editor''s Draft'
summary: 'Controls whether the impulse response from the buffer will be scaled by an equal-power normalization when the buffer atttribute is set. Its default value is true in order to achieve a more uniform output level from the convolver when loaded with diverse impulse responses. If normalize is set to false, then the convolution will be rendered with no pre-processing/scaling of the impulse response. Changes to this value do not take effect until the next time the buffer attribute is set. If the normalize attribute is false when the buffer attribute is set then the ConvolverNode will perform a linear convolution given the exact impulse response contained within the buffer.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/ConvolverNode/normalize

---
## <span>Summary</span>

Controls whether the impulse response from the buffer will be scaled by an equal-power normalization when the buffer atttribute is set. Its default value is true in order to achieve a more uniform output level from the convolver when loaded with diverse impulse responses. If normalize is set to false, then the convolution will be rendered with no pre-processing/scaling of the impulse response. Changes to this value do not take effect until the next time the buffer attribute is set. If the normalize attribute is false when the buffer attribute is set then the ConvolverNode will perform a linear convolution given the exact impulse response contained within the buffer.

Property of [apis/webaudio/ConvolverNode](/apis/webaudio/ConvolverNode)[apis/webaudio/ConvolverNode](/apis/webaudio/ConvolverNode)

## <span>Syntax</span>

``` js
var result = ConvolverNode.normalize;
ConvolverNode.normalize = value;
```

## <span>Return Value</span>

Returns an object of type BooleanBoolean

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var convolver = audioCtx.createConvolver();
convolver.normalize = false;
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
