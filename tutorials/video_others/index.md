---
title: HTML5 Video and Other Recommendations
readiness: 'Ready to Use'
summary: 'Overview about HTML5 Video interaction with other web standards and technologies'
tags:
  - Tutorials
uri: 'tutorials/video others'

---
**By [Carlos Araya](http://carlos.rivendellweb.net/)**
Originally published April 4, 2013

## <span>Summary</span>

Overview about HTML5 Video interaction with other web standards and technologies

## <span>The Fun Part</span>

The main advantage of the video tag being a member of the HTML5 family is its integration with the other layers of web development stack. In the following examples we'll give you an overview of what's possible to do with it.

### <span>Video + other HTML</span>

All the common HTML attributes can now be used in the video player. For instance, in the following snippet we are using `tabindex` to make the player keyboard accessible. There are new attributes that can be used in the video tag that are also common to the audio tag such as `loop` and `autoplay`, both self-explanatory. The attribute `poster` indicates what image will be shown while the video is initially loading and, finally, `controls` is used to indicate that instead of building our custom controls we want the browser to render ones automatically for us. There's also a `preload` attribute we can use to download the video in the background as soon as the page loads, even if it hasn't started playing.

     <video poster="star.png" autoplay loop controls tabindex="0">
       <source src="movie.webm" type="video/webm"; codecs="vp8, vorbis" />
       <source src="movie.ogv" type="video/ogg"; codecs="theora, vorbis" />
     </video>

The full level of integration of the video tag as a native browser element avoids some issues you might have had in the past with third-party embedded players such as dropdown menus and iframes overlaying on the player or weird layout behavior when the other HTML elements surrounding the video were dynamically resized.

Because the video is not treated as an embedded foreign object, there are some other benefits that affect the user experience. For instance, even if the focus is on the player itself, actions like page scrolling or keystrokes will be completely functional.

*Note:* If you are trying to write [polyglot documents](http://dev.w3.org/html5/html-author/#polyglot-documents) to keep the XHTML syntax in the context of HTML5, then the attributes in your code should look like this:

     <video poster="star.png" autoplay="autoplay" loop="loop" controls="controls" tabindex="0"'>
       <source src="movie.webm" type="video/webm"; codecs="vp8, vorbis" />
       <source src="movie.ogv" type="video/ogg"; codecs="theora, vorbis" />
     </video>

### <span>Video + JS</span>

The video tag comes with a set of attributes and methods that give you fine control of your video from your JS code. You can see them in real time in [this example](http://www.w3.org/2010/05/video/mediaevents.html).

As with any other HTML element, you can attach common events to the video tag such as drag events, mouse events, focus events, etc. But the video element comes with a bunch of new events to detect (and control) when the video is playing, paused, or finished. Because loading a video resource can have many caveats, there are equally as many events to allow control of the loading process, both at network level (`loadstart, progress, suspend, abort, error, emptied, stalled`) and at buffering level (`loadedmetadata, loadeddata, waiting, playing, canplay, canplaythrough`).

At its simplest level, you can attach the `canplay` event to start doing stuff with the video.

     video.addEventListener('canplay', function(e) {
       this.volume = 0.4;
       this.currentTime = 10;
       this.play();
     }, false);

There are several custom player controls available on the internet right now. In [this HTML5Rocks! article](http://www.html5rocks.com/en/tutorials/video/basics/) you can see an example that uses some elements to control two videos simultaneously and also to emulate the fast forward effect with the `playbackRate` attribute. Use the slider to toggle the volume between the videos.

### <span>Video + CSS</span>

As you may have guessed, the video tag can be styled using traditional CSS properties (e.g., border, opacity, etc.) because it is a first-class citizen in the DOM. But the cool thing is that you can also style it with the latest CSS3 properties like reflections, masks, gradients, transforms, transitions, and animations.

In [this HTML5Rocks! article](http://www.html5rocks.com/en/tutorials/video/basics/) you can see an example. Hover over the video to see some of these properties in action. The CSS for this example is shown below.

     #video-css.enhanced {
       border: 1px solid white;
       -moz-box-shadow: 0px 0px 4px #ffffff; /* FF3.5+ */
       -webkit-box-shadow: 5px 44px 28px #333; /* Saf3.0+, Chrome */
       box-shadow: 0px 0px 4px #ffffff; /* Opera 10.5, IE 9.0 */

       -moz-transform: translate(0, 10px);  /* FF3.5+ */
       -o-transform: translate(0, 10px);  /* Opera 10.5 */
       -webkit-transform: translate(0, 10px);  /* Saf3.1+, Chrome */
     }

### <span>Video + canvas</span>

Canvas is yet another HTML5 element with many possibilities when used in conjunction with the video tag.

In the next example in [the same HTML5Rocks! article](http://www.html5rocks.com/en/tutorials/video/basics/) we are taking advantage of two features of the \<canvas\> element to import and export images. The first one is the `drawImage<code> method which lets you import images from three different sources: an image element, another canvas element, and a <code><video>` element! This means that every time we run this method, the current frame in the video will be imported and rendered onto the canvas.

The second feature of the `<canvas>` tag we are using is the `toDataURL` method which lets you export the content of the canvas to an image. Click play in the video to see how an image is created from the video every 1.5 seconds. The canvas we use to import/export is actually `hidden`.

You can see in the following code how we are simply creating an interval that runs every 1.5 seconds with the drawImage method which takes the video element as the source.

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

In the next example, available in [the same article](http://www.html5rocks.com/en/tutorials/video/basics/) we are going another step further. If you increase the frequency at which you import and render the image from the video you can really emulate the same video frame rate in the canvas. This lets you do all sorts of fancy transforms in the canvas as if you were doing it in the video.

On the left side you can see the original video playing. In the middle there's a canvas we are using to import the images every 33 milliseconds. On the right side there's a second canvas which will "suffer" all the transforms at the same time as it imports the images from the first canvas. The only reason we are using two canvases is because the performance is much better than using a single one which imports the images and transforms at the same time.

The same technique of importing images can be also applied to [WebGL](https://cvs.khronos.org/svn/repos/registry/trunk/public/webgl/doc/spec/WebGL-spec.html). With WebGL you would be able, for instance, to import the frames of a video and render them on a spinning 3D cube. There are more details about such implementation on the [MDC website](https://developer.mozilla.org/en/WebGL/Animating_textures_in_WebGL).

### <span>Video + SVG</span>

SVG provides a programmatic way to render and manipulate vector graphics, but it also comes with more features such as [SVG filter effects](http://en.wikipedia.org/wiki/SVG_filter_effects). With these filters you can target a specific DOM element and apply some out-of-the-box effects such as blur, composite, tiles, etc. In the following sample we are using JavaScript and canvas to make it also work for browsers which don't support inline SVG yet:

     <svg id='image' version="1.1" xmlns="http://www.w3.org/2000/svg">
       <defs>
         <filter id="myblur">
           <feGaussianBlur stdDeviation="1" />
         </filter>
       </defs>
     </svg>
     <style>
       video { filter:url(#myblur); border: 2px solid red; }
     </style>

One more example can be found in [the HTML5Rocks! article](http://www.html5rocks.com/en/tutorials/video/basics/). Click the video to toggle the blur filter.

## <span>See also</span>

### <span>Related articles</span>

#### <span>Video</span>

-   [audio-video](/apis/audio-video)

-   [enabled](/apis/audio-video/AudioTrack/enabled)

-   [language](/apis/audio-video/AudioTrack/language)

-   [WebRTC](/concepts/Internet_and_Web/webrtc)

-   [object-fit](/css/properties/object-fit)

-   [EMBED](/html/elements/embed)

-   [video](/html/elements/video)

-   [MSEPrimer](/tutorials/MSEPrimer)

-   **HTML5 Video and Other Recommendations**

-   [WebRTC Resources](/tutorials/webrtc_resources)

