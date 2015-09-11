---
title: grid-row-position
notes:
  - 'Add example, description, specifications, compatibility.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`1`'
  'Applies to': 'grid item elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: ''
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'In Progress'
summary: "Specifies a row position based upon an integer location, string value, or desired row size. \n"
tags:
  - CSS
  - Properties
uri: css/properties/grid-row-position

---
## <span>Summary</span>

Specifies a row position based upon an integer location, string value, or desired row size.

[css/properties/grid-row](/css/properties/grid-row) is used as short-hand for grid-row-position and grid-row-position

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `1`

Applies to
:   grid item elements

[Inherited](/css/concepts/inherited)
:   No

Media
:

[Computed value](/css/concepts/computed_value)
:

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## <span>Syntax</span>

-   `grid-row-position: auto`
-   `grid-row-position: integer`
-   `grid-row-position: span [integer] [string]`
-   `grid-row-position: string`

## <span>Values</span>

integer
:   Identifies the specified row.

span [integer] [string]
:   Places an item with contiguous space available to the \<integer\> value. Using the \<string\> value only considers lines with that name.

auto
:   Automatically places an item using the auto-placement algorithm.

string
:   Identifies the specified row.

**Needs Examples**: This section should include examples.

## <span>See also</span>

### <span>Related articles</span>

#### <span>Grid Layout</span>

-   [Responsive Web Design](/concepts/mobile_web/responsive_design)

-   [grid-auto-rows](/css/properties/grid-auto-rows)

-   [grid-column-position](/css/properties/grid-column-position)

-   [grid-column-span](/css/properties/grid-column-span)

-   [grid-definition-columns](/css/properties/grid-definition-columns)

-   [grid-definition-rows](/css/properties/grid-definition-rows)

-   **grid-row-position**

-   [height](/css/properties/height)
