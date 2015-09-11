---
title: value
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/webaudio/AudioParam
    href: /apis/webaudio/AudioParam
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /apis/webaudio/AudioParam
standardization_status: 'W3C Editor''s Draft'
summary: 'The parameter''s floating-point value. If a value is set outside the allowable range no exception is thrown, because these limits are nominal and may be exceeded. If a value is set during a time when there are any automation events scheduled then it will be ignored and no exception will be thrown.'
tags:
  0: API
  1: Object
  2: Properties
  4: WebAudio
uri: apis/webaudio/AudioParam/value

---
## <span>Summary</span>

The parameter's floating-point value. If a value is set outside the allowable range no exception is thrown, because these limits are nominal and may be exceeded. If a value is set during a time when there are any automation events scheduled then it will be ignored and no exception will be thrown.

Property of [apis/webaudio/AudioParam](/apis/webaudio/AudioParam)[apis/webaudio/AudioParam](/apis/webaudio/AudioParam)

## <span>Syntax</span>

``` js
var result = AudioParam.value;
AudioParam.value = value;
```

## <span>Return Value</span>

Returns an object of type NumberNumber

## <span>Examples</span>

``` js
var gainNode = audioCtx.createGain();
gainNode.gain.value = 0; //'gain' is the AudioParam
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

## <span>See also</span>

### <span>Related articles</span>

#### <span>Audio</span>

-   [audio-video](/apis/audio-video)

-   [enabled](/apis/audio-video/AudioTrack/enabled)

-   [language](/apis/audio-video/AudioTrack/language)

-   [Web Audio API](/apis/webaudio)

-   **value**

-   [WebRTC](/concepts/Internet_and_Web/webrtc)

-   [bgSound](/html/elements/bgSound)

-   [bgsound](/html/elements/bgSound/ja)

-   [implementing html5 audio](/tutorials/implementing_html5_audio)

-   [WebRTC Resources](/tutorials/webrtc_resources)
