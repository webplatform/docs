---
title: 'numberOfChannels'
notes:
  - 'Not in spec; deletion candidate. Possibly confused with AudioBuffer/numberOfChannels.'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/AudioDestinationNode
    href: /apis/webaudio/AudioDestinationNode
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned long'
    href: /apis/webaudio/AudioDestinationNode
standardization_status: 'W3C Editor''s Draft'
summary: "The number of channels of the destination's input. This value will default to 2, and may be set to any non-zero value less than or equal to maxChannelCount. An exception will be thrown if this value is not within the valid range.\n"
tags:
  - API_Object_Properties
  - API
  - WebAudio
  - Needs_Examples
uri: apis/webaudio/AudioDestinationNode/numberOfChannels

---
## Summary

The number of channels of the destination's input. This value will default to 2, and may be set to any non-zero value less than or equal to maxChannelCount. An exception will be thrown if this value is not within the valid range.

**Not in spec; deletion candidate. Possibly confused with AudioBuffer/numberOfChannels. See <http://webaudio.github.io/web-audio-api/>.**

Property of [apis/webaudio/AudioDestinationNode](/apis/webaudio/AudioDestinationNode)[apis/webaudio/AudioDestinationNode](/apis/webaudio/AudioDestinationNode)

## Syntax

``` js
var result = AudioDestinationNode.numberOfChannels;
AudioDestinationNode.numberOfChannels = value;
```

## Return Value

Returns an object of type unsigned longunsigned long

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
