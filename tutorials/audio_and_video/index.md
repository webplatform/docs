---
title: audio and video
tags:
  - Tutorials
  - Audio
  - JavaScript
  - Video
readiness: 'Ready to Use'
summary: 'HTML5 has improved embedding of audio and video by providing native support for many different file types. In this guide, we''ll cover the various ways to embed audio and video, including browser compatibility and frameworks to streamline cross-browser compatibility.'
uri: 'tutorials/audio and video'

---
# HTML5 \<audio\> and \<video\>

## Summary

HTML5 has improved embedding of audio and video by providing native support for many different file types. In this guide, we'll cover the various ways to embed audio and video, including browser compatibility and frameworks to streamline cross-browser compatibility.

## Playing Audio

HTML5 introduced `<audio>` tag, as well as the JavaScript APIs, which allow the browser to play audio without the need for an external plugin. The most supported codecs for playing audio in HTML5 are Ogg Vorbis, MP3, and Wav. There is currently no single codec that plays across all browsers. To get around the potential for codec incompatibility, HTML5 allows you to specify multiple source files. The browser looks for the first mime-type it knows it can support.

A simple implementation with only one source looks like this:

    <audio src="file.mp3"> </audio>

An implementation with multiple sources looks like this:

    <audio controls>
        <source src="song.ogg">
        <source src="song.mp3">
        Sorry, but your browser doesn't support audio.
    </audio>

If the browser doesn't support the audio element, then it will display the message, "Sorry, but your browser doesn't support audio."

### Helpful Libraries

Unfortunately, despite the inclusion of the HTML5 `<audio>` tag, there is still some friction in embedding audio and having that work seamlessly across all browsers and devices.

Handling multiple devices and browsers is made easier by using a library such as [Sound Manager 2](http://www.schillmania.com/projects/soundmanager2/) or [Buzz](http://buzz.jaysalvat.com/).

These libraries handle most of the inconsistencies around embedding audio, and let you focus on creating awesome web applications. Both of them provide graceful degradation to handle non-HTML5 browsers.

### Javascript API

The HTML5 Audio Javascript API allows for programmatic control of loading and playing audio files. The API is very straightforward, and provides a robust way to control embedded audio.

Here’s a simple example. In this example, we’ll add a song, jump to 30 seconds into the song, and play it.

    var audioElem = document.createElement('audio');
    audioElem.setAttribute('src', 'Crystal Castles - Untrust Us.ogg');
    audioElem.currentTime = 30;
    audioElem.play();

Retrieve the filename and duration:

    audioElement.src;
    audioElement.duration;

### Additional Reading

For a great tutorial with sample code that explains how to work with audio in the browser, see the [ThinkVitamin audio tutorial](http://thinkvitamin.com/code/html5-audio-unplugged/). Also, HTML5Rocks' Playground has [sample code](http://playground.html5rocks.com/#audio_tag) to help you get started.

## Playing Video

Similar to audio, the `<video>` tag has been introduced in the HTML5 spec, allowing web developers to harness the ability to play video without relying on third-party plugins. Support for various video/audio codecs varies from browser to browser, so it is imperative that you plan for all potential browsers and devices when creating your web application.

Browser compatibility information for [Ogg/Theora](http://caniuse.com/#search=ogg), [WebM/VP8](http://caniuse.com/#search=webm), and [H.264](http://caniuse.com/#search=mpeg) can be found at [CanIUse.com](http://caniuse.com/#search=video).

Apple has [launched a site](http://www.apple.com/html5/showcase/video/) that showcases the possibilities of HTML5 Video. More demos are available at [html5video.org](http://html5video.org/blog/demos/).

At its simplest form, an HTML5 video embed looks much like the audio example from above. Here’s how to add a video to your web app.

    <video src="fb.ogv"><video>

Since there is no single codec and container combination that is supported across all browsers, you will need to specify multiple sources. The browser will start at the first stream listed and go through all of them until it can successfully play one. It is important to specify the `type` field when embedding video. This tells the browser what the container type is, along with information about the video and audio codecs. If you do not specify the type field, the browser has to download a portion of each video until it can find one that it can successfully play.

    <video controls>
      <source src="fb.ogv" type='video/ogg; codecs="theora, vorbis"'>
      <source src="fb.mp4" type='video/mp4; codecs="avc1.42E01E, mp4a.40.2"'>
      <source src="fb.webm" type='video/webm; codecs="vp8, vorbis"'>
    </video>

A more in-depth discussion of types and syntax is available at [Dive Into HTML5](http://diveintohtml5.org/video.html#markup).

### Flash Fallback

A fallback to Flash should be included, as it allows you to embed video on browsers that may not support your video source types. Adding in support to fallback to Flash is straightforward. Using the example above, we can add in support for Flash by adding it as a last option:

    <video controls width="640" height="480">
      <source src="fb.ogv" type='video/ogg; codecs="theora, vorbis"'>
      <source src="fb.mp4" type='video/mp4; codecs="avc1.42E01E, mp4a.40.2"'>
      <source src="fb.webm" type='video/webm; codecs="vp8, vorbis"'>
      <object type="application/x-shockwave-flash" data="player.swf" width="640" height="480">
        <param name="allowfullscreen" value="true">
        <param name="allowscriptaccess" value="always">
        <param name="flashvars" value="file=fb.mp4">
        <!--[if IE]><param name="movie" value="player.swf"><![endif]-->
      </object>
    </video>

### Browser Compatibility

For maximum compatibility it is advisable to include:

-   A video source that uses H.264 baseline video and AAC "low complexity" audio in an MP4 container.
-   A video source that uses WebM (VP8 + Vorbis)
-   A video source that uses Theora video and Vorbis audio in an Ogg container.
-   Fallback to Flash-based video player.

Most developers wanting to leverage the power of HTML5 video will need to consider not only the browser differences, but also backwards compatibility for browsers that do not support HTML5 specs.

Fortunately, libraries such as [VideoJS](http://www.videojs.com) and [MediaElement.js](http://www.mediaelementjs.com/) simplify and streamline the process of embedding video on the web.

### Additional Reading

For tutorials on how the `<video>` tag works and how you can get started, check out [diveintohtml5](http://diveintohtml5.info/video.html). If you'd like to jump right in, HTML5Rocks' Playground has great [sample code](http://playground.html5rocks.com/#video_tag).

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Facebook HTML5 Resource Center.

