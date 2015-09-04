---
title: removeProperty
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs example'
summary: 'Removes a property from a CSS style declaration.'
uri: css/cssom/CSSStyleDeclaration/removeProperty

---
# removeProperty

## Summary

Removes a property from a CSS style declaration.

*Method of [css/cssom/CSSStyleDeclaration/CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)*

## Syntax

``` {.js}
var value = declaration.removeProperty(property);
```

## Parameters

### property

 Data-typeÂ
:   String

 The name of the property to remove.

## Return Value

Returns an object of type String.

The value of the property if it is explicitly set for this declaration block, or null if the property is not explicitly set for this declaration block or if the property name does not correspond to a known CSS property.

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[DOM Level 2 Style](http://www.w3.org/TR/2000/REC-DOM-Level-2-Style-20001113/css.html)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

