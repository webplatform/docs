---
title: 'HTML5 Video Basics'
attributions:
  - 'Portions of this content come from HTML5Rocks! [article](http://www.html5rocks.com/tutorials/video/basics/)'
notes:
  - 'I''m particularly interested in finding out if the type attribute of source must include the code, as this may be too hard for a beginner''s tutorial (assuming this is a beginner''s tutorial)'
readiness: 'Ready to Use'
summary: 'An introduction to the HTML5 video tag.'
tags:
  - Tutorials
  - Video
uri: 'tutorials/video basics'

---
**By [Ernest Delgado](http://www.html5rocks.com/profiles/#ernestd)**
Originally published Aug. 3, 2010

## Summary

An introduction to the HTML5 video tag.

## Introduction

The video tag is one of those HTML5 features that gets a lot of attention. Often presented in the media as an alternative to Flash, the video tag actually goes beyond that. Although it's recently joined the rest of the ubiquitous HTML tags, its capabilities and support across browsers have increased at an amazing speed. As you will see in this tutorial, its main advantage is the natural integration with the other layers of the web development stack such as CSS and JavaScript, as well as with the other HTML tags.

This tutorial will give you a basic understanding of the video tag and also show you various examples of different integrations with other HTML5 features, such as `<canvas>`.

## The Markup

To make HTML video work in your site, the following lines should be sufficient.

     <video>
       <source src="movie.mp4" type='video/mp4; codecs="avc1.42E01E, mp4a.40.2"' />
       <source src="movie.webm" type='video/webm; codecs="vp8, vorbis"' />
     </video>

This snippet uses the `<source>` tag which lets you include multiple formats as fallback types in case the user's browser doesn't support one of them. More about this in the next section.

You can also use a single video format which makes the syntax very similar to the image tag. This syntax will be the most used one in the near future when all browsers support one common video format.

     <video src="movie.webm" controls="controls"></video>

For now, we'll focus on the former case which is currently more common. *The most important thing to remember* is to make sure your server is serving video files with the correct MIME type, specified in the `Content-Type` header. If not, videos might not work properly, even if they are working on a local copy of your site. See [Configuring Mime Types on the server](/tutorials/configuring_mimetypes_on_the_server) for more information on configuring your server with new Mime Types

In order to improve the client side performance it's important to remember to specify the `type` attribute in the `source` tags when dealing with multiple formats. This way, the browser can decide which format it can download and play. In other words, it won't download the ones it can't play, in order to increase the performance of the site.

## Video Formats

Think of a <span style="color:green">video format</span> as a zip file that contains the encoded <span style="color:blue">video stream</span> and an <span style="color:red">audio stream</span>. The three formats you should care about for the web are mp4, ogv, and webm:

-   <span style="color:green">.mp4</span> = <span style="color:blue">H.264</span> + <span style="color:red">AAC</span>
-   <span style="color:green">.ogg/.ogv</span> = <span style="color:blue">Theora</span> + <span style="color:red">Vorbis</span>
-   <span style="color:green">.webm</span> = <span style="color:blue">VP8</span> + <span style="color:red">Vorbis</span>

The speed of evolution of the video tag is really encouraging. Today, most modern browsers support HTML5 video.

In [this HTML5Rocks! article](http://www.html5rocks.com/en/tutorials/video/basics/) you can see which of these formats your browser can render (you should feel lucky if you see all three of them!).

For now, here is the snippet that has the safest combination of formats so you can be sure your video is displayed in all browsers:

     <video>
       <source src="movie.webm" type='video/webm; codecs="vp8, vorbis"' />
       <source src="movie.mp4" type='video/mp4; codecs="avc1.42E01E, mp4a.40.2"' />
       <source src="movie.ogv" type='video/ogg; codecs="theora, vorbis"' />
       Video tag not supported. Download the video <a href="movie.webm">here</a>.
     <video>

*Note*: Because of a bug in the iPad you need to put .mp4 as the first option if you want the video to be loaded in that device, until the bug is fixed.

As mentioned before, most browser vendors have agreed to support a common video format. So, here is the code which will most likely be used across the web soon:

     <video>
       <source src="movie.webm" type='video/webm; codecs="vp8, vorbis"' />
       <source src="movie.mp4" type='video/mp4; codecs="avc1.42E01E, mp4a.40.2"' />
       Video tag not supported. Download the video <a href="movie.webm">here</a>.
     <video>

One of the main concerns about using the .mp4 format is that its video codec (h.264) is not an open codec and the licenses that a company would have to pay for using it are very complex. There's more information about this format in [this video chapter](http://diveintohtml5.info/video.html#licensing).

Another issue with the .mp4 format is that the `type` attribute needs to be more specific than other formats depending on the profile used to encode the video. Although the most common is "avc1.42E01E, mp4a.40.2", you should double check at this [profile list](http://wiki.whatwg.org/wiki/Video_type_parameters#MPEG-4) to be sure.

Even though Microsoft announced the support of the video tag, as well as other HTML5 elements, its user migration rate to newer versions is typically slower than the other major browsers. Hence the following section:

## What happens with IE versions that don't support the video tag?

There are two plugins that can be used as possible solutions:

### Chrome Frame

The advantage of using the [Chrome Frame plugin](http://code.google.com/chrome/chromeframe/) is that, once it's installed, Internet Explorer will have the support for the latest HTML, JavaScript and CSS standard features that older versions of IE don't support. This plugin has an added benefit for web developers, which is that it allows them to code applications with modern web features without leaving IE users behind. Just think the amount of time that a web developer saves without having to code hacks and workarounds for IE.

### Flash fallback

You can also use Flash as a fallback case. Depending on the format of your video you might need to encode it again to a compatible format for the Flash player. The good news is that Adobe has committed to support the *webm* format in their Flash player, although that timeline is still not clear. The biggest drawback of this solution compared to the Chrome Frame plugin is that you will get the Flash player as the degraded version of whatever custom UI or enhanced features you have built for your video tag. The details of this technique can be seen in the [Quick Guide to Implementing the HTML5 Audio](http://tutorials.html5rocks.com/tutorials/audio/quick/#toc-step3) tutorial.

## Encode Your Videos

If you need to encode your existing videos to the formats we mentioned in the previous section you can use [Miro Converter](http://www.mirovideoconverter.com/) for both Windows and Mac to easily get the format you need. The program doesn't allow you to tweak many settings but comes with the most common outputs for the web, including the three formats we use in this tutorial. Under the hood, this software is actually a wrapper for [ffmpeg](http://ffmpeg.org/) and [ffmpeg2theora](http://v2v.cc/~j/ffmpeg2theora/) which you can use in Windows, Mac, and Linux from the command line and specify more parameters. You can read more about this tool at [divintohtml5.org](http://diveintohtml5.info/video.html#webm-cli).

## Missing Features and Differences with Flash

There's no doubt that having the video tag as a native element gives the best environment to integrate video with the rest of your web application. [More](http://www.craftymind.com/2010/04/20/blowing-up-html5-video-and-mapping-it-into-3d-space/) and [more samples](http://demos.hacks.mozilla.org/openweb/WARMCSS/), [video controls](http://dev.opera.com/articles/view/custom-html5-video-player-with-css3-and-jquery/), and [related UI components](http://yayquery.github.com/jquery-singalong/) are being created every day.

It's almost inevitable that comparisons arise between the video element and other technologies which have been around much longer and provide capabilities like fullscreen view, access to [microphones and cameras](http://dev.w3.org/html5/html-device/), or support for [streaming video](http://www.whatwg.org/specs/web-apps/current-work/#stream-api). All these capabilities are currently being addressed both in the specification and browser support. If the video capabilities continue to evolve as fast as they have so far, it won't be long before we have all these features supported and ready for production across the modern browser market.
