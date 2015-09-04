---
title: error
tags:
  - Events
  - API
readiness: 'Almost Ready'
notes:
  - 'Needs spec reference, standardization status'
summary: 'The onerror event occurs when the request could not be completed because of an error.'
uri: apis/xhr/events/error

---
# error

## Summary

The onerror event occurs when the request could not be completed because of an error.

## Overview Table

Synchronous
:   No
Bubbles
:   No
Target
:   dom/Element
Cancelable
:   No
Default action
:

## Examples

Setting the onerror property.

``` {.js}
<script type="text/javascript">
function err()
{
    alert("XDR onerror");
}
...
xdr.onerror = err;
```

## Notes

### Remarks

The document can respond to the error, but there is no way to determine the cause or nature of the error. The **onerror** event does not occur when the [**ontimeout**](/apis/xhr/events/timeout) event occurs. To invoke this event, do one of the following:

-   Cannot invoke.

### Event handler parameters

This method has no parameters.

## See also

### Related pages (MSDN)

-   `XDomainRequest`
-   `Reference`
-   `onload`
-   `onprogress`
-   `Conceptual`
-   `XMLHttpRequest Enhancements in Internet Explorer 8`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

