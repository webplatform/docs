---
title: wrap-margin
tags:
  0: CSS
  1: Properties
  3: CSS-Regions
readiness: 'Not Ready'
standardization_status: Non-Standard
notes:
  - 'This property was renamed to shape-margin. See css/properties/shape-margin for complete information.'
summary: 'Set the value that is used to offset the inner wrap shape from other shapes. Inline content that intersects a shape with this property will be pushed by this shape''s margin.'
uri: css/properties/wrap-margin

---
# wrap-margin

## Summary

Set the value that is used to offset the inner wrap shape from other shapes. Inline content that intersects a shape with this property will be pushed by this shape's margin.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `0`
Applies to
:   exclusion elements
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   ``

## Syntax

-   `wrap-margin: <length>`

## Values

\<length\>
:   The value that is used to offset the inner wrap shape from other shapes.

## Examples

In the following example, we have an image with a CSS class and a paragraph wrapped in a P tag.

``` {.html}
<p>
  <img class="logo" src="http://docs.webplatform.org/w/skins/webplatform/images/logo.png%22/>

  We are an open community of developers building resources for a better web, regardless of brand, browser or platform. Anyone can contribute and each person who does makes us stronger. Together we can continue to drive innovation on the Web to serve the greater good. It starts here, with you.
</p>
```

In the CSS class, we float the image left, set its shape to be the same image, and then we set a margin of 16px.

``` {.css}
.logo {
    float  : left;
    shape-outside : url("http://docs.webplatform.org/w/skins/webplatform/images/logo.png");
    shape-margin : 16px;
}
```

## See also

### Other articles

See also: [wrap-flow](/css/properties/wrap-flow) property

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/windows/apps/hh466103.aspx)

