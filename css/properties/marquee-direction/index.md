---
title: 'marquee-direction'
compatibility:
  feature: marquee-direction
  topic: css
notes:
  - "Add description, compatibility.\nThis property seems to have been deprecated. Once compatibility tables have been updated, consider a note talking about its usage."
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`forward`'
  'Applies to': 'non-replaced block-level elements and non-replaced ’inline-block’ elements'
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`marqueeDirection`'
  Percentages: n/a
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The marquee-direction determines the initial direction in which the marquee content moves.'
tags:
  - CSS
  - Properties
uri: css/properties/marquee-direction

---
## Summary

The marquee-direction determines the initial direction in which the marquee content moves.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `forward`

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
:   `marqueeDirection`

Percentages
:   n/a

## Syntax

-   `marquee-direction: forward`
-   `marquee-direction: reverse`

## Values

forward
:   moves the content in normal reading order

reverse
:   moves the content in reverse reading order

## Usage

     The actual direction depends the 'direction' and 'overflow-style', as follows:

`overflow-style: inline; direction: ltr;marquee-direction:forward;`
 animation direction: right-to-left

`overflow-style: inline; direction: ltr;marquee-direction:reverse;`
 animation direction: left-to-right

`overflow-style: inline; direction: rtl;marquee-direction:forward;`
 animation direction: left-to-right

`overflow-style: inline; direction: rtl;marquee-direction:reverse;`
 animation direction: right-to-left

`overflow-style: block;marquee-direction:forward;`
 animation direction: bottom-to-top

`overflow-style: block;marquee-direction:reverse;`
 animation direction: top-to-bottom

## Related specifications

[CSS Marquee Module Level 3](http://www.w3.org/TR/css3-marquee/#marquee-direction)
:   Candidate Recommendation
