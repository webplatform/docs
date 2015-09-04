---
title: message
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Retrieves a string describing the exception that occurred.'
uri: dom/DOMException/message

---
# message

## Summary

Retrieves a string describing the exception that occurred.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/DOMException](/dom/DOMException)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var exceptionMessage = exception.message;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

A short description of the exception.

## Examples

``` {.js}
function getExceptionMsg(e) {
//retrieve text for DOMException
var exceptionMsg = e.message;
return exceptionMsg;
}
```

## Related specifications

Specification
:   Status
[DOM Level 2 Core](http://www.w3.org/TR/DOM-Level-2-Core/)
:   Recommendation

## See also

### Related pages (MSDN)

-   `RangeException`
-   `EventException`
-   `code`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

