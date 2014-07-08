{{Page_Title|An introduction to the Web Audio API}}
{{Flags
|Checked_Out=No
}}
{{Byline
|Name=Stuart Memo
|URL=http://stuartmemo.com
|Published=June 13th, 2012
}}
{{Summary_Section|The [https://dvcs.w3.org/hg/audio/raw-file/tip/webaudio/specification.html Web Audio API] is a way of creating and manipulating audio within the browser. It&#8217;s a specification proposed by Google, and as such is currently only available in [https://www.google.com/intl/en/chrome/browser/ Chrome], with the hope other browsers adopting it and it becoming a standard.

The actual audio processing itself is done with Assembly/C/C++ code within the browser, but the API gives us a nice high-level way of interacting with this code using JavaScript.
}}
{{Tutorial
|Content==== AudioContext ===
In order to start using the API, we must first create an AudioContext. Think of this as a canvas for sound. It&#8217;s a container for all the playback and manipulation of audio we&#8217;re going to be doing. We create it by simply doing this:
<syntaxHighlight lang="javascript">
    var context = new webkitAudioContext();
    // We use the "webkit" prefix as the API isn't a standard yet
</syntaxHighlight>
<p>Now that we&#8217;ve created this container, what do we put in it? Well, this is where the concept of nodes and modular routing comes in.</p>
<h2>Nodes and modular routing</h2>
<p>Imagine a guitar player who has an electric guitar, a distortion pedal and an amp. When the guitar player strums her guitar, the sound travels from the guitar, down a cable, through the distortion pedal, and down another cable before finally coming out the speaker of the guitar amp. This chain is very similar to the nodes and modular routing model of the Web Audio API. The guitar, distortion pedal and the amp are all nodes, which we&#8217;ve routed in the correct order using cables.</p>
<div id="audio-context-diagram"></div>

== Playing a sound file ==
Ok, time to stop mucking about with concepts and learn how to play an audio file using the Web Audio API. Let&#8217;s start coding by declaring a couple of variables:
<syntaxHighlight lang="javascript">
    var context = new webkitAudioContext(),
        buffer;
</syntaxhighlight>
<p>We already know about <code>context</code>, but what are we going to use <code>buffer</code> for? Well, audio buffers are essentially a holding place in memory for sound data. We read data into a buffer from an audio file using an <a href="http://www.html5rocks.com/en/tutorials/file/xhr2/">XMLHttpRequest</a> like so:</p>
<syntaxHighlight lang="javascript">
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
</syntaxHighlight>
<p>Using an XMLHttpRequest allows us to tell the browser that we&#8217;re not loading a normal text file. By specifying <code>arraybuffer</code>, we&#8217;re flagging up the fact that we&#8217;re expecting binary data. Once we receive that chunk of data from the server, and because we know it&#8217;s an audio file (audiophile! ha!), we decode this data using <code>context.decodeAudioData</code> and specify an anonymous function as the callback that is passed the decoded data in a handy audio buffer that&#8217;s ready to be played. To do so though, we need to write a playback function.</p>
<syntaxHighlight lang="javascript">
    var playAudioFile = function (buffer) {
        var source = context.createBufferSource();

        source.buffer = buffer;
        source.connect(context.destination);
        source.noteOn(0); // Play sound immediately
    };
</syntaxHighlight>
In the above code <code>source</code> is the guitar in our analogy. It&#8217;s the very first node in our chain, and in this case we&#8217;re telling it that the source of the audio is from the buffer we just loaded. We then use <code>source.connect(context.destination)</code> to use a lead to connect the sound source to the speakers, <code>context.destination</code>, and <code>source.noteOn(0)</code> to play the sound after 0 seconds.</p>
<p>Let&#8217;s put all of this together and see what we get:</p>
<syntaxHighlight lang="javascript">
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
</syntaxHighlight>
<p>Reference this in an HTML file, make a cup of tea and relax while you enjoy the sounds of your choosing in the browser.</p>
<p>I wouldn&#8217;t have been able to write this article without [http://smus.com Boris Smus]&#8217; code examples on [http://www.html5rocks.com/en/tutorials/webaudio/intro/ HTML5 Rocks] so check it out!</p>
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=Yes
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=Yes
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=iOS6
|Safari_mobile_prefixed_supported=Yes
|Safari_mobile_prefixed_version=iOS6
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