---
title: 'wrap-flow'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hh772045(v=vs.85).aspx)'
code_samples:
  - 'http://gist.github.com/5867597'
compatibility:
  feature: wrap-flow
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`auto`'
  'Applies to': 'Block-level elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified except for elements whose float computed value is not "none", in which case the computed value is "auto".'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
  Percentages: N/A
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Specifies how exclusions affect inline content within block-level elements. Elements lay out their inline content in their content area but wrap around exclusion areas.'
tags:
  - CSS
  - Properties
uri: css/properties/wrap-flow

---
## Summary

Specifies how exclusions affect inline content within block-level elements. Elements lay out their inline content in their content area but wrap around exclusion areas.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `auto`

Applies to
:   Block-level elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified except for elements whose float computed value is not "none", in which case the computed value is "auto".

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

Percentages
:   N/A

## Syntax

-   `wrap-flow: auto`
-   `wrap-flow: both`
-   `wrap-flow: clear`
-   `wrap-flow: end`
-   `wrap-flow: maximum`
-   `wrap-flow: minimum`
-   `wrap-flow: start`

## Values

auto
:   No exclusion is created. Inline flow content interacts with the element as usual.

![wrap-flow:auto applied to grid positioned elements;](/assets/public/b/ba/exclusion_wrap_side_auto.png)

both
:   Inline flow content can flow on all sides of the exclusion.

![wrap-flow:both applied to grid positioned elements;](/assets/public/5/53/exclusion_wrap_side_both.png)

start
:   Inline flow content can flow around the start edge of the exclusion area but must leave the area next to the end edge of the exclusion empty.

![wrap-flow:start applied to grid positioned elements;](/assets/public/b/b5/exclusion_wrap_side_left.png)

end
:   Inline flow content can flow around the end edge of the exclusion area but must leave the area next to the start edge of the exclusion empty.

![wrap-flow:end applied to grid positioned elements;](/assets/public/d/df/exclusion_wrap_side_right.png)

minimum
:   Inline flow content can flow around the edge of the exclusion with the smallest available space within the flow content's containing block, and must leave the other edge of the exclusion empty.

![wrap-flow:minimum applied to grid positioned elements;](/assets/public/d/d7/exclusion_wrap_side_minimum.png)

maximum
:   Inline flow content can flow around the edge of the exclusion with the largest available space within the flow content's containing block, and must leave the other edge of the exclusion empty.

![wrap-flow:maximum applied to grid positioned elements;](/assets/public/0/0b/exclusion_wrap_side_maximum.png)

clear
:   Inline flow content can only flow before and after the exclusion in the flow content's block direction, and must leave the areas next to the start and end edges of the exclusion empty.

![wrap-flow:clear applied to grid positioned elements;](/assets/public/4/41/exclusion_wrap_side_clear.png)

## Examples

``` css
/*
At the time of writing only available by default in IE10.
Can be enabled in Canary under "Enable experimental WebKit features".
*/

.flow-item {
  left: 5%;
  top: 5%;
  width: 200px;
  position: absolute;
}

.flow--maximum{
  wrap-flow: maximum;
}

.flow--clear{
  wrap-flow: clear;
}
```

[View live example](http://code.webplatform.org/gist/5867597)

## Usage

     If the property's computed value is "auto", the element does not become an exclusion.

An exclusion affects the inline flow content descended from the exclusion's containing block, and that of all descendant elements of the same containing block. All inline flow content inside the containing block of the exclusions is affected. To stop the effect of exclusions defined outside an element, the [wrap-through](/css/properties/wrap-through) property can be used.

## Related specifications

[CSS Exclusions Module Level 1](http://dev.w3.org/csswg/css-exclusions/)
:   Editor's Draft

## See also

### Other articles

[wrap-through](/css/properties/wrap-through)
