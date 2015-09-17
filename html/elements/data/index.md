---
title: 'data'
compatibility:
  feature: data
  topic: html
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLDataElement](/dom/HTMLDataElement)'
standardization_status: 'W3C Recommendation'
summary: 'Annotates content with some machine-readable value.'
tags:
  - Markup_Elements
uri: html/elements/data

---
## Summary

Annotates content with some machine-readable value.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLDataElement](/dom/HTMLDataElement)

## Examples

Give an alternate representation of a value for humans, but embed the machine readable as an annotation.

``` html
<code><data value="9">Nine</data></code>
```

Represent an inventory item within a document, and hide within the markup the inventory code.

``` html
<code><data value="UPC:022014640201">North Coast Organic Apple Cider</data></code>
```

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/text-level-semantics.html#the-data-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/text-level-semantics.html#the-data-element)
:   W3C Recommendation

