---
title: connect
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/webaudio/AudioNode
    href: /apis/webaudio/AudioNode
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/webaudio/AudioNode
standardization_status: 'W3C Editor''s Draft'
summary: 'Connects one AudioNode to another AudioNode.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioNode/connect

---
## <span>Summary</span>

Connects one AudioNode to another AudioNode.

Method of [apis/webaudio/AudioNode](/apis/webaudio/AudioNode)[apis/webaudio/AudioNode](/apis/webaudio/AudioNode)

## <span>Syntax</span>

``` js
var  = AudioNode.connect(destination, output, input);
```

## <span>Parameters</span>

### <span>destination</span>

 Data-type
:   unsigned long

(Optional)

The AudioNode to connect to.

### <span>output</span>

 Data-type
:   unsigned long

(Optional)

An index describing which output of the AudioNode to connect from. An out-of-bound value throws an exception.

### <span>input</span>

 Data-type
:   unsigned long

(Optional)

An index describing which input of the destination AudioNode to connect to. An out-of-bound value throws an exception.

## <span>Return Value</span>

Returns an object of type<span></span>

## <span>Examples</span>

``` js
var oscillator = audioCtx.createOscillator();
oscillator.connect(audioCtx.destination,1,1);
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
