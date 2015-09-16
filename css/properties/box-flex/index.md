---
title: box-flex
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Add example, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0.0`'
  'Applies to': 'in-flow children of box elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'In Progress'
standardization_status: Non-Standard
summary: 'Do not use. This property has been replaced by the flex property.'
tags:
  - CSS
  - Properties
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - flex
uri: css/properties/box-flex

---
## Summary

Do not use. This property has been replaced by the flex property.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `0.0`

Applies to
:   in-flow children of box elements

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

-   `box-flex: integer`

## Values

integer
:   A floating point value that indicates the relative flexibility of a child element.

A value of `0.0` indicates the element is not flexible. Any other value indicates the relative flexiblity of the child element compared to the flexibility of other child elements.

A negative value is not valid.

**Needs Examples**: This section should include examples.

## Usage

     Do not use. This property has been replaced by the flex property. To ensure compatibility in the future, applications using this property should be updated accordingly.

Gets or sets a value that specifies whether the width or height of a child element is flexible based on the space available in the object. This value also indicates the proportion of space available that is allocated to the child element.

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

-   **box-flex**

-   [box-lines](/css/properties/box-lines)

-   [box-orient](/css/properties/box-orient)

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

### Related pages (MSDN)

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `style`
