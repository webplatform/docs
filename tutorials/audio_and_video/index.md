{{Page_Title|HTML5 <audio> and <video>}}
{{Flags}}
{{Byline}}
{{Summary_Section|HTML5 has improved embedding of audio and video by providing native support for many different file types. In this guide, we'll cover the various ways to embed audio and video, including browser compatibility and frameworks to streamline cross-browser compatibility.}}
{{Tutorial
|Content=== Playing Audio ==

HTML5 introduced <code>&lt;audio&gt;</code> tag, as well as the JavaScript APIs, which allow the browser to play audio without the need for an external plugin. The most supported codecs for playing audio in HTML5 are Ogg Vorbis, MP3, and Wav. There is currently no single codec that plays across all browsers. To get around the potential for codec incompatibility, HTML5 allows you to specify multiple source files. The browser looks for the first mime-type it knows it can support.

A simple implementation with only one source looks like this: 

 &lt;audio src="file.mp3"&gt; &lt;/audio&gt;

An implementation with multiple sources looks like this: 

 &lt;audio controls&gt;
     &lt;source src="song.ogg"&gt;
     &lt;source src="song.mp3"&gt;
     Sorry, but your browser doesn't support audio.
 &lt;/audio&gt;

If the browser doesn't support the audio element, then it will display the message, "Sorry, but your browser doesn't support audio."

=== Helpful Libraries ===
Unfortunately, despite the inclusion of the HTML5 <code>&lt;audio&gt;</code> tag, there is still some friction in embedding audio and having that work seamlessly across all browsers and devices. 

Handling multiple devices and browsers is made easier by using a library such as [http://www.schillmania.com/projects/soundmanager2/ Sound Manager 2] or [http://buzz.jaysalvat.com/ Buzz]. 

These libraries handle most of the inconsistencies around embedding audio, and let you focus on creating awesome web applications. Both of them provide graceful degradation to handle non-HTML5 browsers.

=== Javascript API ===
The HTML5 Audio Javascript API allows for programmatic control of loading and playing audio files. The API is very straightforward, and provides a robust way to control embedded audio. 

Here’s a simple example.  In this example, we’ll add a song, jump to 30 seconds into the song, and play it.

 var audioElem = document.createElement('audio');
 audioElem.setAttribute('src', 'Crystal Castles - Untrust Us.ogg');
 audioElem.currentTime = 30;
 audioElem.play();

Retrieve the filename and duration:

 audioElement.src;
 audioElement.duration;

=== Additional Reading ===
For a great tutorial with sample code that explains how to work with audio in the browser, see the [http://thinkvitamin.com/code/html5-audio-unplugged/ ThinkVitamin audio tutorial].  Also, HTML5Rocks' Playground has [http://playground.html5rocks.com/#audio_tag sample code] to help you get started.

== Playing Video ==

Similar to audio, the <code>&lt;video&gt;</code> tag has been introduced in the HTML5 spec, allowing web developers to harness the ability to play video without relying on third-party plugins. Support for various video/audio codecs varies from browser to browser, so it is imperative that you plan for all potential browsers and devices when creating your web application. 

Browser compatibility information for [http://caniuse.com/#search=ogg Ogg/Theora], [http://caniuse.com/#search=webm WebM/VP8], and [http://caniuse.com/#search=mpeg H.264] can be found at [http://caniuse.com/#search=video CanIUse.com]. 

Apple has [http://www.apple.com/html5/showcase/video/ launched a site] that showcases the possibilities of HTML5 Video. More demos are available at [http://html5video.org/blog/demos/ html5video.org]. 

At its simplest form, an HTML5 video embed looks much like the audio example from above.  Here’s how to add a video to your web app.

 &lt;video src="fb.ogv"&gt;&lt;video&gt;

Since there is no single codec and container combination that is supported across all browsers, you will need to specify multiple sources. The browser will start at the first stream listed and go through all of them until it can successfully play one. It is important to specify the <code>type</code> field when embedding video. This tells the browser what the container type is, along with information about the video and audio codecs. If you do not specify the type field, the browser has to download a portion of each video until it can find one that it can successfully play.

 &lt;video controls>
   &lt;source src="fb.ogv" type='video/ogg; codecs="theora, vorbis"'>
   &lt;source src="fb.mp4" type='video/mp4; codecs="avc1.42E01E, mp4a.40.2"'>
   &lt;source src="fb.webm" type='video/webm; codecs="vp8, vorbis"'>
 &lt;/video>

A more in-depth discussion of types and syntax is available at [http://diveintohtml5.org/video.html#markup Dive Into HTML5].

=== Flash Fallback ===
A fallback to Flash should be included, as it allows you to embed video on browsers that may not support your video source types. Adding in support to fallback to Flash is straightforward. Using the example above, we can add in support for Flash by adding it as a last option:

 &lt;video controls width="640" height="480">
   &lt;source src="fb.ogv" type='video/ogg; codecs="theora, vorbis"'>
   &lt;source src="fb.mp4" type='video/mp4; codecs="avc1.42E01E, mp4a.40.2"'>
   &lt;source src="fb.webm" type='video/webm; codecs="vp8, vorbis"'>
   &lt;object type="application/x-shockwave-flash" data="player.swf" width="640" height="480">
     &lt;param name="allowfullscreen" value="true">
     &lt;param name="allowscriptaccess" value="always">
     &lt;param name="flashvars" value="file=fb.mp4">
     &lt;!--[if IE]>&lt;param name="movie" value="player.swf">&lt;![endif]-->
   &lt;/object>
 &lt;/video>

=== Browser Compatibility ===

For maximum compatibility it is advisable to include:

* A video source that uses H.264 baseline video and AAC "low complexity" audio in an MP4 container.
* A video source that uses WebM (VP8 + Vorbis)
* A video source that uses Theora video and Vorbis audio in an Ogg container.
* Fallback to Flash-based video player.

Most developers wanting to leverage the power of HTML5 video will need to consider not only the browser differences, but also backwards compatibility for browsers that do not support HTML5 specs. 

Fortunately, libraries such as [http://www.videojs.com VideoJS] and [http://www.mediaelementjs.com/ MediaElement.js] simplify and streamline the process of embedding video on the web.

=== Additional Reading ===

For tutorials on how the <code>&lt;video&gt;</code> tag works and how you can get started, check out [http://diveintohtml5.info/video.html diveintohtml5].
If you'd like to jump right in, HTML5Rocks' Playground has great [http://playground.html5rocks.com/#video_tag sample code].
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Audio, JavaScript, Video}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=Facebook HTML5 Resource Center
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}