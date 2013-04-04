{{Page_Title|HTML5 Video and Other Recommendations}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Byline
|Name=Carlos Araya
|URL=http://carlos.rivendellweb.net/
|Published=April 4, 2013
}}
{{Summary_Section|Overview about HTML5 Video interaction with other web standards and technologies}}
{{Tutorial
|Content==Video and Other Standards

==The Fun Part==

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

===Video + JS===

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

===Video + CSS===

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

===Video + canvas===

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

===Video + SVG===

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
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Video
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}