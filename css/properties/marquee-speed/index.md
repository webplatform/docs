---
title: marquee-speed
code_samples:
  - 'http://gist.github.com/6948165'
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
  - CSS
  - Properties
uri: css/properties/marquee-speed

---
## <span>Summary</span>

The marquee-speed determines how fast the marquee content scrolls.

## <span>Overview table</span>

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

## <span>Syntax</span>

-   `marquee-speed: fast`
-   `marquee-speed: normal`
-   `marquee-speed: slow`

## <span>Values</span>

slow
:   slower than normal

normal
:   faster than slow, slower than fast

fast
:   faster than normal

## <span>Examples</span>

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

## <span>Notes</span>

The actual speed depends on the UA and the type of content.

## <span>Related specifications</span>

[CSS Marquee Module Level 3](http://www.w3.org/TR/css3-marquee/#marquee-speed)
:   Candidate Recommendation
