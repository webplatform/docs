---
title: alignment-adjust
tags:
  - CSS
  - Properties
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'This property allows precise alignment of elements, such as graphics, that do not have a baseline-table or lack the desired baseline in their baseline-table. With the alignment-adjust property, the position of the baseline identified by the alignment-baseline can be explicitly determined. It also determines precisely the alignment point for each glyph within a textual element.'
code_samples:
  - 'http://gist.github.com/6363838'
uri: css/properties/alignment-adjust

---
# alignment-adjust

## Summary

This property allows precise alignment of elements, such as graphics, that do not have a baseline-table or lack the desired baseline in their baseline-table. With the alignment-adjust property, the position of the baseline identified by the alignment-baseline can be explicitly determined. It also determines precisely the alignment point for each glyph within a textual element.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `auto`
Applies to
:   Inline-level elements
[Inherited](/css/concepts/inherited)
:   No
Media
:   visual
[Computed value](/css/concepts/computed_value)
:   As specified
Animatable
:   No
[CSS Object Model Property](/css/concepts/cssom)
:   ``
Percentages
:   Refers to the line-height of the element

## Syntax

-   `alignment-adjust: <length>`
-   `alignment-adjust: <percentage>`
-   `alignment-adjust: after-edge`
-   `alignment-adjust: alphabetic`
-   `alignment-adjust: auto`
-   `alignment-adjust: baseline`
-   `alignment-adjust: before-edge`
-   `alignment-adjust: central`
-   `alignment-adjust: hanging`
-   `alignment-adjust: ideographic`
-   `alignment-adjust: mathematical`
-   `alignment-adjust: middle`
-   `alignment-adjust: text-after-edge`
-   `alignment-adjust: text-before-edge`

## Values

auto
:   For each glyph corresponding to textual information within the element, the alignment-point is the intersection of the start-edge of the glyph box and the block-progression-direction position of the alignment point from the font. Padding, border or margin do not affect that alignment point. The alignment point of the inline-level element itself is at the intersection of the start-edge of the first inline box and the baseline identified by the ‘alignment-baseline’ property, if this baseline exists in the baseline-table for the element dominant-baseline. If that specific baseline does not exist, the user agent may use heuristics to determine where the missing baseline would be.

baseline
:   The alignment point is at the intersection of the start-edge of the element and the dominant-baseline of the element.

before-edge
:   The alignment point is at the intersection of the start-edge of the element and the before-edge of the extended inline box of the element. This may include or not the line-height of the element, depending on the line-stacking-strategy.

text-before-edge
:   The alignment point is at the intersection of the start-edge of the element and the text-before-edge baseline of the element.

central
:   The alignment point is at the intersection of the start-edge of the element and the central baseline of the element.

middle
:   The alignment point is at the intersection of the start-edge of the element and the middle baseline of the element.

after-edge
:   The alignment point is at the intersection of the start-edge of the element and the after-edge of the extended inline box of the element. This may include or not the line-height of the element, depending on the line-stacking-strategy.

text-after-edge
:   The alignment point is at the intersection of the start-edge of the element and the text-after-edge baseline of the element.

ideographic
:   The alignment point is at the intersection of the start-edge of the element and the ideographic baseline of the element.

alphabetic
:   The alignment point is at the intersection of the start-edge of the element and the alphabetic baseline of the element.

hanging
:   The alignment point is at the intersection of the start-edge of the element and the hanging baseline of the element.

mathematical
:   The alignment point is at the intersection of the start-edge of the element and the mathematical baseline of the element.

\<percentage\>
:   The computed value of the property is this percentage multiplied by the computed line-height of the element. The alignment point is on the start-edge of the inline box. Its position along the start-edge relative to the intersection of the dominant-baseline and the start-edge is offset by the computed value. The offset is opposite to the shift-direction (positive value) or in the shift-direction (negative value). A value of "0%" makes the dominant-baseline the alignment point.

\<length\>
:   The alignment-point is on the start-edge of the inline box. Its position along the start-edge relative to the intersection of the dominant-baseline and the start-edge is offset by the length value. The offset is opposite to the shift-direction (positive value) or in the shift-direction (negative value). A value of "0cm" makes the dominant-baseline the alignment point.

## Examples

``` {.html}
<p>
    alignment-adjust CSS property:
    <img src="http://placehold.it/40x40%22 alt="Image 1" class="image1">
    <img src="http://placehold.it/40x40%22 alt="Image 2" class="image2">
    <img src="http://placehold.it/40x40%22 alt="Image 3" class="image3">
    <img src="http://placehold.it/40x40%22 alt="Image 4" class="image4">
    <img src="http://placehold.it/40x40%22 alt="Image 5" class="image5">
    <img src="http://placehold.it/40x40%22 alt="Image 6" class="image6">
    <img src="http://placehold.it/40x40%22 alt="Image 7" class="image7">
    <img src="http://placehold.it/40x40%22 alt="Image 8" class="image8">
    <img src="http://placehold.it/40x40%22 alt="Image 9" class="image9">
    <img src="http://placehold.it/40x40%22 alt="Image 10" class="image10">
    <img src="http://placehold.it/40x40%22 alt="Image 11" class="image11">
    <img src="http://placehold.it/40x40%22 alt="Image 12" class="image12">
    <img src="http://placehold.it/40x40%22 alt="Image 13" class="image13">
    <img src="http://placehold.it/40x40%22 alt="Image 14" class="image14">
</p>
```

[View live example](http://code.webplatform.org/gist/6363838)

``` {.css}
/**
 * alignment-adjust
 * CSS3 property
 * http://docs.webplatform.org/wiki/css/properties/alignment-adjust
 */

p {
    border: 1px dotted #ddd;
    color: #222;
    font: 1em/5em 'Open Sans', sans-serif;
    padding: 0.5em;
}

p img {
    vertical-align: middle;
}

p img:first-child {
    margin-left: 1em;
}

.image1 { alignment-adjust: auto; }
.image2 { alignment-adjust: baseline; }
.image3 { alignment-adjust: before-edge; }
.image4 { alignment-adjust: text-before-edge; }
.image5 { alignment-adjust: central; }
.image6 { alignment-adjust: middle; }
.image7 { alignment-adjust: after-edge; }
.image8 { alignment-adjust: text-after-edge; }
.image9 { alignment-adjust: ideographic; }
.image10 { alignment-adjust: alphabetic; }
.image11 { alignment-adjust: hanging; }
.image12 { alignment-adjust: mathematical; }
.image13 { alignment-adjust: 75%; }
.image14 { alignment-adjust: -20px; }
```

## Related specifications

Specification
:   Status
[CSS Line Layout Module](http://dev.w3.org/csswg/css-inline/)
:   W3C Editor's Draft

## See also

### External resources

-   [alignment-adjust by Eric Meyer](http://meyerweb.com/eric/css/tests/css3/show.php?p=alignment-adjust)

