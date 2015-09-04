---
title: data
tags:
  - Markup
  - Elements
standardization_status: 'W3C Recommendation'
summary: 'Annotates content with some machine-readable value.'
uri: html/elements/data

---
# data

## Summary

Annotates content with some machine-readable value.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLDataElement](/dom/HTMLDataElement)

## Examples

Give an alternate representation of a value for humans, but embed the machine readable as an annotation.

``` {.html}
<data value="9">Nine</data>
```

Represent an inventory item within a document, and hide within the markup the inventory code.

``` {.html}
<data value="UPC:022014640201">North Coast Organic Apple Cider</data>
```

## Related specifications

Specification
:   Status
[HTML 5.1](http://www.w3.org/TR/html51/text-level-semantics.html#the-data-element)
:   W3C Working Draft
[HTML 5](http://www.w3.org/TR/html5/text-level-semantics.html#the-data-element)
:   W3C Recommendation

