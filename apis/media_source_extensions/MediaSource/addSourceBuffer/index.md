---
title: 'addSourceBuffer'
attributions:
  - 'Microsoft Developer Network.'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/media_source_extensions/MediaSource
    href: /apis/media_source_extensions/MediaSource
  return_type:
    predicate: 'Returns an object of type  '
    value: Object
    href: /apis/media_source_extensions/MediaSource
standardization_status: 'W3C Candidate Recommendation'
summary: 'Creates a new SourceBuffer and adds it to the SourceBuffers property of the MediaSource.'
tags:
  - API
  - Object
  - Methods
uri: 'apis/media source extensions/MediaSource/addSourceBuffer'

---
## Summary

Creates a new SourceBuffer and adds it to the SourceBuffers property of the MediaSource.

Method of [apis/media\_source\_extensions/MediaSource](/apis/media_source_extensions/MediaSource)[apis/media\_source\_extensions/MediaSource](/apis/media_source_extensions/MediaSource)

## Syntax

``` js
var sourcebuffer = MediaSource.addSourceBuffer(MIME type);
```

## Parameters

### MIME type

 Data-type
:   String

 The MIME type. This is expressed typically as 'video/mp4' or optionally as a MIME type and a codec: 'video/mp4;codecs=avc1.4d0020,mp4a.40.2'. Internet Explorer accepts both formats, though other browsers may require the codec be included.

## Return Value

Returns an object of type ObjectObject

Type: SourceBuffer The media source buffer.

## Examples

This example gets a video object, creates a new MediaSource object, and assigns the MediaSource object to the src (source) of the video object. It then waits for the sourceopen event to fire, and then creates a video SourceBuffer using addSourceBuffer.

``` js


// Create mediaSource and initialize video
function setupVideo() {
  clearLog(); // Clear console log

  //  Create the media source
  if (window.MediaSource) {
    mediaSource = new window.MediaSource();
   } else {
    log("mediasource or syntax not supported");
    return;
  }
  var url = URL.createObjectURL(mediaSource);
  videoElement.pause();
  videoElement.src = url;
  videoElement.width = width;
  videoElement.height = height;

  // Wait for event that tells us that our media source object is
  //   ready for a buffer to be added.
  mediaSource.addEventListener('sourceopen', function (e) {
    try {
      videoSource = mediaSource.addSourceBuffer('video/mp4');
      initVideo(initialization, file);
    } catch (e) {
      log('Exception calling addSourceBuffer for video', e);
      return;
    }
  },false);
}
```

</pre>

## Usage

     Exceptions:

INVALID\_ACCESS\_ERR If type is null or an empty string.

NOT\_SUPPORTED\_ERR If type contains a MIME type that's not supported or a MIME type that's not supported by SourceBuffer.

QUOTA\_EXCEEDED\_ERR If the mediaSource can't handle any more SourceBuffer objects.

## Related specifications

[Media Source Extensions](http://www.w3.org/TR/media-source/)
:   W3C Candidate Recommendation

