---
title: width
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: css/cssom/CSSStyleDeclaration/CSSStyleDeclaration
    href: /css/cssom/CSSStyleDeclaration/CSSStyleDeclaration
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /css/cssom/CSSStyleDeclaration/CSSStyleDeclaration
summary: 'Sets the width of an element.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: css/cssom/properties/width

---
## Summary

Sets the width of an element.

Property of [css/cssom/CSSStyleDeclaration/CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)

## Syntax

``` js
var result = declaration.width;
declaration.width = value;
```

## Return Value

Returns an object of type StringString

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The width of the rectangle can also be calculated by subtracting the value of the [**left**](/css/properties/left) property from the value of the [**right**](/css/properties/right) property.

### Standards information

-   [CSSOM View Module](http://go.microsoft.com/fwlink/p/?linkid=199793)
