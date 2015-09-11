---
title: createMediaStreamSource
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
  0: API
  1: Object
  2: Methods
  4: WebAudio
uri: apis/webaudio/AudioContext/createMediaStreamSource

---
## <span>Summary</span>

Creates a MediaStreamAudioSourceNode, given a MediaStream. As a consequence of calling this method, audio playback from the MediaStream will be re-routed into the processing graph of the AudioContext.

Method of [apis/webaudio/AudioContext](/apis/webaudio/AudioContext)[apis/webaudio/AudioContext](/apis/webaudio/AudioContext)

## <span>Syntax</span>

``` js
var  = AudioContext.createMediaStreamSource();
```

## <span>Return Value</span>

Returns an object of type<span></span>

MediaStreamAudioSourceNode

## <span>Examples</span>

``` js
//it may be necessary to prefix getUserMedia and AudioContext in order to work in some browsers

//request microphone stream
navigator.getUserMedia({ audio: true }, function(stream){
     var context = new AudioContext();
     var micStreamSource = context.createMediaStreamSource(stream);

     micStreamSource.connect(context.destination);  //redirects mic input to speakers
}, function(){ console.log('Error getting Microphone stream'); });
```

## <span>Related specifications</span>

[W3C Web Audio API](http://webaudio.github.io/web-audio-api/)
:   W3C Editor's Draft
