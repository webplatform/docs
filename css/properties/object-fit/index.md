---
title: 'object-fit'
code_samples:
  - 'http://gist.github.com/6badc0b20d67be7d939f'
compatibility:
  feature: object-fit
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`fill`'
  'Applies to': 'Replaced elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`objectFit`'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The object-fit property defines how content of a replaced element (e.g., a video or an image) is made to fit the dimensions of its containing box.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/object-fit

---
## Summary

The object-fit property defines how content of a replaced element (e.g., a video or an image) is made to fit the dimensions of its containing box.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `fill`

Applies to
:   Replaced elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `objectFit`

## Syntax

-   `object-fit: contain`
-   `object-fit: cover`
-   `object-fit: fill`
-   `object-fit: none`
-   `object-fit: scale-down`

## Values

fill
:   The replaced content is sized to fill the element's box

contain
:   The replaced content is sized to maintain its aspect ratio while fitting within the element's content box

cover
:   The replaced content is sized to maintain its aspect ratio while filling the element's entire content box

none
:   The replaced content is not resized to fit inside the element's content box

scale-down
:   Size the content as if ‘none’ or ‘contain’ were specified, whichever would result in a smaller concrete object size

## Examples

Five simple img elements.

``` html
<!DOCTYPE HTML>
<html lang="en-US">
<head>
  <meta charset="UTF-8">
  <title>Object-fit example</title>
  <link href="content-fit.css" type="text/css" rel="stylesheet">
</head>
<body>

  <img src="http://www.webplatform.org/logo/wplogo_pillow_wide_tan.png"
      alt="Webplatform Logo" class="fill"/>
  <img src="http://www.webplatform.org/logo/wplogo_pillow_wide_tan.png"
      alt="Webplatform Logo" class="contain"/>
  <img src="http://www.webplatform.org/logo/wplogo_pillow_wide_tan.png"
      alt="Webplatform Logo" class="cover"/>
  <img src="http://www.webplatform.org/logo/wplogo_pillow_wide_tan.png"
      alt="Webplatform Logo" class="none"/>
  <img src="http://www.webplatform.org/logo/wplogo_pillow_wide_tan.png"
      alt="Webplatform Logo" class="scale-down"/>

</body>
</html>
```

All five images are forced to 150x100 pixels, different from both the original size of the image (196x77 pixel) and its aspect ratio.

``` css
img {
  float: left;
  width: 150px;
  height: 100px;
  border: 1px solid #000;
  margin-right: 1em;
}
.fill {
  object-fit: fill;
  /**
    * This is the default behaviour.
    * The image is forced to fill the whole box,
    * the aspect ratio is ignored.
    **/
}
.contain {
  object-fit: contain;
  /**
    * The whole image will be displayed in the box
    * and scaled down or expanded if necessary.
    * The aspect ratio is maintained.
    **/
}
.cover {
  object-fit: cover;
  /**
    * The whole image is scaled down or expanded till
    * it fills the box completely, the aspect ratio is
    * maintained. This normally results in only part of
    * the image being visible.
    **/
}
.none {
  object-fit: none;
  /**
    * The image keeps it's original size.
    * This may result in not filling the box
    * completely or sticking out of it.
    **/
}
.scale-down {
  object-fit: scale-down;
  /**
    * The result of 'none' and 'contain' is compared
    * and the smaller concrete object is displayed.
   **/
}
```

[View live example](http://gist.github.com/6badc0b20d67be7d939f)

## Related specifications

[CSS Image Values and Replaced Content Module Level 3](http://www.w3.org/TR/css3-images/)
:   W3C Candidate Recommendation

## See also

### Related articles

#### Generated and Replaced Content

-   [Generated and Replaced Content](/css/generated_and_replaced_content)

-   [content](/css/properties/content)

-   [counter-increment](/css/properties/counter-increment)

-   [counter-reset](/css/properties/counter-reset)

-   [list-style-image](/css/properties/list-style-image)

-   [list-style-type](/css/properties/list-style-type)

-   **object-fit**

#### Multimedia

-   [Track ended](/apis/MediaStream/ended)

-   [MediaSource](/apis/media_source_extensions/MediaSource)

-   [appendBuffer](/apis/media_source_extensions/MediaSource/appendBuffer)

-   [WebRTC](/concepts/Internet_and_Web/webrtc)

-   **object-fit**

-   [height](/html/attributes/height)

-   [standby](/html/attributes/standby)

-   [EMBED](/html/elements/embed)

-   [img](/html/elements/img)

-   [WebRTC Resources](/tutorials/webrtc_resources)

#### Video

-   [audio-video](/apis/audio-video)

-   [enabled](/apis/audio-video/AudioTrack/enabled)

-   [language](/apis/audio-video/AudioTrack/language)

-   [WebRTC](/concepts/Internet_and_Web/webrtc)

-   **object-fit**

-   [EMBED](/html/elements/embed)

-   [video](/html/elements/video)

-   [MSEPrimer](/tutorials/MSEPrimer)

-   [HTML5 Video and Other Recommendations](/tutorials/video_others)

-   [WebRTC Resources](/tutorials/webrtc_resources)
