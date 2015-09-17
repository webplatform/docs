---
title: 'Using the full-screen API'
readiness: 'Ready to Use'
summary: 'An introduction to using the full-screen API.'
tags:
  - Tutorials
  - Control
  - Video
uri: 'tutorials/using the full-screen api'

---
**By [Dave Gash](/User:Dgash)**
Originally published October 12, 2012

## Summary

An introduction to using the full-screen API.

## Introduction

In some browser applications, such as games, and with some elements, such as videos, it is advantageous to present the content using not just the interior browser window space but the full available screen space, without borders or other chrome elements. This might be desired to increase clarity, reduce distraction, or improve comprehension of the content.

The full-screen API provides a programmatic method for presenting web content using the user's entire monitor and lets you direct the browser to make an element—and its children, if any—occupy all of the available space.

### Visual comparison

The screen captures below show a web page containing a video element in normal and full-screen modes.

*Web page (cropped) with video element in normal mode* ![fs01-normal.png](/assets/public/a/a4/fs01-normal.png)

*Web page (reduced) with video element in full-screen mode* ![fs02-full.png](/assets/public/6/6b/fs02-full.png)

## Use

Beginning with a web page rendered normally in a standard browser window, the developer can enable elements on the page to change the display to full-screen. Once in full-screen mode, the mode may be exited either programmatically or through user interaction.

Two methods control the entry to and exit from full-screen mode, `requestFullscreen()` and `exitFullscreen()`, respectively. The first method is applied to the element, the second to the document object as shown below.

### Entering full-screen mode

Consider a `<video>` element as illustrated above. The element we wish to control has an ID so that it can be addressed programmatically. Also, in this case, the element contains the `controls` attribute to allow user control of playback, volume, etc., and two different `<source>` child elements as a fallback against a given browser not recognizing one or the other.

``` html
<video controls id="myvid">
  <source src="myvideo.webm"></source>
  <source src="myvideo.mp4"></source>
</video>
```

 The following script might be used to put the video element into full-screen mode.

``` js
var elem = document.getElementById("myvid");
elem.requestFullscreen();
```

 The video element will now render in full-screen mode, waiting for either a programmatic or user action to manipulate it or to exit full-screen mode.

### Exiting full-screen mode

While full-screen mode can be exited via standard user actions such as pressing **Esc** or **F11**, you can also exit the mode programmatically. For example, the following code creates a button whose onclick event exits full-screen mode.

``` html
<input type="button" value="Exit full-screen mode"
  onclick="document.exitFullscreen()"/>
```

 In addition, certain other user actions such as navigating to another web page, changing tabs in a browser, or switching to another application (e.g., with **alt-Tab**) will also force an exit from full-screen mode.

### Notification events

When full-screen mode is successfully entered or exited, the document containing the element receives a `fullscreenchange` event. The event itself provides no information about the state of the mode (i.e., whether it is on or off), but the document's `fullscreenElement` property can be tested to determine the mode. A non-null value indicates that full-screen is on, as shown below.

``` js
if (document.fullscreenElement != null) {
  // full-screen is on
}
else {
  // full-screen is off
}
```

### Failures

Attempts to enter full-screen mode may not succeed for various reasons. For example, `<iframe>`s may have to explicity allow full-screen activity, or certain kinds of content such as windowed plug-ins may prevent full-screen activation. In addition, attempting to invoke full-screen mode on a parent or descendant element of an element that *does* allow full-screen mode will fail.

In these cases, the element that requested the full-screen mode will recieve a `fullscreenerror` event, which can be trapped in script and handled appropriately.

## Live example

See a [live example of the full-screen API](https://developer.mozilla.org/samples/domref/fullscreen.html). Once on the page, play the video and then press **Enter** to toggle between full-screen and normal modes.

## Code sample

In this code sample, based on the live example, a video is presented in a web page. As above, the **Enter** key allows the user to toggle between full-screen and normal mode.

### Watching for the Enter key

When the page loads, an event listener is added to detect the **Enter** key.

``` js
document.addEventListener("keydown", function(e) {
  if (e.keyCode == 13) {
    toggleFullScreen();
  }
}, false);
```

 If an **Enter** keypress is detected, the listener calls a toggle function; if not, it returns `false` and does nothing.

### Toggling full-screen mode

When an **Enter** keypress is detected, the toggle function either enters full-screen mode if it is not active or exits full-screen mode if it is active. Prior to entry, a `videoElement` variable has been set containing the ID of the video element to be toggled.

``` js
function toggleFullScreen() {
  if (document.fullscreenElement == null &&) {
    if (videoElement.requestFullscreen) {
      videoElement.requestFullscreen();
    }
  } else {
    if (document.exitFullscreen) {
      document.exitFullscreen();
    }
  }
}
```

 This function begins by testing the document's `fullscreenElement` property.

If the `fullscreenElement` property is null, then the document *is not* in full screen mode. The nested `if` then determines whether the element supports the `requestFullscreen` method and, if so, invokes it on the element. If the element does not support the method, the script does nothing.

If the `fullscreenElement` property is not null, then the document *is* in full screen mode. The nested `if` then determines whether the document supports the `exitFullscreen` method and, if so, invokes it on the document. If the document does not support the method, the script does nothing.

## Support

This API currently has only partial support in modern browsers. See the compatibility tables in the relevant methods and properties below for the latest information.

## See also

-   [requestFullscreen](/dom/Element/requestFullscreen)
-   [exitFullscreen](/dom/Document/exitFullscreen)
-   [fullscreenElement](/dom/Document/fullscreenElement)
-   [fullscreenEnabled](/dom/Document/fullscreenEnabled)
