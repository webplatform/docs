---
title: disconnect
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
summary: 'Disconnects an AudioNode from another that it is already connected to.'
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioNode/disconnect

---
## <span>Summary</span>

Disconnects an AudioNode from another that it is already connected to.

Method of [apis/webaudio/AudioNode](/apis/webaudio/AudioNode)[apis/webaudio/AudioNode](/apis/webaudio/AudioNode)

## <span>Syntax</span>

``` js
var  = AudioNode.disconnect(output);
```

## <span>Parameters</span>

### <span>output</span>

 Data-type
:   unsigned long

(Optional)

An index describing which output of the [**AudioNode**](/apis/webaudio/AudioNode) to disconnect. An out-of-bound value throws an exception.

## <span>Return Value</span>

Returns an object of type<span></span>

## <span>Examples</span>

``` js
oscillator.connect(audioCtx.destination);
oscillator.disconnect();
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
