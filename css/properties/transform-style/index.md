---
title: 'transform-style'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
code_samples:
  - 'http://gist.github.com/6995453'
compatibility:
  feature: transform-style
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`flat`'
  'Applies to': 'Transformable elements.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified.'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'This property specifies how nested elements are rendered in 3D space relative to their parent.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/transform-style

---
## Summary

This property specifies how nested elements are rendered in 3D space relative to their parent.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `flat`

Applies to
:   Transformable elements.

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified.

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   N/A

## Syntax

-   `transform-style: flat`
-   `transform-style: preserve-3d`

## Values

flat
:   Child elements will not preserve their 3D position before applying a transform.

preserve-3d
:   Child elements will preserve their 3D position before applying a transform.

## Examples

``` css
/* The transformed child div (green) will preserve
   the 3D position applied by the parent div (blue)
   before applying its own transform */
#blue {
width: 10em;
height: 10em;
background-color: blue;
transform: rotateY(60deg);
transform-style: preserve-3d;
}

#green {
margin-left: 30px;
width: 10em;
height: 10em;
background-color: green;
transform: rotateY(60deg);
}
```

[View live example](http://gist.github.com/6995453)

## Notes

This property is only applied to child elements that have a [transform](/css/transforms/transform) specified.

## Related specifications

[CSS Transforms](http://www.w3.org/TR/css3-transforms)
:   W3C Working Draft
