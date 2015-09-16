---
title: decodeAudioData
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/webaudio/AudioContext
    href: /apis/webaudio/AudioContext
  return_type:
    predicate: 'Returns an object of type  '
    value: ''
    href: /apis/webaudio/AudioContext
standardization_status: 'W3C Editor''s Draft'
summary: "Asynchronously decodes the audio file data contained in the ArrayBuffer. The ArrayBuffer can, for example, be loaded from an XMLHttpRequest with the new responseType and response attributes. Audio file data can be in any of the formats supported by the audio element.\n"
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioContext/decodeAudioData

---
## Summary

Asynchronously decodes the audio file data contained in the ArrayBuffer. The ArrayBuffer can, for example, be loaded from an XMLHttpRequest with the new responseType and response attributes. Audio file data can be in any of the formats supported by the audio element.

The decodeAudioData() method is preferred over the [createBuffer()](/apis/webaudio/AudioContext/createBuffer) from ArrayBuffer method because it is asynchronous and does not block the main JavaScript thread.

Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## Syntax

``` js
var  = AudioContext.decodeAudioData(audioData, successCallback, errorCallback);
```

## Parameters

### audioData

 Data-type
:   String

 An ArrayBuffer containing audio file data.

### successCallback

 Data-type
:   function

 A callback function which will be invoked when the decoding is finished. The single argument to this callback is an [**AudioBuffer**](/apis/webaudio/AudioBuffer) representing the decoded PCM audio data.

### errorCallback

 Data-type
:   function

(Optional)

A callback function which will be invoked if there is an error decoding the audio file data.

## Return Value

Returns an object of type

## Examples

``` js
var audioCtx = new AudioContext();
audioCtx.decodeAudioData(audioData, function(buffer) { ... };);
```

## Notes

The older callback-based system is still in the spec for legacy reasons and is currently supported across browsers that support the Web Audio API. It is to be superceded by the newer promise-based syntax, which is in the latest spec, but not yet supported by any browser.

See <http://webaudio.github.io/web-audio-api/>.

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
