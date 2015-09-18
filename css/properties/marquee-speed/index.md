---
title: 'marquee-speed'
code_samples:
  - 'http://code.webplatform.org/gist/6948165'
compatibility:
  feature: marquee-speed
  topic: css
notes:
  - 'This property seems to have been deprecated.'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`normal`'
  'Applies to': 'non-replaced block-level elements and non-replaced ’inline-block’ elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`marqueeSpeed`'
  Percentages: n/a
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The marquee-speed determines how fast the marquee content scrolls.'
tags:
  - CSS_Properties
  - CSS
uri: css/properties/marquee-speed

---
## Summary

The marquee-speed determines how fast the marquee content scrolls.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `normal`

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
:   `marqueeSpeed`

Percentages
:   n/a

## Syntax

-   `marquee-speed: fast`
-   `marquee-speed: normal`
-   `marquee-speed: slow`

## Values

slow
:   slower than normal

normal
:   faster than slow, slower than fast

fast
:   faster than normal

## Examples

A basic example on how to use marquee-speed.

``` css
h1 {
    overflow: auto;
    overflow-style: marquee-line;
    white-space: nowrap;
    width: 200px;
    marquee-speed: fast;
}
```

[View live example](http://code.webplatform.org/gist/6948165)

## Notes

The actual speed depends on the UA and the type of content.

## Related specifications

[CSS Marquee Module Level 3](http://www.w3.org/TR/css3-marquee/#marquee-speed)
:   Candidate Recommendation
