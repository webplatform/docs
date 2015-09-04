---
title: DOMError
tags:
  - API
  - Objects
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs spec reference'
summary: 'Represents a DOM operation error object.'
uri: dom/DOMError

---
# DOMError

## Summary

Represents a DOM operation error object.

## Properties

API Name
:   Summary
[message](/dom/DOMError/message)
:   Returns the message associated with an error that occurred during a DOM operation.
[name](/dom/DOMError/name)
:   Returns the name of an error that occurred during a DOM operation.

## Methods

*No methods.*

## Events

*No events.*

## Notes

While similar to [**DOMException**](/dom/DOMException) objects, **DOMError** objects represent errors that are generated through other means, such as return values. (**DOMException** objects are thrown as exceptions.) Both objects return similar values, so it is possible to create general handlers to respond to either type of error.

## See also

### Related pages (MSDN)

-   `DOMException`
-   `DOM Error Codes`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

