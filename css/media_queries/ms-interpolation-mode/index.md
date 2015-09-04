---
title: ms-interpolation-mode
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
notes:
  - 'Add summery, example, specifications, compatibility.'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/css/msInterpolation.htm'
uri: 'css/media queries/ms-interpolation-mode'

---
# ms-interpolation-mode

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [css/media\_queries](/css/media_queries)*

## Syntax

``` {.js}
var object = object.ms-interpolation-mode();
```

## Return Value

Returns an object of type DOM Node.

## Examples

The following example applies the **-ms-interpolation-mode** attribute to determine the resampling algorithm of stretched images. The sample requires Internet Explorer 7 or later to view.

    <html>
    <head>
    <style>
    img.highqual { -ms-interpolation-mode:bicubic }
    img.nearestn { -ms-interpolation-mode:nearest-neighbor }
    </style>
    </head>
    <body>
    <img src="sphere.jpg" width="175" height="350" class="nearestn">
    <img src="sphere.jpg" width="175" height="350">
    <img src="sphere.jpg" width="175" height="350" class="highqual">
    <p>Change the zoom level of the page to see the difference.</p>
    </body>
    </html>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/css/msInterpolation.htm)

## Notes

### Remarks

The **-ms-interpolation-mode** property is obsolete as of Windows Internet Explorer 9. Do not use. The **-ms-interpolation-mode** property was introduced in Windows Internet Explorer 7. The **-ms-interpolation-mode** property applies to stretched images only. For example, if the natural width of the image is 200x200 but the page designer specifies that the height and width should be 400x400, then the image will be stretched to the new dimensions using the nearest-neighbor algorithm, unless otherwise specified. If the zoom level of the page is 100%, the default interpolation is nearest-neighbor, otherwise bicubic mode is used.

### Syntax

`-ms-interpolation-mode: nearest-neighbor | bicubic`

## See also

### Related articles

#### Media Queries

-   [Responsive Web Design](/concepts/mobile_web/responsive_design)

-   [\<resolution\>](/css/data_types/resolution)

-   [accelerator](/css/media_queries/accelerator)

-   [MediaQueryList](/css/media_queries/apis/MediaQueryList)

-   [MediaQueryListListener](/css/media_queries/apis/MediaQueryListListener)

-   [StyleMedia](/css/media_queries/apis/StyleMedia)

-   [addListener](/css/media_queries/apis/addListener)

-   [handleChange](/css/media_queries/apis/handleChange)

-   [matchMedia](/css/media_queries/apis/matchMedia)

-   [matchMedium](/css/media_queries/apis/matchMedium)

-   [matches](/css/media_queries/apis/matches)

-   [media](/css/media_queries/apis/media)

-   [type](/css/media_queries/apis/properties/type)

-   [removeListener](/css/media_queries/apis/removeListener)

-   [Colors by](/css/media_queries/colors_by)

-   [device-height](/css/media_queries/device-height)

-   [filter](/css/media_queries/filter)

-   **ms-interpolation-mode**

-   [behavior](/css/properties/behavior)

-   [Targeting styles with media queries](/tutorials/media_queries)

### Related pages (MSDN)

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `runtimeStyle`
-   `style`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

