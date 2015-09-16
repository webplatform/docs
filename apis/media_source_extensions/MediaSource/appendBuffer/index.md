---
title: appendBuffer
attributions:
  - 'Microsoft Developer Network.'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/media_source_extensions/MediaSource
    href: /apis/media_source_extensions/MediaSource
standardization_status: 'W3C Candidate Recommendation'
summary: 'Appends the specified media segment to the SourceBuffer.'
tags:
  - API
  - Object
  - Methods
  - Media
uri: 'apis/media source extensions/MediaSource/appendBuffer'

---
## Summary

Appends the specified media segment to the SourceBuffer.

Method of [apis/media\_source\_extensions/MediaSource](/apis/media_source_extensions/MediaSource)[apis/media\_source\_extensions/MediaSource](/apis/media_source_extensions/MediaSource)

## Syntax

``` js
 SourceBuffer.appendBuffer(data);
```

## Parameters

### data

 Data-type
:   VARIANT

 Type: ArrayBuffer. The media segment to append

## Return Value

No return value

## Examples

This example uses XMLHttpRequest to get a segment of video (range) from a file (url) and appends it to the current sourceBuffer.

``` js


//  Load video's initialization segment
function initVideo(range, url) {
  var xhr = new XMLHttpRequest();
  if (range || url) { // make sure we've got incoming params
    // Set the desired range of bytes we want from the mp4 video file
    xhr.open('GET', url);
    xhr.setRequestHeader("Range", "bytes=" + range);
    segCheck = (timeToDownload(range) * .8).toFixed(3); // use .8 as fudge factor
    xhr.send();
    xhr.responseType = 'arraybuffer';
    try {   xhr.addEventListener("readystatechange", function () {
         if (xhr.readyState == xhr.DONE) { // wait for video to load
          // Add response to buffer
          try {            videoSource.appendBuffer(new Uint8Array(xhr.response));
            // Wait for the update complete event before continuing            videoSource.addEventListener("update",updateFunct, false);
          } catch (e) {
            log('Exception while appending initialization content', e);
          }
        }
      }, false);
    } catch (e) {
      log(e);
    }
  } else {
    return // No value for range or url
  }
}
function updateFunct() {
  //  This is a one shot function, when init segment finishes loading,
  //    update the buffer flag, call getStarted, and then remove this event.
  bufferUpdated = true;
  getStarted(file); // Get video playback started
  //  Now that video has started, remove the event listener
videoSource.removeEventListener("update", updateFunct);
}
```

</pre>

## Related specifications

[Media Source Extensions](http://www.w3.org/TR/media-source/)
:   W3C Candidate Recommendation

## See also

### Related articles

#### Multimedia

-   [Track ended](/apis/MediaStream/ended)

-   [MediaSource](/apis/media_source_extensions/MediaSource)

-   **appendBuffer**

-   [WebRTC](/concepts/Internet_and_Web/webrtc)

-   [object-fit](/css/properties/object-fit)

-   [height](/html/attributes/height)

-   [standby](/html/attributes/standby)

-   [EMBED](/html/elements/embed)

-   [img](/html/elements/img)

-   [WebRTC Resources](/tutorials/webrtc_resources)
