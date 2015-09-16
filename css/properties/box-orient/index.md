---
title: box-orient
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Add example, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`inline-axis`'
  'Applies to': 'box elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'In Progress'
standardization_status: Non-Standard
summary: Deprecated
tags:
  - CSS
  - Properties
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - '-ms-flex-direction'
uri: css/properties/box-orient

---
## Summary

Deprecated

## Overview table

[Initial value](/css/concepts/initial_value)
:   `inline-axis`

Applies to
:   box elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## Syntax

-   `box-orient: block-axis`
-   `box-orient: horizontal`
-   `box-orient: inherit`
-   `box-orient: inline-axis`
-   `box-orient: vertical`

## Values

horizontal
:   Child elements are displayed in a horizontal line from left to right.

vertical
:   Child elements are displayed in a vertical stack from top to bottom.

inline-axis
:   Default.

Child elements are displayed along the inline axis.

block-axis
:   Child elements are displayed along the block axis.

inherit
:   Child elements are displayed in the same orientation as the computed value of this property for the parent element.

**Needs Examples**: This section should include examples.

## Usage

     Do not use. This property has been replaced by -ms-flex-direction

Specifies the orientation in the layout of all child elements of the object.

## Related specifications

[Flexible Box Layout Module](http://www.w3.org/TR/2009/WD-css3-flexbox-20090723/)
:   W3C Working Draft (Obsolete)

## See also

### Related articles

#### CSS Layout

-   [Responsive Web Design](/concepts/mobile_web/responsive_design)

-   [@import](/css/atrules/@import)

-   [align-self](/css/properties/align-self)

-   [background](/css/properties/background)

-   [box-decoration-break](/css/properties/box-decoration-break)

-   [box-flex](/css/properties/box-flex)

-   [box-lines](/css/properties/box-lines)

-   **box-orient**

-   [box-pack](/css/properties/box-pack)

-   [box-shadow](/css/properties/box-shadow)

-   [break-before](/css/properties/break-before)

-   [flex-align](/css/properties/flex-align)

-   [flex-item-align](/css/properties/flex-item-align)

-   [flex-line-pack](/css/properties/flex-line-pack)

-   [grid-auto-rows](/css/properties/grid-auto-rows)

-   [grid-definition-columns](/css/properties/grid-definition-columns)

-   [grid-definition-rows](/css/properties/grid-definition-rows)

-   [height](/css/properties/height)

-   [max-width](/css/properties/max-width)

-   [user-modify](/css/properties/user-modify)

-   [baseline-shift](/svg/attributes/baseline-shift)

### Related pages

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `style`
