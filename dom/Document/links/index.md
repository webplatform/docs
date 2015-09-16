---
title: 'links'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, specs, and compat'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Document
    href: /dom/Document
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Document/links

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
var result = element.links;
element.links = value;
```

## Examples

This example shows how to display the [**href**](/html/attributes/href) of the third link (Microsoft.com) defined in the document.

``` html
<a href="http://yahoo.com">Yahoo.com</a>
<a href="http://msn.com">MSN.com</a>
<a href="http://microsoft.com">Microsoft.com</a>
<script>
alert(document.links[2].href);
</script>
```

## Notes

### Remarks

For [**a**](/html/elements/a) objects to appear in the collection, they must have an [**href**](/html/attributes/href) attribute.

### Syntax

### Standards information

There are no standards that apply here.
