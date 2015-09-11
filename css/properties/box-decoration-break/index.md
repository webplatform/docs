---
title: box-decoration-break
code_samples:
  - 'http://gist.github.com/6363867'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`slice`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Breaks a box into fragments creating new borders, padding and repeating backgrounds or lets it stay as a continuous box on a page break, column break, or, for inline elements, at a line break.'
tags:
  - CSS
  - Properties
uri: css/properties/box-decoration-break

---
## <span>Summary</span>

Breaks a box into fragments creating new borders, padding and repeating backgrounds or lets it stay as a continuous box on a page break, column break, or, for inline elements, at a line break.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `slice`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## <span>Syntax</span>

-   `box-decoration-break: clone`
-   `box-decoration-break: slice`

## <span>Values</span>

clone
:   Each box fragment is independently wrapped with the border and padding. The `border-radius` and `border-image` and `box-shadow`, if any, are applied to each fragment independently. The background is drawn independently in each fragment of the element. A no-repeat background image will thus be rendered once in each fragment of the element.

slice
:   No border and no padding are inserted at a break. No box-shadow is drawn at a broken edge; `border-radius` does not apply to its corners; and the `border-image` is rendered for the whole box as if it were unbroken. The effect is as though the element were rendered with no breaks present, and then sliced by the breaks afterward. Backgrounds are drawn as if, after the element has been laid out (including any justification, reordering, page breaks, etc.), all the element's box fragments were taken and put one after the other in visual order. The background is applied to the bounding box of this composite box and then the fragments are put back, with each with its share of the background.

## <span>Examples</span>

This is an example of CSS how you can use box-decoration-break for a given element `.clone` which is part of the element element with column breaks.

``` css
/**
 * box-decoration-break
 *
 * Please be aware that this demo uses prefix-free.js to
 * remove the hassle of adding vendor prefixes.
 * This is currently not working in any browser.
 */
.clone {
    /* Set some values to be cloned */
    background: #eee;
    border: 1px solid #aaa;
    padding: 5px;

    /* Clone the box */
    box-decoration-break: clone;
}

/* Creating a bunch of columns */
.box {
    column-count: 4;
    column-gap: 1em;
}
```

[View live example](http://code.webplatform.org/gist/6363867)

## <span>Usage</span>

     This property comes in handy if you want to indicate how a box splits when, for example a user prints a page.

When using CSS columns, grids or regions it is useful to decide how a box looks when it breaks.

## <span>Notes</span>

In Firefox there is `-moz-background-inline-policy` which enables you to treat background images how you want to. This is only a partial implementation of `box-decoration-break`.

## <span>Related specifications</span>

[CSS Level 3 - Backgrounds and Borders Module](http://www.w3.org/TR/css3-background/#box-decoration-break)
:   Candidate Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>CSS Layout</span>

-   [Responsive Web Design](/concepts/mobile_web/responsive_design)

-   [@import](/css/atrules/@import)

-   [align-self](/css/properties/align-self)

-   [background](/css/properties/background)

-   **box-decoration-break**

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

-   [grid-definition-rows](/css/properties/grid-definition-rows)

-   [height](/css/properties/height)

-   [max-width](/css/properties/max-width)

-   [user-modify](/css/properties/user-modify)

-   [baseline-shift](/svg/attributes/baseline-shift)

### <span>External resources</span>

-   [Documentation on -moz-background-inline-policy](https://developer.mozilla.org/en-US/docs/Web/CSS/-moz-background-inline-policy)
-   [The state of box-decoration-break by Lennart Schoors](http://bricss.net/post/24672339016/box-decoration-break-finally-coming-to-more-browsers)
