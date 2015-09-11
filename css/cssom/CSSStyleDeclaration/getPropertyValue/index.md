---
title: getPropertyValue
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
  - API
  - Object
  - Methods
  - DOM
uri: css/cssom/CSSStyleDeclaration/getPropertyValue

---
## <span>Summary</span>

Gets the value of a property in a CSS style declaration.

Method of [css/cssom/CSSStyleDeclaration/CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)

## <span>Syntax</span>

``` js
var value = declaration.getPropertyValue(property);
```

## <span>Parameters</span>

### <span>property</span>

 Data-type
:   String

 The name of the property.

## <span>Return Value</span>

Returns an object of type StringString

The value of the property if it is explicitly set for this declaration block, or null.

**Needs Examples**: This section should include examples.

## <span>Related specifications</span>

[DOM Level 2 Style](http://www.w3.org/TR/2000/REC-DOM-Level-2-Style-20001113/css.html)
:   Recommendation
