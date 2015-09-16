---
title: 'filter'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/filter_8.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/filter_h.htm'
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/filter_s.htm'
notes:
  - 'Add summery, specifications, compatibility.'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: css/media_queries
    href: /css/media_queries
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /css/media_queries
tags:
  - API
  - Object
  - Methods
  - DOM
uri: 'css/media queries/filter'

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [css/media\_queries](/css/media_queries)[css/media\_queries](/css/media_queries)

## Syntax

``` js
var object = object.filter();
```

## Return Value

Returns an object of type DOM NodeDOM Node

## Examples

The following example shows how to use the **-ms-filter** attribute in Internet Explorer 8.

``` html
-ms-filter: 'progid:DXImageTransform.Microsoft.MotionBlur(strength=50), progid:DXImageTransform.Microsoft.BasicImage(mirror=1)';
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/filter_8.htm)

The following example shows how to use an inline style sheet to set the filter on an image.

``` html
<img style="filter:progid:DXImageTransform.Microsoft.MotionBlur(strength=50)
    progid:DXImageTransform.Microsoft.BasicImage(mirror=1)"
    src="/workshop/samples/author/dhtml/graphics/cone.jpg"
    height="80px" width="80px" alt="cone">
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/filter_h.htm)

The following example shows how to use inline scripting to set the filter on an image.

``` html
<script type="text/javascript">
function doFilter ()
{
    filterFrom.filters.item(0).Apply();
    // 12 is the dissolve filter.
    filterFrom.filters.item(0).Transition=12;
    imageFrom.style.visibility = "hidden";
    filterTo.style.visibility = "";
    filterFrom.filters.item(0).play(14);
}
</script>
</head>
<body>
<p>Click the image to start the filter.</p>
// Call the function.
<div id="filterFrom" onclick="doFilter()"
    style="position: absolute;
        width: 200px;
        height: 250px;
        background-color: white;
        filter: revealTrans()">
<img id="imageFrom"
    style="position: absolute;
        top: 20px;
        left: 20px;"
    src="sphere.jpg"
    alt="sphere">
<div id="filterTo"
    style="position: absolute;
        width: 200px;
        height: 250px;
        top: 20px;
        left: 20px;
        background: white;
        visibility: hidden;">
</div>
</div>
</body>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/filter_s.htm)

## Notes

### Remarks

Windows Internet Explorer 8. The **-ms-filter** attribute is an extension to CSS, and can be used as a synonym for **filter** in IE8 Standards mode. When you use **-ms-filter**, enclose the progid in single quotes (') or double quotes ("). Use commas (,) to separate multiple values, as shown in the Examples section. An object must have layout for the filter to render. A simple way to accomplish this is to give the element a specified [**height**](/css/properties/height) and [**hasLayout**](/css/cssom/properties/hasLayout) property. The shadow filter can be applied to the **img** object by setting the filter on the image's parent container. The filter mechanism is extensible and enables you to develop and add filters later. For more information about filters, see Introduction to Filters and Transitions. Not available on the Macintosh platform.

### Syntax

`-ms-filter: filtertype1 (parameter1, parameter2,...) | filtertype2 (parameter1, parameter2,...)`

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

-   **filter**

-   [ms-interpolation-mode](/css/media_queries/ms-interpolation-mode)

-   [behavior](/css/properties/behavior)

### Related pages

-   CSSStyleDeclaration[CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   currentStyle[currentStyle](/css/cssom/currentStyle)
-   style[style](/css/cssom/style)
