---
title: timeout
tags:
  - Events
readiness: 'Almost Ready'
notes:
  - 'Needs spec reference, standardization status'
summary: 'The ontimeout event occurs if the ontimeout period elapses before the onload event occurs.'
uri: apis/xhr/events/timeout

---
# timeout

## Summary

The ontimeout event occurs if the ontimeout period elapses before the onload event occurs.

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

Setting the **ontimeout** property.

``` {.js}
<script type="text/javascript">
function timeo()
{
    alert("XDR ontimeout");
}
...
xdr.ontimeout = timeo;
```

## Notes

### Remarks

The **ontimeout** event occurs if the **ontimeout** period elapses before the [**onload**](/apis/xhr/events/load) event occurs. When the **ontimeout** event occurs, the **responseText** property is unavailable and attempts to access it will raise an error. To invoke this event, do one of the following:

-   Event handlers are called as needed after a request is **sent**.

### Event handler parameters

This method has no parameters.

## See also

### Related pages (MSDN)

-   `XDomainRequest`
-   `XMLHttpRequest`
-   `XMLHttpRequest Enhancements in Internet Explorer 8`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

