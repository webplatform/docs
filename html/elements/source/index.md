---
title: source
tags:
  - Markup
  - Elements
  - HTML
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Allows developer to specify multiple alternative media resources for media elements, such as <video> and <audio>. It does not represent anything on its own, and is used with src attribute to specify the URL.'
code_samples:
  - 'http://test.w3.org/html/examples/elements/source/source01.html'
uri: html/elements/source
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/HTMLSourceElement
    - apis/audio-video/properties/src
    - apis/audio-video/methods/load
    - apis/audio-video/methods/play

---
# source

## Summary

Allows developer to specify multiple alternative media resources for media elements, such as \<video\> and \<audio\>. It does not represent anything on its own, and is used with src attribute to specify the URL.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLSourceElement](/w/index.php?title=dom/HTMLSourceElement&action=edit&redlink=1)

## Attributes

-   `src` = URL potentially surrounded by spaces
    The address of the media source.
-   `type` = MIME type
    The type of the media source (used for helping the UA determine, before fetching this media source, if it can play it).
    A string that identifies a valid MIME media type, as defined in [RFC2046].
-   `media` = media-query list
    The intended media type of the media source (used for helping the UA determine, before fetching this media source, if it is useful to the user).
    A valid media query list, as defined in [MediaQueries].

## Examples

``` {.html}
<video controls="controls">
 <source src="http://media.w3.org/2010/05/sintel/trailer.mp4"
         type='video/mp4; codecs="avc1, mp4a"/>
 <source src="http://media.w3.org/2010/05/sintel/trailer.ogv"
         type='video/ogg; codecs="theora, vorbis"/>
 <p>Your user agent does not support the HTML5 Video element.</p>
</video>
```

[View live example](http://test.w3.org/html/examples/elements/source/source01.html)

## Notes

### Remarks

**Note**  If you change the media file using the [**src**](/w/index.php?title=apis/audio-video/properties/src&action=edit&redlink=1) property on an **audio** or **video** object, you need to call the [**load**](/w/index.php?title=apis/audio-video/methods/load&action=edit&redlink=1) method before calling the [**play**](/w/index.php?title=apis/audio-video/methods/play&action=edit&redlink=1) method. If you change the **src** and call the play() method without loading first, it will continue to play the file specified by the **source** element.

## Related specifications

Specification
:   Status
[HTML 5.1](http://www.w3.org/TR/html51/embedded-content.html#the-source-element)
:   W3C Working Draft
[HTML 5](http://www.w3.org/TR/html5/embedded-content-0.html#the-source-element)
:   W3C Recommendation

## See also

### Related pages (MSDN)

-   `audio`
-   `video`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

