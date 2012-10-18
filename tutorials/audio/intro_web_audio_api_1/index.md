{{Page_Title|Using the web audio API, part 1}}
{{Flags
|High-level issues=Needs Flags
}}
{{Byline
|Name=Dave Gash
|URL=http://docs.webplatform.org/wiki/User:Dgash
|Published=October 18, 2012
}}
{{Summary_Section|An introduction to the web audio API.}}
{{Tutorial
|Content==Using the web audio API, part 1 of 2=

==Introduction==
Web-based audio is becoming more robust all the time, and necessarily so. As the web evolves in stylistic and presentational features, web applications also require a higher degree of sophistication in audio manipulation. Gone are the days of <code>&lt;embed&gt;</code>, <code>&lt;object&gt;</code>, and <code>&lt;bgsound&gt;</code>, when the best you could hope for was a constant, cheesy MIDI file playing in your page, annoying visitors who are trying to read your content.

Today, diverse web apps such as games, audio editors, playlist managers, ringtone stores, musicians' utilities, and more have a need for subtlety and finesse in their use of audio, and users deserve&mdash;and have come to expect&mdash;power and flexibility in those apps.

'''Note:''' The web audio API is not to be confused with the HTML5 <code>&lt;audio&gt;</code> element. For information on that element, see [http://www.w3.org/wiki/HTML/Elements/audio this W3C article], [http://www.html5rocks.com/en/tutorials/audio/quick/ this HTML5Rocks! tutorial], or [http://www.w3schools.com/tags/tag_audio.asp this W3Schools page].

As useful as the <code>&lt;audio&gt;</code> element is in terms of encapsulating the load-decode-play sequence (more about that later), it doesn't include capabilities to precisely control sounds, time them, or fine-tune their playback characteristics. Enter the ''web audio API''.

The web audio API is high-level JavaScript interface that is about much more than just playing sounds. With it, you can process, synthesize, mix, visualize, filter, and otherwise manipulate audio data with extreme precision to accomplish tasks and achieve results previously found only in high-end commercial audio applications.

In this tutorial, part 1 of 2, we'll explore the basics of the API and learn how to load, start, and stop a sound before moving on to more complex tasks.

==Prerequisite concepts==
To effectively use the web audio API, certain things must happen in a certain order; it's that sequence of events we'll explore next. But first, we need to understand a couple of concepts, called ''context'' and ''nodes'', and how they relate to each other.

API sound manipulation takes place within an [https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html#AudioContext-section AudioContext]. A context can be thought of as a master container inside which your web page does all of its audio processing. A major benefit of this "sandbox" approach is that it isolates all the audio work&mdash;even the most complex and demanding processes&mdash;into an independent, high-priority thread and thus prevents this CPU-intensive work from interfering with other events (visual or aural) and marring the user experience.

The context allows for the creation of one or more [https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html#AudioNode-section AudioNode]s, all of which reside in the context. Nodes are the building blocks of audio processing, and may be ''input'', ''processor'', or ''output'' types. 

Nodes may have input and/or output connections, which are used to string them together into a sequence. An audio signal makes its way through the nodes via the various connections, or [https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html#ModularRouting-section modular routing], from one node to the next.

Regardless of how many nodes exist and how they are connected, the signal always terminates at the [https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html#AudioDestinationNode-section AudioDestinationNode]&mdash;essentially, the speaker output through which a user hears the final result.

The simplest connection case, then, consists of a web app containing a context that contains one source node (a previously-loaded sound) whose output is connected directly to the input of one destination node (the speakers), as shown below. That's the case we're going to cover in this tutorial.

[[image:wap1-basic-trans.png]]<br/>
''A context with one source and one destination''

==Producing a sound==

===Step 1: Create a context===
As stated above, each web page/app needs only one context within which to process audio. The context is declared with a JavaScript statement.

<syntaxhighlight lang="javascript">
var context = new webkitAudioContext();
</syntaxhighlight>

'''Note:''' We're using the ''webkit'' prefix because, so far, the web audio API has only limited support in modern browsers. See the compatibility tables at the end of this article for the latest information.

Typically, we would create the context as a global variable so that it's available to later functions. We could simply execute the statement declaring the variable and assigning an audio context to it in one statement as shown above or, more elegantly, we could declare it first and then assign the audio context to it later via a function called from a button click or other event, so we can check for errors.

<syntaxhighlight lang="javascript">
var context;
function initcontext() {
  try {
    context = new webkitAudioContext();
  }
  catch(e) {
    alert('Sorry, your browser does not support the Web Audio API.');
  }
}
</syntaxhighlight>

Having created the audio context for the page, we're ready to move on.

===Step 2: Define a buffer===
External sounds (i.e., audio files) must be loaded into the app in preparation for playing. The storage location used for the audio is an [https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html#AudioBuffer-section AudioBuffer]. For simplicity and ease of access, we'll again declare the buffer as a global variable with an initial value of <code>null</code>.

<syntaxhighlight lang="javascript">
var myAudioBuffer = null;
</syntaxhighlight>

That's all we have to do; the buffer is now defined and ready to receive audio data.

===Step 3: Load a sound===
The load process is typically accomplished with an [https://developer.mozilla.org/En/XMLHttpRequest/Using_XMLHttpRequest XMLHttpRequest] (often just called an XHR). The XHR can be called programmatically based on page load status, timing, or user interaction such as a button click (as we'll do later).

<syntaxhighlight lang="javascript">
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
</syntaxhighlight>

In the first part of the function (above the comment line), the URL of the sound to be loaded is set into a global variable called <code>url</code>. The <code>loadSound()</code> function sets up an XHR and uses the <code>open</code> method to request a <code>GET</code> of the file, defining the <code>responseType</code> property as <code>arraybuffer</code> (this allows the XHR to load the audio as binary data).

'''Note:''' XHRs don't work on a local machine&mdash;they must be executed on a server, e.g., <code><nowiki>http://localhost/~myserver/</nowiki></code> or <code><nowiki>http://www.mysite.com/</nowiki></code>, etc.

But, loading the file only gets us halfway there; next, it must be ''decoded''.

===Step 4: Decode the audio===
In the second part of the function (below the comment line), the audio data is decoded so that it can be used in the page. This is accomplished by passing an anonymous function (<code>function()</code>) to the XHR's <code>onload</code> method. 

This anonymous function uses the context's <code>decodeAudioData</code> method to decode the data, which resides in the request's <code>response</code> property. It then executes a ''callback'' function (the second parameter, <code>function(buffer)</code>). (A callback is a function passed as an argument to another function, which forces it to execute ''asynchronously'', that is, to postpone its own execution until after its parent function has completed.) The callback, having waited for the audio stream to be decoded, now simply assigns it to our previously defined buffer.

Finally, the XHR's <code>send()</code> method is used to send the task to the server for execution and thus wrap up the function. Our audio file is now loaded and decoded, and the decoded data is stored in an audio buffer, ready for use.

===Step 5: Play the audio===
At last we're ready to play the sound. This is achieved through the "connect the nodes" process described and diagrammed earlier. We can define a single function to play our new sound, or any other, as long as we pass it a buffer containing the decoded audio. Let's assume we'll execute the <code>playSound()</code> function on a button click.

<syntaxhighlight lang="javascript">
var source = null;
function playSound(anybuffer) {
  source = context.createBufferSource();
  source.buffer = anybuffer;
  source.connect(context.destination);
  source.noteOn(0);
}
</syntaxhighlight>

Recall that to produce sound we need ''source'' and ''destination'' nodes, and that the former must be connected to the latter. As before, we first declare a global variable, <code>source</code>, for the node. In the function, the source node is created first, assigning the context's <code>createBufferSource()</code> method to the variable. Next, the source node's <code>buffer</code> property is loaded with the <code>anybuffer</code> parameter which we'll pass as an argument into the function (in this case, the buffer containing our decoded audio, <code>myAudioBuffer</code>). 

We don't have to explicitly create the context's <code>destination</code> node&mdash;it's present by default&mdash;but we do have to connect the source to it. This is done using the source node's <code>connect()</code> method, passing it the <code>context.destination</code> node. The sequence is complete: we now have a source node containing a sound whose output is connected to the input of a destination node representing the speakers.

Finally, we can play the sound (hooray!) using the source node's <code>noteOn(0)</code> method, which plays the audio data from beginning to end unless stopped programmatically. And how, you might ask, would that be done? With the source node's complementary <code>noteOff(0)</code> method, of course.

===Step 6: Stop the audio===
<syntaxhighlight lang="javascript">
function stopSound() {
  if (source) {
    source.noteOff(0);
  }
}
</syntaxhighlight>

And we're done!

==The completed example==
Having examined the required steps in bits and pieces, let's now take a look at a complete, working page that loads, decodes, and plays a sound. In this example, we assume that the file "mysound.mp3" exists in the same location as the page, and that the page and the sound reside on a server (either local or remote) so that the XHR will work.

<syntaxhighlight lang="html5">
<!DOCTYPE html>
<html>
<head>
<script>
//Step 1
var context;
//window.addEventListener('load', initContext, false);
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
  source.noteOn(0);
}

function stopSound() {
  if (source) {
    source.noteOff(0);
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
</syntaxhighlight>

In this page, we set up four buttons&mdash;intended to be clicked in order&mdash;that perform, respectively, steps 1, 3 &amp; 4, 5, and 6. (Step 2, declaring the audio buffer, is performed inline as the scripts load.) To see the page in action:
#Save the code to an HTML5 (.htm, .html) file.
#Place the page file and an audio file of your choice into a folder on a web server. Either name the file "mysound.mp3" or change the value of the <code>url</code> variable in the first line of the "Steps 3 and 4" code block to match your file name.
#Open the page on the server in a webkit-compatible browser.
#Click the '''Init''' button. The "context created" alert appears. Click '''OK'''.
#Click the '''Load''' button. The "sound loaded" alert appears. Click '''OK'''. 
#Immediately, the "sound decoded" alert appears. Click '''OK'''.
#Click the '''Play''' button. The sound plays.
#Optional: During playback (assuming the sound plays long enough), click the '''Stop''' button. The sound stops.

==(Not) the end==
This concludes part 1 of the tutorial. '''Part 2''', coming soon, continues with inserting processor nodes between the source and destination to modify the audio before it is played.

==References==
*Chris Wilson's [https://developers.google.com/events/io/sessions/gooio2012/221/ Google I/O 2012 session video] 
*The W3C's [https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html web audio specification]
*Eric Bidelman's [http://ericbidelman.tumblr.com/post/13471195250/web-audio-api-how-to-playing-audio-based-on-user how-to article]
*Boris Smus's [http://www.html5rocks.com/en/tutorials/webaudio/intro/ getting started article]
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=21.0
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=6.0
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Yes
|Safari_mobile_prefixed_version=6.0
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Audio}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}