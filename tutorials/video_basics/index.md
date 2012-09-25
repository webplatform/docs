{{Flags
|High-level issues=Needs Flags
}}
{{Summary_Section|An introduction to the HTML5 video tag.}}
{{Tutorial
|Content==HTML5 Video=

====original by Ernest Delgado====
====published Aug. 3, 2010====

==Introduction==

The video tag is one of those HTML5 features that gets a lot of attention. Often presented in the media as an alternative to Flash, the video tag actually goes beyond that. Although it's recently joined the rest of the ubiquitous HTML tags, its capabilities and support across browsers have increased at an amazing speed. As you will see in this tutorial, its main advantage is the natural integration with the other layers of the web development stack such as CSS and JavaScript, as well as with the other HTML tags.

This tutorial will give you a basic understanding of the video tag and also show you various examples of different integrations with other HTML5 features, such as <code>&lt;canvas&gt;</code>.

==1. The Markup==

To make HTML video work in your site, the following lines should be sufficient.

<pre>
 &lt;video&gt;
   &lt;source src="movie.mp4" type='video/mp4; codecs="avc1.42E01E, mp4a.40.2"' /&gt;
   &lt;source src="movie.webm" type='video/webm; codecs="vp8, vorbis"' /&gt;
 &lt;/video&gt;
</pre>

This snippet uses the <code>&lt;source&gt;</code> tag which lets you include multiple formats as fallback types in case the user's browser doesn't support one of them. More about this in the next section.

You can also use a single video format which makes the syntax very similar to the image tag. This syntax will be the most used one in the near future when all browsers support one common video format.

<pre>
 &lt;video src="movie.webm"&gt;&lt;/video&gt;
</pre>

For now, we'll focus on the former case which is currently more common. ''The most important thing to remember'' is to make sure your server is serving video files with the correct MIME type, specified in the <code>Content-Type</code> header. If not, videos might not work properly, even if they are working on a local copy of your site. In an Apache httpd.conf it's enough by adding these lines:

<pre>
 AddType video/ogg .ogv
 AddType video/mp4 .mp4
 AddType video/webm .webm
</pre>

If your app is being served in a Google App Engine app then you would need to add something like the following to app.yaml (one for each format):

<pre>
 - url: /(.*\.ogv)
   static_files: videos_folder/\1
   mime_type: video/ogg
   upload: videos_folder/(.*\.ogv)
</pre>

In order to improve the client side performance it's important to remember to specify the <code>type</code> attribute in the <code>source</code> tags when dealing with multiple formats. This way, the browser can decide which format it can download and play. In other words, it won't download the ones it can't play, in order to increase the performance of the site.

==2. Video Formats==
<style>
.file_format  { color:green; }
.video_stream { color:blue; }
.audio_stream { color:red; }
</style>

Think of a <span class="file_format">video format</span> as a zip file that contains the encoded <span class="video_stream">video stream</span> and an <span class="audio_stream">audio stream</span>. The three formats you should care about for the web are webm, mp4 and ogv:

* <span class="file_format">.mp4</span> = <span class="video_stream">H.264</span> + <span class="audio_stream">AAC</span>
* <span class="file_format">.ogg/.ogv</span> = <span class="video_stream">Theora</span> + <span class="audio_stream">Vorbis</span>
* <span class="file_format">.webm</span> = <span class="video_stream">VP8</span> + <span class="audio_stream">Vorbis</span>

The speed of evolution of the video tag is really encouraging. Just a year ago the only browser that supported the video tag in its stable version was Safari. Now, most modern browsers support HTML5 video.

In [http://www.html5rocks.com/en/tutorials/video/basics/ this HTML5Rocks! article] you can see which of these formats your browser can render (you should feel lucky if you see all three of them!).

At the time of this writing (August 2010) this is the snippet that has the safest combination of formats so you can be sure your video is displayed in all browsers:

<pre>
 &lt;video&gt;
   &lt;source src="movie.webm" type='video/webm; codecs="vp8, vorbis"' /&gt;
   &lt;source src="movie.mp4" type='video/mp4; codecs="avc1.42E01E, mp4a.40.2"' /&gt;
   &lt;source src="movie.ogv" type='video/ogg; codecs="theora, vorbis"' /&gt;
   Video tag not supported. Download the video &lt;a href="movie.webm"&gt;here&lt;/a&gt;.
 &lt;video&gt;
</pre>

''Note'': Because of a bug in the iPad you will need to put .mp4 as the first option if you want the video to be loaded in that device, until the bug is fixed.

As mentioned before, most browser vendors have agreed to support a common video format. So, here is the code which will most likely be used across the web soon:

<pre>
 &lt;video&gt;
   &lt;source src="movie.webm" type='video/webm; codecs="vp8, vorbis"' /&gt;
   &lt;source src="movie.mp4" type='video/mp4; codecs="avc1.42E01E, mp4a.40.2"' /&gt;
   Video tag not supported. Download the video &lt;a href="movie.webm"&gt;here&lt;/a&gt;.
 &lt;video&gt;
</pre>

One of the main concerns about using the .mp4 format is that its video codec (h.264) is not an open codec and the licenses that a company would have to pay for using it are very complex. There's more information about this format in [http://diveintohtml5.info/video.html#licensing this video chapter].

Another issue with the .mp4 format is that the <code>type</code> attribute needs to be more specific than other formats depending on the profile used to encode the video. Although the most common is "avc1.42E01E, mp4a.40.2", you should double check at this [http://wiki.whatwg.org/wiki/Video_type_parameters#MPEG-4 profile list] to be sure.

Even though Microsoft announced the support of the video tag, as well as other HTML5 elements, its user migration rate to newer versions is typically slower than the other major browsers. Hence the following section:

==3. What happens with current IE versions that don't support the video tag?==

There are two plugins that can be used as possible solutions:

===Chrome Frame===

The advantage of using the [http://code.google.com/chrome/chromeframe/ Chrome Frame plugin] is that, once it's installed, Internet Explorer will have the support for the latest HTML, JavaScript and CSS standard features that older versions of IE don't support. This plugin has an added benefit for web developers, which is that it allows them to code applications with modern web features without leaving IE users behind. Just think the amount of time that a web developer saves without having to code hacks and workarounds for IE.

===Flash fallback===

You can also use Flash as a fallback case. Depending on the format of your video you might need to encode it again to a compatible format for the Flash player. The good news is that Adobe has committed to support the ''webm'' format in their Flash player, although that timeline is still not clear. The biggest drawback of this solution compared to the Chrome Frame plugin is that you will get the Flash player as the degraded version of what ever custom UI or enhanced features you have built for your video tag. The details of this technique can be seen in the [http://tutorials.html5rocks.com/tutorials/audio/quick/#toc-step3 Quick Guide to Implementing the HTML5 Audio] tutorial.

==4. Encode Your Videos==

If you need to encode your existing videos to the formats we mentioned in the previous section you can use [http://www.mirovideoconverter.com/ Miro Converter] for both Windows and Mac to easily get the format you need. The program doesn't allow you to tweak many settings but comes with the most common outputs for the web, including the three formats we use in this tutorial. Under the hood, this software is actually a wrapper for [http://ffmpeg.org/ ffmpeg] and [http://v2v.cc/~j/ffmpeg2theora/ ffmpeg2theora] which you can use in Windows, Mac, and Linux from the command line and specify more parameters. You can read more about this tool at [http://diveintohtml5.info/video.html#webm-cli divintohtml5.org].

==5. The Fun Part==

As we said in the introduction, the main advantage of the video tag being a member of the HTML5 family is its integration with the other layers of web development stack. In the following examples we'll give you an overview of what's possible to do with it.

===5.1. Video + other HTML===

All the common HTML attributes can now be used in the video player. For instance, in the following snippet we are using <code>tabindex</code> to make the player keyboard accessible. There are new attributes that can be used in the video tag that are also common to the audio tag such as <code>loop</code> and <code>autoplay</code>, both self-explanatory. The attribute <code>poster</code> indicates what image will be shown while the video is initially loading and, finally, <code>controls</code> is used to indicate that instead of building our custom controls we want the browser to render ones automatically for us. There's also a <code>preload</code> attribute we can use to download the video in the background as soon as the page loads, even if it hasn't started playing.

<pre>
 &lt;video poster="star.png" autoplay loop controls tabindex="0"&gt;
   &lt;source src="movie.webm" type="video/webm"; codecs="vp8, vorbis" /&gt;
   &lt;source src="movie.ogv" type="video/ogg"; codecs="theora, vorbis" /&gt;
 &lt;/video&gt;
</pre>

The full level of integration of the video tag as a native browser element avoids some issues you might have had in the past with third-party embedded players such as dropdown menus and iframes overlaying on the player or weird layout behavior when the other HTML elements surrounding the video were dynamically resized.

Because the video is not treated as an embedded foreign object, there are some other benefits that affect the user experience. For instance, even if the focus is on the player itself, actions like page scrolling or keystrokes will be completely functional.

''Note:'' If you are trying to write [http://dev.w3.org/html5/html-author/#polyglot-documents polyglot documents] to keep the XHTML syntax in the context of HTML5, then the attributes in your code should look like this:

<pre>
 &lt;video poster="star.png" autoplay="autoplay" loop="loop" controls="controls" tabindex="0"'&gt;
   &lt;source src="movie.webm" type="video/webm"; codecs="vp8, vorbis" /&gt;
   &lt;source src="movie.ogv" type="video/ogg"; codecs="theora, vorbis" /&gt;
 &lt;/video&gt;
</pre>

===5.2. Video + JS===

The video tag comes with a set of attributes and methods that give you fine control of your video from your JS code. You can see them in real time in [http://www.w3.org/2010/05/video/mediaevents.html this example].

As with any other HTML element, you can attach common events to the video tag such as drag events, mouse events, focus events, etc. But the video element comes with a bunch of new events to detect (and control) when the video is playing, paused, or finished. Because loading a video resource can have many caveats, there are equally as many events to allow control of the loading process, both at network level (<code>loadstart, progress, suspend, abort, error, emptied, stalled</code>) and at buffering level (<code>loadedmetadata, loadeddata, waiting, playing, canplay, canplaythrough</code>).

At its simplest level, you can attach the <code>canplay</code> event to start doing stuff with the video.

<pre>
 video.addEventListener('canplay', function(e) {
   this.volume = 0.4;
   this.currentTime = 10;
   this.play();
 }, false);
</pre>

There are several custom player controls available on the internet right now. In [http://www.html5rocks.com/en/tutorials/video/basics/ this HTML5Rocks! article] you can see an example that uses some elements to control two videos simultaneously and also to emulate the fast forward effect with the <code>playbackRate</code> attribute. Use the slider to toggle the volume between the videos.

===5.3. Video + CSS===

As you may have guessed, the video tag can be styled using traditional CSS properties (e.g., border, opacity, etc.) because it is a first-class citizen in the DOM. But the cool thing is that you can also style it with the latest CSS3 properties like reflections, masks, gradients, transforms, transitions, and animations.

In [http://www.html5rocks.com/en/tutorials/video/basics/ this HTML5Rocks! article] you can see an example. Hover over the video to see some of these properties in action. The CSS for this example is shown below.

<pre>
 #video-css.enhanced {
   border: 1px solid white;
   -moz-box-shadow: 0px 0px 4px #ffffff; /* FF3.5+ */
   -webkit-box-shadow: 5px 44px 28px #333; /* Saf3.0+, Chrome */
   box-shadow: 0px 0px 4px #ffffff; /* Opera 10.5, IE 9.0 */
 
   -moz-transform: translate(0, 10px);  /* FF3.5+ */
   -o-transform: translate(0, 10px);  /* Opera 10.5 */
   -webkit-transform: translate(0, 10px);  /* Saf3.1+, Chrome */
 }
</pre>

===5.4. Video + canvas===

Canvas is yet another HTML5 element with many possibilities when used in conjunction with the video tag.

In the next example in [http://www.html5rocks.com/en/tutorials/video/basics/ the same HTML5Rocks! article] we are taking advantage of two features of the &lt;canvas&gt; element to import and export images. The first one is the <code>drawImage<code> method which lets you import images from three different sources: an image element, another canvas element, and a <code>&lt;video&gt;</code> element! This means that every time we run this method, the current frame in the video will be imported and rendered onto the canvas.

The second feature of the <code>&lt;canvas&gt;</code> tag we are using is the <code>toDataURL</code> method which lets you export the content of the canvas to an image. Click play in the video to see how an image is created from the video every 1.5 seconds. The canvas we use to import/export is actually <code>hidden</code>.

You can see in the following code how we are simply creating an interval that runs every 1.5 seconds with the drawImage method which takes the video element as the source.

<pre>
 video_dom.addEventListener('play', function() {
   video_dom.width = canvas_draw.width = video_dom.offsetWidth;
   video_dom.height = canvas_draw.height = video_dom.offsetHeight;
   var ctx_draw = canvas_draw.getContext('2d');
   draw_interval = setInterval(function() {
     // import the image from the video
     ctx_draw.drawImage(video_dom, 0, 0, video_dom.width, video_dom.height);
     // export the image from the canvas
     var img = new Image();
     img.src = canvas_draw.toDataURL('image/png');
     img.width = 40;
     frames.appendChild(img);
   }, 1500)
 }, false);
</pre>

In the next example, available in [http://www.html5rocks.com/en/tutorials/video/basics/ the same article] we are going another step further. If you increase the frequency at which you import and render the image from the video you can really emulate the same video frame rate in the canvas. This lets you do all sorts of fancy transforms in the canvas as if you were doing it in the video.

On the left side you can see the original video playing. In the middle there's a canvas we are using to import the images every 33 milliseconds. On the right side there's a second canvas which will "suffer" all the transforms at the same time as it imports the images from the first canvas. The only reason we are using two canvases is because the performance is much better than using a single one which imports the images and transforms at the same time.

The same technique of importing images can be also applied to [https://cvs.khronos.org/svn/repos/registry/trunk/public/webgl/doc/spec/WebGL-spec.html WebGL]. With WebGL you would be able, for instance, to import the frames of a video and render them on a spinning 3D cube. There are more details about such implementation on the [https://developer.mozilla.org/en/WebGL/Animating_textures_in_WebGL MDC website].

===5.5. Video + SVG===

SVG provides a programmatic way to render and manipulate vector graphics, but it also comes with more features such as [http://en.wikipedia.org/wiki/SVG_filter_effects SVG filter effects]. With these filters you can target a specific DOM element and apply some out-of-the-box effects such as blur, composite, tiles, etc. In the following sample we are using JavaScript and canvas to make it also work for browsers which don't support inline SVG yet:

<pre>
 &lt;svg id='image' version="1.1" xmlns="http://www.w3.org/2000/svg"&gt;
   &lt;defs&gt;
     &lt;filter id="myblur"&gt;
       &lt;feGaussianBlur stdDeviation="1" /&gt;
     &lt;/filter&gt;
   &lt;/defs&gt;
 &lt;/svg&gt;
 &lt;style&gt;
   video { filter:url(#myblur); border: 2px solid red; }
 &lt;/style&gt;
</pre>

One more example can be found in [http://www.html5rocks.com/en/tutorials/video/basics/ the HTML5Rocks! article]. Click the video to toggle the blur filter.

==Missing Features and Differences with Flash==

There's no doubt that having the video tag as a native element gives the best environment to integrate video with the rest of your web application. [http://www.craftymind.com/2010/04/20/blowing-up-html5-video-and-mapping-it-into-3d-space/ More] and [http://demos.hacks.mozilla.org/openweb/WARMCSS/ more samples], [http://dev.opera.com/articles/view/custom-html5-video-player-with-css3-and-jquery/ video controls], and [http://yayquery.github.com/jquery-singalong/ related UI components] are being created every day.

It's almost inevitable that comparisons arise between the video element and other technologies which have been around much longer and provide capabilities like fullscreen view, access to [http://dev.w3.org/html5/html-device/ microphones and cameras], or support for [http://www.whatwg.org/specs/web-apps/current-work/#stream-api streaming video]. All these capabilities are currently being addressed both in the specification and browser support. If the video capabilities continue to evolve as fast as they have so far, it won't be long before we have all these features supported and ready for production across the modern browser market.

}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Video element
|Chrome_supported=Yes
|Chrome_version=20.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=12.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=Video element
|Android_supported=Yes
|Android_version=2.3
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_phone_supported=Unknown
|IE_phone_version=
|IE_phone_prefixed_supported=Unknown
|IE_phone_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Video}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/en/tutorials/video/basics/
}}