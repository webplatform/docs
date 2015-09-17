---
title: 'createMediaStreamSource'
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
summary: 'Creates a MediaStreamAudioSourceNode, given a MediaStream. As a consequence of calling this method, audio playback from the MediaStream will be re-routed into the processing graph of the AudioContext.'
tags:
  - API_Object_Methods
  - API
  - WebAudio
uri: apis/webaudio/AudioContext/createMediaStreamSource

---
## Summary

Creates a MediaStreamAudioSourceNode, given a MediaStream. As a consequence of calling this method, audio playback from the MediaStream will be re-routed into the processing graph of the AudioContext.

Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## Syntax

``` js
var  = AudioContext.createMediaStreamSource();
```

## Return Value

Returns an object of type

MediaStreamAudioSourceNode

## Examples

``` js
//it may be necessary to prefix getUserMedia and AudioContext in order to work in some browsers

//request microphone stream
navigator.getUserMedia({ audio: true }, function(stream){
     var context = new AudioContext();
     var micStreamSource = context.createMediaStreamSource(stream);

     micStreamSource.connect(context.destination);  //redirects mic input to speakers
}, function(){ console.log('Error getting Microphone stream'); });
```

## Related specifications

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
