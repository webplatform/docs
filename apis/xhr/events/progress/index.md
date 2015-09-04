---
title: progress
tags:
  - Events
readiness: 'Almost Ready'
notes:
  - 'Needs spec reference, standardization status'
summary: "When the onprogress event occurs, \npartial data can be retrieved using responseText.\n"
uri: apis/xhr/events/progress

---
# progress

## Summary

When the onprogress event occurs, partial data can be retrieved using responseText.

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

Setting the **onprogress** property.

``` {.js}
function progres()
{
    alert("XDR onprogress");
    alert("Got: " + xdr.responseText);
}
...
xdr.onprogress = progres;
```

## Notes

### Remarks

When the **onprogress** event occurs, partial data can be retrieved using **responseText**. The onprogress event may occur 0, 1 or many times in the time interval between the [**onload**](/apis/xhr/events/load) event. To invoke this event, do one of the following:

-   Event handlers are called as needed after a request is **sent**.

### Event handler parameters

This method has no parameters.

## See also

### Related pages (MSDN)

-   `XDomainRequest`
-   `XMLHttpRequest Enhancements in Internet Explorer 8`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

