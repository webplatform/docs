---
title: frequencyBinCount
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
summary: 'Half the fftSize (the size of the FFT used for frequency-domain analysis).'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AnalyserNode/frequencyBinCount

---
## <span>Summary</span>

Half the fftSize (the size of the FFT used for frequency-domain analysis).

Property of [apis/webaudio/AnalyserNode](/apis/webaudio/AnalyserNode)[apis/webaudio/AnalyserNode](/apis/webaudio/AnalyserNode)

## <span>Syntax</span>

``` js
var result = AnalyserNode.frequencyBinCount;
AnalyserNode.frequencyBinCount = value;
```

## <span>Return Value</span>

Returns an object of type unsigned longunsigned long

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var analyser = audioCtx.createAnalyser();
var bufferLength = analyser.frequencyBinCount;
```

## <span>Related specifications</span>

[Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
