---
title: 'bufferSize'
notes:
  - 'Deprecated; deletion candidate. See http://webaudio.github.io/web-audio-api/.'
readiness: 'Out of Date'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/ScriptProcessorNode
    href: /apis/webaudio/ScriptProcessorNode
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned long'
    href: /apis/webaudio/ScriptProcessorNode
standardization_status: 'W3C Editor''s Draft'
summary: "The size of the buffer (in sample-frames) which needs to be processed each time onaudioprocess is called. Legal values are 256, 512, 1024, 2048, 4096, 8192, and 16384.\n"
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/ScriptProcessorNode/bufferSize

---
## Summary

The size of the buffer (in sample-frames) which needs to be processed each time onaudioprocess is called. Legal values are 256, 512, 1024, 2048, 4096, 8192, and 16384.

**Deprecated; deletion candidate. See <http://webaudio.github.io/web-audio-api/>.**

Property of [apis/webaudio/ScriptProcessorNode](/apis/webaudio/ScriptProcessorNode)[apis/webaudio/ScriptProcessorNode](/apis/webaudio/ScriptProcessorNode)

## Syntax

**Note**: This property is read-only.

``` js
var result = ScriptProcessorNode.bufferSize;
```

## Return Value

Returns an object of type unsigned longunsigned long

**Needs Examples**: This section should include examples.

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
