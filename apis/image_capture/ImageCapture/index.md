---
title: ImageCapture
tags:
  0: API
  1: Objects
  3: Image
  4: Capture
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Specifies the takePhoto() and getFrame() methods, and corresponding camera settings for use with MediaStreams.'
uri: 'apis/image capture/ImageCapture'

---
# ImageCapture

## Summary

Specifies the takePhoto() and getFrame() methods, and corresponding camera settings for use with MediaStreams.

## Properties

API Name
:   Summary
[onerror](/apis/image_capture/ImageCapture/onerror)
:   Register/unregister for Image Capture error events of type ImageCaptureErrorEvent.
[onframegrab](/apis/image_capture/ImageCapture/onframegrab)
:   Register/unregister for frame capture events of type FrameGrabEvent.
[onphoto](/apis/image_capture/ImageCapture/onphoto)
:   Register/unregister for photo events of type BlobEvent.
[onphotosettingschange](/apis/image_capture/ImageCapture/onphotosettingschange)
:   Register/unregister for photo settings change events of type SettingsChangeEvent.
[photoSettingsOptions](/apis/image_capture/ImageCapture/photoSettingsOptions)
:   Describes current photo settings.
[videoStreamTrack](/apis/image_capture/ImageCapture/videoStreamTrack)
:   The MediaStream passed into the constructor.

## Methods

API Name
:   Summary
[getFrame](/apis/image_capture/ImageCapture/getFrame)
:   Gathers data from the VideoStreamTrack into a ImageData object.
[setOptions](/apis/image_capture/ImageCapture/setOptions)
:   Applies the settings specified by the PhotoSettings object passed by parameter.
[takePhoto](/apis/image_capture/ImageCapture/takePhoto)
:   Gathers data from the VideoStreamTrack into a Blob containing a single still image.

## Events

*No events.*

## Related specifications

Specification
:   Status
[Mediastream Image Capture](http://w3c.github.io/mediacapture-image/)
:   W3C Editor's draft

## See also

### Related articles

#### Mobile

-   [Battery Status API](/apis/battery_status)

-   [Mediastream Image Capture](/apis/image_capture)

-   **ImageCapture**

-   [PhotoSettings](/apis/image_capture/PhotoSettings)

-   [Media Capture and Streams](/apis/media_capture_and_streams)

-   [Network Information API](/apis/network_information)

-   [Vibration API](/apis/vibration)

-   [capture](/html/attributes/capture)

### External resources

-   [Mediastream Image Capture](http://www.w3.org/TR/image-capture/)
-   [Mediastream Image Capture - W3C First Public Working Draft 09 July 2013](http://www.w3.org/TR/2013/WD-image-capture-20130709/)
-   [Device APIs working group](http://www.w3.org/2009/dap/)
-   [Media Capture Wiki](http://www.w3.org/wiki/Media_Capture)

