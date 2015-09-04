---
title: disconnect
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Disconnects an AudioNode from another that it is already connected to.'
uri: apis/webaudio/AudioNode/disconnect

---
# disconnect

## Summary

Disconnects an AudioNode from another that it is already connected to.

*Method of [apis/webaudio/AudioNode](/apis/webaudio/AudioNode)*

## Syntax

``` {.js}
var  = AudioNode.disconnect(output);
```

## Parameters

### output

 Data-typeÂ
:   unsigned long

*(Optional)*

An index describing which output of the [**AudioNode**](/apis/webaudio/AudioNode) to disconnect. An out-of-bound value throws an exception.

## Return Value

Returns an object of type .

## Examples

``` {.js}
oscillator.connect(audioCtx.destination);
oscillator.disconnect();
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

