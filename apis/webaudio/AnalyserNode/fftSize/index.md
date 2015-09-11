---
title: fftSize
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/AnalyserNode
    href: /apis/webaudio/AnalyserNode
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned long'
    href: /apis/webaudio/AnalyserNode
standardization_status: 'W3C Editor''s Draft'
summary: 'The size of the FFT (Fast Fourier Transform) used for frequency-domain analysis. Must be a power of two in the range 32-2048; defaults to 2048.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AnalyserNode/fftSize

---
## <span>Summary</span>

The size of the FFT (Fast Fourier Transform) used for frequency-domain analysis. Must be a power of two in the range 32-2048; defaults to 2048.

Property of [apis/webaudio/AnalyserNode](/apis/webaudio/AnalyserNode)[apis/webaudio/AnalyserNode](/apis/webaudio/AnalyserNode)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = AnalyserNode.fftSize;
```

## <span>Return Value</span>

Returns an object of type unsigned longunsigned long

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var analyser = audioCtx.createAnalyser();
analyser.fftSize = 2048;
```

## <span>Related specifications</span>

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
