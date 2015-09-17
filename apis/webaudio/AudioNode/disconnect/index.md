---
title: 'disconnect'
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
  - API_Object_Methods
  - API
  - WebAudio
uri: apis/webaudio/AudioNode/disconnect

---
## Summary

Disconnects an AudioNode from another that it is already connected to.

Method of [apis/webaudio/AudioNode](/apis/webaudio/AudioNode)[apis/webaudio/AudioNode](/apis/webaudio/AudioNode)

## Syntax

``` js
var  = AudioNode.disconnect(output);
```

## Parameters

### output

 Data-type
:   unsigned long

(Optional)

An index describing which output of the [**AudioNode**](/apis/webaudio/AudioNode) to disconnect. An out-of-bound value throws an exception.

## Return Value

Returns an object of type

## Examples

``` js
oscillator.connect(audioCtx.destination);
oscillator.disconnect();
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
