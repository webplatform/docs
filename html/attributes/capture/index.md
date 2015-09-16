---
title: capture
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The capture attribute facilitates user access to a device''s media capture mechanism, such as a camera, or microphone, from within a file upload control, for capturing media on the spot.'
tags:
  - Markup
  - Attributes
  - Mobile
uri: html/attributes/capture

---
## HTML Media Capture

For technical reasons, the title of this article is not the text used to call this API. Instead, use `HTML Media Capture`

## Summary

The capture attribute facilitates user access to a device's media capture mechanism, such as a camera, or microphone, from within a file upload control, for capturing media on the spot.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
[HTMLInputElement](/dom/HTMLInputElement)

</td>
</tr>
</table>
The capture attribute is a boolean attribute that, if specified, indicates that the capture of media directly from the device's environment using a media capture mechanism is preferred.

The capture attribute applies to input elements when the type attribute's value is file and its accept attribute is specified. If the accept attribute's value is set to a MIME type that has no associated capture control type, the user agent acts as if there was no capture attribute.

The media capture mechanism builds upon the security and privacy protections provided by the \<input type="file"\> and the File API specifications; in particular, any offer to start capturing content from the user’s device requires a specific user interaction on an HTML element that is entirely controlled by the user agent.

## Examples

Indicates that image files are accepted to be captured.

``` html
<input type="file" accept="image/*" capture>
```

Indicates that video files are accepted to be captured.

``` html
<input type="file" accept="video/*" capture>
```

Indicates that audio files are accepted to be captured.

``` html
<input type="file" accept="audio/*" capture>
```

To take a picture using the device's camera, and upload the picture taken using an HTML form.

``` html
<form action="upload.php" method="post" enctype="multipart/form-data">
  <input type="file" name="image" accept="image/*" capture>
  <input type="submit" value="Upload">
</form>
```

To capture a video using the device's local video camera, and upload the picture taken using an HTML form.

``` html
<form action="upload.php" method="post" enctype="multipart/form-data">
  <input type="file" name="video" accept="video/*" capture>
  <input type="submit" value="Upload">
</form>
```

To capture audio using the device's local microphone, and upload the picture taken using an HTML form.

``` html
<form action="upload.php" method="post" enctype="multipart/form-data">
  <input type="file" name="audio" accept="audio/*" capture>
  <input type="submit" value="Upload">
</form>
```

## Related specifications

[HTML Media Capture](http://www.w3.org/TR/html-media-capture/#the-capture-attribute)
:   W3C Candidate Recommendation

## See also

### Related articles

#### Mobile

-   [Battery Status API](/apis/battery_status)

-   [Mediastream Image Capture](/apis/image_capture)

-   [Media Capture and Streams](/apis/media_capture_and_streams)

-   [Network Information API](/apis/network_information)

-   [Vibration API](/apis/vibration)

-   **capture**

### External resources

-   [HTML Media Capture - W3C Page](http://www.w3.org/TR/html-media-capture/)
-   [Article on Dev.Opera - 26 September 2013](http://dev.opera.com/articles/view/media-capture-in-mobile-browsers/)
-   [HTML Media Capture - W3C Candidate Recommendation 09 May 2013](http://www.w3.org/TR/2013/CR-html-media-capture-20130509/)
-   [Device APIs working group](http://www.w3.org/2009/dap/)
-   [Media Capture Wiki](http://www.w3.org/wiki/Media_Capture)
