---
title: 'overflow-y'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/6947763'
compatibility:
  feature: overflow-y
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`visible`'
  'Applies to': 'non-replaced block-level elements and non-replaced ‘inline-block’ elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified, except ‘visible’'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`overflowY`'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The overflow-y property is a specific case of the generic overflow property. It controls how extra content exceeding the y-axis of the bounding box of an element is rendered.'
tags:
  - CSS
  - Properties
uri: css/properties/overflow-y

---
## Summary

The overflow-y property is a specific case of the generic overflow property. It controls how extra content exceeding the y-axis of the bounding box of an element is rendered.

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
:   `overflowY`

## Syntax

-   `overflow-y: auto`
-   `overflow-y: hidden`
-   `overflow-y: no-content`
-   `overflow-y: no-display`
-   `overflow-y: scroll`
-   `overflow-y: visible`

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

Using `overflow-y` with its values.

``` css
.hidden {
    overflow-y: hidden;
}
.scroll {
    overflow-y: scroll;
}
.auto {
    overflow-y: auto;
}
.visible {
    overflow-y: visible;
}
```

[View live example](http://code.webplatform.org/gist/6947763)

## Usage

     The overflow-y CSS property specifies whether to clip content, render a scroll mechanism, or display overflow content of a block-level element, when it overflows at the top and bottom edges.

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
-   [overflow-x](/css/properties/overflow-x)
