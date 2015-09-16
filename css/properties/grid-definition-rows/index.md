---
title: grid-definition-rows
notes:
  - "Add description, compatibility.\nThis property is no longer listed in the W3C specification."
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`none`'
  'Applies to': 'grid container'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified, except for ‘auto’ (see prose)'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`gridDefinitionRows`'
  Percentages: n/a
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
summary: "This property can specify the length, a percentage of the grid container’s size, a measurement of the contents occupying the row, or a fraction of the free space in the grid. You can also specify a range using minmax(), which combines any of these measurements to define a min and max size for the row.\n"
tags:
  - CSS
  - Properties
uri: css/properties/grid-definition-rows

---
## Summary

This property can specify the length, a percentage of the grid container’s size, a measurement of the contents occupying the row, or a fraction of the free space in the grid. You can also specify a range using minmax(), which combines any of these measurements to define a min and max size for the row.

As well as referring to grid lines by their numerical index, you can also name lines. Names can make the grid-placement properties easier to understand and maintain. Lines can have multiple names, such as 'first' and 'header'.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `none`

Applies to
:   grid container

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified, except for ‘auto’ (see prose)

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `gridDefinitionRows`

Percentages
:   n/a

## Syntax

-   `grid-definition-rows: <track-list>`
-   `grid-definition-rows: none`

## Values

none
:   No initial grid; any rows are implicitly generated with their size determined by the ‘grid-auto-rows’ property.

\<track-list\>
:   The track-list syntax is:

\<track-list\> = [ \<string\>\* [ \<track-size\> | \<repeat-function\> ] ]+ \<string\>\*

\<track-size\> = minmax( \<track-breadth\> , \<track-breadth\> ) | auto | \<track-breadth\>

\<track-breadth\> = \<length\> | \<percentage\> | \<flex\> | min-content | max-content

Where the values are described as:

-   \<length\>
-   \<percentage\>: Percentage values are relative to the extent (logical height) of the grid container in grid row tracks. If the extent of the grid container is an indefinite size, \<percentage\> values relative to that size are treated as ‘auto’.
-   \<flex\>: A non-negative dimension with the unit "fr". Each \<flex\> value takes a share of the remaining space in proportion to its value. See Flexible Lengths for more details.
-   max-content: Largest max size contribution of the grid items occupying the grid track.
-   min-content: Largest min size contribution of the grid items occupying the grid track.
-   minmax(min, max): Defines a size range greater than or equal to min and less than or equal to max. If max \< min, then max is ignored and ‘minmax(min,max)’ is treated as min.
-   auto: Computes to ‘minmax(min-content, max-content)’.

## Examples

We define four values corresponding to each row of our grid. First row will be exactly 100 pixels, second row will use flex units and will take one 'fr' of the remaining space but because of the third row which takes up two 'fr'. That means the remaining space will divide on three, and second row will take 1/3 of this, and third row will take 2/3.

``` css
#myGrid {
  display: grid;
  grid-definitions-rows: 100px 1fr 2fr;
}
```

We define three rows where the first one will adapt to its content, the second will take 250 pixels of the screen and third one will take 50% of its container.

``` css
#myGrid {
  display: grid;
  grid-definitions-rows: auto 250px 50%
}
```

We can also make use of the min/max values. We define two rows where first one take one 'fr', and the second can use either the minimum content of its size, or the maximum value of 1fr. Notice that we gave names on right lines of each rows. That way we can refer to those lines when we define how space will take their contents.

``` css
#myGrid {
  display: grid;
  grid-definition-rows: 1fr "aside" minmax(min-content, 1fr) "main";
}
```

At last, \`repeat\` function can be used to create a repeating sequence.

``` css
#myGrid {
  display: grid;
  grid-definition-rows: repeat(3, 100px 1fr); // which equals to
  grid-definition-rows: 100px, 1fr, 100px, 1fr, 100px, 1fr;
}
```

## Related specifications

[CSS Grid Layout, Track Sizing: the ‘grid-definition-rows’ and ‘grid-definition-columns’ properties](http://dev.w3.org/csswg/css-grid/#track-sizing)
:   W3C Editor's Draft

[CSS Grid Layout, Track Sizing: the ‘grid-definition-rows’ and ‘grid-definition-columns’ properties](http://www.w3.org/TR/css3-grid-layout/#track-sizing)
:   W3C Working Draft

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

-   [box-orient](/css/properties/box-orient)

-   [box-pack](/css/properties/box-pack)

-   [box-shadow](/css/properties/box-shadow)

-   [break-before](/css/properties/break-before)

-   [flex-align](/css/properties/flex-align)

-   [flex-item-align](/css/properties/flex-item-align)

-   [flex-line-pack](/css/properties/flex-line-pack)

-   [grid-auto-rows](/css/properties/grid-auto-rows)

-   [grid-definition-columns](/css/properties/grid-definition-columns)

-   **grid-definition-rows**

-   [height](/css/properties/height)

-   [max-width](/css/properties/max-width)

-   [user-modify](/css/properties/user-modify)

-   [baseline-shift](/svg/attributes/baseline-shift)

#### Grid Layout

-   [Responsive Web Design](/concepts/mobile_web/responsive_design)

-   [grid-auto-rows](/css/properties/grid-auto-rows)

-   [grid-column-position](/css/properties/grid-column-position)

-   [grid-column-span](/css/properties/grid-column-span)

-   [grid-definition-columns](/css/properties/grid-definition-columns)

-   **grid-definition-rows**

-   [grid-row-position](/css/properties/grid-row-position)

-   [height](/css/properties/height)

### External resources

-   <http://css-tricks.com/almanac/properties/g/grid/>
