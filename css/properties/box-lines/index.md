---
title: box-lines
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Add example, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`single`'
  'Applies to': 'box elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'In Progress'
standardization_status: Non-Standard
summary: "Do not use. This property has been replaced by the flex-wrap property.\n"
tags:
  - CSS
  - Properties
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - flex-wrap
uri: css/properties/box-lines

---
## <span>Summary</span>

Do not use. This property has been replaced by the flex-wrap property.

Gets or sets a value that specifies whether child elements wrap onto multiple lines or columns based on the space available in the object.

## <span>Overview table</span>

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
:

## <span>Syntax</span>

-   `box-lines: multiple`
-   `box-lines: single`

## <span>Values</span>

single
:   Default.

All child elements are displayed in a single row or column. The [**overflow**](/css/properties/overflow) property of the object determines whether the child elements are hidden, clipped, or scrollable.

multiple
:   Child elements are wrapped and displayed in successive, parallel rows or columns. The object expands in height or width, perpendicular to the axis defined by the [**-ms-box-orient**](/css/properties/ms-box-orient) property, to accommodate the additional rows or columns.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

Each child element is resized to its minimum width or height before the object is resized to accomodate additional rows or columns. Each successive rows is inserted below the previous row when [**-box-direction**](/css/properties/box-direction) is set to `normal` or above the previous row when **box-direction** is set to `reverse`. Each successive column is inserted to the right of the previous column when [**-box-direction**](/css/properties/box-direction) is set to `normal` or to the left of the previous column when **-ms-box-direction** is set to `reverse`.

## <span>Related specifications</span>

[Flexible Box Layout Module](http://www.w3.org/TR/2009/WD-css3-flexbox-20090723/)
:   W3C Working Draft (Obsolete)

## <span>See also</span>

### <span>Related articles</span>

#### <span>CSS Layout</span>

-   [Responsive Web Design](/concepts/mobile_web/responsive_design)

-   [@import](/css/atrules/@import)

-   [align-self](/css/properties/align-self)

-   [background](/css/properties/background)

-   [box-decoration-break](/css/properties/box-decoration-break)

-   [box-flex](/css/properties/box-flex)

-   **box-lines**

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

### <span>Related pages</span>

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `style`
