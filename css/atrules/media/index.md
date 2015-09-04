---
title: @media
tags:
  - CSS
  - At
  - Rules
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Sets the media types for a set of rules in a styleSheet object.'
uri: css/atrules/@media

---
# @media

## Summary

Sets the media types for a set of rules in a styleSheet object.

## Examples

In the following example, the **@media** rule is used to specify the [**font-size**](/css/properties/font-size) attribute of the **body** element for two media types.

``` {.css}
// For computer screens, the font size is 12pt.
@media screen {
   BODY {font-size:12pt;}
}
// When printed, the font size is 8pt.
@media print {
   BODY {font-size:8pt;}
}
```

The following declaration is a typical media query. In this case, `screen` indicates the target media type, and `max-width` is the target media property. The declaration states that the specified rules (no border on **div** elements) are only to be applied when the page is displayed on a screen in a browser window with a width of at most 400 pixels.

``` {.css}
@media screen and (max-width:400px) {
   div {border:none;}
}
```

You can use media properties together to create even more specific queries, such as the following. This declaration applies the specified rules when the medium is a screen and the browser window has a width of no more than 400 pixels *and* a height of no more than 600 pixels.

``` {.css}
@media screen and (max-width:400px) and (max-height:600px) {
   ...
}
```

## Notes

### Remarks

The rule has no default value. Dynamic HTML (DHTML) expressions can be used in place of the preceding value(s). As of Windows Internet Explorer 8, expressions are not supported in IE8 Standards mode. For more information, see About Dynamic Properties. Windows Internet Explorer 9 introduces support for media queries. Media queries enable you to scope a style sheet to a set of precise device capabilities. For instance, you might want to design pages differently for users browsing on a mobile device (that has a very small screen, limited color palette, low resolution, and so on) versus a netbook (that has a small screen, full color palette, high resolution, and so on) versus a standard computer (that has a large screen, full color palette, high resolution, and so on). A media query consists of a media type (*sMediaType*) and zero or more expressions (*sMediaFeatures*) that check for the conditions of particular media features. A media query is a logical expression that is either true or false. A media query is true if the media type of the media query matches the media type of the computer on which Windows Internet Explorer is running, and all expressions in the media query are true. The following media features are supported:

-   [width](/css/media_queries/width)
-   [height](/css/media_queries/height)
-   [device-width](/css/media_queries/device-width)
-   [device-height](/css/media_queries/device-height)
-   [orientation](/css/media_queries/orientation)
-   [aspect-ratio](/css/media_queries/aspect-ratio)
-   [device-aspect-ratio](/css/media_queries/device-aspect-ratio)
-   [color](/css/media_queries/colors_by)
-   [color-index](/css/media_queries/color-index)
-   [monochrome](/css/media_queries/monochrome)
-   [resolution](/css/media_queries/resolution)

### Syntax

`@media sMediaType { Media-Rule+ }` **Media-Rule** `@media sRules`

### Parameters

<dl>
<dt>
*sMediaType*

</dt>
<dd>
**String** that specifies one of the following media types:

<dl>
<dt>
Value

</dt>
<dd>
Meaning

</dd>
<dt>
\<a id="screen"/\>\<a id="SCREEN"/\>

<dl>
<dt>
**screen**

</dt>
</dl>
</dt>
<dd>
Output is intended for computer screens.

</dd>
<dt>
\<a id="print"/\>\<a id="PRINT"/\>

<dl>
<dt>
**print**

</dt>
</dl>
</dt>
<dd>
Output is intended for printed material and for documents viewed in Print Preview mode.

</dd>
<dt>
\<a id="all"/\>\<a id="ALL"/\>

<dl>
<dt>
**all**

</dt>
</dl>
</dt>
<dd>
Output is intended for all devices.

</dd>
</dl>
�

</dd>
<dt>
*sRules*

</dt>
<dd>
**String** that specifies one or more rules in a [**styleSheet**](/css/cssom/styleSheet) object.

</dd>
</dl>
## Related specifications

Specification
:   Status
[Media Queries](http://www.w3.org/TR/css3-mediaqueries/)
:   Recommendation

## See also

### Related pages (MSDN)

-   `media`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

