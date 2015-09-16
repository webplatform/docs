---
title: border-corner-shape
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`curve`'
  'Applies to': 'all elements, except table element when ‘border-collapse’ is ‘collapse’'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`borderCornerShape`'
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Specifies different corner clipping effects, such as scoop (inner curves), bevel (straight cuts) or notch (cut-off rectangles). Works along with border-radius to specify the size of each corner effect.'
tags:
  - CSS
  - Properties
uri: css/properties/border-corner-shape

---
## Summary

Specifies different corner clipping effects, such as scoop (inner curves), bevel (straight cuts) or notch (cut-off rectangles). Works along with border-radius to specify the size of each corner effect.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `curve`

Applies to
:   all elements, except table element when ‘border-collapse’ is ‘collapse’

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `borderCornerShape`

Percentages
:   N/A

## Syntax

-   `border-corner-shape: bevel`
-   `border-corner-shape: curve`
-   `border-corner-shape: notch`
-   `border-corner-shape: scoop`

## Values

curve
:   Border radii define a convex curve at the corner (default behavior of border-radius).

bevel
:   Border radii define a diagonal slice at the corner.

scoop
:   Border radii define a concave curve at the corner (informally called "negative border-radius")

notch
:   Border radii define a concave rectangular notch at the corner.

## Examples

Create a diamond (rhombus) shape

``` css
border-corner-shape: bevel;
border-radius: 50%;
```

Create a trapezoid

``` css
border-corner-shape: bevel;
border-radius: 25% / 100% 100% 0 0;
```

## Related specifications

[CSS Level 4 - Backgrounds and Borders Module](http://dev.w3.org/csswg/css-backgrounds-4/#border-corner-shape)
:   W3C Editor’s Draft

## See also

### Related articles

#### Box Model

-   [border](/css/properties/border)

-   **border-corner-shape**

-   [bottom](/css/properties/bottom)

-   [box-shadow](/css/properties/box-shadow)

-   [box-sizing](/css/properties/box-sizing)

-   [break-before](/css/properties/break-before)

-   [clear](/css/properties/clear)

-   [float](/css/properties/float)

-   [height](/css/properties/height)

-   [left](/css/properties/left)

-   [line-height](/css/properties/line-height)

-   [margin](/css/properties/margin)

-   [margin-bottom](/css/properties/margin-bottom)

-   [margin-left](/css/properties/margin-left)

-   [margin-right](/css/properties/margin-right)

-   [margin-top](/css/properties/margin-top)

-   [max-height](/css/properties/max-height)

-   [max-width](/css/properties/max-width)

-   [min-height](/css/properties/min-height)

-   [min-width](/css/properties/min-width)

### External resources

-   [Preview of border-corner-shape with SVG](http://leaverou.github.com/border-corner-shape)
