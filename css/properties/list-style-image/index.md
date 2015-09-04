---
title: list-style-image
tags:
  - CSS
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'This property sets the image that will be used as the list item marker. When the image is available, it will replace the marker set with the ''list-style-type'' marker. That also means that if the image is not available, it will show the style specified by list-style-property'
code_samples:
  - 'http://gist.github.com/6948599'
uri: css/properties/list-style-image

---
# list-style-image

## Summary

This property sets the image that will be used as the list item marker. When the image is available, it will replace the marker set with the 'list-style-type' marker. That also means that if the image is not available, it will show the style specified by list-style-property

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`
Applies to
:   elements with 'display: list-item'
[Inherited](/css/concepts/inherited)
:   Yes
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   absolute URI or 'none'
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   `listStyleImage`

## Syntax

-   `list-style-image: inherit`
-   `list-style-image: none`
-   `list-style-image: url(path/to/image.png)`

## Values

none
:   Default. No image is specified.

url(path/to/image.png)
:   Location of the image, where path/to/image.png is an absolute or relative URL. More details can be found at the [css/functions/url()](/css/functions/url()) section.

inherit
:   Takes the same specified value as the property for the element's parent. (Acts similarly to other uses of inherit in CSS.)

## Examples

The following examples shows the different possible values you can use for the list-style-image property. It also contains an example to show what happened when an unavailable image is not provided and how to use 'none' to break the inheritance.

``` {.css}
/* Using an absolute URI to specify an image */
.first-list {
    list-style-image: url(http://docs.webplatform.org/w/skins/webplatform/images/logo.svg);
}

/* Using a relative URI to specify an image */
.second-list {
    list-style-image: url(favicon.ico);
}

/* When providing an unavailable image, the marker used will be the one specified by the 'list-style-type' property */
.third-list {
    list-style-image: url(http://docs.webplatform.org/w/skins/webplatform/images/logo.svg);
}

/* Setting the value to none we are breaking the inheritance */
.third-list .third-list-inner-non-inherit {
    list-style-image: none;
}

/* When providing an unavailable image, the marker used will be the one specified by the 'list-style-type' property */
.fourth-list {
    list-style-image: url(http://wrong.url.used.com);
    list-style-type: disc;
}
```

[View live example](http://code.webplatform.org/gist/6948599)

## Usage

     The property has limited positioning options for the background image, and in some circumstances doesn’t work at all in IE.

So it has become a far more common practice to simply set a background image on the list items.

## Notes

### Remarks

When the image is available, it replaces the marker that is set with the [**list-style-type**](/css/properties/list-style-type) marker. If the left margin of the list item is set to 0 using one of the [**margin**](/css/properties/margin) properties, the list-item markers do not show.

## Related specifications

Specification
:   Status
[CSS Lists and Counters Module Level 3](http://dev.w3.org/csswg/css3-lists/#list-style-image)
:   Working Draft
[CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/generate.html#propdef-list-style-image)
:   Recommendation

## See also

### Related articles

#### Generated and Replaced Content

-   [Generated and Replaced Content](/css/generated_and_replaced_content)

-   [content](/css/properties/content)

-   [counter-increment](/css/properties/counter-increment)

-   [counter-reset](/css/properties/counter-reset)

-   **list-style-image**

-   [list-style-type](/css/properties/list-style-type)

-   [object-fit](/css/properties/object-fit)

### Related pages (MSDN)

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `runtimeStyle`
-   `style`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/list-style-image)

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

