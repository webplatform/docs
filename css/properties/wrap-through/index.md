---
title: 'wrap-through'
compatibility:
  feature: wrap-through
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`wrap`'
  'Applies to': 'Block-level elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'Specifies whether an element inherits its parent''s wrapping context as defined by the wrap-flow property.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/wrap-through

---
## Summary

Specifies whether an element inherits its parent's wrapping context as defined by the wrap-flow property.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `wrap`

Applies to
:   Block-level elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## Syntax

-   `wrap-through: none`
-   `wrap-through: wrap`

## Values

wrap
:   The element inherits its parent node's wrapping context. Its descendant inline content wraps around exclusions defined outside the element.

none
:   The element ignores its parent's wrapping context. Its descendent inline content only wraps around exclusions defined inside this element.

## Examples

``` css
/* wrap */
.exelem1 {
wrap-through: wrap;
}

/* none */
.exelem2 {
wrap-through: none;
}
```

## Usage

     Top half of image below illustrates "wrap-through:wrap"; bottom half illustrates "wrap-through:none".

![wrap-flow:start applied to grid positioned elements](//static.webplatform.org/2/27/exclusion_wrap_through.png)

## Related specifications

[CSS Exclusions Module Level 1](http://dev.w3.org/csswg/css-exclusions/)
:   Editor's Draft

## See also

### Other articles

[wrap-flow](/css/properties/wrap-flow)
