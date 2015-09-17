---
title: 'Introduction to the web audio API, part 2'
readiness: 'Ready to Use'
summary: 'An introduction to the web audio API: inserting processor nodes between source and destination.'
tags:
  - Tutorials
  - Audio
uri: 'tutorials/audio/intro web audio api 2'

---
**By [Dave Gash](/User:Dgash)**
Originally published November 7, 2012

## Summary

An introduction to the web audio API: inserting processor nodes between source and destination.

## Introduction

Web-based audio is becoming more robust all the time, and necessarily so. As the web evolves in stylistic and presentational features, web applications also require a higher degree of sophistication in audio manipulation. Gone are the days of `<embed>`, `<object>`, and `<bgsound>`, when the best you could hope for was static playback of a fixed music track.

Today, diverse web apps such as games, audio editors, playlist managers, ringtone stores, musicians' utilities, and more have a need for subtlety and finesse in their use of audio, and users deserve—and have come to expect—power and flexibility in those apps.

The web audio API is not to be confused with the HTML5 `<audio>` element. For information on that element, see [this W3C article](http://www.w3.org/wiki/HTML/Elements/audio) or [this HTML5Rocks! tutorial](http://www.html5rocks.com/en/tutorials/audio/quick/). As useful as the `<audio>` element is in terms of encapsulating the load-decode-play sequence (more about that later), it doesn't include capabilities to precisely control sounds, time them, or fine-tune their playback characteristics. Enter the *web audio API*.

The web audio API is high-level JavaScript interface that is about much more than just playing sounds. With it, you can process, synthesize, mix, visualize, filter, and otherwise manipulate audio data with extreme precision to accomplish tasks and achieve results previously found only in high-end commercial audio applications.

In [Part 1](/tutorials/intro_web_audio_api_1) of this tutorial, we explored the basics of the API; in this part, we'll learn how to insert a processor node in the audio path and use it to modify the sound between the source and destination nodes.

## A quick recap of part 1

First, recall that all API sound manipulation takes place within an [AudioContext](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html#AudioContext-section). A context can be thought of as a master container inside which your web page does all of its audio processing. A major benefit of this "sandbox" approach is that it isolates all the audio work—even the most complex and demanding processes—into an independent, high-priority thread and thus prevents this CPU-intensive work from interfering with other events (visual or aural) and marring the user experience.

Second, the audio context allows for the creation of one or more [AudioNode](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html#AudioNode-section)s, all of which reside in the context. Nodes are the building blocks of audio processing, and may be *input*, *processor*, or *output* types.

Finally, nodes may have input and/or output connections, which are used to string them together into a sequence. An audio signal makes its way through the nodes via the various connections, or [modular routing](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html#ModularRouting-section), from one node to the next, terminating at the [AudioDestinationNode](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html#AudioDestinationNode-section)—essentially, the speaker output through which a user hears the final result.

The simplest connection case, then, consists of a web app with a context that contains one source node (a previously-loaded sound in this case) whose output is connected directly to the input of one destination node (the speakers), as shown below. That's the case we covered in Part 1.

*A context with one source and one destination* ![wap1b-basic-trans.gif](/assets/public/6/6e/wap1b-basic-trans.gif)

## In part 2

The next reasonable step is a connection case that consists of a web app with a context that contains a source node and a destination node, but with one or more processing nodes between them. A processing node modifies the sound in some way—volume, EQ, pitch, phase, etc.—after it is output from the source node but before it is input to the destination node, as shown below. That's the case we'll cover in this part.

*A context with a processor between the source and destination* ![wap2b-basic-trans.gif](/assets/public/7/7a/wap2b-basic-trans.gif)

Be sure you understand how the nodes are created and linked together as described in [Part 1](/tutorials/intro_web_audio_api_1) before proceeding with this part of the tutorial.

## A simple processor node

One of the most common (and useful) things we might do to a sound is control its volume during playback, either programmatically, via user interaction, based on timing, etc. We can do this by inserting a gain node into the audio path.

Interestingly, this is a very simple procedure. First, we create a gain node within the audio context using the `createGainNode` method.

``` js
var gainNode = context.createGainNode();
```

 Bear in mind that a gain node is just one of the many built-in processor node types available to an audio context. Other processors are available to control delay, pan, spatialization, splitting, merging, compression, filtering, and more. See the [W3C Web Audio API specification](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html) for a complete list.

## The new connection

This time, rather than connecting the source node directly to the destination node, we route the source into the gain node, and from there to the destination node. That is, instead of this:

``` js
source.connect(context.destination);
```

 we do this:

``` js
source.connect(gainNode);
gainNode.connect(context.destination);
```

 Then, it's just a matter of setting the gain node's value to something less than 1.0 to achieve a lower volume prior to playback. Again, this might be accomplished via a user interface element, a timing mechanism, or, as done here, a simple JavaScript statement.

``` js
gainNode.gain.value = 0.5;
```

 And the sound is ready to play at half volume.

## The modified function

Using the function from Step 5 (Play the audio) in Part 1, we add the four lines above to create a modified function, `playSoundHalf()` (let's call it Step 5.5), that might look like this.

``` js
//Step 5.5
var source = null;
function playSoundHalf(anybuffer) {
  source = context.createBufferSource();
  source.buffer = anybuffer;

  var gainNode = context.createGainNode();
  source.connect(gainNode);
  gainNode.connect(context.destination);
  gainNode.gain.value = 0.5;

  source.start();
  //source.noteOn(0); //see note in Step 6
}
```

 Like the other functions in our example, we'll call this new function from a button.

> ***Note:** The `noteOn(0)` and `noteOff(0)` method names are slated to change to*
>
> `start()` and `stop()`, as noted in the examples' comments, but as of this writing (November 2012) this change has not been fully implemented. See the web audio specification's [deprecation section](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html#deprecation-section) for more
>
> information, and always test applications to ensure that they use the currently supported syntax.

## The completed example

Having examined the required steps in bits and pieces, let's now take a look at a complete, working page that loads, decodes, and plays a sound, including a new button that plays it at half volume. In this example, we assume that the file "mysound.mp3" exists in the same location as the page, and that the page and the sound reside on a server (either local or remote) so that the XHR will work.

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


//Step 5.5
var source = null;
function playSoundHalf(anybuffer) {
  source = context.createBufferSource();
  source.buffer = anybuffer;
  var gainNode = context.createGainNode();
  source.connect(gainNode);
  gainNode.connect(context.destination);
  gainNode.gain.value = 0.5;
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
  <button onclick="playSoundHalf(myAudioBuffer)">Play half volume</button>
  <button onclick="stopSound()">Stop</button>
</body>
</html>
```

 In this page, we set up five buttons—intended to be clicked in order—that perform, respectively, steps 1, 3 & 4, 5, 5.5, and 6. (Step 2, declaring the audio buffer, is performed inline as the scripts load.) To see the page in action:

1.  Save the code to an HTML5 (.htm, .html) file.
2.  Place the page file and an audio file of your choice into a folder on a web server. Either name the file "mysound.mp3" or change the value of the `url` variable in the first line of the "Steps 3 and 4" code block to match your file name.
3.  Open the page on the server in a webkit-compatible browser.
4.  Click the **Init** button. The "context created" alert appears. Click **OK**.
5.  Click the **Load** button. The "sound loaded" alert appears. Click **OK**.
6.  Immediately, the "sound decoded" alert appears. Click **OK**.
7.  Click the **Play** button. The sound plays.
8.  Click the **Play half volume** button. The sound plays at half its full volume.
9.  Optional: During playback (assuming the sound plays long enough), click the **Stop** button. The sound stops.

## Adding processors

As a final example, let's modify the Step 5.5 `playSoundHalf()` function to include a low-pass filter as a second inline processor. First, we create a filter node within the audio context using the `createBiquadFilter()` method and set its filter type to 0 (low-pass) and cutoff value to 440 Hz (A4). (See the [Biquad filter section](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html#BiquadFilterNode-section) of the specs for more information on this filter.)

``` js
var filterNode = context.createBiquadFilter();
filterNode.type = 0;
filterNode.frequency.value = 440;
```

 Then, we insert the filter between the gain node and the destination. That is, instead of this:

``` js
gainNode.connect(context.destination);
```

 we do this:

``` js
gainNode.connect(filterNode);
filterNode.connect(context.destination);
```

 The sound's path is now **audio buffer \> gain node \> filter node \> destination**, and the modified function looks like this:

``` js
//Step 5.5
var source = null;
function playSoundHalf(anybuffer) {
  source = context.createBufferSource();
  source.buffer = anybuffer;
  var gainNode = context.createGainNode();
  source.connect(gainNode);
  gainNode.gain.value = 0.5;

  var filterNode = context.createBiquadFilter();
  filterNode.type = 0;
  filterNode.frequency.value = 440;
  gainNode.connect(filterNode);
  filterNode.connect(context.destination);

  source.start();
  //source.noteOn(0); //see note in Step 6 text
}
```

 The sound will now play at half its original volume *and* frequencies above 440 Hz will be attenuated.

## Summary

As you can see, adding one or more processors to the sound stream is a fairly simple matter of defining the processor(s) and then connecting the inputs and outputs. In this way, you can construct audio paths that include serial (sequential) and/or parallel (simultaneous) processors to achieve sophisticated audio effects.

## References

-   Chris Wilson's [Google I/O 2012 session video](https://developers.google.com/events/io/sessions/gooio2012/221/)
-   The W3C's [web audio specification](https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html)
-   Eric Bidelman's [how-to article](http://ericbidelman.tumblr.com/post/13471195250/web-audio-api-how-to-playing-audio-based-on-user)
-   Boris Smus's [getting started article](http://www.html5rocks.com/en/tutorials/webaudio/intro/)
