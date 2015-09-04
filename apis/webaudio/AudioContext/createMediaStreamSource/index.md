---
title: createMediaStreamSource
tags:
  0: API
  1: Object
  2: Methods
  4: WebAudio
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Creates a MediaStreamAudioSourceNode, given a MediaStream. As a consequence of calling this method, audio playback from the MediaStream will be re-routed into the processing graph of the AudioContext.'
uri: apis/webaudio/AudioContext/createMediaStreamSource

---
# createMediaStreamSource

## Summary

Creates a MediaStreamAudioSourceNode, given a MediaStream. As a consequence of calling this method, audio playback from the MediaStream will be re-routed into the processing graph of the AudioContext.

*Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)*

## Syntax

``` {.js}
var  = AudioContext.createMediaStreamSource();
```

## Return Value

Returns an object of type .

MediaStreamAudioSourceNode

## Examples

``` {.js}
//it may be necessary to prefix getUserMedia and AudioContext in order to work in some browsers

//request microphone stream
navigator.getUserMedia({ audio: true }, function(stream){
     var context = new AudioContext();
     var micStreamSource = context.createMediaStreamSource(stream);

     micStreamSource.connect(context.destination);  //redirects mic input to speakers
}, function(){ console.log('Error getting Microphone stream'); });
```

## Related specifications

Specification
:   Status
[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft

