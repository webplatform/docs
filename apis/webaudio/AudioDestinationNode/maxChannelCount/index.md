---
title: maxChannelCount
readiness: 'Ready to Use'
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
summary: 'The maximum number of channels that the physical hardware is capable of supporting. The AudioNode channelCount property can be set between 0 and this value, inclusive. A value of 0 indicates that the channel count may not be changed. Default is 2.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AudioDestinationNode/maxChannelCount

---
## <span>Summary</span>

The maximum number of channels that the physical hardware is capable of supporting. The AudioNode channelCount property can be set between 0 and this value, inclusive. A value of 0 indicates that the channel count may not be changed. Default is 2.

Property of [apis/webaudio/AudioDestinationNode](/apis/webaudio/AudioDestinationNode)[apis/webaudio/AudioDestinationNode](/apis/webaudio/AudioDestinationNode)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = AudioDestinationNode.maxChannelCount;
```

## <span>Return Value</span>

Returns an object of type unsigned longunsigned long

## <span>Examples</span>

``` js
var audioCtx = new AudioContext();
var myDestination = audioCtx.destination;
mcc = myDestination.maxChannelCount;
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
