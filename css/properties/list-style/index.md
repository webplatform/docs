---
title: list-style
tags:
  - CSS
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Shorthand property that sets the list-style-type, list-style-position and list-style-image properties in one declaration.'
code_samples:
  - 'http://gist.github.com/6950114'
  - 'http://gist.github.com/5598129'
uri: css/properties/list-style

---
# list-style

## Summary

Shorthand property that sets the list-style-type, list-style-position and list-style-image properties in one declaration.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `disc outside none`
Applies to
:   elements with display: list-item
[Inherited](/css/concepts/inherited)
:   Yes
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   see individual properties
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   `listStyle`

## Syntax

-   `list-style: inherit`
-   `list-style: list-style-type list-style-position list-style-image`

## Values

list-style-type list-style-position list-style-image
:   The `list-style` property can contain up to three components:

-   `list-style-type`: This takes any of the range of style values available to the [**list-style-type**](/css/properties/list-style-type), which includes `circle`, `disc`, `decimal`, `upper-roman`, etc. To see a the full list of possible values, see the [**list-style-type**](/css/properties/list-style-type).
-   `list-style-position`: Specifies if the list-item markers should appear inside or outside the content flow.
-   `list-style-image`: This property sets the image that will be used as the list item marker.

inherit
:   Takes the same specified value as the property for the element's parent. (Acts similarly to other uses of inherit in CSS.)

## Examples

The following example contains multiple examples of using this property, omitting some of the values.

``` {.css}
/* Specifying the list-style providing all the values */
.first-list {
    list-style: disc inside url(http://docs.webplatform.org/w/skins/webplatform/images/logo.svg);
}

 /* Omitting the position value it will use its default, 'outside' */
.second-list {
    list-style: disc url(http://docs.webplatform.org/w/skins/webplatform/images/logo.svg);
}

  /* When an available image is provided, it always takes precedence over type */
.third-list {
    list-style: circle url(http://docs.webplatform.org/w/skins/webplatform/images/logo.svg);
}

/* When omitting image and type, it will use their default values: 'disc' for type and and 'none' for image*/
.fourth-list {
    list-style: outside;
}
```

[View live example](http://code.webplatform.org/gist/6950114)

An example to show how setting padding-left to 0 when position is set to outside will produce the market not being shown at all. A ul contained in a div with overflow hidden might run into this issue.

``` {.css}
ul {
    padding-left: 0;
}

.list-position-outside {
    list-style-position: outside;
}

.list-position-inside {
    list-style-position: inside;
}
```

[View live example](http://code.webplatform.org/gist/5598129)

## Usage

     The list-style property is a composite property. You can omit one or more of the values. If both list-style-type and list-style-image are provided, and the value for this last one is different than none and links to an available image, the image takes precedence and it will be shown as the marker.

When the `list-style-position` value is set to **outside** and the [**padding**](/css/properties/padding) or [**padding-left**](/css/properties/padding-left) is set to 0, the list marker won't be displayed.

## Related specifications

Specification
:   Status
[CSS Lists and Counters Module Level 3](http://dev.w3.org/csswg/css3-lists/#list-style)
:   Working Draft
[CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS2/generate.html#propdef-list-style)
:   Recommendation

## See also

### Related articles

#### CSS Attributes

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [background-position](/css/properties/background-position)

-   [break-before](/css/properties/break-before)

-   [height](/css/properties/height)

-   **list-style**

-   [list-style-position](/css/properties/list-style-position)

-   [text-overflow-ellipsis](/css/properties/text-overflow-ellipsis)

-   [text-overflow-mode](/css/properties/text-overflow-mode)

-   [text-rendering](/css/properties/text-rendering)

-   [user-select](/css/properties/user-select)

-   [equality](/css/selectors/attributes/equality)

-   [Attribute selector](/css/selectors/attributes/existence)

-   [hyphen](/css/selectors/attributes/hyphen)

-   [prefix](/css/selectors/attributes/prefix)

-   [substring](/css/selectors/attributes/substring)

-   [suffix](/css/selectors/attributes/suffix)

-   [baseline-shift](/svg/attributes/baseline-shift)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### Related pages

-   `list-style-type`
-   `list-style-position`
-   `list-style-image`
-   `CSSStyleDeclaration`
-   `currentStyle`
-   `runtimeStyle`
-   `style`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

