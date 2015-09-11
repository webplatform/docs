---
title: message
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/DOMException
    href: /dom/DOMException
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/DOMException
standardization_status: 'W3C Recommendation'
summary: 'Retrieves a string describing the exception that occurred.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/DOMException/message

---
## <span>Summary</span>

Retrieves a string describing the exception that occurred.

Property of [dom/DOMException](/dom/DOMException)[dom/DOMException](/dom/DOMException)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var exceptionMessage = exception.message;
```

## <span>Return Value</span>

Returns an object of type StringString

A short description of the exception.

## <span>Examples</span>

``` js
function getExceptionMsg(e) {
//retrieve text for DOMException
var exceptionMsg = e.message;
return exceptionMsg;
}
```

## <span>Related specifications</span>

[DOM Level 2 Core](http://www.w3.org/TR/DOM-Level-2-Core/)
:   Recommendation

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `RangeException`
-   `EventException`
-   `code`
