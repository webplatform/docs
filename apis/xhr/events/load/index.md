---
title: load
tags:
  - Events
readiness: 'Almost Ready'
notes:
  - 'Needs spec reference, standardization status'
summary: "After the onload event has occurred,\nresponseText contains the complete server response.\n"
uri: apis/xhr/events/load

---
# load

## Summary

After the onload event has occurred, responseText contains the complete server response.

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

Setting the **onload** property.

``` {.js}
function loadd()
{
    alert("XDR onload");
    alert("Got: " + xdr.responseText);
}
...
xdr.onload = loadd;
```

## Notes

### Remarks

After the **onload** event has occurred, **responseText** contains the complete server response. To invoke this event, do one of the following:

-   Event handlers are called as needed after a request is **sent**.

### Event handler parameters

This method has no parameters.

## See also

### Related pages (MSDN)

-   `XDomainRequest`
-   `Reference`
-   `onprogress`
-   `Conceptual`
-   `XMLHttpRequest Enhancements in Internet Explorer 8`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

