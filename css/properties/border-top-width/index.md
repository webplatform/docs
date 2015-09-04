---
title: border-top-width
tags:
  - CSS
  - Properties
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Add description, compatibility.'
summary: 'Sets the width of an element''s top border. To set all four borders, use the border-width shorthand property which sets the values simultaneously for border-top-width, border-right-width, border-bottom-width, and border-left-width.'
code_samples:
  - 'http://gist.github.com/5550302'
uri: css/properties/border-top-width

---
# border-top-width

## Summary

Sets the width of an element's top border. To set all four borders, use the border-width shorthand property which sets the values simultaneously for border-top-width, border-right-width, border-bottom-width, and border-left-width.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `medium`
Applies to
:   All elements
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   An absolute length; 0 if the border style is 'none' or 'hidden'
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   `borderTopWidth`
Percentages
:   N/A

## Syntax

-   `border-top-width: <width>`
-   `border-top-width: medium`
-   `border-top-width: thick`
-   `border-top-width: thin`

## Values

medium
:   Default. Â

thin
:   Less than the default width.

thick
:   Greater than the default width.

\<width\>
:   Floating-point number, followed by an absolute units designator (`cm`, `mm`, `in`, `pt`, or `pc`) or a relative units designator (`em`, `ex`, or `px`). For more information about the supported length units, see CSS Values and Units Reference.

## Examples

CSS border width values.

``` {.css}
.medium {
  border-top-width: medium;
}

.thin {
  border-top-width: thin;
}

.thick {
  border-top-width: thick;
}

.width {
  border-top-width: 10px;
}
```

[View live example](http://code.webplatform.org/gist/5550302)

## Related specifications

Specification
:   Status
[W3C CSS Backgrounds and Borders Module Level 3](http://www.w3.org/TR/css3-background/#border-width)
:   Candidate Recommendation

## See also

### Related articles

#### Border

-   [border](/css/properties/border)

-   [border-bottom](/css/properties/border-bottom)

-   [border-bottom-color](/css/properties/border-bottom-color)

-   [border-bottom-left-radius](/css/properties/border-bottom-left-radius)

-   [border-bottom-style](/css/properties/border-bottom-style)

-   [border-bottom-width](/css/properties/border-bottom-width)

-   [border-color](/css/properties/border-color)

-   [border-image](/css/properties/border-image)

-   [border-image-outset](/css/properties/border-image-outset)

-   [border-image-repeat](/css/properties/border-image-repeat)

-   [border-image-slice](/css/properties/border-image-slice)

-   [border-image-source](/css/properties/border-image-source)

-   [border-image-width](/css/properties/border-image-width)

-   [border-left](/css/properties/border-left)

-   [border-left-color](/css/properties/border-left-color)

-   [border-left-style](/css/properties/border-left-style)

-   [border-left-width](/css/properties/border-left-width)

-   [border-radius](/css/properties/border-radius)

-   [border-right](/css/properties/border-right)

-   [border-right-color](/css/properties/border-right-color)

-   [border-right-style](/css/properties/border-right-style)

-   [border-right-width](/css/properties/border-right-width)

-   [border-top](/css/properties/border-top)

-   [border-top-color](/css/properties/border-top-color)

-   [border-top-left-radius](/css/properties/border-top-left-radius)

-   [border-top-right-radius](/css/properties/border-top-right-radius)

-   [border-top-style](/css/properties/border-top-style)

-   **border-top-width**

-   [border-width](/css/properties/border-width)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

