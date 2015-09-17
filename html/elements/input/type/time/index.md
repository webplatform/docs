---
title: 'time'
compatibility:
  feature: time
  topic: html
notes:
  - 'Merge Candidate: html/attributes/type. Add note section.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLInputElement](/dom/HTMLInputElement)'
readiness: 'Not Ready'
standardization_status: 'W3C Candidate Recommendation'
summary: 'An input field for entering a specific time value.'
tags:
  - Markup_Elements
  - HTML
uri: html/elements/input/type/time

---
## Summary

An input field for entering a specific time value.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLInputElement](/dom/HTMLInputElement)

## Examples

Basic usage. Accepts no seconds.

``` html
<input type="time" value="09:00" min="09:00" max="17:00">
```

Accepts seconds.

``` html
<input type="time" step="1">
```

Accepts only hours.

``` html
<input type="time" step="3600">
```

## Notes

On Safari Mobile for iOS, setting [`display`](/css/properties/display)`: block` on an **input** of **type="time"** causes the text within the **input** to become vertically misaligned.
