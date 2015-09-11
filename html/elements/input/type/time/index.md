---
title: time
notes:
  - 'Merge Candidate: html/attributes/type. Add note section.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLInputElement](/dom/HTMLInputElement)'
readiness: 'Not Ready'
standardization_status: 'W3C Candidate Recommendation'
summary: 'An input field for entering a specific time value.'
tags:
  - Markup
  - Elements
  - HTML
uri: html/elements/input/type/time

---
## <span>Summary</span>

An input field for entering a specific time value.

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [HTMLInputElement](/dom/HTMLInputElement)

## <span>Examples</span>

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

## <span>Notes</span>

On Safari Mobile for iOS, setting [`display`](/css/properties/display)`: block` on an **input** of **type="time"** causes the text within the **input** to become vertically misaligned.