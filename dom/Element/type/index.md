---
title: 'type'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, spec, and compat'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Element
    href: /dom/Element
tags:
  - API_Object_Properties
  - DOM
  - Needs_Summary
uri: dom/Element/type

---
Property of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## Syntax

``` js
var result = element.type;
element.type = value;
```

## Examples

This example uses the **type** property to create an alert that indicates the type of object selected by the user. If the user clicks the mouse pointer on the text "Some text", the alert reads "Text". If the user clicks the mouse pointer on the space to the right of the text, the alert reads "None".

``` html
<BODY onclick="alert(document.selection.type)">
Some text.
```

## Notes

### Remarks

[Selection](/dom/Selection) is a child object of the [Document](/dom/Document) object.

### Syntax

## See also

### Related pages

-   Selection[Selection](/dom/Selection)
