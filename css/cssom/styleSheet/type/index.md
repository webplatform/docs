---
title: 'type'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/styleSheet
    href: /css/cssom/styleSheet
summary: 'The type of a document''s stylesheet.'
tags:
  - API_Object_Properties
  - DOM
  - Needs_Examples
uri: css/cssom/styleSheet/type

---
## Summary

The type of a document's stylesheet.

Property of [css/cssom/styleSheet](/css/cssom/styleSheet)[css/cssom/styleSheet](/css/cssom/styleSheet)

## Syntax

``` js
var result = element.type;
element.type = value;
```

## Notes

### Remarks

This property can be any string, including an empty string. Style sheets having any type other than "text/css" are not supported for Microsoft Internet Explorer 4.0. This property can be any string, including an empty string.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5

## See also

### Related pages

-   styleSheet[styleSheet](/css/cssom/styleSheet)
