---
title: getUserMedia
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[getUserMedia Method](https://developer.mozilla.org/en-US/docs/Web/API/Navigator.getUserMedia) Article]'
code_samples:
  - 'http://result.dabblet.com/gist/b0053b13f0dc7d3b8e0c/e7a999df33666b9d624c77ef0d824ad90023842a'
notes:
  - "In development channel for MSIE.\nsee status.modern.ie.\n\nms prefixed method only available on Win8."
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Navigator
    href: /dom/Navigator
  return_type:
    predicate: 'Returns an object of type  '
    value: LocalMediaStream
    href: /dom/Navigator
standardization_status: 'W3C Working Draft'
summary: 'Prompts the user for permission to use a media device such as a camera or microphone. If the user provides permission, the successCallback is invoked on the calling application with a LocalMediaStream object as its argument.'
tags:
  - API
  - Object
  - Methods
  - DOM
  - WebRTC
uri: dom/Navigator/getUserMedia

---
## <span>Summary</span>

Prompts the user for permission to use a media device such as a camera or microphone. If the user provides permission, the successCallback is invoked on the calling application with a LocalMediaStream object as its argument.

Method of [dom/Navigator](/dom/Navigator)[dom/Navigator](/dom/Navigator)

## <span>Syntax</span>

``` js
var stream = navigator.getUserMedia(constraints, successCallback, errorCallback);
```

## <span>Parameters</span>

### <span>constraints</span>

 Data-type
:   MediaStreamConstraints

 The constraints parameter is a MediaStreamConstraints object with two Boolean members: video and audio. These describe the media types supporting the [LocalMediaStream](/apis/webrtc/LocalMediaStream) object. Either or both must be specified to validate the constraint argument. If a specified constraint is not supported by the browser, getUserMedia invokes the errorCallback with the NOT\_SUPPORTED\_ERROR. If the browser cannot find any media track with the specified type, getUserMedia invokes the errorCallback with the MANDATORY\_UNSATISFIED\_ERR.

If the value or the member is not specified in the object, the value for the member defaults to false. The following demonstrates how to set the constraints for both audio and video:

    { video: true, audio: true }

There are additional constraints available. <http://simpl.info/getusermedia/constraints/> demonstrates the use of `maxWidth` and `maxHeight` constraints. There is a set of resolutions that is currently supported at the libjingle level. They are summarized [in this chromium ticket](https://code.google.com/p/chromium/issues/detail?id=143631#c9) and can be confirmed in the [libjingle source code](http://libjingle.googlecode.com/svn/trunk/talk/app/webrtc/localvideosource.cc)

### <span>successCallback</span>

 Data-type
:   function

 The getUserMedia function will call the function specified in the successCallback with the [LocalMediaStream](/apis/webrtc/LocalMediaStream) object that contains the media stream. You may assign that object to the appropriate element and work with it, as shown in the following example:

    function(localMediaStream) {
       var video = document.querySelector('video');
       video.srcObject = localMediaStream;
       video.onloadedmetadata = function(e) {
          // Do something with the video here.
       };
    },

### <span>errorCallback</span>

 Data-type
:   function

(Optional)

The getUserMedia function will call the function specified in the errorCallback with a code argument. The error codes are described as follows:

-   PERMISSION\_DENIED - The user denied permission to use a media device required for the operation.
-   NOT\_SUPPORTED\_ERROR - A constraint specified is not supported by the browser.
-   MANDATORY\_UNSATISFIED\_ERROR - No media tracks of the type specified in the constraints are found.

## <span>Return Value</span>

Returns an object of type LocalMediaStreamLocalMediaStream

## <span>Examples</span>

This live example uses feature detection to determine if the current web browser and operating system version supports the navigator.getUserMedia method.

``` html

```

[View live example](http://result.dabblet.com/gist/b0053b13f0dc7d3b8e0c/e7a999df33666b9d624c77ef0d824ad90023842a)

## <span>Notes</span>

The ms prefixed method is only available on windows 8 operating system. At the time of writing the standards getUserMedia method is 'in development'