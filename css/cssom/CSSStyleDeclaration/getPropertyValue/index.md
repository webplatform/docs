---
title: 'getPropertyValue'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs example'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: css/cssom/CSSStyleDeclaration/CSSStyleDeclaration
    href: /css/cssom/CSSStyleDeclaration/CSSStyleDeclaration
  return_type:
    predicate: 'Returns an object of type  '
    value: String
    href: /css/cssom/CSSStyleDeclaration/CSSStyleDeclaration
standardization_status: 'W3C Recommendation'
summary: 'Gets the value of a property in a CSS style declaration.'
tags:
  - API_Object_Methods
  - DOM
  - Needs_Examples
uri: css/cssom/CSSStyleDeclaration/getPropertyValue

---
## Summary

Gets the value of a property in a CSS style declaration.

Method of [css/cssom/CSSStyleDeclaration/CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)

## Syntax

``` js
var value = declaration.getPropertyValue(property);
```

## Parameters

### property

 Data-type
:   String

 The name of the property.

## Return Value

Returns an object of type StringString

The value of the property if it is explicitly set for this declaration block, or null.

## Related specifications

[DOM Level 2 Style](http://www.w3.org/TR/2000/REC-DOM-Level-2-Style-20001113/css.html)
:   Recommendation
