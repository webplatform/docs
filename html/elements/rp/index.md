---
title: 'rp'
compatibility:
  feature: rp
  topic: html
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLElement](/dom/HTMLElement)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Used to provide fallback text to be shown by user agents that don''t support ruby annotations'
tags:
  - Markup
  - Elements
uri: html/elements/rp

---
## Summary

Used to provide fallback text to be shown by user agents that don't support ruby annotations

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLElement](/dom/HTMLElement)

## Examples

The example above, in which each ideograph in the text 漢字 is annotated with its phonetic reading, could be expanded to use rp so that in legacy user agents the readings are in parentheses

``` html

<p lang="ja" xml:lang="ja">
...
<ruby>
 漢 <rp>(</rp><rt>かん</rt><rp>)</rp>
 字 <rp>(</rp><rt>じ</rt><rp>)</rp>
</ruby>
...
</p>

```

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/text-level-semantics.html#the-rp-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/text-level-semantics.html#the-rp-element)
:   W3C Recommendation

