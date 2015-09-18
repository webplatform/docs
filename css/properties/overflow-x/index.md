---
title: 'overflow-x'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Web/CSS/overflow-y)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://code.webplatform.org/gist/6366308'
compatibility:
  feature: overflow-x
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`visible`'
  'Applies to': 'non-replaced block-level elements and non-replaced ‘inline-block’ elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified, except ‘visible’'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`overflowX`'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The overflow-x property is a specific case of the generic overflow property. It controls how extra content exceeding the x-axis of the bounding box of an element is rendered.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/overflow-x

---
## Summary

The overflow-x property is a specific case of the generic overflow property. It controls how extra content exceeding the x-axis of the bounding box of an element is rendered.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `visible`

Applies to
:   non-replaced block-level elements and non-replaced ‘inline-block’ elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified, except ‘visible’

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `overflowX`

## Syntax

-   `overflow-x: auto`
-   `overflow-x: hidden`
-   `overflow-x: no-content`
-   `overflow-x: no-display`
-   `overflow-x: scroll`
-   `overflow-x: visible`

## Values

visible
:   Default. Content is not clipped and scroll bars are not added. Elements are clipped to the size of the containing window or frame.

scroll
:   Content is clipped and scroll bars are added, even if the content does not exceed the dimensions of the object.

hidden
:   Content that exceeds the dimensions of the object is not shown.

auto
:   Content is clipped and scrolling is added only when necessary.

no-display
:   When the content doesn't fit in the content box, the whole box is removed, as if ‘display: none’ were specified.

no-content
:   When the content doesn't fit in the content box, the whole content is hidden, as if ‘visibility: hidden’ were specified.

## Examples

Using `overflow-x` width its values.

``` css
.hidden {
    overflow-x: hidden;
}
.scroll {
    overflow-x: scroll;
}
.auto {
    overflow-x: auto;
}
.visible {
    overflow-x: visible;
}

p {
    white-space: nowrap;
}

/* Set some default styles */
body {
    width: 20em;
    margin: 0 auto;
}
```

[View live example](http://code.webplatform.org/gist/6366308)

## Usage

     The overflow-x CSS property specifies whether to clip content, render a scroll mechanism, or display overflow content of a block-level element, when it overflows at the left and right edges.

## Notes

Setting the overflow-x property to visible causes the content to clip to the size of the window or frame that contains the object.

## Related specifications

[CSS basic box model](http://dev.w3.org/csswg/css-box/#overflow-x)
:   Editor's Draft

[CSS3 module: The box model](http://www.w3.org/TR/2002/WD-css3-box-20021024/)
:   Working Draft

[CSS basic box model](http://www.w3.org/TR/css3-box/#overflow1)
:   Working Draft

## See also

### Related Properties

-   [overflow](/css/properties/overflow)
-   [overflow-y](/css/properties/overflow-y)
