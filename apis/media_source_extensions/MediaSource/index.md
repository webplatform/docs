---
title: 'MediaSource'
attributions:
  - 'Microsoft Developer Network.'
code_samples:
  - 'http://gist.github.com/9144919/'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Represents a source of media data (audio or video) for a media element.'
tags:
  - API_Objects
uri: 'apis/media source extensions/MediaSource'

---
## Summary

Represents a source of media data (audio or video) for a media element.

## Overview

Provides a buffer based source for a media object. The app creates a MediaSource object and adds it to the media (audio or video) object as a source for the src object. SourceBuffers are then added to the MediaSource object and media content is then appended to the buffers to provide streaming or multi-source playback.

`var mediaSource = new MediaSource();`

## Properties

*No properties.*

## Methods

[addSourceBuffer](/apis/media_source_extensions/MediaSource/addSourceBuffer)
:   Creates a new SourceBuffer and adds it to the SourceBuffers property of the MediaSource.

[appendBuffer](/apis/media_source_extensions/MediaSource/appendBuffer)
:   Appends the specified media segment to the SourceBuffer.

[endOfStream](/apis/media_source_extensions/MediaSource/endOfStream)
:   Used to indicate that the end of the stream has been reached.

## Events

*No events.*

## Examples

This example creates a new MediaSource object and adds it to a video object. It then adds a sourceBuffer and calls to start loading content.

The live sample only runs on a browser that support the W3C syntax and MP4 files.

``` js
// Create mediaSource and initialize video
function setupVideo() {
  //  Create the media source
  if (window.MediaSource) {
    mediaSource = new window.MediaSource();
  } else {
    log("mediasource or syntax not supported");
    return;
  }
  var url = URL.createObjectURL(mediaSource);
  videoElement.src = url;

  // Wait for event that tells us that our media source object is
  //   ready for a buffer to be added.
  mediaSource.addEventListener('sourceopen', function (e) {
    try {
      videoSource = mediaSource.addSourceBuffer('video/mp4');
      //  initialize and start loading segments of video
    } catch (e) {
      //  error reporting here
      return;
    }
  });
}
```

[View live example](http://gist.github.com/9144919/)

## Related specifications

[Media Source Extensions](http://www.w3.org/TR/media-source/)
:   W3C Candidate Recommendation

## See also

### Related articles

#### Multimedia

-   [Track ended](/apis/MediaStream/ended)

-   **MediaSource**

-   [appendBuffer](/apis/media_source_extensions/MediaSource/appendBuffer)

-   [WebRTC](/concepts/Internet_and_Web/webrtc)

-   [object-fit](/css/properties/object-fit)

-   [height](/html/attributes/height)

-   [standby](/html/attributes/standby)

-   [EMBED](/html/elements/embed)

-   [img](/html/elements/img)

-   [WebRTC Resources](/tutorials/webrtc_resources)

 }

}
