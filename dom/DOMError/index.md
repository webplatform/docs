---
title: DOMError
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs spec reference'
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
summary: 'Represents a DOM operation error object.'
tags:
  - API
  - Objects
  - DOM
uri: dom/DOMError

---
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

### Related pages

-   `DOMException`
-   `DOM Error Codes`
