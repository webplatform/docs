---
title: An introduction to the Web Audio API
readiness: 'Ready to Use'
summary: "The Web Audio API is a way of creating and manipulating audio within the browser. It’s a specification proposed by Google, and as such is currently only available in Chrome, with the hope other browsers adopting it and it becoming a standard.\n"
tags:
  - Tutorials
  - Audio
uri: 'tutorials/audio/an introduction to the web audio api'

---
**By [Stuart Memo](http://stuartmemo.com)**
Originally published June 13th, 2012

## Summary

The Web Audio API is a way of creating and manipulating audio within the browser. It’s a specification proposed by Google, and as such is currently only available in Chrome, with the hope other browsers adopting it and it becoming a standard.

The actual audio processing itself is done with Assembly/C/C++ code within the browser, but the API gives us a nice high-level way of interacting with this code using JavaScript.

**This article is part of a three articles series; see [tutorials/audio/intro\_web\_audio\_api\_1](/tutorials/audio/intro_web_audio_api_1).**

### AudioContext

In order to start using the API, we must first create an AudioContext. Think of this as a canvas for sound. It’s a container for all the playback and manipulation of audio we’re going to be doing. We create it by simply doing this:

``` js
    var context = new webkitAudioContext();
    // We use the "webkit" prefix as the API isn't a standard yet
```

Now that we’ve created this container, what do we put in it? Well, this is where the concept of nodes and modular routing comes in.

## Nodes and modular routing

Imagine a guitar player who has an electric guitar, a distortion pedal and an amp. When the guitar player strums her guitar, the sound travels from the guitar, down a cable, through the distortion pedal, and down another cable before finally coming out the speaker of the guitar amp. This chain is very similar to the nodes and modular routing model of the Web Audio API. The guitar, distortion pedal and the amp are all nodes, which we’ve routed in the correct order using cables.

## Playing a sound file

Ok, time to stop mucking about with concepts and learn how to play an audio file using the Web Audio API. Let’s start coding by declaring a couple of variables:

``` js
    var context = new webkitAudioContext(),
        buffer;
```

We already know about `context`, but what are we going to use `buffer` for? Well, audio buffers are essentially a holding place in memory for sound data. We read data into a buffer from an audio file using an \<a href="<http://www.html5rocks.com/en/tutorials/file/xhr2/>"\>XMLHttpRequest\</a\> like so:

``` js
    var loadAudioFile = function (url) {
        var request = new XMLHttpRequest();

        request.open('get', 'path/my-audio.wav', true);
        request.responseType = 'arraybuffer';

        request.onload = function () {
            context.decodeAudioData(request.response,
                function(incomingBuffer) {
                    playAudioFile(incomingBuffer); // Not declared yet
                 }
            );
        };

        request.send();
    };
```

Using an XMLHttpRequest allows us to tell the browser that we’re not loading a normal text file. By specifying `arraybuffer`, we’re flagging up the fact that we’re expecting binary data. Once we receive that chunk of data from the server, and because we know it’s an audio file (audiophile! ha!), we decode this data using `context.decodeAudioData` and specify an anonymous function as the callback that is passed the decoded data in a handy audio buffer that’s ready to be played. To do so though, we need to write a playback function.

``` js
    var playAudioFile = function (buffer) {
        var source = context.createBufferSource();

        source.buffer = buffer;
        source.connect(context.destination);
        source.noteOn(0); // Play sound immediately
    };
```

In the above code `source` is the guitar in our analogy. It’s the very first node in our chain, and in this case we’re telling it that the source of the audio is from the buffer we just loaded. We then use `source.connect(context.destination)` to use a lead to connect the sound source to the speakers, `context.destination`, and `source.noteOn(0)` to play the sound after 0 seconds.\</p\>

Let’s put all of this together and see what we get:

``` js
    var context = new webkitAudioContext(),
        buffer;

    var playAudioFile = function (buffer) {
        var source = context.createBufferSource();
        source.buffer = buffer;
        source.connect(context.destination);
        source.noteOn(0); // Play sound immediately
    };

    var loadAudioFile = (function (url) {
        var request = new XMLHttpRequest();

        request.open('get', 'path/my-audio.wav', true);
        request.responseType = 'arraybuffer';

        request.onload = function () {
                context.decodeAudioData(request.response,
                     function(incomingBuffer) {
                         playAudioFile(incomingBuffer);
                     }
                );
        };

        request.send();
    }());
```

Reference this in an HTML file, make a cup of tea and relax while you enjoy the sounds of your choosing in the browser.

I wouldn’t have been able to write this article without [Boris Smus](http://smus.com)’ code examples on [HTML5 Rocks](http://www.html5rocks.com/en/tutorials/webaudio/intro/) so check it out!
