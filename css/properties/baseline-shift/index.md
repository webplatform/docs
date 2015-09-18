---
title: 'baseline-shift'
code_samples:
  - 'http://code.webplatform.org/gist/7001747'
compatibility:
  feature: baseline-shift
  topic: css
notes:
  - 'Obsolete; deletion candidate'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`baseline`'
  'Applies to': 'inline-level elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'see text'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'Not Ready'
standardization_status: 'W3C Working Draft'
summary: 'Obsolete - spec retired, not implemented.'
tags:
  - CSS_Properties
uri: css/properties/baseline-shift

---
## Summary

Obsolete - spec retired, not implemented.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `baseline`

Applies to
:   inline-level elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   see text

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## Syntax

-   `baseline-shift: <length>`
-   `baseline-shift: <percentage>`
-   `baseline-shift: baseline`
-   `baseline-shift: sub`
-   `baseline-shift: super`

## Values

baseline
:   There is no baseline shift; the dominant baseline remains in its original position.

sub
:   The dominant baseline is shifted to the default position for subscripts. The offset for this position is determined by the font data for the parent nominal font as adjusted by the dominant baseline-table font-size of the parent element. If there is no applicable font data the User Agent may use heuristic to determine the offset.

super
:   The dominant baseline is shifted to the default position for superscripts. The offset for this position is determined by the font data for the parent nominal font as adjusted by the dominant baseline-table font-size of the parent element. If there is no applicable font data the User Agent may use heuristic to determine the offset.

\<percentage\>
:   The computed value of the property is this percentage multiplied by the computed 'line-height' of the parent element. The dominant-baseline is shifted in the shift-direction (positive value) or opposite to the shift-direction (negative value) of the parent area by the computed value. A value of '0%' is equivalent to 'baseline'.

\<length\>
:   The dominant-baseline is shifted in the shift-direction (positive value) or opposite to the shift-direction (negative value) of the parent area by the \<length\> value. A value of '0cm' is equivalent to 'baseline'.

## Examples

This property works with HTML inline-level elements.

``` html
 I really love Webplatform.docs 
```

[View live example](http://code.webplatform.org/gist/7001747)

In this sample, baseline-shift has the value 'baseline' which is the initial value, keeping the baseline in its original position.

``` css
span {
    baseline-shift: baseline;
}
```

In this sample, the baseline-shift has the value 'sub', putting the text in the subscript position.

``` css
span {
    baseline-shift: sub;
}
```

In this sample, the baseline-shift has the value 'super', putting the text in the superscript position.

``` css
span {
    baseline-shift: super;
}
```

This sample show that it's possible to use this property with percentage values.

``` css
/* Percentage values are composed by a number and the '%' symbol */
/* A value of '0%' is equivalent to 'baseline' */
span {
    baseline-shift: 10%;
}
```

Also, it's possible to use length units as values for the 'baseline-shift' property, as shown the next sample.

``` css
/* Length values are composed by a number and the unit symbol (e. g., 'px', 'em', 'cm', etc) */
span {
    baseline-shift: 2em;
}
```

## Notes

Although it may seem that 'baseline-shift' and 'alignment-adjust' properties are doing the same thing, there are important differences. For 'alignment-adjust' the percentage values refer to the 'line-height' of the element being aligned. For 'baseline-shift the percentage values refer to the 'line-height' of the parent element. Similarly, it is the 'sub' and 'super' offsets of the parent that are used to align the shifted baseline rather than the 'sub' and 'super' offsets of the element being positioned. To ensure a consistent sub- or superscript position, it makes more sense to use the parent as the reference rather than the subscript element which may have a changed "line-height" due to "font-size" changes in the sub- or superscript element. Using the "alignment-adjust" property is more suitable for positioning elements, such as graphics, that have no internal textual structure. Using the "baseline-shift" property is intended for sub- and superscripts where the positioned element may itself be textual. The baseline-shift provides a way to define a specific baseline offset other than the named offsets that are defined relative to the dominant-baseline. In addition, having "baseline-shift" makes it easier for a tool to generate the relevant properties; many formatting programs already have a notion of baseline shift.

## Related specifications

[CSS3 module: line](http://www.w3.org/TR/css3-linebox/#baseline-shift)
:   Obsoleted (Working Draft)

