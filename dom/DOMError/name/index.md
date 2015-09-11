---
title: name
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs spec reference'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/DOMError
    href: /dom/DOMError
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/DOMError
standardization_status: 'W3C Working Draft'
summary: 'Returns the name of an error that occurred during a DOM operation.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/DOMError/name

---
## <span>Summary</span>

Returns the name of an error that occurred during a DOM operation.

Property of [dom/DOMError](/dom/DOMError)[dom/DOMError](/dom/DOMError)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var errorName = error.name;
```

## <span>Return Value</span>

Returns an object of type StringString

The name associated with an error.

## <span>Examples</span>

``` js
function getErrorName(e) {
//retrieve name text for DOMError
var errorName = e.name;
return errorName;
}
```

