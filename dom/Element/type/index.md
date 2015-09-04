---
title: type
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs summary, spec, and compat'
uri: dom/Element/type

---
# type

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Element](/dom/Element)</span></span>

## Syntax

``` {.js}
var result = element.type;
element.type = value;
```

## Examples

This example uses the **type** property to create an alert that indicates the type of object selected by the user. If the user clicks the mouse pointer on the text "Some text", the alert reads "Text". If the user clicks the mouse pointer on the space to the right of the text, the alert reads "None".

    <BODY onclick="alert(document.selection.type)">
    Some text.

## Notes

### Remarks

[Selection](/dom/Selection) is a child object of the [Document](/dom/Document) object.

### Syntax

## See also

### Related pages (MSDN)

-   `Selection`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

