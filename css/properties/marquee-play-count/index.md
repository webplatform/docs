---
title: marquee-play-count
code_samples:
  - 'http://gist.github.com/6948452'
notes:
  - 'This property seems to have been deprecated.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`1`'
  'Applies to': 'non-replaced block-level elements and non-replaced ’inline-block’ elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`marqueePlayCount`'
  Percentages: n/a
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'This property specifies how many times the marquee content moves.'
tags:
  - CSS
  - Properties
uri: css/properties/marquee-play-count

---
## Summary

This property specifies how many times the marquee content moves.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `1`

Applies to
:   non-replaced block-level elements and non-replaced ’inline-block’ elements

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `marqueePlayCount`

Percentages
:   n/a

## Syntax

-   `marquee-play-count: <non-negative-integer>`
-   `marquee-play-count: infinite`

## Values

\<non-negative-integer\>
:   Any value of 0 and higher. If the value is greater than 16, the UA may stop after 16 loops.

infinite
:   An infinite loop. The UA may stop after 16 loops.

## Examples

``` css
h1 {
    overflow: auto;
    overflow-style: marquee-line;
    white-space: nowrap;
    width: 200px;
    marquee-play-count: 2;
}
```

[View live example](http://code.webplatform.org/gist/6948452)

## Usage

     If marquee-play-count changes because of a state change (e.g. on hover), the loop counter will reset of the computed value differs:

For example:

     h1 { marquee-play-count: 2; }
     h1:hover { marquee-play-count: 4;}

Now, the `h1` loops 2 times, until you hover over it. Then the loop counter will reset and it loops for 4 times. If you than leave the element, it resets again and it will loop 2 times.

## Related specifications

[CSS Marquee Module Level 3](http://www.w3.org/TR/css3-marquee/#the-marquee-play-count)
:   Candidate Recommendation
