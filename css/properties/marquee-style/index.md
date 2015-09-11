---
title: marquee-style
code_samples:
  - 'http://gist.github.com/6364703'
notes:
  - "Add description and compatibility.\nAccording to W3C specifications, this property should apply to all elements that accept the overflow property. However, it currently only works with the marquee tag. Perhaps this property has been deprecated."
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`scroll`'
  'Applies to': 'non-replaced block-level elements, table cells, and inline-block elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`marqueeStyle`'
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The ''marquee-style'' property determines a marquee''s scrolling behavior.'
tags:
  - CSS
  - Properties
uri: css/properties/marquee-style

---
## <span>Summary</span>

The 'marquee-style' property determines a marquee's scrolling behavior.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `scroll`

Applies to
:   non-replaced block-level elements, table cells, and inline-block elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `marqueeStyle`

## <span>Syntax</span>

-   `marquee-style: alternate`
-   `marquee-style: scroll`
-   `marquee-style: slide`

## <span>Values</span>

scroll
:   Start completely off one side, scroll all the way across and completely off.

slide
:   Start completely off one side, scroll in, and stop as soon as no more content is off that side.

alternate
:   Bounce back and forth.

## <span>Examples</span>

``` css
.scroll { marquee-style: scroll; }
.slide { marquee-style: slide; }
.alternate { marquee-style: alternate; }
```

[View live example](http://code.webplatform.org/gist/6364703)

``` html
<marquee class="scroll">This demonstrates the 'scroll' value of the 'marquee-style' property.</marquee>
<marquee class="slide">This demonstrates the 'slide' value of the 'marquee-style' property.</marquee>
<marquee class="alternate">This demonstrates the 'alternate' value of the 'marquee-style' property.</marquee>
```

## <span>Related specifications</span>

[CSS Marquee Module Level 3](http://www.w3.org/TR/css3-marquee/)
:   W3C Candidate Recommendation

