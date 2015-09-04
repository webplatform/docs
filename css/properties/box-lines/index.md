---
title: box-lines
tags:
  - CSS
  - Properties
readiness: 'In Progress'
standardization_status: Non-Standard
notes:
  - 'Add example, compatibility.'
summary: "Do not use. This property has been replaced by the flex-wrap property.\n"
uri: css/properties/box-lines
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - flex-wrap

---
# box-lines

## Summary

Do not use. This property has been replaced by the flex-wrap property.

Gets or sets a value that specifies whether child elements wrap onto multiple lines or columns based on the space available in the object.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `single`
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
:   ``

## Syntax

-   `box-lines: multiple`
-   `box-lines: single`

## Values

single
:   Default.

All child elements are displayed in a single row or column. The [**overflow**](/css/properties/overflow) property of the object determines whether the child elements are hidden, clipped, or scrollable.

multiple
:   Child elements are wrapped and displayed in successive, parallel rows or columns. The object expands in height or width, perpendicular to the axis defined by the [**-ms-box-orient**](/css/properties/ms-box-orient) property, to accommodate the additional rows or columns.

**Needs Examples**: This section should include examples.

## Notes

### Remarks

Each child element is resized to its minimum width or height before the object is resized to accomodate additional rows or columns. Each successive rows is inserted below the previous row when [**-box-direction**](/css/properties/box-direction) is set to `normal` or above the previous row when **box-direction** is set to `reverse`. Each successive column is inserted to the right of the previous column when [**-box-direction**](/css/properties/box-direction) is set to `normal` or to the left of the previous column when **-ms-box-direction** is set to `reverse`.

## Related specifications

Specification
:   Status
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

-   **box-lines**

-   [box-ordinal-group](/css/properties/box-ordinal-group)

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

### Related pages

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `style`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

