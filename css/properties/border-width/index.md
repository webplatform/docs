---
title: border-width
tags:
  - CSS
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Sets the width of an element''s four borders. This property can have from one to four values. This is a shorthand property for setting values simultaneously for border-top-width, border-right-width, border-bottom-width, and border-left-width.'
code_samples:
  - 'http://gist.github.com/733bf352438f33914fc0'
uri: css/properties/border-width

---
# border-width

## Summary

Sets the width of an element's four borders. This property can have from one to four values. This is a shorthand property for setting values simultaneously for border-top-width, border-right-width, border-bottom-width, and border-left-width.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `medium, for all 4 values`
Applies to
:   All elements
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   An absolute length, for all 4 values; 0 if the border style is 'none' or 'hidden'
Animatable
:   Yes
[CSS Object Model Property](/css/concepts/cssom)
:   `borderWidth`
Percentages
:   N/A

## Syntax

-   `border-width: <border-top-width> <border-right-width> <border-bottom-width> <border-left-width>`
-   `border-width: <width>`
-   `border-width: medium`
-   `border-width: thick`
-   `border-width: thin`

## Values

medium
:   Default. Â

thin
:   Less than the default width.

thick
:   Greater than the default width.

\<width\>
:   Floating-point number, followed by an absolute units designator (`cm`, `mm`, `in`, `pt`, or `pc`) or a relative units designator (`em`, `ex`, or `px`). For more information about the supported length units, see [[Values and Units Reference](http://www.w3.org/TR/css3-background/#the-border-width%7CCSS)].

\<border-top-width\> \<border-right-width\> \<border-bottom-width\> \<border-left-width\>
:   Shorthand syntax. See notes below.

## Examples

CSS border width values.

``` {.css}
.medium {
  border-width: medium;
}

.thin {
  border-width: thin;
}

.thick {
  border-width: thick;
}

.width {
  border-width: 10px;
}

.various {
  border-width: thick medium thin 10px;
}
```

[View live example](http://code.webplatform.org/gist/733bf352438f33914fc0)

## Usage

     * Up to four different widths can be specified, in the following order: top, right, bottom, left.

-   If one width is specified, it is used for all four sides. If two widths are specified, the first is used for the top and bottom borders, and the second is used for left and right borders. If three widths are specified, they are used for top, right/left, and bottom borders, respectively. If left is missing, it is the same as right; if bottom is missing, it is the same as top; if right is missing, it is the same as top.

## Related specifications

Specification
:   Status
[CSS Level 3 - Backgrounds and Borders Module](http://www.w3.org/TR/css3-background/#the-border-width)
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

-   [border-top-width](/css/properties/border-top-width)

-   **border-width**

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

