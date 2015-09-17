---
title: 'Introduction to the web audio API, part 1'
readiness: 'Ready to Use'
summary: 'An introduction to the web audio API: loading and playing an external sound file.'
tags:
  - Tutorials
  - Audio
uri: 'tutorials/audio/intro web audio api 1'

---
**By [Dave Gash](/User:Dgash)**
Originally published October 19, 2012

## Summary

An introduction to the web audio API: loading and playing an external sound file.

**This article is part of a three articles series; see [tutorials/audio/intro\_web\_audio\_api\_2](/tutorials/audio/intro_web_audio_api_2).**

## Introduction

Web-based audio is becoming more robust all the time, and necessarily so. As the web evolves in stylistic and presentational features, web applications also require a higher degree of sophistication in audio manipulation. Gone are the days of `<embed>`, `<object>`, and `<bgsound>`, when the best you could hope for was static playback of a fixed music track.

Today, diverse web apps such as games, audio editors, playlist managers, ringtone stores, musicians' utilities, and more have a need for subtlety and finesse in their use of audio, and users deserve—and have come to expect—power and flexibility in those apps.

The web audio API is not to be confused with the HTML5 `<audio>` element. For information on that element, see [this W3C article](http://www.w3.org/wiki/HTML/Elements/audio) or [this HTML5Rocks! tutorial](http://www.html5rocks.com/en/tutorials/audio/quick/). As useful as the `<audio>` element is in terms of encapsulating the load-decode-play sequence (more about that later), it doesn't include capabilities to precisely control sounds, time them, or fine-tune their playback characteristics. Enter the *web audio API*.

The web audio API is high-level JavaScript interface that is about much more than just playing sounds. With it, you can process, synthesize, mix, visualize, filter, and otherwise manipulate audio data with extreme precision to accomplish tasks and achieve results previously found only in high-end commercial audio applications.

In this tutorial, we'll explore the basics of the API and learn how to load, start, and stop a sound before moving on to more complex tasks.

## Prerequisite concepts

To effectively use the web audio API, certain things must happen in a certain order; it's that sequence of events we'll explore next. But first, we need to understand a couple of concepts, called *context* and *nodes*, and how they relate to each other.

API sound manipulation takes place within an [AudioContext](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html#AudioContext-section). A context can be thought of as a master container inside which your web page does all of its audio processing. A major benefit of this "sandbox" approach is that it isolates all the audio work—even the most complex and demanding processes—into an independent, high-priority thread and thus prevents this CPU-intensive work from interfering with other events (visual or aural) and marring the user experience.

It is important to note that an audio context, when created in software, represents the physical hardware context in which the application is running, and thus implements its characteristics—operating at a fixed sample rate, for example.

The audio context allows for the creation of one or more [AudioNode](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html#AudioNode-section)s, all of which reside in the context. Nodes are the building blocks of audio processing, and may be *input*, *processor*, or *output* types.

Nodes may have input and/or output connections, which are used to string them together into a sequence. An audio signal makes its way through the nodes via the various connections, or [modular routing](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html#ModularRouting-section), from one node to the next.

Regardless of how many nodes exist and how they are connected, the signal always terminates at the [AudioDestinationNode](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html#AudioDestinationNode-section)—essentially, the speaker output through which a user hears the final result.

The simplest connection case, then, consists of a web app with a context that contains one source node (a previously-loaded sound in this case) whose output is connected directly to the input of one destination node (the speakers), as shown below. That's the case we're going to cover in this tutorial.

*A context with one source and one destination* ![wap1b-basic-trans.gif](/assets/public/6/6e/wap1b-basic-trans.gif)

## Producing a sound

### Step 1: Create a context

As stated above, each web page/app needs only one context within which to process audio. The context is declared with a JavaScript statement.

``` js
var context = new webkitAudioContext();
```

**Note:** We're using the *webkit* prefix because, so far, the web audio API has only limited support in modern browsers. See the compatibility tables at the end of this article for the latest information.

Typically, we would create the context as a global variable so that it's available to later functions. We could simply declare the variable and assign an audio context to it in one statement as shown above or, more elegantly, we could declare it first and then assign the audio context to it later via a function called from a button click or other event, so we can check for errors.

``` js
var context;
function initcontext() {
  try {
    context = new webkitAudioContext();
  }
  catch(e) {
    alert('Sorry, your browser does not support the Web Audio API.');
  }
}
```

 Having created the audio context for the page, we're ready to move on.

### Step 2: Define a buffer

External sounds (i.e., audio files) must be loaded into the app in preparation for playing. The storage location used for the audio is an [AudioBuffer](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html#AudioBuffer-section). For simplicity and ease of access, we'll again declare the buffer as a global variable with an initial value of `null`.

``` js
var myAudioBuffer = null;
```

 That's all we have to do; the buffer is now defined and ready to receive audio data.

**Note:** Bear in mind that you don't *have* to use a buffer as a source node. In this example, we use one because we're loading the audio from an external sound file. You can also use other input sources such as oscillators, JavaScript nodes, and [live input](http://updates.html5rocks.com/2012/09/Live-Web-Audio-Input-Enabled) to acquire an audio stream to be processed and played.

### Step 3: Load a sound

The load process is typically accomplished with an [XMLHttpRequest](https://developer.mozilla.org/En/XMLHttpRequest/Using_XMLHttpRequest) (often just called an XHR). The XHR can be called programmatically based on page load status, timing, or user interaction such as a button click (as we'll do later).

``` js
var url = "mysound.mp3";
function loadSound(url) {
  var request = new XMLHttpRequest();
  request.open('GET', url, true);
  request.responseType = 'arraybuffer';
  // . . . step 3 code above this line, step 4 code below
  request.onload = function() {
    context.decodeAudioData(request.response, function(buffer) {
      myAudioBuffer = buffer;
    });
  }
  request.send();
}
```

 In the first part of the function (above the comment line), the URL of the sound to be loaded is set into a global variable called `url`. The `loadSound()` function sets up an XHR and uses the `open` method to request a `GET` of the file, defining the `responseType` property as `arraybuffer` (this allows the XHR to load the audio as binary data).

**Note:** XHRs don't work on a local machine—they must be executed on a server, e.g., `http://localhost/~myserver/` or `http://www.mysite.com/`, etc.

But, loading the file only gets us halfway there; next, it must be *decoded*.

### Step 4: Decode the audio

In the second part of the function (below the comment line), the audio data is decoded so that it can be used in the page. This is accomplished by passing an anonymous function (`function()`) to the XHR's `onload` method.

This anonymous function uses the context's `decodeAudioData` method to decode the data, which resides in the request's `response` property. It then executes a *callback* function (the second parameter, `function(buffer)`). (A callback is a function passed as an argument to another function, which forces it to execute *asynchronously*, that is, to postpone its own execution until after its parent function has completed.) The callback, having waited for the audio stream to be decoded, now simply assigns it to our previously defined buffer.

Finally, the XHR's `send()` method is used to send the task to the server for execution and thus wrap up the function. Our audio file is now loaded and decoded, and the decoded data is stored in an audio buffer, ready for use.

### Step 5: Play the audio

At last we're ready to play the sound. This is achieved through the "connect the nodes" process described and diagrammed earlier. We can define a single function to play our new sound, or any other, as long as we pass it a buffer containing the decoded audio (or other valid source node). Let's assume we'll execute the `playSound()` function on a button click.

``` js
var source = null;
function playSound(anybuffer) {
  source = context.createBufferSource();
  source.buffer = anybuffer;
  source.connect(context.destination);
  source.start();
  //source.noteOn(0); //see note in Step 6
}
```

 Recall that to produce sound we need *source* and *destination* nodes, and that the former must be connected to the latter. As before, we first declare a global variable, `source`, for the node. In the function, the source node is created first, using the context's `createBufferSource()` method. Next, the source node's `buffer` property is loaded with the `anybuffer` parameter which we'll pass as an argument into the function (in this case, the buffer containing our decoded audio, `myAudioBuffer`).

We don't have to explicitly create the context's `destination` node—it's present by default—but we do have to connect the source to it. This is done using the source node's `connect()` method, passing it the `context.destination` node. The sequence is complete: we now have a source node containing a sound whose output is connected to the input of a destination node representing the speakers.

Finally, we can play the sound (hooray!) using the source node's `start()` method, which plays the audio data from beginning to end unless stopped programmatically. And how, you might ask, would that be done? With the source node's complementary `stop()` method, of course.

### Step 6: Stop the audio

``` js
function stopSound() {
  if (source) {
    source.stop();
    //source.noteOff(0); //see note below
  }
}
```

> ***Note:** The `noteOn(0)` and `noteOff(0)` method names are slated to change to `start()` and `stop()`, as noted in the examples' comments, but as of this writing (October 2012) this change has not been fully implemented. See the web audio specification's [deprecation section](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html#deprecation-section) for more information, and always test applications to ensure that they use the currently supported syntax.*

## The completed example

Having examined the required steps in bits and pieces, let's now take a look at a complete, working page that loads, decodes, and plays a sound. In this example, we assume that the file "mysound.mp3" exists in the same location as the page, and that the page and the sound reside on a server (either local or remote) so that the XHR will work.

``` html
<!DOCTYPE html>
<html>
<head>
<script>
//Step 1
var context;
function initContext() {
  try {
    context = new webkitAudioContext();
    alert("context created"); //test
  }
  catch(e) {
    alert('Sorry, your browser does not support the Web Audio API.');
  }
}

//Step 2
var myAudioBuffer = null;

//Steps 3 and 4
var url = "mysound.mp3";
function loadSound(url) {
  var request = new XMLHttpRequest();
  request.open('GET', url, true);
  request.responseType = 'arraybuffer';
  // . . . step 3 code above this line, step 4 code below
  request.onload = function() {
    alert("sound loaded"); //test
    context.decodeAudioData(request.response, function(buffer) {
      myAudioBuffer = buffer;
      alert("sound decoded"); //test
    });
  }
  request.send();
}

//Step 5
var source = null;
function playSound(anybuffer) {
  source = context.createBufferSource();
  source.buffer = anybuffer;
  source.connect(context.destination);
  source.start();
  //source.noteOn(0); //see note in Step 6 text
}

//Step 6
function stopSound() {
  if (source) {
    source.stop();
    //source.noteOff(0); //see note in Step 6 text
  }
}
</script>
</head>

<body>
  <p>Web audio API example: load a sound file and play/stop it on a button click.</p>
  <button onclick="initContext()">Init</button>
  <button onclick="loadSound(url)">Load</button>
  <button onclick="playSound(myAudioBuffer)">Play</button>
  <button onclick="stopSound()">Stop</button>
</body>
</html>
```

 In this page, we set up four buttons—intended to be clicked in order—that perform, respectively, steps 1, 3 & 4, 5, and 6. (Step 2, declaring the audio buffer, is performed inline as the scripts load.) To see the page in action:

1.  Save the code to an HTML5 (.htm, .html) file.
2.  Place the page file and an audio file of your choice into a folder on a web server. Either name the file "mysound.mp3" or change the value of the `url` variable in the first line of the "Steps 3 and 4" code block to match your file name.
3.  Open the page on the server in a webkit-compatible browser.
4.  Click the **Init** button. The "context created" alert appears. Click **OK**.
5.  Click the **Load** button. The "sound loaded" alert appears. Click **OK**.
6.  Immediately, the "sound decoded" alert appears. Click **OK**.
7.  Click the **Play** button. The sound plays.
8.  Optional: During playback (assuming the sound plays long enough), click the **Stop** button. The sound stops.

## Not the end

This concludes part 1 of the tutorial. [Part 2 continues with inserting processor nodes between the source and destination to modify the audio before it is played](/tutorials/intro_web_audio_api_2).

## References

-   Chris Wilson's [Google I/O 2012 session video](https://developers.google.com/events/io/sessions/gooio2012/221/)
-   The W3C's [web audio specification](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html)
-   Eric Bidelman's [how-to article](http://ericbidelman.tumblr.com/post/13471195250/web-audio-api-how-to-playing-audio-based-on-user)
-   Boris Smus's [getting started article](http://www.html5rocks.com/en/tutorials/webaudio/intro/)
