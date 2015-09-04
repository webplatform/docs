---
title: links
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs summary, specs, and compat'
uri: dom/Document/links

---
# links

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Document](/dom/Document)</span></span>

## Syntax

``` {.js}
var result = element.links;
element.links = value;
```

## Examples

This example shows how to display the [**href**](/html/attributes/href) of the third link (Microsoft.com) defined in the document.

    <a href="http://yahoo.com">Yahoo.com</a>
    <a href="http://msn.com">MSN.com</a>
    <a href="http://microsoft.com">Microsoft.com</a>
    <script>
    alert(document.links[2].href);
    </script>

## Notes

### Remarks

For [**a**](/html/elements/a) objects to appear in the collection, they must have an [**href**](/html/attributes/href) attribute.

### Syntax

### Standards information

There are no standards that apply here.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

