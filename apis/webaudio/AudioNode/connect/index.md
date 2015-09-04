---
title: connect
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Connects one AudioNode to another AudioNode.'
uri: apis/webaudio/AudioNode/connect

---
# connect

## Summary

Connects one AudioNode to another AudioNode.

*Method of [apis/webaudio/AudioNode](/apis/webaudio/AudioNode)*

## Syntax

``` {.js}
var  = AudioNode.connect(destination, output, input);
```

## Parameters

### destination

 Data-typeÂ
:   unsigned long

*(Optional)*

The AudioNode to connect to.

### output

 Data-typeÂ
:   unsigned long

*(Optional)*

An index describing which output of the AudioNode to connect from. An out-of-bound value throws an exception.

### input

 Data-typeÂ
:   unsigned long

*(Optional)*

An index describing which input of the destination AudioNode to connect to. An out-of-bound value throws an exception.

## Return Value

Returns an object of type .

## Examples

``` {.js}
var oscillator = audioCtx.createOscillator();
oscillator.connect(audioCtx.destination,1,1);
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

