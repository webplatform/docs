---
title: 'order'
code_samples:
  - 'http://gist.github.com/4741023'
compatibility:
  feature: order
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0`'
  'Applies to': 'flex items and absolutely-positioned flex container children'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'specified value'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`order`'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The order property controls the order in which flex items appear within their flex container, by assigning them to ordinal groups.'
tags:
  0: CSS
  1: Properties
  3: Flexbox
uri: css/properties/order

---
## Summary

The order property controls the order in which flex items appear within their flex container, by assigning them to ordinal groups.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `0`

Applies to
:   flex items and absolutely-positioned flex container children

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   specified value

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `order`

## Syntax

-   `flex-order: integer`
-   `order: <integer>`

## Values

\<integer\>
:   The ordinal group for this flex item.

## Examples

Displaying children in custom sequence

``` css
.list {
  display: flex;
}
.list div {
  flex: 1;
}
.list .first {
  order: 3;
}
.list .second {
  order: 1;
}
.list .third {
  order: 2;
}
```

[View live example](http://code.webplatform.org/gist/4741023)

The Holy Grail Layout example. Given a source order of article-nav-aside, use order to rearrange these elements as flex items into nav-article-aside

``` css
article { order: 2; }
nav { order: 1; }
aside { order: 3; }
```

## Notes

This property was previously named **flex-order** in earlier drafts.

## Related specifications

[CSS Flexible Box Layout Module](http://www.w3.org/TR/css3-flexbox/#order-property)
:   Candidate Recommendation
