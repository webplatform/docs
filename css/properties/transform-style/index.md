---
title: transform-style
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
code_samples:
  - 'http://gist.github.com/6995453'
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
  - CSS
  - Properties
uri: css/properties/transform-style

---
## <span>Summary</span>

This property specifies how nested elements are rendered in 3D space relative to their parent.

## <span>Overview table</span>

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

## <span>Syntax</span>

-   `transform-style: flat`
-   `transform-style: preserve-3d`

## <span>Values</span>

flat
:   Child elements will not preserve their 3D position before applying a transform.

preserve-3d
:   Child elements will preserve their 3D position before applying a transform.

## <span>Examples</span>

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

[View live example](http://code.webplatform.org/gist/6995453)

## <span>Notes</span>

This property is only applied to child elements that have a [transform](/css/transforms/transform) specified.

## <span>Related specifications</span>

[CSS Transforms](http://www.w3.org/TR/css3-transforms)
:   W3C Working Draft
