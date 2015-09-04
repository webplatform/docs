---
title: box-pack
tags:
  - CSS
  - Properties
readiness: 'In Progress'
standardization_status: Non-Standard
notes:
  - 'Add example, compatibility.'
summary: 'Do not use. This property has been replaced by flex-pack.'
uri: css/properties/box-pack
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - flex-pack

---
# box-pack

## Summary

Do not use. This property has been replaced by flex-pack.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `start`
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

-   `box-pack: center`
-   `box-pack: end`
-   `box-pack: justify`
-   `box-pack: start`

## Values

start
:   The starting edge of the first child element is placed at the start of the parent element; the starting edge of the next child element is placed edge to edge with the ending edge of the first child element; and so on along the layout axis direction. All space that remains along the layout axis is placed at the end of the layout axis.

end
:   The ending edge of the first child element is placed at the end of the parent element; the ending edge of the next child element is placed edge to edge with the starting edge of the first child element; and so on along the layout axis direction. All space remaining along the layout axis is placed at the start of the layout axis.

center
:   All child elements are placed edge to edge with each other, as described in the descriptions for the [\#start start] or [\#end end] keywords. However, the group of child elements is centered between the starting and ending edges of the parent element so that all remaining space is evenly distributed before the first child element and after the last child element.

justify
:   The starting edge of the first child element is placed at the start of the parent element; the ending edge of the last child element is placed edge to edge with the end of the parent box; and all remaining children are placed between the first and last child elements, so that any space that remains along the layout axis is equally distributed between child elements.

**Needs Examples**: This section should include examples.

## Notes

### Remarks

Be aware that these are [**writing-mode**](/css/properties/writing-mode) dependent keywords; the starting and ending edges of the parent element and child elements depend on the layout direction. For instance, for a left-to-right layout, the starting edge is the left edge of the parent element, for a top-to-bottom layout the starting edge is the top edge, and so on. Likewise, the ending edge of a child element is the right edge in a left-to-right layout, the bottom edge in a top-to-bottom layout, and so on.

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

-   [box-lines](/css/properties/box-lines)

-   [box-ordinal-group](/css/properties/box-ordinal-group)

-   [box-orient](/css/properties/box-orient)

-   **box-pack**

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

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

